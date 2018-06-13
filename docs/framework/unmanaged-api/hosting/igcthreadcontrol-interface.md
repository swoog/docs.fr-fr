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
ms.openlocfilehash: 9296aedf24979624c3d7357a4d51be835716a16f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33438026"
---
# <a name="igcthreadcontrol-interface"></a><span data-ttu-id="b1891-102">IGCThreadControl, interface</span><span class="sxs-lookup"><span data-stu-id="b1891-102">IGCThreadControl Interface</span></span>
<span data-ttu-id="b1891-103">Fournit des méthodes pour participer à la planification des threads qui seraient sinon bloqués pour un garbage collection.</span><span class="sxs-lookup"><span data-stu-id="b1891-103">Provides methods for participating in the scheduling of threads that would otherwise be blocked for a garbage collection.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b1891-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b1891-104">Methods</span></span>  
  
|<span data-ttu-id="b1891-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="b1891-105">Method</span></span>|<span data-ttu-id="b1891-106">Description</span><span class="sxs-lookup"><span data-stu-id="b1891-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b1891-107">SuspensionEnding, méthode</span><span class="sxs-lookup"><span data-stu-id="b1891-107">SuspensionEnding Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-suspensionending-method.md)|<span data-ttu-id="b1891-108">Avertit l’hôte que le runtime est la reprise de threads après un garbage collection ou une suspension.</span><span class="sxs-lookup"><span data-stu-id="b1891-108">Notifies the host that the runtime is resuming threads after a garbage collection or other suspension.</span></span>|  
|[<span data-ttu-id="b1891-109">SuspensionStarting, méthode</span><span class="sxs-lookup"><span data-stu-id="b1891-109">SuspensionStarting Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-suspensionstarting-method.md)|<span data-ttu-id="b1891-110">Avertit l’hôte que le runtime débute une suspension du thread pour un garbage collection ou une suspension.</span><span class="sxs-lookup"><span data-stu-id="b1891-110">Notifies the host that the runtime is beginning a thread suspension for a garbage collection or other suspension.</span></span>|  
|[<span data-ttu-id="b1891-111">ThreadIsBlockingForSuspension, méthode</span><span class="sxs-lookup"><span data-stu-id="b1891-111">ThreadIsBlockingForSuspension Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-threadisblockingforsuspension-method.md)|<span data-ttu-id="b1891-112">Avertit l’hôte que le thread qui effectue l’appel va bloquer, peut-être pour un garbage collection ou une suspension.</span><span class="sxs-lookup"><span data-stu-id="b1891-112">Notifies the host that the thread making the call is about to block, perhaps for a garbage collection or other suspension.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b1891-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b1891-113">Requirements</span></span>  
 <span data-ttu-id="b1891-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b1891-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b1891-115">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="b1891-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b1891-116">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b1891-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b1891-117">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b1891-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1891-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1891-118">See Also</span></span>  
 [<span data-ttu-id="b1891-119">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="b1891-119">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
