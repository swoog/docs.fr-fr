---
title: IHostThreadPoolManager, interface
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager
helpviewer_keywords:
- IHostThreadPoolManager interface [.NET Framework hosting]
ms.assetid: c3a2cd90-7c4e-4374-bb87-b41befb8344f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2e7976740a79efda8e5ab569f2efb55444012c5d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59220368"
---
# <a name="ihostthreadpoolmanager-interface"></a><span data-ttu-id="bf862-102">IHostThreadPoolManager, interface</span><span class="sxs-lookup"><span data-stu-id="bf862-102">IHostThreadPoolManager Interface</span></span>
<span data-ttu-id="bf862-103">Fournit des méthodes qui permettent le common language runtime (CLR) pour configurer le pool de threads et en file d’attente des éléments de travail au pool de threads.</span><span class="sxs-lookup"><span data-stu-id="bf862-103">Provides methods that enable the common language runtime (CLR) to configure the thread pool and to queue work items to the thread pool.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="bf862-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bf862-104">Methods</span></span>  
  
|<span data-ttu-id="bf862-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="bf862-105">Method</span></span>|<span data-ttu-id="bf862-106">Description</span><span class="sxs-lookup"><span data-stu-id="bf862-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="bf862-107">GetAvailableThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="bf862-107">GetAvailableThreads Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-getavailablethreads-method.md)|<span data-ttu-id="bf862-108">Obtient le nombre de threads du pool de threads qui ne traitent pas actuellement des éléments de travail.</span><span class="sxs-lookup"><span data-stu-id="bf862-108">Gets the number of threads in the thread pool that are not currently processing work items.</span></span>|  
|[<span data-ttu-id="bf862-109">GetMaxThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="bf862-109">GetMaxThreads Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-getmaxthreads-method.md)|<span data-ttu-id="bf862-110">Obtient le nombre maximal de threads que l’hôte conserve simultanément dans le pool de threads.</span><span class="sxs-lookup"><span data-stu-id="bf862-110">Gets the maximum number of threads that the host maintains concurrently in the thread pool.</span></span>|  
|[<span data-ttu-id="bf862-111">GetMinThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="bf862-111">GetMinThreads Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-getminthreads-method.md)|<span data-ttu-id="bf862-112">Obtient le nombre minimal de threads inactifs que l’hôte conserve en prévision des demandes.</span><span class="sxs-lookup"><span data-stu-id="bf862-112">Gets the minimum number of idle threads that the host maintains in anticipation of requests.</span></span>|  
|[<span data-ttu-id="bf862-113">QueueUserWorkItem, méthode</span><span class="sxs-lookup"><span data-stu-id="bf862-113">QueueUserWorkItem Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-queueuserworkitem-method.md)|<span data-ttu-id="bf862-114">Files d’attente d’une fonction pour l’exécution et fournit un objet contenant les données à utiliser par la fonction.</span><span class="sxs-lookup"><span data-stu-id="bf862-114">Queues a function for execution, and provides an object containing data to be used by the function.</span></span>|  
|[<span data-ttu-id="bf862-115">SetMaxThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="bf862-115">SetMaxThreads Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-setmaxthreads-method.md)|<span data-ttu-id="bf862-116">Définit le nombre maximal de threads que l’hôte peut gérer dans le pool de threads.</span><span class="sxs-lookup"><span data-stu-id="bf862-116">Sets the maximum number of threads that the host can maintain in the thread pool.</span></span>|  
|[<span data-ttu-id="bf862-117">SetMinThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="bf862-117">SetMinThreads Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-setminthreads-method.md)|<span data-ttu-id="bf862-118">Définit le nombre minimal de threads inactifs que l’hôte doit gérer en prévision des demandes.</span><span class="sxs-lookup"><span data-stu-id="bf862-118">Sets the minimum number of idle threads that the host must maintain in anticipation of requests.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bf862-119">Notes</span><span class="sxs-lookup"><span data-stu-id="bf862-119">Remarks</span></span>  
 <span data-ttu-id="bf862-120">L’hôte n’est pas nécessaire de configurer le pool de threads en utilisant les valeurs spécifiées dans les appels à la `SetMaxThreads` et `SetMinThreads` méthodes.</span><span class="sxs-lookup"><span data-stu-id="bf862-120">The host is not required to configure the thread pool by using the values specified in calls to the `SetMaxThreads` and `SetMinThreads` methods.</span></span> <span data-ttu-id="bf862-121">Dans ce cas, l’hôte doit retourner une valeur HRESULT d’E_NOTIMPL à partir de ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="bf862-121">In this case, the host should return an HRESULT value of E_NOTIMPL from these methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bf862-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf862-122">Requirements</span></span>  
 <span data-ttu-id="bf862-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bf862-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bf862-124">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="bf862-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bf862-125">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bf862-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bf862-126">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bf862-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bf862-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf862-127">See also</span></span>

- <xref:System.Threading>
- <xref:System.Threading.ThreadPool>
- [<span data-ttu-id="bf862-128">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="bf862-128">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
