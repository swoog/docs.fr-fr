---
title: ICorDebugController::HasQueuedCallbacks, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugController.HasQueuedCallbacks
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::HasQueuedCallbacks
helpviewer_keywords:
- HasQueuedCallbacks method [.NET Framework debugging]
- ICorDebugController::HasQueuedCallbacks method [.NET Framework debugging]
ms.assetid: 0d6a1cd9-370b-4462-adbf-e3980e897ea7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: eba265b727d00690ab77c6ae831e954d59df7c50
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33411608"
---
# <a name="icordebugcontrollerhasqueuedcallbacks-method"></a><span data-ttu-id="2429a-102">ICorDebugController::HasQueuedCallbacks, méthode</span><span class="sxs-lookup"><span data-stu-id="2429a-102">ICorDebugController::HasQueuedCallbacks Method</span></span>
<span data-ttu-id="2429a-103">Obtient une valeur qui indique si des rappels managés sont actuellement en file d’attente pour le thread spécifié.</span><span class="sxs-lookup"><span data-stu-id="2429a-103">Gets a value that indicates whether any managed callbacks are currently queued for the specified thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2429a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2429a-104">Syntax</span></span>  
  
```  
HRESULT HasQueuedCallbacks (  
    [in] ICorDebugThread *pThread,  
    [out] BOOL           *pbQueued  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2429a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2429a-105">Parameters</span></span>  
 `pThread`  
 <span data-ttu-id="2429a-106">[in] Pointeur vers un objet « ICorDebugThread » qui représente le thread.</span><span class="sxs-lookup"><span data-stu-id="2429a-106">[in] A pointer to an "ICorDebugThread" object that represents the thread.</span></span>  
  
 `pbQueued`  
 <span data-ttu-id="2429a-107">[out] Un pointeur vers une valeur qui est `true` si des rappels managés sont actuellement en file d’attente pour le thread spécifié ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="2429a-107">[out] A pointer to a value that is `true` if any managed callbacks are currently queued for the specified thread; otherwise, `false`.</span></span>  
  
 <span data-ttu-id="2429a-108">Si null est spécifié pour le `pThread` paramètre, `HasQueuedCallbacks` retournera `true` s’il n’y rappels managés en file d’attente pour n’importe quel thread.</span><span class="sxs-lookup"><span data-stu-id="2429a-108">If null is specified for the `pThread` parameter, `HasQueuedCallbacks` will return `true` if there are currently managed callbacks queued for any thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2429a-109">Notes</span><span class="sxs-lookup"><span data-stu-id="2429a-109">Remarks</span></span>  
 <span data-ttu-id="2429a-110">Les rappels sont distribués un par un, chaque fois [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="2429a-110">Callbacks will be dispatched one at a time, each time [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) is called.</span></span> <span data-ttu-id="2429a-111">Le débogueur peut contrôler cet indicateur si elle souhaite créer un rapport de plusieurs événements de débogage qui se produisent simultanément.</span><span class="sxs-lookup"><span data-stu-id="2429a-111">The debugger can check this flag if it wants to report multiple debugging events that occur simultaneously.</span></span>  
  
 <span data-ttu-id="2429a-112">Lorsque les événements de débogage sont en attente, ils ont déjà eu lieu, donc le débogueur doit vider la file d’attente entière pour vous assurer de l’état de l’élément débogué.</span><span class="sxs-lookup"><span data-stu-id="2429a-112">When debugging events are queued, they have already occurred, so the debugger must drain the entire queue to be sure of the state of the debuggee.</span></span> <span data-ttu-id="2429a-113">(Appeler `ICorDebugController::Continue` pour vider la file d’attente.) Par exemple, si la file d’attente contient deux événements de débogage sur le thread *X*, et le débogueur suspend le thread *X* après le premier événement de débogage, puis appelle `ICorDebugController::Continue`, le deuxième événement de débogage pour thread *X* sera distribué bien que le thread a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="2429a-113">(Call `ICorDebugController::Continue` to drain the queue.) For example, if the queue contains two debugging events on thread *X*, and the debugger suspends thread *X* after the first debugging event and then calls `ICorDebugController::Continue`, the second debugging event for thread *X* will be dispatched although the thread has been suspended.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2429a-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2429a-114">Requirements</span></span>  
 <span data-ttu-id="2429a-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2429a-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2429a-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2429a-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2429a-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2429a-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2429a-118">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2429a-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2429a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2429a-119">See Also</span></span>  
 
