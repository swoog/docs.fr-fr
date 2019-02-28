---
title: ICorDebugFrame, interface
ms.date: 03/30/2017
api_name:
- ICorDebugFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame
helpviewer_keywords:
- ICorDebugFrame interface [.NET Framework debugging]
ms.assetid: 0c48f764-3c64-4602-b2f4-4ffc60eb2c65
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f77708a5b315cb65b54ffa0983caa17176d01324
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56974469"
---
# <a name="icordebugframe-interface"></a><span data-ttu-id="20e47-102">ICorDebugFrame, interface</span><span class="sxs-lookup"><span data-stu-id="20e47-102">ICorDebugFrame Interface</span></span>

<span data-ttu-id="20e47-103">Représente un frame sur la pile en cours.</span><span class="sxs-lookup"><span data-stu-id="20e47-103">Represents a frame on the current stack.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="20e47-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="20e47-104">Methods</span></span>  
  
|<span data-ttu-id="20e47-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="20e47-105">Method</span></span>|<span data-ttu-id="20e47-106">Description</span><span class="sxs-lookup"><span data-stu-id="20e47-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="20e47-107">CreateStepper, méthode</span><span class="sxs-lookup"><span data-stu-id="20e47-107">CreateStepper Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-createstepper-method.md)|<span data-ttu-id="20e47-108">Obtient un ICorDebugStepper pour effectuer des opérations pas à pas concernant ce `ICorDebugFrame`.</span><span class="sxs-lookup"><span data-stu-id="20e47-108">Gets an ICorDebugStepper to perform stepping operations relative to this `ICorDebugFrame`.</span></span>|  
|[<span data-ttu-id="20e47-109">GetCallee, méthode</span><span class="sxs-lookup"><span data-stu-id="20e47-109">GetCallee Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcallee-method.md)|<span data-ttu-id="20e47-110">Obtient un pointeur vers le `ICorDebugFrame` dans la chaîne actuelle que ce frame est appelé, ou retourne null si c’est le frame plus profond dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="20e47-110">Gets a pointer to the `ICorDebugFrame` in the current chain that this frame called, or returns null if this is the innermost frame in the chain.</span></span>|  
|[<span data-ttu-id="20e47-111">GetCaller, méthode</span><span class="sxs-lookup"><span data-stu-id="20e47-111">GetCaller Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcaller-method.md)|<span data-ttu-id="20e47-112">Obtient un pointeur vers le `ICorDebugFrame` dans la chaîne actuelle qui appelé ce frame, ou retourne null si c’est le frame le plus extérieur dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="20e47-112">Gets a pointer to the `ICorDebugFrame` in the current chain that called this frame, or returns null if this is the outermost frame in the chain.</span></span>|  
|[<span data-ttu-id="20e47-113">GetChain, méthode</span><span class="sxs-lookup"><span data-stu-id="20e47-113">GetChain Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getchain-method.md)|<span data-ttu-id="20e47-114">Obtient un pointeur vers ICorDebugChain ce `ICorDebugFrame` fait partie de.</span><span class="sxs-lookup"><span data-stu-id="20e47-114">Gets a pointer to the ICorDebugChain this `ICorDebugFrame` is a part of.</span></span>|  
|[<span data-ttu-id="20e47-115">GetCode, méthode</span><span class="sxs-lookup"><span data-stu-id="20e47-115">GetCode Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcode-method.md)|<span data-ttu-id="20e47-116">Obtient un pointeur vers ICorDebugCode associé à ce frame de pile.</span><span class="sxs-lookup"><span data-stu-id="20e47-116">Gets a pointer to the ICorDebugCode associated with this stack frame.</span></span>|  
|[<span data-ttu-id="20e47-117">GetFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="20e47-117">GetFunction Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getfunction-method.md)|<span data-ttu-id="20e47-118">Obtient un pointeur vers ICorDebugFunction qui contient le code associé à ce frame de pile.</span><span class="sxs-lookup"><span data-stu-id="20e47-118">Gets a pointer to the ICorDebugFunction that contains the code associated with this stack frame.</span></span>|  
|[<span data-ttu-id="20e47-119">GetFunctionToken, méthode</span><span class="sxs-lookup"><span data-stu-id="20e47-119">GetFunctionToken Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getfunctiontoken-method.md)|<span data-ttu-id="20e47-120">Obtient le jeton de métadonnées pour la fonction qui contient le code associé à ce frame de pile.</span><span class="sxs-lookup"><span data-stu-id="20e47-120">Gets the metadata token for the function that contains the code associated with this stack frame.</span></span>|  
|[<span data-ttu-id="20e47-121">GetStackRange, méthode</span><span class="sxs-lookup"><span data-stu-id="20e47-121">GetStackRange Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getstackrange-method.md)|<span data-ttu-id="20e47-122">Obtient la plage d’adresses absolues du frame de pile représenté par cet `ICorDebugFrame`.</span><span class="sxs-lookup"><span data-stu-id="20e47-122">Gets the absolute address range of the stack frame represented by this `ICorDebugFrame`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="20e47-123">Notes</span><span class="sxs-lookup"><span data-stu-id="20e47-123">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="20e47-124">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="20e47-124">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="20e47-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="20e47-125">Requirements</span></span>  
 <span data-ttu-id="20e47-126">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="20e47-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="20e47-127">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="20e47-127">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="20e47-128">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="20e47-128">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="20e47-129">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="20e47-129">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20e47-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20e47-130">See also</span></span>
- [<span data-ttu-id="20e47-131">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="20e47-131">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
