---
title: Implémentation de nouvelles tentatives d’appel HTTP avec interruption exponentielle avec Polly
description: Architecture des microservices .NET pour les applications .NET en conteneur | Implémentation de nouvelles tentatives d’appel HTTP avec interruption exponentielle avec Polly
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: cce1392bb381859e7cad89c9f2518113241ae724
ms.sourcegitcommit: 979597cd8055534b63d2c6ee8322938a27d0c87b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37106929"
---
# <a name="implementing-http-call-retries-with-exponential-backoff-with-polly"></a><span data-ttu-id="c084f-103">Implémentation de nouvelles tentatives d’appel HTTP avec interruption exponentielle avec Polly</span><span class="sxs-lookup"><span data-stu-id="c084f-103">Implementing HTTP call retries with exponential backoff with Polly</span></span>

<span data-ttu-id="c084f-104">L’approche recommandée pour les nouvelles tentatives avec interruption exponentielle est d’utiliser des bibliothèques .NET plus avancées telles que la bibliothèque open source [Polly](https://github.com/App-vNext/Polly).</span><span class="sxs-lookup"><span data-stu-id="c084f-104">The recommended approach for retries with exponential backoff is to take advantage of more advanced .NET libraries like the open source [Polly](https://github.com/App-vNext/Polly) library.</span></span>

<span data-ttu-id="c084f-105">Polly est une bibliothèque .NET qui fournit des fonctionnalités de résilience et de gestion des erreurs temporaires.</span><span class="sxs-lookup"><span data-stu-id="c084f-105">Polly is a .NET library that provides resilience and transient-fault handling capabilities.</span></span> <span data-ttu-id="c084f-106">Vous pouvez facilement implémenter ces fonctionnalités en appliquant des stratégies Polly comme Retry, Circuit Breaker, Bulkhead Isolation, Timeout et Fallback.</span><span class="sxs-lookup"><span data-stu-id="c084f-106">You can implement those capabilities easily by applying Polly policies such as Retry, Circuit Breaker, Bulkhead Isolation, Timeout, and Fallback.</span></span> <span data-ttu-id="c084f-107">Polly cible .NET 4.x et .NET Standard version 1.0 (qui prend en charge .NET Core).</span><span class="sxs-lookup"><span data-stu-id="c084f-107">Polly targets .NET 4.x and the .NET Standard version 1.0 (which supports .NET Core).</span></span>

<span data-ttu-id="c084f-108">La stratégie Retry de Polly est l’approche utilisée dans eShopOnContainers pour implémenter de nouvelles tentatives HTTP.</span><span class="sxs-lookup"><span data-stu-id="c084f-108">The Retry policy in Polly is the approach used in eShopOnContainers when implementing HTTP retries.</span></span> <span data-ttu-id="c084f-109">Vous pouvez implémenter une interface pour injecter une fonctionnalité HttpClient standard ou une version résiliente de HttpClient avec Polly, en fonction de la configuration de la stratégie de nouvelles tentatives que vous souhaitez appliquer.</span><span class="sxs-lookup"><span data-stu-id="c084f-109">You can implement an interface so you can inject either standard HttpClient functionality or a resilient version of HttpClient using Polly, depending on what retry policy configuration you want to use.</span></span>

<span data-ttu-id="c084f-110">L’exemple suivant montre l’interface implémentée dans eShopOnContainers.</span><span class="sxs-lookup"><span data-stu-id="c084f-110">The following example shows the interface implemented in eShopOnContainers.</span></span>

```csharp
public interface IHttpClient
{
    Task<string> GetStringAsync(string uri, string authorizationToken = null,
        string authorizationMethod = "Bearer");
        Task<HttpResponseMessage> PostAsync<T>(string uri, T item,
        string authorizationToken = null, string requestId = null,
        string authorizationMethod = "Bearer");

    Task<HttpResponseMessage> DeleteAsync(string uri,
        string authorizationToken = null, string requestId = null,
        string authorizationMethod = "Bearer");

    // Other methods ...
}
```

<span data-ttu-id="c084f-111">Vous pouvez choisir l’implémentation standard si vous n’avez pas besoin de mécanisme résilient, comme c’est le cas lorsque vous développez ou testez des approches plus simples.</span><span class="sxs-lookup"><span data-stu-id="c084f-111">You can use the standard implementation if you do not want to use a resilient mechanism, as when you are developing or testing simpler approaches.</span></span> <span data-ttu-id="c084f-112">Le code suivant montre un cas possible d’implémentation HttpClient standard qui autorise les requêtes avec des jetons d’authentification.</span><span class="sxs-lookup"><span data-stu-id="c084f-112">The following code shows the standard HttpClient implementation allowing requests with authentication tokens as an optional case.</span></span>

```csharp
public class StandardHttpClient : IHttpClient
{
    private HttpClient _client;
    private ILogger<StandardHttpClient> _logger;

    public StandardHttpClient(ILogger<StandardHttpClient> logger)
    {
        _client = new HttpClient();
        _logger = logger;
    }

    public async Task<string> GetStringAsync(string uri,
        string authorizationToken = null,
        string authorizationMethod = "Bearer")
    {
        var requestMessage = new HttpRequestMessage(HttpMethod.Get, uri);
        if (authorizationToken != null)
        {
            requestMessage.Headers.Authorization =
                new AuthenticationHeaderValue(authorizationMethod, authorizationToken);
        }
        var response = await _client.SendAsync(requestMessage);
        return await response.Content.ReadAsStringAsync();
    }

    public async Task<HttpResponseMessage> PostAsync<T>(string uri, T item,
        string authorizationToken = null, string requestId = null,
        string authorizationMethod = "Bearer")
    {
        // Rest of the code and other Http methods ...
```

<span data-ttu-id="c084f-113">Une implémentation intéressante consiste à coder une autre classe similaire, mais en utilisant Polly pour implémenter les mécanismes résilients que vous souhaitez utiliser, comme les nouvelles tentatives avec interruption exponentielle dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="c084f-113">The interesting implementation is to code another, similar class, but using Polly to implement the resilient mechanisms you want to use—in the following example, retries with exponential backoff.</span></span>

```csharp
public class ResilientHttpClient : IHttpClient
{
    private HttpClient _client;
    private PolicyWrap _policyWrapper;
    private ILogger<ResilientHttpClient> _logger;

    public ResilientHttpClient(Policy[] policies,
        ILogger<ResilientHttpClient> logger)
    {
        _client = new HttpClient();
        _logger = logger;
        // Add Policies to be applied
        _policyWrapper = Policy.WrapAsync(policies);
    }

    private Task<T> HttpInvoker<T>(Func<Task<T>> action)
    {
        // Executes the action applying all
        // the policies defined in the wrapper
        return _policyWrapper.ExecuteAsync(() => action());
    }

    public Task<string> GetStringAsync(string uri,
        string authorizationToken = null,
        string authorizationMethod = "Bearer")
    {
        return HttpInvoker(async () =>
        {
            var requestMessage = new HttpRequestMessage(HttpMethod.Get, uri);
            // The Token's related code eliminated for clarity in code snippet
            var response = await _client.SendAsync(requestMessage);
            return await response.Content.ReadAsStringAsync();
        });
    }
    // Other Http methods executed through HttpInvoker so it applies Polly policies
    // ...
}
```

<span data-ttu-id="c084f-114">Avec Polly, vous définissez une stratégie Retry en spécifiant le nombre de nouvelles tentatives, la configuration de l’interruption exponentielle et les actions à effectuer quand une exception HTTP se produit (par exemple, journaliser l’erreur).</span><span class="sxs-lookup"><span data-stu-id="c084f-114">With Polly, you define a Retry policy with the number of retries, the exponential backoff configuration, and the actions to take when there is an HTTP exception, such as logging the error.</span></span> <span data-ttu-id="c084f-115">Dans ce cas, la stratégie est configurée pour effectuer le nombre de tentatives spécifié lors de l’inscription des types dans le conteneur loC.</span><span class="sxs-lookup"><span data-stu-id="c084f-115">In this case, the policy is configured so it will try the number of times specified when registering the types in the IoC container.</span></span> <span data-ttu-id="c084f-116">Du fait de la configuration de l’interruption exponentielle, chaque fois que le code détecte une exception HttpRequest, il retente la requête Http après un temps d’attente qui augmente de façon exponentielle selon ce qui a été configuré dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="c084f-116">Because of the exponential backoff configuration, whenever the code detects an HttpRequest exception, it retries the Http request after waiting an amount of time that increases exponentially depending on how the policy was configured.</span></span>

<span data-ttu-id="c084f-117">La méthode importante est HttpInvoker, qui traite les requêtes HTTP dans toute cette classe utilitaire.</span><span class="sxs-lookup"><span data-stu-id="c084f-117">The important method is HttpInvoker, which is what makes HTTP requests throughout this utility class.</span></span> <span data-ttu-id="c084f-118">Cette méthode exécute en interne la requête HTTP avec \_policyWrapper.ExecuteAsync, qui applique la stratégie de nouvelles tentatives.</span><span class="sxs-lookup"><span data-stu-id="c084f-118">That method internally executes the HTTP request with \_policyWrapper.ExecuteAsync, which takes into account the retry policy.</span></span>

<span data-ttu-id="c084f-119">Dans eShopOnContainers, vous spécifiez les stratégies Polly au moment de l’inscription des types dans le conteneur IoC, comme dans le code suivant de l’[application web MVC pour la classe startup.cs](https://github.com/dotnet-architecture/eShopOnContainers/blob/master/src/Web/WebMVC/Startup.cs).</span><span class="sxs-lookup"><span data-stu-id="c084f-119">In eShopOnContainers you specify Polly policies when registering the types at the IoC container, as in the following code from the [MVC web app at the startup.cs](https://github.com/dotnet-architecture/eShopOnContainers/blob/master/src/Web/WebMVC/Startup.cs) class.</span></span>

```csharp
// Startup.cs class
if (Configuration.GetValue<string>("UseResilientHttp") == bool.TrueString)
{
    services.AddTransient<IResilientHttpClientFactory,
        ResilientHttpClientFactory>();
    services.AddSingleton<IHttpClient,
        ResilientHttpClient>(sp =>
            sp.GetService<IResilientHttpClientFactory>().
            CreateResilientHttpClient());
}
else
{
    services.AddSingleton<IHttpClient, StandardHttpClient>();
}
```

<span data-ttu-id="c084f-120">Notez que les objets IHttpClient sont instanciés en tant qu’objets singleton au lieu d’objets transitoires pour que les connexions TCP soient utilisées efficacement par le service et que cela ne génère pas de [problème avec les sockets](https://aspnetmonsters.com/2016/08/2016-08-27-httpclientwrong/).</span><span class="sxs-lookup"><span data-stu-id="c084f-120">Note that the IHttpClient objects are instantiated as singleton instead of as transient so that TCP connections are used efficiently by the service and [an issue with sockets](https://aspnetmonsters.com/2016/08/2016-08-27-httpclientwrong/) will not occur.</span></span>

<span data-ttu-id="c084f-121">Cependant, le point important à retenir sur la résilience est que vous appliquez la stratégie WaitAndRetryAsync de Polly dans ResilientHttpClientFactory dans la méthode CreateResilientHttpClient, comme illustré dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="c084f-121">But the important point about resiliency is that you apply the Polly WaitAndRetryAsync policy within ResilientHttpClientFactory in the CreateResilientHttpClient method, as shown in the following code:</span></span>

```csharp
public ResilientHttpClient CreateResilientHttpClient()
    => new ResilientHttpClient(CreatePolicies(), _logger);

// Other code
private Policy[] CreatePolicies()
    => new Policy[]
    {
        Policy.Handle<HttpRequestException>()
            .WaitAndRetryAsync(
        // number of retries
        6,
        // exponential backoff
        retryAttempt => TimeSpan.FromSeconds(Math.Pow(2, retryAttempt)),
        // on retry
        (exception, timeSpan, retryCount, context) =>
        {
            var msg = $"Retry {retryCount} implemented with Pollys RetryPolicy " +
            $"of {context.PolicyKey} " +
            $"at {context.ExecutionKey}, " +
            $"due to: {exception}.";
            _logger.LogWarning(msg);
            _logger.LogDebug(msg);
        }),
    }
```


>[!div class="step-by-step"]
<span data-ttu-id="c084f-122">[Précédent](implement-custom-http-call-retries-exponential-backoff.md)
[Suivant](implement-circuit-breaker-pattern.md)</span><span class="sxs-lookup"><span data-stu-id="c084f-122">[Previous](implement-custom-http-call-retries-exponential-backoff.md)
[Next](implement-circuit-breaker-pattern.md)</span></span>
