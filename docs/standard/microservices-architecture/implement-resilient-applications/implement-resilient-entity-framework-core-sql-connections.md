---
title: Implémentation de connexions SQL à Entity Framework Core résilientes
description: Architecture des microservices .NET pour les applications .NET en conteneur | Implémentation de connexions SQL à Entity Framework Core résilientes
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: 54d0df517514c359c155de35d34e1e0f56eed4eb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="implementing-resilient-entity-framework-core-sql-connections"></a><span data-ttu-id="6488e-103">Implémentation de connexions SQL à Entity Framework Core résilientes</span><span class="sxs-lookup"><span data-stu-id="6488e-103">Implementing resilient Entity Framework Core SQL connections</span></span>

<span data-ttu-id="6488e-104">Pour Azure SQL DB, Entity Framework Core fournit déjà la logique de résilience et de nouvelle tentative de connexion de base de données interne.</span><span class="sxs-lookup"><span data-stu-id="6488e-104">For Azure SQL DB, Entity Framework Core already provides internal database connection resiliency and retry logic.</span></span> <span data-ttu-id="6488e-105">Par contre, vous devez autoriser la stratégie d’exécution d’Entity Framework pour chaque connexion DbContext si vous voulez avoir des [connexions EF Core résilientes](https://docs.microsoft.com/ef/core/miscellaneous/connection-resiliency).</span><span class="sxs-lookup"><span data-stu-id="6488e-105">But you need to enable the Entity Framework execution strategy for each DbContext connection if you want to have [resilient EF Core connections](https://docs.microsoft.com/ef/core/miscellaneous/connection-resiliency).</span></span>

<span data-ttu-id="6488e-106">Par exemple, le code suivant au niveau des connexions EF Core autorise les connexions SQL résilientes qui sont retentées si elles échouent.</span><span class="sxs-lookup"><span data-stu-id="6488e-106">For instance, the following code at the EF Core connection level enables resilient SQL connections that are retried if the connection fails.</span></span>

```csharp
// Startup.cs from any ASP.NET Core Web API
public class Startup
{
    // Other code ...
    public IServiceProvider ConfigureServices(IServiceCollection services)
    {
        // ...
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
}
```

## <a name="execution-strategies-and-explicit-transactions-using-begintransaction-and-multiple-dbcontexts"></a><span data-ttu-id="6488e-107">Stratégies d’exécution et transactions explicites utilisant BeginTransaction et plusieurs DbContexts</span><span class="sxs-lookup"><span data-stu-id="6488e-107">Execution strategies and explicit transactions using BeginTransaction and multiple DbContexts</span></span>

<span data-ttu-id="6488e-108">Quand les nouvelles tentatives sont activées dans les connexions EF Core, chaque opération que vous effectuez avec EF Core devient sa propre opération de nouvelle tentative.</span><span class="sxs-lookup"><span data-stu-id="6488e-108">When retries are enabled in EF Core connections, each operation you perform using EF Core becomes its own retriable operation.</span></span> <span data-ttu-id="6488e-109">Chaque requête et chaque appel à SaveChanges sont retentés ensemble si une défaillance passagère se produit.</span><span class="sxs-lookup"><span data-stu-id="6488e-109">Each query and each call to SaveChanges will be retried as a unit if a transient failure occurs.</span></span>

<span data-ttu-id="6488e-110">Toutefois, si votre code lance une transaction à l’aide de BeginTransaction, définissez votre propre groupe d’opérations à traiter ensemble : tout le contenu de la transaction doit être restauré si une défaillance se produit.</span><span class="sxs-lookup"><span data-stu-id="6488e-110">However, if your code initiates a transaction using BeginTransaction, you are defining your own group of operations that need to be treated as a unit—everything inside the transaction has be rolled back if a failure occurs.</span></span> <span data-ttu-id="6488e-111">Une exception semblable à la suivante s’affiche si vous tentez d’exécuter cette transaction quand vous utilisez une stratégie d’exécution EF (stratégie de nouvelle tentative) et que vous incluez plusieurs appels à SaveChanges de plusieurs DbContexts dans la transaction.</span><span class="sxs-lookup"><span data-stu-id="6488e-111">You will see an exception like the following if you attempt to execute that transaction when using an EF execution strategy (retry policy) and you include several SaveChanges calls from multiple DbContexts in the transaction.</span></span>

> <span data-ttu-id="6488e-112">System.InvalidOperationException : La stratégie d’exécution configurée « SqlServerRetryingExecutionStrategy » ne prend pas en charge les transactions lancées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6488e-112">System.InvalidOperationException: The configured execution strategy 'SqlServerRetryingExecutionStrategy' does not support user initiated transactions.</span></span> <span data-ttu-id="6488e-113">Utilisez la stratégie d’exécution retournée par « DbContext.Database.CreateExecutionStrategy() » pour exécuter toutes les opérations de la transaction en tant qu’ensemble pouvant être retenté.</span><span class="sxs-lookup"><span data-stu-id="6488e-113">Use the execution strategy returned by 'DbContext.Database.CreateExecutionStrategy()' to execute all the operations in the transaction as a retriable unit.</span></span>

<span data-ttu-id="6488e-114">La solution consiste à appeler manuellement la stratégie d’exécution EF avec un délégué représentant tout ce qui doit être exécuté.</span><span class="sxs-lookup"><span data-stu-id="6488e-114">The solution is to manually invoke the EF execution strategy with a delegate representing everything that needs to be executed.</span></span> <span data-ttu-id="6488e-115">Si une défaillance passagère se produit, la stratégie d’exécution appelle à nouveau le délégué.</span><span class="sxs-lookup"><span data-stu-id="6488e-115">If a transient failure occurs, the execution strategy will invoke the delegate again.</span></span> <span data-ttu-id="6488e-116">Par exemple, le code suivant montre comment elle est implémentée dans eShopOnContainers avec plusieurs DbContexts (\_catalogContext et IntegrationEventLogContext) quand un produit est mis à jour puis que l’objet ProductPriceChangedIntegrationEvent est enregistré, ce qui nécessite d’utiliser un autre DbContext.</span><span class="sxs-lookup"><span data-stu-id="6488e-116">For example, the following code show how it is implemented in eShopOnContainers with two multiple DbContexts (\_catalogContext and the IntegrationEventLogContext) when updating a product and then saving the ProductPriceChangedIntegrationEvent object, which needs to use a different DbContext.</span></span>

```csharp
public async Task<IActionResult> UpdateProduct([FromBody]CatalogItem
    productToUpdate)
{
    // Other code ...
    // Update current product
    catalogItem = productToUpdate;

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
}
```

<span data-ttu-id="6488e-117">Le premier DbContext est \_catalogContext et le second DbContext se trouve dans l’objet \_integrationEventLogService.</span><span class="sxs-lookup"><span data-stu-id="6488e-117">The first DbContext is \_catalogContext and the second DbContext is within the \_integrationEventLogService object.</span></span> <span data-ttu-id="6488e-118">L’action de validation est effectuée entre plusieurs DbContexts utilisant une stratégie d’exécution EF.</span><span class="sxs-lookup"><span data-stu-id="6488e-118">The Commit action is performed across multiple DbContexts using an EF execution strategy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6488e-119">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="6488e-119">Additional resources</span></span>

-   <span data-ttu-id="6488e-120">**Résilience des connexions et interception des commandes avec Entity Framework**
    [*https://docs.microsoft.com/azure/architecture/patterns/category/resiliency*](https://docs.microsoft.com/azure/architecture/patterns/category/resiliency)</span><span class="sxs-lookup"><span data-stu-id="6488e-120">**Connection Resiliency and Command Interception with the Entity Framework**
[*https://docs.microsoft.com/azure/architecture/patterns/category/resiliency*](https://docs.microsoft.com/azure/architecture/patterns/category/resiliency)</span></span>

-   <span data-ttu-id="6488e-121">**Cesar de la Torre. Using Resilient Entity Framework Core Sql Connections and Transactions**
    <https://blogs.msdn.microsoft.com/cesardelatorre/2017/03/26/using-resilient-entity-framework-core-sql-connections-and-transactions-retries-with-exponential-backoff/></span><span class="sxs-lookup"><span data-stu-id="6488e-121">**Cesar de la Torre. Using Resilient Entity Framework Core Sql Connections and Transactions**
<https://blogs.msdn.microsoft.com/cesardelatorre/2017/03/26/using-resilient-entity-framework-core-sql-connections-and-transactions-retries-with-exponential-backoff/></span></span>


>[!div class="step-by-step"]
<span data-ttu-id="6488e-122">[Précédent] (implement-retries-exponential-backoff.md) [Suivant] (implement-custom-http-call-retries-exponential-backoff.md)</span><span class="sxs-lookup"><span data-stu-id="6488e-122">[Previous] (implement-retries-exponential-backoff.md) [Next] (implement-custom-http-call-retries-exponential-backoff.md)</span></span>
