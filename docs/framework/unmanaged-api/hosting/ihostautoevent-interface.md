---
title: IHostAutoEvent, interface
ms.date: 03/30/2017
api_name:
- IHostAutoEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAutoEvent
helpviewer_keywords:
- IHostAutoEvent interface [.NET Framework hosting]
ms.assetid: 6c1d15c1-a80a-4ee9-b1e4-6e859db6575a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fb5fea403f8210ea93d240aa3aabd4325524b987
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61599453"
---
# <a name="ihostautoevent-interface"></a><span data-ttu-id="cb5ef-102">IHostAutoEvent, interface</span><span class="sxs-lookup"><span data-stu-id="cb5ef-102">IHostAutoEvent Interface</span></span>
<span data-ttu-id="cb5ef-103">Fournit une représentation de l’implémentation de l’hôte d’un événement d’auto-réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="cb5ef-103">Provides a representation of the host's implementation of an auto-reset event.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="cb5ef-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb5ef-104">Methods</span></span>  
  
|<span data-ttu-id="cb5ef-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="cb5ef-105">Method</span></span>|<span data-ttu-id="cb5ef-106">Description</span><span class="sxs-lookup"><span data-stu-id="cb5ef-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="cb5ef-107">Set, méthode</span><span class="sxs-lookup"><span data-stu-id="cb5ef-107">Set Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-set-method.md)|<span data-ttu-id="cb5ef-108">Définit l’actuel `IHostAutoEvent` instance à un état signalé.</span><span class="sxs-lookup"><span data-stu-id="cb5ef-108">Sets the current `IHostAutoEvent` instance to a signaled state.</span></span>|  
|[<span data-ttu-id="cb5ef-109">Wait, méthode</span><span class="sxs-lookup"><span data-stu-id="cb5ef-109">Wait Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-wait-method.md)|<span data-ttu-id="cb5ef-110">Fait en `IHostAutoEvent` instance attendre que l’événement est détenu ou un certain laps de temps.</span><span class="sxs-lookup"><span data-stu-id="cb5ef-110">Causes the current `IHostAutoEvent` instance to wait until the event is owned or a specified amount of time elapses.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="cb5ef-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb5ef-111">Requirements</span></span>  
 <span data-ttu-id="cb5ef-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cb5ef-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cb5ef-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="cb5ef-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="cb5ef-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cb5ef-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cb5ef-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cb5ef-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cb5ef-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb5ef-116">See also</span></span>

- [<span data-ttu-id="cb5ef-117">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="cb5ef-117">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [<span data-ttu-id="cb5ef-118">IHostManualEvent, interface</span><span class="sxs-lookup"><span data-stu-id="cb5ef-118">IHostManualEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md)
- [<span data-ttu-id="cb5ef-119">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="cb5ef-119">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
- [<span data-ttu-id="cb5ef-120">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="cb5ef-120">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
