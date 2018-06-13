---
title: Utiliser des données dans les applications ASP.NET Core
description: Architecturer des applications web modernes avec ASP.NET Core et Azure | Utilisation de données dans les applications ASP.NET Core
author: ardalis
ms.author: wiwagn
ms.date: 10/07/2017
ms.openlocfilehash: 89df46c8e04e1826c84058e5d2a92d089eb96098
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33592520"
---
# <a name="working-with-data-in-aspnet-core-apps"></a><span data-ttu-id="7f968-103">Utilisation de données dans les applications ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="7f968-103">Working with Data in ASP.NET Core Apps</span></span>

> <span data-ttu-id="7f968-104">« Les données sont une chose précieuse et durent plus longtemps que les systèmes eux-mêmes. »</span><span class="sxs-lookup"><span data-stu-id="7f968-104">"Data is a precious thing and will last longer than the systems themselves."</span></span>

<span data-ttu-id="7f968-105">Tim Berners-Lee</span><span class="sxs-lookup"><span data-stu-id="7f968-105">Tim Berners-Lee</span></span>

## <a name="summary"></a><span data-ttu-id="7f968-106">Récapitulatif</span><span class="sxs-lookup"><span data-stu-id="7f968-106">Summary</span></span>

<span data-ttu-id="7f968-107">L’accès aux données est une partie importante de la plupart des applications logicielles.</span><span class="sxs-lookup"><span data-stu-id="7f968-107">Data access is an important part of almost any software application.</span></span> <span data-ttu-id="7f968-108">ASP.NET Core prend en charge diverses options d’accès aux données, notamment Entity Framework Core (et Entity Framework 6), et peut fonctionner avec tout framework d’accès aux données .NET.</span><span class="sxs-lookup"><span data-stu-id="7f968-108">ASP.NET Core supports a variety of data access options, including Entity Framework Core (and Entity Framework 6 as well), and can work with any .NET data access framework.</span></span> <span data-ttu-id="7f968-109">Le choix du framework d’accès aux données à utiliser dépend des besoins de l’application.</span><span class="sxs-lookup"><span data-stu-id="7f968-109">The choice of which data access framework to use depends on the application's needs.</span></span> <span data-ttu-id="7f968-110">L’abstraction de ces choix par rapport aux projets d’interface utilisateur et ApplicationCore, ainsi que l’encapsulation des détails d’implémentation dans l’infrastructure, permettent de produire des logiciels faiblement couplés et testables.</span><span class="sxs-lookup"><span data-stu-id="7f968-110">Abstracting these choices from the ApplicationCore and UI projects, and encapsulating implementation details in Infrastructure, helps to produce loosely coupled, testable software.</span></span>

## <a name="entity-framework-core-for-relational-databases"></a><span data-ttu-id="7f968-111">Entity Framework Core (pour les bases de données relationnelles)</span><span class="sxs-lookup"><span data-stu-id="7f968-111">Entity Framework Core (for relational databases)</span></span>

<span data-ttu-id="7f968-112">Si vous écrivez une application ASP.NET Core qui doit fonctionner avec des données relationnelles, Entity Framework Core (EF Core) est la méthode recommandée pour l’accès de l’application à ses données.</span><span class="sxs-lookup"><span data-stu-id="7f968-112">If you're writing a new ASP.NET Core application that needs to work with relational data, then Entity Framework Core (EF Core) is the recommended way for your application to access its data.</span></span> <span data-ttu-id="7f968-113">EF Core est un mappeur objet-relationnel (ORM) qui permet aux développeurs .NET de conserver des objets vers et à partir d’une source de données.</span><span class="sxs-lookup"><span data-stu-id="7f968-113">EF Core is an object-relational mapper (O/RM) that enables .NET developers to persist objects to and from a data source.</span></span> <span data-ttu-id="7f968-114">Du coup, ils n’ont plus à écrire une grande partie du code d’accès aux données qu’ils devraient généralement écrire.</span><span class="sxs-lookup"><span data-stu-id="7f968-114">It eliminates the need for most of the data access code developers would typically need to write.</span></span> <span data-ttu-id="7f968-115">Comme ASP.NET Core, EF Core a été entièrement réécrit afin de prendre en charge les applications multiplateformes modulaires.</span><span class="sxs-lookup"><span data-stu-id="7f968-115">Like ASP.NET Core, EF Core has been rewritten from the ground up to support modular cross-platform applications.</span></span> <span data-ttu-id="7f968-116">Vous l’ajoutez à votre application en tant que package NuGet, vous le configurez dans Startup et vous le demandez par l’intermédiaire de l’injection de dépendances quand vous en avez besoin.</span><span class="sxs-lookup"><span data-stu-id="7f968-116">You add it to your application as a NuGet package, configure it in Startup, and request it through dependency injection wherever you need it.</span></span>

<span data-ttu-id="7f968-117">Pour utiliser EF Core avec une base de données SQL Server, exécutez la commande d’interface CLI dotnet suivante :</span><span class="sxs-lookup"><span data-stu-id="7f968-117">To use EF Core with a SQL Server database, run the following dotnet CLI command:</span></span>

<span data-ttu-id="7f968-118">dotnet add package Microsoft.EntityFrameworkCore.SqlServer</span><span class="sxs-lookup"><span data-stu-id="7f968-118">dotnet add package Microsoft.EntityFrameworkCore.SqlServer</span></span>

<span data-ttu-id="7f968-119">Pour ajouter la prise en charge d’une source de données InMemory, à des fins de test :</span><span class="sxs-lookup"><span data-stu-id="7f968-119">To add support for an InMemory data source, for testing:</span></span>

<span data-ttu-id="7f968-120">dotnet add package Microsoft.EntityFrameworkCore.InMemory</span><span class="sxs-lookup"><span data-stu-id="7f968-120">dotnet add package Microsoft.EntityFrameworkCore.InMemory</span></span>

### <a name="the-dbcontext"></a><span data-ttu-id="7f968-121">Le DbContext</span><span class="sxs-lookup"><span data-stu-id="7f968-121">The DbContext</span></span>

<span data-ttu-id="7f968-122">Pour travailler avec EF Core, vous avez besoin d’une sous-classe de DbContext.</span><span class="sxs-lookup"><span data-stu-id="7f968-122">To work with EF Core, you need a subclass of DbContext.</span></span> <span data-ttu-id="7f968-123">Cette classe contient des propriétés représentant des collections d’entités que votre application utilisera.</span><span class="sxs-lookup"><span data-stu-id="7f968-123">This class holds properties representing collections of the entities your application will work with.</span></span> <span data-ttu-id="7f968-124">L’exemple eShopOnWeb comprend un CatalogContext avec des collections d’éléments, de marques et de types :</span><span class="sxs-lookup"><span data-stu-id="7f968-124">The eShopOnWeb sample includes a CatalogContext with collections for items, brands, and types:</span></span>

```csharp
public class CatalogContext : DbContext
{
    public CatalogContext(DbContextOptions<CatalogContext> options) : base(options)
    {

    }

    public DbSet<CatalogItem> CatalogItems { get; set; }

    public DbSet<CatalogBrand> CatalogBrands { get; set; }

    public DbSet<CatalogType> CatalogTypes { get; set; }
}
```

<span data-ttu-id="7f968-125">Votre DbContext doit avoir un constructeur qui accepte des DbContextOptions et passer cet argument au constructeur DbContext de base.</span><span class="sxs-lookup"><span data-stu-id="7f968-125">Your DbContext must have a constructor that accepts DbContextOptions and pass this argument to the base DbContext constructor.</span></span> <span data-ttu-id="7f968-126">Notez que si vous n’avez qu’un seul DbContext dans votre application, vous pouvez passer une instance de DbContextOptions, mais si vous en avez plusieurs vous devez utiliser le type DbContextOptions<T> générique et passer votre type DbContext comme paramètre générique.</span><span class="sxs-lookup"><span data-stu-id="7f968-126">Note that if you have only one DbContext in your application, you can pass an instance of DbContextOptions, but if you have more than one you must use the generic DbContextOptions<T> type, passing in your DbContext type as the generic parameter.</span></span>

### <a name="configuring-ef-core"></a><span data-ttu-id="7f968-127">Configuration d’EF Core</span><span class="sxs-lookup"><span data-stu-id="7f968-127">Configuring EF Core</span></span>

<span data-ttu-id="7f968-128">Dans votre application ASP.NET Core, vous devez généralement configurer EF Core dans votre méthode ConfigureServices.</span><span class="sxs-lookup"><span data-stu-id="7f968-128">In your ASP.NET Core application, you'll typically configure EF Core in your ConfigureServices method.</span></span> <span data-ttu-id="7f968-129">EF Core utilise un DbContextOptionsBuilder, qui prend en charge plusieurs méthodes d’extension utiles pour simplifier sa configuration.</span><span class="sxs-lookup"><span data-stu-id="7f968-129">EF Core uses a DbContextOptionsBuilder, which supports several helpful extension methods to streamline its configuration.</span></span> <span data-ttu-id="7f968-130">Pour configurer CatalogContext afin d’utiliser une base de données SQL Server avec une chaîne de connexion définie dans Configuration, vous devez ajouter le code suivant à ConfigureServices :</span><span class="sxs-lookup"><span data-stu-id="7f968-130">To configure CatalogContext to use a SQL Server database with a connection string defined in Configuration, you would add the following code to ConfigureServices:</span></span>

```csharp
services.AddDbContext<CatalogContext>(options => options.UseSqlServer (Configuration.GetConnectionString("DefaultConnection")));
```

