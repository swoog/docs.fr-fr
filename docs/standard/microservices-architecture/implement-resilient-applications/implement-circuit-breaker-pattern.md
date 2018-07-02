---
title: Implémentation du modèle Disjoncteur
description: Architecture des microservices .NET pour les applications .NET en conteneur | Implémentation du modèle Disjoncteur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/12/2017
ms.openlocfilehash: 2c89992c4c60ca7f1085050e6fed4922ecd4d8cc
ms.sourcegitcommit: 979597cd8055534b63d2c6ee8322938a27d0c87b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37106125"
---
# <a name="implementing-the-circuit-breaker-pattern"></a><span data-ttu-id="ef4b7-103">Implémentation du modèle Disjoncteur</span><span class="sxs-lookup"><span data-stu-id="ef4b7-103">Implementing the Circuit Breaker pattern</span></span>

<span data-ttu-id="ef4b7-104">Comme indiqué précédemment, vous devez gérer des erreurs dont le temps de récupération peut être variable, comme ça peut être le cas quand vous essayez de vous connecter à une ressource ou à un service distant.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-104">As noted earlier, you should handle faults that might take a variable amount of time to recover from, as might happen when you try to connect to a remote service or resource.</span></span> <span data-ttu-id="ef4b7-105">La gestion de ce type d’erreur peut améliorer la stabilité et la résilience d’une application.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-105">Handling this type of fault can improve the stability and resiliency of an application.</span></span>

<span data-ttu-id="ef4b7-106">Dans un environnement distribué, les appels à des ressources et services distants peuvent échouer en raison d’erreurs temporaires, telles que des connexions réseau lentes, l’expiration de délais d’attente, ou si des ressources sont lentes ou temporairement indisponibles.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-106">In a distributed environment, calls to remote resources and services can fail due to transient faults, such as slow network connections and timeouts, or if resources are being slow or are temporarily unavailable.</span></span> <span data-ttu-id="ef4b7-107">En général, ces erreurs se corrigent d’elles-mêmes après un bref laps de temps, et une application cloud fiable doit être prête à les gérer à l’aide d’une stratégie comme le modèle Nouvelle tentative.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-107">These faults typically correct themselves after a short time, and a robust cloud application should be prepared to handle them by using a strategy like the Retry pattern.</span></span>

<span data-ttu-id="ef4b7-108">Toutefois, dans certaines situations, les erreurs sont dues à des événements imprévus dont la correction peut prendre beaucoup plus de temps.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-108">However, there can also be situations where faults are due to unanticipated events that might take much longer to fix.</span></span> <span data-ttu-id="ef4b7-109">La gravité de ces erreurs peut aller d’une perte partielle de connectivité à la défaillance complète d’un service.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-109">These faults can range in severity from a partial loss of connectivity to the complete failure of a service.</span></span> <span data-ttu-id="ef4b7-110">Dans ces cas de figure, il peut être inutile qu’une application effectue de nouvelles tentatives dont la réussite sera peu probable.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-110">In these situations, it might be pointless for an application to continually retry an operation that is unlikely to succeed.</span></span> <span data-ttu-id="ef4b7-111">L’application doit plutôt être codée pour reconnaître que l’opération a échoué et gérer l’échec en conséquence.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-111">Instead, the application should be coded to accept that the operation has failed and handle the failure accordingly.</span></span>

<span data-ttu-id="ef4b7-112">L’objectif du modèle Disjoncteur est différent de celui du modèle Nouvelle tentative.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-112">The Circuit Breaker pattern has a different purpose than the Retry pattern.</span></span> <span data-ttu-id="ef4b7-113">Le modèle Nouvelle tentative permet à une application de retenter une opération en partant du principe qu’elle finira par réussir.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-113">The Retry pattern enables an application to retry an operation in the expectation that the operation will eventually succeed.</span></span> <span data-ttu-id="ef4b7-114">Le modèle Disjoncteur empêche une application d’effectuer une opération qui échouera probablement.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-114">The Circuit Breaker pattern prevents an application from performing an operation that is likely to fail.</span></span> <span data-ttu-id="ef4b7-115">Une application peut combiner ces deux modèles en utilisant le modèle Nouvelle tentative pour appeler une opération par le biais d’un disjoncteur.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-115">An application can combine these two patterns by using the Retry pattern to invoke an operation through a circuit breaker.</span></span> <span data-ttu-id="ef4b7-116">Toutefois, la logique de nouvelle tentative doit être sensible aux exceptions retournées par le disjoncteur, et abandonner les nouvelles tentatives si le disjoncteur indique qu’une erreur n’est pas temporaire.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-116">However, the retry logic should be sensitive to any exceptions returned by the circuit breaker, and it should abandon retry attempts if the circuit breaker indicates that a fault is not transient.</span></span>

