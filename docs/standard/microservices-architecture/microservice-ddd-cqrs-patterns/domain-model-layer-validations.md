---
title: Conception de validations dans la couche de modèle de domaine
description: Architecture des microservices .NET pour les applications .NET en conteneur | Conception de validations dans la couche de modèle de domaine
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: 6ff325bb062da2ebff815fc847d2247707a0bf7f
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188051"
---
# <a name="designing-validations-in-the-domain-model-layer"></a>Conception de validations dans la couche de modèle de domaine

Dans la conception DDD, les règles de validation peuvent être considérées comme des invariants. La responsabilité principale d’un agrégat est d’appliquer des invariants aux changements d’état pour toutes les entités de cet agrégat.

Les entités de domaine doivent toujours être des entités valides. Pour un objet, il existe un certain nombre d’invariants qui doivent toujours avoir la valeur true. Par exemple, un objet d’élément de commande doit toujours avoir une quantité qui doit être un entier positif, ainsi qu’un nom d’article et un prix. Par conséquent, il incombe aux entités de domaine (en particulier celles de la racine d’agrégat) de mettre en application les invariants, et un objet d’entité ne doit pas pouvoir exister s’il n’est pas valide. Les règles invariantes sont simplement exprimées sous la forme de contrats. Quand elles sont enfreintes, des exceptions ou des notifications sont déclenchées.

