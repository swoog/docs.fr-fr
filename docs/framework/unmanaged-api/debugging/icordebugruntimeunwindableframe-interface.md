---
title: ICorDebugRuntimeUnwindableFrame, interface
ms.date: 03/30/2017
api_name:
- ICorDebugUnwindableFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugUnwindableFrame
helpviewer_keywords:
- ICorDebugUnwindableFrame interface [.NET Framework debugging]
ms.assetid: cd6a3982-6ed3-4909-808d-a66055e813e0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bf6bc73683a6c37ceaaffc635a58803b71c3b6cd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61782757"
---
# <a name="icordebugruntimeunwindableframe-interface"></a><span data-ttu-id="eb76a-102">ICorDebugRuntimeUnwindableFrame, interface</span><span class="sxs-lookup"><span data-stu-id="eb76a-102">ICorDebugRuntimeUnwindableFrame Interface</span></span>
<span data-ttu-id="eb76a-103">Fournit un support technique pour les méthodes non managées qui requièrent que le Common Language Runtime (CLR) déroule un frame.</span><span class="sxs-lookup"><span data-stu-id="eb76a-103">Provides support for unmanaged methods that require the common language runtime (CLR) to unwind a frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="eb76a-104">Notes</span><span class="sxs-lookup"><span data-stu-id="eb76a-104">Remarks</span></span>  
 <span data-ttu-id="eb76a-105">`ICorDebugRuntimeUnwindableFrame` est une version spécialisée de l’interface ICorDebugFrame.</span><span class="sxs-lookup"><span data-stu-id="eb76a-105">`ICorDebugRuntimeUnwindableFrame` is a specialized version of the ICorDebugFrame interface.</span></span> <span data-ttu-id="eb76a-106">Il est utilisé par les méthodes non managées qui nécessitent le runtime déroule un frame sur la pile actuelle.</span><span class="sxs-lookup"><span data-stu-id="eb76a-106">It is used by unmanaged methods that require the runtime to unwind a frame on the current stack.</span></span> <span data-ttu-id="eb76a-107">Conventions de déroulement existantes ne fonctionnent pas, car ils n’utilisent pas de code compilé par JIT.</span><span class="sxs-lookup"><span data-stu-id="eb76a-107">Existing unwinding conventions do not work, because they do not use JIT-compiled code.</span></span> <span data-ttu-id="eb76a-108">Lorsque le débogueur détecte un frame déroulable, il doit utiliser le [ICorDebugStackWalk::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-next-method.md) méthode déroulement, mais il doit exécuter l’inspection lui-même.</span><span class="sxs-lookup"><span data-stu-id="eb76a-108">When the debugger sees an unwindable frame, it should use the [ICorDebugStackWalk::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-next-method.md) method to unwind it, but it should perform inspection itself.</span></span> <span data-ttu-id="eb76a-109">Lorsque le débogueur reçoit un `ICorDebugRuntimeUnwindableFrame`, elle peut appeler le [ICorDebugStackWalk::GetContext](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-getcontext-method.md) méthode pour récupérer le contexte de l’image.</span><span class="sxs-lookup"><span data-stu-id="eb76a-109">When the debugger receives an `ICorDebugRuntimeUnwindableFrame`, it can call the [ICorDebugStackWalk::GetContext](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-getcontext-method.md) method to retrieve the context of the frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eb76a-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb76a-110">Requirements</span></span>  
 <span data-ttu-id="eb76a-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="eb76a-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eb76a-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="eb76a-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="eb76a-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eb76a-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eb76a-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eb76a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb76a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb76a-115">See also</span></span>

- [<span data-ttu-id="eb76a-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="eb76a-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="eb76a-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="eb76a-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
