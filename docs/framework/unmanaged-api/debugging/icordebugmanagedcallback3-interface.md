---
title: ICorDebugManagedCallback3, interface
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback3
helpviewer_keywords:
- ICorDebugManagedCallback3 interface [.NET Framework debugging]
ms.assetid: a95389d3-cf2e-47a4-9805-61426acc6b65
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: acab49097059081540ec364d7f134d31432988a3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59108275"
---
# <a name="icordebugmanagedcallback3-interface"></a><span data-ttu-id="5795d-102">ICorDebugManagedCallback3, interface</span><span class="sxs-lookup"><span data-stu-id="5795d-102">ICorDebugManagedCallback3 Interface</span></span>
<span data-ttu-id="5795d-103">Fournit une méthode de rappel indiquant qu'une notification de débogueur personnalisée active a été déclenchée.</span><span class="sxs-lookup"><span data-stu-id="5795d-103">Provides a callback method that indicates that an enabled custom debugger notification has been raised.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5795d-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5795d-104">Methods</span></span>  
  
|<span data-ttu-id="5795d-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="5795d-105">Method</span></span>|<span data-ttu-id="5795d-106">Description</span><span class="sxs-lookup"><span data-stu-id="5795d-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5795d-107">CustomNotification, méthode</span><span class="sxs-lookup"><span data-stu-id="5795d-107">CustomNotification Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback3-customnotification-method.md)|<span data-ttu-id="5795d-108">Indique qu’une notification de débogueur personnalisée active a été déclenchée.</span><span class="sxs-lookup"><span data-stu-id="5795d-108">Indicates that an enabled custom debugger notification has been raised.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5795d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="5795d-109">Remarks</span></span>  
 <span data-ttu-id="5795d-110">Cette interface est une extension logique de la [ICorDebugManagedCallback](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md) et [ICorDebugManagedCallback2](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md) interfaces.</span><span class="sxs-lookup"><span data-stu-id="5795d-110">This interface is a logical extension of the [ICorDebugManagedCallback](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md) and [ICorDebugManagedCallback2](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md) interfaces.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5795d-111">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="5795d-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5795d-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5795d-112">Requirements</span></span>  
 <span data-ttu-id="5795d-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5795d-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5795d-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5795d-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5795d-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5795d-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5795d-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5795d-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5795d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5795d-117">See also</span></span>

- [<span data-ttu-id="5795d-118">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="5795d-118">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
- [<span data-ttu-id="5795d-119">ICorDebugManagedCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="5795d-119">ICorDebugManagedCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md)
- [<span data-ttu-id="5795d-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="5795d-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="5795d-121">Débogage</span><span class="sxs-lookup"><span data-stu-id="5795d-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
