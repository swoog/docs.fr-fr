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
ms.openlocfilehash: 7eb5c7ec85c0adb301fb722155caaed3c14e0e19
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59137720"
---
# <a name="ihosttaskmanagerbeginthreadaffinity-method"></a><span data-ttu-id="b7306-102">IHostTaskManager::BeginThreadAffinity, méthode</span><span class="sxs-lookup"><span data-stu-id="b7306-102">IHostTaskManager::BeginThreadAffinity Method</span></span>
<span data-ttu-id="b7306-103">Avertit l’hôte que le code managé entre dans une période dans laquelle la tâche actuelle ne doit pas être déplacée vers un autre thread de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b7306-103">Notifies the host that managed code is entering a period in which the current task must not be moved to another operating system thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7306-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7306-104">Syntax</span></span>  
  
```  
HRESULT BeginThreadAffinity ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="b7306-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b7306-105">Return Value</span></span>  
  
|<span data-ttu-id="b7306-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b7306-106">HRESULT</span></span>|<span data-ttu-id="b7306-107">Description</span><span class="sxs-lookup"><span data-stu-id="b7306-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b7306-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7306-108">S_OK</span></span>|`BeginThreadAffinity` <span data-ttu-id="b7306-109">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="b7306-109">returned successfully.</span></span>|  
|<span data-ttu-id="b7306-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b7306-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="b7306-111">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="b7306-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="b7306-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b7306-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="b7306-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="b7306-113">The call timed out.</span></span>|  
|<span data-ttu-id="b7306-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="b7306-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="b7306-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="b7306-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="b7306-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="b7306-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="b7306-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="b7306-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="b7306-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b7306-118">E_FAIL</span></span>|<span data-ttu-id="b7306-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b7306-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="b7306-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="b7306-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="b7306-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="b7306-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b7306-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b7306-122">Remarks</span></span>  
 <span data-ttu-id="b7306-123">Le CLR appelle généralement `IHostTaskManager::BeginThreadAffinity` dans le contexte d’un appel à <xref:System.Threading.Thread.BeginThreadAffinity%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="b7306-123">The CLR typically calls `IHostTaskManager::BeginThreadAffinity` in the context of a call to <xref:System.Threading.Thread.BeginThreadAffinity%2A?displayProperty=nameWithType>.</span></span> <span data-ttu-id="b7306-124">La tâche actuelle ne doit pas être replanifiée jusqu'à l’appel correspondant à [IHostTaskManager::EndThreadAffinity](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-endthreadaffinity-method.md).</span><span class="sxs-lookup"><span data-stu-id="b7306-124">The current task must not be rescheduled until a corresponding call is made to [IHostTaskManager::EndThreadAffinity](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-endthreadaffinity-method.md).</span></span> <span data-ttu-id="b7306-125">Les tâches peuvent être interrompues, mais lorsqu’ils sont reprises, ils doivent posséder le même thread de système d’exploitation à partir de laquelle elles ont été interrompues. Les appels imbriqués à `BeginThreadAffinity` n’ont aucun effet, car l’appel fait référence à la tâche actuelle.</span><span class="sxs-lookup"><span data-stu-id="b7306-125">Tasks can be switched out, but when they are switched back in, they must be assigned to the same operating system thread from which they were switched out. Nested calls to `BeginThreadAffinity` have no effect, because the call refers to the current task.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7306-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7306-126">Requirements</span></span>  
 <span data-ttu-id="b7306-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b7306-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7306-128">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="b7306-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b7306-129">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b7306-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="b7306-130">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="b7306-130">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="b7306-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7306-131">See also</span></span>

- [<span data-ttu-id="b7306-132">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="b7306-132">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="b7306-133">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="b7306-133">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="b7306-134">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="b7306-134">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="b7306-135">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="b7306-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
