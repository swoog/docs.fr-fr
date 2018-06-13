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
ms.openlocfilehash: c3abb3e80226da909a0c7eb8e4bf54959557dcbf
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33436265"
---
# <a name="iclriocompletionmanager-interface"></a><span data-ttu-id="dc654-102">ICLRIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="dc654-102">ICLRIoCompletionManager Interface</span></span>
<span data-ttu-id="dc654-103">Implémente une méthode de rappel qui permet à l’hôte notifier le common language runtime (CLR) de l’état d’e/s spécifié des demandes.</span><span class="sxs-lookup"><span data-stu-id="dc654-103">Implements a callback method that allows the host to notify the common language runtime (CLR) of the status of specified I/O requests.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="dc654-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dc654-104">Methods</span></span>  
  
|<span data-ttu-id="dc654-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="dc654-105">Method</span></span>|<span data-ttu-id="dc654-106">Description</span><span class="sxs-lookup"><span data-stu-id="dc654-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="dc654-107">OnComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="dc654-107">OnComplete Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-oncomplete-method.md)|<span data-ttu-id="dc654-108">Notifie le CLR de l’état d’une demande d’e/s qui a été effectuée à l’aide d’un appel à la [IHostIoCompletionManager::Bind](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-bind-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="dc654-108">Notifies the CLR of the status of an I/O request that was made by using a call to the [IHostIoCompletionManager::Bind](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-bind-method.md) method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dc654-109">Notes</span><span class="sxs-lookup"><span data-stu-id="dc654-109">Remarks</span></span>  
 <span data-ttu-id="dc654-110">L’hôte implémente l’abstraction de terminaison d’e/s à l’aide de la [IHostIoCompletionManager](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="dc654-110">The host implements the I/O completion abstraction by using the [IHostIoCompletionManager](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md) interface.</span></span> <span data-ttu-id="dc654-111">Le CLR effectue les demandes d’e/s via cette interface et l’hôte notifie l’exécution du résultat de ces requêtes à l’aide de la `ICLRIoCompletionManager` interface.</span><span class="sxs-lookup"><span data-stu-id="dc654-111">The CLR makes I/O requests through this interface, and the host notifies the runtime of the outcome of such requests by using the `ICLRIoCompletionManager` interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dc654-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dc654-112">Requirements</span></span>  
 <span data-ttu-id="dc654-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dc654-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dc654-114">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="dc654-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="dc654-115">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="dc654-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="dc654-116">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dc654-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc654-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc654-117">See Also</span></span>  
 [<span data-ttu-id="dc654-118">IHostIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="dc654-118">IHostIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md)  
 [<span data-ttu-id="dc654-119">IHostThreadPoolManager, interface</span><span class="sxs-lookup"><span data-stu-id="dc654-119">IHostThreadPoolManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-interface.md)  
 [<span data-ttu-id="dc654-120">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="dc654-120">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
