---
title: ICLRIoCompletionManager, interface
ms.date: 03/30/2017
api_name:
- ICLRIoCompletionManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRIoCompletionManager
helpviewer_keywords:
- ICLRIoCompletionManager interface [.NET Framework hosting]
ms.assetid: c6c3ace6-e5e7-4450-8cc5-a9a48208c493
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b71c177c7c0cb029fb7cfa734f54c87abf20b348
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54557836"
---
# <a name="iclriocompletionmanager-interface"></a><span data-ttu-id="f16e3-102">ICLRIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="f16e3-102">ICLRIoCompletionManager Interface</span></span>
<span data-ttu-id="f16e3-103">Implémente une méthode de rappel qui permet à l’hôte notifier le common language runtime (CLR) de l’état des e/s spécifié demande.</span><span class="sxs-lookup"><span data-stu-id="f16e3-103">Implements a callback method that allows the host to notify the common language runtime (CLR) of the status of specified I/O requests.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f16e3-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f16e3-104">Methods</span></span>  
  
|<span data-ttu-id="f16e3-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="f16e3-105">Method</span></span>|<span data-ttu-id="f16e3-106">Description</span><span class="sxs-lookup"><span data-stu-id="f16e3-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f16e3-107">OnComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="f16e3-107">OnComplete Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-oncomplete-method.md)|<span data-ttu-id="f16e3-108">Notifie le CLR de l’état d’une requête d’e/s qui a été effectuée à l’aide d’un appel à la [IHostIoCompletionManager::Bind](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-bind-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="f16e3-108">Notifies the CLR of the status of an I/O request that was made by using a call to the [IHostIoCompletionManager::Bind](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-bind-method.md) method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f16e3-109">Notes</span><span class="sxs-lookup"><span data-stu-id="f16e3-109">Remarks</span></span>  
 <span data-ttu-id="f16e3-110">L’hôte implémente l’abstraction de terminaison d’e/s à l’aide de la [IHostIoCompletionManager](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="f16e3-110">The host implements the I/O completion abstraction by using the [IHostIoCompletionManager](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md) interface.</span></span> <span data-ttu-id="f16e3-111">Le CLR effectue les demandes d’e/s via cette interface et l’hôte notifie l’exécution du résultat de ces demandes à l’aide de la `ICLRIoCompletionManager` interface.</span><span class="sxs-lookup"><span data-stu-id="f16e3-111">The CLR makes I/O requests through this interface, and the host notifies the runtime of the outcome of such requests by using the `ICLRIoCompletionManager` interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f16e3-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f16e3-112">Requirements</span></span>  
 <span data-ttu-id="f16e3-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f16e3-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f16e3-114">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f16e3-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f16e3-115">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f16e3-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f16e3-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f16e3-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f16e3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f16e3-117">See also</span></span>
- [<span data-ttu-id="f16e3-118">IHostIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="f16e3-118">IHostIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md)
- [<span data-ttu-id="f16e3-119">IHostThreadPoolManager, interface</span><span class="sxs-lookup"><span data-stu-id="f16e3-119">IHostThreadPoolManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-interface.md)
- [<span data-ttu-id="f16e3-120">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="f16e3-120">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
