---
title: IDebuggerThreadControl::ReleaseAllRuntimeThreads, méthode
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl.ReleaseAllRuntimeThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ReleaseAllRuntimeThreads
helpviewer_keywords:
- ReleaseAllRuntimeThreads method [.NET Framework hosting]
- IDebuggerThreadControl::ReleaseAllRuntimeThreads method [.NET Framework hosting]
ms.assetid: 1a2995ff-5f02-4b49-84dc-3a5f9cfd7d55
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 136dab5c05c310d85a5e18bcdc6da0de901d3ace
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59227468"
---
# <a name="idebuggerthreadcontrolreleaseallruntimethreads-method"></a><span data-ttu-id="1ab67-102">IDebuggerThreadControl::ReleaseAllRuntimeThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="1ab67-102">IDebuggerThreadControl::ReleaseAllRuntimeThreads Method</span></span>
<span data-ttu-id="1ab67-103">Avertit l’hôte que les services de débogage sont sur le point de mise en production de tous les threads qui sont bloqués.</span><span class="sxs-lookup"><span data-stu-id="1ab67-103">Notifies the host that the debugging services are about to release all threads that are blocked.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ab67-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ab67-104">Syntax</span></span>  
  
```  
HRESULT ReleaseAllRuntimeThreads ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="1ab67-105">Notes</span><span class="sxs-lookup"><span data-stu-id="1ab67-105">Remarks</span></span>  
 <span data-ttu-id="1ab67-106">Le `ReleaseAllRuntimeThreads` méthode ne sera jamais appelée sur un thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1ab67-106">The `ReleaseAllRuntimeThreads` method will never be called on a runtime thread.</span></span> <span data-ttu-id="1ab67-107">Si l’hôte a un thread du runtime bloqué, il doit le libérer maintenant.</span><span class="sxs-lookup"><span data-stu-id="1ab67-107">If the host has a runtime thread blocked, it should release it now.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1ab67-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ab67-108">Requirements</span></span>  
 <span data-ttu-id="1ab67-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1ab67-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1ab67-110">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="1ab67-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1ab67-111">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1ab67-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="1ab67-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="1ab67-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="1ab67-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ab67-113">See also</span></span>

- [<span data-ttu-id="1ab67-114">IDebuggerThreadControl, interface</span><span class="sxs-lookup"><span data-stu-id="1ab67-114">IDebuggerThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-interface.md)
