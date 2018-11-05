---
title: Création d’un microservice CRUD simple piloté par les données
description: Architecture des microservices .NET pour les applications .NET en conteneur | Création d’un microservice CRUD simple piloté par les données
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 12/11/2017
ms.openlocfilehash: bba0b93ee7e68ae0320460c6a45ab252ac34c326
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2018
ms.locfileid: "48873494"
---
# <a name="creating-a-simple-data-driven-crud-microservice"></a><span data-ttu-id="ba733-103">Création d’un microservice CRUD simple piloté par les données</span><span class="sxs-lookup"><span data-stu-id="ba733-103">Creating a simple data-driven CRUD microservice</span></span>

<span data-ttu-id="ba733-104">Cette section explique comment créer un microservice simple devant effectuer des opérations de création, de lecture, de mise à jour et de suppression (CRUD) dans une source de données.</span><span class="sxs-lookup"><span data-stu-id="ba733-104">This section outlines how to create a simple microservice that performs create, read, update, and delete (CRUD) operations on a data source.</span></span>

## <a name="designing-a-simple-crud-microservice"></a><span data-ttu-id="ba733-105">Conception d’un microservice CRUD simple</span><span class="sxs-lookup"><span data-stu-id="ba733-105">Designing a simple CRUD microservice</span></span>

<span data-ttu-id="ba733-106">La conception de ce type de microservice en conteneur est très simple.</span><span class="sxs-lookup"><span data-stu-id="ba733-106">From a design point of view, this type of containerized microservice is very simple.</span></span> <span data-ttu-id="ba733-107">Le problème est peut-être simple à résoudre, ou l’implémentation n’est peut-être qu’une preuve de concept.</span><span class="sxs-lookup"><span data-stu-id="ba733-107">Perhaps the problem to solve is simple, or perhaps the implementation is only a proof of concept.</span></span>

![](./media/image4.png)

<span data-ttu-id="ba733-108">**Figure 8-4**.</span><span class="sxs-lookup"><span data-stu-id="ba733-108">**Figure 8-4**.</span></span> <span data-ttu-id="ba733-109">Conception interne de microservices CRUD simples</span><span class="sxs-lookup"><span data-stu-id="ba733-109">Internal design for simple CRUD microservices</span></span>

<span data-ttu-id="ba733-110">Il peut s’agir, par exemple, du microservice de catalogue de l’exemple d’application eShopOnContainers.</span><span class="sxs-lookup"><span data-stu-id="ba733-110">An example of this kind of simple data-drive service is the catalog microservice from the eShopOnContainers sample application.</span></span> <span data-ttu-id="ba733-111">Ce type de service implémente toutes ses fonctionnalités dans un même projet d’API web ASP.NET Core, qui comprend des classes pour son modèle de données, sa logique métier et son code d’accès aux données.</span><span class="sxs-lookup"><span data-stu-id="ba733-111">This type of service implements all its functionality in a single ASP.NET Core Web API project that includes classes for its data model, its business logic, and its data access code.</span></span> <span data-ttu-id="ba733-112">Il stocke également ses données associées dans une base de données qui exécute SQL Server (utilisée comme un conteneur à des fins de développement ou de test). Toutefois, il peut aussi s’agir d’un hôte SQL Server standard, comme illustré à la Figure 8-5.</span><span class="sxs-lookup"><span data-stu-id="ba733-112">It also stores its related data in a database running in SQL Server (as another container for dev/test purposes), but could also be any regular SQL Server host, as shown in Figure 8-5.</span></span>

![](./media/image5.png)

<span data-ttu-id="ba733-113">**Figure 8-5**.</span><span class="sxs-lookup"><span data-stu-id="ba733-113">**Figure 8-5**.</span></span> <span data-ttu-id="ba733-114">Conception d’un microservice CRUD simple piloté par les données</span><span class="sxs-lookup"><span data-stu-id="ba733-114">Simple data-driven/CRUD microservice design</span></span>

