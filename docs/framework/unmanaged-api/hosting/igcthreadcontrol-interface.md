---
title: IGCThreadControl, interface
ms.date: 03/30/2017
api_name:
- IGCThreadControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IGCThreadControl
helpviewer_keywords:
- IGCThreadControl interface [.NET Framework hosting]
ms.assetid: 3ff04d75-85ac-4df9-886d-dbaa037c0552
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5c00f401bedc1a2810c4e9b3046a45e53a79f1ea
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61992769"
---
# <a name="igcthreadcontrol-interface"></a><span data-ttu-id="ab6b1-102">IGCThreadControl, interface</span><span class="sxs-lookup"><span data-stu-id="ab6b1-102">IGCThreadControl Interface</span></span>
<span data-ttu-id="ab6b1-103">Fournit des méthodes pour participer à la planification des threads qui seraient sinon bloqués pour un garbage collection.</span><span class="sxs-lookup"><span data-stu-id="ab6b1-103">Provides methods for participating in the scheduling of threads that would otherwise be blocked for a garbage collection.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ab6b1-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ab6b1-104">Methods</span></span>  
  
|<span data-ttu-id="ab6b1-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="ab6b1-105">Method</span></span>|<span data-ttu-id="ab6b1-106">Description</span><span class="sxs-lookup"><span data-stu-id="ab6b1-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ab6b1-107">SuspensionEnding, méthode</span><span class="sxs-lookup"><span data-stu-id="ab6b1-107">SuspensionEnding Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-suspensionending-method.md)|<span data-ttu-id="ab6b1-108">Avertit l’hôte que le runtime est reprise des threads après un garbage collection ou une suspension.</span><span class="sxs-lookup"><span data-stu-id="ab6b1-108">Notifies the host that the runtime is resuming threads after a garbage collection or other suspension.</span></span>|  
|[<span data-ttu-id="ab6b1-109">SuspensionStarting, méthode</span><span class="sxs-lookup"><span data-stu-id="ab6b1-109">SuspensionStarting Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-suspensionstarting-method.md)|<span data-ttu-id="ab6b1-110">Avertit l’hôte que le runtime débute une suspension du thread pour un garbage collection ou une suspension.</span><span class="sxs-lookup"><span data-stu-id="ab6b1-110">Notifies the host that the runtime is beginning a thread suspension for a garbage collection or other suspension.</span></span>|  
|[<span data-ttu-id="ab6b1-111">ThreadIsBlockingForSuspension, méthode</span><span class="sxs-lookup"><span data-stu-id="ab6b1-111">ThreadIsBlockingForSuspension Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-threadisblockingforsuspension-method.md)|<span data-ttu-id="ab6b1-112">Avertit l’hôte que le thread qui effectue l’appel va bloquer, peut-être pour une opération garbage collection ou une suspension.</span><span class="sxs-lookup"><span data-stu-id="ab6b1-112">Notifies the host that the thread making the call is about to block, perhaps for a garbage collection or other suspension.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ab6b1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab6b1-113">Requirements</span></span>  
 <span data-ttu-id="ab6b1-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ab6b1-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ab6b1-115">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="ab6b1-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ab6b1-116">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ab6b1-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ab6b1-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ab6b1-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab6b1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab6b1-118">See also</span></span>

- [<span data-ttu-id="ab6b1-119">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="ab6b1-119">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
