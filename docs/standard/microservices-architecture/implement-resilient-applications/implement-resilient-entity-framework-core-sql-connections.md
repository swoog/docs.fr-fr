---
title: Implémenter des connexions SQL à Entity Framework Core résilientes
description: Architecture des microservices .NET pour les applications .NET en conteneur | Implémenter des connexions SQL à Entity Framework Core résilientes Cette technique est particulièrement importante lors de l’utilisation d’Azure SQL Database dans le cloud.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 06/08/2018
ms.openlocfilehash: 59db9cdb894f76f54e77732be47dc6140a594121
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46561511"
---
# <a name="implement-resilient-entity-framework-core-sql-connections"></a>Implémenter des connexions SQL à Entity Framework Core résilientes

Pour Azure SQL DB, Entity Framework Core fournit déjà la logique de résilience et de nouvelle tentative de connexion de base de données interne. Par contre, vous devez autoriser la stratégie d’exécution d’Entity Framework pour chaque connexion DbContext si vous voulez avoir des [connexions EF Core résilientes](https://docs.microsoft.com/ef/core/miscellaneous/connection-resiliency).

Par exemple, le code suivant au niveau des connexions EF Core autorise les connexions SQL résilientes qui sont retentées si elles échouent.

```csharp
// Startup.cs from any ASP.NET Core Web API
public class Startup
{
    // Other code ...
    public IServiceProvider ConfigureServices(IServiceCollection services)
    {
        // ...
        services.AddDbContext<CatalogContext>(options =>
        {
            options.UseSqlServer(Configuration["ConnectionString"],
            sqlServerOptionsAction: sqlOptions =>
            {
                sqlOptions.EnableRetryOnFailure(
                maxRetryCount: 10,
                maxRetryDelay: TimeSpan.FromSeconds(30),
                errorNumbersToAdd: null);
            });
        });
    }
//...
}
```

## <a name="execution-strategies-and-explicit-transactions-using-begintransaction-and-multiple-dbcontexts"></a>Stratégies d’exécution et transactions explicites utilisant BeginTransaction et plusieurs DbContexts

Quand les nouvelles tentatives sont activées dans les connexions EF Core, chaque opération que vous effectuez avec EF Core devient sa propre opération de nouvelle tentative. Chaque requête et chaque appel à SaveChanges sont retentés ensemble si une défaillance passagère se produit.

Toutefois, si votre code lance une transaction à l’aide de BeginTransaction, définissez votre propre groupe d’opérations à traiter ensemble : tout le contenu de la transaction doit être restauré si une défaillance se produit. Une exception semblable à la suivante s’affiche si vous tentez d’exécuter cette transaction quand vous utilisez une stratégie d’exécution EF (stratégie de nouvelle tentative) et que vous incluez plusieurs appels à SaveChanges de plusieurs DbContexts dans la transaction.

> System.InvalidOperationException : La stratégie d’exécution configurée « SqlServerRetryingExecutionStrategy » ne prend pas en charge les transactions lancées par l’utilisateur. Utilisez la stratégie d’exécution retournée par « DbContext.Database.CreateExecutionStrategy() » pour exécuter toutes les opérations de la transaction en tant qu’ensemble pouvant être retenté.

La solution consiste à appeler manuellement la stratégie d’exécution EF avec un délégué représentant tout ce qui doit être exécuté. Si une défaillance passagère se produit, la stratégie d’exécution appelle à nouveau le délégué. Par exemple, le code suivant montre comment elle est implémentée dans eShopOnContainers avec plusieurs DbContexts (\_catalogContext et IntegrationEventLogContext) quand un produit est mis à jour puis que l’objet ProductPriceChangedIntegrationEvent est enregistré, ce qui nécessite d’utiliser un autre DbContext.

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

Le premier DbContext est \_catalogContext et le second DbContext se trouve dans l’objet \_integrationEventLogService. L’action de validation est effectuée entre plusieurs DbContexts utilisant une stratégie d’exécution EF.

## <a name="additional-resources"></a>Ressources supplémentaires

-   **Résilience des connexions EF** (Entity Framework Core) [*https://docs.microsoft.com/ef/core/miscellaneous/connection-resiliency*](https://docs.microsoft.com/ef/core/miscellaneous/connection-resiliency)

-   **Résilience des connexions et interception des commandes avec Entity Framework**
    [*https://docs.microsoft.com/azure/architecture/patterns/category/resiliency*](https://docs.microsoft.com/azure/architecture/patterns/category/resiliency)

-   **Cesar de la Torre. Using Resilient Entity Framework Core Sql Connections and Transactions**
    <https://blogs.msdn.microsoft.com/cesardelatorre/2017/03/26/using-resilient-entity-framework-core-sql-connections-and-transactions-retries-with-exponential-backoff/>

>[!div class="step-by-step"]
[Précédent](implement-retries-exponential-backoff.md)
[Suivant](explore-custom-http-call-retries-exponential-backoff.md)
