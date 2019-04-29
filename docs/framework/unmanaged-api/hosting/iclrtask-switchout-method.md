---
title: ICLRTask::SwitchOut, méthode
ms.date: 03/30/2017
api_name:
- ICLRTask.SwitchOut
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::SwitchOut
helpviewer_keywords:
- ICLRTask::SwitchOut method [.NET Framework hosting]
- SwitchOut method [.NET Framework hosting]
ms.assetid: b6fb168c-b24b-4ecf-a390-2b5ba3317ae6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a215189461bd22011462842bf02ff6c0109119fa
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61763475"
---
# <a name="iclrtaskswitchout-method"></a><span data-ttu-id="25ffe-102">ICLRTask::SwitchOut, méthode</span><span class="sxs-lookup"><span data-stu-id="25ffe-102">ICLRTask::SwitchOut Method</span></span>
<span data-ttu-id="25ffe-103">Notifie le common language runtime (CLR) que la tâche représentée par l’actuel [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance n’est plus dans un état opérationnel.</span><span class="sxs-lookup"><span data-stu-id="25ffe-103">Notifies the common language runtime (CLR) that the task represented by the current [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance is no longer in an operable state.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="25ffe-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25ffe-104">Syntax</span></span>  
  
```  
HRESULT SwitchOut ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="25ffe-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="25ffe-105">Return Value</span></span>  
  
|<span data-ttu-id="25ffe-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="25ffe-106">HRESULT</span></span>|<span data-ttu-id="25ffe-107">Description</span><span class="sxs-lookup"><span data-stu-id="25ffe-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="25ffe-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="25ffe-108">S_OK</span></span>|<span data-ttu-id="25ffe-109">`SwitchOut` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="25ffe-109">`SwitchOut` returned successfully.</span></span>|  
|<span data-ttu-id="25ffe-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="25ffe-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="25ffe-111">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="25ffe-111">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="25ffe-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="25ffe-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="25ffe-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="25ffe-113">The call timed out.</span></span>|  
|<span data-ttu-id="25ffe-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="25ffe-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="25ffe-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="25ffe-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="25ffe-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="25ffe-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="25ffe-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="25ffe-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="25ffe-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="25ffe-118">E_FAIL</span></span>|<span data-ttu-id="25ffe-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="25ffe-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="25ffe-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="25ffe-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="25ffe-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="25ffe-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="25ffe-122">Notes</span><span class="sxs-lookup"><span data-stu-id="25ffe-122">Remarks</span></span>  
 <span data-ttu-id="25ffe-123">Un hôte appelle `SwitchOut` d’informer le CLR qu’il a arrêté temporairement l’exécution de la tâche qui en cours `ICLRTask` représente l’instance et va la replanifier la tâche.</span><span class="sxs-lookup"><span data-stu-id="25ffe-123">A host calls `SwitchOut` to inform the CLR that it has temporarily stopped executing the task that the current `ICLRTask` instance represents, and will reschedule the task.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="25ffe-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25ffe-124">Requirements</span></span>  
 <span data-ttu-id="25ffe-125">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="25ffe-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="25ffe-126">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="25ffe-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="25ffe-127">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="25ffe-127">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="25ffe-128">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="25ffe-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="25ffe-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25ffe-129">See also</span></span>

- [<span data-ttu-id="25ffe-130">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="25ffe-130">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="25ffe-131">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="25ffe-131">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="25ffe-132">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="25ffe-132">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="25ffe-133">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="25ffe-133">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
