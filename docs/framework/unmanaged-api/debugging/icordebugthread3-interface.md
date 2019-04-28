---
title: ICorDebugThread3, interface
ms.date: 03/30/2017
api_name:
- ICorDebugThread3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread3
helpviewer_keywords:
- ICorDebugThread3 interface [.NET Framework debugging]
ms.assetid: eb2860ef-06cb-4968-a6c3-6d048ecda2a4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1d34a3395605505ca0ebda072e33d8083d51123a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61902419"
---
# <a name="icordebugthread3-interface"></a><span data-ttu-id="f854f-102">ICorDebugThread3, interface</span><span class="sxs-lookup"><span data-stu-id="f854f-102">ICorDebugThread3 Interface</span></span>
<span data-ttu-id="f854f-103">Fournit le point d’entrée pour le [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) et les interfaces correspondantes.</span><span class="sxs-lookup"><span data-stu-id="f854f-103">Provides the entry point to the [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) and corresponding interfaces.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f854f-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f854f-104">Methods</span></span>  
  
|<span data-ttu-id="f854f-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="f854f-105">Method</span></span>|<span data-ttu-id="f854f-106">Description</span><span class="sxs-lookup"><span data-stu-id="f854f-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f854f-107">CreateStackWalk, méthode</span><span class="sxs-lookup"><span data-stu-id="f854f-107">CreateStackWalk Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread3-createstackwalk-method.md)|<span data-ttu-id="f854f-108">Crée un [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) objet pour le thread dont vous souhaitez dérouler la pile.</span><span class="sxs-lookup"><span data-stu-id="f854f-108">Creates an [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) object for the thread whose stack you want to unwind.</span></span>|  
|[<span data-ttu-id="f854f-109">GetActiveInternalFrames, méthode</span><span class="sxs-lookup"><span data-stu-id="f854f-109">GetActiveInternalFrames Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread3-getactiveinternalframes-method.md)|<span data-ttu-id="f854f-110">Retourne un tableau de frames internes ([ICorDebugInternalFrame2](../../../../docs/framework/unmanaged-api/debugging/icordebuginternalframe2-interface.md) objets) sur la pile.</span><span class="sxs-lookup"><span data-stu-id="f854f-110">Returns an array of internal frames ([ICorDebugInternalFrame2](../../../../docs/framework/unmanaged-api/debugging/icordebuginternalframe2-interface.md) objects) on the stack.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f854f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f854f-111">Remarks</span></span>  
 <span data-ttu-id="f854f-112">`ICorDebugThread3` est une extension logique à l’interface ICorDebugThread.</span><span class="sxs-lookup"><span data-stu-id="f854f-112">`ICorDebugThread3` is a logical extension to the ICorDebugThread interface.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f854f-113">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="f854f-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f854f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f854f-114">Requirements</span></span>  
 <span data-ttu-id="f854f-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f854f-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f854f-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f854f-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f854f-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f854f-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f854f-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f854f-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f854f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f854f-119">See also</span></span>

- [<span data-ttu-id="f854f-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="f854f-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="f854f-121">Débogage</span><span class="sxs-lookup"><span data-stu-id="f854f-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
