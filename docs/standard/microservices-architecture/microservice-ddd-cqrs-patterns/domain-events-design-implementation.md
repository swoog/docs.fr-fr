---
title: Événements de domaine. Conception et implémentation
description: 'Architecture des microservices .NET pour les applications .NET en conteneur | Événements de domaine : conception et implémentation'
keywords: Docker, microservices, ASP.NET, conteneur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 12/11/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: bec1341df85f86d5f2aa15753a11a9c4a2d0173f
ms.sourcegitcommit: 2e8acae16ae802f2d6d04e3ce0a6dbf04e476513
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2018
---
# <a name="domain-events-design-and-implementation"></a>Événements de domaine : conception et implémentation

Utilisez des événements de domaine pour implémenter explicitement les effets secondaires des modifications apportées à votre domaine. En d’autres termes, pour utiliser la terminologie DDD, les événements de domaine permettent d’implémenter explicitement des effets secondaires sur plusieurs agrégats. Si vous le souhaitez, pour une meilleure scalabilité et un impact moindre sur les verrous de base de données, utilisez la cohérence à terme entre les agrégats d’un même domaine.

## <a name="what-is-a-domain-event"></a>Qu’est-ce qu’un événement de domaine ?

Un événement est quelque chose qui s’est produit dans le passé. Logiquement, un événement de domaine est quelque chose qui s’est produit dans un domaine particulier, et dont vous voulez que les autres composants du domaine (in-process) soient informés pour éventuellement y réagir.

Les événements de domaine présentent l’avantage important de pouvoir être exprimés de manière explicite et non implicite lorsque des effets secondaires se produisent dans un domaine. Ces effets doivent être cohérents, c’est-à-dire que soit toutes les opérations relatives à la tâche se produisent, soit aucune ne se produit. En outre, les événements de domaine permettent une meilleure séparation des classes appartenant au même domaine.

Par exemple, si vous utilisez Entity Framework et des entités, voire des agrégats, si un cas d’usage doit provoquer des effets secondaires, ceux-ci seront implémentés comme un concept implicite dans le code couplé après la survenue d’un problème. Toutefois, si vous voyez uniquement ce code, vous pouvez ne pas savoir si ce code (l’effet secondaire) fait partie de l’opération principale ou s’il s’agit réellement d’un effet secondaire. En revanche, l’utilisation d’événements de domaine rend le concept explicite et l’intègre au langage omniprésent. Par exemple, dans l’application eShopOnContainers, la création d’une commande ne se résume pas à la commande. L’application met à jour ou crée un agrégat d’acheteur basé sur l’utilisateur d’origine, car l’utilisateur n’est pas un acheteur tant qu’il n’a pas passé de commande. Si vous utilisez des événements de domaine, vous pouvez exprimer explicitement cette règle de domaine dans le langage omniprésent fourni par les experts du domaine.

Les événements de domaine sont quelque peu similaires aux événements de type messagerie, avec toutefois une différence importante. Avec les systèmes de messagerie réels, la mise en file d’attente des messages, les répartiteurs de messages et les bus de services utilisant le protocole AMPQ, les messages sont toujours envoyés de manière asynchrone sur plusieurs processus et ordinateurs. Cela est utile pour l’intégration de plusieurs contextes délimités ou de plusieurs microservices, voire d’applications différentes. Toutefois, avec les événements de domaine, vous devez déclencher un événement à partir de l’opération de domaine actuellement exécutée, et les effets secondaires doivent se produire dans le même domaine.

Les événements de domaine et leurs effets secondaires (les actions déclenchées par la suite qui sont gérées par les gestionnaires d’événements) doivent se produire presque immédiatement, généralement in-process, et dans le même domaine. Par conséquent, les événements de domaine peuvent être synchrones ou asynchrones. Cependant, les événements d’intégration doivent toujours être asynchrones.

## <a name="domain-events-versus-integration-events"></a>Comparaison des événements de domaine et des événements d’intégration

D’un point de vue sémantique, les événements de domaine et d’intégration sont identiques : ce sont des notifications à propos de quelque chose qui vient de se produire. Toutefois, leur implémentation doit être différente. Les événements de domaine ne sont que des messages envoyés vers un répartiteur d’événements de domaine, qui peut être implémenté comme un médiateur en mémoire basé sur un conteneur IoC ou toute autre méthode.

En revanche, le rôle des événements d’intégration est de propager les transactions et les mises à jour validées sur d’autres sous-systèmes, tels que des microservices, des contextes délimités ou des applications externes. Par conséquent, ils doivent se produire uniquement si l’entité est rendue persistante, puisque dans de nombreux scénarios, en cas d’échec, l’opération n’est jamais effectuée dans son intégralité.

