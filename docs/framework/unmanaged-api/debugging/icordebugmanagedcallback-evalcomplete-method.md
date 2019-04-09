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
ms.openlocfilehash: c1261942865419762fa454eb8d4bc5e5d99e86d6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59193172"
---
# <a name="icordebugmanagedcallbackevalcomplete-method"></a><span data-ttu-id="2f504-102">ICorDebugManagedCallback::EvalComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="2f504-102">ICorDebugManagedCallback::EvalComplete Method</span></span>
<span data-ttu-id="2f504-103">Notifie le débogueur qu’une évaluation a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="2f504-103">Notifies the debugger that an evaluation has been completed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2f504-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f504-104">Syntax</span></span>  
  
```  
HRESULT EvalComplete (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *pThread,  
    [in] ICorDebugEval      *pEval  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2f504-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f504-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="2f504-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application dans lequel l’évaluation a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="2f504-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain in which the evaluation was performed.</span></span>  
  
 `pThread`  
 <span data-ttu-id="2f504-107">[in] Pointeur vers un objet ICorDebugThread qui représente le thread dans lequel l’évaluation a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="2f504-107">[in] A pointer to an ICorDebugThread object that represents the thread in which the evaluation was performed.</span></span>  
  
 `pEval`  
 <span data-ttu-id="2f504-108">[in] Pointeur vers un objet ICorDebugEval qui représente le code qui a effectué l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="2f504-108">[in] A pointer to an ICorDebugEval object that represents the code that performed the evaluation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2f504-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f504-109">Requirements</span></span>  
 <span data-ttu-id="2f504-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2f504-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2f504-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2f504-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2f504-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2f504-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="2f504-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="2f504-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="2f504-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f504-114">See also</span></span>

- [<span data-ttu-id="2f504-115">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="2f504-115">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
