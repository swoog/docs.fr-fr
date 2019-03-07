---
title: ICorDebugController::Stop, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugController.Stop
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::Stop
helpviewer_keywords:
- Stop method, ICorDebugController interface [.NET Framework debugging]
- ICorDebugController::Stop method [.NET Framework debugging]
ms.assetid: c34e79be-a7fb-479e-8dec-d126a4c330e5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fbe0459824499aba86c908012f038256f9923513
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57496683"
---
# <a name="icordebugcontrollerstop-method"></a><span data-ttu-id="b39d9-102">ICorDebugController::Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="b39d9-102">ICorDebugController::Stop Method</span></span>
<span data-ttu-id="b39d9-103">Effectue un arrêt coopératif sur tous les threads qui exécutent du code managé dans le processus.</span><span class="sxs-lookup"><span data-stu-id="b39d9-103">Performs a cooperative stop on all threads that are running managed code in the process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b39d9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b39d9-104">Syntax</span></span>  
  
```  
HRESULT Stop (  
    [in] DWORD dwTimeoutIgnored  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b39d9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b39d9-105">Parameters</span></span>  
 `dwTimeoutIgnored`  
 <span data-ttu-id="b39d9-106">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="b39d9-106">Not used.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b39d9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b39d9-107">Remarks</span></span>  
 <span data-ttu-id="b39d9-108">`Stop` effectue un arrêt coopératif sur tous les threads en cours d’exécution code managé dans le processus.</span><span class="sxs-lookup"><span data-stu-id="b39d9-108">`Stop` performs a cooperative stop on all threads running managed code in the process.</span></span> <span data-ttu-id="b39d9-109">Pendant une session de débogage managé uniquement, les threads non managés peuvent continuer à exécuter (mais sera bloqué lorsque vous tentez d’appeler du code managé).</span><span class="sxs-lookup"><span data-stu-id="b39d9-109">During a managed-only debugging session, unmanaged threads may continue to run (but will be blocked when trying to call managed code).</span></span> <span data-ttu-id="b39d9-110">Pendant une session de débogage d’interopérabilité, les threads non managés seront également arrêtés.</span><span class="sxs-lookup"><span data-stu-id="b39d9-110">During an interop debugging session, unmanaged threads will also be stopped.</span></span> <span data-ttu-id="b39d9-111">Le `dwTimeoutIgnored` valeur est actuellement ignorée et traitée en tant que « Infinite » (-1).</span><span class="sxs-lookup"><span data-stu-id="b39d9-111">The `dwTimeoutIgnored` value is currently ignored and treated as INFINITE (-1).</span></span> <span data-ttu-id="b39d9-112">Si l’arrêt coopératif échoue en raison d’un blocage, tous les threads sont suspendus et E_TIMEOUT est retourné.</span><span class="sxs-lookup"><span data-stu-id="b39d9-112">If the cooperative stop fails due to a deadlock, all threads are suspended and E_TIMEOUT is returned.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b39d9-113">`Stop` est la seule méthode synchrone dans l’API de débogage.</span><span class="sxs-lookup"><span data-stu-id="b39d9-113">`Stop` is the only synchronous method in the debugging API.</span></span> <span data-ttu-id="b39d9-114">Lorsque `Stop` retourne S_OK, le processus est arrêté.</span><span class="sxs-lookup"><span data-stu-id="b39d9-114">When `Stop` returns S_OK, the process is stopped.</span></span> <span data-ttu-id="b39d9-115">Aucun rappel n’est donné à informer les écouteurs de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="b39d9-115">No callback is given to notify listeners of the stop.</span></span> <span data-ttu-id="b39d9-116">Le débogueur doit appeler [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) pour permettre la reprise du processus.</span><span class="sxs-lookup"><span data-stu-id="b39d9-116">The debugger must call [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) to allow the process to resume.</span></span>  
  
 <span data-ttu-id="b39d9-117">Le débogueur gère un compteur de mots vides.</span><span class="sxs-lookup"><span data-stu-id="b39d9-117">The debugger maintains a stop counter.</span></span> <span data-ttu-id="b39d9-118">Lorsque le compteur atteint zéro, le contrôleur est repris.</span><span class="sxs-lookup"><span data-stu-id="b39d9-118">When the counter goes to zero, the controller is resumed.</span></span> <span data-ttu-id="b39d9-119">Chaque appel à `Stop` ou chaque rappel distribué incrémente le compteur.</span><span class="sxs-lookup"><span data-stu-id="b39d9-119">Each call to `Stop` or each dispatched callback increments the counter.</span></span> <span data-ttu-id="b39d9-120">Chaque appel à `ICorDebugController::Continue` décrémente le compteur.</span><span class="sxs-lookup"><span data-stu-id="b39d9-120">Each call to `ICorDebugController::Continue` decrements the counter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b39d9-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b39d9-121">Requirements</span></span>  
 <span data-ttu-id="b39d9-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b39d9-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b39d9-123">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b39d9-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b39d9-124">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b39d9-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b39d9-125">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b39d9-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b39d9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b39d9-126">See also</span></span>

