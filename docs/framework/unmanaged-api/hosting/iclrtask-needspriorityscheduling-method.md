---
title: ICLRTask::NeedsPriorityScheduling, méthode
ms.date: 03/30/2017
api_name:
- ICLRTask.NeedsPriorityScheduling
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::NeedsPriorityScheduling
helpviewer_keywords:
- ICLRTask::NeedsPriorityScheduling method [.NET Framework hosting]
- NeedsPriorityScheduling method [.NET Framework hosting]
ms.assetid: 9c9db3f3-26bf-4317-88de-5eb926a22a1d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 36403abcae4d4e691fe6362e61cf7fa979ec7f5e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33435736"
---
# <a name="iclrtaskneedspriorityscheduling-method"></a><span data-ttu-id="9ce27-102">ICLRTask::NeedsPriorityScheduling, méthode</span><span class="sxs-lookup"><span data-stu-id="9ce27-102">ICLRTask::NeedsPriorityScheduling Method</span></span>
<span data-ttu-id="9ce27-103">Obtient une valeur qui indique si la tâche actuelle, qui est en cours de basculement, doit être marquée comme une priorité élevée pour une nouvelle planification.</span><span class="sxs-lookup"><span data-stu-id="9ce27-103">Gets a value that indicates whether the current task, which is being switched out, needs to be marked as a high priority for rescheduling.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ce27-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ce27-104">Syntax</span></span>  
  
```  
HRESULT NeedsPriorityScheduling (  
    [out] BOOL *pbNeedsPriorityScheduling  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9ce27-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ce27-105">Parameters</span></span>  
 `pbNeedsPriorityRescheduling`  
 <span data-ttu-id="9ce27-106">[out] `true`, si l’hôte doit tenter de replanifier l’instance actuelle de la tâche dès que possible ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="9ce27-106">[out] `true`, if the host should attempt to reschedule the current task instance as soon as possible; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9ce27-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9ce27-107">Return Value</span></span>  
  
|<span data-ttu-id="9ce27-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9ce27-108">HRESULT</span></span>|<span data-ttu-id="9ce27-109">Description</span><span class="sxs-lookup"><span data-stu-id="9ce27-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="9ce27-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ce27-110">S_OK</span></span>|<span data-ttu-id="9ce27-111">`NeedsPriorityRescheduling` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="9ce27-111">`NeedsPriorityRescheduling` returned successfully.</span></span>|  
|<span data-ttu-id="9ce27-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="9ce27-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="9ce27-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="9ce27-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="9ce27-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="9ce27-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="9ce27-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="9ce27-115">The call timed out.</span></span>|  
|<span data-ttu-id="9ce27-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="9ce27-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="9ce27-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="9ce27-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="9ce27-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="9ce27-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="9ce27-119">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="9ce27-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="9ce27-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="9ce27-120">E_FAIL</span></span>|<span data-ttu-id="9ce27-121">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9ce27-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="9ce27-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="9ce27-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="9ce27-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="9ce27-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9ce27-124">Notes</span><span class="sxs-lookup"><span data-stu-id="9ce27-124">Remarks</span></span>  
 <span data-ttu-id="9ce27-125">Dans les situations où la tâche est proche de collectés par le garbage collector, le CLR définit la valeur de `pbNeedsPriorityScheduling` à `true`, indiquant la replanification de haute priorité.</span><span class="sxs-lookup"><span data-stu-id="9ce27-125">In situations where the task is close to being collected by the garbage collector, the CLR sets the value of `pbNeedsPriorityScheduling` to `true`, indicating high-priority rescheduling.</span></span> <span data-ttu-id="9ce27-126">Cela permet à l’hôte de replanifier la tâche rapidement, pour minimiser le risque de retard du garbage collection et l’activation de l’hôte et le runtime de coopérer pour conserver des ressources mémoire.</span><span class="sxs-lookup"><span data-stu-id="9ce27-126">This allows the host to reschedule the task quickly, thereby minimizing the potential for delays in garbage collection, and enabling the host and the runtime to cooperate in conserving memory resources.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9ce27-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9ce27-127">Requirements</span></span>  
 <span data-ttu-id="9ce27-128">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9ce27-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ce27-129">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="9ce27-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9ce27-130">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9ce27-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9ce27-131">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ce27-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ce27-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ce27-132">See Also</span></span>  
 [<span data-ttu-id="9ce27-133">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="9ce27-133">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [<span data-ttu-id="9ce27-134">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="9ce27-134">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="9ce27-135">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="9ce27-135">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="9ce27-136">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="9ce27-136">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
