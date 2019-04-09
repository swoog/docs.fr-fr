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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59138474"
---
# <a name="icordebugcontrollersetallthreadsdebugstate-method"></a><span data-ttu-id="12b5a-102">ICorDebugController::SetAllThreadsDebugState, méthode</span><span class="sxs-lookup"><span data-stu-id="12b5a-102">ICorDebugController::SetAllThreadsDebugState Method</span></span>
<span data-ttu-id="12b5a-103">Définit l’état de débogage de tous les threads managés dans le processus.</span><span class="sxs-lookup"><span data-stu-id="12b5a-103">Sets the debug state of all managed threads in the process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="12b5a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12b5a-104">Syntax</span></span>  
  
```  
HRESULT SetAllThreadsDebugState (  
    [in] CorDebugThreadState  state,  
    [in] ICorDebugThread      *pExceptThisThread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="12b5a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12b5a-105">Parameters</span></span>  
 `state`  
 <span data-ttu-id="12b5a-106">[in] Une valeur de l’énumération « CorDebugThreadState » qui spécifie l’état du thread pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="12b5a-106">[in] A value of the "CorDebugThreadState" enumeration that specifies the state of the thread for debugging.</span></span>  
  
 `pExceptThisThread`  
 <span data-ttu-id="12b5a-107">[in] Pointeur vers un objet « ICorDebugThread » qui représente un thread à exempter le paramètre d’état de débogage.</span><span class="sxs-lookup"><span data-stu-id="12b5a-107">[in] A pointer to an "ICorDebugThread" object that represents a thread to be exempted from the debug state setting.</span></span> <span data-ttu-id="12b5a-108">Si cette valeur est null, aucun thread n’est exempté.</span><span class="sxs-lookup"><span data-stu-id="12b5a-108">If this value is null, no thread is exempted.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="12b5a-109">Notes</span><span class="sxs-lookup"><span data-stu-id="12b5a-109">Remarks</span></span>  
 <span data-ttu-id="12b5a-110">Le `SetAllThreadsDebugState` threads qui ne sont pas visibles par le biais de la méthode peut affecter [EnumerateThreads, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-enumeratethreads-method.md), les threads qui ont été suspendus avec la `SetAllThreadsDebugState` méthode devrez reprise, avec la `SetAllThreadsDebugState` (méthode).</span><span class="sxs-lookup"><span data-stu-id="12b5a-110">The `SetAllThreadsDebugState` method may affect threads that are not visible via [EnumerateThreads Method](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-enumeratethreads-method.md), so threads that were suspended with the `SetAllThreadsDebugState` method will need to be resumed with the `SetAllThreadsDebugState` method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="12b5a-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12b5a-111">Requirements</span></span>  
 <span data-ttu-id="12b5a-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="12b5a-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="12b5a-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="12b5a-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="12b5a-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="12b5a-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="12b5a-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="12b5a-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="12b5a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12b5a-116">See also</span></span>
