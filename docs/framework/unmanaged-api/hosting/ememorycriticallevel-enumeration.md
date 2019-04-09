---
title: EMemoryCriticalLevel, énumération
ms.date: 03/30/2017
api_name:
- EMemoryCriticalLevel
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EMemoryCriticalLevel
helpviewer_keywords:
- EMemoryCriticalLevel enumeration [.NET Framework hosting]
ms.assetid: 2ca8a7a2-7b54-4ba3-8e73-277c7df485f3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4ee8705d00e1f63f69863d0bf8e7d0d9d62807e6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59122289"
---
# <a name="ememorycriticallevel-enumeration"></a><span data-ttu-id="b0457-102">EMemoryCriticalLevel, énumération</span><span class="sxs-lookup"><span data-stu-id="b0457-102">EMemoryCriticalLevel Enumeration</span></span>
<span data-ttu-id="b0457-103">Contient des valeurs qui indiquent l’impact d’un échec lors de l’allocation de mémoire spécifique a été demandée mais ne peut pas être satisfaite.</span><span class="sxs-lookup"><span data-stu-id="b0457-103">Contains values that indicate the impact of a failure when a specific memory allocation has been requested but cannot be satisfied.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b0457-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0457-104">Syntax</span></span>  
  
```  
typedef enum {  
    eTaskCritical      = 0,  
    eAppDomainCritical = 1,  
    eProcessCritical   = 2  
} EMemoryCriticalLevel;  
```  
  
## <a name="members"></a><span data-ttu-id="b0457-105">Membres</span><span class="sxs-lookup"><span data-stu-id="b0457-105">Members</span></span>  
  
|<span data-ttu-id="b0457-106">Membre</span><span class="sxs-lookup"><span data-stu-id="b0457-106">Member</span></span>|<span data-ttu-id="b0457-107">Description</span><span class="sxs-lookup"><span data-stu-id="b0457-107">Description</span></span>|  
|------------|-----------------|  
|`eAppDomainCritical`|<span data-ttu-id="b0457-108">Indique que l’allocation est critique pour l’exécution de code managé dans le domaine qui a demandé l’allocation.</span><span class="sxs-lookup"><span data-stu-id="b0457-108">Indicates that the allocation is critical for executing managed code in the domain that has requested the allocation.</span></span> <span data-ttu-id="b0457-109">Si la mémoire ne peut pas être allouée, le CLR ne garantit pas que le domaine est toujours utilisable.</span><span class="sxs-lookup"><span data-stu-id="b0457-109">If memory cannot be allocated, the CLR cannot guarantee that the domain is still usable.</span></span> <span data-ttu-id="b0457-110">L’hôte décide d’action à entreprendre lorsque l’allocation ne peut pas être satisfaite.</span><span class="sxs-lookup"><span data-stu-id="b0457-110">The host decides what action to take when the allocation cannot be satisfied.</span></span> <span data-ttu-id="b0457-111">Il peut indiquer au CLR pour abandonner la `AppDomain` automatiquement, ou lui permettre de poursuivre son exécution en appelant des méthodes sur [ICLRPolicyManager](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md).</span><span class="sxs-lookup"><span data-stu-id="b0457-111">It can instruct the CLR to abort the `AppDomain` automatically, or allow it to keep running by calling methods on [ICLRPolicyManager](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md).</span></span>|  
|`eProcessCritical`|<span data-ttu-id="b0457-112">Indique que l’allocation est critique pour l’exécution du code managé dans le processus.</span><span class="sxs-lookup"><span data-stu-id="b0457-112">Indicates that the allocation is critical to the execution of managed code in the process.</span></span> <span data-ttu-id="b0457-113">Cette valeur est utilisée lors du démarrage et lors de l’exécution des finaliseurs.</span><span class="sxs-lookup"><span data-stu-id="b0457-113">This value is used during startup and when running finalizers.</span></span> <span data-ttu-id="b0457-114">Si la mémoire ne peut pas être allouée, le CLR ne peut pas fonctionner dans le processus.</span><span class="sxs-lookup"><span data-stu-id="b0457-114">If memory cannot be allocated, the CLR cannot operate in the process.</span></span> <span data-ttu-id="b0457-115">Si l’allocation échoue, le CLR est désactivé.</span><span class="sxs-lookup"><span data-stu-id="b0457-115">If the allocation fails, the CLR is effectively disabled.</span></span> <span data-ttu-id="b0457-116">Tous les appels ultérieurs dans le CLR échouent avec HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="b0457-116">All subsequent calls into the CLR fail with HOST_E_CLRNOTAVAILABLE.</span></span>|  
|`eTaskCritical`|<span data-ttu-id="b0457-117">Indique que l’allocation est critique pour l’exécution de la tâche qui a demandé l’allocation.</span><span class="sxs-lookup"><span data-stu-id="b0457-117">Indicates that the allocation is critical to running the task that has requested the allocation.</span></span> <span data-ttu-id="b0457-118">Si la mémoire ne peut pas être allouée, le CLR ne garantit pas que la tâche peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="b0457-118">If memory cannot be allocated, the CLR cannot guarantee that the task can be executed.</span></span> <span data-ttu-id="b0457-119">En cas de défaillance, le CLR lève une <xref:System.Threading.ThreadAbortException> sur le thread de système d’opération physique.</span><span class="sxs-lookup"><span data-stu-id="b0457-119">In the event of failure, the CLR raises a <xref:System.Threading.ThreadAbortException> on the physical operation system thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b0457-120">Notes</span><span class="sxs-lookup"><span data-stu-id="b0457-120">Remarks</span></span>  
 <span data-ttu-id="b0457-121">Les méthodes d’allocation de mémoire définies dans le [IHostMemoryManager](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md) et [IHostMAlloc](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-interface.md) interfaces prennent un paramètre de ce type.</span><span class="sxs-lookup"><span data-stu-id="b0457-121">The memory allocation methods defined in the [IHostMemoryManager](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md) and [IHostMAlloc](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-interface.md) interfaces take a parameter of this type.</span></span> <span data-ttu-id="b0457-122">Selon la gravité d’une défaillance, un hôte peut décider à échouer la demande d’allocation immédiatement ou attendre jusqu'à ce qu’il peut être satisfaite.</span><span class="sxs-lookup"><span data-stu-id="b0457-122">Depending upon the severity of a failure, a host can decide whether to fail the allocation request immediately or to wait until it can be satisfied.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b0457-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0457-123">Requirements</span></span>  
 <span data-ttu-id="b0457-124">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b0457-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b0457-125">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="b0457-125">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b0457-126">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b0457-126">**Library:** MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="b0457-127">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="b0457-127">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="b0457-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0457-128">See also</span></span>

- [<span data-ttu-id="b0457-129">ICLRMemoryNotificationCallback, interface</span><span class="sxs-lookup"><span data-stu-id="b0457-129">ICLRMemoryNotificationCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmemorynotificationcallback-interface.md)
- [<span data-ttu-id="b0457-130">Énumérations d'hébergement</span><span class="sxs-lookup"><span data-stu-id="b0457-130">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
