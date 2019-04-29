---
title: ICLRTaskManager, interface
ms.date: 03/30/2017
api_name:
- ICLRTaskManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTaskManager
helpviewer_keywords:
- ICLRTaskManager interface [.NET Framework hosting]
ms.assetid: 2bd55e0c-001b-41fd-b29d-f01670fe8216
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 19ef7cb78791496de76e5741f8254ee88563c776
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61763371"
---
# <a name="iclrtaskmanager-interface"></a><span data-ttu-id="261aa-102">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="261aa-102">ICLRTaskManager Interface</span></span>
<span data-ttu-id="261aa-103">Fournit des méthodes qui permettent à l’hôte à demander explicitement que le common language runtime (CLR) créer une nouvelle tâche, obtenir la tâche en cours d’exécution et définir le langage géographique et la culture pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="261aa-103">Provides methods that allow the host to request explicitly that the common language runtime (CLR) create a new task, get the currently executing task, and set the geographic language and culture for the task.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="261aa-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="261aa-104">Methods</span></span>  
  
|<span data-ttu-id="261aa-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="261aa-105">Method</span></span>|<span data-ttu-id="261aa-106">Description</span><span class="sxs-lookup"><span data-stu-id="261aa-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="261aa-107">CreateTask, méthode</span><span class="sxs-lookup"><span data-stu-id="261aa-107">CreateTask Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-createtask-method.md)|<span data-ttu-id="261aa-108">Demande explicitement que le CLR crée un nouveau [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance.</span><span class="sxs-lookup"><span data-stu-id="261aa-108">Requests explicitly that the CLR create a new [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance.</span></span>|  
|[<span data-ttu-id="261aa-109">GetCurrentTask, méthode</span><span class="sxs-lookup"><span data-stu-id="261aa-109">GetCurrentTask Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-getcurrenttask-method.md)|<span data-ttu-id="261aa-110">Obtient le `ICLRTask` instance qui représente la tâche en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="261aa-110">Gets the `ICLRTask` instance that represents the task that is currently executing.</span></span>|  
|[<span data-ttu-id="261aa-111">GetCurrentTaskType, méthode</span><span class="sxs-lookup"><span data-stu-id="261aa-111">GetCurrentTaskType Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-getcurrenttasktype-method.md)|<span data-ttu-id="261aa-112">Obtient le type de la tâche en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="261aa-112">Gets the type of the task that is currently executing.</span></span>|  
|[<span data-ttu-id="261aa-113">SetLocale, méthode</span><span class="sxs-lookup"><span data-stu-id="261aa-113">SetLocale Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-setlocale-method.md)|<span data-ttu-id="261aa-114">Notifie le CLR que l’hôte a modifié l’identificateur de paramètres régionaux sur la tâche en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="261aa-114">Notifies the CLR that the host has modified the locale identifier on the currently executing task.</span></span>|  
|[<span data-ttu-id="261aa-115">SetUILocale, méthode</span><span class="sxs-lookup"><span data-stu-id="261aa-115">SetUILocale Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-setuilocale-method.md)|<span data-ttu-id="261aa-116">Notifie le common language runtime que l’hôte a modifié l’identificateur de paramètres régionaux d’interface utilisateur sur la tâche en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="261aa-116">Notifies the common language runtime that the host has modified the user interface locale identifier on the currently executing task.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="261aa-117">Notes</span><span class="sxs-lookup"><span data-stu-id="261aa-117">Remarks</span></span>  
 <span data-ttu-id="261aa-118">Chaque tâche qui s’exécute dans un environnement hébergé a des représentations à la fois du côté hôte (une instance de [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)) et sur le côté CLR (une instance de [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)).</span><span class="sxs-lookup"><span data-stu-id="261aa-118">Each task that is running in a hosted environment has representations both on the host side (an instance of [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)) and on the CLR side (an instance of [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)).</span></span> <span data-ttu-id="261aa-119">L’hôte ou le CLR peut lancer la création d’une tâche, mais la représentation côté hôte doit être associée à une représentation côté CLR correspondante pour garantir une communication réussie entre l’hôte et le CLR concernant la tâche.</span><span class="sxs-lookup"><span data-stu-id="261aa-119">Either the host or the CLR can initiate the creation of a task, but the host-side representation must be associated with a corresponding CLR-side representation to ensure successful communication between the host and the CLR regarding the task.</span></span> <span data-ttu-id="261aa-120">Les deux objets doivent être créées et instanciés avant que le code managé peut s’exécuter sur un thread de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="261aa-120">The two objects must be created and instantiated before managed code can execute on an operating system thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="261aa-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="261aa-121">Requirements</span></span>  
 <span data-ttu-id="261aa-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="261aa-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="261aa-123">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="261aa-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="261aa-124">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="261aa-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="261aa-125">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="261aa-125">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="261aa-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="261aa-126">See also</span></span>

- [<span data-ttu-id="261aa-127">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="261aa-127">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="261aa-128">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="261aa-128">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="261aa-129">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="261aa-129">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
- [<span data-ttu-id="261aa-130">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="261aa-130">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
