---
title: Implémentation du modèle Disjoncteur
description: Architecture des microservices .NET pour les applications .NET en conteneur | Implémenter le modèle Disjoncteur comme système complémentaire aux nouvelles tentatives Http
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 07/03/2018
ms.openlocfilehash: d5902c5a0744d74ae5086a4df3aee606b24b6030
ms.sourcegitcommit: 59b51cd7c95c75be85bd6ef715e9ef8c85720bac
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/06/2018
ms.locfileid: "37875165"
---
# <a name="implement-the-circuit-breaker-pattern"></a><span data-ttu-id="c4764-103">Implémenter le modèle Disjoncteur</span><span class="sxs-lookup"><span data-stu-id="c4764-103">Implement the Circuit Breaker pattern</span></span>

<span data-ttu-id="c4764-104">Comme indiqué précédemment, vous devez gérer des erreurs dont le temps de récupération est variable, comme cela peut être le cas quand vous essayez de vous connecter à une ressource ou à un service distant.</span><span class="sxs-lookup"><span data-stu-id="c4764-104">As noted earlier, you should handle faults that might take a variable amount of time to recover from, as it might happen when you try to connect to a remote service or resource.</span></span> <span data-ttu-id="c4764-105">La gestion de ce type d’erreur peut améliorer la stabilité et la résilience d’une application.</span><span class="sxs-lookup"><span data-stu-id="c4764-105">Handling this type of fault can improve the stability and resiliency of an application.</span></span>

<span data-ttu-id="c4764-106">Dans un environnement distribué, les appels à des ressources et services distants peuvent échouer en raison d’erreurs temporaires, telles que des connexions réseau lentes, l’expiration de délais d’attente, ou si des ressources sont lentes ou temporairement indisponibles.</span><span class="sxs-lookup"><span data-stu-id="c4764-106">In a distributed environment, calls to remote resources and services can fail due to transient faults, such as slow network connections and timeouts, or if resources are being slow or are temporarily unavailable.</span></span> <span data-ttu-id="c4764-107">En général, ces erreurs se corrigent d’elles-mêmes après un bref laps de temps, et une application cloud fiable doit être prête à les gérer à l’aide d’une stratégie comme le « modèle Nouvelle tentative ».</span><span class="sxs-lookup"><span data-stu-id="c4764-107">These faults typically correct themselves after a short time, and a robust cloud application should be prepared to handle them by using a strategy like the "Retry pattern".</span></span> 

<span data-ttu-id="c4764-108">Toutefois, dans certaines situations, les erreurs sont dues à des événements imprévus dont la correction peut prendre beaucoup plus de temps.</span><span class="sxs-lookup"><span data-stu-id="c4764-108">However, there can also be situations where faults are due to unanticipated events that might take much longer to fix.</span></span> <span data-ttu-id="c4764-109">La gravité de ces erreurs peut aller d’une perte partielle de connectivité à la défaillance complète d’un service.</span><span class="sxs-lookup"><span data-stu-id="c4764-109">These faults can range in severity from a partial loss of connectivity to the complete failure of a service.</span></span> <span data-ttu-id="c4764-110">Dans ces cas de figure, il peut être inutile qu’une application effectue de nouvelles tentatives dont la réussite sera peu probable.</span><span class="sxs-lookup"><span data-stu-id="c4764-110">In these situations, it might be pointless for an application to continually retry an operation that is unlikely to succeed.</span></span> 

<span data-ttu-id="c4764-111">L’application doit plutôt être codée pour reconnaître que l’opération a échoué et gérer l’échec en conséquence.</span><span class="sxs-lookup"><span data-stu-id="c4764-111">Instead, the application should be coded to accept that the operation has failed and handle the failure accordingly.</span></span>

