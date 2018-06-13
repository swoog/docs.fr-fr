---
title: Implémentation de nouvelles tentatives d’appel HTTP personnalisées avec interruption exponentielle
description: Architecture des microservices .NET pour les applications .NET en conteneur | Implémentation de nouvelles tentatives d’appel HTTP personnalisées avec interruption exponentielle
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: 10751bb74ed648839fabec67ff7a71e458fb2a44
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33574944"
---
# <a name="implementing-custom-http-call-retries-with-exponential-backoff"></a><span data-ttu-id="e1502-103">Implémentation de nouvelles tentatives d’appel HTTP personnalisées avec interruption exponentielle</span><span class="sxs-lookup"><span data-stu-id="e1502-103">Implementing custom HTTP call retries with exponential backoff</span></span>

<span data-ttu-id="e1502-104">Pour créer des microservices résilients, vous devez prévoir des mécanismes de gestion des scénarios possibles de défaillance HTTP.</span><span class="sxs-lookup"><span data-stu-id="e1502-104">In order to create resilient microservices, you need to handle possible HTTP failure scenarios.</span></span> <span data-ttu-id="e1502-105">Pour cela, vous pouvez créer votre propre implémentation de nouvelles tentatives avec interruption exponentielle.</span><span class="sxs-lookup"><span data-stu-id="e1502-105">For that purpose, you could create your own implementation of retries with exponential backoff.</span></span>

