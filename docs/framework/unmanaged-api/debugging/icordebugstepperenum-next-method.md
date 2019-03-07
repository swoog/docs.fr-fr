---
title: ICorDebugStepperEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugStepperEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepperEnum::Next
helpviewer_keywords:
- Next method, ICorDebugStepperEnum interface [.NET Framework debugging]
- ICorDebugStepperEnum::Next method [.NET Framework debugging]
ms.assetid: d0ea0f30-e8d2-48b0-8477-e1a029ceb4dd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6ac3165ab17eb1b4bc55a4bee4d2d2b467f8aefe
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57494595"
---
# <a name="icordebugstepperenumnext-method"></a><span data-ttu-id="e016b-102">ICorDebugStepperEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="e016b-102">ICorDebugStepperEnum::Next Method</span></span>
<span data-ttu-id="e016b-103">Obtient le nombre spécifié d’instances ICorDebugStepper à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="e016b-103">Gets the specified number of ICorDebugStepper instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e016b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e016b-104">Syntax</span></span>  
  
```  
HRESULT Next(  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugStepper *steppers[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e016b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e016b-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="e016b-106">[in] Le nombre de `ICorDebugStepper` instances à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e016b-106">[in] The number of `ICorDebugStepper` instances to be retrieved.</span></span>  
  
 `steppers`  
 <span data-ttu-id="e016b-107">[out] Un tableau de pointeurs, chacun d’eux pointe vers un `ICorDebugStepper` objet.</span><span class="sxs-lookup"><span data-stu-id="e016b-107">[out] An array of pointers, each of which points to an `ICorDebugStepper` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="e016b-108">[out] Pointeur vers le nombre de `ICorDebugStepper` instances réellement retournés.</span><span class="sxs-lookup"><span data-stu-id="e016b-108">[out] Pointer to the number of `ICorDebugStepper` instances actually returned.</span></span> <span data-ttu-id="e016b-109">Cette valeur peut être null si `celt` fait partie.</span><span class="sxs-lookup"><span data-stu-id="e016b-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e016b-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e016b-110">Requirements</span></span>  
 <span data-ttu-id="e016b-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e016b-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e016b-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e016b-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e016b-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e016b-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e016b-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e016b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
