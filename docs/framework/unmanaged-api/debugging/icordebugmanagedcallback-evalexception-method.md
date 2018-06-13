---
title: ICorDebugManagedCallback::EvalException, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.EvalException
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::EvalException
helpviewer_keywords:
- EvalException method [.NET Framework debugging]
- ICorDebugManagedCallback::EvalException method [.NET Framework debugging]
ms.assetid: d6036345-18a3-45c1-a302-b1c6f2dced9b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4414bab535b63f55a580e93cc6de9cb0dedc073c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33415514"
---
# <a name="icordebugmanagedcallbackevalexception-method"></a><span data-ttu-id="3416c-102">ICorDebugManagedCallback::EvalException, méthode</span><span class="sxs-lookup"><span data-stu-id="3416c-102">ICorDebugManagedCallback::EvalException Method</span></span>
<span data-ttu-id="3416c-103">Notifie le débogueur qu’une évaluation s’est terminé avec une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="3416c-103">Notifies the debugger that an evaluation has terminated with an unhandled exception.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3416c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3416c-104">Syntax</span></span>  
  
```  
HRESULT EvalException (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *pThread,  
    [in] ICorDebugEval      *pEval  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3416c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3416c-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="3416c-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application dans lequel l’évaluation s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="3416c-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain in which the evaluation terminated.</span></span>  
  
 `pThread`  
 <span data-ttu-id="3416c-107">[in] Pointeur vers un objet ICorDebugThread qui représente le thread dans lequel l’évaluation s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="3416c-107">[in] A pointer to an ICorDebugThread object that represents the thread in which the evaluation terminated.</span></span>  
  
 `pEval`  
 <span data-ttu-id="3416c-108">[in] Pointeur vers un objet ICorDebugEval qui représente le code qui a effectué l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="3416c-108">[in] A pointer to an ICorDebugEval object that represents the code that performed the evaluation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3416c-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3416c-109">Requirements</span></span>  
 <span data-ttu-id="3416c-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3416c-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3416c-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3416c-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3416c-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3416c-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3416c-113">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3416c-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3416c-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3416c-114">See Also</span></span>  
 [<span data-ttu-id="3416c-115">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="3416c-115">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
