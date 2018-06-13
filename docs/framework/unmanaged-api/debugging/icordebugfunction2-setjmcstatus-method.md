---
title: ICorDebugFunction2::SetJMCStatus, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugFunction2.SetJMCStatus
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction2::SetJMCStatus
helpviewer_keywords:
- ICorDebugFunction2::SetJMCStatus method [.NET Framework debugging]
- SetJMCStatus method, ICorDebugFunction2 interface [.NET Framework debugging]
ms.assetid: 22c27b01-2869-4214-b840-5921f7c874fc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 15b102be5a792f982edeb320199576bdddbd859a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33412358"
---
# <a name="icordebugfunction2setjmcstatus-method"></a><span data-ttu-id="0dda4-102">ICorDebugFunction2::SetJMCStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="0dda4-102">ICorDebugFunction2::SetJMCStatus Method</span></span>
<span data-ttu-id="0dda4-103">Marque la fonction représentée par ICorDebugFunction2 pour uniquement mon Code pas à pas détaillé.</span><span class="sxs-lookup"><span data-stu-id="0dda4-103">Marks the function represented by this ICorDebugFunction2 for Just My Code stepping.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0dda4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0dda4-104">Syntax</span></span>  
  
```  
HRESULT SetJMCStatus (  
    [in] BOOL   bIsJustMyCode  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0dda4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0dda4-105">Parameters</span></span>  
 `bIsJustMyCode`  
 <span data-ttu-id="0dda4-106">[in] La valeur `true` pour marquer la fonction en tant que code utilisateur ; sinon, valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="0dda4-106">[in] Set to `true` to mark the function as user code; otherwise, set to `false`.</span></span>  
  
## <a name="return-values"></a><span data-ttu-id="0dda4-107">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0dda4-107">Return Values</span></span>  
  
|<span data-ttu-id="0dda4-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="0dda4-108">HRESULT</span></span>|<span data-ttu-id="0dda4-109">Description</span><span class="sxs-lookup"><span data-stu-id="0dda4-109">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="0dda4-110">La fonction a été marquée avec succès.</span><span class="sxs-lookup"><span data-stu-id="0dda4-110">The function was successfully marked.</span></span>|  
|`CORDBG_E_FUNCTION_NOT_DEBUGGABLE`|<span data-ttu-id="0dda4-111">La fonction n’a pas pu être marquée comme du code utilisateur, car il ne peut pas être débogué.</span><span class="sxs-lookup"><span data-stu-id="0dda4-111">The function could not be marked as user code because it cannot be debugged.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0dda4-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0dda4-112">Remarks</span></span>  
 <span data-ttu-id="0dda4-113">Une exécution pas à pas uniquement mon Code ignorera le code non-utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0dda4-113">A Just My Code stepper will skip non-user code.</span></span> <span data-ttu-id="0dda4-114">Code utilisateur doit être un sous-ensemble de code pouvant être débogué.</span><span class="sxs-lookup"><span data-stu-id="0dda4-114">User code must be a subset of debuggable code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0dda4-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0dda4-115">Requirements</span></span>  
 <span data-ttu-id="0dda4-116">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0dda4-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0dda4-117">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0dda4-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0dda4-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0dda4-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0dda4-119">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0dda4-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
