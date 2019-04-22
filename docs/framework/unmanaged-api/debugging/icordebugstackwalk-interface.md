---
title: ICorDebugStackWalk, interface
ms.date: 03/30/2017
api_name:
- ICorDebugStackWalk
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStackWalk
helpviewer_keywords:
- ICorDebugStackWalk interface [.NET Framework debugging]
ms.assetid: 16d695e8-975d-431b-8421-e9e6c3e3f476
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e33e9be112a6a10f89b88005496ce2e63dff2d54
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59080681"
---
# <a name="icordebugstackwalk-interface"></a><span data-ttu-id="b73bf-102">ICorDebugStackWalk, interface</span><span class="sxs-lookup"><span data-stu-id="b73bf-102">ICorDebugStackWalk Interface</span></span>
<span data-ttu-id="b73bf-103">Fournit des méthodes pour obtenir les méthodes managées, ou frames, sur la pile d'un thread.</span><span class="sxs-lookup"><span data-stu-id="b73bf-103">Provides methods for getting the managed methods, or frames, on a thread’s stack.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b73bf-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b73bf-104">Methods</span></span>  
  
|<span data-ttu-id="b73bf-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="b73bf-105">Method</span></span>|<span data-ttu-id="b73bf-106">Description</span><span class="sxs-lookup"><span data-stu-id="b73bf-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b73bf-107">GetContext, méthode</span><span class="sxs-lookup"><span data-stu-id="b73bf-107">GetContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-getcontext-method.md)|<span data-ttu-id="b73bf-108">Retourne le contexte pour le frame actuel dans le `ICorDebugStackWalk` objet.</span><span class="sxs-lookup"><span data-stu-id="b73bf-108">Returns the context for the current frame in the `ICorDebugStackWalk` object.</span></span>|  
|[<span data-ttu-id="b73bf-109">SetContext, méthode</span><span class="sxs-lookup"><span data-stu-id="b73bf-109">SetContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-setcontext-method.md)|<span data-ttu-id="b73bf-110">Définit le `ICorDebugStackWalk` contexte actuel de l’objet à un contexte valid pour le thread.</span><span class="sxs-lookup"><span data-stu-id="b73bf-110">Sets the `ICorDebugStackWalk` object’s current context to a valid context for the thread.</span></span>|  
|[<span data-ttu-id="b73bf-111">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="b73bf-111">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-next-method.md)|<span data-ttu-id="b73bf-112">Déplace le `ICorDebugStackWalk` objet vers le frame suivant.</span><span class="sxs-lookup"><span data-stu-id="b73bf-112">Moves the `ICorDebugStackWalk` object to the next frame.</span></span>|  
|[<span data-ttu-id="b73bf-113">GetFrame, méthode</span><span class="sxs-lookup"><span data-stu-id="b73bf-113">GetFrame Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-getframe-method.md)|<span data-ttu-id="b73bf-114">Obtient le frame actuel le `ICorDebugStackWalk` objet.</span><span class="sxs-lookup"><span data-stu-id="b73bf-114">Gets the current frame in the `ICorDebugStackWalk` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b73bf-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b73bf-115">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b73bf-116">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="b73bf-116">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b73bf-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b73bf-117">Requirements</span></span>  
 <span data-ttu-id="b73bf-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b73bf-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b73bf-119">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b73bf-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b73bf-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b73bf-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b73bf-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b73bf-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b73bf-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b73bf-122">See also</span></span>

- [<span data-ttu-id="b73bf-123">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="b73bf-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="b73bf-124">Débogage</span><span class="sxs-lookup"><span data-stu-id="b73bf-124">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
