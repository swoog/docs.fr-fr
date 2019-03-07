---
title: ICorDebugStepper::SetInterceptMask, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugStepper.SetInterceptMask
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper::SetInterceptMask
helpviewer_keywords:
- SetInterceptMask method [.NET Framework debugging]
- ICorDebugStepper::SetInterceptMask method [.NET Framework debugging]
ms.assetid: 6245e2ae-5cc2-43ff-8cc1-71953d12113a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 25a9d287e6520f1fc7826d85dfbcd8e9a6da22f7
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57481060"
---
# <a name="icordebugsteppersetinterceptmask-method"></a><span data-ttu-id="88e72-102">ICorDebugStepper::SetInterceptMask, méthode</span><span class="sxs-lookup"><span data-stu-id="88e72-102">ICorDebugStepper::SetInterceptMask Method</span></span>
<span data-ttu-id="88e72-103">Définit une valeur qui spécifie les types de code sont détaillé.</span><span class="sxs-lookup"><span data-stu-id="88e72-103">Sets a value that specifies the types of code that are stepped into.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="88e72-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88e72-104">Syntax</span></span>  
  
```  
HRESULT SetInterceptMask (  
    [in] CorDebugIntercept    mask  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="88e72-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88e72-105">Parameters</span></span>  
 `mask`  
 <span data-ttu-id="88e72-106">[in] Une combinaison de valeurs de l’énumération CorDebugIntercept qui spécifie les types de code.</span><span class="sxs-lookup"><span data-stu-id="88e72-106">[in] A combination of values of the CorDebugIntercept enumeration that specifies the types of code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="88e72-107">Notes</span><span class="sxs-lookup"><span data-stu-id="88e72-107">Remarks</span></span>  
 <span data-ttu-id="88e72-108">Si le bit pour un intercepteur est défini, l’exécution pas à pas se termine lorsque le type donné de code d’interception est rencontré.</span><span class="sxs-lookup"><span data-stu-id="88e72-108">If the bit for an interceptor is set, the stepper will complete when the given type of intercepting code is encountered.</span></span> <span data-ttu-id="88e72-109">Si le bit est désactivé, le code d’interception sera ignoré.</span><span class="sxs-lookup"><span data-stu-id="88e72-109">If the bit is cleared, the intercepting code will be skipped.</span></span>  
  
 <span data-ttu-id="88e72-110">Le `SetInterceptMask` méthode peut avoir des interactions imprévues avec [ICorDebugStepper::SetUnmappedStopMask](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setunmappedstopmask-method.md) (à partir du point de vue utilisateur).</span><span class="sxs-lookup"><span data-stu-id="88e72-110">The `SetInterceptMask` method may have unforeseen interactions with [ICorDebugStepper::SetUnmappedStopMask](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setunmappedstopmask-method.md) (from the user's point of view).</span></span> <span data-ttu-id="88e72-111">Par exemple, si visible uniquement (autrement dit, non interne) partie du code d’initialisation de classe ne possède pas les informations de mappage et que STOP_NO_MAPPING_INFO n’est pas définie (voir la [ICorDebugStepper::SetUnmappedStopMask](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setunmappedstopmask-method.md) (méthode) et le CorDebugUnmappedStop, énumération), l’ignorera l’initialisation de classe.</span><span class="sxs-lookup"><span data-stu-id="88e72-111">For example, if the only visible (that is, non-internal) portion of class initialization code lacks mapping information and STOP_NO_MAPPING_INFO isn't set (see the [ICorDebugStepper::SetUnmappedStopMask](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setunmappedstopmask-method.md) method and the CorDebugUnmappedStop enumeration), the stepper will step over the class initialization.</span></span> <span data-ttu-id="88e72-112">Par défaut, seule la valeur INTERCEPT_NONE de le `CorDebugIntercept` énumération sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="88e72-112">By default, only the INTERCEPT_NONE value of the `CorDebugIntercept` enumeration will be used.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="88e72-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="88e72-113">Requirements</span></span>  
 <span data-ttu-id="88e72-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="88e72-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="88e72-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="88e72-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="88e72-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="88e72-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="88e72-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="88e72-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
