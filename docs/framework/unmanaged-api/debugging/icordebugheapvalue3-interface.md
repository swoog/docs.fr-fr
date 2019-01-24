---
title: ICorDebugHeapValue3, interface
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue3
helpviewer_keywords:
- ICorDebugHeapValue3 interface [.NET Framework debugging]
ms.assetid: 9c421bb0-e647-4b2d-a986-f3d578cc7f20
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 08a9bc8aa4aa70ad6b01c58abccd145ae43d8a52
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54568289"
---
# <a name="icordebugheapvalue3-interface"></a><span data-ttu-id="abd16-102">ICorDebugHeapValue3, interface</span><span class="sxs-lookup"><span data-stu-id="abd16-102">ICorDebugHeapValue3 Interface</span></span>
<span data-ttu-id="abd16-103">Expose les propriétés du verrou du moniteur d'objets.</span><span class="sxs-lookup"><span data-stu-id="abd16-103">Exposes the monitor lock properties of objects.</span></span> <span data-ttu-id="abd16-104">Cette interface étend les interfaces ICorDebugHeapValue et ICorDebugHeapValue2.</span><span class="sxs-lookup"><span data-stu-id="abd16-104">This interface extends the ICorDebugHeapValue and ICorDebugHeapValue2 interfaces.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="abd16-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="abd16-105">Methods</span></span>  
  
|<span data-ttu-id="abd16-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="abd16-106">Method</span></span>|<span data-ttu-id="abd16-107">Description</span><span class="sxs-lookup"><span data-stu-id="abd16-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="abd16-108">GetThreadOwningMonitorLock, méthode</span><span class="sxs-lookup"><span data-stu-id="abd16-108">GetThreadOwningMonitorLock Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugheapvalue3-getthreadowningmonitorlock-method.md)|<span data-ttu-id="abd16-109">Retourne le thread managé qui possède le verrou du moniteur sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="abd16-109">Returns the managed thread that owns the monitor lock on this object.</span></span>|  
|[<span data-ttu-id="abd16-110">GetMonitorEventWaitList, méthode</span><span class="sxs-lookup"><span data-stu-id="abd16-110">GetMonitorEventWaitList Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugheapvalue3-getmonitoreventwaitlist-method.md)|<span data-ttu-id="abd16-111">Fournit une liste ordonnée de threads qui sont en attente sur l’événement qui est associé à un verrou du moniteur.</span><span class="sxs-lookup"><span data-stu-id="abd16-111">Provides an ordered list of threads that are queued on the event that is associated with a monitor lock.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="abd16-112">Notes</span><span class="sxs-lookup"><span data-stu-id="abd16-112">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="abd16-113">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="abd16-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="abd16-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="abd16-114">Requirements</span></span>  
 <span data-ttu-id="abd16-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="abd16-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="abd16-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="abd16-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="abd16-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="abd16-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="abd16-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="abd16-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="abd16-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abd16-119">See also</span></span>
- [<span data-ttu-id="abd16-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="abd16-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="abd16-121">Débogage</span><span class="sxs-lookup"><span data-stu-id="abd16-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
