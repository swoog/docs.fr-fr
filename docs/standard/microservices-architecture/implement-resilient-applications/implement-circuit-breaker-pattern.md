---
title: "Implémentation du modèle Disjoncteur"
description: "Architecture des microservices .NET pour les applications .NET en conteneur | Implémentation du modèle Disjoncteur"
keywords: Docker, microservices, ASP.NET, conteneur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/12/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 5d7db6899068f84f9165022cfbf17767a75e7db9
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="implementing-the-circuit-breaker-pattern"></a>Implémentation du modèle Disjoncteur

Comme indiqué précédemment, vous devez gérer des erreurs dont le temps de récupération peut être variable, comme ça peut être le cas quand vous essayez de vous connecter à une ressource ou à un service distant. La gestion de ce type d’erreur peut améliorer la stabilité et la résilience d’une application.

Dans un environnement distribué, les appels à des ressources et services distants peuvent échouer en raison d’erreurs temporaires, telles que des connexions réseau lentes, l’expiration de délais d’attente, ou si des ressources sont lentes ou temporairement indisponibles. En général, ces erreurs se corrigent d’elles-mêmes après un bref laps de temps, et une application cloud fiable doit être prête à les gérer à l’aide d’une stratégie comme le modèle Nouvelle tentative.

Toutefois, dans certaines situations, les erreurs sont dues à des événements imprévus dont la correction peut prendre beaucoup plus de temps. La gravité de ces erreurs peut aller d’une perte partielle de connectivité à la défaillance complète d’un service. Dans ces cas de figure, il peut être inutile qu’une application effectue de nouvelles tentatives dont la réussite sera peu probable. L’application doit plutôt être codée pour reconnaître que l’opération a échoué et gérer l’échec en conséquence.

L’objectif du modèle Disjoncteur est différent de celui du modèle Nouvelle tentative. Le modèle Nouvelle tentative permet à une application de retenter une opération en partant du principe qu’elle finira par réussir. Le modèle Disjoncteur empêche une application d’effectuer une opération qui échouera probablement. Une application peut combiner ces deux modèles en utilisant le modèle Nouvelle tentative pour appeler une opération par le biais d’un disjoncteur. Toutefois, la logique de nouvelle tentative doit être sensible aux exceptions retournées par le disjoncteur, et abandonner les nouvelles tentatives si le disjoncteur indique qu’une erreur n’est pas temporaire.

## <a name="implementing-a-circuit-breaker-pattern-with-polly"></a>Implémentation d’un modèle Disjoncteur avec Polly

Comme lors de l’implémentation de nouvelles tentatives, l’approche recommandée pour les disjoncteurs consiste à tirer parti de bibliothèques .NET éprouvées comme Polly.

L’application eShopOnContainers utilise la stratégie Disjoncteur de Polly lors de l’implémentation de nouvelles tentatives HTTP. En fait, l’application applique les deux stratégies à la classe d’utilitaire ResilientHttpClient. Chaque fois que vous utilisez un objet de type ResilientHttpClient pour des requêtes HTTP (à partir d’eShopOnContainers), vous appliquez ces deux stratégies, mais vous pouvez également ajouter des stratégies supplémentaires.

Ici, le seul ajout au code utilisé pour les nouvelles tentatives d’appel HTTP est le code où vous ajoutez la stratégie Disjoncteur à la liste des stratégies à utiliser, comme indiqué à la fin du code suivant :

```csharp
public ResilientHttpClient CreateResilientHttpClient()
    => new ResilientHttpClient(CreatePolicies(), _logger);

private Policy[] CreatePolicies()
    => new Policy[]
    {
        Policy.Handle<HttpRequestException>()
            .WaitAndRetryAsync(
            // number of retries
            6,
            // exponential backofff
            retryAttempt => TimeSpan.FromSeconds(Math.Pow(2, retryAttempt)),
            // on retry
            (exception, timeSpan, retryCount, context) =>
            {
                var msg = $"Retry {retryCount} implemented with Polly RetryPolicy " +
                    $"of {context.PolicyKey} " +
                    $"at {context.ExecutionKey}, " +
                    $"due to: {exception}.";
                _logger.LogWarning(msg);
                _logger.LogDebug(msg);
            }),
            Policy.Handle<HttpRequestException>()
                .CircuitBreakerAsync(
                    // number of exceptions before breaking circuit
                    5,
                    // time circuit opened before retry
                    TimeSpan.FromMinutes(1),
                    (exception, duration) =>
                    {
                        // on circuit opened
                        _logger.LogTrace("Circuit breaker opened");
                    },
                    () =>
                    {
                        // on circuit closed
                        _logger.LogTrace("Circuit breaker reset");
                    })
    };
}
```