<span data-ttu-id="c4764-112">L’utilisation désinvolte des nouvelles tentatives Http peut entraîner la création d’une attaque par déni de service ([DoS](https://en.wikipedia.org/wiki/Denial-of-service_attack)) au sein de votre propre logiciel.</span><span class="sxs-lookup"><span data-stu-id="c4764-112">Using Http retries carelessly could result in creating a Denial of Service ([DoS](https://en.wikipedia.org/wiki/Denial-of-service_attack)) attack within your own software.</span></span> <span data-ttu-id="c4764-113">Lorsqu’un microservice échoue ou s’exécute lentement, plusieurs clients peuvent répéter à plusieurs reprises les demandes ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="c4764-113">As a microservice fails or performs slowly, multiple clients might repeatedly retry failed requests.</span></span> <span data-ttu-id="c4764-114">Ceci crée un risque dangereux d’augmentation exponentielle du trafic ciblé vers le service défaillant.</span><span class="sxs-lookup"><span data-stu-id="c4764-114">That creates a dangerous risk of exponentially increasing traffic targeted at the failing service.</span></span>

<span data-ttu-id="c4764-115">Par conséquent, vous avez besoin d’une sorte de barrière de défense afin que les nouvelles tentatives arrêtent les demandes lorsqu’il ne vaut pas la peine de continuer à essayer.</span><span class="sxs-lookup"><span data-stu-id="c4764-115">Therefore, you need some kind of defense barrier so the retries stop requests when it is not worth to keep trying.</span></span> <span data-ttu-id="c4764-116">Cette barrière de défense est précisément le disjoncteur.</span><span class="sxs-lookup"><span data-stu-id="c4764-116">That defense barrier is precisely the circuit breaker.</span></span>

<span data-ttu-id="c4764-117">L’objectif du modèle Disjoncteur est différent de celui du « modèle Nouvelle tentative ».</span><span class="sxs-lookup"><span data-stu-id="c4764-117">The Circuit Breaker pattern has a different purpose than the "Retry pattern".</span></span> <span data-ttu-id="c4764-118">Le « modèle Nouvelle tentative » permet à une application de retenter une opération en partant du principe qu’elle finira par réussir.</span><span class="sxs-lookup"><span data-stu-id="c4764-118">The "Retry pattern" enables an application to retry an operation in the expectation that the operation will eventually succeed.</span></span> <span data-ttu-id="c4764-119">Le modèle Disjoncteur empêche une application d’effectuer une opération qui échouera probablement.</span><span class="sxs-lookup"><span data-stu-id="c4764-119">The Circuit Breaker pattern prevents an application from performing an operation that is likely to fail.</span></span> <span data-ttu-id="c4764-120">Une application peut combiner ces deux modèles.</span><span class="sxs-lookup"><span data-stu-id="c4764-120">An application can combine these two patterns.</span></span> <span data-ttu-id="c4764-121">Toutefois, la logique de nouvelle tentative doit être sensible aux exceptions retournées par le disjoncteur et doit abandonner les nouvelles tentatives si le disjoncteur indique qu’une erreur n’est pas temporaire.</span><span class="sxs-lookup"><span data-stu-id="c4764-121">However, the retry logic should be sensitive to any exception returned by the circuit breaker, and it should abandon retry attempts if the circuit breaker indicates that a fault is not transient.</span></span>

## <a name="implement-circuit-breaker-pattern-with-httpclientfactory-and-polly"></a><span data-ttu-id="c4764-122">Implémenter le modèle Disjoncteur avec HttpClientFactory et Polly</span><span class="sxs-lookup"><span data-stu-id="c4764-122">Implement Circuit Breaker pattern with HttpClientFactory and Polly</span></span>

<span data-ttu-id="c4764-123">Comme lors de l’implémentation de nouvelles tentatives, l’approche recommandée pour les disjoncteurs consiste à tirer parti de bibliothèques .NET éprouvées comme Polly et de leur intégration native avec HttpClientFactory.</span><span class="sxs-lookup"><span data-stu-id="c4764-123">As when implementing retries, the recommended approach for circuit breakers is to take advantage of proven .NET libraries like Polly and its native integration with HttpClientFactory.</span></span>

<span data-ttu-id="c4764-124">L’ajout d’une stratégie de disjoncteur dans votre pipeline d’intergiciel (middleware) sortant HttpClientFactory est aussi simple que l’ajout d’un fragment de code incrémentiel individuel à ce que vous avez déjà lorsque vous utilisez HttpClientFactory.</span><span class="sxs-lookup"><span data-stu-id="c4764-124">Adding a circuit breaker policy into your HttpClientFactory outgoing middleware pipeline is as simple as adding a single incremental piece of code to what you already have when using HttpClientFactory.</span></span>

<span data-ttu-id="c4764-125">Ici, le seul ajout au code utilisé pour les nouvelles tentatives d’appel HTTP est le code où vous ajoutez la stratégie Disjoncteur à la liste des stratégies à utiliser, comme indiqué dans le code incrémentiel suivant, inscrit dans la méthode ConfigureServices().</span><span class="sxs-lookup"><span data-stu-id="c4764-125">The only addition here to the code used for HTTP call retries is the code where you add the Circuit Breaker policy to the list of policies to use, as shown in the following incremental code, part of the ConfigureServices() method.</span></span>

```csharp
//ConfigureServices()  - Startup.cs
services.AddHttpClient<IBasketService, BasketService>()
        .SetHandlerLifetime(TimeSpan.FromMinutes(5))  //Set lifetime to 5 minutes
        .AddPolicyHandler(GetRetryPolicy())
        .AddPolicyHandler(GetCircuitBreakerPolicy());
```

<span data-ttu-id="c4764-126">La méthode `AddPolicyHandler()` ajoute des stratégies aux objets HttpClient que vous utiliserez.</span><span class="sxs-lookup"><span data-stu-id="c4764-126">The `AddPolicyHandler()`method is what adds policies to the HttpClient objects you will use.</span></span> <span data-ttu-id="c4764-127">Dans ce cas, elle ajoute une stratégie Polly pour un disjoncteur.</span><span class="sxs-lookup"><span data-stu-id="c4764-127">In this case, it is adding a Polly’s policy for a circuit breaker.</span></span>

<span data-ttu-id="c4764-128">Afin de bénéficier d’une approche plus modulaire, la stratégie Disjoncteur est définie dans une méthode distincte nommée GetCircuitBreakerPolicy(), comme dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="c4764-128">In order to have a more modular approach, the Circuit Breaker Policy is defined in a separate method named GetCircuitBreakerPolicy(), as the following code.</span></span>

```csharp
static IAsyncPolicy<HttpResponseMessage> GetCircuitBreakerPolicy()
{
    return HttpPolicyExtensions
        .HandleTransientHttpError()
        .CircuitBreakerAsync(5, TimeSpan.FromSeconds(30));
}
```

<span data-ttu-id="c4764-129">Dans l’exemple de code ci-dessus, la stratégie Disjoncteur est configurée de manière à rompre ou ouvrir le circuit après cinq exceptions lors des nouvelles tentatives de requêtes Http.</span><span class="sxs-lookup"><span data-stu-id="c4764-129">In the code example above, the circuit breaker policy is configured so it breaks or opens the circuit when there have been five exceptions when retrying the Http requests.</span></span> <span data-ttu-id="c4764-130">Ensuite, la durée de l’arrêt passe à 30 secondes.</span><span class="sxs-lookup"><span data-stu-id="c4764-130">Then, 30 seconds will be the duration or the break.</span></span>

<span data-ttu-id="c4764-131">Les disjoncteurs doivent également être utilisés pour rediriger les demandes vers une infrastructure de secours si vous rencontrez des problèmes dans une ressource particulière déployée dans un environnement autre que l’application cliente ou le service qui effectue l’appel HTTP.</span><span class="sxs-lookup"><span data-stu-id="c4764-131">Circuit breakers should also be used to redirect requests to a fallback infrastructure if you had issues in a particular resource that is deployed in a different environment than the client application or service that is performing the HTTP call.</span></span> <span data-ttu-id="c4764-132">De cette façon, si le centre de données subit une panne qui a un impact uniquement sur vos microservices backend, mais pas sur vos applications clientes, ces dernières peuvent effectuer une redirection vers les services de secours.</span><span class="sxs-lookup"><span data-stu-id="c4764-132">That way, if there is an outage in the datacenter that impacts only your backend microservices but not your client applications, the client applications can redirect to the fallback services.</span></span> <span data-ttu-id="c4764-133">Polly planifie une nouvelle stratégie pour automatiser ce scénario de [stratégie de basculement](https://github.com/App-vNext/Polly/wiki/Polly-Roadmap#failover-policy).</span><span class="sxs-lookup"><span data-stu-id="c4764-133">Polly is planning a new policy to automate this [failover policy](https://github.com/App-vNext/Polly/wiki/Polly-Roadmap#failover-policy) scenario.</span></span> 

<span data-ttu-id="c4764-134">Toutes ces fonctionnalités sont appropriées pour les cas où vous gérez le basculement à partir du code .NET, au lieu qu’il soit géré automatiquement par Azure, avec la transparence des emplacements.</span><span class="sxs-lookup"><span data-stu-id="c4764-134">All those features are for cases where you're managing the failover from within the .NET code, as opposed to having it managed automatically for you by Azure, with location transparency.</span></span> 

<span data-ttu-id="c4764-135">Du point de vue de l’utilisation, lorsque vous utilisez HttpClient, il est inutile d’ajouter quoi que ce soit de nouveau ici, car le code est le même que lors de l’utilisation de HttpClient avec HttpClientFactory, comme indiqué dans les sections précédentes.</span><span class="sxs-lookup"><span data-stu-id="c4764-135">From a usage point of view, when using HttpClient, there’s no need to add anything new here because the code is the same than when using HttpClient with HttpClientFactory, as shown in previous sections.</span></span> 

## <a name="testing-http-retries-and-circuit-breakers-in-eshoponcontainers"></a><span data-ttu-id="c4764-136">Test des disjoncteurs et des nouvelles tentatives Http dans eShopOnContainers</span><span class="sxs-lookup"><span data-stu-id="c4764-136">Testing Http retries and circuit breakers in eShopOnContainers</span></span>


<span data-ttu-id="c4764-137">Chaque fois que vous démarrez la solution eShopOnContainers sur un hôte Docker, celle-ci doit démarrer plusieurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="c4764-137">Whenever you start the eShopOnContainers solution in a Docker host, it needs to start multiple containers.</span></span> <span data-ttu-id="c4764-138">Certains des conteneurs sont plus lents à démarrer et à initialiser, comme le conteneur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c4764-138">Some of the containers are slower to start and initialize, like the SQL Server container.</span></span> <span data-ttu-id="c4764-139">Cela est particulièrement vrai la première fois que vous déployez l’application eShopOnContainers dans Docker, car elle doit configurer les images et la base de données.</span><span class="sxs-lookup"><span data-stu-id="c4764-139">This is especially true the first time you deploy the eShopOnContainers application into Docker, because it needs to set up the images and the database.</span></span> <span data-ttu-id="c4764-140">Le fait que certains conteneurs démarrent plus lentement que d’autres peut entraîner la levée d’exceptions HTTP par le reste des services, même si vous définissez des dépendances entre les conteneurs au niveau de Docker Compose, comme expliqué dans les sections précédentes.</span><span class="sxs-lookup"><span data-stu-id="c4764-140">The fact that some containers start slower than others can cause the rest of the services to initially throw HTTP exceptions, even if you set dependencies between containers at the docker-compose level, as explained in previous sections.</span></span> <span data-ttu-id="c4764-141">Ces dépendances Docker Compose entre les conteneurs sont uniquement au niveau processus.</span><span class="sxs-lookup"><span data-stu-id="c4764-141">Those docker-compose dependencies between containers are just at the process level.</span></span> <span data-ttu-id="c4764-142">Il est possible que le processus de point d’entrée du conteneur soit démarré alors que SQL Server n’est pas prêt pour les requêtes.</span><span class="sxs-lookup"><span data-stu-id="c4764-142">The container’s entry point process might be started, but SQL Server might not be ready for queries.</span></span> <span data-ttu-id="c4764-143">Cela peut avoir pour conséquence une cascade d’erreurs, et l’application peut recevoir une exception lors d’une tentative d’utilisation de ce conteneur particulier.</span><span class="sxs-lookup"><span data-stu-id="c4764-143">The result can be a cascade of errors, and the application can get an exception when trying to consume that particular container.</span></span> 

<span data-ttu-id="c4764-144">Vous pouvez également voir ce type d’erreur au démarrage pendant le déploiement de l’application dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="c4764-144">You might also see this type of error on startup when the application is deploying to the cloud.</span></span> <span data-ttu-id="c4764-145">Dans ce cas, il est possible que les orchestrateurs déplacent des conteneurs d’un nœud ou d’une machine virtuelle vers un autre nœud ou une autre machine virtuelle (autrement dit, de démarrer de nouvelles instances) lors de l’équilibrage du nombre de conteneurs entre les nœuds du cluster.</span><span class="sxs-lookup"><span data-stu-id="c4764-145">In that case, orchestrators might be moving containers from one node or VM to another (that is, starting new instances) when balancing the number of containers across the cluster’s nodes.</span></span>

<span data-ttu-id="c4764-146">La façon dont « eShopOnContainers » résout ces problèmes lors du démarrage de tous les conteneurs consiste à utiliser le modèle de nouvelle tentative illustré précédemment.</span><span class="sxs-lookup"><span data-stu-id="c4764-146">The way 'eShopOnContainers' solves those issues when starting all the containers is by using the Retry pattern illustrated earlier.</span></span> 

### <a name="testing-the-circuit-breaker-in-eshoponcontainers"></a><span data-ttu-id="c4764-147">Test du disjoncteur dans eShopOnContainers</span><span class="sxs-lookup"><span data-stu-id="c4764-147">Testing the circuit breaker in eShopOnContainers</span></span>

<span data-ttu-id="c4764-148">Il existe plusieurs façons de rompre/ouvrir le circuit et de le tester avec eShopOnContainers.</span><span class="sxs-lookup"><span data-stu-id="c4764-148">There are a few ways you can break/open the circuit and test it with eShopOnContainers.</span></span>

<span data-ttu-id="c4764-149">L’une des options consiste à réduire le nombre de tentatives autorisées à 1 dans la stratégie Disjoncteur et à redéployer l’ensemble de la solution dans Docker.</span><span class="sxs-lookup"><span data-stu-id="c4764-149">One option is to lower the allowed number of retries to 1 in the circuit breaker policy and redeploy the whole solution into Docker.</span></span> <span data-ttu-id="c4764-150">Avec une seule nouvelle tentative, il y a de fortes chances qu’une requête HTTP échoue pendant le déploiement, que le disjoncteur s’ouvre et que vous obteniez une erreur.</span><span class="sxs-lookup"><span data-stu-id="c4764-150">With a single retry, there is a good chance that an HTTP request will fail during deployment, the circuit breaker will open, and you get an error.</span></span>

<span data-ttu-id="c4764-151">Une autre option est d’utiliser l’intergiciel (middleware) personnalisé qui est implémenté dans le microservice Basket.</span><span class="sxs-lookup"><span data-stu-id="c4764-151">Another option is to use custom middleware that is implemented in the Basket microservice.</span></span> <span data-ttu-id="c4764-152">Quand ce middleware est activé, il intercepte toutes les requêtes HTTP et retourne le code d’état 500.</span><span class="sxs-lookup"><span data-stu-id="c4764-152">When this middleware is enabled, it catches all HTTP requests and returns status code 500.</span></span> <span data-ttu-id="c4764-153">Vous pouvez activer le middleware en effectuant une requête GET à l’URI qui a échoué, comme suit :</span><span class="sxs-lookup"><span data-stu-id="c4764-153">You can enable the middleware by making a GET request to the failing URI, like the following:</span></span>

- `GET http://localhost:5103/failing`

<span data-ttu-id="c4764-154">Cette requête retourne l’état actuel du middleware.</span><span class="sxs-lookup"><span data-stu-id="c4764-154">This request returns the current state of the middleware.</span></span> <span data-ttu-id="c4764-155">Si le middleware est activé, la requête retourne le code d’état 500.</span><span class="sxs-lookup"><span data-stu-id="c4764-155">If the middleware is enabled, the request return status code 500.</span></span> <span data-ttu-id="c4764-156">Si le middleware est désactivé, il n’y a pas de réponse.</span><span class="sxs-lookup"><span data-stu-id="c4764-156">If the middleware is disabled, there is no response.</span></span> 

- `GET http://localhost:5103/failing?enable`

<span data-ttu-id="c4764-157">Cette requête active le middleware.</span><span class="sxs-lookup"><span data-stu-id="c4764-157">This request enables the middleware.</span></span> 

- `GET http://localhost:5103/failing?disable`

<span data-ttu-id="c4764-158">Cette requête désactive le middleware.</span><span class="sxs-lookup"><span data-stu-id="c4764-158">This request disables the middleware.</span></span> 

<span data-ttu-id="c4764-159">Par exemple, une fois que l’application est en cours d’exécution, vous pouvez activer le middleware en créant une requête à l’aide de l’URI suivant dans n’importe quel navigateur.</span><span class="sxs-lookup"><span data-stu-id="c4764-159">For instance, once the application is running, you can enable the middleware by making a request using the following URI in any browser.</span></span> <span data-ttu-id="c4764-160">Notez que le microservice de commandes utilise le port 5103.</span><span class="sxs-lookup"><span data-stu-id="c4764-160">Note that the ordering microservice uses port 5103.</span></span>

`http://localhost:5103/failing?enable` 

<span data-ttu-id="c4764-161">Vous pouvez alors vérifier l’état à l’aide de l’URI http://localhost:5103/failing, comme illustré à la figure 10-4.</span><span class="sxs-lookup"><span data-stu-id="c4764-161">You can then check the status using the URI http://localhost:5103/failing, as shown in Figure 10-4.</span></span>

![](./media/image4.png)

<span data-ttu-id="c4764-162">**Figure 10-4**.</span><span class="sxs-lookup"><span data-stu-id="c4764-162">**Figure 10-4**.</span></span> <span data-ttu-id="c4764-163">Vérification de l’état du middleware ASP.NET (désactivé dans le cas présent) « Failing » (En échec).</span><span class="sxs-lookup"><span data-stu-id="c4764-163">Checking the state of the “Failing” ASP.NET middleware – In this case, disabled.</span></span> 

<span data-ttu-id="c4764-164">À ce stade, le microservice Basket répond avec le code d’état 500 chaque fois que vous l’appelez.</span><span class="sxs-lookup"><span data-stu-id="c4764-164">At this point, the Basket microservice responds with status code 500 whenever you call invoke it.</span></span>

<span data-ttu-id="c4764-165">Une fois que le middleware est en cours d’exécution, vous pouvez essayer d’effectuer une commande à partir de l’application web MVC.</span><span class="sxs-lookup"><span data-stu-id="c4764-165">Once the middleware is running, you can try making an order from the MVC web application.</span></span> <span data-ttu-id="c4764-166">Étant donné que les requêtes échouent, le circuit s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="c4764-166">Because the requests fail, the circuit will open.</span></span> 

<span data-ttu-id="c4764-167">Dans l’exemple suivant, vous pouvez voir que l’application web MVC a un bloc catch dans la logique du processus consistant à passer une commande.</span><span class="sxs-lookup"><span data-stu-id="c4764-167">In the following example, you can see that the MVC web application has a catch block in the logic for placing an order.</span></span>  <span data-ttu-id="c4764-168">Si le code intercepte une exception de circuit ouvert, il affiche à l’utilisateur un message convivial l’invitant à patienter.</span><span class="sxs-lookup"><span data-stu-id="c4764-168">If the code catches an open-circuit exception, it shows the user a friendly message telling them to wait.</span></span>

```csharp
public class CartController : Controller
{
    //…
    public async Task<IActionResult> Index()
    {
        try
        {          
            var user = _appUserParser.Parse(HttpContext.User);
            //Http requests using the Typed Client (Service Agent)
            var vm = await _basketSvc.GetBasket(user);
            return View(vm);
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

<span data-ttu-id="c4764-169">Voici un résumé.</span><span class="sxs-lookup"><span data-stu-id="c4764-169">Here’s a summary.</span></span> <span data-ttu-id="c4764-170">La stratégie Nouvelle tentative tente plusieurs fois d’exécuter la requête HTTP et obtient des erreurs HTTP.</span><span class="sxs-lookup"><span data-stu-id="c4764-170">The Retry policy tries several times to make the HTTP request and gets HTTP errors.</span></span> <span data-ttu-id="c4764-171">Quand le nombre maximal de nouvelles tentatives pour la stratégie Disjoncteur est atteint (dans le cas présent, 5), l’application lève une exception BrokenCircuitException.</span><span class="sxs-lookup"><span data-stu-id="c4764-171">When the number of retries reaches the maximum number set for the Circuit Breaker policy (in this case, 5), the application throws a BrokenCircuitException.</span></span> <span data-ttu-id="c4764-172">Le résultat est un message convivial, comme illustré dans la figure 10-5.</span><span class="sxs-lookup"><span data-stu-id="c4764-172">The result is a friendly message, as shown in Figure 10-5.</span></span>

![](./media/image5.png)

<span data-ttu-id="c4764-173">**Figure 10-5**.</span><span class="sxs-lookup"><span data-stu-id="c4764-173">**Figure 10-5**.</span></span> <span data-ttu-id="c4764-174">Disjoncteur retournant une erreur à l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="c4764-174">Circuit breaker returning an error to the UI</span></span>

<span data-ttu-id="c4764-175">Vous pouvez implémenter une logique différente pour déterminer quand ouvrir/rompre le circuit.</span><span class="sxs-lookup"><span data-stu-id="c4764-175">You can implement different logic for when to open/break the circuit.</span></span> <span data-ttu-id="c4764-176">Vous pouvez également essayer une requête HTTP sur un autre microservice backend s’il existe un centre de données de secours ou un système backend redondant.</span><span class="sxs-lookup"><span data-stu-id="c4764-176">Or you can try an HTTP request against a different back-end microservice if there is a fallback datacenter or redundant back-end system.</span></span> 

<span data-ttu-id="c4764-177">Enfin, une autre solution pour la stratégie `CircuitBreakerPolicy` consiste à utiliser `Isolate` (qui force l’ouverture du circuit et le maintient ouvert) et `Reset` (qui le referme).</span><span class="sxs-lookup"><span data-stu-id="c4764-177">Finally, another possibility for the `CircuitBreakerPolicy` is to use `Isolate` (which forces open and holds open the circuit) and `Reset` (which closes it again).</span></span> <span data-ttu-id="c4764-178">Ces solutions peuvent être utilisées pour créer un point de terminaison HTTP d’utilitaire qui appelle Isolate et Reset directement sur la stratégie.</span><span class="sxs-lookup"><span data-stu-id="c4764-178">These could be used to build a utility HTTP endpoint that invokes Isolate and Reset directly on the policy.</span></span>  <span data-ttu-id="c4764-179">Un tel point de terminaison HTTP peut également être utilisé, correctement sécurisé, en production pour l’isolation temporaire d’un système en aval, par exemple quand vous voulez procéder à sa mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="c4764-179">Such an HTTP endpoint could also be used, suitably secured, in production for temporarily isolating a downstream system, such as when you want to upgrade it.</span></span> <span data-ttu-id="c4764-180">Ou bien il peut déclencher le circuit manuellement pour protéger un système en aval que vous soupçonnez d’avoir provoqué l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c4764-180">Or it could trip the circuit manually to protect a downstream system you suspect to be faulting.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="c4764-181">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="c4764-181">Additional resources</span></span>


-   <span data-ttu-id="c4764-182">**Modèle Disjoncteur**
    [*https://docs.microsoft.com/azure/architecture/patterns/circuit-breaker*](https://docs.microsoft.com/azure/architecture/patterns/circuit-breaker)</span><span class="sxs-lookup"><span data-stu-id="c4764-182">**Circuit Breaker pattern**
[*https://docs.microsoft.com/azure/architecture/patterns/circuit-breaker*](https://docs.microsoft.com/azure/architecture/patterns/circuit-breaker)</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="c4764-183">[Précédent](implement-http-call-retries-exponential-backoff-polly.md)
[Suivant](monitor-app-health.md)</span><span class="sxs-lookup"><span data-stu-id="c4764-183">[Previous](implement-http-call-retries-exponential-backoff-polly.md)
[Next](monitor-app-health.md)</span></span>
