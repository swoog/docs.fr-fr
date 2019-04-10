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
ms.openlocfilehash: a15d7f16676b8b9d66f8d1ba7484f3fec5735a44
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59222561"
---
# <a name="icordebugframe-interface"></a><span data-ttu-id="e47f4-102">ICorDebugFrame, interface</span><span class="sxs-lookup"><span data-stu-id="e47f4-102">ICorDebugFrame Interface</span></span>

<span data-ttu-id="e47f4-103">Représente un frame sur la pile en cours.</span><span class="sxs-lookup"><span data-stu-id="e47f4-103">Represents a frame on the current stack.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e47f4-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e47f4-104">Methods</span></span>  
  
|<span data-ttu-id="e47f4-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="e47f4-105">Method</span></span>|<span data-ttu-id="e47f4-106">Description</span><span class="sxs-lookup"><span data-stu-id="e47f4-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e47f4-107">CreateStepper, méthode</span><span class="sxs-lookup"><span data-stu-id="e47f4-107">CreateStepper Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-createstepper-method.md)|<span data-ttu-id="e47f4-108">Obtient un ICorDebugStepper pour effectuer des opérations pas à pas concernant ce `ICorDebugFrame`.</span><span class="sxs-lookup"><span data-stu-id="e47f4-108">Gets an ICorDebugStepper to perform stepping operations relative to this `ICorDebugFrame`.</span></span>|  
|[<span data-ttu-id="e47f4-109">GetCallee, méthode</span><span class="sxs-lookup"><span data-stu-id="e47f4-109">GetCallee Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcallee-method.md)|<span data-ttu-id="e47f4-110">Obtient un pointeur vers le `ICorDebugFrame` dans la chaîne actuelle que ce frame est appelé, ou retourne null si c’est le frame plus profond dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="e47f4-110">Gets a pointer to the `ICorDebugFrame` in the current chain that this frame called, or returns null if this is the innermost frame in the chain.</span></span>|  
|[<span data-ttu-id="e47f4-111">GetCaller, méthode</span><span class="sxs-lookup"><span data-stu-id="e47f4-111">GetCaller Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcaller-method.md)|<span data-ttu-id="e47f4-112">Obtient un pointeur vers le `ICorDebugFrame` dans la chaîne actuelle qui appelé ce frame, ou retourne null si c’est le frame le plus extérieur dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="e47f4-112">Gets a pointer to the `ICorDebugFrame` in the current chain that called this frame, or returns null if this is the outermost frame in the chain.</span></span>|  
|[<span data-ttu-id="e47f4-113">GetChain, méthode</span><span class="sxs-lookup"><span data-stu-id="e47f4-113">GetChain Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getchain-method.md)|<span data-ttu-id="e47f4-114">Obtient un pointeur vers ICorDebugChain ce `ICorDebugFrame` fait partie de.</span><span class="sxs-lookup"><span data-stu-id="e47f4-114">Gets a pointer to the ICorDebugChain this `ICorDebugFrame` is a part of.</span></span>|  
|[<span data-ttu-id="e47f4-115">GetCode, méthode</span><span class="sxs-lookup"><span data-stu-id="e47f4-115">GetCode Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcode-method.md)|<span data-ttu-id="e47f4-116">Obtient un pointeur vers ICorDebugCode associé à ce frame de pile.</span><span class="sxs-lookup"><span data-stu-id="e47f4-116">Gets a pointer to the ICorDebugCode associated with this stack frame.</span></span>|  
|[<span data-ttu-id="e47f4-117">GetFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="e47f4-117">GetFunction Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getfunction-method.md)|<span data-ttu-id="e47f4-118">Obtient un pointeur vers ICorDebugFunction qui contient le code associé à ce frame de pile.</span><span class="sxs-lookup"><span data-stu-id="e47f4-118">Gets a pointer to the ICorDebugFunction that contains the code associated with this stack frame.</span></span>|  
|[<span data-ttu-id="e47f4-119">GetFunctionToken, méthode</span><span class="sxs-lookup"><span data-stu-id="e47f4-119">GetFunctionToken Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getfunctiontoken-method.md)|<span data-ttu-id="e47f4-120">Obtient le jeton de métadonnées pour la fonction qui contient le code associé à ce frame de pile.</span><span class="sxs-lookup"><span data-stu-id="e47f4-120">Gets the metadata token for the function that contains the code associated with this stack frame.</span></span>|  
|[<span data-ttu-id="e47f4-121">GetStackRange, méthode</span><span class="sxs-lookup"><span data-stu-id="e47f4-121">GetStackRange Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getstackrange-method.md)|<span data-ttu-id="e47f4-122">Obtient la plage d’adresses absolues du frame de pile représenté par cet `ICorDebugFrame`.</span><span class="sxs-lookup"><span data-stu-id="e47f4-122">Gets the absolute address range of the stack frame represented by this `ICorDebugFrame`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e47f4-123">Notes</span><span class="sxs-lookup"><span data-stu-id="e47f4-123">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e47f4-124">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="e47f4-124">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e47f4-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e47f4-125">Requirements</span></span>  
 <span data-ttu-id="e47f4-126">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e47f4-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e47f4-127">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e47f4-127">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e47f4-128">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e47f4-128">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="e47f4-129">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="e47f4-129">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="e47f4-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e47f4-130">See also</span></span>

- [<span data-ttu-id="e47f4-131">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="e47f4-131">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
