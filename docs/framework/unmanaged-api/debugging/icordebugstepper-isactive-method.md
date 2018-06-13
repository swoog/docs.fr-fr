---
title: ICorDebugStepper::IsActive, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugStepper.IsActive
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper::IsActive
helpviewer_keywords:
- IsActive method, ICorDebugStepper interface [.NET Framework debugging]
- ICorDebugStepper::IsActive method [.NET Framework debugging]
ms.assetid: 8b35e7a9-b40e-40a9-8d8e-b82e823fc575
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: dcb276e6fba6a1b46b6be630804dc6f07c211b86
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33420506"
---
# <a name="icordebugstepperisactive-method"></a><span data-ttu-id="45c71-102">ICorDebugStepper::IsActive, méthode</span><span class="sxs-lookup"><span data-stu-id="45c71-102">ICorDebugStepper::IsActive Method</span></span>
<span data-ttu-id="45c71-103">Obtient une valeur qui indique si cet ICorDebugStepper exécute actuellement une étape.</span><span class="sxs-lookup"><span data-stu-id="45c71-103">Gets a value that indicates whether this ICorDebugStepper is currently executing a step.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="45c71-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45c71-104">Syntax</span></span>  
  
```  
HRESULT IsActive (  
    [out] BOOL   *pbActive  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="45c71-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45c71-105">Parameters</span></span>  
 `pbActive`  
 <span data-ttu-id="45c71-106">[out] Retourne `true` si l’exécution pas à pas exécute actuellement une étape ; sinon, retourne `false`.</span><span class="sxs-lookup"><span data-stu-id="45c71-106">[out] Returns `true` if the stepper is currently executing a step; otherwise, returns `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="45c71-107">Notes</span><span class="sxs-lookup"><span data-stu-id="45c71-107">Remarks</span></span>  
 <span data-ttu-id="45c71-108">Toute étape reste active jusqu'à ce que le débogueur reçoive un [ICorDebugManagedCallback::StepComplete](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-stepcomplete-method.md) appeler, ce qui désactive automatiquement l’exécution pas à pas.</span><span class="sxs-lookup"><span data-stu-id="45c71-108">Any step action remains active until the debugger receives a [ICorDebugManagedCallback::StepComplete](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-stepcomplete-method.md) call, which automatically deactivates the stepper.</span></span> <span data-ttu-id="45c71-109">Une exécution pas à pas peut également être désactivée prématurément en appelant [ICorDebugStepper::Deactivate](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-deactivate-method.md) avant le rappel condition est atteinte.</span><span class="sxs-lookup"><span data-stu-id="45c71-109">A stepper may also be deactivated prematurely by calling [ICorDebugStepper::Deactivate](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-deactivate-method.md) before the callback condition is reached.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="45c71-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="45c71-110">Requirements</span></span>  
 <span data-ttu-id="45c71-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="45c71-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="45c71-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="45c71-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="45c71-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="45c71-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="45c71-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="45c71-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
