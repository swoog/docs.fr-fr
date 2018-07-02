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
# <a name="implementing-http-call-retries-with-exponential-backoff-with-polly"></a>Implémentation de nouvelles tentatives d’appel HTTP avec interruption exponentielle avec Polly

L’approche recommandée pour les nouvelles tentatives avec interruption exponentielle est d’utiliser des bibliothèques .NET plus avancées telles que la bibliothèque open source [Polly](https://github.com/App-vNext/Polly).

Polly est une bibliothèque .NET qui fournit des fonctionnalités de résilience et de gestion des erreurs temporaires. Vous pouvez facilement implémenter ces fonctionnalités en appliquant des stratégies Polly comme Retry, Circuit Breaker, Bulkhead Isolation, Timeout et Fallback. Polly cible .NET 4.x et .NET Standard version 1.0 (qui prend en charge .NET Core).

La stratégie Retry de Polly est l’approche utilisée dans eShopOnContainers pour implémenter de nouvelles tentatives HTTP. Vous pouvez implémenter une interface pour injecter une fonctionnalité HttpClient standard ou une version résiliente de HttpClient avec Polly, en fonction de la configuration de la stratégie de nouvelles tentatives que vous souhaitez appliquer.

L’exemple suivant montre l’interface implémentée dans eShopOnContainers.

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

Vous pouvez choisir l’implémentation standard si vous n’avez pas besoin de mécanisme résilient, comme c’est le cas lorsque vous développez ou testez des approches plus simples. Le code suivant montre un cas possible d’implémentation HttpClient standard qui autorise les requêtes avec des jetons d’authentification.

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

Une implémentation intéressante consiste à coder une autre classe similaire, mais en utilisant Polly pour implémenter les mécanismes résilients que vous souhaitez utiliser, comme les nouvelles tentatives avec interruption exponentielle dans l’exemple suivant.

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

Avec Polly, vous définissez une stratégie Retry en spécifiant le nombre de nouvelles tentatives, la configuration de l’interruption exponentielle et les actions à effectuer quand une exception HTTP se produit (par exemple, journaliser l’erreur). Dans ce cas, la stratégie est configurée pour effectuer le nombre de tentatives spécifié lors de l’inscription des types dans le conteneur loC. Du fait de la configuration de l’interruption exponentielle, chaque fois que le code détecte une exception HttpRequest, il retente la requête Http après un temps d’attente qui augmente de façon exponentielle selon ce qui a été configuré dans la stratégie.

La méthode importante est HttpInvoker, qui traite les requêtes HTTP dans toute cette classe utilitaire. Cette méthode exécute en interne la requête HTTP avec \_policyWrapper.ExecuteAsync, qui applique la stratégie de nouvelles tentatives.

Dans eShopOnContainers, vous spécifiez les stratégies Polly au moment de l’inscription des types dans le conteneur IoC, comme dans le code suivant de l’[application web MVC pour la classe startup.cs](https://github.com/dotnet-architecture/eShopOnContainers/blob/master/src/Web/WebMVC/Startup.cs).

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

Notez que les objets IHttpClient sont instanciés en tant qu’objets singleton au lieu d’objets transitoires pour que les connexions TCP soient utilisées efficacement par le service et que cela ne génère pas de [problème avec les sockets](https://aspnetmonsters.com/2016/08/2016-08-27-httpclientwrong/).

Cependant, le point important à retenir sur la résilience est que vous appliquez la stratégie WaitAndRetryAsync de Polly dans ResilientHttpClientFactory dans la méthode CreateResilientHttpClient, comme illustré dans le code suivant :

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
[Précédent](implement-custom-http-call-retries-exponential-backoff.md)
[Suivant](implement-circuit-breaker-pattern.md)