<span data-ttu-id="7f968-131">Pour utiliser la base de données en mémoire :</span><span class="sxs-lookup"><span data-stu-id="7f968-131">To use the in-memory database:</span></span>

```csharp
services.AddDbContext<CatalogContext>(options =>
    options.UseInMemoryDatabase());
```

<span data-ttu-id="7f968-132">Une fois que vous avez installé Core EF, que vous avez créé un type enfant DbContext et que vous l’avez configuré dans ConfigureServices, vous êtes prêt à utiliser EF Core.</span><span class="sxs-lookup"><span data-stu-id="7f968-132">Once you have installed EF Core, created a DbContext child type, and configured it in ConfigureServices, you are ready to use EF Core.</span></span> <span data-ttu-id="7f968-133">Vous pouvez demander une instance de votre type DbContext dans n’importe quel service qui en a besoin, et commencer à travailler avec vos entités persistantes à l’aide de LINQ comme si elles se trouvaient simplement dans une collection.</span><span class="sxs-lookup"><span data-stu-id="7f968-133">You can request an instance of your DbContext type in any service that needs it, and start working with your persisted entities using LINQ as if they were simply in a collection.</span></span> <span data-ttu-id="7f968-134">EF Core effectue la traduction de vos expressions LINQ en requêtes SQL pour stocker et récupérer vos données.</span><span class="sxs-lookup"><span data-stu-id="7f968-134">EF Core does the work of translating your LINQ expressions into SQL queries to store and retrieve your data.</span></span>

<span data-ttu-id="7f968-135">Vous pouvez voir les requêtes qu’EF Core exécute en configurant un enregistreur d’événements et en réglant son niveau au moins sur Informations, comme indiqué dans la Figure 8-1.</span><span class="sxs-lookup"><span data-stu-id="7f968-135">You can see the queries EF Core is executing by configuring a logger and ensuring its level is set to at least Information, as shown in Figure 8-1.</span></span>

![](./media/image8-1.png)

<span data-ttu-id="7f968-136">Figure 8-1 Journalisation des requêtes EF Core dans la console</span><span class="sxs-lookup"><span data-stu-id="7f968-136">Figure 8-1 Logging EF Core queries to the console</span></span>

### <a name="fetching-and-storing-data"></a><span data-ttu-id="7f968-137">Extraction et stockage des données</span><span class="sxs-lookup"><span data-stu-id="7f968-137">Fetching and Storing Data</span></span>

<span data-ttu-id="7f968-138">Pour récupérer des données à partir d’EF Core, vous devez accéder à la propriété appropriée et utiliser LINQ afin de filtrer le résultat.</span><span class="sxs-lookup"><span data-stu-id="7f968-138">To retrieve data from EF Core, you access the appropriate property and use LINQ to filter the result.</span></span> <span data-ttu-id="7f968-139">Vous pouvez également utiliser LINQ pour effectuer une projection et transformer le résultat d’un type en un autre.</span><span class="sxs-lookup"><span data-stu-id="7f968-139">You can also use LINQ to perform projection, transforming the result from one type to another.</span></span> <span data-ttu-id="7f968-140">L’exemple suivant permet de récupérer des CatalogBrands, classés par nom, filtrés d’après leur propriété Enabled et projetés sur un type SelectListItem :</span><span class="sxs-lookup"><span data-stu-id="7f968-140">The following example would retrieve CatalogBrands, ordered by name, filtered by their Enabled property, and projected onto a SelectListItem type:</span></span>

```csharp
var brandItems = await _context.CatalogBrands
    .Where(b => b.Enabled)
    .OrderBy(b => b.Name)
    .Select(b => new SelectListItem {
        Value = b.Id, Text = b.Name })
    .ToListAsync();
```

<span data-ttu-id="7f968-141">Il est important dans l’exemple ci-dessus d’ajouter l’appel à ToListAsync afin d’exécuter la requête immédiatement.</span><span class="sxs-lookup"><span data-stu-id="7f968-141">It's important in the above example to add the call to ToListAsync in order to execute the query immediately.</span></span> <span data-ttu-id="7f968-142">Sinon, l’instruction affecte un IQueryable<SelectListItem> à brandItems, qui ne sera pas exécutée avant son énumération.</span><span class="sxs-lookup"><span data-stu-id="7f968-142">Otherwise, the statement will assign an IQueryable<SelectListItem> to brandItems, which will not be executed until it is enumerated.</span></span> <span data-ttu-id="7f968-143">Le fait de retourner des résultats IQueryable à partir de méthodes présente des avantages et des inconvénients.</span><span class="sxs-lookup"><span data-stu-id="7f968-143">There are pros and cons to returning IQueryable results from methods.</span></span> <span data-ttu-id="7f968-144">Cela permet de modifier davantage la requête qu’EF Core construira, mais peut également provoquer des erreurs qui se produiront uniquement au moment de l’exécution, si des opérations sont ajoutées à la requête qu’EF Core ne peut pas traduire.</span><span class="sxs-lookup"><span data-stu-id="7f968-144">It allows the query EF Core will construct to be further modified, but can also result in errors that only occur at runtime, if operations are added to the query that EF Core cannot translate.</span></span> <span data-ttu-id="7f968-145">Il est généralement plus sûr de passer les filtres à la méthode qui effectue l’accès aux données, et de retourner une collection en mémoire (par exemple, List<T>) comme résultat.</span><span class="sxs-lookup"><span data-stu-id="7f968-145">It's generally safer to pass any filters into the method performing the data access, and return back an in-memory collection (for example, List<T>) as the result.</span></span>

<span data-ttu-id="7f968-146">EF Core effectue le suivi des modifications apportées aux entités qu’il extrait de la persistance.</span><span class="sxs-lookup"><span data-stu-id="7f968-146">EF Core tracks changes on entities it fetches from persistence.</span></span> <span data-ttu-id="7f968-147">Pour enregistrer les modifications apportées à une entité suivie, il vous suffit d’appeler la méthode SaveChanges sur le DbContext, en vérifiant qu’il s’agit de la même instance de DbContext que celle utilisée pour extraire l’entité.</span><span class="sxs-lookup"><span data-stu-id="7f968-147">To save changes to a tracked entity, you just call the SaveChanges method on the DbContext, making sure it's the same DbContext instance that was used to fetch the entity.</span></span> <span data-ttu-id="7f968-148">L’ajout et la suppression d’entités s’effectuent directement sur la propriété DbSet appropriée, là aussi avec un appel à SaveChanges pour exécuter les commandes de base de données.</span><span class="sxs-lookup"><span data-stu-id="7f968-148">Adding and removing entities is directly on the appropriate DbSet property, again with a call to SaveChanges to execute the database commands.</span></span> <span data-ttu-id="7f968-149">L’exemple suivant illustre l’ajout, la mise à jour et la suppression d’entités de la persistance.</span><span class="sxs-lookup"><span data-stu-id="7f968-149">The following example demonstrates adding, updating, and removing entities from persistence.</span></span>

```csharp
// create
var newBrand = new CatalogBrand() { Brand = "Acme" };
_context.Add(newBrand);
await _context.SaveChangesAsync();

// read and update
var existingBrand = _context.CatalogBrands.Find(1);
existingBrand.Brand = "Updated Brand";
await _context.SaveChangesAsync();

// read and delete (alternate Find syntax)
var brandToDelete = _context.Find<CatalogBrand>(2);
_context.CatalogBrands.Remove(brandToDelete);
await _context.SaveChangesAsync();
```

<span data-ttu-id="7f968-150">EF Core prend en charge les méthodes synchrones et asynchrones pour l’extraction et l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="7f968-150">EF Core supports both synchronous and async methods for fetching and saving.</span></span> <span data-ttu-id="7f968-151">Dans les applications web, nous vous recommandons d’utiliser le modèle async/await avec les méthodes asynchrones, afin que les threads du serveur web ne soient pas bloqués pendant qu’ils attendent la fin des opérations d’accès aux données.</span><span class="sxs-lookup"><span data-stu-id="7f968-151">In web applications, it's recommended to use the async/await pattern with the async methods, so that web server threads are not blocked while waiting for data access operations to complete.</span></span>

### <a name="fetching-related-data"></a><span data-ttu-id="7f968-152">Extraction de données associées</span><span class="sxs-lookup"><span data-stu-id="7f968-152">Fetching Related Data</span></span>

<span data-ttu-id="7f968-153">Quand EF Core récupère des entités, il remplit toutes les propriétés qui sont stockées directement avec cette entité dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="7f968-153">When EF Core retrieves entities, it populates all of the properties that are stored directly with that entity in the database.</span></span> <span data-ttu-id="7f968-154">Les propriétés de navigation (telles que les listes d’entités associées) ne sont pas remplies, et leur valeur peut être définie sur null.</span><span class="sxs-lookup"><span data-stu-id="7f968-154">Navigation properties, such as lists of related entities, are not populated and may have their value set to null.</span></span> <span data-ttu-id="7f968-155">Cela garantit qu’EF Core n’extrait pas plus de données que nécessaire, ce qui est particulièrement important pour les applications web, qui doivent rapidement traiter les requêtes et retourner des réponses de manière efficace.</span><span class="sxs-lookup"><span data-stu-id="7f968-155">This ensures EF Core is not fetching more data than is needed, which is especially important for web applications, which must quickly process requests and return responses in an efficient manner.</span></span> <span data-ttu-id="7f968-156">Pour inclure des relations avec une entité en utilisant le *chargement hâtif*, vous spécifiez la propriété à l’aide de la méthode d’extension Include sur la requête, comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="7f968-156">To include relationships with an entity using *eager loading*, you specify the property using the Include extension method on the query, as shown:</span></span>