Le code ajoute une stratégie au wrapper HTTP. Cette stratégie définit un disjoncteur qui s’ouvre quand le code détecte le nombre spécifié d’exceptions consécutives (exceptions dans une ligne), tel qu’il a été passé dans le paramètre exceptionsAllowedBeforeBreaking (5 dans le cas présent). Quand le circuit est ouvert, les requêtes HTTP ne fonctionnent pas, mais une exception est levée.

Les disjoncteurs doivent également être utilisés pour rediriger les requêtes vers une infrastructure de secours si vous rencontrez des problèmes dans une ressource particulière déployée dans un environnement autre que l’application cliente ou le service qui effectue l’appel HTTP. De cette façon, si le centre de données subit une panne qui a un impact uniquement sur vos microservices backend, mais pas sur vos applications clientes, ces dernières peuvent effectuer une redirection vers les services de secours. Polly planifie une nouvelle stratégie pour automatiser ce scénario de [stratégie de basculement](https://github.com/App-vNext/Polly/wiki/Polly-Roadmap#failover-policy).

Bien entendu, toutes ces fonctionnalités sont appropriées pour les cas où vous gérez le basculement à partir du code .NET, au lieu qu’il soit géré automatiquement par Azure, avec la transparence des emplacements.

## <a name="using-the-resilienthttpclient-utility-class-from-eshoponcontainers"></a>Utilisation de la classe utilitaire ResilientHttpClient d’eShopOnContainers

Vous utilisez la classe utilitaire ResilientHttpClient de la même manière que vous utilisez la classe .NET HttpClient. Dans l’exemple suivant de l’application web MVC eShopOnContainers (la classe de l’agent OrderingService utilisée par OrderController), l’objet ResilientHttpClient est injecté par le biais du paramètre httpClient du constructeur. L’objet est ensuite utilisé pour exécuter des requêtes HTTP.

```csharp
public class OrderingService : IOrderingService
{
    private IHttpClient _apiClient;
    private readonly string _remoteServiceBaseUrl;
    private readonly IOptionsSnapshot<AppSettings> _settings;
    private readonly IHttpContextAccessor _httpContextAccesor;

    public OrderingService(IOptionsSnapshot<AppSettings> settings,
        IHttpContextAccessor httpContextAccesor,
        IHttpClient httpClient)
    {
        _remoteServiceBaseUrl = $"{settings.Value.OrderingUrl}/api/v1/orders";
        _settings = settings;
        _httpContextAccesor = httpContextAccesor;
        _apiClient = httpClient;
    }

    async public Task<List<Order>> GetMyOrders(ApplicationUser user)
    {
        var context = _httpContextAccesor.HttpContext;
        var token = await context.Authentication.GetTokenAsync("access_token");
        _apiClient.Inst.DefaultRequestHeaders.Authorization = new
            System.Net.Http.Headers.AuthenticationHeaderValue("Bearer", token);
        var ordersUrl = _remoteServiceBaseUrl;
        var dataString = await _apiClient.GetStringAsync(ordersUrl);
        var response = JsonConvert.DeserializeObject<List<Order>>(dataString);
        return response;
    }

    // Other methods ...
    async public Task CreateOrder(Order order)
    {
        var context = _httpContextAccesor.HttpContext;
        var token = await context.Authentication.GetTokenAsync("access_token");
        _apiClient.Inst.DefaultRequestHeaders.Authorization = new
            System.Net.Http.Headers.AuthenticationHeaderValue("Bearer", token);
        _apiClient.Inst.DefaultRequestHeaders.Add("x-requestid",
            order.RequestId.ToString());
        var ordersUrl = $"{_remoteServiceBaseUrl}/new";
        order.CardTypeId = 1;
        order.CardExpirationApiFormat();
        SetFakeIdToProducts(order);
        var response = await _apiClient.PostAsync(ordersUrl, order);
        response.EnsureSuccessStatusCode();
    }
}
```

Chaque fois que l’objet membre \_apiClient est utilisé, il utilise en interne la classe wrapper avec des stratégies de Polly (la stratégie Nouvelle tentative, la stratégie Disjoncteur et toute autre stratégie que vous voulez appliquer à partir de la collection de stratégies de Polly).

## <a name="testing-retries-in-eshoponcontainers"></a>Test de nouvelles tentatives dans eShopOnContainers

Chaque fois que vous démarrez la solution eShopOnContainers sur un hôte Docker, celle-ci doit démarrer plusieurs conteneurs. Certains des conteneurs sont plus lents à démarrer et à initialiser, comme le conteneur SQL Server. Cela est particulièrement vrai la première fois que vous déployez l’application eShopOnContainers dans Docker, car elle doit configurer les images et la base de données. Le fait que certains conteneurs démarrent plus lentement que d’autres peut entraîner la levée d’exceptions HTTP par le reste des services, même si vous définissez des dépendances entre les conteneurs au niveau de Docker Compose, comme expliqué dans les sections précédentes. Ces dépendances Docker Compose entre les conteneurs sont uniquement au niveau processus. Il est possible que le processus de point d’entrée du conteneur soit démarré alors que SQL Server n’est pas prêt pour les requêtes. Cela peut avoir pour conséquence une cascade d’erreurs, et l’application peut recevoir une exception lors d’une tentative d’utilisation de ce conteneur particulier.

Vous pouvez également voir ce type d’erreur au démarrage pendant le déploiement de l’application dans le cloud. Dans ce cas, il est possible que les orchestrateurs déplacent des conteneurs d’un nœud ou d’une machine virtuelle vers un autre nœud ou une autre machine virtuelle (autrement dit, de démarrer de nouvelles instances) lors de l’équilibrage du nombre de conteneurs entre les nœuds du cluster.

eShopOnContainers résout ce problème en utilisant le modèle Nouvelle tentative illustré précédemment. C’est également pourquoi, lors du démarrage de la solution, vous pouvez obtenir des traces de journal ou des avertissements semblables à ce qui suit :

> « **Retry 1 implemented with Polly's RetryPolicy**, due to: System.Net.Http.HttpRequestException: An error occurred while sending the request. ---&gt; System.Net.Http.CurlException: Couldn't connect to server\\n at System.Net.Http.CurlHandler.ThrowIfCURLEError(CURLcode error)\\n at \[...\] ».

## <a name="testing-the-circuit-breaker-in-eshoponcontainers"></a>Test du disjoncteur dans eShopOnContainers

Il existe plusieurs façons d’ouvrir le circuit et de le tester avec eShopOnContainers.

L’une des options consiste à réduire le nombre de tentatives autorisées à 1 dans la stratégie Disjoncteur et à redéployer l’ensemble de la solution dans Docker. Avec une seule nouvelle tentative, il y a de fortes chances qu’une requête HTTP échoue pendant le déploiement, que le disjoncteur s’ouvre et que vous obteniez une erreur.

Une autre option est d’utiliser l’intergiciel (middleware) personnalisé qui est implémenté dans le microservice `Basket`. Quand ce middleware est activé, il intercepte toutes les requêtes HTTP et retourne le code d’état 500. Vous pouvez activer le middleware en effectuant une requête GET à l’URI qui a échoué, comme suit :

-   GET /failing

Cette requête retourne l’état actuel du middleware. Si le middleware est activé, la requête retourne le code d’état 500. Si le middleware est désactivé, il n’y a pas de réponse.

-   GET /failing?enable

Cette requête active le middleware.

-   GET /failing?disable

Cette requête désactive le middleware.

Par exemple, une fois que l’application est en cours d’exécution, vous pouvez activer le middleware en créant une requête à l’aide de l’URI suivant dans n’importe quel navigateur. Notez que le microservice de commandes utilise le port 5103.

http://localhost:5103/failing?enable

Vous pouvez alors vérifier l’état à l’aide de l’URI [http://localhost:5103/failing](http://localhost:5103/failing), comme illustré dans la figure 10-4.

![](./media/image4.png)

**Figure 10-4**. Vérification de l’état du middleware ASP.NET (désactivé dans le cas présent) « Failing » (En échec). 

À ce stade, le microservice Basket répond avec le code d’état 500 chaque fois que vous l’appelez.

Une fois que le middleware est en cours d’exécution, vous pouvez essayer d’effectuer une commande à partir de l’application web MVC. Étant donné que les requêtes échouent, le circuit s’ouvre.

Dans l’exemple suivant, vous pouvez voir que l’application web MVC a un bloc catch dans la logique du processus consistant à passer une commande. Si le code intercepte une exception de circuit ouvert, il affiche à l’utilisateur un message convivial l’invitant à patienter.

```csharp
public class CartController : Controller
{
    //…
    public async Task<IActionResult> Index()
    {
        try
        {
            //… Other code
        }
        catch (BrokenCircuitException)
        {
            // Catches error when Basket.api is in circuit-opened mode                 
            HandleBrokenCircuitException();
        }
        return View();
    }       

    private void HandleBrokenCircuitException()
    {
        TempData["BasketInoperativeMsg"] = "Basket Service is inoperative, please try later on. (Business message due to Circuit-Breaker)";
    }
}
```

Voici un résumé. La stratégie Nouvelle tentative tente plusieurs fois d’exécuter la requête HTTP et obtient des erreurs HTTP. Quand le nombre maximal de tentatives pour la stratégie Disjoncteur est atteint (dans le cas présent, 5), l’application lève un BrokenCircuitException. Le résultat est un message convivial, comme illustré dans la figure 10-5.

![](./media/image5.png)

**Figure 10-5**. Disjoncteur retournant une erreur à l’interface utilisateur

Vous pouvez implémenter une logique différente pour ouvrir le circuit. Vous pouvez également essayer une requête HTTP sur un autre microservice backend s’il existe un centre de données de secours ou un système backend redondant.

Enfin, une autre solution pour la stratégie Disjoncteur consiste à utiliser Isolate (qui force l’ouverture du circuit et le maintient ouvert) et Reset (qui le referme). Ces solutions peuvent être utilisées pour créer un point de terminaison HTTP d’utilitaire qui appelle Isolate et Reset directement sur la stratégie. Un tel point de terminaison HTTP peut également être utilisé, correctement sécurisé, en production pour l’isolation temporaire d’un système en aval, par exemple quand vous voulez procéder à sa mise à niveau. Ou bien il peut déclencher le circuit manuellement pour protéger un système en aval que vous soupçonnez d’avoir provoqué l’erreur.

## <a name="adding-a-jitter-strategy-to-the-retry-policy"></a>Ajout d’une stratégie d’instabilité à la stratégie de nouvelle tentative

Une stratégie Nouvelle tentative standard peut avoir un impact sur votre système en cas de fort accès concurrentiel, de haute scalabilité et de contention élevée. Pour surmonter les pointes de nouvelles tentatives similaires provenant de nombreux clients en cas de pannes partielles, une solution de contournement efficace consiste à ajouter une stratégie d’instabilité à la stratégie/l’algorithme de nouvelle tentative. Cela peut améliorer les performances globales du système de bout en bout en ajoutant le caractère aléatoire à l’interruption exponentielle. Les pointes sont alors réparties quand des problèmes surviennent. Quand vous utilisez Polly, le code permettant d’implémenter l’instabilité peut ressembler à l’exemple suivant :

```csharp
Random jitterer = new Random();
Policy.Handle<HttpResponseException>() // etc
    .WaitAndRetry(5, // exponential back-off plus some jitter
        retryAttempt => TimeSpan.FromSeconds(Math.Pow(2, retryAttempt))
            + TimeSpan.FromMilliseconds(jitterer.Next(0, 100))
    );
```

## <a name="additional-resources"></a>Ressources supplémentaires

-   **Modèle Nouvelle tentative**
    [*https://docs.microsoft.com/azure/architecture/patterns/retry*](https://docs.microsoft.com/azure/architecture/patterns/retry)

-   **Résilience des connexions** (Entity Framework Core) [*https://docs.microsoft.com/ef/core/miscellaneous/connection-resiliency*](https://docs.microsoft.com/ef/core/miscellaneous/connection-resiliency)

-   **Polly** (Résilience .NET et bibliothèque de gestion des erreurs temporaires) [*https://github.com/App-vNext/Polly*](https://github.com/App-vNext/Polly)

-   **Modèle Disjoncteur**
    [*https://docs.microsoft.com/azure/architecture/patterns/circuit-breaker*](https://docs.microsoft.com/azure/architecture/patterns/circuit-breaker)

-   **Marc Brooker. Jitter: Making Things Better With Randomness** https://brooker.co.za/blog/2015/03/21/backoff.html


>[!div class="step-by-step"]
[Précédent] (implement-http-call-retries-exponential-backoff-polly.md) [Suivant] (monitor-app-health.md)