<span data-ttu-id="ba733-115">Lorsque vous développez ce type de service, vous avez seulement besoin [d’ASP.NET Core](https://docs.microsoft.com/aspnet/core/) et d’une API ou d’un outil ORM d’accès aux données, comme, par exemple, [Entity Framework Core](https://docs.microsoft.com/ef/core/index).</span><span class="sxs-lookup"><span data-stu-id="ba733-115">When you are developing this kind of service, you only need [ASP.NET Core](https://docs.microsoft.com/aspnet/core/) and a data-access API or ORM like [Entity Framework Core](https://docs.microsoft.com/ef/core/index).</span></span> <span data-ttu-id="ba733-116">Vous pouvez également générer automatiquement des métadonnées [Swagger](https://swagger.io/) par le biais de [Swashbuckle](https://github.com/domaindrivendev/Swashbuckle.AspNetCore), afin de fournir une description de votre service, comme l’explique la section suivante.</span><span class="sxs-lookup"><span data-stu-id="ba733-116">You could also generate [Swagger](https://swagger.io/) metadata automatically through [Swashbuckle](https://github.com/domaindrivendev/Swashbuckle.AspNetCore) to provide a description of what your service offers, as explained in the next section.</span></span>

<span data-ttu-id="ba733-117">Notez que les serveurs de base de données, tels que SQL Server, qui sont situés dans un conteneur Docker constituent la solution idéale pour les environnements de développement. En effet, vous pouvez utiliser directement toutes vos dépendances, sans avoir à provisionner une base de données locale ou cloud.</span><span class="sxs-lookup"><span data-stu-id="ba733-117">Note that running a database server like SQL Server within a Docker container is great for development environments, because you can have all your dependencies up and running without needing to provision a database in the cloud or on-premises.</span></span> <span data-ttu-id="ba733-118">Ceci est très utile lorsque vous effectuez des tests d’intégration.</span><span class="sxs-lookup"><span data-stu-id="ba733-118">This is very convenient when running integration tests.</span></span> <span data-ttu-id="ba733-119">Toutefois, pour les environnements de production, l’exécution d’un serveur de base de données dans un conteneur est déconseillée, car elle ne permet pas d’obtenir une haute disponibilité.</span><span class="sxs-lookup"><span data-stu-id="ba733-119">However, for production environments, running a database server in a container is not recommended, because you usually do not get high availability with that approach.</span></span> <span data-ttu-id="ba733-120">Pour un environnement de production Azure, il est recommandé d’utiliser Azure SQL DB ou une autre technologie de base de données capable de fournir une haute disponibilité et une scalabilité importante.</span><span class="sxs-lookup"><span data-stu-id="ba733-120">For a production environment in Azure, it is recommended that you use Azure SQL DB or any other database technology that can provide high availability and high scalability.</span></span> <span data-ttu-id="ba733-121">Par exemple, pour une approche NoSQL, vous pourriez utiliser DocumentDB.</span><span class="sxs-lookup"><span data-stu-id="ba733-121">For example, for a NoSQL approach, you might choose DocumentDB.</span></span>

<span data-ttu-id="ba733-122">Enfin, en modifiant les fichiers de métadonnées Dockerfile et docker-compose.yml, vous pouvez configurer la création de l’image de ce conteneur, c’est-à-dire, quelle image de base elle va utiliser, ainsi que les paramètres de conception, tels que le nom interne et externe, et les ports TCP.</span><span class="sxs-lookup"><span data-stu-id="ba733-122">Finally, by editing the Dockerfile and docker-compose.yml metadata files, you can configure how the image of this container will be created—what base image it will use, plus design settings such as internal and external names and TCP ports.</span></span> 

## <a name="implementing-a-simple-crud-microservice-with-aspnet-core"></a><span data-ttu-id="ba733-123">Implémentation d’un microservice CRUD simple avec ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="ba733-123">Implementing a simple CRUD microservice with ASP.NET Core</span></span>

<span data-ttu-id="ba733-124">Pour implémenter un microservice CRUD simple à l’aide de .NET Core et de Visual Studio, commencez par créer un projet d’API web ASP.NET Core simple (et exécutez-le sur .NET Core pour qu’il puisse s’exécuter sur un hôte Docker Linux), comme indiqué dans la Figure 8-6.</span><span class="sxs-lookup"><span data-stu-id="ba733-124">To implement a simple CRUD microservice using .NET Core and Visual Studio, you start by creating a simple ASP.NET Core Web API project (running on .NET Core so it can run on a Linux Docker host), as shown in Figure 8-6.</span></span>

  ------------------------------------------------------------------------------------- -------------------------------------------------------------------------------------
  <span data-ttu-id="ba733-125">![](./media/image6.png)   ![](./media/image7.png)</span><span class="sxs-lookup"><span data-stu-id="ba733-125">![](./media/image6.png)   ![](./media/image7.png)</span></span>
  ------------------------------------------------------------------------------------- -------------------------------------------------------------------------------------

<span data-ttu-id="ba733-126">**Figure 8-6**.</span><span class="sxs-lookup"><span data-stu-id="ba733-126">**Figure 8-6**.</span></span> <span data-ttu-id="ba733-127">Création d’un projet d’API web ASP.NET Core dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ba733-127">Creating an ASP.NET Core Web API project in Visual Studio</span></span>

<span data-ttu-id="ba733-128">Après avoir créé le projet, vous pouvez implémenter vos contrôleurs MVC comme vous le feriez dans n’importe quel autre projet d’API web, à l’aide de l’API Entity Framework ou d’une autre API.</span><span class="sxs-lookup"><span data-stu-id="ba733-128">After creating the project, you can implement your MVC controllers as you would in any other Web API project, using the Entity Framework API or other API.</span></span> <span data-ttu-id="ba733-129">Dans un nouveau projet d’API web, vous pouvez voir que la seule dépendance de ce microservice se trouve au niveau d’ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="ba733-129">In a new Web API project, you can see that the only dependency you have in that microservice is on ASP.NET Core itself.</span></span> <span data-ttu-id="ba733-130">En interne, dans la dépendance `Microsoft.AspNetCore.All`, il référence Entity Framework et de nombreux autres packages Nuget .NET Core, comme indiqué dans la Figure 8-7.</span><span class="sxs-lookup"><span data-stu-id="ba733-130">Internally, within the `Microsoft.AspNetCore.All` dependency, it is referencing Entity Framework and many other .NET Core Nuget packages, as shown in Figure 8-7.</span></span>

![](./media/image8.PNG)

<span data-ttu-id="ba733-131">**Figure 8-7**.</span><span class="sxs-lookup"><span data-stu-id="ba733-131">**Figure 8-7**.</span></span> <span data-ttu-id="ba733-132">Dépendances d’un microservice d’API web CRUD simple</span><span class="sxs-lookup"><span data-stu-id="ba733-132">Dependencies in a simple CRUD Web API microservice</span></span>

### <a name="implementing-crud-web-api-services-with-entity-framework-core"></a><span data-ttu-id="ba733-133">Implémentation de services d’API web CRUD avec Entity Framework Core</span><span class="sxs-lookup"><span data-stu-id="ba733-133">Implementing CRUD Web API services with Entity Framework Core</span></span>

<span data-ttu-id="ba733-134">Entity Framework (EF) Core est une version légère, extensible et multiplateforme de la technologie d’accès aux données Entity Framework populaire.</span><span class="sxs-lookup"><span data-stu-id="ba733-134">Entity Framework (EF) Core is a lightweight, extensible, and cross-platform version of the popular Entity Framework data access technology.</span></span> <span data-ttu-id="ba733-135">Entity Framework Core est un outil de mappage objet-relationnel (ORM) qui permet aux développeurs .NET d’utiliser une base de données avec des objets .NET.</span><span class="sxs-lookup"><span data-stu-id="ba733-135">EF Core is an object-relational mapper (ORM) that enables .NET developers to work with a database using .NET objects.</span></span>

<span data-ttu-id="ba733-136">Le microservice de catalogue utilise Entity Framework et le fournisseur SQL Server, car sa base de données est exécutée dans un conteneur avec l’image SQL Server pour Linux Docker.</span><span class="sxs-lookup"><span data-stu-id="ba733-136">The catalog microservice uses EF and the SQL Server provider because its database is running in a container with the SQL Server for Linux Docker image.</span></span> <span data-ttu-id="ba733-137">Toutefois, la base de données peut être déployée sur n’importe quel serveur SQL Server (instance locale Windows ou Azure SQL DB).</span><span class="sxs-lookup"><span data-stu-id="ba733-137">However, the database could be deployed into any SQL Server, such as Windows on-premises or Azure SQL DB.</span></span> <span data-ttu-id="ba733-138">La seule chose que vous devez modifier est la chaîne de connexion située dans le microservice de l’API web ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="ba733-138">The only thing you would need to change is the connection string in the ASP.NET Web API microservice.</span></span>


#### <a name="the-data-model"></a><span data-ttu-id="ba733-139">Modèle de données</span><span class="sxs-lookup"><span data-stu-id="ba733-139">The data model</span></span>

<span data-ttu-id="ba733-140">Avec Entity Framework Core, l’accès aux données est effectué à l’aide d’un modèle.</span><span class="sxs-lookup"><span data-stu-id="ba733-140">With EF Core, data access is performed by using a model.</span></span> <span data-ttu-id="ba733-141">Un modèle est composé de classes d’entité et d’un contexte dérivé qui représente une session avec la base de données, ce qui vous permet d’interroger et d’enregistrer des données.</span><span class="sxs-lookup"><span data-stu-id="ba733-141">A model is made up of entity classes and a derived context that represents a session with the database, allowing you to query and save data.</span></span> <span data-ttu-id="ba733-142">Vous pouvez générer un modèle à partir d’une base de données existante, coder manuellement un modèle en fonction de votre base de données ou utiliser des migrations Entity Framework pour créer une base de données à partir de votre modèle (et la faire évoluer au même rythme que celui-ci).</span><span class="sxs-lookup"><span data-stu-id="ba733-142">You can generate a model from an existing database, manually code a model to match your database, or use EF migrations to create a database from your model (and evolve it as your model changes over time).</span></span> <span data-ttu-id="ba733-143">Pour le microservice de catalogue, nous utilisons la dernière méthode.</span><span class="sxs-lookup"><span data-stu-id="ba733-143">For the catalog microservice we are using the last approach.</span></span> <span data-ttu-id="ba733-144">Vous pouvez voir un exemple de la classe d’entité CatalogItem dans l’exemple de code suivant, qui est une classe d’entité [POCO](https://en.wikipedia.org/wiki/Plain_Old_CLR_Object).</span><span class="sxs-lookup"><span data-stu-id="ba733-144">You can see an example of the CatalogItem entity class in the following code example, which is a simple Plain Old CLR Object ([POCO](https://en.wikipedia.org/wiki/Plain_Old_CLR_Object)) entity class.</span></span>

```csharp
public class CatalogItem
{
    public int Id { get; set; }
    public string Name { get; set; }
    public string Description { get; set; }
    public decimal Price { get; set; }
    public string PictureFileName { get; set; }
    public string PictureUri { get; set; }
    public int CatalogTypeId { get; set; }
    public CatalogType CatalogType { get; set; }
    public int CatalogBrandId { get; set; }
    public CatalogBrand CatalogBrand { get; set; }
    public int AvailableStock { get; set; }
    public int RestockThreshold { get; set; }
    public int MaxStockThreshold { get; set; }

    public bool OnReorder { get; set; }
    public CatalogItem() { }

    // Additional code ...
}
```

<span data-ttu-id="ba733-145">Vous avez également besoin d’un DbContext qui représente une session pour la base de données.</span><span class="sxs-lookup"><span data-stu-id="ba733-145">You also need a DbContext that represents a session with the database.</span></span> <span data-ttu-id="ba733-146">Pour le microservice de catalogue, la classe CatalogContext est dérivée de la classe de base DbContext, comme le montre l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="ba733-146">For the catalog microservice, the CatalogContext class derives from the DbContext base class, as shown in the following example:</span></span>

```csharp
public class CatalogContext : DbContext
{
    public CatalogContext(DbContextOptions<CatalogContext> options) : base(options)
    {
    }
    public DbSet<CatalogItem> CatalogItems { get; set; }
    public DbSet<CatalogBrand> CatalogBrands { get; set; }
    public DbSet<CatalogType> CatalogTypes { get; set; }

    // Additional code ...

}
```

<span data-ttu-id="ba733-147">Vous pouvez avoir d’autres implémentations `DbContext`.</span><span class="sxs-lookup"><span data-stu-id="ba733-147">You can have additional `DbContext` implementations.</span></span> <span data-ttu-id="ba733-148">Par exemple, dans l’exemple de microservice Catalog.API, il existe un deuxième `DbContext` nommé `CatalogContextSeed` où des exemples de données sont automatiquement ajoutés lors du premier accès à la base de données.</span><span class="sxs-lookup"><span data-stu-id="ba733-148">For example, in the sample Catalog.API microservice, there's a second `DbContext` named `CatalogContextSeed` where it automatically populates the sample data the first time it tries to access the database.</span></span> <span data-ttu-id="ba733-149">Cette méthode est utile pour les données de démonstration et pour les scénarios de tests automatisés.</span><span class="sxs-lookup"><span data-stu-id="ba733-149">This method is useful for demo data and for automated testing scenarios, as well.</span></span> <span data-ttu-id="ba733-150">Dans le `DbContext`, utilisez la méthode `OnModelCreating` pour personnaliser les mappages d’entités objet/base de données, et d’autres [points d’extension Entity Framework](https://blogs.msdn.microsoft.com/dotnet/2016/09/29/implementing-seeding-custom-conventions-and-interceptors-in-ef-core-1-0/).</span><span class="sxs-lookup"><span data-stu-id="ba733-150">Within the `DbContext`, you use the `OnModelCreating` method to customize object/database entity mappings with and other [EF extensibility points](https://blogs.msdn.microsoft.com/dotnet/2016/09/29/implementing-seeding-custom-conventions-and-interceptors-in-ef-core-1-0/).</span></span>

##### <a name="querying-data-from-web-api-controllers"></a><span data-ttu-id="ba733-151">Interrogation des données à partir de contrôleurs d’API web</span><span class="sxs-lookup"><span data-stu-id="ba733-151">Querying data from Web API controllers</span></span>

<span data-ttu-id="ba733-152">Les instances des classes d’entité sont généralement récupérées dans la base de données à l’aide de LINQ, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="ba733-152">Instances of your entity classes are typically retrieved from the database using Language Integrated Query (LINQ), as shown in the following example:</span></span>

```csharp
[Route("api/v1/[controller]")]
public class CatalogController : ControllerBase
{
    private readonly CatalogContext _catalogContext;
    private readonly CatalogSettings _settings;
    private readonly ICatalogIntegrationEventService _catalogIntegrationEventService;

    public CatalogController(CatalogContext context, 
                             IOptionsSnapshot<CatalogSettings> settings,
                             ICatalogIntegrationEventService catalogIntegrationEventService)
    {
        _catalogContext = context ?? throw new ArgumentNullException(nameof(context));
        _catalogIntegrationEventService = catalogIntegrationEventService ?? throw new ArgumentNullException(nameof(catalogIntegrationEventService));

        _settings = settings.Value;
        ((DbContext)context).ChangeTracker.QueryTrackingBehavior = QueryTrackingBehavior.NoTracking;
    }

    // GET api/v1/[controller]/items[?pageSize=3&pageIndex=10]
    [HttpGet]
    [Route("[action]")]
    [ProducesResponseType(typeof(PaginatedItemsViewModel<CatalogItem>), (int)HttpStatusCode.OK)]
    public async Task<IActionResult> Items([FromQuery]int pageSize = 10, 
                                           [FromQuery]int pageIndex = 0)

    {
        var totalItems = await _catalogContext.CatalogItems
            .LongCountAsync();

        var itemsOnPage = await _catalogContext.CatalogItems
            .OrderBy(c => c.Name)
            .Skip(pageSize * pageIndex)
            .Take(pageSize)
            .ToListAsync();

        itemsOnPage = ChangeUriPlaceholder(itemsOnPage);

        var model = new PaginatedItemsViewModel<CatalogItem>(
            pageIndex, pageSize, totalItems, itemsOnPage);

        return Ok(model);
    } 
    //...
}
```

##### <a name="saving-data"></a><span data-ttu-id="ba733-153">Enregistrement de données</span><span class="sxs-lookup"><span data-stu-id="ba733-153">Saving data</span></span>

<span data-ttu-id="ba733-154">Les données sont créées, supprimées et modifiées dans la base de données à l’aide d’instances de vos classes d’entité.</span><span class="sxs-lookup"><span data-stu-id="ba733-154">Data is created, deleted, and modified in the database using instances of your entity classes.</span></span> <span data-ttu-id="ba733-155">Vous pouvez ajouter du code similaire à celui de l’exemple codé en dur suivant (il s’agit ici de données fictives) dans vos contrôleurs d’API web.</span><span class="sxs-lookup"><span data-stu-id="ba733-155">You could add code like the following hard-coded example (mock data, in this case) to your Web API controllers.</span></span>

```csharp
var catalogItem = new CatalogItem() {CatalogTypeId=2, CatalogBrandId=2,
                                     Name="Roslyn T-Shirt", Price = 12};
_context.Catalog.Add(catalogItem);
_context.SaveChanges();
```

##### <a name="dependency-injection-in-aspnet-core-and-web-api-controllers"></a><span data-ttu-id="ba733-156">Injection de dépendances dans ASP.NET Core et dans les contrôleurs d’API web</span><span class="sxs-lookup"><span data-stu-id="ba733-156">Dependency Injection in ASP.NET Core and Web API controllers</span></span>

<span data-ttu-id="ba733-157">Dans ASP.NET Core, vous pouvez utiliser une injection de dépendances prête à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="ba733-157">In ASP.NET Core you can use Dependency Injection (DI) out of the box.</span></span> <span data-ttu-id="ba733-158">Il n’est pas nécessaire de configurer un conteneur IoC tiers. Toutefois, si vous le souhaitez, vous pouvez connecter votre conteneur IoC par défaut à l’infrastructure ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="ba733-158">You do not need to set up a third-party Inversion of Control (IoC) container, although you can plug your preferred IoC container into the ASP.NET Core infrastructure if you want.</span></span> <span data-ttu-id="ba733-159">Dans ce cas, vous pouvez injecter directement le DBContext Entity Framework (et autres dépôts) via le constructeur de contrôleur.</span><span class="sxs-lookup"><span data-stu-id="ba733-159">In this case, it means that you can directly inject the required EF DBContext or additional repositories through the controller constructor.</span></span> <span data-ttu-id="ba733-160">Dans l’exemple situé au-dessus de la classe `CatalogController`, nous allons injecter un objet de type `CatalogContext`, ainsi que d’autres objets via le constructeur `CatalogController()`.</span><span class="sxs-lookup"><span data-stu-id="ba733-160">In the example above of the `CatalogController` class, we are injecting an object of `CatalogContext` type plus other objects through the `CatalogController()` constructor.</span></span>

<span data-ttu-id="ba733-161">L’un des éléments importants à configurer pour le projet d’API web est l’inscription de la classe DbContext auprès du conteneur IoC du service.</span><span class="sxs-lookup"><span data-stu-id="ba733-161">An important configuration to set up in the Web API project is the DbContext class registration into the service’s IoC container.</span></span> <span data-ttu-id="ba733-162">Pour cela, dans la classe `Startup`, appelez la méthode `services.AddDbContext<DbContext>()` à l’intérieur de la méthode `ConfigureServices()`, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="ba733-162">You typically do so in the `Startup` class by calling the `services.AddDbContext<DbContext>()` method inside the `ConfigureServices()` method, as shown in the following example:</span></span>

```csharp
public void ConfigureServices(IServiceCollection services)
{
    // Additional code...

    services.AddDbContext<CatalogContext>(options =>
    {
        options.UseSqlServer(Configuration["ConnectionString"],
        sqlServerOptionsAction: sqlOptions =>
        {
           sqlOptions.
               MigrationsAssembly(
                   typeof(Startup).
                    GetTypeInfo().
                     Assembly.
                      GetName().Name);

           //Configuring Connection Resiliency:
           sqlOptions.
               EnableRetryOnFailure(maxRetryCount: 5,
               maxRetryDelay: TimeSpan.FromSeconds(30),
               errorNumbersToAdd: null);

       });

       // Changing default behavior when client evaluation occurs to throw.
       // Default in EFCore would be to log warning when client evaluation is done.
       options.ConfigureWarnings(warnings => warnings.Throw(
           RelationalEventId.QueryClientEvaluationWarning));
   });

  //...

}
```

### <a name="additional-resources"></a><span data-ttu-id="ba733-163">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ba733-163">Additional resources</span></span>

-   <span data-ttu-id="ba733-164">**Interrogation des données**
    [*https://docs.microsoft.com/ef/core/querying/index*](https://docs.microsoft.com/ef/core/querying/index)</span><span class="sxs-lookup"><span data-stu-id="ba733-164">**Querying Data**
[*https://docs.microsoft.com/ef/core/querying/index*](https://docs.microsoft.com/ef/core/querying/index)</span></span>

-   <span data-ttu-id="ba733-165">**Enregistrement de données**
    [*https://docs.microsoft.com/ef/core/saving/index*](https://docs.microsoft.com/ef/core/saving/index)</span><span class="sxs-lookup"><span data-stu-id="ba733-165">**Saving Data**
[*https://docs.microsoft.com/ef/core/saving/index*](https://docs.microsoft.com/ef/core/saving/index)</span></span>

## <a name="the-db-connection-string-and-environment-variables-used-by-docker-containers"></a><span data-ttu-id="ba733-166">Chaîne de connexion de la base de données et variables d’environnement utilisées par les conteneurs Docker</span><span class="sxs-lookup"><span data-stu-id="ba733-166">The DB connection string and environment variables used by Docker containers</span></span>

<span data-ttu-id="ba733-167">Vous pouvez utiliser les paramètres ASP.NET Core et ajouter une propriété ConnectionString à votre fichier settings.json, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="ba733-167">You can use the ASP.NET Core settings and add a ConnectionString property to your settings.json file as shown in the following example:</span></span>

```csharp
{
    "ConnectionString": "Server=tcp:127.0.0.1,5433;Initial Catalog=Microsoft.eShopOnContainers.Services.CatalogDb;User Id=sa;Password=Pass@word",
    "ExternalCatalogBaseUrl": "http://localhost:5101",
    "Logging": {
        "IncludeScopes": false,
        "LogLevel": {
            "Default": "Debug",
            "System": "Information",
            "Microsoft": "Information"
        }
    }
}
```

<span data-ttu-id="ba733-168">Le fichier settings.json peut avoir des valeurs par défaut pour la propriété ConnectionString ou pour toute autre propriété.</span><span class="sxs-lookup"><span data-stu-id="ba733-168">The settings.json file can have default values for the ConnectionString property or for any other property.</span></span> <span data-ttu-id="ba733-169">Toutefois, ces propriétés seront remplacées par les valeurs des variables d’environnement que vous spécifiez dans le fichier docker-compose.override.yml lors de l’utilisation de Docker.</span><span class="sxs-lookup"><span data-stu-id="ba733-169">However, those properties will be overridden by the values of environment variables that you specify in the docker-compose.override.yml file, when using Docker.</span></span>

<span data-ttu-id="ba733-170">Dans les fichiers docker-compose.yml et docker-compose.override.yml, vous pouvez initialiser les variables d’environnement pour que Docker les configure comme des variables d’environnement du système d’exploitation, comme dans le fichier docker-compose.override.yml suivant (dans cet exemple, un retour automatique à la ligne est effectué pour la chaîne de connexion et les autres lignes, mais ce ne sera pas le cas dans votre fichier de code).</span><span class="sxs-lookup"><span data-stu-id="ba733-170">From your docker-compose.yml or docker-compose.override.yml files, you can initialize those environment variables so that Docker will set them up as OS environment variables for you, as shown in the following docker-compose.override.yml file (the connection string and other lines wrap in this example, but it would not wrap in your own code file).</span></span>

```yml
# docker-compose.override.yml

#
catalog.api:
  environment:
    - ConnectionString=Server=sql.data;Database=Microsoft.eShopOnContainers.Services.CatalogDb;User Id=sa;Password=Pass@word
    # Additional environment variables for this service
  ports:
    - "5101:80"
```

<span data-ttu-id="ba733-171">Les fichiers docker-compose.yml situés au niveau de la solution non seulement sont plus flexibles que les fichiers de configuration situés au niveau du projet ou microservice, mais ils sont aussi plus sécurisés si vous remplacez les variables d’environnement déclarées dans les fichiers docker-compose par des valeurs définies dans vos outils de déploiement (par exemple, dans les tâches de déploiement Azure DevOps Services Docker).</span><span class="sxs-lookup"><span data-stu-id="ba733-171">The docker-compose.yml files at the solution level are not only more flexible than configuration files at the project or microservice level, but also more secure if you override the environment variables declared at the docker-compose files with values set from your deployment tools, like from Azure DevOps Services Docker deployment tasks.</span></span> 

<span data-ttu-id="ba733-172">Enfin, vous pouvez obtenir cette valeur à partir de votre code à l’aide de Configuration\["ConnectionString"\], comme illustré dans la méthode ConfigureServices de l’exemple de code précédent.</span><span class="sxs-lookup"><span data-stu-id="ba733-172">Finally, you can get that value from your code by using Configuration\["ConnectionString"\], as shown in the ConfigureServices method in an earlier code example.</span></span>

<span data-ttu-id="ba733-173">Toutefois, pour les environnements de production, vous pouvez explorer d’autres moyens de stocker des secrets, comme les chaînes de connexion.</span><span class="sxs-lookup"><span data-stu-id="ba733-173">However, for production environments, you might want to explore additional ways on how to store secrets like the connection strings.</span></span> <span data-ttu-id="ba733-174">Ceci est généralement géré par l’orchestrateur de votre choix, comme pour la [gestion de secrets Docker Swarm](https://docs.docker.com/engine/swarm/secrets/).</span><span class="sxs-lookup"><span data-stu-id="ba733-174">Usually that will be managed by your chosen orchestrator, like you can do with [Docker Swarm secrets management](https://docs.docker.com/engine/swarm/secrets/).</span></span>

### <a name="implementing-versioning-in-aspnet-web-apis"></a><span data-ttu-id="ba733-175">Implémentation de la gestion de version dans les API web ASP.NET</span><span class="sxs-lookup"><span data-stu-id="ba733-175">Implementing versioning in ASP.NET Web APIs</span></span>

<span data-ttu-id="ba733-176">L’évolution des exigences métier peut entraîner l’ajout de collections de ressources, le changement des relations entre les ressources et la modification de la structure des données contenues dans ces ressources.</span><span class="sxs-lookup"><span data-stu-id="ba733-176">As business requirements change, new collections of resources may be added, the relationships between resources might change, and the structure of the data in resources might be amended.</span></span> <span data-ttu-id="ba733-177">La modification d’une API web pour s’adapter aux nouvelles exigences est un processus relativement simple. Toutefois, vous devez prendre en compte les conséquences d’une telle modification sur l’utilisation de l’API web par les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="ba733-177">Updating a Web API to handle new requirements is a relatively straightforward process, but you must consider the effects that such changes will have on client applications consuming the Web API.</span></span> <span data-ttu-id="ba733-178">Même si le développeur qui conçoit et implémente une API web dispose d’un contrôle total sur cette API, il ne dispose pas du même degré de contrôle sur les applications clientes qui peuvent avoir été créées par des organisations tierces distantes.</span><span class="sxs-lookup"><span data-stu-id="ba733-178">Although the developer designing and implementing a Web API has full control over that API, the developer does not have the same degree of control over client applications that might be built by third party organizations operating remotely.</span></span>

<span data-ttu-id="ba733-179">La gestion de version permet à une API web d’indiquer les fonctionnalités et les ressources qu’elle expose.</span><span class="sxs-lookup"><span data-stu-id="ba733-179">Versioning enables a Web API to indicate the features and resources that it exposes.</span></span> <span data-ttu-id="ba733-180">Une application cliente peut ensuite envoyer des requêtes à une version précise d’une fonctionnalité ou d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="ba733-180">A client application can then submit requests to a specific version of a feature or resource.</span></span> <span data-ttu-id="ba733-181">Il existe plusieurs méthodes pour implémenter la gestion de version :</span><span class="sxs-lookup"><span data-stu-id="ba733-181">There are several approaches to implement versioning:</span></span>

-   <span data-ttu-id="ba733-182">Gestion des versions d’URI</span><span class="sxs-lookup"><span data-stu-id="ba733-182">URI versioning</span></span>

-   <span data-ttu-id="ba733-183">Gestion des versions de chaîne de requête</span><span class="sxs-lookup"><span data-stu-id="ba733-183">Query string versioning</span></span>

-   <span data-ttu-id="ba733-184">Gestion des versions d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ba733-184">Header versioning</span></span>

<span data-ttu-id="ba733-185">La gestion des versions de chaîne de requête et d’URI sont les plus simples à implémenter.</span><span class="sxs-lookup"><span data-stu-id="ba733-185">Query string and URI versioning are the simplest to implement.</span></span> <span data-ttu-id="ba733-186">La gestion des versions d’en-tête est une bonne méthode.</span><span class="sxs-lookup"><span data-stu-id="ba733-186">Header versioning is a good approach.</span></span> <span data-ttu-id="ba733-187">Toutefois, elle n’est pas aussi explicite et directe que la gestion des versions d’URI.</span><span class="sxs-lookup"><span data-stu-id="ba733-187">However, header versioning not as explicit and straightforward as URI versioning.</span></span> <span data-ttu-id="ba733-188">Étant donné que la gestion des versions d’URI est la plus simple et la plus explicite, c’est elle qu’utilise l’exemple d’application eShopOnContainers.</span><span class="sxs-lookup"><span data-stu-id="ba733-188">Because URL versioning is the simplest and most explicit, the eShopOnContainers sample application uses URI versioning.</span></span>

<span data-ttu-id="ba733-189">Avec la gestion des versions d’URI (comme dans l’exemple d’application eShopOnContainers), chaque fois que vous modifiez l’API web ou que vous modifiez le schéma des ressources, vous ajoutez un numéro de version à l’URI de chaque ressource.</span><span class="sxs-lookup"><span data-stu-id="ba733-189">With URI versioning, as in the eShopOnContainers sample application, each time you modify the Web API or change the schema of resources, you add a version number to the URI for each resource.</span></span> <span data-ttu-id="ba733-190">Les URI existants continuent de fonctionner comme avant, en retournant des ressources conformes au schéma de la version demandée.</span><span class="sxs-lookup"><span data-stu-id="ba733-190">Existing URIs should continue to operate as before, returning resources that conform to the schema that matches the requested version.</span></span>

<span data-ttu-id="ba733-191">Comme le montre l’exemple de code suivant, la version peut être définie à l’aide de l’attribut Route dans l’API web, ce qui rend la version explicite dans l’URI (v1, dans ce cas).</span><span class="sxs-lookup"><span data-stu-id="ba733-191">As shown in the following code example, the version can be set by using the Route attribute in the Web API, which makes the version explicit in the URI (v1 in this case).</span></span>

```csharp
[Route("api/v1/[controller]")]
public class CatalogController : ControllerBase
{
    // Implementation ...
```

<span data-ttu-id="ba733-192">Ce mécanisme de gestion de version est simple et dépend du serveur qui achemine la demande vers le point de terminaison approprié.</span><span class="sxs-lookup"><span data-stu-id="ba733-192">This versioning mechanism is simple and depends on the server routing the request to the appropriate endpoint.</span></span> <span data-ttu-id="ba733-193">Toutefois, pour une gestion de version plus sophistiquée et pour une utilisation optimale avec REST, vous devez utiliser des hypermédias et implémenter [HATEOAS](https://docs.microsoft.com/azure/architecture/best-practices/api-design#using-the-hateoas-approach-to-enable-navigation-to-related-resources).</span><span class="sxs-lookup"><span data-stu-id="ba733-193">However, for a more sophisticated versioning and the best method when using REST, you should use hypermedia and implement [HATEOAS (Hypertext as the Engine of Application State)](https://docs.microsoft.com/azure/architecture/best-practices/api-design#using-the-hateoas-approach-to-enable-navigation-to-related-resources).</span></span>

### <a name="additional-resources"></a><span data-ttu-id="ba733-194">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ba733-194">Additional resources</span></span>

-   <span data-ttu-id="ba733-195">**Scott Hanselman. ASP.NET Core RESTful Web API versioning made easy**
    [*https://www.hanselman.com/blog/ASPNETCoreRESTfulWebAPIVersioningMadeEasy.aspx*](https://www.hanselman.com/blog/ASPNETCoreRESTfulWebAPIVersioningMadeEasy.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba733-195">**Scott Hanselman. ASP.NET Core RESTful Web API versioning made easy**
[*https://www.hanselman.com/blog/ASPNETCoreRESTfulWebAPIVersioningMadeEasy.aspx*](https://www.hanselman.com/blog/ASPNETCoreRESTfulWebAPIVersioningMadeEasy.aspx)</span></span>

-   <span data-ttu-id="ba733-196">**Contrôle de version d’une API web RESTful**
    [*https://docs.microsoft.com/azure/architecture/best-practices/api-design#versioning-a-restful-web-api*](https://docs.microsoft.com/azure/architecture/best-practices/api-design#versioning-a-restful-web-api)</span><span class="sxs-lookup"><span data-stu-id="ba733-196">**Versioning a RESTful web API**
[*https://docs.microsoft.com/azure/architecture/best-practices/api-design#versioning-a-restful-web-api*](https://docs.microsoft.com/azure/architecture/best-practices/api-design#versioning-a-restful-web-api)</span></span>

-   <span data-ttu-id="ba733-197">**Roy Fielding. Versioning, Hypermedia, and REST**
    [*https://www.infoq.com/articles/roy-fielding-on-versioning*](https://www.infoq.com/articles/roy-fielding-on-versioning)</span><span class="sxs-lookup"><span data-stu-id="ba733-197">**Roy Fielding. Versioning, Hypermedia, and REST**
[*https://www.infoq.com/articles/roy-fielding-on-versioning*](https://www.infoq.com/articles/roy-fielding-on-versioning)</span></span>

## <a name="generating-swagger-description-metadata-from-your-aspnet-core-web-api"></a><span data-ttu-id="ba733-198">Génération de métadonnées de description Swagger à partir de votre API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="ba733-198">Generating Swagger description metadata from your ASP.NET Core Web API</span></span> 

<span data-ttu-id="ba733-199">[Swagger](https://swagger.io/) est un framework open source couramment utilisé qui s’appuie sur un large écosystème d’outils permettant de concevoir, de générer, de documenter et de consommer vos API RESTful.</span><span class="sxs-lookup"><span data-stu-id="ba733-199">[Swagger](https://swagger.io/) is a commonly used open source framework backed by a large ecosystem of tools that helps you design, build, document, and consume your RESTful APIs.</span></span> <span data-ttu-id="ba733-200">C’est désormais une référence dans le domaine des métadonnées de description d’API.</span><span class="sxs-lookup"><span data-stu-id="ba733-200">It is becoming the standard for the APIs description metadata domain.</span></span> <span data-ttu-id="ba733-201">Vous devez ajouter des métadonnées de description Swagger à tous les microservices, qu’il s’agisse de microservices pilotés par les données ou de microservices plus avancés pilotés par le domaine (comme expliqué dans la section suivante).</span><span class="sxs-lookup"><span data-stu-id="ba733-201">You should include Swagger description metadata with any kind of microservice, either data-driven microservices or more advanced domain-driven microservices (as explained in following section).</span></span>

<span data-ttu-id="ba733-202">Le principal intérêt de Swagger est la spécification Swagger, c’est-à-dire les métadonnées de description d’API contenues dans un fichier JSON ou YAML.</span><span class="sxs-lookup"><span data-stu-id="ba733-202">The heart of Swagger is the Swagger specification, which is API description metadata in a JSON or YAML file.</span></span> <span data-ttu-id="ba733-203">La spécification crée le contrat RESTful pour votre API, en détaillant toutes ses ressources et opérations dans un format lisible par l’homme et par la machine, pour un développement, une découverte et une intégration facilités.</span><span class="sxs-lookup"><span data-stu-id="ba733-203">The specification creates the RESTful contract for your API, detailing all its resources and operations in both a human- and machine-readable format for easy development, discovery, and integration.</span></span>

<span data-ttu-id="ba733-204">Cette spécification est la base de la spécification OpenAPI (OAS). Elle a été développée par une communauté ouverte, transparente et collaborative pour normaliser la façon dont les interfaces RESTful sont définies.</span><span class="sxs-lookup"><span data-stu-id="ba733-204">The specification is the basis of the OpenAPI Specification (OAS) and is developed in an open, transparent, and collaborative community to standardize the way RESTful interfaces are defined.</span></span>

<span data-ttu-id="ba733-205">La spécification permet de définir la façon dont un service peut être découvert et la façon dont ses fonctionnalités sont comprises.</span><span class="sxs-lookup"><span data-stu-id="ba733-205">The specification defines the structure for how a service can be discovered and how its capabilities understood.</span></span> <span data-ttu-id="ba733-206">Pour plus d’informations, notamment sur l’éditeur web Swagger, et pour obtenir les exemples de spécifications Swagger d’entreprises comme Spotify, Uber, Slack et Microsoft, consultez le site Swagger (<https://swagger.io/>).</span><span class="sxs-lookup"><span data-stu-id="ba733-206">For more information, including a web editor and examples of Swagger specifications from companies like Spotify, Uber, Slack, and Microsoft, see the Swagger site (<https://swagger.io/>).</span></span>

### <a name="why-use-swagger"></a><span data-ttu-id="ba733-207">Pourquoi utiliser Swagger ?</span><span class="sxs-lookup"><span data-stu-id="ba733-207">Why use Swagger?</span></span>

<span data-ttu-id="ba733-208">Voici pourquoi il est utile de générer des métadonnées Swagger pour votre API.</span><span class="sxs-lookup"><span data-stu-id="ba733-208">The main reasons to generate Swagger metadata for your APIs are the following.</span></span>

<span data-ttu-id="ba733-209">**Les autres produits peuvent consommer et intégrer automatiquement vos API**.</span><span class="sxs-lookup"><span data-stu-id="ba733-209">**Ability for other products to automatically consume and integrate your APIs**.</span></span> <span data-ttu-id="ba733-210">Swagger est pris en charge par des dizaines de produits et [d’outils professionnels](https://swagger.io/commercial-tools/), ainsi que par un grand nombre de [bibliothèques et de frameworks](https://swagger.io/open-source-integrations/).</span><span class="sxs-lookup"><span data-stu-id="ba733-210">Dozens of products and [commercial tools](https://swagger.io/commercial-tools/) and many [libraries and frameworks](https://swagger.io/open-source-integrations/) support Swagger.</span></span> <span data-ttu-id="ba733-211">Microsoft propose des produits et des outils de niveau supérieur qui peuvent consommer automatiquement les API Swagger, comme celles qui suivent :</span><span class="sxs-lookup"><span data-stu-id="ba733-211">Microsoft has high-level products and tools that can automatically consume Swagger-based APIs, such as the following:</span></span>

-   <span data-ttu-id="ba733-212">[AutoRest](https://github.com/Azure/AutoRest).</span><span class="sxs-lookup"><span data-stu-id="ba733-212">[AutoRest](https://github.com/Azure/AutoRest).</span></span> <span data-ttu-id="ba733-213">Vous pouvez générer automatiquement des classes client .NET pour appeler Swagger.</span><span class="sxs-lookup"><span data-stu-id="ba733-213">You can automatically generate .NET client classes for calling Swagger.</span></span> <span data-ttu-id="ba733-214">Cet outil peut être utilisé à partir de l’interface CLI. En outre, il s’intègre à Visual Studio pour une utilisation facilitée via l’interface utilisateur graphique.</span><span class="sxs-lookup"><span data-stu-id="ba733-214">This tool can be used from the CLI and it also integrates with Visual Studio for easy use through the GUI.</span></span>

-   <span data-ttu-id="ba733-215">[Microsoft Flow](https://flow.microsoft.com/en-us/).</span><span class="sxs-lookup"><span data-stu-id="ba733-215">[Microsoft Flow](https://flow.microsoft.com/en-us/).</span></span> <span data-ttu-id="ba733-216">Vous pouvez [utiliser et intégrer votre API](https://flow.microsoft.com/en-us/blog/integrating-custom-api/) automatiquement dans un flux de travail Microsoft Flow de haut niveau, sans avoir de compétences en programmation.</span><span class="sxs-lookup"><span data-stu-id="ba733-216">You can automatically [use and integrate your API](https://flow.microsoft.com/en-us/blog/integrating-custom-api/) into a high-level Microsoft Flow workflow, with no programming skills required.</span></span>

-   <span data-ttu-id="ba733-217">[Microsoft PowerApps](https://powerapps.microsoft.com/en-us/).</span><span class="sxs-lookup"><span data-stu-id="ba733-217">[Microsoft PowerApps](https://powerapps.microsoft.com/en-us/).</span></span> <span data-ttu-id="ba733-218">Vous pouvez consommer automatiquement votre API à partir [d’applications mobiles PowerApps](https://powerapps.microsoft.com/en-us/blog/register-and-use-custom-apis-in-powerapps/) créées dans [PowerApps Studio](https://powerapps.microsoft.com/en-us/guided-learning/learning-powerapps-parts/), sans avoir de compétences en programmation.</span><span class="sxs-lookup"><span data-stu-id="ba733-218">You can automatically consume your API from [PowerApps mobile apps](https://powerapps.microsoft.com/en-us/blog/register-and-use-custom-apis-in-powerapps/) built with [PowerApps Studio](https://powerapps.microsoft.com/en-us/guided-learning/learning-powerapps-parts/), with no programming skills required.</span></span>

-   <span data-ttu-id="ba733-219">[Applications logiques Azure App Service](https://docs.microsoft.com/azure/app-service-logic/app-service-logic-what-are-logic-apps).</span><span class="sxs-lookup"><span data-stu-id="ba733-219">[Azure App Service Logic Apps](https://docs.microsoft.com/azure/app-service-logic/app-service-logic-what-are-logic-apps).</span></span> <span data-ttu-id="ba733-220">Vous pouvez [utiliser et intégrer votre API dans une application logique Azure App Service](https://docs.microsoft.com/azure/app-service-logic/app-service-logic-custom-hosted-api) automatiquement, sans avoir de compétences en programmation.</span><span class="sxs-lookup"><span data-stu-id="ba733-220">You can automatically [use and integrate your API into an Azure App Service Logic App](https://docs.microsoft.com/azure/app-service-logic/app-service-logic-custom-hosted-api), with no programming skills required.</span></span>

<span data-ttu-id="ba733-221">**Vous pouvez générer automatiquement la documentation de l’API**.</span><span class="sxs-lookup"><span data-stu-id="ba733-221">**Ability to automatically generate API documentation**.</span></span> <span data-ttu-id="ba733-222">Lorsque vous créez des API RESTful à grande échelle, telles que des applications de microservice complexes, vous devez gérer de nombreux points de terminaison avec les différents modèles de données utilisés dans les charges utiles de demande et de réponse.</span><span class="sxs-lookup"><span data-stu-id="ba733-222">When you create large-scale RESTful APIs, such as complex microservice-based applications, you need to handle many endpoints with different data models used in the request and response payloads.</span></span> <span data-ttu-id="ba733-223">Une documentation appropriée et un explorateur d’API solide (comme ceux fournis par Swagger) sont essentiels au succès de votre API et à son adoption par les développeurs.</span><span class="sxs-lookup"><span data-stu-id="ba733-223">Having proper documentation and having a solid API explorer, as you get with Swagger, is key for the success of your API and adoption by developers.</span></span>

<span data-ttu-id="ba733-224">Les métadonnées Swagger sont utilisées par Microsoft Flow, PowerApps et Azure Logic Apps pour comprendre comment utiliser les API et s’y connecter.</span><span class="sxs-lookup"><span data-stu-id="ba733-224">Swagger’s metadata is what Microsoft Flow, PowerApps, and Azure Logic Apps use to understand how to use APIs and connect to them.</span></span>

### <a name="how-to-automate-api-swagger-metadata-generation-with-the-swashbuckle-nuget-package"></a><span data-ttu-id="ba733-225">Comment automatiser la génération de métadonnées d’API Swagger avec le package NuGet Swashbuckle</span><span class="sxs-lookup"><span data-stu-id="ba733-225">How to automate API Swagger metadata generation with the Swashbuckle NuGet package</span></span>

<span data-ttu-id="ba733-226">La génération manuelle de métadonnées Swagger (dans un fichier JSON ou YAML) peut être fastidieuse.</span><span class="sxs-lookup"><span data-stu-id="ba733-226">Generating Swagger metadata manually (in a JSON or YAML file) can be tedious work.</span></span> <span data-ttu-id="ba733-227">Toutefois, vous pouvez automatiser la découverte d’API des services d’API web ASP.NET à l’aide du [package NuGet Swashbuckle](https://aka.ms/swashbuckledotnetcore) afin de générer dynamiquement les métadonnées d’API Swagger.</span><span class="sxs-lookup"><span data-stu-id="ba733-227">However, you can automate API discovery of ASP.NET Web API services by using the [Swashbuckle NuGet package](https://aka.ms/swashbuckledotnetcore) to dynamically generate Swagger API metadata.</span></span>

<span data-ttu-id="ba733-228">Swashbuckle génère automatiquement les métadonnées Swagger pour vos projets d’API web ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="ba733-228">Swashbuckle automatically generates Swagger metadata for your ASP.NET Web API projects.</span></span> <span data-ttu-id="ba733-229">Il prend en charge les projets d’API web ASP.NET Core et l’API web ASP.NET traditionnelle, ainsi que toutes les autres versions, telles qu’Azure API App, Azure Mobile App ou les microservices Azure Service Fabric reposant sur ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="ba733-229">It supports ASP.NET Core Web API projects and the traditional ASP.NET Web API and any other flavor, such as Azure API App, Azure Mobile App, Azure Service Fabric microservices based on ASP.NET.</span></span> <span data-ttu-id="ba733-230">Il prend également en charge les API web simples déployées dans des conteneurs, comme l’application de référence.</span><span class="sxs-lookup"><span data-stu-id="ba733-230">It also supports plain Web API deployed on containers, as in for the reference application.</span></span>

<span data-ttu-id="ba733-231">Swashbuckle associe l’explorateur d’API et Swagger (ou [swagger-ui](https://github.com/swagger-api/swagger-ui)) pour fournir aux utilisateurs de votre API des fonctionnalités avancées de découverte et de documentation.</span><span class="sxs-lookup"><span data-stu-id="ba733-231">Swashbuckle combines API Explorer and Swagger or [swagger-ui](https://github.com/swagger-api/swagger-ui) to provide a rich discovery and documentation experience for your API consumers.</span></span> <span data-ttu-id="ba733-232">Outre son moteur de génération de métadonnées Swagger, Swashbuckle contient également une version intégrée de swagger-ui, qu’il fournit automatiquement après son installation.</span><span class="sxs-lookup"><span data-stu-id="ba733-232">In addition to its Swagger metadata generator engine, Swashbuckle also contains an embedded version of swagger-ui, which it will automatically serve up once Swashbuckle is installed.</span></span>

<span data-ttu-id="ba733-233">Cela signifie que vous pouvez compléter votre API avec une interface utilisateur de découverte pour aider les développeurs à utiliser votre API.</span><span class="sxs-lookup"><span data-stu-id="ba733-233">This means you can complement your API with a nice discovery UI to help developers to use your API.</span></span> <span data-ttu-id="ba733-234">Elle nécessite très peu de code et de maintenance, car elle est générée automatiquement, ce qui vous permet de vous concentrer sur la création de votre API.</span><span class="sxs-lookup"><span data-stu-id="ba733-234">It requires a very small amount of code and maintenance because it is automatically generated, allowing you to focus on building your API.</span></span> <span data-ttu-id="ba733-235">Le résultat de l’explorateur d’API ressemble à celui de la Figure 8-8.</span><span class="sxs-lookup"><span data-stu-id="ba733-235">The result for the API Explorer looks like Figure 8-8.</span></span>

![](./media/image9.png)

<span data-ttu-id="ba733-236">**Figure 8-8**.</span><span class="sxs-lookup"><span data-stu-id="ba733-236">**Figure 8-8**.</span></span> <span data-ttu-id="ba733-237">L’explorateur d’API Swashbuckle basé sur les métadonnées Swagger - Microservice de catalogue eShopOnContainers</span><span class="sxs-lookup"><span data-stu-id="ba733-237">Swashbuckle API Explorer based on Swagger metadata—eShopOnContainers catalog microservice</span></span>

<span data-ttu-id="ba733-238">L’explorateur d’API n’est pas le plus important ici.</span><span class="sxs-lookup"><span data-stu-id="ba733-238">The API explorer is not the most important thing here.</span></span> <span data-ttu-id="ba733-239">Une fois que votre API web peut se décrire dans les métadonnées Swagger, elle peut être utilisée facilement dans les outils Swagger, y compris dans les générateurs de code de classe proxy client qui peuvent cibler plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="ba733-239">Once you have a Web API that can describe itself in Swagger metadata, your API can be used seamlessly from Swagger-based tools, including client proxy-class code generators that can target many platforms.</span></span> <span data-ttu-id="ba733-240">Par exemple, [AutoRest](https://github.com/Azure/AutoRest) génère automatiquement des classes client .NET.</span><span class="sxs-lookup"><span data-stu-id="ba733-240">For example, as mentioned, [AutoRest](https://github.com/Azure/AutoRest) automatically generates .NET client classes.</span></span> <span data-ttu-id="ba733-241">Toutefois, d’autres outils comme [swagger-codegen](https://github.com/swagger-api/swagger-codegen) sont également disponibles, et permettent la génération automatique de code pour les bibliothèques clientes d’API, pour les stubs serveur et pour la documentation.</span><span class="sxs-lookup"><span data-stu-id="ba733-241">But additional tools like [swagger-codegen](https://github.com/swagger-api/swagger-codegen) are also available, which allow code generation of API client libraries, server stubs, and documentation automatically.</span></span>

<span data-ttu-id="ba733-242">Actuellement, Swashbuckle se compose de deux packages NuGet internes situés sous le métapackage de niveau supérieur [Swashbuckle.AspNetCore](https://www.nuget.org/packages/Swashbuckle.AspNetCore/) version 1.0.0 ou ultérieure pour les applications ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="ba733-242">Currently, Swashbuckle consists of several internal NuGet packages under the high-level meta-package [Swashbuckle.AspNetCore](https://www.nuget.org/packages/Swashbuckle.AspNetCore/) version 1.0.0 or later for ASP.NET Core applications.</span></span>

<span data-ttu-id="ba733-243">Lorsque vous avez installé ces packages NuGet dans votre projet d’API web, vous devez configurer Swagger dans la classe de démarrage, comme dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="ba733-243">After you have installed these NuGet packages in your Web API project, you need to configure Swagger in the Startup class, as in the following code:</span></span>

```csharp
public class Startup
{
    public IConfigurationRoot Configuration { get; }
    // Other startup code...

    public void ConfigureServices(IServiceCollection services)
    {
        // Other ConfigureServices() code...

        // Add framework services.
        services.AddSwaggerGen(options =>
        {
            options.DescribeAllEnumsAsStrings();
            options.SwaggerDoc("v1", new Swashbuckle.AspNetCore.Swagger.Info
            {
                Title = "eShopOnContainers - Catalog HTTP API",
                Version = "v1",
                Description = "The Catalog Microservice HTTP API. This is a Data-Driven/CRUD microservice sample",
                TermsOfService = "Terms Of Service"
            });
        });

        // Other ConfigureServices() code...
    }

    public void Configure(IApplicationBuilder app,
        IHostingEnvironment env,
        ILoggerFactory loggerFactory)
    {
        // Other Configure() code...
        // ...
        app.UseSwagger()
            .UseSwaggerUI(c =>
            {
                c.SwaggerEndpoint("/swagger/v1/swagger.json", "My API V1");
            });
    }
}
```

<span data-ttu-id="ba733-244">Après cela, vous pouvez démarrer votre application et parcourir les points de terminaison JSON et d’interface utilisateur Swagger suivants à l’aide d’URL de ce type :</span><span class="sxs-lookup"><span data-stu-id="ba733-244">Once this is done, you can start your application and browse the following Swagger JSON and UI endpoints using URLs like these:</span></span>

```json
  http://<your-root-url>/swagger/v1/swagger.json
  
  http://<your-root-url>/swagger/
```

<span data-ttu-id="ba733-245">Vous avez déjà vu l’interface utilisateur générée par Swashbuckle pour une URL telle que `http://<your-root-url>/swagger/ui`.</span><span class="sxs-lookup"><span data-stu-id="ba733-245">You previously saw the generated UI created by Swashbuckle for a URL like `http://<your-root-url>/swagger/ui`.</span></span> <span data-ttu-id="ba733-246">Dans la Figure 8-9, vous pouvez également voir comment tester une méthode d’API.</span><span class="sxs-lookup"><span data-stu-id="ba733-246">In Figure 8-9 you can also see how you can test any API method.</span></span>

![](./media/image10.png)

<span data-ttu-id="ba733-247">**Figure 8-9**.</span><span class="sxs-lookup"><span data-stu-id="ba733-247">**Figure 8-9**.</span></span> <span data-ttu-id="ba733-248">Interface utilisateur Swashbuckle UI testant la méthode d’API Catalog/Items</span><span class="sxs-lookup"><span data-stu-id="ba733-248">Swashbuckle UI testing the Catalog/Items API method</span></span>

<span data-ttu-id="ba733-249">La Figure 8-10 montre les métadonnées JSON Swagger générées à partir du microservice eShopOnContainers (utilisé par les outils ci-dessous) lorsque vous envoyez une requête pour &lt;votre-url-racine&gt;/swagger/v1/swagger.json à l’aide de [Postman](https://www.getpostman.com/).</span><span class="sxs-lookup"><span data-stu-id="ba733-249">Figure 8-10 shows the Swagger JSON metadata generated from the eShopOnContainers microservice (which is what the tools use underneath) when you request &lt;your-root-url&gt;/swagger/v1/swagger.json using [Postman](https://www.getpostman.com/).</span></span>

![](./media/image11.png)

<span data-ttu-id="ba733-250">**Figure 8-10**.</span><span class="sxs-lookup"><span data-stu-id="ba733-250">**Figure 8-10**.</span></span> <span data-ttu-id="ba733-251">Métadonnées JSON Swagger</span><span class="sxs-lookup"><span data-stu-id="ba733-251">Swagger JSON metadata</span></span>

<span data-ttu-id="ba733-252">C’est aussi simple que cela.</span><span class="sxs-lookup"><span data-stu-id="ba733-252">It is that simple.</span></span> <span data-ttu-id="ba733-253">Et parce qu’elles sont générées automatiquement, les métadonnées Swagger grandissent à mesure que vous ajoutez des fonctionnalités à votre API.</span><span class="sxs-lookup"><span data-stu-id="ba733-253">And because it is automatically generated, the Swagger metadata will grow when you add more functionality to your API.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="ba733-254">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ba733-254">Additional resources</span></span>

-   <span data-ttu-id="ba733-255">**Pages d’aide d’API web ASP.NET Core à l’aide de Swagger**
    [*https://docs.microsoft.com/aspnet/core/tutorials/web-api-help-pages-using-swagger*](https://docs.microsoft.com/aspnet/core/tutorials/web-api-help-pages-using-swagger)</span><span class="sxs-lookup"><span data-stu-id="ba733-255">**ASP.NET Web API Help Pages using Swagger**
[*https://docs.microsoft.com/aspnet/core/tutorials/web-api-help-pages-using-swagger*](https://docs.microsoft.com/aspnet/core/tutorials/web-api-help-pages-using-swagger)</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="ba733-256">[Précédent](microservice-application-design.md)
[Suivant](multi-container-applications-docker-compose.md)</span><span class="sxs-lookup"><span data-stu-id="ba733-256">[Previous](microservice-application-design.md)
[Next](multi-container-applications-docker-compose.md)</span></span>