```csharp
// .Include requires using Microsoft.EntityFrameworkCore
var brandsWithItems = await _context.CatalogBrands
    .Include(b => b.Items)
    .ToListAsync();
```

<span data-ttu-id="7f968-157">Vous pouvez inclure plusieurs relations, et également inclure des sous-relations à l’aide de ThenInclude.</span><span class="sxs-lookup"><span data-stu-id="7f968-157">You can include multiple relationships, and you can also include sub-relationships using ThenInclude.</span></span> <span data-ttu-id="7f968-158">EF Core exécutera une seule requête pour récupérer le jeu d’entités résultant.</span><span class="sxs-lookup"><span data-stu-id="7f968-158">EF Core will execute a single query to retrieve the resulting set of entities.</span></span>

<span data-ttu-id="7f968-159">Une autre option de chargement des données associées consiste à utiliser le *chargement explicite*.</span><span class="sxs-lookup"><span data-stu-id="7f968-159">Another option for loading related data is to use *explicit loading*.</span></span> <span data-ttu-id="7f968-160">Le chargement explicite vous permet de charger des données supplémentaires dans une entité qui a déjà été récupérée.</span><span class="sxs-lookup"><span data-stu-id="7f968-160">Explicit loading allows you to load additional data into an entity that has already been retrieved.</span></span> <span data-ttu-id="7f968-161">Comme cela implique une requête distincte à la base de données, ce n’est pas recommandé pour les applications web, qui doivent réduire le nombre d’allers-retours vers la base de données effectués par requête.</span><span class="sxs-lookup"><span data-stu-id="7f968-161">Since this involves a separate request to the database, it's not recommended for web applications, which should minimize the number of database round trips made per request.</span></span>

<span data-ttu-id="7f968-162">Le *chargement différé* est une fonctionnalité qui charge automatiquement les données associées telles qu’elles sont référencées par l’application.</span><span class="sxs-lookup"><span data-stu-id="7f968-162">*Lazy loading* is a feature that automatically loads related data as it is referenced by the application.</span></span> <span data-ttu-id="7f968-163">Il n’est pas pris en charge par EF Core actuellement, mais comme le chargement explicite il doit généralement être désactivé pour les applications web.</span><span class="sxs-lookup"><span data-stu-id="7f968-163">It's not currently supported by EF Core, but as with explicit loading it should typically be disabled for web applications.</span></span>

### <a name="resilient-connections"></a><span data-ttu-id="7f968-164">Connexions résilientes</span><span class="sxs-lookup"><span data-stu-id="7f968-164">Resilient Connections</span></span>

