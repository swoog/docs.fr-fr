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
ms.openlocfilehash: 602bcd12d1fd4c5806de6db81252731baa447b7b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59120014"
---
# <a name="icordebugmanagedcallbackevalexception-method"></a><span data-ttu-id="c0baf-102">ICorDebugManagedCallback::EvalException, méthode</span><span class="sxs-lookup"><span data-stu-id="c0baf-102">ICorDebugManagedCallback::EvalException Method</span></span>
<span data-ttu-id="c0baf-103">Notifie le débogueur qu’une évaluation s’est terminée avec une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="c0baf-103">Notifies the debugger that an evaluation has terminated with an unhandled exception.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0baf-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0baf-104">Syntax</span></span>  
  
```  
HRESULT EvalException (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *pThread,  
    [in] ICorDebugEval      *pEval  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c0baf-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0baf-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="c0baf-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application dans lequel l’évaluation a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="c0baf-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain in which the evaluation terminated.</span></span>  
  
 `pThread`  
 <span data-ttu-id="c0baf-107">[in] Pointeur vers un objet ICorDebugThread qui représente le thread dans lequel l’évaluation a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="c0baf-107">[in] A pointer to an ICorDebugThread object that represents the thread in which the evaluation terminated.</span></span>  
  
 `pEval`  
 <span data-ttu-id="c0baf-108">[in] Pointeur vers un objet ICorDebugEval qui représente le code qui a effectué l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="c0baf-108">[in] A pointer to an ICorDebugEval object that represents the code that performed the evaluation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c0baf-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0baf-109">Requirements</span></span>  
 <span data-ttu-id="c0baf-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c0baf-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0baf-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c0baf-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c0baf-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c0baf-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c0baf-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c0baf-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0baf-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0baf-114">See also</span></span>

- [<span data-ttu-id="c0baf-115">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="c0baf-115">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
