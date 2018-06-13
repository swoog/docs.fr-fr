---
title: ICorDebugStepper::StepOut, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugStepper.StepOut
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper::StepOut
helpviewer_keywords:
- ICorDebugStepper::StepOut method [.NET Framework debugging]
- StepOut method [.NET Framework debugging]
ms.assetid: aae0f48c-4ede-4256-9251-a7fc85a229dc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f663f5134cf34bf9beb66da20bbb5886baff5415
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33419164"
---
# <a name="icordebugstepperstepout-method"></a><span data-ttu-id="8552c-102">ICorDebugStepper::StepOut, méthode</span><span class="sxs-lookup"><span data-stu-id="8552c-102">ICorDebugStepper::StepOut Method</span></span>
<span data-ttu-id="8552c-103">Provoque un ICorDebugStepper exécute pas à pas son thread conteneur et se termine lorsque le frame actuel retourne le contrôle au frame appelant.</span><span class="sxs-lookup"><span data-stu-id="8552c-103">Causes this ICorDebugStepper to single-step through its containing thread, and to complete when the current frame returns control to the calling frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8552c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8552c-104">Syntax</span></span>  
  
```  
HRESULT StepOut ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="8552c-105">Notes</span><span class="sxs-lookup"><span data-stu-id="8552c-105">Remarks</span></span>  
 <span data-ttu-id="8552c-106">A `StepOut` opération se termine après le retour normal du frame actuel au frame appelant.</span><span class="sxs-lookup"><span data-stu-id="8552c-106">A `StepOut` operation will complete after returning normally from the current frame to the calling frame.</span></span>  
  
 <span data-ttu-id="8552c-107">Si `StepOut` est appelée lorsque en code non managé, l’étape se termine lorsque le frame actuel retourne du code managé qui l’a appelée.</span><span class="sxs-lookup"><span data-stu-id="8552c-107">If `StepOut` is called when in unmanaged code, the step will complete when the current frame returns to the managed code that called it.</span></span>  
  
 <span data-ttu-id="8552c-108">Dans le .NET Framework version 2.0, n’utilisez pas `StepOut` avec l’indicateur STOP_UNMANAGED ensemble, car elle échouera.</span><span class="sxs-lookup"><span data-stu-id="8552c-108">In the .NET Framework version 2.0, do not use `StepOut` with the STOP_UNMANAGED flag set because it will fail.</span></span> <span data-ttu-id="8552c-109">(Utilisez [ICorDebugStepper::SetUnmappedStopMask](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setunmappedstopmask-method.md) pour définir les indicateurs d’exécution pas à pas.) Les débogueurs d’interopérabilité doivent sortir en code natif eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="8552c-109">(Use [ICorDebugStepper::SetUnmappedStopMask](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setunmappedstopmask-method.md) to set flags for stepping.) Interop debuggers must step out to native code themselves.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8552c-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8552c-110">Requirements</span></span>  
 <span data-ttu-id="8552c-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8552c-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8552c-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8552c-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8552c-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8552c-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8552c-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8552c-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