<span data-ttu-id="7f968-165">Les ressources externes telles que les bases de données SQL peuvent parfois être indisponibles.</span><span class="sxs-lookup"><span data-stu-id="7f968-165">External resources like SQL databases may occasionally be unavailable.</span></span> <span data-ttu-id="7f968-166">En cas d’indisponibilité temporaire, les applications peuvent utiliser une logique de nouvelle tentative pour éviter de lever une exception.</span><span class="sxs-lookup"><span data-stu-id="7f968-166">In cases of temporary unavailability, applications can use retry logic to avoid raising an exception.</span></span> <span data-ttu-id="7f968-167">Cette technique est communément appelée *résilience de la connexion*.</span><span class="sxs-lookup"><span data-stu-id="7f968-167">This technique is commonly referred to as *connection resiliency*.</span></span> <span data-ttu-id="7f968-168">Vous pouvez implémenter votre [propre technique de nouvelle tentative avec interruption exponentielle](https://docs.microsoft.com/azure/architecture/patterns/retry) en retentant une opération après un temps d’attente qui augmente de manière exponentielle, jusqu’à ce que le nombre maximal de tentatives configuré ait été atteint.</span><span class="sxs-lookup"><span data-stu-id="7f968-168">You can implement your [own retry with exponential backoff](https://docs.microsoft.com/azure/architecture/patterns/retry) technique by attempting to rety with an exponentially increasing wait time, until a maximum retry count has been reached.</span></span> <span data-ttu-id="7f968-169">Cette technique prend en compte le fait que les ressources du cloud peuvent être indisponibles par intermittence pendant de brèves périodes, ce qui entraîne l’échec de certaines requêtes.</span><span class="sxs-lookup"><span data-stu-id="7f968-169">This technique embraces the fact that cloud resources might intermittently be unavailable for short periods of time, resulting in failure of some requests.</span></span>

<span data-ttu-id="7f968-170">Pour Azure SQL DB, Entity Framework Core fournit déjà la logique de résilience et de nouvelle tentative de connexion de base de données interne.</span><span class="sxs-lookup"><span data-stu-id="7f968-170">For Azure SQL DB, Entity Framework Core already provides internal database connection resiliency and retry logic.</span></span> <span data-ttu-id="7f968-171">Par contre, vous devez autoriser la stratégie d’exécution d’Entity Framework pour chaque connexion DbContext si vous voulez avoir des connexions EF Core résilientes.</span><span class="sxs-lookup"><span data-stu-id="7f968-171">But you need to enable the Entity Framework execution strategy for each DbContext connection if you want to have resilient EF Core connections.</span></span>

<span data-ttu-id="7f968-172">Par exemple, le code suivant au niveau des connexions EF Core autorise les connexions SQL résilientes qui sont retentées si elles échouent.</span><span class="sxs-lookup"><span data-stu-id="7f968-172">For instance, the following code at the EF Core connection level enables resilient SQL connections that are retried if the connection fails.</span></span>

```csharp
// Startup.cs from any ASP.NET Core Web API
public class Startup
{
    public IServiceProvider ConfigureServices(IServiceCollection services)
    {
        //...
        services.AddDbContext<OrderingContext>(options =>
        {
            options.UseSqlServer(Configuration["ConnectionString"],
            sqlServerOptionsAction: sqlOptions =>
        {
            sqlOptions.EnableRetryOnFailure(
            maxRetryCount: 5,
            maxRetryDelay: TimeSpan.FromSeconds(30), 
            errorNumbersToAdd: null); 
        });
    });
}
//...
```

  #### <a name="execution-strategies-and-explicit-transactions-using-begintransaction-and-multiple-dbcontexts"></a><span data-ttu-id="7f968-173">Stratégies d’exécution et transactions explicites utilisant BeginTransaction et plusieurs DbContexts</span><span class="sxs-lookup"><span data-stu-id="7f968-173">Execution strategies and explicit transactions using BeginTransaction and multiple DbContexts</span></span> 
  
  <span data-ttu-id="7f968-174">Quand les nouvelles tentatives sont activées dans les connexions EF Core, chaque opération que vous effectuez avec EF Core devient sa propre opération de nouvelle tentative.</span><span class="sxs-lookup"><span data-stu-id="7f968-174">When retries are enabled in EF Core connections, each operation you perform using EF Core becomes its own retriable operation.</span></span> <span data-ttu-id="7f968-175">Chaque requête et chaque appel à SaveChanges sont retentés ensemble si une défaillance passagère se produit.</span><span class="sxs-lookup"><span data-stu-id="7f968-175">Each query and each call to SaveChanges will be retried as a unit if a transient failure occurs.</span></span>
  
  <span data-ttu-id="7f968-176">Toutefois, si votre code lance une transaction à l’aide de BeginTransaction, définissez votre propre groupe d’opérations à traiter ensemble : tout le contenu de la transaction doit être restauré si une défaillance se produit.</span><span class="sxs-lookup"><span data-stu-id="7f968-176">However, if your code initiates a transaction using BeginTransaction, you are defining your own group of operations that need to be treated as a unit—everything inside the transaction has be rolled back if a failure occurs.</span></span> <span data-ttu-id="7f968-177">Une exception semblable à la suivante s’affiche si vous tentez d’exécuter cette transaction quand vous utilisez une stratégie d’exécution EF (stratégie de nouvelle tentative) et que vous incluez dedans plusieurs SaveChanges de plusieurs DbContexts.</span><span class="sxs-lookup"><span data-stu-id="7f968-177">You will see an exception like the following if you attempt to execute that transaction when using an EF execution strategy (retry policy) and you include several SaveChanges from multiple DbContexts in it.</span></span>

<span data-ttu-id="7f968-178">System.InvalidOperationException : La stratégie d’exécution configurée « SqlServerRetryingExecutionStrategy » ne prend pas en charge les transactions lancées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7f968-178">System.InvalidOperationException: The configured execution strategy 'SqlServerRetryingExecutionStrategy' does not support user initiated transactions.</span></span> <span data-ttu-id="7f968-179">Utilisez la stratégie d’exécution retournée par « DbContext.Database.CreateExecutionStrategy() » pour exécuter toutes les opérations de la transaction en tant qu’ensemble pouvant être retenté.</span><span class="sxs-lookup"><span data-stu-id="7f968-179">Use the execution strategy returned by 'DbContext.Database.CreateExecutionStrategy()' to execute all the operations in the transaction as a retriable unit.</span></span>

<span data-ttu-id="7f968-180">La solution consiste à appeler manuellement la stratégie d’exécution EF avec un délégué représentant tout ce qui doit être exécuté.</span><span class="sxs-lookup"><span data-stu-id="7f968-180">The solution is to manually invoke the EF execution strategy with a delegate representing everything that needs to be executed.</span></span> <span data-ttu-id="7f968-181">Si une défaillance passagère se produit, la stratégie d’exécution appelle à nouveau le délégué.</span><span class="sxs-lookup"><span data-stu-id="7f968-181">If a transient failure occurs, the execution strategy will invoke the delegate again.</span></span> <span data-ttu-id="7f968-182">Le code suivant montre comment implémenter cette approche :</span><span class="sxs-lookup"><span data-stu-id="7f968-182">The following code shows how to implement this approach:</span></span>

```csharp
// Use of an EF Core resiliency strategy when using multiple DbContexts
// within an explicit transaction
// See:
// https://docs.microsoft.com/ef/core/miscellaneous/connection-resiliency
var strategy = _catalogContext.Database.CreateExecutionStrategy(); 
await strategy.ExecuteAsync(async () =>
{
    // Achieving atomicity between original Catalog database operation and the
    // IntegrationEventLog thanks to a local transaction
    using (var transaction = _catalogContext.Database.BeginTransaction())
    {
        _catalogContext.CatalogItems.Update(catalogItem);
        await _catalogContext.SaveChangesAsync();
        
        // Save to EventLog only if product price changed
        if (raiseProductPriceChangedEvent)
        await _integrationEventLogService.SaveEventAsync(priceChangedEvent);
        transaction.Commit();
    }
});
```

<span data-ttu-id="7f968-183">Le premier DbContext est le \_catalogContext et le second DbContext se trouve dans l’objet \_integrationEventLogService.</span><span class="sxs-lookup"><span data-stu-id="7f968-183">The first DbContext is the \_catalogContext and the second DbContext is within the \_integrationEventLogService object.</span></span> <span data-ttu-id="7f968-184">Pour finir, l’action de validation serait effectuée avec plusieurs DbContexts et avec une stratégie d’exécution EF.</span><span class="sxs-lookup"><span data-stu-id="7f968-184">Finally, the Commit action would be performed multiple DbContexts and using an EF Execution Strategy.</span></span>

> ### <a name="references--entity-framework-core"></a><span data-ttu-id="7f968-185">Références : Entity Framework Core</span><span class="sxs-lookup"><span data-stu-id="7f968-185">References – Entity Framework Core</span></span>
> - <span data-ttu-id="7f968-186">**Documentation EF Core**</span><span class="sxs-lookup"><span data-stu-id="7f968-186">**EF Core Docs**</span></span>  
> <https://docs.microsoft.com/ef/>
> - <span data-ttu-id="7f968-187">**EF Core : Données associées**</span><span class="sxs-lookup"><span data-stu-id="7f968-187">**EF Core: Related Data**</span></span>  
> <https://docs.microsoft.com/ef/core/querying/related-data>
> - <span data-ttu-id="7f968-188">**Éviter le chargement différé des entités dans les applications ASPNET**</span><span class="sxs-lookup"><span data-stu-id="7f968-188">**Avoid Lazy Loading Entities in ASPNET Applications**</span></span>  
> <https://ardalis.com/avoid-lazy-loading-entities-in-asp-net-applications>

## <a name="ef-core-or-micro-orm"></a><span data-ttu-id="7f968-189">EF Core ou micro-ORM ?</span><span class="sxs-lookup"><span data-stu-id="7f968-189">EF Core or micro-ORM?</span></span>

<span data-ttu-id="7f968-190">Bien qu’EF Core soit un bon choix pour la gestion de la persistance, et que dans la plupart des cas il encapsule les détails de la base de données des développeurs d’applications, ce n’est pas le seul choix possible.</span><span class="sxs-lookup"><span data-stu-id="7f968-190">While EF Core is a great choice for managing persistence, and for the most part encapsulates database details from application developers, it is not the only choice.</span></span> <span data-ttu-id="7f968-191">Une alternative open source populaire est [Dapper](https://github.com/StackExchange/Dapper), qui est ce que l’on appelle un micro-ORM.</span><span class="sxs-lookup"><span data-stu-id="7f968-191">Another popular open source alternative is [Dapper](https://github.com/StackExchange/Dapper), a so-called micro-ORM.</span></span> <span data-ttu-id="7f968-192">Un micro-ORM est un outil allégé, avec moins de fonctionnalités, qui permet de mapper des objets à des structures de données.</span><span class="sxs-lookup"><span data-stu-id="7f968-192">A micro-ORM is a lightweight, less full-featured tool for mapping objects to data structures.</span></span> <span data-ttu-id="7f968-193">Dans le cas de Dapper, ses objectifs de conception sont axés sur les performances, plutôt que sur l’encapsulation entière des requêtes sous-jacentes qu’il utilise afin de récupérer et de mettre à jour des données.</span><span class="sxs-lookup"><span data-stu-id="7f968-193">In the case of Dapper, its design goals focus on performance, rather than fully encapsulating the underlying queries it uses to retrieve and update data.</span></span> <span data-ttu-id="7f968-194">Comme il n’effectue pas d’abstraction de SQL par rapport au développeur, Dapper est « au plus proche du métal » et permet aux développeurs d’écrire les requêtes exactes qu’ils souhaitent utiliser pour une opération d’accès aux données spécifique.</span><span class="sxs-lookup"><span data-stu-id="7f968-194">Because it doesn't abstract SQL from the developer, Dapper is "closer to the metal" and lets developers write the exact queries they want to use for a given data access operation.</span></span>

<span data-ttu-id="7f968-195">EF Core offre deux fonctionnalités importantes qui le distinguent de Dapper, mais qui ajoutent également à sa surcharge de performances.</span><span class="sxs-lookup"><span data-stu-id="7f968-195">EF Core has two significant features it provides which separate it from Dapper but also add to its performance overhead.</span></span> <span data-ttu-id="7f968-196">La première est la conversion des expressions LINQ en SQL.</span><span class="sxs-lookup"><span data-stu-id="7f968-196">The first is translation from LINQ expressions into SQL.</span></span> <span data-ttu-id="7f968-197">Ces conversions sont mises en cache, mais leur exécution initiale implique tout de même une surcharge.</span><span class="sxs-lookup"><span data-stu-id="7f968-197">These translations are cached, but even so there is overhead in performing them the first time.</span></span> <span data-ttu-id="7f968-198">La deuxième est le suivi des modifications sur les entités (afin que des instructions de mise à jour efficaces puissent être générées).</span><span class="sxs-lookup"><span data-stu-id="7f968-198">The second is change tracking on entities (so that efficient update statements can be generated).</span></span> <span data-ttu-id="7f968-199">Ce comportement peut être désactivé pour des requêtes spécifiques à l’aide de l’extension AsNotTracking.</span><span class="sxs-lookup"><span data-stu-id="7f968-199">This behavior can be turned off for specific queries by using the AsNotTracking extension.</span></span> <span data-ttu-id="7f968-200">EF Core génère aussi des requêtes SQL qui sont en général très efficaces et dans tous les cas parfaitement acceptables du point de vue des performances, mais si vous avez besoin d’un contrôle affiné de la requête précise à exécuter, vous pouvez également passer du code SQL personnalisé (ou exécuter une procédure stockée) à l’aide d’EF Core.</span><span class="sxs-lookup"><span data-stu-id="7f968-200">EF Core also generates SQL queries that usually are very efficient and in any case perfectly acceptable from a performance standpoint, but if you need fine control over the precise query to be executed, you can pass in custom SQL (or execute a stored procedure) using EF Core, too.</span></span> <span data-ttu-id="7f968-201">Dans ce cas, les performances de Dapper sont encore supérieures à celles d’EF Core, mais seulement légèrement.</span><span class="sxs-lookup"><span data-stu-id="7f968-201">In this case, Dapper still outperforms EF Core, but only slightly.</span></span> <span data-ttu-id="7f968-202">Julie Lerman présente certaines données de performances dans son article MSDN de mai 2016 intitulé [Dapper, Entity Framework, and Hybrid Apps (Dapper, Entity Framework et applications hybrides)](https://msdn.microsoft.com/magazine/mt703432.aspx).</span><span class="sxs-lookup"><span data-stu-id="7f968-202">Julie Lerman presents some performance data in her May 2016 MSDN article [Dapper, Entity Framework, and Hybrid Apps](https://msdn.microsoft.com/magazine/mt703432.aspx).</span></span> <span data-ttu-id="7f968-203">Vous trouverez des données de point de référence de performances supplémentaires pour diverses méthodes d’accès aux données sur [le site de Dapper](https://github.com/StackExchange/Dapper).</span><span class="sxs-lookup"><span data-stu-id="7f968-203">Additional performance benchmark data for a variety of data access methods can be found on [the Dapper site](https://github.com/StackExchange/Dapper).</span></span>

<span data-ttu-id="7f968-204">Pour comparer les syntaxes de Dapper et d’EF, examinez ces deux versions de la même méthode servant à récupérer une liste d’éléments :</span><span class="sxs-lookup"><span data-stu-id="7f968-204">To see how the syntax for Dapper varies from EF Core, consider these two versions of the same method for retrieving a list of items:</span></span>

```csharp
// EF Core
private readonly CatalogContext _context;
public async Task<IEnumerable<CatalogType>> GetCatalogTypes()
{
    return await _context.CatalogTypes.ToListAsync();
}

// Dapper
private readonly SqlConnection _conn;
public async Task<IEnumerable<CatalogType>> GetCatalogTypesWithDapper()
{
    return await _conn.QueryAsync<CatalogType>("SELECT * FROM CatalogType");
}
```

<span data-ttu-id="7f968-205">Si vous avez besoin de générer des graphiques d’objets plus complexes avec Dapper, vous devez écrire vous-même les requêtes associées (alors que dans EF Core vous devez ajouter un Include).</span><span class="sxs-lookup"><span data-stu-id="7f968-205">If you need to build more complex object graphs with Dapper, you need to write the associated queries yourself (as opposed to adding an Include as you would in EF Core).</span></span> <span data-ttu-id="7f968-206">Ceci est pris en charge par diverses syntaxes, notamment une fonctionnalité appelée Mappage multiple, qui vous permet de mapper des lignes individuelles à plusieurs objets mappés.</span><span class="sxs-lookup"><span data-stu-id="7f968-206">This is supported through a variety of syntaxes, including a feature called Multi Mapping that lets you map individual rows to multiple mapped objects.</span></span> <span data-ttu-id="7f968-207">Par exemple, étant donné une classe Post avec une propriété Owner de type User, l’instruction SQL suivante retourne toutes les données nécessaires :</span><span class="sxs-lookup"><span data-stu-id="7f968-207">For example, given a class Post with a property Owner of type User, the following SQL would return all of the necessary data:</span></span>

```sql
select * from #Posts p
left join #Users u on u.Id = p.OwnerId
Order by p.Id
```

<span data-ttu-id="7f968-208">Chaque ligne retournée inclut des données User et Post.</span><span class="sxs-lookup"><span data-stu-id="7f968-208">Each returned row includes both User and Post data.</span></span> <span data-ttu-id="7f968-209">Puisque les données User doivent être attachées aux données Post par le biais de leur propriété Owner, la fonction suivante est utilisée :</span><span class="sxs-lookup"><span data-stu-id="7f968-209">Since the User data should be attached to the Post data via its Owner property, the following function is used:</span></span>

```csharp
(post, user) => { post.Owner = user; return post; }
```

<span data-ttu-id="7f968-210">Voici le code complet permettant de retourner une collection de publications dont la propriété Owner est renseignée avec les données utilisateur associées :</span><span class="sxs-lookup"><span data-stu-id="7f968-210">The full code listing to return a collection of posts with their Owner property populated with the associated user data would be:</span></span>

```csharp
var sql = @"select * from #Posts p
left join #Users u on u.Id = p.OwnerId
Order by p.Id";
var data = connection.Query<Post, User, Post>(sql,
(post, user) => { post.Owner = user; return post;});
```

<span data-ttu-id="7f968-211">Comme il offre moins d’encapsulation, Dapper exige des développeurs une meilleure connaissance de la façon dont leurs données sont stockées et de la manière de les interroger efficacement. Ils doivent aussi écrire davantage de code pour les récupérer.</span><span class="sxs-lookup"><span data-stu-id="7f968-211">Because it offers less encapsulation, Dapper requires developers know more about how their data is stored, how to query it efficiently, and write more code to fetch it.</span></span> <span data-ttu-id="7f968-212">Quand le modèle change, au lieu de simplement créer une nouvelle migration (une autre fonctionnalité d’EF Core) et/ou de mettre à jour les informations de mappage à un emplacement dans un DbContext, chaque requête affectée doit être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="7f968-212">When the model changes, instead of simply creating a new migration (another EF Core feature), and/or updating mapping information in one place in a DbContext, every query that is impacted must be updated.</span></span> <span data-ttu-id="7f968-213">Ces requêtes n’offrent pas de garantie au moment de la compilation. Elles peuvent donc échouer au moment de l’exécution en réponse à des changements du modèle ou de la base de données, ce qui rend les erreurs plus difficiles à détecter rapidement.</span><span class="sxs-lookup"><span data-stu-id="7f968-213">These queries have not compile time guarantees, so they may break at runtime in response to changes to the model or database, making errors more difficult to detect quickly.</span></span> <span data-ttu-id="7f968-214">En contrepartie, Dapper offre des performances extrêmement élevées en termes de rapidité.</span><span class="sxs-lookup"><span data-stu-id="7f968-214">In exchange for these tradeoffs, Dapper offers extremely fast performance.</span></span>

<span data-ttu-id="7f968-215">Pour la plupart des applications, et pour la plupart des composants de presque toutes les applications, EF Core offre des performances acceptables.</span><span class="sxs-lookup"><span data-stu-id="7f968-215">For most applications, and most parts of almost all applications, EF Core offers acceptable performance.</span></span> <span data-ttu-id="7f968-216">Ainsi, ses avantages en matière de productivité du développeur l’emporteront sans doute sur sa surcharge de performances.</span><span class="sxs-lookup"><span data-stu-id="7f968-216">Thus, its developer productivity benefits are likely to outweigh its performance overhead.</span></span> <span data-ttu-id="7f968-217">Pour les requêtes qui peuvent tirer parti de la mise en cache, il est possible que la requête réelle ne soit que rarement exécutée, ce qui atténue les différences pour les requêtes relativement petites.</span><span class="sxs-lookup"><span data-stu-id="7f968-217">For queries that can benefit from caching, the actual query may only be executed a tiny percentage of the time, making relatively small query performance differences moot.</span></span>

## <a name="sql-or-nosql"></a><span data-ttu-id="7f968-218">SQL ou NoSQL</span><span class="sxs-lookup"><span data-stu-id="7f968-218">SQL or NoSQL</span></span>

<span data-ttu-id="7f968-219">En règle générale, les bases de données relationnelles telles que SQL Server dominent la place de marché pour le stockage des données persistantes, mais elles ne constituent pas l’unique solution possible.</span><span class="sxs-lookup"><span data-stu-id="7f968-219">Traditionally, relational databases like SQL Server have dominated the marketplace for persistent data storage, but they are not the only solution available.</span></span> <span data-ttu-id="7f968-220">Des bases de données NoSQL telles que [MongoDB](https://www.mongodb.com/what-is-mongodb) offrent une approche différente pour le stockage d’objets.</span><span class="sxs-lookup"><span data-stu-id="7f968-220">NoSQL databases like [MongoDB](https://www.mongodb.com/what-is-mongodb) offer a different approach to storing objects.</span></span> <span data-ttu-id="7f968-221">Plutôt que de mapper des objets à des tables et des lignes, une autre option consiste à sérialiser le graphique d’objets entier et à stocker le résultat.</span><span class="sxs-lookup"><span data-stu-id="7f968-221">Rather than mapping objects to tables and rows, another option is to serialize the entire object graph, and store the result.</span></span> <span data-ttu-id="7f968-222">Les avantages de cette approche, du moins initialement, sont la simplicité et les performances.</span><span class="sxs-lookup"><span data-stu-id="7f968-222">The benefits of this approach, at least initially, are simplicity and performance.</span></span> <span data-ttu-id="7f968-223">Il est certainement plus simple de stocker un objet sérialisé unique avec une clé, plutôt que de décomposer l’objet en nombreuses tables avec des relations et de mettre à jour les lignes qui peuvent avoir changé depuis la dernière fois où l’objet a été récupéré à partir de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7f968-223">It's certainly simpler to store a single serialized object with a key than to decompose the object into many tables with relationships and update and rows that may have changed since the object was last retrieved from the database.</span></span> <span data-ttu-id="7f968-224">De même, l’extraction et la désérialisation d’un objet unique à partir d’un magasin basé sur des clés sont généralement beaucoup plus rapides et plus faciles à effectuer que les jointures complexes ou les requêtes de base de données multiples requises pour composer entièrement le même objet à partir d’une base de données relationnelle.</span><span class="sxs-lookup"><span data-stu-id="7f968-224">Likewise, fetching and deserializing a single object from a key-based store is typically much faster and easier than complex joins or multiple database queries required to fully compose the same object from a relational database.</span></span> <span data-ttu-id="7f968-225">L’absence de verrous, de transactions ou de schéma fixe rend également les bases de données NoSQL très adaptées à la mise à l’échelle entre plusieurs ordinateurs, ce qui permet de prendre en charge les jeux de données très volumineux.</span><span class="sxs-lookup"><span data-stu-id="7f968-225">The lack of locks or transactions or a fixed schema also makes NoSQL databases very amenable to scaling across many machines, supporting very large datasets.</span></span>

<span data-ttu-id="7f968-226">En revanche, les bases de données NoSQL (comme elles sont généralement appelées) ont leurs inconvénients.</span><span class="sxs-lookup"><span data-stu-id="7f968-226">On the other hand, NoSQL databases (as they are typically called) have their drawbacks.</span></span> <span data-ttu-id="7f968-227">Les bases de données relationnelles utilisent la normalisation afin d’appliquer la cohérence et éviter la duplication des données.</span><span class="sxs-lookup"><span data-stu-id="7f968-227">Relational databases use normalization to enforce consistency and avoid duplication of data.</span></span> <span data-ttu-id="7f968-228">Cela réduit la taille totale de la base de données et garantit que les mises à jour des données partagées sont disponibles immédiatement dans l’ensemble de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7f968-228">This reduces the total size of the database and ensures that updates to shared data are available immediately throughout the database.</span></span> <span data-ttu-id="7f968-229">Dans une base de données relationnelle, une table Adresse peut référencer une table Pays par ID, de telle manière que si le nom d’un pays est modifié, les enregistrements d’adresses tireront parti de la mise à jour sans avoir à être eux-mêmes mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7f968-229">In a relational database, an Address table might reference a Country table by ID, such that if a country's name were changed, the address records would benefit from the update without themselves having to be updated.</span></span> <span data-ttu-id="7f968-230">Toutefois, dans une base de données NoSQL, Adresse et son Pays associé peuvent être sérialisées dans le cadre de nombreux objets stockés.</span><span class="sxs-lookup"><span data-stu-id="7f968-230">However, in a NoSQL database, Address and its associated Country might be serialized as part of many stored objects.</span></span> <span data-ttu-id="7f968-231">La mise à jour du nom d’un pays nécessiterait la mise à jour de tous ces objets, plutôt que celle d’une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="7f968-231">An update to a country name would require all such objects to be updated, rather than a single row.</span></span> <span data-ttu-id="7f968-232">Les bases de données relationnelles peuvent également garantir l’intégrité relationnelle en appliquant des règles comme des clés étrangères.</span><span class="sxs-lookup"><span data-stu-id="7f968-232">Relational databases can also ensure relational integrity by enforcing rules like foreign keys.</span></span> <span data-ttu-id="7f968-233">Les bases de données NoSQL n’offrent généralement pas ces contraintes sur leurs données.</span><span class="sxs-lookup"><span data-stu-id="7f968-233">NoSQL databases typically do not offer such constraints on their data.</span></span>

<span data-ttu-id="7f968-234">Une autre complexité que les bases de données NoSQL doivent gérer est le contrôle de version.</span><span class="sxs-lookup"><span data-stu-id="7f968-234">Another complexity NoSQL databases must deal with is versioning.</span></span> <span data-ttu-id="7f968-235">Quand les propriétés d’un objet changent, il se peut qu’il soit impossible de le désérialiser à partir des versions antérieures qui ont été stockées.</span><span class="sxs-lookup"><span data-stu-id="7f968-235">When an object's properties change, it may not be able to be deserialized from past versions that were stored.</span></span> <span data-ttu-id="7f968-236">Par conséquent, tous les objets existants qui ont une version sérialisée (précédente) de l’objet doivent être mis à jour pour être conformes à son nouveau schéma.</span><span class="sxs-lookup"><span data-stu-id="7f968-236">Thus, all existing objects that have a serialized (previous) version of the object must be updated to conform to its new schema.</span></span> <span data-ttu-id="7f968-237">Sur le plan conceptuel, ceci ne diffère pas d’une base de données relationnelle, où les modifications de schéma nécessitent parfois des scripts de mise à jour ou des mises à jour du mappage.</span><span class="sxs-lookup"><span data-stu-id="7f968-237">This is not conceptually different from a relational database, where schema changes sometimes require update scripts or mapping updates.</span></span> <span data-ttu-id="7f968-238">Toutefois, le nombre d’entrées qui doivent être modifiées est souvent beaucoup plus élevé avec l’approche NoSQL, car il y a plus de duplication de données.</span><span class="sxs-lookup"><span data-stu-id="7f968-238">However, the number of entries that must be modified is often much greater in the NoSQL approach, because there is more duplication of data.</span></span>

<span data-ttu-id="7f968-239">Il est possible dans les bases de données NoSQL de stocker plusieurs versions d’objets, ce qui n’est en général pas pris en charge par les bases de données relationnelles à schéma fixe.</span><span class="sxs-lookup"><span data-stu-id="7f968-239">It's possible in NoSQL databases to store multiple versions of objects, something fixed schema relational databases typically do not support.</span></span> <span data-ttu-id="7f968-240">Toutefois, dans ce cas votre code d’application devra prendre en compte l’existence de versions d’objets précédentes, ce qui augmentera la complexité.</span><span class="sxs-lookup"><span data-stu-id="7f968-240">However, in this case your application code will need to account for the existence of previous versions of objects, adding additional complexity.</span></span>

<span data-ttu-id="7f968-241">Les bases de données NoSQL n’appliquent généralement pas [ACID](https://en.wikipedia.org/wiki/ACID), ce qui signifie qu’elles présentent des avantages en termes de performances et de scalabilité par rapport aux bases de données relationnelles.</span><span class="sxs-lookup"><span data-stu-id="7f968-241">NoSQL databases typically do not enforce [ACID](https://en.wikipedia.org/wiki/ACID), which means they have both performance and scalability benefits over relational databases.</span></span> <span data-ttu-id="7f968-242">Elles conviennent bien aux jeux de données très volumineux et aux objets qui ne sont pas adaptés au stockage dans des structures de tables normalisées.</span><span class="sxs-lookup"><span data-stu-id="7f968-242">They're well-suited to extremely large datasets and objects that are not well-suited to storage in normalized table structures.</span></span> <span data-ttu-id="7f968-243">Rien n’empêche une application de tirer parti à la fois des bases de données relationnelles et NoSQL, en utilisant chacune là où c’est préférable.</span><span class="sxs-lookup"><span data-stu-id="7f968-243">There is no reason why a single application cannot take advantage of both relational and NoSQL databases, using each where it is best suited.</span></span>

## <a name="azure-documentdb"></a><span data-ttu-id="7f968-244">Azure DocumentDB</span><span class="sxs-lookup"><span data-stu-id="7f968-244">Azure DocumentDB</span></span>

<span data-ttu-id="7f968-245">Azure DocumentDB est un service de base de données NoSQL entièrement géré qui propose un stockage des données dans le cloud sans schéma.</span><span class="sxs-lookup"><span data-stu-id="7f968-245">Azure DocumentDB is a fully managed NoSQL database service that offers cloud-based schema-free data storage.</span></span> <span data-ttu-id="7f968-246">DocumentDB est conçu pour offrir des performances rapides et prévisibles, une haute disponibilité, une mise à l’échelle élastique et une distribution globale.</span><span class="sxs-lookup"><span data-stu-id="7f968-246">DocumentDB is built for fast and predictable performance, high availability, elastic scaling, and global distribution.</span></span> <span data-ttu-id="7f968-247">Même s’il s’agit d’une base de données NoSQL, les développeurs peuvent utiliser des fonctionnalités de requête SQL riches et familières sur des données JSON.</span><span class="sxs-lookup"><span data-stu-id="7f968-247">Despite being a NoSQL database, developers can use rich and familiar SQL query capabilities on JSON data.</span></span> <span data-ttu-id="7f968-248">Toutes les ressources DocumentDB sont stockées sous forme de documents JSON.</span><span class="sxs-lookup"><span data-stu-id="7f968-248">All resources in DocumentDB are stored as JSON documents.</span></span> <span data-ttu-id="7f968-249">Elles sont gérées en tant qu’*éléments*, qui sont des documents contenant des métadonnées, et en tant que *flux*, qui sont des collections d’éléments.</span><span class="sxs-lookup"><span data-stu-id="7f968-249">Resources are managed as *items*, which are documents containing metadata, and *feeds*, which are collections of items.</span></span> <span data-ttu-id="7f968-250">La Figure 8-2 montre la relation entre différentes ressources DocumentDB.</span><span class="sxs-lookup"><span data-stu-id="7f968-250">Figure 8-2 shows the relationship between different DocumentDB resources.</span></span>


![La relation hiérarchique entre les ressources dans DocumentDB, une base de données JSON NoSQL](./media/image8-2.png)

<span data-ttu-id="7f968-252">**Figure 8-2.**</span><span class="sxs-lookup"><span data-stu-id="7f968-252">**Figure 8-2.**</span></span> <span data-ttu-id="7f968-253">Organisation des ressources DocumentDB.</span><span class="sxs-lookup"><span data-stu-id="7f968-253">DocumentDB resource organization.</span></span>

<span data-ttu-id="7f968-254">Le langage de requête DocumentDB est une interface simple et puissante permettant d’interroger des documents JSON.</span><span class="sxs-lookup"><span data-stu-id="7f968-254">The DocumentDB query language is a simple yet powerful interface for querying JSON documents.</span></span> <span data-ttu-id="7f968-255">Il prend en charge un sous-ensemble de la grammaire ANSI SQL et ajoute l’intégration étroite de l’appel de fonction, de la construction d’objet, des tableaux et des objets JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7f968-255">The language supports a subset of ANSI SQL grammar and adds deep integration of JavaScript object, arrays, object construction, and function invocation.</span></span>

<span data-ttu-id="7f968-256">**Références : DocumentDB**</span><span class="sxs-lookup"><span data-stu-id="7f968-256">**References – DocumentDB**</span></span>

-   <span data-ttu-id="7f968-257">Introduction à DocumentDB</span><span class="sxs-lookup"><span data-stu-id="7f968-257">DocumentDB Introduction\\</span></span>
    <https://docs.microsoft.com/azure/documentdb/documentdb-introduction>

## <a name="other-persistence-options"></a><span data-ttu-id="7f968-258">Autres options de persistance</span><span class="sxs-lookup"><span data-stu-id="7f968-258">Other Persistence Options</span></span>

<span data-ttu-id="7f968-259">Outre les options de stockage NoSQL et relationnel, les applications ASP.NET Core peuvent utiliser Stockage Azure pour stocker différents formats de données et fichiers de façon scalable et basée sur le cloud.</span><span class="sxs-lookup"><span data-stu-id="7f968-259">In addition to relational and NoSQL storage options, ASP.NET Core applications can use Azure Storage to store a variety of data formats and files in a cloud-based, scalable fashion.</span></span> <span data-ttu-id="7f968-260">Stockage Azure étant extrêmement scalable, vous pouvez commencer par stocker de petites quantités de données, puis monter en charge et stocker jusqu’à des téraoctets de données si votre application l’exige.</span><span class="sxs-lookup"><span data-stu-id="7f968-260">Azure Storage is massively scalable, so you can start out storing small amounts of data and scale up to storing hundreds or terabytes if your application requires it.</span></span> <span data-ttu-id="7f968-261">Stockage Azure prend en charge quatre genres de données :</span><span class="sxs-lookup"><span data-stu-id="7f968-261">Azure Storage supports four kinds of data:</span></span>

-   <span data-ttu-id="7f968-262">Stockage Blob pour le stockage binaire ou de texte non structuré, également appelé stockage d’objets.</span><span class="sxs-lookup"><span data-stu-id="7f968-262">Blob Storage for unstructured text or binary storage, also referred to as object storage.</span></span>

-   <span data-ttu-id="7f968-263">Stockage Table pour les jeux de données structurés, accessibles par le biais de clés de lignes.</span><span class="sxs-lookup"><span data-stu-id="7f968-263">Table Storage for structured datasets, accessible via row keys.</span></span>

-   <span data-ttu-id="7f968-264">Stockage File d’attente pour la messagerie fiable basée sur les files d’attente.</span><span class="sxs-lookup"><span data-stu-id="7f968-264">Queue Storage for reliable queue-based messaging.</span></span>

-   <span data-ttu-id="7f968-265">Stockage Fichier pour l’accès aux fichiers partagé entre les machines virtuelles Azure et les applications locales.</span><span class="sxs-lookup"><span data-stu-id="7f968-265">File Storage for shared file access between Azure virtual machines and on-premises applications.</span></span>

<span data-ttu-id="7f968-266">**Références : Stockage Azure**</span><span class="sxs-lookup"><span data-stu-id="7f968-266">**References – Azure Storage**</span></span>

-   <span data-ttu-id="7f968-267">Introduction au Stockage Azure</span><span class="sxs-lookup"><span data-stu-id="7f968-267">Azure Storage Introduction\\</span></span>
    <https://docs.microsoft.com/azure/storage/storage-introduction>

## <a name="caching"></a><span data-ttu-id="7f968-268">Mise en cache</span><span class="sxs-lookup"><span data-stu-id="7f968-268">Caching</span></span>

<span data-ttu-id="7f968-269">Dans les applications web, chaque requête web doit se terminer dans les plus brefs délais.</span><span class="sxs-lookup"><span data-stu-id="7f968-269">In web applications, each web request should be completed in the shortest time possible.</span></span> <span data-ttu-id="7f968-270">L’une des manières de satisfaire à cette exigence consiste à limiter le nombre d’appels externes que le serveur doit effectuer pour terminer la requête.</span><span class="sxs-lookup"><span data-stu-id="7f968-270">One way to achieve this is to limit the number of external calls the server must make to complete the request.</span></span> <span data-ttu-id="7f968-271">La mise en cache implique de stocker une copie des données sur le serveur (ou un autre magasin de données plus facilement interrogeable que la source de données).</span><span class="sxs-lookup"><span data-stu-id="7f968-271">Caching involves storing a copy of data on the server (or another data store that is more easily queried than the source of the data).</span></span> <span data-ttu-id="7f968-272">Les applications web, et en particulier les applications web traditionnelles non-monopages, doivent générer l’interface utilisateur entière lors de chaque requête.</span><span class="sxs-lookup"><span data-stu-id="7f968-272">Web applications, and especially non-SPA traditional web applications, need to build the entire user interface with every request.</span></span> <span data-ttu-id="7f968-273">Cela implique souvent d’effectuer nombre des mêmes requêtes de base de données de manière répétée lors de chaque requête utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7f968-273">This frequently involves making many of the same database queries repeatedly from one user request to the next.</span></span> <span data-ttu-id="7f968-274">Dans la plupart des cas, ces données changent rarement ; il y a donc peu de raisons de les demander en permanence à la base de données.</span><span class="sxs-lookup"><span data-stu-id="7f968-274">In most cases, this data changes rarely, so there is little reason to constantly request it from the database.</span></span> <span data-ttu-id="7f968-275">ASP.NET Core prend en charge la mise en cache des réponses, pour la mise en cache de pages entières, et la mise en cache des données, qui prend en charge un comportement de mise en cache plus granulaire.</span><span class="sxs-lookup"><span data-stu-id="7f968-275">ASP.NET Core supports response caching, for caching entire pages, and data caching, which supports more granular caching behavior.</span></span>

<span data-ttu-id="7f968-276">Lors de l’implémentation de la mise en cache, il est important de garder à l’esprit la séparation des fonctions.</span><span class="sxs-lookup"><span data-stu-id="7f968-276">When implementing caching, it's important to keep in mind separation of concerns.</span></span> <span data-ttu-id="7f968-277">Évitez d’implémenter la logique de mise en cache dans votre logique d’accès aux données ou dans votre interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7f968-277">Avoid implementing caching logic in your data access logic, or in your user interface.</span></span> <span data-ttu-id="7f968-278">Au lieu de cela, encapsulez la mise en cache dans ses propres classes, et utilisez la configuration pour gérer son comportement.</span><span class="sxs-lookup"><span data-stu-id="7f968-278">Instead, encapsulate caching in its own classes, and use configuration to manage its behavior.</span></span> <span data-ttu-id="7f968-279">Cela permet de respecter le principe de responsabilité unique et le principe ouvert/fermé, et il vous sera plus facile de gérer la façon dont vous utilisez la mise en cache dans votre application à mesure qu’elle évolue.</span><span class="sxs-lookup"><span data-stu-id="7f968-279">This follows the Open/Closed and Single Responsibility principles, and will make it easier for you to manage how you use caching in your application as it grows.</span></span>

### <a name="aspnet-core-response-caching"></a><span data-ttu-id="7f968-280">Mise en cache des réponses dans ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="7f968-280">ASP.NET Core Response Caching</span></span>

<span data-ttu-id="7f968-281">ASP.NET Core prend en charge deux niveaux de mise en cache des réponses.</span><span class="sxs-lookup"><span data-stu-id="7f968-281">ASP.NET Core supports two levels of response caching.</span></span> <span data-ttu-id="7f968-282">Le premier niveau ne met rien en cache sur le serveur, mais ajoute des en-têtes HTTP qui demandent aux clients et aux serveurs proxy de mettre en cache les réponses.</span><span class="sxs-lookup"><span data-stu-id="7f968-282">The first level does not cache anything on the server, but adds HTTP headers that instruct clients and proxy servers to cache responses.</span></span> <span data-ttu-id="7f968-283">Ceci est implémenté en ajoutant l’attribut ResponseCache à des contrôleurs ou des actions spécifiques :</span><span class="sxs-lookup"><span data-stu-id="7f968-283">This is implemented by adding the ResponseCache attribute to individual controllers or actions:</span></span>

```csharp
    [ResponseCache(Duration = 60)]
    public IActionResult Contact()
    { }
    
    ViewData["Message"] = "Your contact page.";
    return View();
}

The above example will result in the following header being added to the response, instructing clients to cache the result for up to 60 seconds.

Cache-Control: public,max-age=60

In order to add server-side in-memory caching to the application, you must reference the Microsoft.AspNetCore.ResponseCaching NuGet package, and then add the Response Caching middleware. This middleware is configured in both ConfigureServices and Configure in Startup:

```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddResponseCaching();
}

public void Configure(IApplicationBuilder app)
{
    app.UseResponseCaching();
}
```

<span data-ttu-id="7f968-284">L’intergiciel (middleware) de mise en cache des réponses mettra automatiquement en cache les réponses conformément à un ensemble de conditions, que vous pouvez personnaliser.</span><span class="sxs-lookup"><span data-stu-id="7f968-284">The Response Caching Middleware will automatically cache responses based on a set of conditions, which you can customize.</span></span> <span data-ttu-id="7f968-285">Par défaut, seules 200 réponses (OK) demandées par le biais des méthodes GET ou HEAD sont mises en cache.</span><span class="sxs-lookup"><span data-stu-id="7f968-285">By default, only 200 (OK) responses requested via GET or HEAD methods are cached.</span></span> <span data-ttu-id="7f968-286">En outre, les requêtes doivent avoir une réponse avec un en-tête Cache-Control: public et ne peuvent pas inclure des en-têtes pour Authorization ou Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="7f968-286">In addition, requests must have a response with a Cache-Control: public header, and cannot include headers for Authorization or Set-Cookie.</span></span> <span data-ttu-id="7f968-287">Consultez la [liste complète des conditions de mise en cache utilisées par l’intergiciel (middleware) de mise en cache des réponses](https://docs.microsoft.com/aspnet/core/performance/caching/middleware#conditions-for-caching).</span><span class="sxs-lookup"><span data-stu-id="7f968-287">See a [complete list of the caching conditions used by the response caching middleware](https://docs.microsoft.com/aspnet/core/performance/caching/middleware#conditions-for-caching).</span></span>

### <a name="data-caching"></a><span data-ttu-id="7f968-288">Mise en cache des données</span><span class="sxs-lookup"><span data-stu-id="7f968-288">Data Caching</span></span>

<span data-ttu-id="7f968-289">Au lieu (ou en plus) de mettre en cache des réponses web complètes, vous pouvez mettre en cache les résultats de requêtes de données individuelles.</span><span class="sxs-lookup"><span data-stu-id="7f968-289">Rather than (or in addition to) caching full web responses, you can cache the results of individual data queries.</span></span> <span data-ttu-id="7f968-290">Pour ce faire, vous pouvez utiliser la mise en cache en mémoire sur le serveur web, ou utiliser [un cache distribué](https://docs.microsoft.com/aspnet/core/performance/caching/distributed).</span><span class="sxs-lookup"><span data-stu-id="7f968-290">For this, you can use in memory caching on the web server, or use [a distributed cache](https://docs.microsoft.com/aspnet/core/performance/caching/distributed).</span></span> <span data-ttu-id="7f968-291">Cette section illustre comment implémenter la mise en cache en mémoire.</span><span class="sxs-lookup"><span data-stu-id="7f968-291">This section will demonstrate how to implement in memory caching.</span></span>

<span data-ttu-id="7f968-292">Vous ajoutez la prise en charge de la mise en cache en mémoire (ou distribuée) dans ConfigureServices :</span><span class="sxs-lookup"><span data-stu-id="7f968-292">You add support for memory (or distributed) caching in ConfigureServices:</span></span>

```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddMemoryCache();
    services.AddMvc();
}
```

<span data-ttu-id="7f968-293">N’oubliez pas d’ajouter aussi le package NuGet Microsoft.Extensions.Caching.Memory.</span><span class="sxs-lookup"><span data-stu-id="7f968-293">Be sure to add the Microsoft.Extensions.Caching.Memory NuGet package as well.</span></span>

<span data-ttu-id="7f968-294">Une fois que vous avez ajouté le service, vous demandez IMemoryCache par le biais de l’injection de dépendances partout où vous avez besoin d’accéder au cache.</span><span class="sxs-lookup"><span data-stu-id="7f968-294">Once you've added the service, you request IMemoryCache via dependency injection wherever you need to access the cache.</span></span> <span data-ttu-id="7f968-295">Dans cet exemple, le CachedCatalogService utilise le modèle de conception Proxy (ou Decorator), en fournissant une autre implémentation d’ICatalogService qui contrôle l’accès à l’implémentation sous-jacente de CatalogService (ou y ajoute un comportement).</span><span class="sxs-lookup"><span data-stu-id="7f968-295">In this example, the CachedCatalogService is using the Proxy (or Decorator) design pattern, by providing an alternative implementation of ICatalogService that controls access to (or adds behavior to) the underlying CatalogService implementation.</span></span>

```csharp
public class CachedCatalogService : ICatalogService
{
    private readonly IMemoryCache _cache;
    private readonly CatalogService _catalogService;
    private static readonly string _brandsKey = "brands";
    private static readonly string _typesKey = "types";
    private static readonly string _itemsKeyTemplate = "items-{0}-{1}-{2}-{3}";
    private static readonly TimeSpan _defaultCacheDuration = TimeSpan.FromSeconds(30);
    public CachedCatalogService(IMemoryCache cache,
    CatalogService catalogService)
    {
        _cache = cache;
        _catalogService = catalogService;
    }
    
    public async Task<IEnumerable<SelectListItem>> GetBrands()
    {
        return await _cache.GetOrCreateAsync(_brandsKey, async entry =>
        {
            entry.SlidingExpiration = _defaultCacheDuration;
            return await _catalogService.GetBrands();
        });
    }
    
    public async Task<Catalog> GetCatalogItems(int pageIndex, int itemsPage, int? brandID, int? typeId)
    {
        string cacheKey = String.Format(_itemsKeyTemplate, pageIndex, itemsPage, brandID, typeId);
        return await _cache.GetOrCreateAsync(cacheKey, async entry =>
        {
            entry.SlidingExpiration = _defaultCacheDuration;
            return await _catalogService.GetCatalogItems(pageIndex, itemsPage, brandID, typeId);
        });
    }
    
    public async Task<IEnumerable<SelectListItem>> GetTypes()
    {
        return await _cache.GetOrCreateAsync(_typesKey, async entry =>
        {
            entry.SlidingExpiration = _defaultCacheDuration;
            return await _catalogService.GetTypes();
        });
    }
}
```

<span data-ttu-id="7f968-296">Pour configurer l’application afin qu’elle utilise la version mise en cache du service, tout en autorisant le service à obtenir l’instance de CatalogService dont il a besoin dans son constructeur, vous devez ajouter ce qui suit dans ConfigureServices :</span><span class="sxs-lookup"><span data-stu-id="7f968-296">To configure the application to use the cached version of the service, but still allow the service to get the instance of CatalogService it needs in its constructor, you would add the following in ConfigureServices:</span></span>

```csharp
services.AddMemoryCache();
services.AddScoped<ICatalogService, CachedCatalogService>();
services.AddScoped<CatalogService>();
```

<span data-ttu-id="7f968-297">Tout ceci étant en place, les appels de base de données afin d’extraire les données du catalogue ne seront effectués qu’une fois par minute, plutôt qu’à chaque requête.</span><span class="sxs-lookup"><span data-stu-id="7f968-297">With this in place, the database calls to fetch the catalog data will only be made once per minute, rather than on every request.</span></span> <span data-ttu-id="7f968-298">En fonction du trafic vers le site, cela peut avoir un impact considérable sur le nombre de requêtes effectuées sur la base de données et sur la durée moyenne de chargement de la page d’accueil, qui dépend actuellement des trois requêtes exposées par ce service.</span><span class="sxs-lookup"><span data-stu-id="7f968-298">Depending on the traffic to the site, this can have a very significant impact on the number of queries made to the database, and the average page load time for the home page that currently depends on all three of the queries exposed by this service.</span></span>

<span data-ttu-id="7f968-299">Quand la mise en cache est implémentée, un problème apparaît : les *données périmées*. Il s’agit de données qui ont changé à la source, mais dont il reste une version obsolète dans le cache.</span><span class="sxs-lookup"><span data-stu-id="7f968-299">An issue that arises when caching is implemented is *stale data* – that is, data that has changed at the source but an out of date version remains in the cache.</span></span> <span data-ttu-id="7f968-300">Un moyen simple de résoudre ce problème consiste à utiliser de faibles durées de mise en cache, puisque pour une application occupée l’extension de la durée de mise en cache des données offre un avantage supplémentaire limité.</span><span class="sxs-lookup"><span data-stu-id="7f968-300">A simple way to mitigate this issue is to use small cache durations, since for a busy application there is limited additional benefit to extending the length data is cached.</span></span> <span data-ttu-id="7f968-301">Par exemple, prenez une page qui effectue une seule requête de base de données, et qui est demandée 10 fois par seconde.</span><span class="sxs-lookup"><span data-stu-id="7f968-301">For example, consider a page that makes a single database query, and is requested 10 times per second.</span></span> <span data-ttu-id="7f968-302">Si cette page est mise en cache pendant une minute, le nombre de requêtes de base de données effectuées par minute baissera de 600 à 1, une réduction de 99,8 %.</span><span class="sxs-lookup"><span data-stu-id="7f968-302">If this page is cached for one minute, it will result in the number of database queries made per minute to drop from 600 to 1, a reduction of 99.8%.</span></span> <span data-ttu-id="7f968-303">Si la durée de mise en cache était d’une heure, la réduction globale serait de 99,997 %, mais la probabilité et l’âge potentiel des données périmées augmenteraient tous deux considérablement.</span><span class="sxs-lookup"><span data-stu-id="7f968-303">If instead the cache duration were made one hour, the overall reduction would be 99.997%, but now the likelihood and potential age of stale data are both increased dramatically.</span></span>

<span data-ttu-id="7f968-304">Une autre approche consiste à supprimer de manière proactive les entrées de cache quand les données qu’elles contiennent sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="7f968-304">Another approach is to proactively remove cache entries when the data they contain is updated.</span></span> <span data-ttu-id="7f968-305">Vous pouvez supprimer une entrée si vous connaissez sa clé :</span><span class="sxs-lookup"><span data-stu-id="7f968-305">Any individual entry can be removed if its key is known:</span></span>

```csharp
_cache.Remove(cacheKey);
```

<span data-ttu-id="7f968-306">Si votre application expose une fonctionnalité pour la mise à jour des entrées qu’elle met en cache, vous pouvez supprimer les entrées de cache correspondantes dans votre code qui effectue les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="7f968-306">If your application exposes functionality for updating entries that it caches, you can remove the corresponding cache entries in your code that performs the updates.</span></span> <span data-ttu-id="7f968-307">Il peut parfois y avoir de nombreuses entrées différentes qui dépendent d’un jeu de données particulier.</span><span class="sxs-lookup"><span data-stu-id="7f968-307">Sometimes there may be many different entries that depend on a particular set of data.</span></span> <span data-ttu-id="7f968-308">Dans ce cas, il peut être utile de créer des dépendances entre les entrées du cache, à l’aide d’un CancellationChangeToken.</span><span class="sxs-lookup"><span data-stu-id="7f968-308">In that case, it can be useful to create dependencies between cache entries, by using a CancellationChangeToken.</span></span> <span data-ttu-id="7f968-309">Avec un CancellationChangeToken, vous pouvez faire expirer plusieurs entrées de cache à la fois en annulant le jeton.</span><span class="sxs-lookup"><span data-stu-id="7f968-309">With a CancellationChangeToken, you can expire multiple cache entries at once by cancelling the token.</span></span>

```csharp
// configure CancellationToken and add entry to cache
var cts = new CancellationTokenSource();
_cache.Set("cts", cts);
_cache.Set(cacheKey,
itemToCache,
new CancellationChangeToken(cts.Token));

// elsewhere, expire the cache by cancelling the token\
_cache.Get<CancellationTokenSource>("cts").Cancel();
```

>[!div class="step-by-step"]
<span data-ttu-id="7f968-310">[Précédent] (develop-asp-net-core-mvc-apps.md) [Next] (test-asp-net-core-mvc-apps.md)</span><span class="sxs-lookup"><span data-stu-id="7f968-310">[Previous] (develop-asp-net-core-mvc-apps.md) [Next] (test-asp-net-core-mvc-apps.md)</span></span>
