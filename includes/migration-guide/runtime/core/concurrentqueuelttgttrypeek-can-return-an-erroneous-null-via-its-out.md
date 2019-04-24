---
ms.openlocfilehash: a93fbbd787aa50f080337a6170cf8f56d0d24e31
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803869"
---
### <a name="concurrentqueuettrypeek-can-return-an-erroneous-null-via-its-out-parameter"></a><span data-ttu-id="77d3b-101">ConcurrentQueue\<T>.TryPeek risque de retourner une valeur Null erronée dans son paramètre de sortie</span><span class="sxs-lookup"><span data-stu-id="77d3b-101">ConcurrentQueue\<T>.TryPeek can return an erroneous null via its out parameter</span></span>

|   |   |
|---|---|
|<span data-ttu-id="77d3b-102">Détails</span><span class="sxs-lookup"><span data-stu-id="77d3b-102">Details</span></span>|<span data-ttu-id="77d3b-103">Dans certains scénarios multithreads, <xref:System.Collections.Concurrent.ConcurrentQueue%601.TryPeek(%600@)?displayProperty=name> peut retourner la valeur true, mais renseigner le paramètre de sortie avec la valeur Null (au lieu de la valeur correcte).</span><span class="sxs-lookup"><span data-stu-id="77d3b-103">In some multi-threaded scenarios, <xref:System.Collections.Concurrent.ConcurrentQueue%601.TryPeek(%600@)?displayProperty=name> can return true, but populate the out parameter with a null value (instead of the correct, peeked value).</span></span>|
|<span data-ttu-id="77d3b-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="77d3b-104">Suggestion</span></span>|<span data-ttu-id="77d3b-105">Ce problème a été résolu dans le .NET Framework 4.5.1.</span><span class="sxs-lookup"><span data-stu-id="77d3b-105">This issue is fixed in the .NET Framework 4.5.1.</span></span> <span data-ttu-id="77d3b-106">Pour résoudre votre problème, effectuez une mise niveau vers le .NET Framework 4.5.1.</span><span class="sxs-lookup"><span data-stu-id="77d3b-106">Upgrading to that Framework will solve the issue.</span></span>|
|<span data-ttu-id="77d3b-107">Portée</span><span class="sxs-lookup"><span data-stu-id="77d3b-107">Scope</span></span>|<span data-ttu-id="77d3b-108">Majeur</span><span class="sxs-lookup"><span data-stu-id="77d3b-108">Major</span></span>|
|<span data-ttu-id="77d3b-109">Version</span><span class="sxs-lookup"><span data-stu-id="77d3b-109">Version</span></span>|<span data-ttu-id="77d3b-110">4.5</span><span class="sxs-lookup"><span data-stu-id="77d3b-110">4.5</span></span>|
|<span data-ttu-id="77d3b-111">Type</span><span class="sxs-lookup"><span data-stu-id="77d3b-111">Type</span></span>|<span data-ttu-id="77d3b-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="77d3b-112">Runtime</span></span>|
|<span data-ttu-id="77d3b-113">API affectées</span><span class="sxs-lookup"><span data-stu-id="77d3b-113">Affected APIs</span></span>|<ul><li><xref:System.Collections.Concurrent.ConcurrentQueue%601.TryPeek(%600@)?displayProperty=nameWithType></li></ul>|