<span data-ttu-id="e1502-106">En plus de gérer l’indisponibilité temporelle des ressources, l’interruption exponentielle doit également prendre en compte le fait que le fournisseur de cloud peut limiter la disponibilité des ressources afin d’éviter une surcharge d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="e1502-106">In addition to handling temporal resource unavailability, the exponential backoff also needs to take into account that the cloud provider might throttle availability of resources to prevent usage overload.</span></span> <span data-ttu-id="e1502-107">Par exemple, l’envoi coup sur coup d’un trop grand nombre de requêtes de connexion peut être considéré comme une attaque par déni de service ([DoS](https://en.wikipedia.org/wiki/Denial-of-service_attack)) par le fournisseur de cloud.</span><span class="sxs-lookup"><span data-stu-id="e1502-107">For example, creating too many connection requests very quickly might be viewed as a Denial of Service ([DoS](https://en.wikipedia.org/wiki/Denial-of-service_attack)) attack by the cloud provider.</span></span> <span data-ttu-id="e1502-108">Vous devez donc fournir un mécanisme de réduction des requêtes de connexion quand un seuil de capacité a été atteint.</span><span class="sxs-lookup"><span data-stu-id="e1502-108">As a result, you need to provide a mechanism to scale back connection requests when a capacity threshold has been encountered.</span></span>

<span data-ttu-id="e1502-109">Pour commencer, vous pouvez implémenter votre propre code avec une classe utilitaire pour l’interruption exponentielle comme dans [RetryWithExponentialBackoff.cs](https://gist.github.com/CESARDELATORRE/6d7f647b29e55fdc219ee1fd2babb260), et implémenter du code similaire à l’exemple ci-dessous (qui est également disponible dans un [dépôt GitHub](https://gist.github.com/CESARDELATORRE/d80c6423a1aebaffaf387469f5194f5b)).</span><span class="sxs-lookup"><span data-stu-id="e1502-109">As an initial exploration, you could implement your own code with a utility class for exponential backoff as in [RetryWithExponentialBackoff.cs](https://gist.github.com/CESARDELATORRE/6d7f647b29e55fdc219ee1fd2babb260), plus code like the following (which is also available on a [GitHub repo](https://gist.github.com/CESARDELATORRE/d80c6423a1aebaffaf387469f5194f5b)).</span></span>

```csharp
public sealed class RetryWithExponentialBackoff
{
    private readonly int maxRetries, delayMilliseconds, maxDelayMilliseconds;

    public RetryWithExponentialBackoff(int maxRetries = 50,
        int delayMilliseconds = 200,
        int maxDelayMilliseconds = 2000)
    {
        this.maxRetries = maxRetries;
        this.delayMilliseconds = delayMilliseconds;
        this.maxDelayMilliseconds = maxDelayMilliseconds;
    }

    public async Task RunAsync(Func<Task> func)
    {
        ExponentialBackoff backoff = new ExponentialBackoff(this.maxRetries,
            this.delayMilliseconds,
            this.maxDelayMilliseconds);
        retry:
        try
        {
            await func();
        }
        catch (Exception ex) when (ex is TimeoutException ||
            ex is System.Net.Http.HttpRequestException)
        {
            Debug.WriteLine("Exception raised is: " +
                ex.GetType().ToString() +
                " –Message: " + ex.Message +
                " -- Inner Message: " +
                ex.InnerException.Message);
            await backoff.Delay();
            goto retry;
        }
    }
}

public struct ExponentialBackoff
{
    private readonly int m_maxRetries, m_delayMilliseconds, m_maxDelayMilliseconds;
    private int m_retries, m_pow;

    public ExponentialBackoff(int maxRetries, int delayMilliseconds,
        int maxDelayMilliseconds)
    {
        m_maxRetries = maxRetries;
        m_delayMilliseconds = delayMilliseconds;
        m_maxDelayMilliseconds = maxDelayMilliseconds;
        m_retries = 0;
        m_pow = 1;
    }

    public Task Delay()
    {
        if (m_retries == m_maxRetries)
        {
            throw new TimeoutException("Max retry attempts exceeded.");
        }
        ++m_retries;
        if (m_retries < 31)
        {
            m_pow = m_pow << 1; // m_pow = Pow(2, m_retries - 1)
        }
        int delay = Math.Min(m_delayMilliseconds * (m_pow - 1) / 2,
            m_maxDelayMilliseconds);
        return Task.Delay(delay);
    }
}
```

<span data-ttu-id="e1502-110">L’utilisation de ce code dans une application C\# cliente (un autre microservice client d’API web, une application ASP.NET MVC ou même une application Xamarin C\#) est simple.</span><span class="sxs-lookup"><span data-stu-id="e1502-110">Using this code in a client C\# application (another Web API client microservice, an ASP.NET MVC application, or even a C\# Xamarin application) is straightforward.</span></span> <span data-ttu-id="e1502-111">L’exemple suivant montre comment implémenter ce code à l’aide de la classe HttpClient.</span><span class="sxs-lookup"><span data-stu-id="e1502-111">The following example shows how, using the HttpClient class.</span></span>

```csharp
public async Task<Catalog> GetCatalogItems(int page,int take, int? brand, int? type)
{
    _apiClient = new HttpClient();
    var itemsQs = $"items?pageIndex={page}&pageSize={take}";
    var filterQs = "";
    var catalogUrl = $"{_remoteServiceBaseUrl}items{filterQs}?pageIndex={page}&pageSize={take}";
    var dataString = "";
    //
    // Using HttpClient with Retry and Exponential Backoff
    //
    var retry = new RetryWithExponentialBackoff();
    await retry.RunAsync(async () =>
    {
        // work with HttpClient call
        dataString = await _apiClient.GetStringAsync(catalogUrl);
    });
    return JsonConvert.DeserializeObject<Catalog>(dataString);
}
```

<span data-ttu-id="e1502-112">Toutefois, ce code est approprié uniquement comme preuve de concept.</span><span class="sxs-lookup"><span data-stu-id="e1502-112">However, this code is suitable only as a proof of concept.</span></span> <span data-ttu-id="e1502-113">La rubrique suivante explique comment utiliser des bibliothèques plus avancées et éprouvées.</span><span class="sxs-lookup"><span data-stu-id="e1502-113">The next topic explains how to use more sophisticated and proven libraries.</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="e1502-114">[Previous] (implement-resilient-entity-framework-core-sql-connections.md) [Next] (implement-http-call-retries-exponential-backoff-polly.md)</span><span class="sxs-lookup"><span data-stu-id="e1502-114">[Previous] (implement-resilient-entity-framework-core-sql-connections.md) [Next] (implement-http-call-retries-exponential-backoff-polly.md)</span></span>
