---
title: ICorDebugStackWalk::GetFrame, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugStackWalk.GetFrame Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStackWalk::GetFrame
helpviewer_keywords:
- GetFrame method [.NET Framework debugging]
- ICorDebugStackWalk::GetFrame method [.NET Framework debugging]
ms.assetid: 4083b505-5b59-44fb-8c5d-129db6a96c10
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 548a8a7743c02be5734b677010627f847c5bc4b0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33421985"
---
# <a name="icordebugstackwalkgetframe-method"></a><span data-ttu-id="e3bab-102">ICorDebugStackWalk::GetFrame, méthode</span><span class="sxs-lookup"><span data-stu-id="e3bab-102">ICorDebugStackWalk::GetFrame Method</span></span>
<span data-ttu-id="e3bab-103">Obtient le frame actuel le [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="e3bab-103">Gets the current frame in the [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e3bab-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3bab-104">Syntax</span></span>  
  
```  
HRESULT GetFrame([out] ICorDebugFrame ** pFrame);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e3bab-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3bab-105">Parameters</span></span>  
 `pFrame`  
 <span data-ttu-id="e3bab-106">[in] Pointeur vers l’adresse de l’objet frame créé qui représente le frame actuel dans la pile.</span><span class="sxs-lookup"><span data-stu-id="e3bab-106">[in] A pointer to the address of the created frame object that represents the current frame in the stack.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e3bab-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e3bab-107">Return Value</span></span>  
 <span data-ttu-id="e3bab-108">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="e3bab-108">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="e3bab-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e3bab-109">HRESULT</span></span>|<span data-ttu-id="e3bab-110">Description</span><span class="sxs-lookup"><span data-stu-id="e3bab-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e3bab-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3bab-111">S_OK</span></span>|<span data-ttu-id="e3bab-112">Le runtime retournée avec succès le frame actuel.</span><span class="sxs-lookup"><span data-stu-id="e3bab-112">The runtime successfully returned the current frame.</span></span>|  
|<span data-ttu-id="e3bab-113">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e3bab-113">E_FAIL</span></span>|<span data-ttu-id="e3bab-114">Le frame actuel n’a pas été retourné.</span><span class="sxs-lookup"><span data-stu-id="e3bab-114">The current frame was not returned.</span></span>|  
|<span data-ttu-id="e3bab-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="e3bab-115">S_FALSE</span></span>|<span data-ttu-id="e3bab-116">Le frame actuel est un frame de pile native.</span><span class="sxs-lookup"><span data-stu-id="e3bab-116">The current frame is a native stack frame.</span></span>|  
|<span data-ttu-id="e3bab-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e3bab-117">E_INVALIDARG</span></span>|<span data-ttu-id="e3bab-118">`pFrame` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="e3bab-118">`pFrame` is null.</span></span>|  
|<span data-ttu-id="e3bab-119">CORDBG_E_PAST_END_OF_STACK</span><span class="sxs-lookup"><span data-stu-id="e3bab-119">CORDBG_E_PAST_END_OF_STACK</span></span>|<span data-ttu-id="e3bab-120">Le pointeur de frame est déjà à la fin de la pile. Par conséquent, aucun frame supplémentaire n’est accessible.</span><span class="sxs-lookup"><span data-stu-id="e3bab-120">The frame pointer is already at the end of the stack; therefore, no additional frames can be accessed.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="e3bab-121">Exceptions</span><span class="sxs-lookup"><span data-stu-id="e3bab-121">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e3bab-122">Notes</span><span class="sxs-lookup"><span data-stu-id="e3bab-122">Remarks</span></span>  
 <span data-ttu-id="e3bab-123">`ICorDebugStackWalk` retourne uniquement des frames de pile réels.</span><span class="sxs-lookup"><span data-stu-id="e3bab-123">`ICorDebugStackWalk` returns only actual stack frames.</span></span> <span data-ttu-id="e3bab-124">Utilisez le [ICorDebugThread3::GetActiveInternalFrames](../../../../docs/framework/unmanaged-api/debugging/icordebugthread3-getactiveinternalframes-method.md) méthode pour retourner des frames internes.</span><span class="sxs-lookup"><span data-stu-id="e3bab-124">Use the [ICorDebugThread3::GetActiveInternalFrames](../../../../docs/framework/unmanaged-api/debugging/icordebugthread3-getactiveinternalframes-method.md) method to return internal frames.</span></span> <span data-ttu-id="e3bab-125">(Les frames internes sont des structures de données placés sur la pile par le runtime pour stocker des données temporaires.)</span><span class="sxs-lookup"><span data-stu-id="e3bab-125">(Internal frames are data structures pushed onto the stack by the runtime to store temporary data.)</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e3bab-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e3bab-126">Requirements</span></span>  
 <span data-ttu-id="e3bab-127">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e3bab-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e3bab-128">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e3bab-128">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e3bab-129">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e3bab-129">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e3bab-130">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e3bab-130">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3bab-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3bab-131">See Also</span></span>  
 [<span data-ttu-id="e3bab-132">ICorDebugStackWalk, interface</span><span class="sxs-lookup"><span data-stu-id="e3bab-132">ICorDebugStackWalk Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md)  
 [<span data-ttu-id="e3bab-133">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="e3bab-133">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="e3bab-134">Débogage</span><span class="sxs-lookup"><span data-stu-id="e3bab-134">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
