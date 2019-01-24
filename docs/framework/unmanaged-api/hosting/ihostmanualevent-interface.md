---
title: IHostManualEvent, interface
ms.date: 03/30/2017
api_name:
- IHostManualEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostManualEvent
helpviewer_keywords:
- IHostManualEvent interface [.NET Framework hosting]
ms.assetid: 300c2661-b7d1-4c39-b080-9ebdef0fd523
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: eb09422872a0d9565be286c25ca1b28d1c45e08f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54501696"
---
# <a name="ihostmanualevent-interface"></a><span data-ttu-id="570b2-102">IHostManualEvent, interface</span><span class="sxs-lookup"><span data-stu-id="570b2-102">IHostManualEvent Interface</span></span>
<span data-ttu-id="570b2-103">Fournit l’implémentation de l’hôte d’une représentation d’un événement de réinitialisation manuelle.</span><span class="sxs-lookup"><span data-stu-id="570b2-103">Provides the host's implementation of a representation of a manual reset event.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="570b2-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="570b2-104">Methods</span></span>  
  
|<span data-ttu-id="570b2-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="570b2-105">Method</span></span>|<span data-ttu-id="570b2-106">Description</span><span class="sxs-lookup"><span data-stu-id="570b2-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="570b2-107">Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="570b2-107">Reset Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-reset-method.md)|<span data-ttu-id="570b2-108">Réinitialise l’actuel `IHostManualEvent` instance à un état non signalé.</span><span class="sxs-lookup"><span data-stu-id="570b2-108">Resets the current `IHostManualEvent` instance to a non-signaled state.</span></span>|  
|[<span data-ttu-id="570b2-109">Set, méthode</span><span class="sxs-lookup"><span data-stu-id="570b2-109">Set Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-set-method.md)|<span data-ttu-id="570b2-110">Définit l’actuel `IHostManualEvent` instance à un état signalé.</span><span class="sxs-lookup"><span data-stu-id="570b2-110">Sets the current `IHostManualEvent` instance to a signaled state.</span></span>|  
|[<span data-ttu-id="570b2-111">Wait, méthode</span><span class="sxs-lookup"><span data-stu-id="570b2-111">Wait Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-wait-method.md)|<span data-ttu-id="570b2-112">Fait en `IHostManualEvent` instance à attendre jusqu'à ce qu’il appartient, ou un certain laps de temps.</span><span class="sxs-lookup"><span data-stu-id="570b2-112">Causes the current `IHostManualEvent` instance to wait until it is owned, or a specified amount of time elapses.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="570b2-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="570b2-113">Requirements</span></span>  
 <span data-ttu-id="570b2-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="570b2-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="570b2-115">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="570b2-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="570b2-116">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="570b2-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="570b2-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="570b2-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="570b2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="570b2-118">See also</span></span>
- [<span data-ttu-id="570b2-119">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="570b2-119">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [<span data-ttu-id="570b2-120">IHostAutoEvent, interface</span><span class="sxs-lookup"><span data-stu-id="570b2-120">IHostAutoEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md)
- [<span data-ttu-id="570b2-121">IHostSemaphore, interface</span><span class="sxs-lookup"><span data-stu-id="570b2-121">IHostSemaphore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-interface.md)
- [<span data-ttu-id="570b2-122">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="570b2-122">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
- [<span data-ttu-id="570b2-123">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="570b2-123">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
