---
title: ICorDebugEval::GetResult, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEval.GetResult
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::GetResult
helpviewer_keywords:
- ICorDebugEval::GetResult method [.NET Framework debugging]
- GetResult method [.NET Framework debugging]
ms.assetid: 50dbb9af-58a1-41f4-b56d-3da20011884f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7e160eddf667b542929c8dd3790de666a8e8bb77
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33413057"
---
# <a name="icordebugevalgetresult-method"></a><span data-ttu-id="b512f-102">ICorDebugEval::GetResult, méthode</span><span class="sxs-lookup"><span data-stu-id="b512f-102">ICorDebugEval::GetResult Method</span></span>
<span data-ttu-id="b512f-103">Obtient les résultats de cette évaluation.</span><span class="sxs-lookup"><span data-stu-id="b512f-103">Gets the results of this evaluation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b512f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b512f-104">Syntax</span></span>  
  
```  
HRESULT GetResult (  
    [out] ICorDebugValue    **ppResult  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b512f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b512f-105">Parameters</span></span>  
 `ppResult`  
 <span data-ttu-id="b512f-106">[out] Pointeur vers l’adresse d’un objet ICorDebugValue qui représente les résultats de cette évaluation, si l’évaluation s’exécute normalement.</span><span class="sxs-lookup"><span data-stu-id="b512f-106">[out] Pointer to the address of an ICorDebugValue object that represents the results of this evaluation, if the evaluation completes normally.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b512f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b512f-107">Remarks</span></span>  
 <span data-ttu-id="b512f-108">Le `GetResult` méthode est valide uniquement lorsque l’évaluation est terminée.</span><span class="sxs-lookup"><span data-stu-id="b512f-108">The `GetResult` method is valid only after the evaluation is completed.</span></span>  
  
 <span data-ttu-id="b512f-109">Si l’évaluation s’exécute normalement, `ppResult` spécifie les résultats.</span><span class="sxs-lookup"><span data-stu-id="b512f-109">If the evaluation completes normally, `ppResult` specifies the results.</span></span> <span data-ttu-id="b512f-110">Si elle se termine avec une exception, le résultat est l’exception levée.</span><span class="sxs-lookup"><span data-stu-id="b512f-110">If it terminates with an exception, the result is the exception thrown.</span></span> <span data-ttu-id="b512f-111">Si l’évaluation a été d’un nouvel objet, le résultat est la référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="b512f-111">If the evaluation was for a new object, the result is the reference to the new object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b512f-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b512f-112">Requirements</span></span>  
 <span data-ttu-id="b512f-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b512f-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b512f-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b512f-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b512f-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b512f-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b512f-116">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b512f-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
