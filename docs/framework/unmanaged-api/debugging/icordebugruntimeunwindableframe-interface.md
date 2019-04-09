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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59134197"
---
# <a name="icordebugruntimeunwindableframe-interface"></a><span data-ttu-id="2aca7-102">ICorDebugRuntimeUnwindableFrame, interface</span><span class="sxs-lookup"><span data-stu-id="2aca7-102">ICorDebugRuntimeUnwindableFrame Interface</span></span>
<span data-ttu-id="2aca7-103">Fournit un support technique pour les méthodes non managées qui requièrent que le Common Language Runtime (CLR) déroule un frame.</span><span class="sxs-lookup"><span data-stu-id="2aca7-103">Provides support for unmanaged methods that require the common language runtime (CLR) to unwind a frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2aca7-104">Notes</span><span class="sxs-lookup"><span data-stu-id="2aca7-104">Remarks</span></span>  
 `ICorDebugRuntimeUnwindableFrame` <span data-ttu-id="2aca7-105">est une version spécialisée de l’interface ICorDebugFrame.</span><span class="sxs-lookup"><span data-stu-id="2aca7-105">is a specialized version of the ICorDebugFrame interface.</span></span> <span data-ttu-id="2aca7-106">Il est utilisé par les méthodes non managées qui nécessitent le runtime déroule un frame sur la pile actuelle.</span><span class="sxs-lookup"><span data-stu-id="2aca7-106">It is used by unmanaged methods that require the runtime to unwind a frame on the current stack.</span></span> <span data-ttu-id="2aca7-107">Conventions de déroulement existantes ne fonctionnent pas, car ils n’utilisent pas de code compilé par JIT.</span><span class="sxs-lookup"><span data-stu-id="2aca7-107">Existing unwinding conventions do not work, because they do not use JIT-compiled code.</span></span> <span data-ttu-id="2aca7-108">Lorsque le débogueur détecte un frame déroulable, il doit utiliser le [ICorDebugStackWalk::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-next-method.md) méthode déroulement, mais il doit exécuter l’inspection lui-même.</span><span class="sxs-lookup"><span data-stu-id="2aca7-108">When the debugger sees an unwindable frame, it should use the [ICorDebugStackWalk::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-next-method.md) method to unwind it, but it should perform inspection itself.</span></span> <span data-ttu-id="2aca7-109">Lorsque le débogueur reçoit un `ICorDebugRuntimeUnwindableFrame`, elle peut appeler le [ICorDebugStackWalk::GetContext](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-getcontext-method.md) méthode pour récupérer le contexte de l’image.</span><span class="sxs-lookup"><span data-stu-id="2aca7-109">When the debugger receives an `ICorDebugRuntimeUnwindableFrame`, it can call the [ICorDebugStackWalk::GetContext](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-getcontext-method.md) method to retrieve the context of the frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2aca7-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2aca7-110">Requirements</span></span>  
 <span data-ttu-id="2aca7-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2aca7-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2aca7-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2aca7-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2aca7-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2aca7-113">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="2aca7-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="2aca7-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="2aca7-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2aca7-115">See also</span></span>

- [<span data-ttu-id="2aca7-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="2aca7-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="2aca7-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="2aca7-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
