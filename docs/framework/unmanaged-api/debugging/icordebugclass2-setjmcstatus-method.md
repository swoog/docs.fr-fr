---
title: ICorDebugClass2::SetJMCStatus, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugClass2.SetJMCStatus
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass2::SetJMCStatus
helpviewer_keywords:
- ICorDebugClass2::SetJMCStatus method [.NET Framework debugging]
- SetJMCStatus method, ICorDebugClass2 interface [.NET Framework debugging]
ms.assetid: 077e6c7f-f857-480c-bebb-76ee1de4e8fc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6ed6570e11008e52d4b1f97c2dc90e2ccbef2e35
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61750616"
---
# <a name="icordebugclass2setjmcstatus-method"></a><span data-ttu-id="17874-102">ICorDebugClass2::SetJMCStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="17874-102">ICorDebugClass2::SetJMCStatus Method</span></span>
<span data-ttu-id="17874-103">Pour chaque méthode de la classe, définit une valeur qui indique si la méthode est un code défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="17874-103">For each method of the class, sets a value that indicates whether the method is user-defined code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="17874-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17874-104">Syntax</span></span>  
  
```  
HRESULT SetJMCStatus (  
    [in] BOOL   bIsJustMyCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="17874-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17874-105">Parameters</span></span>  
 `bIsJustMyCode`  
 <span data-ttu-id="17874-106">[in] La valeur `true` pour indiquer que la méthode est défini par l’utilisateur de code ; sinon, la valeur est `false`.</span><span class="sxs-lookup"><span data-stu-id="17874-106">[in] Set to `true` to indicate that the method is user-defined code; otherwise, set to `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="17874-107">Notes</span><span class="sxs-lookup"><span data-stu-id="17874-107">Remarks</span></span>  
 <span data-ttu-id="17874-108">Un juste mon code (JMC) ignorera le code non défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="17874-108">A just-my-code (JMC) stepper will skip non-user-defined code.</span></span> <span data-ttu-id="17874-109">Code défini par l’utilisateur doit être un sous-ensemble de code pouvant être débogué.</span><span class="sxs-lookup"><span data-stu-id="17874-109">User-defined code must be a subset of debuggable code.</span></span>  
  
 <span data-ttu-id="17874-110">`SetJMCStatus` Retourne une valeur HRESULT de S_FALSE si elle ne parvient pas à définir la valeur de n’importe quelle méthode, même si la valeur pour toutes les autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="17874-110">`SetJMCStatus` returns an HRESULT value of S_FALSE if it fails to set the value for any method, even if it successfully sets the value for all other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="17874-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17874-111">Requirements</span></span>  
 <span data-ttu-id="17874-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="17874-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="17874-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="17874-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="17874-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="17874-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="17874-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="17874-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