## <a name="implementing-a-circuit-breaker-pattern-with-polly"></a><span data-ttu-id="ef4b7-117">Implémentation d’un modèle Disjoncteur avec Polly</span><span class="sxs-lookup"><span data-stu-id="ef4b7-117">Implementing a Circuit Breaker pattern with Polly</span></span>

<span data-ttu-id="ef4b7-118">Comme lors de l’implémentation de nouvelles tentatives, l’approche recommandée pour les disjoncteurs consiste à tirer parti de bibliothèques .NET éprouvées comme Polly.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-118">As when implementing retries, the recommended approach for circuit breakers is to take advantage of proven .NET libraries like Polly.</span></span>

<span data-ttu-id="ef4b7-119">L’application eShopOnContainers utilise la stratégie Disjoncteur de Polly lors de l’implémentation de nouvelles tentatives HTTP.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-119">The eShopOnContainers application uses the Polly Circuit Breaker policy when implementing HTTP retries.</span></span> <span data-ttu-id="ef4b7-120">En fait, l’application applique les deux stratégies à la classe d’utilitaire ResilientHttpClient.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-120">In fact, the application applies both policies to the ResilientHttpClient utility class.</span></span> <span data-ttu-id="ef4b7-121">Chaque fois que vous utilisez un objet de type ResilientHttpClient pour des requêtes HTTP (à partir d’eShopOnContainers), vous appliquez ces deux stratégies, mais vous pouvez également ajouter des stratégies supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-121">Whenever you use an object of type ResilientHttpClient for HTTP requests (from eShopOnContainers), you will be applying both those policies, but you could add additional policies, too.</span></span>

<span data-ttu-id="ef4b7-122">Ici, le seul ajout au code utilisé pour les nouvelles tentatives d’appel HTTP est le code où vous ajoutez la stratégie Disjoncteur à la liste des stratégies à utiliser, comme indiqué à la fin du code suivant :</span><span class="sxs-lookup"><span data-stu-id="ef4b7-122">The only addition here to the code used for HTTP call retries is the code where you add the Circuit Breaker policy to the list of policies to use, as shown at the end of the following code:</span></span>

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

<span data-ttu-id="ef4b7-123">Le code ajoute une stratégie au wrapper HTTP.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-123">The code adds a policy to the HTTP wrapper.</span></span> <span data-ttu-id="ef4b7-124">Cette stratégie définit un disjoncteur qui s’ouvre quand le code détecte le nombre spécifié d’exceptions consécutives (exceptions dans une ligne), tel qu’il a été passé dans le paramètre exceptionsAllowedBeforeBreaking (5 dans le cas présent).</span><span class="sxs-lookup"><span data-stu-id="ef4b7-124">That policy defines a circuit breaker that opens when the code detects the specified number of consecutive exceptions (exceptions in a row), as passed in the exceptionsAllowedBeforeBreaking parameter (5 in this case).</span></span> <span data-ttu-id="ef4b7-125">Quand le circuit est ouvert, les requêtes HTTP ne fonctionnent pas, mais une exception est levée.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-125">When the circuit is open, HTTP requests do not work, but an exception is raised.</span></span>

