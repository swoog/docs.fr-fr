---
title: ICorDebugILFrame2::RemapFunction, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame2.RemapFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame2::RemapFunction
helpviewer_keywords:
- ICorDebugILFrame2::RemapFunction method [.NET Framework debugging]
- RemapFunction method [.NET Framework debugging]
ms.assetid: dd639ba0-f77b-426d-9ff6-f92706840348
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b92885d2a6514839a864d6a345dd8af8b07b90c1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61946521"
---
# <a name="icordebugilframe2remapfunction-method"></a><span data-ttu-id="7f16f-102">ICorDebugILFrame2::RemapFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="7f16f-102">ICorDebugILFrame2::RemapFunction Method</span></span>
<span data-ttu-id="7f16f-103">Remappe une fonction modifiée en spécifiant l’offset du nouveau Microsoft intermediate language (MSIL)</span><span class="sxs-lookup"><span data-stu-id="7f16f-103">Remaps an edited function by specifying the new Microsoft intermediate language (MSIL) offset</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f16f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f16f-104">Syntax</span></span>  
  
```  
HRESULT RemapFunction (  
    [in] ULONG32      newILOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7f16f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f16f-105">Parameters</span></span>  
 `newILOffset`  
 <span data-ttu-id="7f16f-106">[in] Nouvel offset MSIL du frame de pile à laquelle le pointeur d’instruction doit être placé.</span><span class="sxs-lookup"><span data-stu-id="7f16f-106">[in] The stack frame's new MSIL offset at which the instruction pointer should be placed.</span></span> <span data-ttu-id="7f16f-107">Cette valeur doit être un point de séquence.</span><span class="sxs-lookup"><span data-stu-id="7f16f-107">This value must be a sequence point.</span></span>  
  
 <span data-ttu-id="7f16f-108">Il est responsable de l’appelant pour garantir la validité de cette valeur.</span><span class="sxs-lookup"><span data-stu-id="7f16f-108">It is the caller’s responsibility to ensure the validity of this value.</span></span> <span data-ttu-id="7f16f-109">Par exemple, l’offset MSIL n’est pas valide s’il est en dehors des limites de la fonction.</span><span class="sxs-lookup"><span data-stu-id="7f16f-109">For example, the MSIL offset is not valid if it is outside the bounds of the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7f16f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7f16f-110">Remarks</span></span>  
 <span data-ttu-id="7f16f-111">Lors de la fonction d’un frame a été modifiée, le débogueur peut appeler le `RemapFunction` méthode pour passer à la dernière version de la fonction du frame afin de pouvoir être exécuté.</span><span class="sxs-lookup"><span data-stu-id="7f16f-111">When a frame’s function has been edited, the debugger can call the `RemapFunction` method to swap in the latest version of the frame's function so it can be executed.</span></span> <span data-ttu-id="7f16f-112">L’exécution du code commence à l’offset MSIL donné.</span><span class="sxs-lookup"><span data-stu-id="7f16f-112">The code execution will begin at the given MSIL offset.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7f16f-113">Appel `RemapFunction`, comme l’appel [ICorDebugILFrame::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-setip-method.md), invalidera immédiatement toutes les interfaces de débogage qui sont liées à la génération d’une trace de pile pour le thread.</span><span class="sxs-lookup"><span data-stu-id="7f16f-113">Calling `RemapFunction`, like calling [ICorDebugILFrame::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-setip-method.md), will immediately invalidate all debugging interfaces that are related to generating a stack trace for the thread.</span></span> <span data-ttu-id="7f16f-114">Ces interfaces comprennent [ICorDebugChain](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-interface.md), ICorDebugILFrame ICorDebugInternalFrame et ICorDebugNativeFrame.</span><span class="sxs-lookup"><span data-stu-id="7f16f-114">These interfaces include [ICorDebugChain](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-interface.md), ICorDebugILFrame, ICorDebugInternalFrame, and ICorDebugNativeFrame.</span></span>  
  
 <span data-ttu-id="7f16f-115">Le `RemapFunction` méthode peut être appelée uniquement dans le contexte de l’image actuelle et uniquement dans un des cas suivants :</span><span class="sxs-lookup"><span data-stu-id="7f16f-115">The `RemapFunction` method can be called only in the context of the current frame, and only in one of the following cases:</span></span>  
  
- <span data-ttu-id="7f16f-116">Après réception d’un [ICorDebugManagedCallback2::FunctionRemapOpportunity](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-functionremapopportunity-method.md) rappel qui n’a pas encore repris.</span><span class="sxs-lookup"><span data-stu-id="7f16f-116">After receipt of a [ICorDebugManagedCallback2::FunctionRemapOpportunity](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-functionremapopportunity-method.md) callback that has not yet been continued.</span></span>  
  
- <span data-ttu-id="7f16f-117">Pendant l’exécution de code est arrêtée en raison d’une [ICorDebugManagedCallback::EditAndContinueRemap](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-editandcontinueremap-method.md) événement pour ce frame.</span><span class="sxs-lookup"><span data-stu-id="7f16f-117">While code execution is stopped because of an [ICorDebugManagedCallback::EditAndContinueRemap](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-editandcontinueremap-method.md) event for this frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7f16f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f16f-118">Requirements</span></span>  
 <span data-ttu-id="7f16f-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7f16f-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7f16f-120">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7f16f-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7f16f-121">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7f16f-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7f16f-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7f16f-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
