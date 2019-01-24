---
title: IDebuggerThreadControl, interface
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IDebuggerThreadControl
helpviewer_keywords:
- IDebuggerThreadControl interface [.NET Framework hosting]
ms.assetid: 0a270c42-a7d1-45f1-a64d-fa3e84d14532
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b969f43e48d7292f695e2355dea0eaa36fd0b73a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54593392"
---
# <a name="idebuggerthreadcontrol-interface"></a><span data-ttu-id="0aea6-102">IDebuggerThreadControl, interface</span><span class="sxs-lookup"><span data-stu-id="0aea6-102">IDebuggerThreadControl Interface</span></span>
<span data-ttu-id="0aea6-103">Fournit des méthodes pour notifier l’hôte sur le blocage et déblocage des threads par les services de débogage.</span><span class="sxs-lookup"><span data-stu-id="0aea6-103">Provides methods for notifying the host about the blocking and unblocking of threads by the debugging services.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0aea6-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0aea6-104">Methods</span></span>  
  
|<span data-ttu-id="0aea6-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="0aea6-105">Method</span></span>|<span data-ttu-id="0aea6-106">Description</span><span class="sxs-lookup"><span data-stu-id="0aea6-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0aea6-107">ThreadIsBlockingForDebugger, méthode</span><span class="sxs-lookup"><span data-stu-id="0aea6-107">ThreadIsBlockingForDebugger Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-threadisblockingfordebugger-method.md)|<span data-ttu-id="0aea6-108">Avertit l’hôte que le thread qui envoie ce rappel concerne à blocs dans les services de débogage.</span><span class="sxs-lookup"><span data-stu-id="0aea6-108">Notifies the host that the thread that is sending this callback is about to block within the debugging services.</span></span>|  
|[<span data-ttu-id="0aea6-109">ReleaseAllRuntimeThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="0aea6-109">ReleaseAllRuntimeThreads Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-releaseallruntimethreads-method.md)|<span data-ttu-id="0aea6-110">Avertit l’hôte que les services de débogage sont sur le point de mise en production de tous les threads qui sont bloqués.</span><span class="sxs-lookup"><span data-stu-id="0aea6-110">Notifies the host that the debugging services are about to release all threads that are blocked.</span></span>|  
|[<span data-ttu-id="0aea6-111">StartBlockingForDebugger, méthode</span><span class="sxs-lookup"><span data-stu-id="0aea6-111">StartBlockingForDebugger Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-startblockingfordebugger-method.md)|<span data-ttu-id="0aea6-112">Avertit l’hôte que les services de débogage sont sur le point de démarrer tous les threads de blocage.</span><span class="sxs-lookup"><span data-stu-id="0aea6-112">Notifies the host that the debugging services are about to start blocking all threads.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0aea6-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0aea6-113">Requirements</span></span>  
 <span data-ttu-id="0aea6-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0aea6-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0aea6-115">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="0aea6-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0aea6-116">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0aea6-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0aea6-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0aea6-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0aea6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0aea6-118">See also</span></span>
- [<span data-ttu-id="0aea6-119">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="0aea6-119">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
