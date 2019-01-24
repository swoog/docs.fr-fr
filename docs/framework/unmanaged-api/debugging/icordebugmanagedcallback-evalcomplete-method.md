---
title: ICorDebugManagedCallback::EvalComplete, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.EvalComplete
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::EvalComplete
helpviewer_keywords:
- ICorDebugManagedCallback::EvalComplete method [.NET Framework debugging]
- EvalComplete method [.NET Framework debugging]
ms.assetid: f74ab4eb-cd1b-407c-a66d-8ec0d85647f3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3243429f52bda58953296c4bb32624440792ad02
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54636467"
---
# <a name="icordebugmanagedcallbackevalcomplete-method"></a><span data-ttu-id="88d2e-102">ICorDebugManagedCallback::EvalComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="88d2e-102">ICorDebugManagedCallback::EvalComplete Method</span></span>
<span data-ttu-id="88d2e-103">Notifie le débogueur qu’une évaluation a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="88d2e-103">Notifies the debugger that an evaluation has been completed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="88d2e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88d2e-104">Syntax</span></span>  
  
```  
HRESULT EvalComplete (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *pThread,  
    [in] ICorDebugEval      *pEval  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="88d2e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88d2e-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="88d2e-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application dans lequel l’évaluation a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="88d2e-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain in which the evaluation was performed.</span></span>  
  
 `pThread`  
 <span data-ttu-id="88d2e-107">[in] Pointeur vers un objet ICorDebugThread qui représente le thread dans lequel l’évaluation a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="88d2e-107">[in] A pointer to an ICorDebugThread object that represents the thread in which the evaluation was performed.</span></span>  
  
 `pEval`  
 <span data-ttu-id="88d2e-108">[in] Pointeur vers un objet ICorDebugEval qui représente le code qui a effectué l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="88d2e-108">[in] A pointer to an ICorDebugEval object that represents the code that performed the evaluation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="88d2e-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="88d2e-109">Requirements</span></span>  
 <span data-ttu-id="88d2e-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="88d2e-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="88d2e-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="88d2e-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="88d2e-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="88d2e-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="88d2e-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="88d2e-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="88d2e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88d2e-114">See also</span></span>
- [<span data-ttu-id="88d2e-115">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="88d2e-115">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
