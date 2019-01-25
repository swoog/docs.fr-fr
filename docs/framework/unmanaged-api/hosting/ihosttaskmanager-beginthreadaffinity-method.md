---
title: IHostTaskManager::BeginThreadAffinity, méthode
ms.date: 03/30/2017
api_name:
- IHostTaskManager.BeginThreadAffinity
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::BeginThreadAffinity
helpviewer_keywords:
- IHostTaskManager::BeginThreadAffinity method [.NET Framework hosting]
- BeginThreadAffinity method [.NET Framework hosting]
ms.assetid: fea3ab88-ce41-4c5a-847b-bb78cd748da6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 67a133604e269b8c20dc8640b91e378c498cf038
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745575"
---
# <a name="ihosttaskmanagerbeginthreadaffinity-method"></a><span data-ttu-id="fd414-102">IHostTaskManager::BeginThreadAffinity, méthode</span><span class="sxs-lookup"><span data-stu-id="fd414-102">IHostTaskManager::BeginThreadAffinity Method</span></span>
<span data-ttu-id="fd414-103">Avertit l’hôte que le code managé entre dans une période dans laquelle la tâche actuelle ne doit pas être déplacée vers un autre thread de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fd414-103">Notifies the host that managed code is entering a period in which the current task must not be moved to another operating system thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fd414-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd414-104">Syntax</span></span>  
  
```  
HRESULT BeginThreadAffinity ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="fd414-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fd414-105">Return Value</span></span>  
  
|<span data-ttu-id="fd414-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="fd414-106">HRESULT</span></span>|<span data-ttu-id="fd414-107">Description</span><span class="sxs-lookup"><span data-stu-id="fd414-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="fd414-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd414-108">S_OK</span></span>|<span data-ttu-id="fd414-109">`BeginThreadAffinity` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="fd414-109">`BeginThreadAffinity` returned successfully.</span></span>|  
|<span data-ttu-id="fd414-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="fd414-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="fd414-111">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="fd414-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="fd414-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="fd414-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="fd414-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="fd414-113">The call timed out.</span></span>|  
|<span data-ttu-id="fd414-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="fd414-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="fd414-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="fd414-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="fd414-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="fd414-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="fd414-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="fd414-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="fd414-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="fd414-118">E_FAIL</span></span>|<span data-ttu-id="fd414-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="fd414-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="fd414-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="fd414-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="fd414-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="fd414-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fd414-122">Notes</span><span class="sxs-lookup"><span data-stu-id="fd414-122">Remarks</span></span>  
 <span data-ttu-id="fd414-123">Le CLR appelle généralement `IHostTaskManager::BeginThreadAffinity` dans le contexte d’un appel à <xref:System.Threading.Thread.BeginThreadAffinity%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="fd414-123">The CLR typically calls `IHostTaskManager::BeginThreadAffinity` in the context of a call to <xref:System.Threading.Thread.BeginThreadAffinity%2A?displayProperty=nameWithType>.</span></span> <span data-ttu-id="fd414-124">La tâche actuelle ne doit pas être replanifiée jusqu'à l’appel correspondant à [IHostTaskManager::EndThreadAffinity](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-endthreadaffinity-method.md).</span><span class="sxs-lookup"><span data-stu-id="fd414-124">The current task must not be rescheduled until a corresponding call is made to [IHostTaskManager::EndThreadAffinity](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-endthreadaffinity-method.md).</span></span> <span data-ttu-id="fd414-125">Les tâches peuvent être interrompues, mais lorsqu’ils sont reprises, ils doivent posséder le même thread de système d’exploitation à partir de laquelle elles ont été interrompues. Les appels imbriqués à `BeginThreadAffinity` n’ont aucun effet, car l’appel fait référence à la tâche actuelle.</span><span class="sxs-lookup"><span data-stu-id="fd414-125">Tasks can be switched out, but when they are switched back in, they must be assigned to the same operating system thread from which they were switched out. Nested calls to `BeginThreadAffinity` have no effect, because the call refers to the current task.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fd414-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fd414-126">Requirements</span></span>  
 <span data-ttu-id="fd414-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fd414-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fd414-128">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="fd414-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fd414-129">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fd414-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fd414-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd414-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd414-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd414-131">See also</span></span>
- [<span data-ttu-id="fd414-132">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="fd414-132">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="fd414-133">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="fd414-133">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="fd414-134">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="fd414-134">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="fd414-135">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="fd414-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