En outre, comme nous l’avons déjà dit, les événements d’intégration doivent être basés sur une communication asynchrone entre plusieurs microservices (d’autres contextes délimités), voire entre plusieurs systèmes/applications externes. Par conséquent, l’interface du bus d’événements a besoin d’une infrastructure permettant une communication entre processus et distribuée entre des services potentiellement distants. Elle peut reposer sur un bus de services commercial, sur des files d’attente, sur une base de données partagée utilisée comme une boîte aux lettres, ou sur tout autre système de messagerie distribué et idéalement basé sur les opérations d’envoi (push).

## <a name="domain-events-as-a-preferred-way-to-trigger-side-effects-across-multiple-aggregates-within-the-same-domain"></a>Utilisation des événements de domaine comme méthode par défaut de déclenchement des effets secondaires sur plusieurs agrégats appartenant à un même domaine

Si l’exécution d’une commande liée à une instance d’agrégat nécessite que d’autres règles de domaine soient exécutées sur un ou plusieurs autres agrégats, vous devez concevoir et implémenter ces effets secondaires de manière à ce qu’ils soient déclenchés par les événements de domaine. Comme le montre la Figure 9-14, et c’est là l’un des principaux cas d’usage, un événement de domaine doit être utilisé pour propager les changements d’état sur plusieurs agrégats appartenant au même modèle de domaine.

![](./media/image15.png)

**Figure 9-14**. Utilisation des événements de domaine pour obtenir la cohérence entre les différents agrégats d’un même domaine

Dans la figure ci-dessus, lorsque l’utilisateur démarre la création d’une commande, l’événement de domaine OrderStarted déclenche la création d’un objet Acheteur dans le microservice de commande, en se basant sur les informations de l’utilisateur d’origine provenant du microservice d’identité (avec les informations fournies dans la commande CreateOrder). L’événement de domaine est généré par l’agrégat de commande lors de sa création.

Vous pouvez également abonner l’agrégat racine aux événements déclenchés par les membres de ses agrégats (entités enfants). Par exemple, chaque entité enfant d’OrderItem peut déclencher un événement lorsque le prix du produit est supérieur à un montant donné, ou lorsque le montant du produit est trop élevé. L’agrégat racine peut ensuite recevoir ces événements et effectuer un calcul global ou un agrégat.

Il est important de comprendre que cette communication basée sur les événements n’est pas implémentée directement dans les agrégats. Vous devez implémenter des gestionnaires d’événements de domaine. La gestion des événements de domaine est située au niveau de l’application. La couche de modèle de domaine doit se concentrer uniquement sur la logique de domaine (que seuls des experts en domaines sont à même de comprendre), et non sur l’infrastructure de l’application (par exemple, les gestionnaires et les actions de persistance des effets secondaires utilisant des dépôts). Par conséquent, c’est au niveau de la couche Application que les gestionnaires d’événements de domaine doivent déclencher des actions lorsqu’un événement de domaine est déclenché.

Les événements de domaine peuvent également servir à déclencher autant d’actions d’application que nécessaire, et plus important encore, ils doivent permettre l’augmentation future du nombre d’actions d’une manière découplée. Par exemple, lorsque vous démarrez la création de la commande, vous pouvez publier un événement de domaine pour propager ces informations sur d’autres agrégats ou même pour déclencher des actions telles que des notifications.

