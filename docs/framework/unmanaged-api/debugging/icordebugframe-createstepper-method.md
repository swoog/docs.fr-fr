---
title: ICorDebugFrame::CreateStepper, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.CreateStepper
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::CreateStepper
helpviewer_keywords:
- ICorDebugFrame::CreateStepper method [.NET Framework debugging]
- CreateStepper method, ICorDebugFrame interface [.NET Framework debugging]
ms.assetid: 689e7f28-20c1-4d5c-9baa-17441cd63a88
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3fe3cbc4bad83496bcc58aaea60e6724b1d1f06c
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57466386"
---
# <a name="icordebugframecreatestepper-method"></a><span data-ttu-id="db189-102">ICorDebugFrame::CreateStepper, méthode</span><span class="sxs-lookup"><span data-stu-id="db189-102">ICorDebugFrame::CreateStepper Method</span></span>
<span data-ttu-id="db189-103">Obtient une exécution pas à pas qui permet au débogueur d’effectuer des opérations ICorDebugFrame pas à pas.</span><span class="sxs-lookup"><span data-stu-id="db189-103">Gets a stepper that allows the debugger to perform stepping operations relative to this ICorDebugFrame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db189-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db189-104">Syntax</span></span>  
  
```  
HRESULT CreateStepper (  
    [out] ICorDebugStepper   **ppStepper  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="db189-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db189-105">Parameters</span></span>  
 `ppStepper`  
 <span data-ttu-id="db189-106">[out] Pointeur vers l’adresse d’un objet ICorDebugStepper qui permet au débogueur d’effectuer des opérations pas à pas relatif à l’image actuelle.</span><span class="sxs-lookup"><span data-stu-id="db189-106">[out] A pointer to the address of an ICorDebugStepper object that allows the debugger to perform stepping operations relative to the current frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="db189-107">Notes</span><span class="sxs-lookup"><span data-stu-id="db189-107">Remarks</span></span>  
 <span data-ttu-id="db189-108">Si le frame n’est pas actif, l’objet d’exécution pas à pas aura généralement revenir à l’image avant la fin de l’étape.</span><span class="sxs-lookup"><span data-stu-id="db189-108">If the frame is not active, the stepper object will typically have to return to the frame before the step is completed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="db189-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="db189-109">Requirements</span></span>  
 <span data-ttu-id="db189-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="db189-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="db189-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="db189-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="db189-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="db189-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="db189-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="db189-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
