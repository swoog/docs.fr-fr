---
title: ICLRTask2::BeginPreventAsyncAbort, méthode
ms.date: 03/30/2017
api_name:
- ICLRTask2.BeginPreventAsyncAbort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask2::BeginPreventAsyncAbort
helpviewer_keywords:
- ICLRTask2::BeginPreventAsyncAbort method [.NET Framework hosting]
- BeginPreventAsyncAbort method [.NET Framework hosting]
ms.assetid: 75754c2f-38c7-4707-85fe-559db4542729
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 85a43fef7f6dfa6dbe0bb9f1c4caec2c9c224b93
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61763429"
---
# <a name="iclrtask2beginpreventasyncabort-method"></a><span data-ttu-id="4eb88-102">ICLRTask2::BeginPreventAsyncAbort, méthode</span><span class="sxs-lookup"><span data-stu-id="4eb88-102">ICLRTask2::BeginPreventAsyncAbort Method</span></span>
<span data-ttu-id="4eb88-103">Nouveau thread de retards demandes d’abandon de ce qui entraîne des abandons de thread sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="4eb88-103">Delays new thread abort requests from resulting in thread aborts on the current thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4eb88-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4eb88-104">Syntax</span></span>  
  
```  
HRESULT BeginPreventAsyncAbort();  
```  
  
## <a name="return-value"></a><span data-ttu-id="4eb88-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4eb88-105">Return Value</span></span>  
 <span data-ttu-id="4eb88-106">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="4eb88-106">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="4eb88-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="4eb88-107">HRESULT</span></span>|<span data-ttu-id="4eb88-108">Description</span><span class="sxs-lookup"><span data-stu-id="4eb88-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="4eb88-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="4eb88-109">S_OK</span></span>|<span data-ttu-id="4eb88-110">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="4eb88-110">The method completed successfully.</span></span>|  
|<span data-ttu-id="4eb88-111">HOST_E_INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="4eb88-111">HOST_E_INVALIDOPERATION</span></span>|<span data-ttu-id="4eb88-112">La méthode a été appelée sur un thread qui n’est pas le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="4eb88-112">The method was called on a thread which is not the current thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4eb88-113">Notes</span><span class="sxs-lookup"><span data-stu-id="4eb88-113">Remarks</span></span>  
 <span data-ttu-id="4eb88-114">Appel de cette méthode incrémente le compteur de délai d’abandon de thread pour le thread actuel d’une unité.</span><span class="sxs-lookup"><span data-stu-id="4eb88-114">Calling this method increments the delay-thread-abort counter for the current thread by one.</span></span>  
  
 <span data-ttu-id="4eb88-115">Les appels à `BeginPreventAsyncAbort` et [ICLRTask2::EndPreventAsyncAbort](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-endpreventasyncabort-method.md) peuvent être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="4eb88-115">Calls to `BeginPreventAsyncAbort` and [ICLRTask2::EndPreventAsyncAbort](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-endpreventasyncabort-method.md) can be nested.</span></span> <span data-ttu-id="4eb88-116">Tant que le compteur est supérieur à zéro, pour le thread actuel abandons de thread.</span><span class="sxs-lookup"><span data-stu-id="4eb88-116">As long as the counter is greater than zero, thread aborts for the current thread are delayed.</span></span> <span data-ttu-id="4eb88-117">Si cet appel n’est pas associé à un appel à la `EndPreventAsyncAbort` (méthode), il est possible d’atteindre un état dans lequel thread abandons ne peut pas être remis au thread actuel.</span><span class="sxs-lookup"><span data-stu-id="4eb88-117">If this call is not paired with a call to the `EndPreventAsyncAbort` method, it is possible to reach a state in which thread aborts cannot be delivered to the current thread.</span></span>  
  
 <span data-ttu-id="4eb88-118">Le délai n’est pas reconnue pour un thread qui abandonne lui-même.</span><span class="sxs-lookup"><span data-stu-id="4eb88-118">The delay is not honored for a thread that aborts itself.</span></span>  
  
 <span data-ttu-id="4eb88-119">La fonctionnalité exposée par cette fonctionnalité est utilisée en interne par la machine virtuelle (VM).</span><span class="sxs-lookup"><span data-stu-id="4eb88-119">The functionality that is exposed by this feature is used internally by the virtual machine (VM).</span></span> <span data-ttu-id="4eb88-120">Une mauvaise utilisation de ces méthodes peut-être provoquer un comportement non spécifié dans la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="4eb88-120">Misuse of these methods may cause unspecified behavior in the VM.</span></span> <span data-ttu-id="4eb88-121">Par exemple, l’appel `EndPreventAsyncAbort` sans appeler d’abord `BeginPreventAsyncAbort` Impossible de définir le compteur à zéro lors de la machine virtuelle a précédemment incrémenté.</span><span class="sxs-lookup"><span data-stu-id="4eb88-121">For example, calling `EndPreventAsyncAbort` without first calling `BeginPreventAsyncAbort` could set the counter to zero when the VM has previously incremented it.</span></span> <span data-ttu-id="4eb88-122">De même, le compteur interne n’est pas vérifié pour dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="4eb88-122">Similarly, the internal counter is not checked for overflow.</span></span> <span data-ttu-id="4eb88-123">S’il dépasse sa limite intégrale, car il est incrémenté par l’hôte et la machine virtuelle, le comportement résultant n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="4eb88-123">If it exceeds its integral limit because it is incremented by both the host and the VM, the resulting behavior is unspecified.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4eb88-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4eb88-124">Requirements</span></span>  
 <span data-ttu-id="4eb88-125">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4eb88-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4eb88-126">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="4eb88-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="4eb88-127">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4eb88-127">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4eb88-128">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4eb88-128">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4eb88-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4eb88-129">See also</span></span>

- [<span data-ttu-id="4eb88-130">EndPreventAsyncAbort, méthode</span><span class="sxs-lookup"><span data-stu-id="4eb88-130">EndPreventAsyncAbort Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-endpreventasyncabort-method.md)
- [<span data-ttu-id="4eb88-131">ICLRTask2, interface</span><span class="sxs-lookup"><span data-stu-id="4eb88-131">ICLRTask2 Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-interface.md)
- [<span data-ttu-id="4eb88-132">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="4eb88-132">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="4eb88-133">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="4eb88-133">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="4eb88-134">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="4eb88-134">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
- [<span data-ttu-id="4eb88-135">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="4eb88-135">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
