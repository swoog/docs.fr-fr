---
title: Implémentation de la couche de persistance de l’infrastructure avec Entity Framework Core
description: Architecture des microservices .NET pour les applications .NET en conteneur | Implémentation de la couche de persistance de l’infrastructure avec Entity Framework Core
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 12/12/2017
ms.openlocfilehash: 6003252d7e87428c7f954b57c3b67a041e3f3b15
ms.sourcegitcommit: 979597cd8055534b63d2c6ee8322938a27d0c87b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37106474"
---
# <a name="implementing-the-infrastructure-persistence-layer-with-entity-framework-core"></a><span data-ttu-id="0327e-103">Implémentation de la couche de persistance de l’infrastructure avec Entity Framework Core</span><span class="sxs-lookup"><span data-stu-id="0327e-103">Implementing the infrastructure persistence layer with Entity Framework Core</span></span>

<span data-ttu-id="0327e-104">Quand vous utilisez des bases de données relationnelles telles que SQL Server, Oracle ou PostgreSQL, une approche recommandée consiste à implémenter la couche de persistance en fonction d’Entity Framework (EF).</span><span class="sxs-lookup"><span data-stu-id="0327e-104">When you use relational databases such as SQL Server, Oracle, or PostgreSQL, a recommended approach is to implement the persistence layer based on Entity Framework (EF).</span></span> <span data-ttu-id="0327e-105">EF prend en charge LINQ et fournit des objets fortement typés pour votre modèle, ainsi qu’une persistance simplifiée dans votre base de données.</span><span class="sxs-lookup"><span data-stu-id="0327e-105">EF supports LINQ and provides strongly typed objects for your model, as well as simplified persistence into your database.</span></span>

<span data-ttu-id="0327e-106">Entity Framework présente un long historique dans le cadre du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="0327e-106">Entity Framework has a long history as part of the .NET Framework.</span></span> <span data-ttu-id="0327e-107">Quand vous utilisez .NET Core, vous devez également utiliser Entity Framework Core, qui s’exécute sur Windows ou Linux de la même façon que .NET Core.</span><span class="sxs-lookup"><span data-stu-id="0327e-107">When you use .NET Core, you should also use Entity Framework Core, which runs on Windows or Linux in the same way as .NET Core.</span></span> <span data-ttu-id="0327e-108">EF Core est une réécriture complète d’Entity Framework, implémentée avec un encombrement beaucoup plus faible et d’importantes améliorations en matière de performances.</span><span class="sxs-lookup"><span data-stu-id="0327e-108">EF Core is a complete rewrite of Entity Framework, implemented with a much smaller footprint and important improvements in performance.</span></span>

## <a name="introduction-to-entity-framework-core"></a><span data-ttu-id="0327e-109">Introduction à Entity Framework Core</span><span class="sxs-lookup"><span data-stu-id="0327e-109">Introduction to Entity Framework Core</span></span>

<span data-ttu-id="0327e-110">Entity Framework (EF) Core est une version légère, extensible et multiplateforme de la technologie d’accès aux données Entity Framework populaire.</span><span class="sxs-lookup"><span data-stu-id="0327e-110">Entity Framework (EF) Core is a lightweight, extensible, and cross-platform version of the popular Entity Framework data access technology.</span></span> <span data-ttu-id="0327e-111">Elle a été introduite avec .NET Core au milieu de l’année 2016.</span><span class="sxs-lookup"><span data-stu-id="0327e-111">It was introduced with .NET Core in mid-2016.</span></span>

<span data-ttu-id="0327e-112">Dans la mesure où une introduction à EF Core est déjà disponible dans la documentation Microsoft, nous indiquons simplement ici les liens vers ces informations.</span><span class="sxs-lookup"><span data-stu-id="0327e-112">Since an introduction to EF Core is already available in Microsoft documentation, here we simply provide links to that information.</span></span>

#### <a name="additional-resources"></a><span data-ttu-id="0327e-113">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="0327e-113">Additional resources</span></span>

