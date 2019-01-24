---
title: ICorDebugController::Continue, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugController.Continue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::Continue
helpviewer_keywords:
- Continue method [.NET Framework debugging]
- ICorDebugController::Continue method [.NET Framework debugging]
ms.assetid: 8684cd06-ad3e-48ef-832e-15320e1f43a2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 115a998f8be233c38efac1a301b4b24b7d861662
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54540180"
---
# <a name="icordebugcontrollercontinue-method"></a><span data-ttu-id="9f01c-102">ICorDebugController::Continue, méthode</span><span class="sxs-lookup"><span data-stu-id="9f01c-102">ICorDebugController::Continue Method</span></span>
<span data-ttu-id="9f01c-103">Reprend l’exécution de threads managés après un appel à [méthode Stop](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-stop-method.md).</span><span class="sxs-lookup"><span data-stu-id="9f01c-103">Resumes execution of managed threads after a call to [Stop Method](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-stop-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f01c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f01c-104">Syntax</span></span>  
  
```  
HRESULT Continue (  
    [in] BOOL fIsOutOfBand  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9f01c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f01c-105">Parameters</span></span>  
 `fIsOutOfBand`  
 <span data-ttu-id="9f01c-106">[in] La valeur `true` s’il continue à partir d’un événement hors-bande ; sinon, la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="9f01c-106">[in] Set to `true` if continuing from an out-of-band event; otherwise, set to `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9f01c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="9f01c-107">Remarks</span></span>  
 <span data-ttu-id="9f01c-108">`Continue` continue le processus après un appel à la `ICorDebugController::Stop` (méthode).</span><span class="sxs-lookup"><span data-stu-id="9f01c-108">`Continue` continues the process after a call to the `ICorDebugController::Stop` method.</span></span>  
  
 <span data-ttu-id="9f01c-109">Lorsque vous effectuez un débogage en mode mixte, n’appelez pas `Continue` sur Win32 thread d’événement, sauf si vous continuez à partir d’un événement hors-bande.</span><span class="sxs-lookup"><span data-stu-id="9f01c-109">When doing mixed-mode debugging, do not call `Continue` on the Win32 event thread unless you are continuing from an out-of-band event.</span></span>  
  
 <span data-ttu-id="9f01c-110">Un *événement dans la bande* est un événement managé ou un événement non managé normal au cours de laquelle le débogueur prend en charge l’interaction avec l’état managé du processus.</span><span class="sxs-lookup"><span data-stu-id="9f01c-110">An *in-band event* is either a managed event or a normal unmanaged event during which the debugger supports interaction with the managed state of the process.</span></span> <span data-ttu-id="9f01c-111">Dans ce cas, le débogueur reçoit le [ICorDebugUnmanagedCallback::DebugEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugunmanagedcallback-debugevent-method.md) rappel avec son `fOutOfBand` paramètre défini sur `false`.</span><span class="sxs-lookup"><span data-stu-id="9f01c-111">In this case, the debugger receives the [ICorDebugUnmanagedCallback::DebugEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugunmanagedcallback-debugevent-method.md) callback with its `fOutOfBand` parameter set to `false`.</span></span>  
  
 <span data-ttu-id="9f01c-112">Un *out-of-band événement* est un événement non managé pendant lequel l’interaction avec l’état managé du processus est impossible pendant le processus est arrêté en raison de l’événement.</span><span class="sxs-lookup"><span data-stu-id="9f01c-112">An *out-of-band event* is an unmanaged event during which interaction with the managed state of the process is impossible while the process is stopped due to the event.</span></span> <span data-ttu-id="9f01c-113">Dans ce cas, le débogueur reçoit le `ICorDebugUnmanagedCallback::DebugEvent` rappel avec son `fOutOfBand` paramètre défini sur `true`.</span><span class="sxs-lookup"><span data-stu-id="9f01c-113">In this case, the debugger receives the `ICorDebugUnmanagedCallback::DebugEvent` callback with its `fOutOfBand` parameter set to `true`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9f01c-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9f01c-114">Requirements</span></span>  
 <span data-ttu-id="9f01c-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9f01c-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9f01c-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9f01c-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9f01c-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9f01c-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9f01c-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9f01c-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f01c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f01c-119">See also</span></span>

