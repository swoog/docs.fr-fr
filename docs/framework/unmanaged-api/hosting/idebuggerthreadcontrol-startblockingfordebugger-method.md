---
title: IDebuggerThreadControl::StartBlockingForDebugger, méthode
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl.StartBlockingForDebugger
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StartBlockingForDebugger
helpviewer_keywords:
- IDebuggerThreadControl::StartBlockingForDebugger method [.NET Framework hosting]
- StartBlockingForDebugger method [.NET Framework hosting]
ms.assetid: 5c8f11b4-35d3-4c39-9bbd-58b896ba5ba6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 29c999d1561cd4ee035bec379e0f78e762f6946a
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57476274"
---
# <a name="idebuggerthreadcontrolstartblockingfordebugger-method"></a><span data-ttu-id="94557-102">IDebuggerThreadControl::StartBlockingForDebugger, méthode</span><span class="sxs-lookup"><span data-stu-id="94557-102">IDebuggerThreadControl::StartBlockingForDebugger Method</span></span>
<span data-ttu-id="94557-103">Avertit l’hôte que les services de débogage sont sur le point de démarrer tous les threads de blocage.</span><span class="sxs-lookup"><span data-stu-id="94557-103">Notifies the host that the debugging services are about to start blocking all threads.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="94557-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94557-104">Syntax</span></span>  
  
```  
HRESULT StartBlockingForDebugger (  
    [in] DWORD dwUnused  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="94557-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94557-105">Parameters</span></span>  
 `dwUnused`  
 <span data-ttu-id="94557-106">[in] Réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="94557-106">[in] Reserved for future use.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="94557-107">Notes</span><span class="sxs-lookup"><span data-stu-id="94557-107">Remarks</span></span>  
 <span data-ttu-id="94557-108">Le `StartBlockingForDebugger` méthode peut être appelée sur un thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="94557-108">The `StartBlockingForDebugger` method could be called on a runtime thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="94557-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="94557-109">Requirements</span></span>  
 <span data-ttu-id="94557-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="94557-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="94557-111">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="94557-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="94557-112">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="94557-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="94557-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="94557-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94557-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94557-114">See also</span></span>
- [<span data-ttu-id="94557-115">IDebuggerThreadControl, interface</span><span class="sxs-lookup"><span data-stu-id="94557-115">IDebuggerThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-interface.md)