-   <span data-ttu-id="0327e-114">**Entity Framework Core**
    [*https://docs.microsoft.com/ef/core/*](https://docs.microsoft.com/ef/core/)</span><span class="sxs-lookup"><span data-stu-id="0327e-114">**Entity Framework Core**
[*https://docs.microsoft.com/ef/core/*](https://docs.microsoft.com/ef/core/)</span></span>

-   <span data-ttu-id="0327e-115">**Bien démarrer avec ASP.NET Core et Entity Framework Core à l’aide de Visual Studio**
    [*https://docs.microsoft.com/aspnet/core/data/ef-mvc/*](https://docs.microsoft.com/aspnet/core/data/ef-mvc/)</span><span class="sxs-lookup"><span data-stu-id="0327e-115">**Getting started with ASP.NET Core and Entity Framework Core using Visual Studio**
[*https://docs.microsoft.com/aspnet/core/data/ef-mvc/*](https://docs.microsoft.com/aspnet/core/data/ef-mvc/)</span></span>

-   <span data-ttu-id="0327e-116">**Classe DbContext**
    [*https://docs.microsoft.com/ef/core/api/microsoft.entityframeworkcore.dbcontext*](https://docs.microsoft.com/ef/core/api/microsoft.entityframeworkcore.dbcontext)</span><span class="sxs-lookup"><span data-stu-id="0327e-116">**DbContext Class**
[*https://docs.microsoft.com/ef/core/api/microsoft.entityframeworkcore.dbcontext*](https://docs.microsoft.com/ef/core/api/microsoft.entityframeworkcore.dbcontext)</span></span>

-   <span data-ttu-id="0327e-117">**Comparer EF Core et EF6.x**
    [*https://docs.microsoft.com/ef/efcore-and-ef6/index*](https://docs.microsoft.com/ef/efcore-and-ef6/index)</span><span class="sxs-lookup"><span data-stu-id="0327e-117">**Compare EF Core & EF6.x**
[*https://docs.microsoft.com/ef/efcore-and-ef6/index*](https://docs.microsoft.com/ef/efcore-and-ef6/index)</span></span>

## <a name="infrastructure-in-entity-framework-core-from-a-ddd-perspective"></a><span data-ttu-id="0327e-118">Infrastructure dans Entity Framework Core à partir d’une perspective DDD</span><span class="sxs-lookup"><span data-stu-id="0327e-118">Infrastructure in Entity Framework Core from a DDD perspective</span></span>

<span data-ttu-id="0327e-119">D’un point de vue DDD, une fonctionnalité importante d’EF est la possibilité d’utiliser les entités de domaine OCT, également désignées dans la terminologie EF sous le nom *d’entités Code First*  OCT.</span><span class="sxs-lookup"><span data-stu-id="0327e-119">From a DDD point of view, an important capability of EF is the ability to use POCO domain entities, also known in EF terminology as POCO *code-first entities*.</span></span> <span data-ttu-id="0327e-120">Si vous utilisez des entités de domaine OCT, vos classes de modèle de domaine ignorent la persistance, selon les principes [d’ignorance de la persistance](http://deviq.com/persistence-ignorance/) et [d’ignorance de l’infrastructure](https://ayende.com/blog/3137/infrastructure-ignorance).</span><span class="sxs-lookup"><span data-stu-id="0327e-120">If you use POCO domain entities, your domain model classes are persistence-ignorant, following the [Persistence Ignorance](http://deviq.com/persistence-ignorance/) and the [Infrastructure Ignorance](https://ayende.com/blog/3137/infrastructure-ignorance) principles.</span></span>

<span data-ttu-id="0327e-121">Selon les modèles DDD, vous devez encapsuler le comportement et les règles du domaine au sein de la classe d’entité pour qu’elle puisse contrôler les règles, les validations et les invariants lors de l’accès à toute collection.</span><span class="sxs-lookup"><span data-stu-id="0327e-121">Per DDD patterns, you should encapsulate domain behavior and rules within the entity class itself, so it can control invariants, validations, and rules when accessing any collection.</span></span> <span data-ttu-id="0327e-122">Par conséquent, il est déconseillé dans DDD d’autoriser un accès public à des collections d’objets de valeur ou d’entités enfants.</span><span class="sxs-lookup"><span data-stu-id="0327e-122">Therefore, it is not a good practice in DDD to allow public access to collections of child entities or value objects.</span></span> <span data-ttu-id="0327e-123">Au lieu de cela, vous pouvez exposer des méthodes qui contrôlent comment et quand vos champs et collections de propriétés peuvent être mis à jour, ainsi que le comportement et les actions qui doivent se produire à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="0327e-123">Instead, you want to expose methods that control how and when your fields and property collections can be updated, and what behavior and actions should occur when that happens.</span></span>

<span data-ttu-id="0327e-124">Depuis EF Core 1.1, pour répondre à ces exigences DDD, vous pouvez avoir des champs tout simples dans vos entités au lieu de propriétés publiques.</span><span class="sxs-lookup"><span data-stu-id="0327e-124">Since EF Core 1.1, to satisfy those DDD requirements, you can have plain fields in your entities instead of public properties.</span></span> <span data-ttu-id="0327e-125">Si vous ne souhaitez pas qu’un champ d’entité soit accessible en externe, il vous suffit de créer l’attribut ou le champ au lieu d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="0327e-125">If you do not want an entity field to be externally accessible, you can just create the attribute or field instead of a property.</span></span> <span data-ttu-id="0327e-126">Vous pouvez également utiliser des méthodes setter de propriétés privées.</span><span class="sxs-lookup"><span data-stu-id="0327e-126">You can also use private property setters.</span></span>

<span data-ttu-id="0327e-127">De la même façon, vous pouvez maintenant accéder en lecture seule aux collections à l’aide d’une propriété publique typée comme `IReadOnlyCollection<T>`, qui est associée à un membre de champ privé pour la collection (tel qu’un `List<T>`) dans votre entité qui s’appuie sur EF pour la persistance.</span><span class="sxs-lookup"><span data-stu-id="0327e-127">In a similar way, you can now have read-only access to collections by using a public property typed as  `IReadOnlyCollection<T>`, which is backed by a private field member for the collection (like a `List<T>`) in your entity that relies on EF for persistence.</span></span> <span data-ttu-id="0327e-128">Les versions précédentes d’Entity Framework exigeaient que les propriétés de collection prennent en charge `ICollection<T>`, ce qui signifiait que tout développeur utilisant la classe d’entité parente pouvait ajouter ou supprimer des éléments via ses collections de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0327e-128">Previous versions of Entity Framework required collection properties to support `ICollection<T>`, which meant that any developer using the parent entity class could add or remove items through its property collections.</span></span> <span data-ttu-id="0327e-129">Cette possibilité s’oppose aux modèles recommandés dans DDD.</span><span class="sxs-lookup"><span data-stu-id="0327e-129">That possibility would be against the recommended patterns in DDD.</span></span>

<span data-ttu-id="0327e-130">Vous pouvez utiliser une collection privée tout en exposant un objet `IReadOnlyCollection<T>` en lecture seule, comme illustré dans l’exemple de code suivant :</span><span class="sxs-lookup"><span data-stu-id="0327e-130">You can use a private collection while exposing a read-only `IReadOnlyCollection<T>` object, as shown in the following code example:</span></span>

```csharp
public class Order : Entity
{
    // Using private fields, allowed since EF Core 1.1
    private DateTime _orderDate;
    // Other fields ...

    private readonly List<OrderItem> _orderItems; 
    public IReadOnlyCollection<OrderItem> OrderItems => _orderItems;

    protected Order() { }

    public Order(int buyerId, int paymentMethodId, Address address)
    {
        // Initializations ...
    }

    public void AddOrderItem(int productId, string productName,
                             decimal unitPrice, decimal discount,
                             string pictureUrl, int units = 1)
    {
        // Validation logic...

        var orderItem = new OrderItem(productId, productName, 
                                      unitPrice, discount,
                                      pictureUrl, units);
        _orderItems.Add(orderItem);
    }
}
```

<span data-ttu-id="0327e-131">Notez que la propriété `OrderItems` est uniquement accessible en lecture seule avec `IReadOnlyCollection<OrderItem>`.</span><span class="sxs-lookup"><span data-stu-id="0327e-131">Note that the `OrderItems` property can only be accessed as read-only using `IReadOnlyCollection<OrderItem>`.</span></span> <span data-ttu-id="0327e-132">Ce type est en lecture seule et donc protégé contre les mises à jour externes standard.</span><span class="sxs-lookup"><span data-stu-id="0327e-132">This type is read-only so it is protected against regular external updates.</span></span> 

<span data-ttu-id="0327e-133">EF Core offre un moyen de mapper le modèle de domaine à la base de données physique sans « contaminer » le modèle de domaine.</span><span class="sxs-lookup"><span data-stu-id="0327e-133">EF Core provides a way to map the domain model to the physical database without "contaminating" the domain model.</span></span> <span data-ttu-id="0327e-134">Il s’agit de code .NET purement OCT, étant donné que l’action de mappage est implémentée dans la couche de persistance.</span><span class="sxs-lookup"><span data-stu-id="0327e-134">It is pure .NET POCO code, because the mapping action is implemented in the persistence layer.</span></span> <span data-ttu-id="0327e-135">Dans cette action de mappage, vous devez configurer le mappage de champs à base de données.</span><span class="sxs-lookup"><span data-stu-id="0327e-135">In that mapping action, you need to configure the fields-to-database mapping.</span></span> <span data-ttu-id="0327e-136">Dans l’exemple suivant d’une méthode OnModelCreating, le code en surbrillance indique à EF Core d’accéder à la propriété OrderItems via son champ.</span><span class="sxs-lookup"><span data-stu-id="0327e-136">In the following example of an OnModelCreating method, the highlighted code tells EF Core to access the OrderItems property through its field.</span></span>

```csharp
// At OrderingContext.cs from eShopOnContainers
protected override void OnModelCreating(ModelBuilder modelBuilder)
{
   // ...
   modelBuilder.ApplyConfiguration(new OrderEntityTypeConfiguration());
   // Other entities’ configuration ...
}

// At OrderEntityTypeConfiguration.cs from eShopOnContainers
class OrderEntityTypeConfiguration : IEntityTypeConfiguration<Order>
{
    public void Configure(EntityTypeBuilder<Order> orderConfiguration)
    {
        orderConfiguration.ToTable("orders", OrderingContext.DEFAULT_SCHEMA);
        // Other configuration

        var navigation = 
              orderConfiguration.Metadata.FindNavigation(nameof(Order.OrderItems));

        //EF access the OrderItem collection property through its backing field
        navigation.SetPropertyAccessMode(PropertyAccessMode.Field);

        // Other configuration
    }
}
```

<span data-ttu-id="0327e-137">Quand vous utilisez des champs au lieu de propriétés, l’entité OrderItem est conservée comme si elle avait une propriété List&lt;OrderItem&gt;.</span><span class="sxs-lookup"><span data-stu-id="0327e-137">When you use fields instead of properties, the OrderItem entity is persisted just as if it had a List&lt;OrderItem&gt; property.</span></span> <span data-ttu-id="0327e-138">Toutefois, elle expose un seul accesseur, la méthode `AddOrderItem` pour ajouter de nouveaux articles à la commande.</span><span class="sxs-lookup"><span data-stu-id="0327e-138">However, it exposes a single accessor, the `AddOrderItem` method for adding new items to the order.</span></span> <span data-ttu-id="0327e-139">Par conséquent, le comportement et les données sont reliés et seront cohérents dans n’importe quel code d’application qui utilise le modèle de domaine.</span><span class="sxs-lookup"><span data-stu-id="0327e-139">As a result, behavior and data are tied together and will be consistent throughout any application code that uses the domain model.</span></span>

## <a name="implementing-custom-repositories-with-entity-framework-core"></a><span data-ttu-id="0327e-140">Implémentation de dépôts personnalisés avec Entity Framework Core</span><span class="sxs-lookup"><span data-stu-id="0327e-140">Implementing custom repositories with Entity Framework Core</span></span>

<span data-ttu-id="0327e-141">Au niveau de l’implémentation, un dépôt est simplement une classe avec un code de persistance de données coordonné par une unité de travail (DBContext dans EF Core) quand vous effectuez des mises à jour, comme indiqué dans la classe suivante :</span><span class="sxs-lookup"><span data-stu-id="0327e-141">At the implementation level, a repository is simply a class with data persistence code coordinated by a unit of work (DBContext in EF Core) when performing updates, as shown in the following class:</span></span>

```csharp
// using statements...
namespace Microsoft.eShopOnContainers.Services.Ordering.Infrastructure.Repositories
{
    public class BuyerRepository : IBuyerRepository
    {
        private readonly OrderingContext _context;
        public IUnitOfWork UnitOfWork
        {
            get
            {
                return _context;
            }
        }

        public BuyerRepository(OrderingContext context)
        {
            _context = context ?? throw new ArgumentNullException(nameof(context));
        }

        public Buyer Add(Buyer buyer)
        {
            return _context.Buyers.Add(buyer).Entity; 
        }

        public async Task<Buyer> FindAsync(string BuyerIdentityGuid)
        {
            var buyer = await _context.Buyers
                .Include(b => b.Payments)
                .Where(b => b.FullName == BuyerIdentityGuid)
                .SingleOrDefaultAsync();

            return buyer;
        }
    }
}
```

<span data-ttu-id="0327e-142">Notez que l’interface IBuyerRepository provient de la couche de modèle de domaine en tant que contrat.</span><span class="sxs-lookup"><span data-stu-id="0327e-142">Note that the IBuyerRepository interface comes from the domain model layer as a contract.</span></span> <span data-ttu-id="0327e-143">Toutefois, l’implémentation du dépôt est effectuée au niveau de la couche de persistance et de la couche d’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="0327e-143">However, the repository implementation is done at the persistence and infrastructure layer.</span></span>

<span data-ttu-id="0327e-144">DBContext EF passe par le constructeur via une injection de dépendances.</span><span class="sxs-lookup"><span data-stu-id="0327e-144">The EF DbContext comes through the constructor through Dependency Injection.</span></span> <span data-ttu-id="0327e-145">Elle est partagée entre plusieurs dépôts dans la même portée de requête HTTP grâce à sa durée de vie par défaut (ServiceLifetime.Scoped) dans le conteneur IoC (qui peut également être explicitement défini avec services.AddDbContext&lt;&gt;).</span><span class="sxs-lookup"><span data-stu-id="0327e-145">It is shared between multiple repositories within the same HTTP request scope, thanks to its default lifetime (ServiceLifetime.Scoped) in the IoC container (which can also be explicitly set with services.AddDbContext&lt;&gt;).</span></span>

### <a name="methods-to-implement-in-a-repository-updates-or-transactions-versus-queries"></a><span data-ttu-id="0327e-146">Méthodes à implémenter dans un dépôt (mises à jour ou transactions et requêtes)</span><span class="sxs-lookup"><span data-stu-id="0327e-146">Methods to implement in a repository (updates or transactions versus queries)</span></span>

<span data-ttu-id="0327e-147">Dans chaque classe de dépôt, vous devez placer les méthodes de persistance qui mettent à jour l’état des entités contenues par son agrégat associé.</span><span class="sxs-lookup"><span data-stu-id="0327e-147">Within each repository class, you should put the persistence methods that update the state of entities contained by its related aggregate.</span></span> <span data-ttu-id="0327e-148">Gardez à l’esprit qu’il existe une relation un-à-un entre un agrégat et son dépôt associé.</span><span class="sxs-lookup"><span data-stu-id="0327e-148">Remember there is one-to-one relationship between an aggregate and its related repository.</span></span> <span data-ttu-id="0327e-149">Tenez compte du fait qu’un objet entité racine d’agrégat peut avoir des entités enfants incorporées dans son graphique EF.</span><span class="sxs-lookup"><span data-stu-id="0327e-149">Take into account that an aggregate root entity object might have embedded child entities within its EF graph.</span></span> <span data-ttu-id="0327e-150">Par exemple, un acheteur peut avoir plusieurs modes de paiement en tant qu’entités enfants associées.</span><span class="sxs-lookup"><span data-stu-id="0327e-150">For example, a buyer might have multiple payment methods as related child entities.</span></span>

<span data-ttu-id="0327e-151">Étant donné que l’approche pour le microservice de commandes dans eShopOnContainers repose également sur CQS/CQRS, la plupart des requêtes ne sont pas implémentées dans les dépôts personnalisés.</span><span class="sxs-lookup"><span data-stu-id="0327e-151">Since the approach for the ordering microservice in eShopOnContainers is also based on CQS/CQRS, most of the queries are not implemented in custom repositories.</span></span> <span data-ttu-id="0327e-152">Les développeurs ont la possibilité de créer les requêtes et les jointures dont ils ont besoin pour la couche de présentation sans les restrictions imposées par les agrégats, les dépôts personnalisés par agrégat et DDD en général.</span><span class="sxs-lookup"><span data-stu-id="0327e-152">Developers have the freedom to create the queries and joins they need for the presentation layer without the restrictions imposed by aggregates, custom repositories per aggregate, and DDD in general.</span></span> <span data-ttu-id="0327e-153">La plupart des dépôts personnalisés suggérés par ce guide ont plusieurs méthodes de mise à jour ou transactionnelles, mais uniquement les méthodes de requête nécessaires pour obtenir les données à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="0327e-153">Most of the custom repositories suggested by this guide have several update or transactional methods but just the query methods needed to get data to be updated.</span></span> <span data-ttu-id="0327e-154">Par exemple, le dépôt BuyerRepository implémente une méthode FindAsync, car l’application doit savoir si un acheteur donné existe avant d’en créer un nouveau lié à la commande.</span><span class="sxs-lookup"><span data-stu-id="0327e-154">For example, the BuyerRepository repository implements a FindAsync method, because the application needs to know whether a particular buyer exists before creating a new buyer related to the order.</span></span>

<span data-ttu-id="0327e-155">Toutefois, les méthodes de requête réelles pour obtenir des données à envoyer à la couche de présentation ou aux applications clientes sont implémentées, comme indiqué, dans les requêtes CQRS basées sur des requêtes flexibles à l’aide de Dapper.</span><span class="sxs-lookup"><span data-stu-id="0327e-155">However, the real query methods to get data to send to the presentation layer or client apps are implemented, as mentioned, in the CQRS queries based on flexible queries using Dapper.</span></span>

### <a name="using-a-custom-repository-versus-using-ef-dbcontext-directly"></a><span data-ttu-id="0327e-156">Comparaison entre l’utilisation d’un dépôt personnalisé et l’utilisation directe de DbContext EF</span><span class="sxs-lookup"><span data-stu-id="0327e-156">Using a custom repository versus using EF DbContext directly</span></span>

<span data-ttu-id="0327e-157">La classe DbContext Entity Framework est basée sur les modèles d’unité de travail et de dépôt, et peut servir directement à partir de votre code, par exemple à partir d’un contrôleur ASP.NET Core MVC.</span><span class="sxs-lookup"><span data-stu-id="0327e-157">The Entity Framework DbContext class is based on the Unit of Work and Repository patterns, and can be used directly from your code, such as from an ASP.NET Core MVC controller.</span></span> <span data-ttu-id="0327e-158">Il s’agit de la façon dont vous pouvez créer le code le plus simple, comme dans le microservice du catalogue CRUD dans eShopOnContainers.</span><span class="sxs-lookup"><span data-stu-id="0327e-158">That is the way you can create the simplest code, as in the CRUD catalog microservice in eShopOnContainers.</span></span> <span data-ttu-id="0327e-159">Quand vous voulez le code le plus simple possible, vous pouvez utiliser directement la classe DbContext, comme de nombreux développeurs.</span><span class="sxs-lookup"><span data-stu-id="0327e-159">In cases where you want the simplest code possible, you might want to directly use the DbContext class, as many developers do.</span></span>

<span data-ttu-id="0327e-160">Toutefois, l’implémentation de dépôts personnalisés présente plusieurs avantages lors de l’implémentation de microservices ou d’applications plus complexes.</span><span class="sxs-lookup"><span data-stu-id="0327e-160">However, implementing custom repositories provides several benefits when implementing more complex microservices or applications.</span></span> <span data-ttu-id="0327e-161">Les modèles d’unité de travail et de dépôt sont destinés à encapsuler la couche de persistance de l’infrastructure afin qu’elle soit découplée de l’application et des couches de modèle de domaine.</span><span class="sxs-lookup"><span data-stu-id="0327e-161">The Unit of Work and Repository patterns are intended to encapsulate the infrastructure persistence layer so it is decoupled from the application and domain model layers.</span></span> <span data-ttu-id="0327e-162">L’implémentation de ces modèles peut faciliter l’utilisation de dépôts fictifs simulant l’accès à la base de données.</span><span class="sxs-lookup"><span data-stu-id="0327e-162">Implementing these patterns can facilitate the use of mock repositories simulating access to the database.</span></span>

<span data-ttu-id="0327e-163">Dans la Figure 9-18, vous pouvez voir les différences entre le fait de ne pas utiliser de dépôts (utilisation directe de DbContext EF) et l’utilisation de dépôts qui facilitent la simulation de ces dépôts.</span><span class="sxs-lookup"><span data-stu-id="0327e-163">In Figure 9-18 you can see the differences between not using repositories (directly using the EF DbContext) versus using repositories which make it easier to mock those repositories.</span></span>

![](./media/image19.png)

<span data-ttu-id="0327e-164">**Figure 9-18**.</span><span class="sxs-lookup"><span data-stu-id="0327e-164">**Figure 9-18**.</span></span> <span data-ttu-id="0327e-165">Utilisation de dépôts personnalisés par rapport à un simple DbContext</span><span class="sxs-lookup"><span data-stu-id="0327e-165">Using custom repositories versus a plain DbContext</span></span>

<span data-ttu-id="0327e-166">Il existe plusieurs alternatives lors de la simulation.</span><span class="sxs-lookup"><span data-stu-id="0327e-166">There are multiple alternatives when mocking.</span></span> <span data-ttu-id="0327e-167">Vous pouvez simuler uniquement les dépôts ou l’intégralité d’une unité de travail.</span><span class="sxs-lookup"><span data-stu-id="0327e-167">You could mock just repositories or you could mock a whole unit of work.</span></span> <span data-ttu-id="0327e-168">Généralement, la simulation des dépôts uniquement est suffisante, et la tâche complexe d’abstraction et de simulation de l’intégralité d’une unité de travail n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0327e-168">Usually mocking just the repositories is enough, and the complexity to abstract and mock a whole unit of work is usually not needed.</span></span>

<span data-ttu-id="0327e-169">Plus tard, quand nous nous concentrerons sur la couche d’application, vous verrez comment fonctionne l’injection de dépendances dans ASP.NET Core et comment elle est implémentée lors de l’utilisation de dépôts.</span><span class="sxs-lookup"><span data-stu-id="0327e-169">Later, when we focus on the application layer, you will see how Dependency Injection works in ASP.NET Core and how it is implemented when using repositories.</span></span>

<span data-ttu-id="0327e-170">En bref, les dépôts personnalisés vous permettent de tester plus facilement le code avec des tests unitaires qui ne sont pas affectés par l’état de la couche Données.</span><span class="sxs-lookup"><span data-stu-id="0327e-170">In short, custom repositories allow you to test code more easily with unit tests that are not impacted by the data tier state.</span></span> <span data-ttu-id="0327e-171">Si vous exécutez des tests qui accèdent également à la base de données réelle via Entity Framework, il ne s’agit pas de tests unitaires, mais de tests d’intégration qui sont beaucoup plus lents.</span><span class="sxs-lookup"><span data-stu-id="0327e-171">If you run tests that also access the actual database through the Entity Framework, they are not unit tests but integration tests, which are a lot slower.</span></span>

<span data-ttu-id="0327e-172">Si vous utilisiez DbContext directement, votre seul choix serait d’exécuter des tests unitaires à l’aide de SQL Server en mémoire avec des données prévisibles pour les tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="0327e-172">If you were using DbContext directly, the only choice you would have would be to run unit tests by using an in-memory SQL Server with predictable data for unit tests.</span></span> <span data-ttu-id="0327e-173">Vous ne pourriez pas contrôler les objets fictifs et les données fictives de la même manière au niveau du dépôt.</span><span class="sxs-lookup"><span data-stu-id="0327e-173">You would not be able to control mock objects and fake data in the same way at the repository level.</span></span> <span data-ttu-id="0327e-174">Bien entendu, vous pouvez toujours tester les contrôleurs MVC.</span><span class="sxs-lookup"><span data-stu-id="0327e-174">Of course, you could always test the MVC controllers.</span></span>

## <a name="ef-dbcontext-and-iunitofwork-instance-lifetime-in-your-ioc-container"></a><span data-ttu-id="0327e-175">Durée de vie des instances DbContext EF et IUnitOfWork dans votre conteneur IoC</span><span class="sxs-lookup"><span data-stu-id="0327e-175">EF DbContext and IUnitOfWork instance lifetime in your IoC container</span></span>

<span data-ttu-id="0327e-176">L’objet DbContext (exposé comme objet IUnitOfWork) peut devoir être partagé entre plusieurs dépôts au sein de la même portée de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="0327e-176">The DbContext object (exposed as an IUnitOfWork object) might need to be shared among multiple repositories within the same HTTP request scope.</span></span> <span data-ttu-id="0327e-177">Par exemple, cela est vrai quand l’opération en cours d’exécution doit gérer plusieurs agrégats ou simplement parce que vous utilisez plusieurs instances de dépôt.</span><span class="sxs-lookup"><span data-stu-id="0327e-177">For example, this is true when the operation being executed must deal with multiple aggregates, or simply because you are using multiple repository instances.</span></span> <span data-ttu-id="0327e-178">Il est également important de mentionner que l’interface IUnitOfWork fait partie de votre couche de domaine, et n’est pas un type EF Core.</span><span class="sxs-lookup"><span data-stu-id="0327e-178">It is also important to mention that the IUnitOfWork interface is part of your domain layer, not an EF Core type.</span></span>

<span data-ttu-id="0327e-179">Pour ce faire, l’instance de l’objet DbContext doit avoir la valeur ServiceLifetime.Scoped définie pour sa durée de vie de service.</span><span class="sxs-lookup"><span data-stu-id="0327e-179">In order to do that, the instance of the DbContext object has to have its service lifetime set to ServiceLifetime.Scoped.</span></span> <span data-ttu-id="0327e-180">Il s’agit de la durée de vie par défaut lors de l’inscription d’un DbContext auprès de services.AddDbContext dans votre conteneur IoC à partir de la méthode ConfigureServices du fichier Startup.cs dans votre projet d’API web ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="0327e-180">This is the default lifetime when registering a DbContext with services.AddDbContext in your IoC container from the ConfigureServices method of the Startup.cs file in your ASP.NET Core Web API project.</span></span> <span data-ttu-id="0327e-181">Le code suivant illustre ce comportement :</span><span class="sxs-lookup"><span data-stu-id="0327e-181">The following code illustrates this.</span></span>

```csharp
public IServiceProvider ConfigureServices(IServiceCollection services)
{
    // Add framework services.
    services.AddMvc(options =>
    {
        options.Filters.Add(typeof(HttpGlobalExceptionFilter));
    }).AddControllersAsServices();

    services.AddEntityFrameworkSqlServer()
      .AddDbContext<OrderingContext>(options =>
      {
          options.UseSqlServer(Configuration["ConnectionString"],
                               sqlOptions => sqlOptions.MigrationsAssembly(typeof(Startup).GetTypeInfo().
                                                                                    Assembly.GetName().Name));
      },
      ServiceLifetime.Scoped // Note that Scoped is the default choice
                             // in AddDbContext. It is shown here only for
                             // pedagogic purposes.
      );
}
```

<span data-ttu-id="0327e-182">Le mode d’instanciation de DbContext ne doit pas être configuré comme ServiceLifetime.Transient ni ServiceLifetime.Singleton.</span><span class="sxs-lookup"><span data-stu-id="0327e-182">The DbContext instantiation mode should not be configured as ServiceLifetime.Transient or ServiceLifetime.Singleton.</span></span>

## <a name="the-repository-instance-lifetime-in-your-ioc-container"></a><span data-ttu-id="0327e-183">Durée de vie de l’instance de dépôt dans votre conteneur IoC</span><span class="sxs-lookup"><span data-stu-id="0327e-183">The repository instance lifetime in your IoC container</span></span>

<span data-ttu-id="0327e-184">De la même façon, la durée de vie du dépôt doit généralement être définie comme délimitée (InstancePerLifetimeScope dans Autofac).</span><span class="sxs-lookup"><span data-stu-id="0327e-184">In a similar way, repository’s lifetime should usually be set as scoped (InstancePerLifetimeScope in Autofac).</span></span> <span data-ttu-id="0327e-185">Cela peut également être temporaire (InstancePerDependency dans Autofac), mais votre service sera plus efficace en ce qui concerne la mémoire lors de l’utilisation de la durée de vie délimitée.</span><span class="sxs-lookup"><span data-stu-id="0327e-185">It could also be transient (InstancePerDependency in Autofac), but your service will be more efficient in regards memory when using the scoped lifetime.</span></span>

```csharp
// Registering a Repository in Autofac IoC container
builder.RegisterType<OrderRepository>()
    .As<IOrderRepository>()
    .InstancePerLifetimeScope();
```

<span data-ttu-id="0327e-186">Notez que l’utilisation de la durée de vie singleton pour le dépôt peut vous causer des problèmes d’accès concurrentiel graves quand votre DbContext a une durée de vie délimitée (InstancePerLifetimeScope), durée de vie par défaut d’un DBContext.</span><span class="sxs-lookup"><span data-stu-id="0327e-186">Note that using the singleton lifetime for the repository could cause you serious concurrency problems when your DbContext is set to scoped (InstancePerLifetimeScope) lifetime (the default lifetimes for a DBContext).</span></span>

#### <a name="additional-resources"></a><span data-ttu-id="0327e-187">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="0327e-187">Additional resources</span></span>

-   <span data-ttu-id="0327e-188">**Implémentation du dépôt et des modèles d’unité de travail dans une application ASP.NET MVC**
    [*https://www.asp.net/mvc/overview/older-versions/getting-started-with-ef-5-using-mvc-4/implementing-the-repository-and-unit-of-work-patterns-in-an-asp-net-mvc-application*](https://www.asp.net/mvc/overview/older-versions/getting-started-with-ef-5-using-mvc-4/implementing-the-repository-and-unit-of-work-patterns-in-an-asp-net-mvc-application)</span><span class="sxs-lookup"><span data-stu-id="0327e-188">**Implementing the Repository and Unit of Work Patterns in an ASP.NET MVC Application**
[*https://www.asp.net/mvc/overview/older-versions/getting-started-with-ef-5-using-mvc-4/implementing-the-repository-and-unit-of-work-patterns-in-an-asp-net-mvc-application*](https://www.asp.net/mvc/overview/older-versions/getting-started-with-ef-5-using-mvc-4/implementing-the-repository-and-unit-of-work-patterns-in-an-asp-net-mvc-application)</span></span>

-   <span data-ttu-id="0327e-189">**Jonathan Allen. Stratégies d’implémentation du modèle Dépôt avec Entity Framework, Dapper et Chain**
    [*https://www.infoq.com/articles/repository-implementation-strategies*](https://www.infoq.com/articles/repository-implementation-strategies)</span><span class="sxs-lookup"><span data-stu-id="0327e-189">**Jonathan Allen. Implementation Strategies for the Repository Pattern with Entity Framework, Dapper, and Chain**
[*https://www.infoq.com/articles/repository-implementation-strategies*](https://www.infoq.com/articles/repository-implementation-strategies)</span></span>

-   <span data-ttu-id="0327e-190">**Cesar de la Torre. Comparaison des durées de vie du service conteneur ASP.NET Core IoC avec des étendues d’instance conteneur Autofac IoC**
    [*https://blogs.msdn.microsoft.com/cesardelatorre/2017/01/26/comparing-asp-net-core-ioc-service-life-times-and-autofac-ioc-instance-scopes/*](https://blogs.msdn.microsoft.com/cesardelatorre/2017/01/26/comparing-asp-net-core-ioc-service-life-times-and-autofac-ioc-instance-scopes/)</span><span class="sxs-lookup"><span data-stu-id="0327e-190">**Cesar de la Torre. Comparing ASP.NET Core IoC container service lifetimes with Autofac IoC container instance scopes**
[*https://blogs.msdn.microsoft.com/cesardelatorre/2017/01/26/comparing-asp-net-core-ioc-service-life-times-and-autofac-ioc-instance-scopes/*](https://blogs.msdn.microsoft.com/cesardelatorre/2017/01/26/comparing-asp-net-core-ioc-service-life-times-and-autofac-ioc-instance-scopes/)</span></span>

## <a name="table-mapping"></a><span data-ttu-id="0327e-191">Mappage de tables</span><span class="sxs-lookup"><span data-stu-id="0327e-191">Table mapping</span></span>

<span data-ttu-id="0327e-192">Le mappage de tables identifie les données de table à interroger et enregistrer dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="0327e-192">Table mapping identifies the table data to be queried from and saved to the database.</span></span> <span data-ttu-id="0327e-193">Précédemment, vous avez vu comment les entités de domaine (par exemple, un produit ou domaine de commande) pouvaient servir à générer un schéma de base de données associé.</span><span class="sxs-lookup"><span data-stu-id="0327e-193">Previously you saw how domain entities (for example, a product or order domain) can be used to generate a related database schema.</span></span> <span data-ttu-id="0327e-194">EF est en grande partie conçu autour du concept de *conventions*.</span><span class="sxs-lookup"><span data-stu-id="0327e-194">EF is strongly designed around the concept of *conventions*.</span></span> <span data-ttu-id="0327e-195">Les conventions répondent aux questions telles que « Quel sera le nom d’une table ? »</span><span class="sxs-lookup"><span data-stu-id="0327e-195">Conventions address questions like “What will the name of a table be?”</span></span> <span data-ttu-id="0327e-196">ou « Quelle propriété est la clé primaire ? »</span><span class="sxs-lookup"><span data-stu-id="0327e-196">or “What property is the primary key?”</span></span> <span data-ttu-id="0327e-197">Les conventions sont généralement basées sur des noms conventionnels, par exemple il est classique que la clé primaire soit une propriété qui se termine par Id.</span><span class="sxs-lookup"><span data-stu-id="0327e-197">Conventions are typically based on conventional names—for example, it is typical for the primary key to be a property that ends with Id.</span></span>

<span data-ttu-id="0327e-198">Par convention, chaque entité est configurée pour mapper à une table avec le même nom que la propriété DbSet&lt;TEntity&gt; qui expose l’entité sur le contexte dérivé.</span><span class="sxs-lookup"><span data-stu-id="0327e-198">By convention, each entity will be set up to map to a table with the same name as the DbSet&lt;TEntity&gt; property that exposes the entity on the derived context.</span></span> <span data-ttu-id="0327e-199">Si aucune valeur DbSet&lt;TEntity&gt; n’est fournie pour l’entité donnée, le nom de classe est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0327e-199">If no DbSet&lt;TEntity&gt; value is provided for the given entity, the class name is used.</span></span>

### <a name="data-annotations-versus-fluent-api"></a><span data-ttu-id="0327e-200">Annotations de données et API Fluent</span><span class="sxs-lookup"><span data-stu-id="0327e-200">Data Annotations versus Fluent API</span></span>

<span data-ttu-id="0327e-201">Il existe de nombreuses conventions EF Core supplémentaires et la plupart d’entre elles peuvent être modifiées à l’aide des annotations de données ou de l’API Fluent, implémentée dans la méthode OnModelCreating.</span><span class="sxs-lookup"><span data-stu-id="0327e-201">There are many additional EF Core conventions, and most of them can be changed by using either data annotations or Fluent API, implemented within the OnModelCreating method.</span></span>

<span data-ttu-id="0327e-202">Les annotations de données doivent être utilisées sur les classes de modèle d’entité, ce qui représente un moyen plus intrusif du point de vue DDD.</span><span class="sxs-lookup"><span data-stu-id="0327e-202">Data annotations must be used on the entity model classes themselves, which is a more intrusive way from a DDD point of view.</span></span> <span data-ttu-id="0327e-203">En effet, vous contaminez votre modèle avec des annotations de données liées à la base de données de l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="0327e-203">This is because you are contaminating your model with data annotations related to the infrastructure database.</span></span> <span data-ttu-id="0327e-204">En revanche, l’API Fluent représente un moyen pratique de modifier la plupart des conventions et des mappages dans la couche d’infrastructure de persistance de données ; le modèle d’entité est donc propre et découplé de l’infrastructure de persistance.</span><span class="sxs-lookup"><span data-stu-id="0327e-204">On the other hand, Fluent API is a convenient way to change most conventions and mappings within your data persistence infrastructure layer, so the entity model will be clean and decoupled from the persistence infrastructure.</span></span>

### <a name="fluent-api-and-the-onmodelcreating-method"></a><span data-ttu-id="0327e-205">API Fluent et la méthode OnModelCreating</span><span class="sxs-lookup"><span data-stu-id="0327e-205">Fluent API and the OnModelCreating method</span></span>

<span data-ttu-id="0327e-206">Comme mentionné, afin de modifier les conventions et les mappages, vous pouvez utiliser la méthode OnModelCreating dans la classe DbContext.</span><span class="sxs-lookup"><span data-stu-id="0327e-206">As mentioned, in order to change conventions and mappings, you can use the OnModelCreating method in the DbContext class.</span></span> 

<span data-ttu-id="0327e-207">Le microservice de commandes dans eShopOnContainers implémente une configuration et un mappage explicites, si nécessaire, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="0327e-207">The ordering microservice in eShopOnContainers implements explicit mapping and configuration, when needed, as shown in the following code.</span></span>

```csharp
// At OrderingContext.cs from eShopOnContainers
protected override void OnModelCreating(ModelBuilder modelBuilder)
{
   // ...
   modelBuilder.ApplyConfiguration(new OrderEntityTypeConfiguration());
   // Other entities’ configuration ...
}

// At OrderEntityTypeConfiguration.cs from eShopOnContainers
class OrderEntityTypeConfiguration : IEntityTypeConfiguration<Order>
{
    public void Configure(EntityTypeBuilder<Order> orderConfiguration)
    {
            orderConfiguration.ToTable("orders", OrderingContext.DEFAULT_SCHEMA);

            orderConfiguration.HasKey(o => o.Id);

            orderConfiguration.Ignore(b => b.DomainEvents);

            orderConfiguration.Property(o => o.Id)
                .ForSqlServerUseSequenceHiLo("orderseq", OrderingContext.DEFAULT_SCHEMA);

            //Address Value Object persisted as owned entity type supported since EF Core 2.0
            orderConfiguration.OwnsOne(o => o.Address);

            orderConfiguration.Property<DateTime>("OrderDate").IsRequired();
            orderConfiguration.Property<int?>("BuyerId").IsRequired(false);
            orderConfiguration.Property<int>("OrderStatusId").IsRequired();
            orderConfiguration.Property<int?>("PaymentMethodId").IsRequired(false);
            orderConfiguration.Property<string>("Description").IsRequired(false);

            var navigation = orderConfiguration.Metadata.FindNavigation(nameof(Order.OrderItems));
            
            // DDD Patterns comment:
            //Set as field (New since EF 1.1) to access the OrderItem collection property through its field
            navigation.SetPropertyAccessMode(PropertyAccessMode.Field);

            orderConfiguration.HasOne<PaymentMethod>()
                .WithMany()
                .HasForeignKey("PaymentMethodId")
                .IsRequired(false)
                .OnDelete(DeleteBehavior.Restrict);

            orderConfiguration.HasOne<Buyer>()
                .WithMany()
                .IsRequired(false)
                .HasForeignKey("BuyerId");

            orderConfiguration.HasOne(o => o.OrderStatus)
                .WithMany()
                .HasForeignKey("OrderStatusId");
    }
}
```

<span data-ttu-id="0327e-208">Vous pouvez définir tous les mappages de l’API Fluent au sein de la même méthode OnModelCreating, mais il est recommandé de partitionner ce code et d’avoir plusieurs classes de configuration, une par entité, comme indiqué dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="0327e-208">You could set all the Fluent API mappings within the same OnModelCreating method, but it is advisable to partition that code and have multiple configuration classes, one per entity, as shown in the example.</span></span> <span data-ttu-id="0327e-209">Plus précisément pour les modèles particulièrement volumineux, il est recommandé d’avoir des classes de configuration distinctes pour la configuration de différents types d’entités.</span><span class="sxs-lookup"><span data-stu-id="0327e-209">Especially for particularly large models, it is advisable to have separate configuration classes for configuring different entity types.</span></span>

<span data-ttu-id="0327e-210">Le code dans l’exemple montre quelques déclarations et mappages explicites.</span><span class="sxs-lookup"><span data-stu-id="0327e-210">The code in the example shows a few explicit declarations and mapping.</span></span> <span data-ttu-id="0327e-211">Toutefois, les conventions EF Core effectuant un grand nombre de ces mappages automatiquement, le code réel nécessaire dans votre cas peut être moindre.</span><span class="sxs-lookup"><span data-stu-id="0327e-211">However, EF Core conventions do many of those mappings automatically, so the actual code you would need in your case might be smaller.</span></span>


### <a name="the-hilo-algorithm-in-ef-core"></a><span data-ttu-id="0327e-212">Algorithme Hi/Lo dans EF Core</span><span class="sxs-lookup"><span data-stu-id="0327e-212">The Hi/Lo algorithm in EF Core</span></span>

<span data-ttu-id="0327e-213">Un aspect intéressant du code dans l’exemple précédent est qu’il utilise [l’algorithme Hi/Lo](https://vladmihalcea.com/the-hilo-algorithm/) comme stratégie de génération de clés.</span><span class="sxs-lookup"><span data-stu-id="0327e-213">An interesting aspect of code in the preceding example is that it uses the [Hi/Lo algorithm](https://vladmihalcea.com/the-hilo-algorithm/) as the key generation strategy.</span></span>

<span data-ttu-id="0327e-214">L’algorithme Hi/Lo est utile quand vous avez besoin de clés uniques.</span><span class="sxs-lookup"><span data-stu-id="0327e-214">The Hi/Lo algorithm is useful when you need unique keys.</span></span> <span data-ttu-id="0327e-215">En résumé, l’algorithme Hi/Lo affecte des identificateurs uniques aux lignes de table sans dépendre du stockage immédiat de la ligne dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="0327e-215">As a summary, the Hi-Lo algorithm assigns unique identifiers to table rows while not depending on storing the row in the database immediately.</span></span> <span data-ttu-id="0327e-216">Cela vous permet de commencer à utiliser les identificateurs dès à présent, comme c’est le cas avec les ID de base de données séquentiels standard.</span><span class="sxs-lookup"><span data-stu-id="0327e-216">This lets you start using the identifiers right away, as happens with regular sequential database IDs.</span></span>

<span data-ttu-id="0327e-217">L’algorithme Hi/Lo décrit un mécanisme pour générer des ID sécurisés sur le côté client plutôt que dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="0327e-217">The Hi/Lo algorithm describes a mechanism for generating safe IDs on the client side rather than in the database.</span></span> <span data-ttu-id="0327e-218">*Sécurisé* dans ce contexte signifie sans collisions.</span><span class="sxs-lookup"><span data-stu-id="0327e-218">*Safe* in this context means without collisions.</span></span> <span data-ttu-id="0327e-219">Cet algorithme est intéressant pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="0327e-219">This algorithm is interesting for these reasons:</span></span>

-   <span data-ttu-id="0327e-220">Il n’interrompt pas le modèle d’unité de travail.</span><span class="sxs-lookup"><span data-stu-id="0327e-220">It does not break the Unit of Work pattern.</span></span>

-   <span data-ttu-id="0327e-221">Il ne nécessite pas des allers-retours comme c’est le cas pour des générateurs de séquences dans d’autres systèmes SGBD.</span><span class="sxs-lookup"><span data-stu-id="0327e-221">It does not require round trips the way sequence generators do in other DBMSs.</span></span>

-   <span data-ttu-id="0327e-222">Il génère un identificateur contrôlable de visu, contrairement aux techniques qui utilisent des GUID.</span><span class="sxs-lookup"><span data-stu-id="0327e-222">It generates a human readable identifier, unlike techniques that use GUIDs.</span></span>

<span data-ttu-id="0327e-223">EF Core prend en charge [HiLo](https://stackoverflow.com/questions/282099/whats-the-hi-lo-algorithm) avec la méthode ForSqlServerUseSequenceHiLo, comme indiqué dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="0327e-223">EF Core supports [HiLo](https://stackoverflow.com/questions/282099/whats-the-hi-lo-algorithm) with the ForSqlServerUseSequenceHiLo method, as shown in the preceding example.</span></span>

### <a name="mapping-fields-instead-of-properties"></a><span data-ttu-id="0327e-224">Mappage de champs au lieu de propriétés</span><span class="sxs-lookup"><span data-stu-id="0327e-224">Mapping fields instead of properties</span></span>

<span data-ttu-id="0327e-225">Avec cette fonctionnalité, disponible depuis EF Core 1.1, vous pouvez directement mapper les colonnes aux champs.</span><span class="sxs-lookup"><span data-stu-id="0327e-225">With this feature, available since EF Core 1.1, you can directly map columns to fields.</span></span> <span data-ttu-id="0327e-226">Il est possible de ne pas utiliser de propriétés dans la classe d’entité et uniquement pour mapper les colonnes d’une table aux champs.</span><span class="sxs-lookup"><span data-stu-id="0327e-226">It is possible to not use properties in the entity class, and just to map columns from a table to fields.</span></span> <span data-ttu-id="0327e-227">Cette fonctionnalité est couramment utilisée dans le cadre des champs privés pour n’importe quel état interne qui ne doit pas être accessible depuis l’extérieur de l’entité.</span><span class="sxs-lookup"><span data-stu-id="0327e-227">A common use for that would be private fields for any internal state that do not need to be accessed from outside the entity.</span></span> 

<span data-ttu-id="0327e-228">Pour ce faire, utilisez des champs uniques, mais également des collections, comme un champ `List<>`.</span><span class="sxs-lookup"><span data-stu-id="0327e-228">You can do this with single fields or also with collections, like a `List<>` field.</span></span> <span data-ttu-id="0327e-229">Ce point a été mentionné précédemment quand nous avons abordé la modélisation des classes de modèle de domaine, mais vous pouvez voir ici comment ce mappage est effectué avec la configuration `PropertyAccessMode.Field` mise en surbrillance dans le code précédent.</span><span class="sxs-lookup"><span data-stu-id="0327e-229">This point was mentioned earlier when we discussed modeling the domain model classes, but here you can see how that mapping is performed with the `PropertyAccessMode.Field` configuration highlighted in the previous code.</span></span>

### <a name="using-shadow-properties-in-ef-core-hidden-at-the-infrastructure-level"></a><span data-ttu-id="0327e-230">Utilisation de propriétés cachées dans EF Core, masquées au niveau de l’infrastructure</span><span class="sxs-lookup"><span data-stu-id="0327e-230">Using shadow properties in EF Core, hidden at the infrastructure level</span></span>

<span data-ttu-id="0327e-231">Les propriétés cachées dans EF Core sont des propriétés qui n’existent pas dans votre modèle de classe d’entité.</span><span class="sxs-lookup"><span data-stu-id="0327e-231">Shadow properties in EF Core are properties that do not exist in your entity class model.</span></span> <span data-ttu-id="0327e-232">Les valeurs et les états de ces propriétés sont conservés uniquement dans la classe [ChangeTracker](https://docs.microsoft.com/ef/core/api/microsoft.entityframeworkcore.changetracking.changetracker) au niveau de l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="0327e-232">The values and states of these properties are maintained purely in the [ChangeTracker](https://docs.microsoft.com/ef/core/api/microsoft.entityframeworkcore.changetracking.changetracker) class at the infrastructure level.</span></span>


## <a name="implementing-the-specification-pattern"></a><span data-ttu-id="0327e-233">Implémentation du modèle de spécification</span><span class="sxs-lookup"><span data-stu-id="0327e-233">Implementing the Specification pattern</span></span>

<span data-ttu-id="0327e-234">Comme introduit précédemment dans la section relative à la conception, le modèle de spécification (son nom complet est le modèle de spécification de requête) est un modèle DDD (Domain-Driven Design) conçu comme l’endroit où vous pouvez placer la définition d’une requête avec une logique de pagination et de tri en option.</span><span class="sxs-lookup"><span data-stu-id="0327e-234">As introduced earlier in the design section, the Specification pattern (its full name would be Query-specification pattern) is a Domain-Driven Design pattern designed as the place where you can put the definition of a query with optional sorting and paging logic.</span></span> <span data-ttu-id="0327e-235">Le modèle de spécification définit une requête dans un objet.</span><span class="sxs-lookup"><span data-stu-id="0327e-235">The Specification pattern defines a query in an object.</span></span> <span data-ttu-id="0327e-236">Par exemple, pour encapsuler une requête paginée qui recherche certains produits, vous pouvez créer une spécification PagedProduct qui accepte les paramètres d’entrée nécessaires (pageNumber, pageSize, filtre, etc.).</span><span class="sxs-lookup"><span data-stu-id="0327e-236">For example, in order to encapsulate a paged query that searches for some products you can create a PagedProduct specification that takes the necessary input parameters (pageNumber, pageSize, filter, etc.).</span></span> <span data-ttu-id="0327e-237">Ensuite, toute méthode de dépôt (généralement une surcharge List()) peut accepter une ISpecification et exécuter la requête prévue en fonction de cette spécification.</span><span class="sxs-lookup"><span data-stu-id="0327e-237">Then, any Repository’s method (usually a List() overload) would accept an ISpecification and run the expected query based on that specification.</span></span>

<span data-ttu-id="0327e-238">Un exemple d’une interface de spécification générique est le code suivant issu [d’eShopOnweb](https://github.com/dotnet-architecture/eShopOnWeb).</span><span class="sxs-lookup"><span data-stu-id="0327e-238">An example of a generic Specification interface is the following code from [eShopOnweb](https://github.com/dotnet-architecture/eShopOnWeb).</span></span> 

```csharp
// GENERIC SPECIFICATION INTERFACE
// https://github.com/dotnet-architecture/eShopOnWeb 

public interface ISpecification<T>
{
    Expression<Func<T, bool>> Criteria { get; }
    List<Expression<Func<T, object>>> Includes { get; }
    List<string> IncludeStrings { get; }
}
```

<span data-ttu-id="0327e-239">Ensuite, l’implémentation d’une classe de base de spécification générique s’affiche comme suit.</span><span class="sxs-lookup"><span data-stu-id="0327e-239">Then, the implementation of a generic specification base class is the following.</span></span>

```csharp
// GENERIC SPECIFICATION IMPLEMENTATION (BASE CLASS)
// https://github.com/dotnet-architecture/eShopOnWeb
 
public abstract class BaseSpecification<T> : ISpecification<T>
{
    public BaseSpecification(Expression<Func<T, bool>> criteria)
    {
        Criteria = criteria;
    }
    public Expression<Func<T, bool>> Criteria { get; }

    public List<Expression<Func<T, object>>> Includes { get; } = 
                                           new List<Expression<Func<T, object>>>();

    public List<string> IncludeStrings { get; } = new List<string>();
 
    protected virtual void AddInclude(Expression<Func<T, object>> includeExpression)
    {
        Includes.Add(includeExpression);
    }
    
    // string-based includes allow for including children of children
    // e.g. Basket.Items.Product
    protected virtual void AddInclude(string includeString)
    {
        IncludeStrings.Add(includeString);
    }
}
```

<span data-ttu-id="0327e-240">La spécification suivante charge une entité de panier unique avec l’ID du panier ou l’ID de l’acheteur auquel appartient le panier.</span><span class="sxs-lookup"><span data-stu-id="0327e-240">The following specification loads a single basket entity given either the basket’s ID or the ID of the buyer to whom the basket belongs.</span></span> <span data-ttu-id="0327e-241">Elle effectue un [chargement hâtif](https://docs.microsoft.com/en-us/ef/core/querying/related-data) de la collection Items du panier.</span><span class="sxs-lookup"><span data-stu-id="0327e-241">It will [eager load](https://docs.microsoft.com/en-us/ef/core/querying/related-data) the basket’s Items collection.</span></span>

```csharp
// SAMPLE QUERY SPECIFICATION IMPLEMENTATION

public class BasketWithItemsSpecification : BaseSpecification<Basket>
{
    public BasketWithItemsSpecification(int basketId)
        : base(b => b.Id == basketId)
    {
        AddInclude(b => b.Items);
    }
    public BasketWithItemsSpecification(string buyerId)
        : base(b => b.BuyerId == buyerId)
    {
        AddInclude(b => b.Items);
    }
}
```

<span data-ttu-id="0327e-242">Enfin, vous pouvez voir ci-dessous comment un dépôt EF générique peut utiliser ce type de spécification pour filtrer et charger hâtivement des données liées à un type d’entité T donné.</span><span class="sxs-lookup"><span data-stu-id="0327e-242">And finally, you can see below how a generic EF Repository can use such a specification to filter and eager-load data related to a given entity type T.</span></span>

```csharp
// GENERIC EF REPOSITORY WITH SPECIFICATION
// https://github.com/dotnet-architecture/eShopOnWeb

public IEnumerable<T> List(ISpecification<T> spec)
{
    // fetch a Queryable that includes all expression-based includes
    var queryableResultWithIncludes = spec.Includes
        .Aggregate(_dbContext.Set<T>().AsQueryable(),
            (current, include) => current.Include(include));
 
    // modify the IQueryable to include any string-based include statements
    var secondaryResult = spec.IncludeStrings
        .Aggregate(queryableResultWithIncludes,
            (current, include) => current.Include(include));
 
    // return the result of the query using the specification's criteria expression
    return secondaryResult
                    .Where(spec.Criteria)
                    .AsEnumerable();
}
```
<span data-ttu-id="0327e-243">En plus de l’encapsulation de la logique de filtrage, la spécification peut spécifier la forme des données à retourner, dont les propriétés à remplir.</span><span class="sxs-lookup"><span data-stu-id="0327e-243">In addition to encapsulating filtering logic, the specification can specify the shape of the data to be returned, including which properties to populate.</span></span> 

<span data-ttu-id="0327e-244">Même si nous ne recommandons pas de retourner des données IQueryable à partir d’un dépôt, vous pouvez parfaitement les utiliser dans le dépôt pour générer un jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="0327e-244">Although we don't recommended to return IQueryable from a repository, it’s perfectly fine to use them within the repository to build up a set of results.</span></span> <span data-ttu-id="0327e-245">Vous pouvez voir cette approche utilisée dans la méthode List ci-dessus, qui utilise des expressions IQueryable intermédiaires pour générer la liste des fichiers Include de la requête avant d’exécuter la requête avec les critères de la spécification sur la dernière ligne.</span><span class="sxs-lookup"><span data-stu-id="0327e-245">You can see this approach used in the List method above, which uses intermediate IQueryable expressions to build up the query’s list of includes before executing the query with the specification’s criteria on the last line.</span></span>


#### <a name="additional-resources"></a><span data-ttu-id="0327e-246">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="0327e-246">Additional resources</span></span>

-   <span data-ttu-id="0327e-247">**Mappage de tables**
    [*https://docs.microsoft.com/ef/core/modeling/relational/tables*](https://docs.microsoft.com/ef/core/modeling/relational/tables)</span><span class="sxs-lookup"><span data-stu-id="0327e-247">**Table Mapping**
[*https://docs.microsoft.com/ef/core/modeling/relational/tables*](https://docs.microsoft.com/ef/core/modeling/relational/tables)</span></span>

-   <span data-ttu-id="0327e-248">**Utiliser HiLo pour générer des clés avec Entity Framework Core**
    [*http://www.talkingdotnet.com/use-hilo-to-generate-keys-with-entity-framework-core/*](http://www.talkingdotnet.com/use-hilo-to-generate-keys-with-entity-framework-core/)</span><span class="sxs-lookup"><span data-stu-id="0327e-248">**Use HiLo to generate keys with Entity Framework Core**
[*http://www.talkingdotnet.com/use-hilo-to-generate-keys-with-entity-framework-core/*](http://www.talkingdotnet.com/use-hilo-to-generate-keys-with-entity-framework-core/)</span></span>

-   <span data-ttu-id="0327e-249">**Champs de stockage**
    [*https://docs.microsoft.com/ef/core/modeling/backing-field*](https://docs.microsoft.com/ef/core/modeling/backing-field)</span><span class="sxs-lookup"><span data-stu-id="0327e-249">**Backing Fields**
[*https://docs.microsoft.com/ef/core/modeling/backing-field*](https://docs.microsoft.com/ef/core/modeling/backing-field)</span></span>

-   <span data-ttu-id="0327e-250">**Steve Smith. Collections encapsulées dans Entity Framework Core**
    [*https://ardalis.com/encapsulated-collections-in-entity-framework-core*](https://ardalis.com/encapsulated-collections-in-entity-framework-core)</span><span class="sxs-lookup"><span data-stu-id="0327e-250">**Steve Smith. Encapsulated Collections in Entity Framework Core**
[*https://ardalis.com/encapsulated-collections-in-entity-framework-core*](https://ardalis.com/encapsulated-collections-in-entity-framework-core)</span></span>

-   <span data-ttu-id="0327e-251">**Propriétés cachées**
    [*https://docs.microsoft.com/ef/core/modeling/shadow-properties*](https://docs.microsoft.com/ef/core/modeling/shadow-properties)</span><span class="sxs-lookup"><span data-stu-id="0327e-251">**Shadow Properties**
[*https://docs.microsoft.com/ef/core/modeling/shadow-properties*](https://docs.microsoft.com/ef/core/modeling/shadow-properties)</span></span>

-   <span data-ttu-id="0327e-252">**Modèle Spécification**
    [*http://deviq.com/specification-pattern/*](http://deviq.com/specification-pattern/)</span><span class="sxs-lookup"><span data-stu-id="0327e-252">**The Specification pattern**
[*http://deviq.com/specification-pattern/*](http://deviq.com/specification-pattern/)</span></span>
    

>[!div class="step-by-step"]
<span data-ttu-id="0327e-253">[Précédent](infrastructure-persistence-layer-design.md)
[Suivant](nosql-database-persistence-infrastructure.md)</span><span class="sxs-lookup"><span data-stu-id="0327e-253">[Previous](infrastructure-persistence-layer-design.md)
[Next](nosql-database-persistence-infrastructure.md)</span></span>
