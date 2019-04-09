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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59120014"
---
# <a name="icordebugmanagedcallbackevalexception-method"></a><span data-ttu-id="b71a0-102">ICorDebugManagedCallback::EvalException, méthode</span><span class="sxs-lookup"><span data-stu-id="b71a0-102">ICorDebugManagedCallback::EvalException Method</span></span>
<span data-ttu-id="b71a0-103">Notifie le débogueur qu’une évaluation s’est terminée avec une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="b71a0-103">Notifies the debugger that an evaluation has terminated with an unhandled exception.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b71a0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b71a0-104">Syntax</span></span>  
  
```  
HRESULT EvalException (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *pThread,  
    [in] ICorDebugEval      *pEval  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b71a0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b71a0-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="b71a0-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application dans lequel l’évaluation a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="b71a0-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain in which the evaluation terminated.</span></span>  
  
 `pThread`  
 <span data-ttu-id="b71a0-107">[in] Pointeur vers un objet ICorDebugThread qui représente le thread dans lequel l’évaluation a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="b71a0-107">[in] A pointer to an ICorDebugThread object that represents the thread in which the evaluation terminated.</span></span>  
  
 `pEval`  
 <span data-ttu-id="b71a0-108">[in] Pointeur vers un objet ICorDebugEval qui représente le code qui a effectué l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="b71a0-108">[in] A pointer to an ICorDebugEval object that represents the code that performed the evaluation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b71a0-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b71a0-109">Requirements</span></span>  
 <span data-ttu-id="b71a0-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b71a0-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b71a0-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b71a0-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b71a0-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b71a0-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="b71a0-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="b71a0-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="b71a0-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b71a0-114">See also</span></span>

- [<span data-ttu-id="b71a0-115">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="b71a0-115">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
