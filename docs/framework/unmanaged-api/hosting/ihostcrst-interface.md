---
title: IHostCrst, interface
ms.date: 03/30/2017
api_name:
- IHostCrst
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostCrst
helpviewer_keywords:
- IHostCrst interface [.NET Framework hosting]
ms.assetid: ac298ebd-0815-47e4-a823-30b31baab903
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 939f100e8ee386642a29c33827a8339caf0467b9
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59193185"
---
# <a name="ihostcrst-interface"></a><span data-ttu-id="8846a-102">IHostCrst, interface</span><span class="sxs-lookup"><span data-stu-id="8846a-102">IHostCrst Interface</span></span>
<span data-ttu-id="8846a-103">Sert de représentation sous forme de l’hôte d’une section critique de thread.</span><span class="sxs-lookup"><span data-stu-id="8846a-103">Serves as the host's representation of a critical section for threading.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8846a-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8846a-104">Methods</span></span>  
  
|<span data-ttu-id="8846a-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="8846a-105">Method</span></span>|<span data-ttu-id="8846a-106">Description</span><span class="sxs-lookup"><span data-stu-id="8846a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8846a-107">Enter, méthode</span><span class="sxs-lookup"><span data-stu-id="8846a-107">Enter Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-enter-method.md)|<span data-ttu-id="8846a-108">Passe à la section critique.</span><span class="sxs-lookup"><span data-stu-id="8846a-108">Enters the critical section.</span></span>|  
|[<span data-ttu-id="8846a-109">Leave, méthode</span><span class="sxs-lookup"><span data-stu-id="8846a-109">Leave Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-leave-method.md)|<span data-ttu-id="8846a-110">Quitte la section critique.</span><span class="sxs-lookup"><span data-stu-id="8846a-110">Leaves the critical section.</span></span>|  
|[<span data-ttu-id="8846a-111">SetSpinCount, méthode</span><span class="sxs-lookup"><span data-stu-id="8846a-111">SetSpinCount Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-setspincount-method.md)|<span data-ttu-id="8846a-112">Définit le nombre de sélection numérique pour la section critique.</span><span class="sxs-lookup"><span data-stu-id="8846a-112">Sets the spin count for the critical section.</span></span>|  
|[<span data-ttu-id="8846a-113">TryEnter, méthode</span><span class="sxs-lookup"><span data-stu-id="8846a-113">TryEnter Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-tryenter-method.md)|<span data-ttu-id="8846a-114">Tentatives de saisie de la section critique et signale la réussite ou l’échec immédiatement.</span><span class="sxs-lookup"><span data-stu-id="8846a-114">Attempts to enter the critical section, and reports success or failure immediately.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8846a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8846a-115">Remarks</span></span>  
 `IHostCrst` <span data-ttu-id="8846a-116">permet le common language runtime (CLR) de communiquer directement avec la représentation sous forme de l’hôte d’une section critique, au lieu d’utiliser les fonctions Win32 comme `EnterCriticalSection` ou `LeaveCriticalSection`.</span><span class="sxs-lookup"><span data-stu-id="8846a-116">allows the common language runtime (CLR) to communicate directly with the host's representation of a critical section, rather than using Win32 functions such as `EnterCriticalSection` or `LeaveCriticalSection`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8846a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8846a-117">Requirements</span></span>  
 <span data-ttu-id="8846a-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8846a-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8846a-119">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="8846a-119">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8846a-120">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8846a-120">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="8846a-121">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="8846a-121">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="8846a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8846a-122">See also</span></span>

- [<span data-ttu-id="8846a-123">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="8846a-123">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [<span data-ttu-id="8846a-124">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="8846a-124">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
- [<span data-ttu-id="8846a-125">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="8846a-125">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