Le point essentiel est le nombre ouvert d’actions à exécuter lorsqu’un événement de domaine se produit. Avec le temps, le nombre d’actions et de règles dans le domaine et dans l’application va augmenter. La complexité ou le nombre d’actions d’effet secondaire lors d’un événement vont augmenter avec le temps. Toutefois, si votre code était couplé avec « glue » (c’est-à-dire que les objets seraient simplement instanciés avec le mot clé new en C\#), chaque fois que vous auriez besoin d’ajouter une nouvelle action, une modification du code d’origine serait nécessaire. Cela pourrait entraîner de nouveaux bogues, car chaque nouvelle exigence nécessiterait la modification du code d’origine. Cela va à l’encontre du [principe ouvert/fermé](https://en.wikipedia.org/wiki/Open/closed_principle), issu des principes [SOLID](https://en.wikipedia.org/wiki/SOLID_(object-oriented_design)). En outre, le volume de la classe d’origine orchestrant les opérations ne ferait qu’augmenter, ce qui irait à l’encontre du [principe de responsabilité unique](https://en.wikipedia.org/wiki/Single_responsibility_principle).

En revanche, si vous utilisez des événements de domaine, vous pouvez créer une implémentation affinée et découplée en séparant les responsabilités à l’aide de la méthode suivante :

1.  Envoyez une commande (par exemple, CreateOrder).
2.  Recevez la commande dans un gestionnaire de commandes.
    -   Exécutez la transaction d’un seul agrégat.
    -   (Facultatif) Déclenchez des événements de domaine pour les effets secondaires (par exemple, OrderStartedDomainEvent).
1.  Gérez les événements de domaine (dans le processus actuel) qui vont exécuter un nombre ouvert d’effets secondaires dans plusieurs agrégats ou actions d’application. Exemple :
    -   Vérifiez ou créez l’acheteur et la méthode de paiement.
    -   Créez et envoyez un événement d’intégration associé au bus d’événements pour propager les états sur les microservices ou déclencher des actions externes, comme l’envoi d’un e-mail à l’acheteur.
    -   Gérez les autres effets secondaires.

Comme le montre la Figure 9-15, à partir du même événement de domaine, vous pouvez gérer plusieurs actions liées aux autres agrégats du domaine ou à d’autres actions d’application devant être exécutées sur les microservices en se connectant aux événements d’intégration et au bus d’événements.

![](./media/image16.png)

**Figure 9-15**. Gestion de plusieurs actions par domaine

Les gestionnaires d’événements se trouvent en général dans la couche Application, car vous allez utiliser les objets d’infrastructure comme les dépôts ou une API d’application pour le comportement du microservice. Dans ce sens, les gestionnaires d’événements sont similaires aux gestionnaires de commandes, car tous deux font partie de la couche Application. La principale différence est qu’une commande ne doit être traitée qu’une seule fois. Un événement de domaine peut être traité zéro ou *n* fois, car il peut être reçu par plusieurs récepteurs ou gestionnaires d’événements, chacun ayant un objectif différent.

La possibilité d’un nombre ouvert de gestionnaires pour chaque événement de domaine permet d’ajouter plusieurs règles de domaine sans impacter votre code actuel. Par exemple, pour implémenter la règle métier suivante qui doit se produire juste après un événement, vous pouvez simplement ajouter quelques gestionnaires d’événements (voire un seul) :

Lorsque le montant total dépensé par un client (quel que soit le nombre de commandes) dépasse 6 000 $, appliquer une remise de 10 % à chaque nouvelle commande et envoyer un e-mail au client pour l’informer de cette remise sur ses commandes futures.

## <a name="implementing-domain-events"></a>Implémentation des événements de domaine

En C#, un événement de domaine est une simple structure ou classe contenant des données, tel qu’un objet de transfert de données (DTO), avec toutes les informations relatives à ce qui vient de se passer dans le domaine, comme dans l’exemple suivant :

```csharp
public class OrderStartedDomainEvent : INotification
{
    public string UserId { get; }
    public int CardTypeId { get; }
    public string CardNumber { get; }
    public string CardSecurityNumber { get; }
    public string CardHolderName { get; }
    public DateTime CardExpiration { get; }
    public Order Order { get; }

    public OrderStartedDomainEvent(Order order,
                                   int cardTypeId, string cardNumber,
                                   string cardSecurityNumber, string cardHolderName,
                                   DateTime cardExpiration)
    {
        Order = order;
        CardTypeId = cardTypeId;
        CardNumber = cardNumber;
        CardSecurityNumber = cardSecurityNumber;
        CardHolderName = cardHolderName;
        CardExpiration = cardExpiration;
    }
}
```

Il s’agit essentiellement d’une classe qui contient toutes les données associées à l’événement OrderStarted.

En ce qui concerne le langage omniprésent du domaine, dans la mesure où un événement est quelque chose qui s’est produit dans le passé, le nom de classe de l’événement doit être représenté comme un verbe au passé, comme dans OrderStartedDomainEvent ou OrderShippedDomainEvent. C’est ainsi qu’est implémenté l’événement de domaine dans le microservice de commande dans eShopOnContainers.

Comme mentionné précédemment, l’une des caractéristiques les plus importantes des événements est, puisqu’ils se sont produits dans le passé, ils ne doivent pas changer. Par conséquent, il doit s’agir d’une classe immuable. Dans le code précédent, vous pouvez voir qu’en dehors de l’objet, les propriétés sont en lecture seule. La seule façon de mettre à jour l’objet est via le constructeur lorsque vous créez l’objet d’événement.

### <a name="raising-domain-events"></a>Déclenchement des événements de domaine

L’étape suivante consiste à déclencher un événement de domaine pour qu’il atteigne ses gestionnaires d’événements associés. Il existe pour cela plusieurs méthodes.

Udi Dahan proposait à l’origine (dans plusieurs billets de blog comme, par exemple, [Domain Events – Take 2](http://udidahan.com/2008/08/25/domain-events-take-2/)) d’utiliser une classe statique pour gérer et déclencher les événements. Cela peut inclure une classe statique nommée DomainEvents qui déclenche des événements de domaine immédiatement après son appel, en utilisant une syntaxe similaire à celle-ci : DomainEvents.Raise(Event myEvent). Jimmy Bogard a écrit un billet de blog ([Strengthening your domain: Domain Events](https://lostechies.com/jimmybogard/2010/04/08/strengthening-your-domain-domain-events/)) qui recommande une approche similaire.

Toutefois, lorsque la classe d’événements de domaine est statique, elle distribue aussi les événements aux gestionnaires immédiatement. Les tests et le débogage deviennent alors plus difficiles, car les gestionnaires d’événements avec une logique d’effets secondaires sont exécutés immédiatement après le déclenchement de l’événement. Lorsque vous effectuez des tests et des débogages, vous devez vous concentrer uniquement sur ce qui se passe actuellement dans les classes d’agrégats. Vous ne voulez pas être soudainement redirigé vers d’autres gestionnaires d’événements pour des effets secondaires liés à d’autres agrégats ou à une autre logique d’application. C’est pour cela que les autres approches ont évolué, comme nous allons le voir dans la section suivante.

#### <a name="the-deferred-approach-for-raising-and-dispatching-events"></a>Approche différée pour déclencher et distribuer les événements

Au lieu de distribuer immédiatement les événements vers un gestionnaire d’événements de domaine, il est préférable d’ajouter les événements de domaine à une collection, puis de distribuer les événements de domaine *juste avant* ou *juste* *après* avoir validé la transaction (comme avec SaveChanges dans Entity Framework). Cette approche est expliquée par Jimmy Bogard dans le billet de blog [A better domain events pattern](https://lostechies.com/jimmybogard/2014/05/13/a-better-domain-events-pattern/).

Il est important de décider si les événements de domaine doivent être envoyés juste avant ou juste après avoir validé la transaction, car cela permet de déterminer si vous devez inclure les effets secondaires dans la même transaction ou dans des transactions différentes. Dans ce dernier cas, vous devez appliquer la cohérence à terme sur plusieurs agrégats. Ce sujet est abordé dans la section suivante.

L’approche différée est celle utilisée par l’aplication eShopOnContainers. Tout d’abord, vous devez ajouter les événements qui se produisent dans vos entités à une collection ou à une liste d’événements pour chaque entité. Cette liste doit faire partie de l’objet entité, ou mieux encore, de votre classe d’entité de base, comme indiqué dans l’exemple suivant :

```csharp
public abstract class Entity
{
     //... 
    private List<INotification> _domainEvents;
    public List<INotification> DomainEvents => _domainEvents;

    public void AddDomainEvent(INotification eventItem)
    {
        _domainEvents = _domainEvents ?? new List<INotification>();
        _domainEvents.Add(eventItem);
    }

    public void RemoveDomainEvent(INotification eventItem)
    {
        if (_domainEvents is null) return;
        _domainEvents.Remove(eventItem);
    }
    // ...
}
```

Lorsque vous souhaitez déclencher un événement,il vous suffit de l’ajouter à la collection d’événements à partir du code, au niveau de n’importe quelle méthode de l’entité d’agrégat racine.

Le code suivant, qui fait partie de la [commande agregate-root d’eShopOnContainers](https://github.com/dotnet-architecture/eShopOnContainers/blob/dev/src/Services/Ordering/Ordering.Domain/AggregatesModel/OrderAggregate/Order.cs), montre un exemple :

```csharp
var orderStartedDomainEvent = new OrderStartedDomainEvent(this, //Order object
                                                          cardTypeId, cardNumber,
                                                          cardSecurityNumber,
                                                          cardHolderName,
                                                          cardExpiration);
this.AddDomainEvent(orderStartedDomainEvent);
```

Notez que la seule chose qu’effectue la méthode AddDomainEvent est d’ajouter un événement à la liste. Aucun événement n’est encore distribué, et aucun gestionnaire d’événements n’a encore été appelé.

Les événements doivent être distribués plus tard, lorsque vous validez la transaction dans la base de données. Si vous utilisez Entity Framework Core, ce sera dans la méthode SaveChanges de votre DbContext Entity Framework, comme dans le code suivant :

```csharp
// EF Core DbContext
public class OrderingContext : DbContext, IUnitOfWork
{
    // ...
    public async Task<bool> SaveEntitiesAsync(CancellationToken cancellationToken = default(CancellationToken))
    {
        // Dispatch Domain Events collection.
        // Choices:
        // A) Right BEFORE committing data (EF SaveChanges) into the DB. This makes
        // a single transaction including side effects from the domain event
        // handlers that are using the same DbContext with Scope lifetime
        // B) Right AFTER committing data (EF SaveChanges) into the DB. This makes
        // multiple transactions. You will need to handle eventual consistency and
        // compensatory actions in case of failures.        
        await _mediator.DispatchDomainEventsAsync(this);

        // After this line runs, all the changes (from the Command Handler and Domain
        // event handlers) performed through the DbContext will be commited
        var result = await base.SaveChangesAsync();
    }
}
```

Avec ce code, vous distribuez les événements des entités à leurs gestionnaires d’événements respectifs.

Le résultat global est que vous avez découplé le déclenchement d’un événement de domaine (un simple ajout à une liste en mémoire) de sa distribution à un gestionnaire d’événements. En outre, selon le type de répartiteur que vous utilisez, vous pouvez distribuer les événements de façon synchrone ou asynchrone.

N’oubliez pas qu’ici, les limites transactionnelles jouent un rôle important. Si votre unité de travail et votre transaction peuvent s’étendre sur plusieurs agrégats (comme lorsque vous utilisez EF Core et une base de données relationnelle), cela peut bien fonctionner. Toutefois, si la transaction ne peut pas s’étendre sur plusieurs agrégats, comme lorsque vous utilisez une base de données NoSQL telle qu’Azure DocumentDB, vous devrez implémenter des étapes supplémentaires pour obtenir la cohérence. C’est une des raisons pour lesquelles l’ignorance de la persistance n’est pas universelle. Elle dépend du système de stockage que vous utilisez.

### <a name="single-transaction-across-aggregates-versus-eventual-consistency-across-aggregates"></a>Méthode de la transaction unique sur plusieurs agrégats versus méthode de la cohérence à terme

Effectuer une même transaction sur plusieurs agrégats ou compter sur la cohérence à terme de ces agrégats ? Il s’agit là d’une question controversée. De nombreux auteurs DDD comme Eric Evans et Vaughn Vernon préconisent la règle « une transaction = un agrégat », et prennent donc position pour la méthode de la cohérence à terme. Par exemple, dans son livre *Domain-Driven Design*, Eric Evans dit ceci :

Une règle qui s’étend sur plusieurs agrégats ne peut pas être constamment à jour. Grâce au traitement des événements, au traitement par lots et autres mécanismes de mise à jour, les autres dépendances peuvent être résolues dans un temps donné. (page 128)

Vaughn Vernon dit ce qui suit dans [Effective Aggregate Design. Part II: Making Aggregates Work Together](https://dddcommunity.org/wp-content/uploads/files/pdf_articles/Vernon_2011_2.pdf) :

Par conséquent, si l’exécution d’une commande sur une instance d’agrégat nécessite que d’autres règles métier soient exécutées sur un ou plusieurs agrégats, utilisez la cohérence à terme \[...\] Il existe un moyen pratique de prendre en charge la cohérence à terme dans un modèle DDD. Une méthode d’agrégation publie un événement de domaine qui est remis à un ou plusieurs abonnés asynchrones.

Cette logique est basée sur l’exécution de transactions affinées plutôt que de transactions s’étendant sur un grand nombre d’agrégats ou d’entités. L’idée est que, dans le deuxième cas, le nombre de verrous de base de données sera important dans les applications à grande échelle nécessitant une haute scalabilité. Le fait de reconnaître que les applications hautement scalables n’ont pas besoin d’une cohérence transactionnelle instantanée entre les différents agrégats aide à accepter le concept de cohérence à terme. Les modifications atomiques ne sont généralement pas nécessaires à l’entreprise, et il revient aux experts en domaines de décider si certaines opérations ont besoin de transactions atomiques. Si une opération nécessite toujours une transaction atomique entre plusieurs agrégats, vous pouvez vous demander si la taille de votre agrégat doit être augmentée ou si vous l’avez conçu correctement.

Toutefois, les autres développeurs et architectes comme Jimmy Bogard sont d’accord pour utiliser une même transaction sur plusieurs agrégats, mais uniquement si les agrégats supplémentaires sont associés à des effets secondaires de la même commande d’origine. Par exemple, dans [A better domain events pattern](https://lostechies.com/jimmybogard/2014/05/13/a-better-domain-events-pattern/), Bogard dit ceci :

En règle générale, je veux que les effets secondaires d’un événement de domaine se produisent dans la même transaction logique, mais pas nécessairement dans la même étendue de déclenchement de l’événement domaine \[...\] Juste avant de valider notre transaction, nous distribuons nos événements à leurs gestionnaires respectifs.

Si vous distribuez les événements de domaine juste *avant* de valider la transaction d’origine, c’est parce que les effets secondaires doivent être inclus dans la même transaction. Par exemple, si la méthode SaveChanges du DbContext EF échoue, la transaction annule toutes les modifications, y compris le résultat de toutes les opérations d’effet secondaire implémentées par les gestionnaires d’événements de domaine associés. Cela est dû au fait que la durée de vie de DbContext est configurée par défaut comme étant limitée. Par conséquent, l’objet DbContext est partagé par plusieurs objets de dépôt qui sont instanciés dans la même étendue ou le même graphe d’objet. Cela coïncide avec l’étendue HttpRequest lors du développement d’API web ou d’applications MVC.

En réalité, les deux approches (transaction atomique et cohérence à terme) peuvent être appropriées. Cela dépend en réalité des exigences métier ou de votre domaine, et de ce que les experts en domaines vous disent. Cela dépend également du niveau de scalabilité dont doit disposer le service (les transactions plus granulaires ont un impact moindre sur les verrous de base de données). Enfin, cela dépend de l’investissement que vous êtes prêt à mettre dans votre code, puisque la cohérence à terme nécessite un code plus complexe afin de détecter les éventuelles incohérences entre les agrégats et la nécessité d’implémenter des actions compensatoires. Prenez en compte le fait que si vous validez des modifications dans l’agrégat d’origine et que par la suite, lorsque les événements sont distribués, un problème se produit et les gestionnaires d’événements ne peuvent pas valider leurs effets secondaires, vous aurez des incohérences entre les agrégats.

Pour permettre les actions compensatoires, vous pouvez stocker les événements de domaine dans des tables de base de données supplémentaires, pour qu’elles fassent partie de la transaction d’origine. Ensuite, vous pouvez avoir un traitement par lots qui détecte des incohérences et exécute des actions compensatoires en comparant la liste des événements à l’état actuel des agrégats. Les actions compensatoires sont un sujet complexe qui nécessite une analyse approfondie, impliquant à la fois les utilisateurs et les experts en domaines.

Quoi qu’il en soit, vous pouvez choisir l’approche dont vous avez besoin. Toutefois, l’approche différée du début (qui déclenche les événements avant de les valider, permettant ainsi d’utiliser une seule transaction) est la plus simple lorsque vous utilisez EF Core et une base de données relationnelle. Elle est plus facile à implémenter et convient dans de nombreux cas en entreprise. Il s’agit également de l’approche utilisée dans le microservice de commande de l’application eShopOnContainers.

Mais comment faire pour distribuer ces événements à leurs gestionnaires d’événements respectifs ? Quel est cet objet \_mediator que vous voyez dans l’exemple précédent ? Il s’agit de techniques et d’artefacts que vous pouvez utiliser pour le mappage des événements aux gestionnaires d’événements.

### <a name="the-domain-event-dispatcher-mapping-from-events-to-event-handlers"></a>Répartiteur d’événements de domaine : mappage des événements aux gestionnaires d’événements

Une fois que vous êtes en mesure de distribuer ou publier les événements, vous avez besoin d’un artefact pour ces événements, et faire en sorte que le gestionnaire associé puisse les recevoir et traiter les effets secondaires en fonction des événements.

L’une des méthodes possibles consiste à utiliser un système de messagerie réel, voire un bus d’événements, éventuellement basé sur un bus de services au lieu d’événements en mémoire. Toutefois, pour le premier cas, un système de messagerie réel serait excessif pour traiter les événements de domaine, puisque vous avez seulement besoin de traiter ces événements au sein d’un même processus (c’est-à-dire, dans le même domaine et la même couche Application).

Une autre façon de mapper des événements vers plusieurs gestionnaires d’événements est d’utiliser l’inscription des types dans un conteneur IoC, pour déduire dynamiquement où distribuer les événements. En d’autres termes, vous devez savoir ce dont les gestionnaires d’événements ont besoin pour recevoir un événement spécifique. La Figure 9-16 montre une approche simplifiée de cela.

![](./media/image17.png)

**Figure 9-16**. Répartiteur d’événements de domaine utilisant l’IoC

Vous pouvez créer vous-même tous les éléments et artefacts pour implémenter cette approche. Toutefois, vous pouvez également utiliser les bibliothèques disponibles telles que [MediatR](https://github.com/jbogard/MediatR), qui utilisent votre conteneur IoC en arrière-plan. Vous pouvez donc directement utiliser les interfaces prédéfinies, ainsi que les méthodes de publication/distribution de l’objet _mediator.

Dans le code, vous devez d’abord inscrire les types de gestionnaires d’événements dans votre conteneur IoC, comme le montre l’exemple suivant du [microservice de commande eShopOnContainers](https://github.com/dotnet-architecture/eShopOnContainers/blob/dev/src/Services/Ordering/Ordering.API/Infrastructure/AutofacModules/MediatorModule.cs) :

```csharp
public class MediatorModule : Autofac.Module
{
    protected override void Load(ContainerBuilder builder)
    {
        // Other registrations ...
        // Register the DomainEventHandler classes (they implement IAsyncNotificationHandler<>)
        // in assembly holding the Domain Events
        builder.RegisterAssemblyTypes(typeof(ValidateOrAddBuyerAggregateWhenOrderStartedDomainEventHandler)
                                       .GetTypeInfo().Assembly)
                                         .AsClosedTypesOf(typeof(IAsyncNotificationHandler<>));
        // Other registrations ...
    }
}
```

Le code identifie tout d’abord l’assembly qui contient les gestionnaires d’événements de domaine en recherchant l’assembly qui contient l’un des gestionnaires (en utilisant typeof(ValidateOrAddBuyerAggregateWhenXxxx). Toutefois, vous auriez pu choisir n’importe quel autre gestionnaire d’événements pour rechercher l’assembly. Étant donné que tous les gestionnaires d’événements implémentent l’interface IAsyncNotificationHandler, le code recherche donc uniquement ces types et inscrit tous les gestionnaires d’événements.

### <a name="how-to-subscribe-to-domain-events"></a>Comment s’abonner aux événements de domaine

Lorsque vous utilisez MediatR, chaque gestionnaire d’événements doit utiliser un type d’événement fourni par le paramètre générique de l’interface INotificationHandler, comme vous pouvez le voir dans le code suivant :

```csharp
public class ValidateOrAddBuyerAggregateWhenOrderStartedDomainEventHandler
  : IAsyncNotificationHandler<OrderStartedDomainEvent>
```

En fonction de la relation qui existe entre l’événement et le gestionnaire d’événements, que l’on peut voir comme l’abonnement, l’artefact MediatR peut découvrir tous les gestionnaires d’événements pour chaque événement, et déclencher chacun de ces gestionnaires.

### <a name="how-to-handle-domain-events"></a>Comment gérer les événements de domaine

Enfin, le gestionnaire d’événements implémente généralement le code de la couche Application qui utilise les dépôts de l’infrastructure pour obtenir les agrégats supplémentaires nécessaires et pour exécuter la logique de domaine d’effet secondaire. Le [code de gestionnaire d’événements de domaine de l’application eShopOnContainers](https://github.com/dotnet-architecture/eShopOnContainers/blob/dev/src/Services/Ordering/Ordering.API/Application/DomainEventHandlers/OrderStartedEvent/ValidateOrAddBuyerAggregateWhenOrderStartedDomainEventHandler.cs) suivant montre un exemple d’implémentation.

```csharp
public class ValidateOrAddBuyerAggregateWhenOrderStartedDomainEventHandler
                   : INotificationHandler<OrderStartedDomainEvent>
{
    private readonly ILoggerFactory _logger;
    private readonly IBuyerRepository<Buyer> _buyerRepository;
    private readonly IIdentityService _identityService;

    public ValidateOrAddBuyerAggregateWhenOrderStartedDomainEventHandler(
        ILoggerFactory logger,
        IBuyerRepository<Buyer> buyerRepository,
        IIdentityService identityService)
    {
        // ...Parameter validations...
    }

    public async Task Handle(OrderStartedDomainEvent orderStartedEvent)
    {
        var cardTypeId = (orderStartedEvent.CardTypeId != 0) ? orderStartedEvent.CardTypeId : 1;        
        var userGuid = _identityService.GetUserIdentity();
        var buyer = await _buyerRepository.FindAsync(userGuid);
        bool buyerOriginallyExisted = (buyer == null) ? false : true;

        if (!buyerOriginallyExisted)
        {
            buyer = new Buyer(userGuid);
        }

        buyer.VerifyOrAddPaymentMethod(cardTypeId,
                                       $"Payment Method on {DateTime.UtcNow}",
                                       orderStartedEvent.CardNumber,
                                       orderStartedEvent.CardSecurityNumber,
                                       orderStartedEvent.CardHolderName,
                                       orderStartedEvent.CardExpiration,
                                       orderStartedEvent.Order.Id);

        var buyerUpdated = buyerOriginallyExisted ? _buyerRepository.Update(buyer) 
                                                                      : _buyerRepository.Add(buyer);

        await _buyerRepository.UnitOfWork
                .SaveEntitiesAsync();

        // Logging code using buyerUpdated info, etc.
    }
}
```

Le code du gestionnaire d’événements de domaine précédent est considéré comme du code de couche Application, car il utilise des dépôts d’infrastructure, comme expliqué dans la section suivante concernant la couche Persistance d’infrastructure. Les gestionnaires d’événements peuvent également utiliser d’autres composants d’infrastructure.

#### <a name="domain-events-can-generate-integration-events-to-be-published-outside-of-the-microservice-boundaries"></a>Les événements de domaine peuvent générer des événements d’intégration devant être publiés en dehors des limites du microservice.

Enfin, il est important de mentionner qu’il est parfois utile de propager des événements sur plusieurs microservices. C’est considéré comme un événement d’intégration, qui peut être publié via un bus d’événements à partir de n’importe quel gestionnaire d’événements de domaine.

## <a name="conclusions-on-domain-events"></a>Conclusions sur les événements de domaine

Comme nous l’avons vu, les événements de domaine permettent d’implémenter explicitement les effets secondaires des modifications apportées à votre domaine. Pour utiliser la terminologie DDD, les événements de domaine permettent d’implémenter explicitement des effets secondaires sur un ou plusieurs agrégats. Si vous le souhaitez, pour une meilleure scalabilité et un impact moindre sur les verrous de base de données, utilisez la cohérence à terme entre les agrégats d’un même domaine.

## <a name="additional-resources"></a>Ressources supplémentaires

-   **Greg Young. What is a Domain Event?**
    [*http://codebetter.com/gregyoung/2010/04/11/what-is-a-domain-event/*](http://codebetter.com/gregyoung/2010/04/11/what-is-a-domain-event/)

-   **Jan Stenberg. Domain Events and Eventual Consistency**
    [*https://www.infoq.com/news/2015/09/domain-events-consistency*](https://www.infoq.com/news/2015/09/domain-events-consistency)

-   **Jimmy Bogard. A better domain events pattern**
    [*https://lostechies.com/jimmybogard/2014/05/13/a-better-domain-events-pattern/*](https://lostechies.com/jimmybogard/2014/05/13/a-better-domain-events-pattern/)

-   **Vaughn Vernon. Effective Aggregate Design Part II: Making Aggregates Work Together**
    [*http://dddcommunity.org/wp-content/uploads/files/pdf\_articles/Vernon\_2011\_2.pdf*](https://dddcommunity.org/wp-content/uploads/files/pdf_articles/Vernon_2011_2.pdf)

-   **Jimmy Bogard. Strengthening your domain: Domain Events**
    *<https://lostechies.com/jimmybogard/2010/04/08/strengthening-your-domain-domain-events/> *

-   **Tony Truong. Domain Events Pattern Example**
    [*https://www.tonytruong.net/domain-events-pattern-example/*](https://www.tonytruong.net/domain-events-pattern-example/)

-   **Udi Dahan. How to create fully encapsulated Domain Models**
    [*http://udidahan.com/2008/02/29/how-to-create-fully-encapsulated-domain-models/*](http://udidahan.com/2008/02/29/how-to-create-fully-encapsulated-domain-models/)

-   **Udi Dahan. Domain Events – Take 2**
    [*http://udidahan.com/2008/08/25/domain-events-take-2/*](http://udidahan.com/2008/08/25/domain-events-take-2/%20)

-   **Udi Dahan. Domain Events – Salvation**
    [*http://udidahan.com/2009/06/14/domain-events-salvation/*](http://udidahan.com/2009/06/14/domain-events-salvation/)

-   **Jan Kronquist. Don’t publish Domain Events, return them!**
    [*https://blog.jayway.com/2013/06/20/dont-publish-domain-events-return-them/*](https://blog.jayway.com/2013/06/20/dont-publish-domain-events-return-them/)

-   **Cesar de la Torre. Domain Events vs. Integration Events in DDD and microservices architectures**
    [*https://blogs.msdn.microsoft.com/cesardelatorre/2017/02/07/domain-events-vs-integration-events-in-domain-driven-design-and-microservices-architectures/*](https://blogs.msdn.microsoft.com/cesardelatorre/2017/02/07/domain-events-vs-integration-events-in-domain-driven-design-and-microservices-architectures/)


>[!div class="step-by-step"]
[précédent] (client-side-validation.md) [suivant] (infrastructure-persistence-layer-design.md)
