---
title: ICorDebugController::SetAllThreadsDebugState, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugController.SetAllThreadsDebugState
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::SetAllThreadsDebugState
helpviewer_keywords:
- SetAllThreadsDebugState method [.NET Framework debugging]
- ICorDebugController::SetAllThreadsDebugState method [.NET Framework debugging]
ms.assetid: bdda4bd7-4743-4d58-a22b-8067e967db95
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 280dc3f0271d7326fe4c22b813abebfd4d45c89e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59138474"
---
# <a name="icordebugcontrollersetallthreadsdebugstate-method"></a><span data-ttu-id="a282d-102">ICorDebugController::SetAllThreadsDebugState, méthode</span><span class="sxs-lookup"><span data-stu-id="a282d-102">ICorDebugController::SetAllThreadsDebugState Method</span></span>
<span data-ttu-id="a282d-103">Définit l’état de débogage de tous les threads managés dans le processus.</span><span class="sxs-lookup"><span data-stu-id="a282d-103">Sets the debug state of all managed threads in the process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a282d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a282d-104">Syntax</span></span>  
  
```  
HRESULT SetAllThreadsDebugState (  
    [in] CorDebugThreadState  state,  
    [in] ICorDebugThread      *pExceptThisThread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a282d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a282d-105">Parameters</span></span>  
 `state`  
 <span data-ttu-id="a282d-106">[in] Une valeur de l’énumération « CorDebugThreadState » qui spécifie l’état du thread pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="a282d-106">[in] A value of the "CorDebugThreadState" enumeration that specifies the state of the thread for debugging.</span></span>  
  
 `pExceptThisThread`  
 <span data-ttu-id="a282d-107">[in] Pointeur vers un objet « ICorDebugThread » qui représente un thread à exempter le paramètre d’état de débogage.</span><span class="sxs-lookup"><span data-stu-id="a282d-107">[in] A pointer to an "ICorDebugThread" object that represents a thread to be exempted from the debug state setting.</span></span> <span data-ttu-id="a282d-108">Si cette valeur est null, aucun thread n’est exempté.</span><span class="sxs-lookup"><span data-stu-id="a282d-108">If this value is null, no thread is exempted.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a282d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a282d-109">Remarks</span></span>  
 <span data-ttu-id="a282d-110">Le `SetAllThreadsDebugState` threads qui ne sont pas visibles par le biais de la méthode peut affecter [EnumerateThreads, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-enumeratethreads-method.md), les threads qui ont été suspendus avec la `SetAllThreadsDebugState` méthode devrez reprise, avec la `SetAllThreadsDebugState` (méthode).</span><span class="sxs-lookup"><span data-stu-id="a282d-110">The `SetAllThreadsDebugState` method may affect threads that are not visible via [EnumerateThreads Method](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-enumeratethreads-method.md), so threads that were suspended with the `SetAllThreadsDebugState` method will need to be resumed with the `SetAllThreadsDebugState` method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a282d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a282d-111">Requirements</span></span>  
 <span data-ttu-id="a282d-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a282d-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a282d-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a282d-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a282d-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a282d-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a282d-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a282d-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a282d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a282d-116">See also</span></span>
