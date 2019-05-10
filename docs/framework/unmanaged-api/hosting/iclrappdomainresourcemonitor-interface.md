---
title: ICLRAppDomainResourceMonitor, interface
ms.date: 03/30/2017
api_name:
- ICLRAppDomainResourceMonitor
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAppDomainResourceMonitor
helpviewer_keywords:
- ICLRAppDomainResourceMonitor interface [.NET Framework hosting]
ms.assetid: 72fa83a1-8997-41d7-b355-ab177a24a303
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f336ac45e4bf5894c667412ff89acde4b9524c80
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64666066"
---
# <a name="iclrappdomainresourcemonitor-interface"></a><span data-ttu-id="dea8f-102">ICLRAppDomainResourceMonitor, interface</span><span class="sxs-lookup"><span data-stu-id="dea8f-102">ICLRAppDomainResourceMonitor Interface</span></span>
<span data-ttu-id="dea8f-103">Fournit des méthodes qui inspectent la mémoire et l’utilisation du processeur d’un domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="dea8f-103">Provides methods that inspect an application domain's memory and CPU usage.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="dea8f-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dea8f-104">Methods</span></span>  
  
|<span data-ttu-id="dea8f-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="dea8f-105">Method</span></span>|<span data-ttu-id="dea8f-106">Description</span><span class="sxs-lookup"><span data-stu-id="dea8f-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="dea8f-107">GetCurrentAllocated, méthode</span><span class="sxs-lookup"><span data-stu-id="dea8f-107">GetCurrentAllocated Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrappdomainresourcemonitor-getcurrentallocated-method.md)|<span data-ttu-id="dea8f-108">Obtient la taille totale, en octets, de toutes les allocations de mémoire qui ont été apportées par le domaine d’application depuis sa création, sans soustraire la mémoire qui a été le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="dea8f-108">Gets the total size, in bytes, of all memory allocations that have been made by the application domain since it was created, without subtracting memory that has been garbage-collected.</span></span>|  
|[<span data-ttu-id="dea8f-109">GetCurrentSurvived, méthode</span><span class="sxs-lookup"><span data-stu-id="dea8f-109">GetCurrentSurvived Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrappdomainresourcemonitor-getcurrentsurvived-method.md)|<span data-ttu-id="dea8f-110">Obtient le nombre d’octets qui ont survécu à la dernière complète, le garbage collection de blocage et qui sont référencés par le domaine d’application actuel.</span><span class="sxs-lookup"><span data-stu-id="dea8f-110">Gets the number of bytes that survived the last full, blocking garbage collection and that are referenced by the current application domain.</span></span>|  
|[<span data-ttu-id="dea8f-111">GetCurrentCpuTime, méthode</span><span class="sxs-lookup"><span data-stu-id="dea8f-111">GetCurrentCpuTime Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrappdomainresourcemonitor-getcurrentcputime-method.md)|<span data-ttu-id="dea8f-112">Obtient le temps processeur total utilisé par tous les threads lors de l’exécution dans le domaine d’application actuel, dans la mesure où le domaine d’application a été créé.</span><span class="sxs-lookup"><span data-stu-id="dea8f-112">Gets the total processor time that has been used by all threads while executing in the current application domain, since the application domain was created.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dea8f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="dea8f-113">Remarks</span></span>  
 <span data-ttu-id="dea8f-114">Le `ICLRAppDomainResourceMonitor` interface fournit des fonctionnalités qui sont semblables aux propriétés managées suivantes :</span><span class="sxs-lookup"><span data-stu-id="dea8f-114">The `ICLRAppDomainResourceMonitor` interface provides functionality that is similar to the following managed properties:</span></span>  
  
- <xref:System.AppDomain.MonitoringIsEnabled%2A?displayProperty=nameWithType>  
  
- <xref:System.AppDomain.MonitoringTotalProcessorTime%2A?displayProperty=nameWithType>  
  
- <xref:System.AppDomain.MonitoringTotalAllocatedMemorySize%2A?displayProperty=nameWithType>  
  
- <xref:System.AppDomain.MonitoringSurvivedProcessMemorySize%2A?displayProperty=nameWithType>  
  
- <xref:System.AppDomain.MonitoringSurvivedMemorySize%2A?displayProperty=nameWithType>  
  
## <a name="requirements"></a><span data-ttu-id="dea8f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dea8f-115">Requirements</span></span>  
 <span data-ttu-id="dea8f-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dea8f-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dea8f-117">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="dea8f-117">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="dea8f-118">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="dea8f-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="dea8f-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dea8f-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dea8f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dea8f-120">See also</span></span>

- [<span data-ttu-id="dea8f-121">\<appDomainResourceMonitoring > élément</span><span class="sxs-lookup"><span data-stu-id="dea8f-121">\<appDomainResourceMonitoring> Element</span></span>](../../../../docs/framework/configure-apps/file-schema/runtime/appdomainresourcemonitoring-element.md)
- [<span data-ttu-id="dea8f-122">Analyse de ressource de domaine d'application</span><span class="sxs-lookup"><span data-stu-id="dea8f-122">Application Domain Resource Monitoring</span></span>](../../../../docs/standard/garbage-collection/app-domain-resource-monitoring.md)
- [<span data-ttu-id="dea8f-123">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="dea8f-123">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="dea8f-124">Hébergement</span><span class="sxs-lookup"><span data-stu-id="dea8f-124">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