Le raisonnement derrière cette règle est que de nombreux bogues se produisent car les objets sont dans un état dans lequel ils n’auraient jamais dû se trouver. Ce qui suit en est une bonne explication de Greg Young dans une [discussion en ligne](https://jeffreypalermo.com/blog/the-fallacy-of-the-always-valid-entity/) :

Supposons que nous disposons désormais d’un service SendUserCreationEmailService qui prend un UserProfile... Comment pouvons-nous justifier, dans ce service, que le nom ne soit pas null ? Le vérifions-nous à nouveau ? Ou plus probablement... vous ne vous souciez simplement pas de la vérification et « espérez que tout se passera au mieux » : vous espérez que quelqu’un a pris la peine de le valider avant de vous l’envoyer. Bien entendu, en utilisant TDD, l’un des premiers tests que nous devons écrire est que si j’envoie un client avec un nom null, une erreur doit être déclenchée. Mais une fois que nous commençons à écrire ce genre de tests encore et encore, nous réalisons ceci : « Si nous n’avions pas autorisé qu’un nom devienne null, nous n’aurions pas tous ces tests ».

## <a name="implementing-validations-in-the-domain-model-layer"></a>Implémentation de validations dans la couche du modèle de domaine

Les validations sont généralement implémentées dans des constructeurs d’entité de domaine ou dans des méthodes qui peuvent mettre à jour l’entité. Il existe plusieurs façons d’implémenter des validations, comme la vérification des données et la levée d’exceptions si la validation échoue. Il existe également des modèles plus avancés comme l’utilisation du modèle Spécification pour les validations, et le modèle Notification pour retourner une collection d’erreurs au lieu de retourner une exception pour chaque validation quand elle se produit.

### <a name="validating-conditions-and-throwing-exceptions"></a>Validation de conditions et levée d’exceptions

L’exemple de code suivant illustre l’approche de validation la plus simple dans une entité de domaine en levant une exception. La table de références figurant à la fin de cette section indique des liens vers des implémentations plus avancées basées sur les modèles abordés précédemment.

```csharp
public void SetAddress(Address address)
{
    _shippingAddress = address?? throw new ArgumentNullException(nameof(address));
}
```

La nécessité de garantir que l’état interne n’a pas changé ou que toutes les mutations pour une méthode se sont produites constituerait un meilleur exemple. Ainsi, l’implémentation suivante laisse l’objet dans un état non valide :

```csharp
public void SetAddress(string line1, string line2,
    string city, string state, int zip)
{
    _shipingAddress.line1 = line1 ?? throw new ...
    _shippingAddress.line2 = line2;
    _shippingAddress.city = city ?? throw new ...
    _shippingAddress.state = (IsValid(state) ? state : throw new …);
}
```

Si la valeur de l’état n’est pas valide, la première ligne d’adresse et la ville ont déjà été modifiées. Cela peut rendre l’adresse non valide.

Une approche similaire peut être utilisée dans le constructeur de l’entité, levant une exception pour vérifier que l’entité est valide une fois créée.

### <a name="using-validation-attributes-in-the-model-based-on-data-annotations"></a>Utilisation d’attributs de validation dans le modèle basé sur des annotations de données

Une autre approche consiste à utiliser des attributs de validation basés sur des annotations de données. Les attributs de validation offrent un moyen de configurer la validation de modèle, qui est, d’un point de vue conceptuel, semblable à la validation des champs dans des tables de base de données. Cela inclut des contraintes comme l’affectation de types de données ou des champs obligatoires. L’application de modèles à des données pour forcer le respect de règles métier, comme un numéro de carte de crédit, un numéro de téléphone ou une adresse e-mail, est un autre type de validation. Les attributs de validation facilitent l’application d’une configuration requise.

Toutefois, comme indiqué dans le code suivant, cette approche peut être trop intrusive dans un modèle DDD, car elle a une dépendance sur ModelState.IsValid à partir de Microsoft.AspNetCore.Mvc.ModelState, que vous devez appeler à partir de vos contrôleurs MVC. La validation de modèle se produit avant l’appel de chaque action du contrôleur ; il incombe à la méthode de contrôleur d’inspecter le résultat de l’appel à ModelState.IsValid et de réagir de façon appropriée. La décision de l’utiliser dépend du degré de couplage fort souhaité pour le modèle avec cette infrastructure.

```csharp
using System.ComponentModel.DataAnnotations;
// Other using statements ...
// Entity is a custom base class which has the ID
public class Product : Entity
{
    [Required]
    [StringLength(100)]
    public string Title { get; private set; }

    [Required]
    [Range(0, 999.99)]
    public decimal Price { get; private set; }

    [Required]
    [VintageProduct(1970)]
    [DataType(DataType.Date)]
    public DateTime ReleaseDate { get; private set; }

    [Required]
    [StringLength(1000)]
    public string Description { get; private set; }

    // Constructor...
    // Additional methods for entity logic and constructor...
}
```

Toutefois, du point de vue DDD, il est préférable de conserver le modèle de domaine épuré en utilisant des exceptions dans les méthodes de comportement de votre entité, ou en implémentant les modèles Spécification et Notification pour appliquer des règles de validation. Les frameworks de validation comme les annotations de données dans ASP.NET Core ou tout autre framework de validation comme FluentValidation comportent l’obligation d’appeler le framework d’application. Par exemple, quand vous appelez la méthode ModelState.IsValid dans des annotations de données, vous devez appeler des contrôleurs ASP.NET.

Il peut être judicieux d’utiliser des annotations de données au niveau de la couche Application dans les classes ViewModel (plutôt que des entités de domaine) qui accepteront des entrées, pour permettre la validation de modèle dans la couche d’interface utilisateur. Toutefois, cela ne doit pas être effectué à l’exclusion de la validation dans le modèle de domaine.

### <a name="validating-entities-by-implementing-the-specification-pattern-and-the-notification-pattern"></a>Validation d’entités en implémentant le modèle Spécification et le modèle Notification

Enfin, une approche plus élaborée pour implémenter des validations dans le modèle de domaine consiste à implémenter le modèle Spécification conjointement avec le modèle Notification, comme expliqué dans certaines des ressources supplémentaires répertoriées ultérieurement.

Il convient de mentionner que vous pouvez également utiliser un seul de ces modèles, par exemple en effectuant la validation manuellement avec des instructions de contrôle, mais en utilisant le modèle Notification pour empiler des erreurs de validation et en retourner la liste.

### <a name="using-deferred-validation-in-the-domain"></a>Utilisation de la validation différée dans le domaine

Il existe différentes approches pour traiter les validations différées dans le domaine. Dans son livre [Implementing Domain-Driven Design](https://www.amazon.com/Implementing-Domain-Driven-Design-Vaughn-Vernon/dp/0321834577), Vaughn Vernon les décrit dans la section relative à la validation.

### <a name="two-step-validation"></a>Validation en deux étapes

Considérons également la validation en deux étapes. Utilisez la validation au niveau des champs sur vos objets de transfert de données (DTO) de commande et la validation au niveau du domaine à l’intérieur de vos entités. Pour cela, retournez un objet de résultat plutôt que des exceptions afin de faciliter la gestion des erreurs de validation.

En utilisant la validation de champ avec des annotations de données, par exemple, vous ne dupliquez pas la définition de la validation. L’exécution peut toutefois être à la fois côté serveur et côté client dans le cas d’objets DTO (commandes et ViewModels, par exemple).

## <a name="additional-resources"></a>Ressources supplémentaires

-   **Rachel Appel. Présentation de la validation de modèle dans ASP.NET Core MVC**
    [*https://docs.microsoft.com/aspnet/core/mvc/models/validation*](https://docs.microsoft.com/aspnet/core/mvc/models/validation)

-   **Rick Anderson. Ajout de la validation**
    [*https://docs.microsoft.com/aspnet/core/tutorials/first-mvc-app/validation*](https://docs.microsoft.com/aspnet/core/tutorials/first-mvc-app/validation)

-   **Martin Fowler. Replacing Throwing Exceptions with Notification in Validations**
    [*https://martinfowler.com/articles/replaceThrowWithNotification.html*](https://martinfowler.com/articles/replaceThrowWithNotification.html)

-   **Specification and Notification Patterns**
    [*https://www.codeproject.com/Tips/790758/Specification-and-Notification-Patterns*](https://www.codeproject.com/Tips/790758/Specification-and-Notification-Patterns)

-   **Lev Gorodinski. Validation in Domain-Driven Design (DDD)**
    [*http://gorodinski.com/blog/2012/05/19/validation-in-domain-driven-design-ddd/*](http://gorodinski.com/blog/2012/05/19/validation-in-domain-driven-design-ddd/)

-   **Colin Jack. Domain Model Validation**
    [*http://colinjack.blogspot.com/2008/03/domain-model-validation.html*](http://colinjack.blogspot.com/2008/03/domain-model-validation.html)

-   **Jimmy Bogard. Validation in a DDD world**
    [*https://lostechies.com/jimmybogard/2009/02/15/validation-in-a-ddd-world/*](https://lostechies.com/jimmybogard/2009/02/15/validation-in-a-ddd-world/)


>[!div class="step-by-step"]
[Précédent](enumeration-classes-over-enum-types.md)
[Suivant](client-side-validation.md)
