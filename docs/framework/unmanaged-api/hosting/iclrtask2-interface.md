---
title: ICLRTask2, interface
ms.date: 03/30/2017
api_name:
- ICLRTask2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask2
helpviewer_keywords:
- ICLRTask2 interface [.NET Framework hosting]
ms.assetid: b5a22ebc-0582-49de-91f9-97a3d9789290
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 518248651de6d8afdf25692c5f48da52b11eb0f7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59172469"
---
# <a name="iclrtask2-interface"></a><span data-ttu-id="fd2ac-102">ICLRTask2, interface</span><span class="sxs-lookup"><span data-stu-id="fd2ac-102">ICLRTask2 Interface</span></span>
<span data-ttu-id="fd2ac-103">Fournit toutes les fonctionnalités de la [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) interface ; en outre, fournit des méthodes qui permettent les abandons de thread pour être retardée sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="fd2ac-103">Provides all the functionality of the [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) interface; in addition, provides methods that allow thread aborts to be delayed on the current thread.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="fd2ac-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fd2ac-104">Methods</span></span>  
  
|<span data-ttu-id="fd2ac-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="fd2ac-105">Method</span></span>|<span data-ttu-id="fd2ac-106">Description</span><span class="sxs-lookup"><span data-stu-id="fd2ac-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="fd2ac-107">BeginPreventAsyncAbort, méthode</span><span class="sxs-lookup"><span data-stu-id="fd2ac-107">BeginPreventAsyncAbort Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-beginpreventasyncabort-method.md)|<span data-ttu-id="fd2ac-108">Nouveau thread de retards interrompre les requêtes sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="fd2ac-108">Delays new thread abort requests on the current thread.</span></span>|  
|[<span data-ttu-id="fd2ac-109">BeginPreventAsyncAbort, méthode</span><span class="sxs-lookup"><span data-stu-id="fd2ac-109">EndPreventAsyncAbort Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-endpreventasyncabort-method.md)|<span data-ttu-id="fd2ac-110">Permet à nouveau ou en attente de demandes d’abandon de thread pour le thread sur abandonnée sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="fd2ac-110">Allows new or pending thread abort requests to result in thread aborts on the current thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fd2ac-111">Notes</span><span class="sxs-lookup"><span data-stu-id="fd2ac-111">Remarks</span></span>  
 <span data-ttu-id="fd2ac-112">Le `ICLRTask2` interface hérite le `ICLRTask` interface et ajoute des méthodes qui permettent à l’hôte de différer les abandons de thread, pour protéger une région de code qui ne doit pas échouer.</span><span class="sxs-lookup"><span data-stu-id="fd2ac-112">The `ICLRTask2` interface inherits the `ICLRTask` interface and adds methods that allow the host to delay thread aborts, to protect a region of code that must not fail.</span></span> <span data-ttu-id="fd2ac-113">Appel `BeginPreventAsyncAbort` incrémente le compteur de délai d’abandon de thread pour le thread actuel et l’appel `EndPreventAsyncAbort` décrémente il.</span><span class="sxs-lookup"><span data-stu-id="fd2ac-113">Calling `BeginPreventAsyncAbort` increments the delay-thread-abort counter for the current thread, and calling `EndPreventAsyncAbort` decrements it.</span></span> <span data-ttu-id="fd2ac-114">Les appels à `BeginPreventAsyncAbort` et `EndPreventAsyncAbort` peuvent être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="fd2ac-114">Calls to `BeginPreventAsyncAbort` and `EndPreventAsyncAbort` can be nested.</span></span> <span data-ttu-id="fd2ac-115">Tant que le compteur est supérieur à zéro, pour le thread actuel abandons de thread.</span><span class="sxs-lookup"><span data-stu-id="fd2ac-115">As long as the counter is greater than zero, thread aborts for the current thread are delayed.</span></span>  
  
 <span data-ttu-id="fd2ac-116">Si les appels à `BeginPreventAsyncAbort` et `EndPreventAsyncAbort` sont ne pas jumelées, il est possible d’atteindre un état dans lequel thread abandons ne peut pas être remis au thread actuel.</span><span class="sxs-lookup"><span data-stu-id="fd2ac-116">If calls to `BeginPreventAsyncAbort` and `EndPreventAsyncAbort` are not paired, it is possible to reach a state in which thread aborts cannot be delivered to the current thread.</span></span>  
  
 <span data-ttu-id="fd2ac-117">Le délai n’est pas reconnue pour un thread qui abandonne lui-même.</span><span class="sxs-lookup"><span data-stu-id="fd2ac-117">The delay is not honored for a thread that aborts itself.</span></span>  
  
 <span data-ttu-id="fd2ac-118">La fonctionnalité exposée par cette fonctionnalité est utilisée en interne par la machine virtuelle (VM).</span><span class="sxs-lookup"><span data-stu-id="fd2ac-118">The functionality that is exposed by this feature is used internally by the virtual machine (VM).</span></span> <span data-ttu-id="fd2ac-119">Une mauvaise utilisation de ces méthodes peut-être provoquer un comportement non spécifié dans la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="fd2ac-119">Misuse of these methods may cause unspecified behavior in the VM.</span></span> <span data-ttu-id="fd2ac-120">Par exemple, l’appel `EndPreventAsyncAbort` sans appeler d’abord `BeginPreventAsyncAbort` Impossible de définir le compteur à zéro lors de la machine virtuelle a précédemment incrémenté.</span><span class="sxs-lookup"><span data-stu-id="fd2ac-120">For example, calling `EndPreventAsyncAbort` without first calling `BeginPreventAsyncAbort` could set the counter to zero when the VM has previously incremented it.</span></span> <span data-ttu-id="fd2ac-121">De même, le compteur interne n’est pas vérifié pour dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="fd2ac-121">Similarly, the internal counter is not checked for overflow.</span></span> <span data-ttu-id="fd2ac-122">S’il dépasse sa limite intégrale, car il est incrémenté par l’hôte et la machine virtuelle, le comportement résultant n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="fd2ac-122">If it exceeds its integral limit because it is incremented by both the host and the VM, the resulting behavior is unspecified.</span></span>  
  
 <span data-ttu-id="fd2ac-123">Pour plus d’informations sur les membres hérités de `ICLRTask` et sur les autres utilisations de cette interface, consultez la [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="fd2ac-123">For information about members inherited from `ICLRTask` and about the other uses of this interface, see the [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fd2ac-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd2ac-124">Requirements</span></span>  
 <span data-ttu-id="fd2ac-125">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fd2ac-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fd2ac-126">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="fd2ac-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fd2ac-127">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fd2ac-127">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="fd2ac-128">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="fd2ac-128">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="fd2ac-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd2ac-129">See also</span></span>

- [<span data-ttu-id="fd2ac-130">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="fd2ac-130">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="fd2ac-131">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="fd2ac-131">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="fd2ac-132">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="fd2ac-132">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="fd2ac-133">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="fd2ac-133">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
- [<span data-ttu-id="fd2ac-134">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="fd2ac-134">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