<span data-ttu-id="ef4b7-126">Les disjoncteurs doivent également être utilisés pour rediriger les requêtes vers une infrastructure de secours si vous rencontrez des problèmes dans une ressource particulière déployée dans un environnement autre que l’application cliente ou le service qui effectue l’appel HTTP.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-126">Circuit breakers should also be used to redirect requests to a fallback infrastructure if you might have issues in a particular resource that is deployed in a different environment than the client application or service that is performing the HTTP call.</span></span> <span data-ttu-id="ef4b7-127">De cette façon, si le centre de données subit une panne qui a un impact uniquement sur vos microservices backend, mais pas sur vos applications clientes, ces dernières peuvent effectuer une redirection vers les services de secours.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-127">That way, if there is an outage in the datacenter that impacts only your backend microservices but not your client applications, the client applications can redirect to the fallback services.</span></span> <span data-ttu-id="ef4b7-128">Polly planifie une nouvelle stratégie pour automatiser ce scénario de [stratégie de basculement](https://github.com/App-vNext/Polly/wiki/Polly-Roadmap#failover-policy).</span><span class="sxs-lookup"><span data-stu-id="ef4b7-128">Polly is planning a new policy to automate this [failover policy](https://github.com/App-vNext/Polly/wiki/Polly-Roadmap#failover-policy) scenario.</span></span>

<span data-ttu-id="ef4b7-129">Bien entendu, toutes ces fonctionnalités sont appropriées pour les cas où vous gérez le basculement à partir du code .NET, au lieu qu’il soit géré automatiquement par Azure, avec la transparence des emplacements.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-129">Of course, all those features are for cases where you are managing the failover from within the .NET code, as opposed to having it managed automatically for you by Azure, with location transparency.</span></span>

## <a name="using-the-resilienthttpclient-utility-class-from-eshoponcontainers"></a><span data-ttu-id="ef4b7-130">Utilisation de la classe utilitaire ResilientHttpClient d’eShopOnContainers</span><span class="sxs-lookup"><span data-stu-id="ef4b7-130">Using the ResilientHttpClient utility class from eShopOnContainers</span></span>

<span data-ttu-id="ef4b7-131">Vous utilisez la classe utilitaire ResilientHttpClient de la même manière que vous utilisez la classe .NET HttpClient.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-131">You use the ResilientHttpClient utility class in a way similar to how you use the .NET HttpClient class.</span></span> <span data-ttu-id="ef4b7-132">Dans l’exemple suivant de l’application web MVC eShopOnContainers (la classe de l’agent OrderingService utilisée par OrderController), l’objet ResilientHttpClient est injecté par le biais du paramètre httpClient du constructeur.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-132">In the following example from the eShopOnContainers MVC web application (the OrderingService agent class used by OrderController), the ResilientHttpClient object is injected through the httpClient parameter of the constructor.</span></span> <span data-ttu-id="ef4b7-133">L’objet est ensuite utilisé pour exécuter des requêtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-133">Then the object is used to perform HTTP requests.</span></span>

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

<span data-ttu-id="ef4b7-134">Chaque fois que l’objet membre \_apiClient est utilisé, il utilise en interne la classe wrapper avec des stratégies de Polly (la stratégie Nouvelle tentative, la stratégie Disjoncteur et toute autre stratégie que vous voulez appliquer à partir de la collection de stratégies de Polly).</span><span class="sxs-lookup"><span data-stu-id="ef4b7-134">Whenever the \_apiClient member object is used, it internally uses the wrapper class with Polly policiesؙ—the Retry policy, the Circuit Breaker policy, and any other policy that you might want to apply from the Polly policies collection.</span></span>

## <a name="testing-retries-in-eshoponcontainers"></a><span data-ttu-id="ef4b7-135">Test de nouvelles tentatives dans eShopOnContainers</span><span class="sxs-lookup"><span data-stu-id="ef4b7-135">Testing retries in eShopOnContainers</span></span>

<span data-ttu-id="ef4b7-136">Chaque fois que vous démarrez la solution eShopOnContainers sur un hôte Docker, celle-ci doit démarrer plusieurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-136">Whenever you start the eShopOnContainers solution in a Docker host, it needs to start multiple containers.</span></span> <span data-ttu-id="ef4b7-137">Certains des conteneurs sont plus lents à démarrer et à initialiser, comme le conteneur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-137">Some of the containers are slower to start and initialize, like the SQL Server container.</span></span> <span data-ttu-id="ef4b7-138">Cela est particulièrement vrai la première fois que vous déployez l’application eShopOnContainers dans Docker, car elle doit configurer les images et la base de données.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-138">This is especially true the first time you deploy the eShopOnContainers application into Docker, because it needs to set up the images and the database.</span></span> <span data-ttu-id="ef4b7-139">Le fait que certains conteneurs démarrent plus lentement que d’autres peut entraîner la levée d’exceptions HTTP par le reste des services, même si vous définissez des dépendances entre les conteneurs au niveau de Docker Compose, comme expliqué dans les sections précédentes.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-139">The fact that some containers start slower than others can cause the rest of the services to initially throw HTTP exceptions, even if you set dependencies between containers at the docker-compose level, as explained in previous sections.</span></span> <span data-ttu-id="ef4b7-140">Ces dépendances Docker Compose entre les conteneurs sont uniquement au niveau processus.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-140">Those docker-compose dependencies between containers are just at the process level.</span></span> <span data-ttu-id="ef4b7-141">Il est possible que le processus de point d’entrée du conteneur soit démarré alors que SQL Server n’est pas prêt pour les requêtes.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-141">The container’s entry point process might be started, but SQL Server might not be ready for queries.</span></span> <span data-ttu-id="ef4b7-142">Cela peut avoir pour conséquence une cascade d’erreurs, et l’application peut recevoir une exception lors d’une tentative d’utilisation de ce conteneur particulier.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-142">The result can be a cascade of errors, and the application can get an exception when trying to consume that particular container.</span></span>

<span data-ttu-id="ef4b7-143">Vous pouvez également voir ce type d’erreur au démarrage pendant le déploiement de l’application dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-143">You might also see this type of error on startup when the application is deploying to the cloud.</span></span> <span data-ttu-id="ef4b7-144">Dans ce cas, il est possible que les orchestrateurs déplacent des conteneurs d’un nœud ou d’une machine virtuelle vers un autre nœud ou une autre machine virtuelle (autrement dit, de démarrer de nouvelles instances) lors de l’équilibrage du nombre de conteneurs entre les nœuds du cluster.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-144">In that case, orchestrators might be moving containers from one node or VM to another (that is, starting new instances) when balancing the number of containers across the cluster’s nodes.</span></span>

<span data-ttu-id="ef4b7-145">eShopOnContainers résout ce problème en utilisant le modèle Nouvelle tentative illustré précédemment.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-145">The way eShopOnContainers solves this issue is by using the Retry pattern we illustrated earlier.</span></span> <span data-ttu-id="ef4b7-146">C’est également pourquoi, lors du démarrage de la solution, vous pouvez obtenir des traces de journal ou des avertissements semblables à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="ef4b7-146">It is also why, when starting the solution, you might get log traces or warnings like the following:</span></span>

> <span data-ttu-id="ef4b7-147">« **Retry 1 implemented with Polly's RetryPolicy**, due to: System.Net.Http.HttpRequestException: An error occurred while sending the request.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-147">"**Retry 1 implemented with Polly's RetryPolicy**, due to: System.Net.Http.HttpRequestException: An error occurred while sending the request.</span></span><span data-ttu-id="ef4b7-148"> ---&gt; System.Net.Http.CurlException: Couldn't connect to server\\n at System.Net.Http.CurlHandler.ThrowIfCURLEError(CURLcode error)\\n at \[...\] ».</span><span class="sxs-lookup"><span data-stu-id="ef4b7-148"> ---&gt; System.Net.Http.CurlException: Couldn't connect to server\\n at System.Net.Http.CurlHandler.ThrowIfCURLEError(CURLcode error)\\n at \[...\].</span></span>

## <a name="testing-the-circuit-breaker-in-eshoponcontainers"></a><span data-ttu-id="ef4b7-149">Test du disjoncteur dans eShopOnContainers</span><span class="sxs-lookup"><span data-stu-id="ef4b7-149">Testing the circuit breaker in eShopOnContainers</span></span>

<span data-ttu-id="ef4b7-150">Il existe plusieurs façons d’ouvrir le circuit et de le tester avec eShopOnContainers.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-150">There are a few ways you can open the circuit and test it with eShopOnContainers.</span></span>

<span data-ttu-id="ef4b7-151">L’une des options consiste à réduire le nombre de tentatives autorisées à 1 dans la stratégie Disjoncteur et à redéployer l’ensemble de la solution dans Docker.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-151">One option is to lower the allowed number of retries to 1 in the circuit breaker policy and redeploy the whole solution into Docker.</span></span> <span data-ttu-id="ef4b7-152">Avec une seule nouvelle tentative, il y a de fortes chances qu’une requête HTTP échoue pendant le déploiement, que le disjoncteur s’ouvre et que vous obteniez une erreur.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-152">With a single retry, there is a good chance that an HTTP request will fail during deployment, the circuit breaker will open, and you get an error.</span></span>

<span data-ttu-id="ef4b7-153">Une autre option est d’utiliser l’intergiciel (middleware) personnalisé qui est implémenté dans le microservice `Basket`.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-153">Another option is to use custom middleware that is implemented in the `Basket` microservice.</span></span> <span data-ttu-id="ef4b7-154">Quand ce middleware est activé, il intercepte toutes les requêtes HTTP et retourne le code d’état 500.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-154">When this middleware is enabled, it catches all HTTP requests and returns status code 500.</span></span> <span data-ttu-id="ef4b7-155">Vous pouvez activer le middleware en effectuant une requête GET à l’URI qui a échoué, comme suit :</span><span class="sxs-lookup"><span data-stu-id="ef4b7-155">You can enable the middleware by making a GET request to the failing URI, like the following:</span></span>

-   <span data-ttu-id="ef4b7-156">GET /failing</span><span class="sxs-lookup"><span data-stu-id="ef4b7-156">GET /failing</span></span>

<span data-ttu-id="ef4b7-157">Cette requête retourne l’état actuel du middleware.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-157">This request returns the current state of the middleware.</span></span> <span data-ttu-id="ef4b7-158">Si le middleware est activé, la requête retourne le code d’état 500.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-158">If the middleware is enabled, the request return status code 500.</span></span> <span data-ttu-id="ef4b7-159">Si le middleware est désactivé, il n’y a pas de réponse.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-159">If the middleware is disabled, there is no response.</span></span>

-   <span data-ttu-id="ef4b7-160">GET /failing?enable</span><span class="sxs-lookup"><span data-stu-id="ef4b7-160">GET /failing?enable</span></span>

<span data-ttu-id="ef4b7-161">Cette requête active le middleware.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-161">This request enables the middleware.</span></span>

-   <span data-ttu-id="ef4b7-162">GET /failing?disable</span><span class="sxs-lookup"><span data-stu-id="ef4b7-162">GET /failing?disable</span></span>

<span data-ttu-id="ef4b7-163">Cette requête désactive le middleware.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-163">This request disables the middleware.</span></span>

<span data-ttu-id="ef4b7-164">Par exemple, une fois que l’application est en cours d’exécution, vous pouvez activer le middleware en créant une requête à l’aide de l’URI suivant dans n’importe quel navigateur.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-164">For instance, once the application is running, you can enable the middleware by making a request using the following URI in any browser.</span></span> <span data-ttu-id="ef4b7-165">Notez que le microservice de commandes utilise le port 5103.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-165">Note that the ordering microservice uses port 5103.</span></span>

http://localhost:5103/failing?enable

<span data-ttu-id="ef4b7-166">Vous pouvez alors vérifier l’état à l’aide de l’URI [http://localhost:5103/failing](http://localhost:5103/failing), comme illustré dans la figure 10-4.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-166">You can then check the status using the URI [http://localhost:5103/failing](http://localhost:5103/failing), as shown in Figure 10-4.</span></span>

![](./media/image4.png)

<span data-ttu-id="ef4b7-167">**Figure 10-4**.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-167">**Figure 10-4**.</span></span> <span data-ttu-id="ef4b7-168">Vérification de l’état du middleware ASP.NET (désactivé dans le cas présent) « Failing » (En échec).</span><span class="sxs-lookup"><span data-stu-id="ef4b7-168">Checking the state of the “Failing” ASP.NET middleware – In this case, disabled.</span></span> 

<span data-ttu-id="ef4b7-169">À ce stade, le microservice Basket répond avec le code d’état 500 chaque fois que vous l’appelez.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-169">At this point, the Basket microservice responds with status code 500 whenever you call invoke it.</span></span>

<span data-ttu-id="ef4b7-170">Une fois que le middleware est en cours d’exécution, vous pouvez essayer d’effectuer une commande à partir de l’application web MVC.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-170">Once the middleware is running, you can try making an order from the MVC web application.</span></span> <span data-ttu-id="ef4b7-171">Étant donné que les requêtes échouent, le circuit s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-171">Because the requests fails, the circuit will open.</span></span>

<span data-ttu-id="ef4b7-172">Dans l’exemple suivant, vous pouvez voir que l’application web MVC a un bloc catch dans la logique du processus consistant à passer une commande.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-172">In the following example, you can see that the MVC web application has a catch block in the logic for placing an order.</span></span> <span data-ttu-id="ef4b7-173">Si le code intercepte une exception de circuit ouvert, il affiche à l’utilisateur un message convivial l’invitant à patienter.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-173">If the code catches an open-circuit exception, it shows the user a friendly message telling them to wait.</span></span>

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

<span data-ttu-id="ef4b7-174">Voici un résumé.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-174">Here’s a summary.</span></span> <span data-ttu-id="ef4b7-175">La stratégie Nouvelle tentative tente plusieurs fois d’exécuter la requête HTTP et obtient des erreurs HTTP.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-175">The Retry policy tries several times to make the HTTP request and gets HTTP errors.</span></span> <span data-ttu-id="ef4b7-176">Quand le nombre maximal de tentatives pour la stratégie Disjoncteur est atteint (dans le cas présent, 5), l’application lève un BrokenCircuitException.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-176">When the number of tries reaches the maximum number set for the Circuit Breaker policy (in this case, 5), the application throws a BrokenCircuitException.</span></span> <span data-ttu-id="ef4b7-177">Le résultat est un message convivial, comme illustré dans la figure 10-5.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-177">The result is a friendly message, as shown in Figure 10-5.</span></span>

![](./media/image5.png)

<span data-ttu-id="ef4b7-178">**Figure 10-5**.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-178">**Figure 10-5**.</span></span> <span data-ttu-id="ef4b7-179">Disjoncteur retournant une erreur à l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="ef4b7-179">Circuit breaker returning an error to the UI</span></span>

<span data-ttu-id="ef4b7-180">Vous pouvez implémenter une logique différente pour ouvrir le circuit.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-180">You can implement different logic for when to open the circuit.</span></span> <span data-ttu-id="ef4b7-181">Vous pouvez également essayer une requête HTTP sur un autre microservice backend s’il existe un centre de données de secours ou un système backend redondant.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-181">Or you can try an HTTP request against a different back-end microservice if there is a fallback datacenter or redundant back-end system.</span></span>

<span data-ttu-id="ef4b7-182">Enfin, une autre solution pour la stratégie Disjoncteur consiste à utiliser Isolate (qui force l’ouverture du circuit et le maintient ouvert) et Reset (qui le referme).</span><span class="sxs-lookup"><span data-stu-id="ef4b7-182">Finally, another possibility for the CircuitBreakerPolicy is to use Isolate (which forces open and holds open the circuit) and Reset (which closes it again).</span></span> <span data-ttu-id="ef4b7-183">Ces solutions peuvent être utilisées pour créer un point de terminaison HTTP d’utilitaire qui appelle Isolate et Reset directement sur la stratégie.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-183">These could be used to build a utility HTTP endpoint that invokes Isolate and Reset directly on the policy.</span></span> <span data-ttu-id="ef4b7-184">Un tel point de terminaison HTTP peut également être utilisé, correctement sécurisé, en production pour l’isolation temporaire d’un système en aval, par exemple quand vous voulez procéder à sa mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-184">Such an HTTP endpoint could also be used, suitably secured, in production for temporarily isolating a downstream system, such as when you want to upgrade it.</span></span> <span data-ttu-id="ef4b7-185">Ou bien il peut déclencher le circuit manuellement pour protéger un système en aval que vous soupçonnez d’avoir provoqué l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-185">Or it could trip the circuit manually to protect a downstream system you suspect to be faulting.</span></span>

## <a name="adding-a-jitter-strategy-to-the-retry-policy"></a><span data-ttu-id="ef4b7-186">Ajout d’une stratégie d’instabilité à la stratégie de nouvelle tentative</span><span class="sxs-lookup"><span data-stu-id="ef4b7-186">Adding a jitter strategy to the retry policy</span></span>

<span data-ttu-id="ef4b7-187">Une stratégie Nouvelle tentative standard peut avoir un impact sur votre système en cas de fort accès concurrentiel, de haute scalabilité et de contention élevée.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-187">A regular Retry policy can impact your system in cases of high concurrency and scalability and under high contention.</span></span> <span data-ttu-id="ef4b7-188">Pour surmonter les pointes de nouvelles tentatives similaires provenant de nombreux clients en cas de pannes partielles, une solution de contournement efficace consiste à ajouter une stratégie d’instabilité à la stratégie/l’algorithme de nouvelle tentative.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-188">To overcome peaks of similar retries coming from many clients in case of partial outages, a good workaround is to add a jitter strategy to the retry algorithm/policy.</span></span> <span data-ttu-id="ef4b7-189">Cela peut améliorer les performances globales du système de bout en bout en ajoutant le caractère aléatoire à l’interruption exponentielle.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-189">This can improve the overall performance of the end-to-end system by adding randomness to the exponential backoff.</span></span> <span data-ttu-id="ef4b7-190">Les pointes sont alors réparties quand des problèmes surviennent.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-190">This spreads out the spikes when issues arise.</span></span> <span data-ttu-id="ef4b7-191">Quand vous utilisez Polly, le code permettant d’implémenter l’instabilité peut ressembler à l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="ef4b7-191">When you use Polly, code to implement jitter could look like the following example:</span></span>

```csharp
Random jitterer = new Random();
Policy.Handle<HttpResponseException>() // etc
    .WaitAndRetry(5, // exponential back-off plus some jitter
        retryAttempt => TimeSpan.FromSeconds(Math.Pow(2, retryAttempt))
            + TimeSpan.FromMilliseconds(jitterer.Next(0, 100))
    );
```

## <a name="additional-resources"></a><span data-ttu-id="ef4b7-192">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ef4b7-192">Additional resources</span></span>

-   <span data-ttu-id="ef4b7-193">**Modèle Nouvelle tentative**
    [*https://docs.microsoft.com/azure/architecture/patterns/retry*](https://docs.microsoft.com/azure/architecture/patterns/retry)</span><span class="sxs-lookup"><span data-stu-id="ef4b7-193">**Retry pattern**
[*https://docs.microsoft.com/azure/architecture/patterns/retry*](https://docs.microsoft.com/azure/architecture/patterns/retry)</span></span>

-   <span data-ttu-id="ef4b7-194">**Résilience des connexions** (Entity Framework Core) [*https://docs.microsoft.com/ef/core/miscellaneous/connection-resiliency*](https://docs.microsoft.com/ef/core/miscellaneous/connection-resiliency)</span><span class="sxs-lookup"><span data-stu-id="ef4b7-194">**Connection Resiliency** (Entity Framework Core) [*https://docs.microsoft.com/ef/core/miscellaneous/connection-resiliency*](https://docs.microsoft.com/ef/core/miscellaneous/connection-resiliency)</span></span>

-   <span data-ttu-id="ef4b7-195">**Polly** (Résilience .NET et bibliothèque de gestion des erreurs temporaires) [*https://github.com/App-vNext/Polly*](https://github.com/App-vNext/Polly)</span><span class="sxs-lookup"><span data-stu-id="ef4b7-195">**Polly** (.NET resilience and transient-fault-handling library) [*https://github.com/App-vNext/Polly*](https://github.com/App-vNext/Polly)</span></span>

-   <span data-ttu-id="ef4b7-196">**Modèle Disjoncteur**
    [*https://docs.microsoft.com/azure/architecture/patterns/circuit-breaker*](https://docs.microsoft.com/azure/architecture/patterns/circuit-breaker)</span><span class="sxs-lookup"><span data-stu-id="ef4b7-196">**Circuit Breaker pattern**
[*https://docs.microsoft.com/azure/architecture/patterns/circuit-breaker*](https://docs.microsoft.com/azure/architecture/patterns/circuit-breaker)</span></span>

-   <span data-ttu-id="ef4b7-197">**Marc Brooker. Jitter: Making Things Better With Randomness** https://brooker.co.za/blog/2015/03/21/backoff.html</span><span class="sxs-lookup"><span data-stu-id="ef4b7-197">**Marc Brooker. Jitter: Making Things Better With Randomness** https://brooker.co.za/blog/2015/03/21/backoff.html</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="ef4b7-198">[Précédent](implement-http-call-retries-exponential-backoff-polly.md)
[Suivant](monitor-app-health.md)</span><span class="sxs-lookup"><span data-stu-id="ef4b7-198">[Previous](implement-http-call-retries-exponential-backoff-polly.md)
[Next](monitor-app-health.md)</span></span>
