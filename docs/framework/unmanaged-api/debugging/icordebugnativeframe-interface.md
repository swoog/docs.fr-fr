---
title: ICorDebugNativeFrame, interface
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame
helpviewer_keywords:
- ICorDebugNativeFrame interface [.NET Framework debugging]
ms.assetid: 04819c58-7246-4b32-befb-680cf1dbc436
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fbdb17bcd502b75da0a73d9a36cf36d6564320bc
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56975483"
---
# <a name="icordebugnativeframe-interface"></a><span data-ttu-id="41e6f-102">ICorDebugNativeFrame, interface</span><span class="sxs-lookup"><span data-stu-id="41e6f-102">ICorDebugNativeFrame Interface</span></span>

<span data-ttu-id="41e6f-103">Une implémentation spécialisée de ICorDebugFrame utilisée pour les frames natifs.</span><span class="sxs-lookup"><span data-stu-id="41e6f-103">A specialized implementation of ICorDebugFrame used for native frames.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="41e6f-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="41e6f-104">Methods</span></span>  
  
|<span data-ttu-id="41e6f-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="41e6f-105">Method</span></span>|<span data-ttu-id="41e6f-106">Description</span><span class="sxs-lookup"><span data-stu-id="41e6f-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="41e6f-107">CanSetIP, méthode</span><span class="sxs-lookup"><span data-stu-id="41e6f-107">CanSetIP Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-cansetip-method.md)|<span data-ttu-id="41e6f-108">Obtient une valeur qui indique s’il est sans risque de définir le pointeur d’instruction à l’emplacement de décalage spécifié dans le code natif.</span><span class="sxs-lookup"><span data-stu-id="41e6f-108">Gets a value that indicates whether it is safe to set the instruction pointer to the specified offset location in native code.</span></span>|  
|[<span data-ttu-id="41e6f-109">GetIP, méthode</span><span class="sxs-lookup"><span data-stu-id="41e6f-109">GetIP Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-getip-method.md)|<span data-ttu-id="41e6f-110">Obtient l’offset du frame de pile en code natif.</span><span class="sxs-lookup"><span data-stu-id="41e6f-110">Gets the stack frame's offset into native code.</span></span>|  
|[<span data-ttu-id="41e6f-111">GetLocalDoubleRegisterValue, méthode</span><span class="sxs-lookup"><span data-stu-id="41e6f-111">GetLocalDoubleRegisterValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-getlocaldoubleregistervalue-method.md)|<span data-ttu-id="41e6f-112">Obtient un pointeur vers un ICorDebugValue qui représente la valeur d’un argument ou une variable locale stockée dans deux registres de mémoire d’un frame natif.</span><span class="sxs-lookup"><span data-stu-id="41e6f-112">Gets a pointer to an ICorDebugValue that represents the value of an argument or local variable stored in two memory registers of a native frame.</span></span>|  
|[<span data-ttu-id="41e6f-113">GetLocalMemoryRegisterValue, méthode</span><span class="sxs-lookup"><span data-stu-id="41e6f-113">GetLocalMemoryRegisterValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-getlocalmemoryregistervalue-method.md)|<span data-ttu-id="41e6f-114">Obtient un pointeur vers un `ICorDebugValue` qui représente la valeur d’une variable locale, dont les bits de poids faibles sont stockés dans le Registre spécifié et les bits de poids fort sont stockés à l’adresse mémoire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="41e6f-114">Gets a pointer to an `ICorDebugValue` that represents the value of a local variable, of which the low bits are stored in the specified register and the high bits are stored at the specified memory address.</span></span>|  
|[<span data-ttu-id="41e6f-115">GetLocalMemoryValue, méthode</span><span class="sxs-lookup"><span data-stu-id="41e6f-115">GetLocalMemoryValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-getlocalmemoryvalue-method.md)|<span data-ttu-id="41e6f-116">Obtient un pointeur vers un `ICorDebugValue` qui représente la valeur d’une variable locale stockée à l’adresse mémoire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="41e6f-116">Gets a pointer to an `ICorDebugValue` that represents the value of a local variable stored at the specified memory address.</span></span>|  
|[<span data-ttu-id="41e6f-117">GetLocalRegisterMemoryValue, méthode</span><span class="sxs-lookup"><span data-stu-id="41e6f-117">GetLocalRegisterMemoryValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-getlocalregistermemoryvalue-method.md)|<span data-ttu-id="41e6f-118">Obtient un pointeur vers un `ICorDebugValue` qui représente la valeur d’une variable locale, dont les bits de poids fort sont stockés dans le Registre spécifié et les bits de poids faibles sont stockés à l’adresse mémoire spécifiée</span><span class="sxs-lookup"><span data-stu-id="41e6f-118">Gets a pointer to an `ICorDebugValue` that represents the value of a local variable, of which the high bits are stored in the specified register and the low bits are stored at the specified memory address</span></span>|  
|[<span data-ttu-id="41e6f-119">GetLocalRegisterValue, méthode</span><span class="sxs-lookup"><span data-stu-id="41e6f-119">GetLocalRegisterValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-getlocalregistervalue-method.md)|<span data-ttu-id="41e6f-120">Obtient un pointeur vers un `ICorDebugValue` qui représente la valeur d’un argument ou une variable locale stockée dans le Registre natif spécifié.</span><span class="sxs-lookup"><span data-stu-id="41e6f-120">Gets a pointer to an `ICorDebugValue` that represents the value of an argument or a local variable stored in the specified native register.</span></span>|  
|[<span data-ttu-id="41e6f-121">GetRegisterSet, méthode</span><span class="sxs-lookup"><span data-stu-id="41e6f-121">GetRegisterSet Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-getregisterset-method.md)|<span data-ttu-id="41e6f-122">Obtient un pointeur vers un [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) qui représente le Registre défini pour ce `ICorDebugNativeFrame`.</span><span class="sxs-lookup"><span data-stu-id="41e6f-122">Gets a pointer to an [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) that represents the register set for this `ICorDebugNativeFrame`.</span></span>|  
|[<span data-ttu-id="41e6f-123">SetIP, méthode</span><span class="sxs-lookup"><span data-stu-id="41e6f-123">SetIP Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-setip-method.md)|<span data-ttu-id="41e6f-124">Définit le pointeur d’instruction à l’emplacement de décalage spécifié dans le code natif.</span><span class="sxs-lookup"><span data-stu-id="41e6f-124">Sets the instruction pointer to the specified offset location in native code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="41e6f-125">Notes</span><span class="sxs-lookup"><span data-stu-id="41e6f-125">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="41e6f-126">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="41e6f-126">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="41e6f-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="41e6f-127">Requirements</span></span>  
 <span data-ttu-id="41e6f-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="41e6f-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="41e6f-129">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="41e6f-129">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="41e6f-130">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="41e6f-130">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="41e6f-131">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="41e6f-131">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="41e6f-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41e6f-132">See also</span></span>
- [<span data-ttu-id="41e6f-133">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="41e6f-133">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
