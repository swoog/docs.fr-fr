---
title: Conception de la couche de persistance de l’infrastructure
description: Architecture des microservices .NET pour les applications .NET en conteneur | Conception de la couche de persistance de l’infrastructure
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/08/2017
ms.openlocfilehash: 9da1020ac5b43971a8f976c518f4537bec866c26
ms.sourcegitcommit: 979597cd8055534b63d2c6ee8322938a27d0c87b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37105844"
---
# <a name="designing-the-infrastructure-persistence-layer"></a>Conception de la couche de persistance de l’infrastructure

Les composants de persistance des données fournissent l’accès aux données hébergées dans les limites d’un microservice (autrement dit, la base de données d’un microservice). Ils contiennent l’implémentation réelle des composants tels que les dépôts et les classes d’[unité de travail](https://martinfowler.com/eaaCatalog/unitOfWork.html), comme les DBContexts EF personnalisés.

## <a name="the-repository-pattern"></a>Le modèle Dépôt

Les dépôts sont des classes ou composants qui encapsulent la logique nécessaire pour accéder aux sources de données. Ils centralisent les fonctionnalités d’accès aux données communes, en fournissant une meilleure maintenabilité et en découplant l’infrastructure ou la technologie utilisée pour accéder aux bases de données à partir de la couche du modèle de domaine. Si vous utilisez un ORM comme Entity Framework, le code à implémenter est simplifié grâce à LINQ et à un typage fort. Ainsi, vous pouvez vous concentrer sur la logique de persistance des données plutôt que sur le raccordement de l’accès aux données.

Le modèle Dépôt est une façon bien décrite d’utiliser une source de données. Dans l’ouvrage [Patterns of Enterprise Application Architecture](https://www.amazon.com/Patterns-Enterprise-Application-Architecture-Martin/dp/0321127420/), Martin Fowler décrit un dépôt comme suit :

Un dépôt effectue les tâches d’un intermédiaire entre les couches du modèle de domaine et le mappage de données, en agissant d’une manière similaire à un ensemble d’objets de domaine dans la mémoire. Les objets clients génèrent des requêtes de façon déclarative et les envoient aux dépôts pour obtenir des réponses. D’un point de vue conceptuel, un dépôt encapsule un ensemble d’objets stockés dans la base de données et les opérations pouvant être effectuées sur ces derniers, en fournissant un moyen plus proche de la couche de persistance. Les dépôts, par ailleurs, prennent en charge l’objectif de séparation, claire et dans un seul sens, de la dépendance entre le domaine de travail et l’allocation ou le mappage de données.

### <a name="define-one-repository-per-aggregate"></a>Définir un seul dépôt par agrégat

Pour chaque agrégat ou racine d’agrégat, vous devez créer une seule classe de dépôt. Dans un microservice basé sur des modèles de conception pilotée par le domaine (DDD, Domain-Driver Design), le seul canal que vous devez utiliser pour mettre à jour la base de données doit être les dépôts. En effet, ils ont une relation un-à-un avec la racine d’agrégat, qui contrôle les invariants et la cohérence transactionnelle de l’agrégat. Il est possible d’interroger la base de données par le biais d’autres canaux (selon une approche CQRS par exemple), car les requêtes ne changent pas l’état de la base de données. Toutefois, la zone transactionnelle (les mises à jour) doit toujours être contrôlée par les dépôts et les racines d’agrégat.

En bref, un dépôt vous permet de renseigner les données en mémoire provenant de la base de données sous la forme d’entités de domaine. Une fois que les entités sont en mémoire, elles peuvent être modifiées et de nouveau rendues persistantes dans la base de données par le biais de transactions.

Comme indiqué précédemment, si vous utilisez le modèle architectural CQS/CQRS, les requêtes initiales sont effectuées par des requêtes latérales en dehors du modèle de domaine, effectuées par de simples instructions SQL à l’aide de Dapper. Cette approche est beaucoup plus souple que les dépôts, car vous pouvez interroger et joindre les tables dont vous avez besoin, et ces requêtes ne sont pas limitées par des règles issues des agrégats. Ces données accèdent à la couche présentation ou à l’application cliente.

Si l’utilisateur apporte des modifications, les données à mettre à jour passent de l’application cliente ou de la couche présentation à la couche Application (comme un service API web). Quand vous recevez une commande (avec des données) dans un gestionnaire de commandes, vous utilisez des dépôts pour obtenir les données à mettre à jour à partir de la base de données. Vous les mettez à jour dans la mémoire avec les informations passées avec les commandes, puis vous ajoutez ou mettez à jour les données (entités de domaine) dans la base de données par le biais d’une transaction.

N’oubliez pas qu’un seul dépôt doit être défini pour chaque racine d’agrégat, comme l’illustre la figure 9-17. Pour atteindre l’objectif de la racine d’agrégat visant à maintenir la cohérence transactionnelle entre tous les objets au sein de l’agrégat, vous ne devez jamais créer un dépôt pour chaque table dans la base de données.

![](./media/image18.png)

**Figure 9-17**. Relation entre les dépôts, les agrégats et les tables de base de données

### <a name="enforcing-one-aggregate-root-per-repository"></a>Appliquer une seule racine d’agrégat par dépôt

Il peut s’avérer très utile d’implémenter votre conception de dépôt de sorte à faire respecter la règle stipulant que seules les racines d’agrégat doivent avoir des dépôts. Vous pouvez créer un type de dépôt générique ou basique qui limite le type des entités utilisées pour veiller à ce qu’elles aient l’interface de marqueur IAggregateRoot.

Ainsi, chaque classe de dépôt implémentée au niveau de la couche d’infrastructure implémente son propre contrat ou sa propre interface, comme le montre le code suivant :

```csharp
namespace Microsoft.eShopOnContainers.Services.Ordering.Infrastructure.Repositories
{
    public class OrderRepository : IOrderRepository
    {
```

Chaque interface de dépôt spécifique implémente l’interface IRepository générique :

```csharp
public interface IOrderRepository : IRepository<Order>
{
    Order Add(Order order);
    // ...
}
```

Toutefois, un meilleur moyen d’obliger le code à appliquer la convention selon laquelle chaque dépôt doit être lié à un seul agrégat consiste à implémenter un type de dépôt générique pour qu’il soit explicite que vous utilisez un dépôt pour cibler un agrégat spécifique. Vous pouvez le faire facilement en implémentant ce type générique dans l’interface de base IRepository, comme dans le code suivant :

```csharp
  public interface IRepository<T> where T : IAggregateRoot
```

### <a name="the-repository-pattern-makes-it-easier-to-test-your-application-logic"></a>Le modèle Dépôt facilite le test de votre logique d’application

Le modèle Dépôt vous permet de tester facilement votre application avec des tests unitaires. N’oubliez pas que les tests unitaires testent uniquement votre code, pas l’infrastructure, si bien que les abstractions de dépôt facilitent la réalisation de cet objectif.

Comme indiqué dans une section précédente, il est recommandé de définir et placer les interfaces de dépôt dans la couche du modèle de domaine pour que la couche Application (par exemple, votre microservice d’API web) ne dépende pas directement de la couche d’infrastructure, dans laquelle vous avez implémenté les classes de dépôt réelles. Ce faisant et à l’aide de l’injection de dépendances dans les contrôleurs de votre API web, vous pouvez implémenter des dépôts fictifs qui retournent de fausses données au lieu des données de la base de données. Cette approche découplée vous permet de créer et d’exécuter des tests unitaires permettant de tester seulement la logique de votre application sans nécessiter de connectivité à la base de données.

Les connexions aux bases de données peuvent échouer et, ce qui est plus important, l’exécution de centaines de tests sur une base de données est mauvaise pour deux raisons. Tout d’abord, elle peut s’avérer très chronophage en raison du grand nombre de tests. Ensuite, les enregistrements de base de données peuvent changer et affecter les résultats de vos tests, qui peuvent ne pas être cohérents. Un test sur une base de données n’est pas un test unitaire, mais un test d’intégration. Vous devez effectuer de nombreux tests unitaires qui s’exécutent rapidement, mais un nombre moindre de tests d’intégration sur les bases de données.

En termes de séparation des responsabilités pour les tests unitaires, votre logique s’exécute sur des entités de domaine dans la mémoire. Elle suppose que la classe de dépôt les a remises. Une fois que votre logique modifie les entités de domaine, elle suppose que la classe de dépôt les stocke correctement. Il est important de créer des tests unitaires sur votre modèle de domaine et sa logique de domaine. Les racines d’agrégat correspondent aux limites de cohérence principales dans la conception DDD.

### <a name="the-difference-between-the-repository-pattern-and-the-legacy-data-access-class-dal-class-pattern"></a>La différence entre le modèle Dépôt et le modèle de la classe d’accès aux données héritée (classe DAL)

Un objet d’accès aux données exécute directement des opérations d’accès aux données et de persistance des données dans le stockage. Un dépôt marque les données avec les opérations à effectuer dans la mémoire d’une unité d’objet de travail (comme dans EF lorsque vous utilisez DbContext), mais ces mises à jour ne sont pas effectuées immédiatement.

Une unité de travail est définie comme une transaction unique qui implique plusieurs opérations d’insertion, de mise à jour ou de suppression. En termes simples, cela signifie que, pour une action utilisateur spécifique (par exemple, une inscription sur un site web), toutes les transactions d’insertion, de mise à jour et de suppression sont gérées dans une transaction unique. Une telle gestion est plus efficace que de gérer plusieurs transactions de base de données d’une manière plus bavarde.

Ces multiples opérations de persistance sont effectuées ultérieurement en une seule action quand votre code de la couche Application la commande. La décision d’appliquer les modifications en mémoire au stockage réel de la base de données se base généralement sur le [modèle Unité de travail](https://martinfowler.com/eaaCatalog/unitOfWork.html). Dans EF, le modèle Unité de travail est implémenté en tant que DBContext.

Dans de nombreux cas, ce modèle ou cette façon d’appliquer des opérations dans le stockage peut augmenter les performances de l’application et réduire le risque d’incohérences. De plus, cela réduit le blocage des transactions dans les tables de base de données, car toutes les opérations prévues sont validées dans le cadre d’une seule transaction. Ce modèle est plus efficace que l’exécution de nombreuses opérations isolées sur la base de données. Par conséquent, l’ORM sélectionné est en mesure d’optimiser l’exécution sur la base de données en regroupant plusieurs actions de mise à jour au sein de la même transaction, au lieu d’exécuter de nombreuses transactions distinctes de petite taille.

### <a name="repositories-should-not-be-mandatory"></a>Les dépôts ne doivent pas être obligatoires

Les dépôts personnalisés sont utiles pour les raisons citées précédemment. C’est l’approche utilisée pour le microservice de passation de commandes dans eShopOnContainers. Toutefois, il ne s’agit pas d’un modèle essentiel à implémenter dans une conception DDD voire même dans le cadre du développement général dans .NET.

Par exemple, Jimmy Bogard, en commentant directement le présent guide, a tenu les propos suivants :

Ces commentaires seront probablement mes plus longs. Je ne suis vraiment pas fan des dépôts, principalement parce qu’ils cachent les détails importants du mécanisme de persistance sous-jacent. C’est pour cela que je préfère MediatR pour les commandes, aussi. Je peux utiliser toute la puissance de la couche de persistance et transmettre tout ce comportement de domaine à mes racines d’agrégat. En général, je ne veux pas simuler mes dépôts. J’ai quand même besoin de confronter ce test d’intégration avec la réalité. L’adoption de CQRS signifie que nous n’avons plus vraiment besoin des dépôts.

Nous les trouvons utiles, mais nous reconnaissons qu’ils ne sont pas essentiels pour votre DDD, comme le sont le modèle Agrégat et le modèle de domaine riche. Par conséquent, utilisez le modèle Dépôt ou ne l’utilisez pas, en fonction de vos besoins.

## <a name="the-specification-pattern"></a>Le modèle Spécification

Le modèle Spécification (son nom complet est modèle Spécification de requêtes) est un modèle de conception pilotée par le domaine (DDD, Domain-Driven Design) conçu comme l’emplacement où vous pouvez placer la définition d’une requête avec une éventuelle logique de tri et de pagination.

Le modèle Spécification définit une requête dans un objet. Par exemple, pour encapsuler une requête paginée qui recherche certains produits, vous pouvez créer une spécification PagedProduct qui accepte les paramètres d’entrée nécessaires (pageNumber, pageSize, filtre, etc.). Ensuite, au sein de toute méthode de dépôt (généralement une surcharge List()), elle peut accepter une ISpecification et exécuter la requête prévue en fonction de cette spécification.

Il existe plusieurs avantages à cette approche :

* La spécification porte un nom (par opposition à une simple série d’expressions LINQ) dont vous pouvez discuter.

* La spécification peut faire l’objet d’un test unitaire de manière isolée pour vérifier qu’elle est correcte. Elle peut aussi être réutilisée facilement si vous avez besoin d’un comportement similaire. Par exemple, sur une action de vue MVC et une action d’API web, ainsi que dans divers services.

* Une spécification peut également servir à décrire la forme des données à retourner, afin que les requêtes puissent retourner uniquement les données requises. Le besoin de chargement différé est ainsi éliminé dans les applications web (ce qui n’est généralement pas une bonne idée) et les implémentations de dépôt ne s’encombrent pas avec ces détails.

Le code suivant issu d’[eShopOnweb](https://github.com/dotnet-architecture/eShopOnWeb ) est un exemple d’interface Spécification générique.

```csharp
// https://github.com/dotnet-architecture/eShopOnWeb 
public interface ISpecification<T>
{
    Expression<Func<T, bool>> Criteria { get; }
    List<Expression<Func<T, object>>> Includes { get; }
    List<string> IncludeStrings { get; }
}
```

Dans les sections ci-après, la manière d’implémenter le modèle Spécification avec Entity Framework Core 2.0 et la manière de l’utiliser à partir d’une classe de dépôt sont expliquées.

**Remarque importante :** Le modèle Spécification est un ancien modèle qui peut être implémenté de différentes façons, comme dans les ressources supplémentaires suivantes. En tant que modèle/idée, les approches plus anciennes sont bonnes à savoir, mais méfiez-vous des implémentations plus anciennes qui n’exploitent pas les fonctionnalités des langages modernes comme Linq et les expressions.

## <a name="additional-resources"></a>Ressources supplémentaires

### <a name="the-repository-pattern"></a>Le modèle Dépôt

-   **Edward Hieatt et Rob Mee. Repository pattern.**
    [*https://martinfowler.com/eaaCatalog/repository.html*](https://martinfowler.com/eaaCatalog/repository.html)

-   **The Repository pattern**
    [*https://msdn.microsoft.com/library/ff649690.aspx*](https://msdn.microsoft.com/library/ff649690.aspx)

-   **Repository Pattern: A data persistence abstraction**
    [*http://deviq.com/repository-pattern/*](http://deviq.com/repository-pattern/)

-   **Eric Evans. Domain-Driven Design: Tackling Complexity in the Heart of Software.** (Book; includes a discussion of the Repository pattern) [*https://www.amazon.com/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215/*](https://www.amazon.com/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215/)

### <a name="unit-of-work-pattern"></a>Modèle Unité de travail

-   **Martin Fowler. Unit of Work pattern.**
    [*https://martinfowler.com/eaaCatalog/unitOfWork.html*](https://martinfowler.com/eaaCatalog/unitOfWork.html)

<!-- -->

-   **Implémentation du dépôt et des modèles d’unité de travail dans une application ASP.NET MVC**
    [*https://www.asp.net/mvc/overview/older-versions/getting-started-with-ef-5-using-mvc-4/implementing-the-repository-and-unit-of-work-patterns-in-an-asp-net-mvc-application*](https://www.asp.net/mvc/overview/older-versions/getting-started-with-ef-5-using-mvc-4/implementing-the-repository-and-unit-of-work-patterns-in-an-asp-net-mvc-application)

### <a name="the-specification-pattern"></a>Le modèle Spécification

-   **The Specification pattern.**
    [*http://deviq.com/specification-pattern/*](http://deviq.com/specification-pattern/)

-   **Evans, Eric (2004). Domain Driven Design. Addison-Wesley. p. 224.**

-   **Specifications. Martin Fowler**
    [*https://www.martinfowler.com/apsupp/spec.pdf/*](https://www.martinfowler.com/apsupp/spec.pdf)

>[!div class="step-by-step"]
[Précédent](domain-events-design-implementation.md)
[Suivant](infrastructure-persistence-layer-implemenation-entity-framework-core.md)
