---
title: IHostTask, interface
ms.date: 03/30/2017
api_name:
- IHostTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTask
helpviewer_keywords:
- IHostTask interface [.NET Framework hosting]
ms.assetid: a71dbbd5-64b8-47eb-9f03-8e8c85fbe2bc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cb15da31d91565d49df83099045f742866eebcaa
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61992834"
---
# <a name="ihosttask-interface"></a><span data-ttu-id="7695e-102">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="7695e-102">IHostTask Interface</span></span>
<span data-ttu-id="7695e-103">Fournit des méthodes qui permettent le common language runtime (CLR) pour communiquer avec l’hôte pour gérer les tâches.</span><span class="sxs-lookup"><span data-stu-id="7695e-103">Provides methods that allow the common language runtime (CLR) to communicate with the host to manage tasks.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7695e-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7695e-104">Methods</span></span>  
  
|<span data-ttu-id="7695e-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="7695e-105">Method</span></span>|<span data-ttu-id="7695e-106">Description</span><span class="sxs-lookup"><span data-stu-id="7695e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7695e-107">Alert, méthode</span><span class="sxs-lookup"><span data-stu-id="7695e-107">Alert Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-alert-method.md)|<span data-ttu-id="7695e-108">Demande que l’hôte réactive la tâche représentée par le `IHostTask` de l’instance, donc la tâche peut être abandonnée.</span><span class="sxs-lookup"><span data-stu-id="7695e-108">Requests that the host wake the task represented by the current `IHostTask` instance, so the task can be aborted.</span></span>|  
|[<span data-ttu-id="7695e-109">GetPriority, méthode</span><span class="sxs-lookup"><span data-stu-id="7695e-109">GetPriority Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-getpriority-method.md)|<span data-ttu-id="7695e-110">Obtient le niveau de priorité de thread de la tâche représentée par l’actuel `IHostTask` instance.</span><span class="sxs-lookup"><span data-stu-id="7695e-110">Gets the thread priority level of the task represented by the current `IHostTask` instance.</span></span>|  
|[<span data-ttu-id="7695e-111">Join, méthode</span><span class="sxs-lookup"><span data-stu-id="7695e-111">Join Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-join-method.md)|<span data-ttu-id="7695e-112">Bloque la tâche appelante jusqu'à ce que la tâche représentée par le `IHostTask` instance se termine, l’intervalle de temps spécifié écoulé, ou [IHostTask::Alert](../../../../docs/framework/unmanaged-api/hosting/ihosttask-alert-method.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="7695e-112">Blocks the calling task until the task represented by the current `IHostTask` instance completes, the specified time interval elapses, or [IHostTask::Alert](../../../../docs/framework/unmanaged-api/hosting/ihosttask-alert-method.md) is called.</span></span>|  
|[<span data-ttu-id="7695e-113">SetCLRTask, méthode</span><span class="sxs-lookup"><span data-stu-id="7695e-113">SetCLRTask Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-setclrtask-method.md)|<span data-ttu-id="7695e-114">Associe un [ICLRTask, Interface](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance avec actuel `IHostTask` instance.</span><span class="sxs-lookup"><span data-stu-id="7695e-114">Associates an [ICLRTask Interface](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance with the current `IHostTask` instance.</span></span>|  
|[<span data-ttu-id="7695e-115">SetPriority, méthode</span><span class="sxs-lookup"><span data-stu-id="7695e-115">SetPriority Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-setpriority-method.md)|<span data-ttu-id="7695e-116">Le niveau de demande que l’hôte ajuste la priorité de thread de la tâche représentée par l’actuel `IHostTask` instance.</span><span class="sxs-lookup"><span data-stu-id="7695e-116">Requests that the host adjust the thread priority level for the task represented by the current `IHostTask` instance.</span></span>|  
|[<span data-ttu-id="7695e-117">Start, méthode</span><span class="sxs-lookup"><span data-stu-id="7695e-117">Start Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-start-method.md)|<span data-ttu-id="7695e-118">Demande que l’hôte déplace la tâche représentée par l’actuel `IHostTask` instance à partir d’un état suspendu à un état actif, dans lequel le code peut être exécuté.</span><span class="sxs-lookup"><span data-stu-id="7695e-118">Requests that the host move the task represented by the current `IHostTask` instance from a suspended state to a live state, in which code can be executed.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7695e-119">Notes</span><span class="sxs-lookup"><span data-stu-id="7695e-119">Remarks</span></span>  
 <span data-ttu-id="7695e-120">Le CLR appelle les méthodes définies par `IHostTask` pour démarrer une tâche, définir sa priorité de thread niveau, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="7695e-120">The CLR calls methods defined by `IHostTask` to start a task, set its thread priority level, and so on.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7695e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7695e-121">Requirements</span></span>  
 <span data-ttu-id="7695e-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7695e-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7695e-123">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="7695e-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="7695e-124">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7695e-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7695e-125">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7695e-125">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7695e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7695e-126">See also</span></span>

- [<span data-ttu-id="7695e-127">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="7695e-127">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="7695e-128">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="7695e-128">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="7695e-129">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="7695e-129">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
- [<span data-ttu-id="7695e-130">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="7695e-130">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
