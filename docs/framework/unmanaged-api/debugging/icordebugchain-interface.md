---
title: ICorDebugChain, Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugChain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain
helpviewer_keywords:
- ICorDebugChain interface [.NET Framework debugging]
ms.assetid: f671f519-1cb3-4ae5-b9f1-abc5e783459f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e0bb716f1ad4087642a76dc84266ec6d3f46c1ae
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54571202"
---
# <a name="icordebugchain-interface1"></a><span data-ttu-id="74b5e-102">ICorDebugChain, Interface1</span><span class="sxs-lookup"><span data-stu-id="74b5e-102">ICorDebugChain Interface1</span></span>
<span data-ttu-id="74b5e-103">Représente un segment d'une pile des appels physique ou logique.</span><span class="sxs-lookup"><span data-stu-id="74b5e-103">Represents a segment of a physical or logical call stack.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="74b5e-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="74b5e-104">Methods</span></span>  
  
|<span data-ttu-id="74b5e-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="74b5e-105">Method</span></span>|<span data-ttu-id="74b5e-106">Description</span><span class="sxs-lookup"><span data-stu-id="74b5e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="74b5e-107">EnumerateFrames, méthode</span><span class="sxs-lookup"><span data-stu-id="74b5e-107">EnumerateFrames Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-enumerateframes-method.md)|<span data-ttu-id="74b5e-108">Obtient un énumérateur qui contient tous les frames de pile managés dans la chaîne, en commençant par le frame le plus récent.</span><span class="sxs-lookup"><span data-stu-id="74b5e-108">Gets an enumerator that contains all the managed stack frames in the chain, starting with the most recent frame.</span></span>|  
|[<span data-ttu-id="74b5e-109">GetActiveFrame, méthode</span><span class="sxs-lookup"><span data-stu-id="74b5e-109">GetActiveFrame Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getactiveframe-method.md)|<span data-ttu-id="74b5e-110">Obtient l’actif (autrement dit, plus récente) frame sur la chaîne.</span><span class="sxs-lookup"><span data-stu-id="74b5e-110">Gets the active (that is, most recent) frame on the chain.</span></span>|  
|[<span data-ttu-id="74b5e-111">GetCallee, méthode</span><span class="sxs-lookup"><span data-stu-id="74b5e-111">GetCallee Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getcallee-method.md)|<span data-ttu-id="74b5e-112">Obtient la chaîne qui a été appelée par cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="74b5e-112">Gets the chain that was called by this chain.</span></span>|  
|[<span data-ttu-id="74b5e-113">GetCaller, méthode</span><span class="sxs-lookup"><span data-stu-id="74b5e-113">GetCaller Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getcaller-method.md)|<span data-ttu-id="74b5e-114">Obtient la chaîne qui a appelé cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="74b5e-114">Gets the chain that called this chain.</span></span>|  
|[<span data-ttu-id="74b5e-115">GetContext, méthode</span><span class="sxs-lookup"><span data-stu-id="74b5e-115">GetContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getcontext-method.md)|<span data-ttu-id="74b5e-116">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="74b5e-116">Not implemented.</span></span>|  
|[<span data-ttu-id="74b5e-117">GetNext, méthode</span><span class="sxs-lookup"><span data-stu-id="74b5e-117">GetNext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getnext-method.md)|<span data-ttu-id="74b5e-118">Obtient la chaîne suivante de frames pour le thread.</span><span class="sxs-lookup"><span data-stu-id="74b5e-118">Gets the next chain of frames for the thread.</span></span>|  
|[<span data-ttu-id="74b5e-119">GetPrevious, méthode</span><span class="sxs-lookup"><span data-stu-id="74b5e-119">GetPrevious Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getprevious-method.md)|<span data-ttu-id="74b5e-120">Obtient la chaîne précédente de frames pour le thread.</span><span class="sxs-lookup"><span data-stu-id="74b5e-120">Gets the previous chain of frames for the thread.</span></span>|  
|[<span data-ttu-id="74b5e-121">GetReason, méthode</span><span class="sxs-lookup"><span data-stu-id="74b5e-121">GetReason Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getreason-method.md)|<span data-ttu-id="74b5e-122">Obtient la raison pour la genèse de cette chaîne appelante.</span><span class="sxs-lookup"><span data-stu-id="74b5e-122">Gets the reason for the genesis of this calling chain.</span></span>|  
|[<span data-ttu-id="74b5e-123">GetRegisterSet, méthode</span><span class="sxs-lookup"><span data-stu-id="74b5e-123">GetRegisterSet Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getregisterset-method.md)|<span data-ttu-id="74b5e-124">Obtient le jeu de registres pour la partie active de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="74b5e-124">Gets the register set for the active part of this chain.</span></span>|  
|[<span data-ttu-id="74b5e-125">GetStackRange, méthode</span><span class="sxs-lookup"><span data-stu-id="74b5e-125">GetStackRange Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getstackrange-method.md)|<span data-ttu-id="74b5e-126">Obtient la plage d’adresses du segment de pile pour cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="74b5e-126">Gets the address range of the stack segment for this chain.</span></span>|  
|[<span data-ttu-id="74b5e-127">GetThread, méthode</span><span class="sxs-lookup"><span data-stu-id="74b5e-127">GetThread Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getthread-method.md)|<span data-ttu-id="74b5e-128">Obtient le thread physique cette chaîne d’appel est partie.</span><span class="sxs-lookup"><span data-stu-id="74b5e-128">Gets the physical thread this call chain is part of.</span></span>|  
|[<span data-ttu-id="74b5e-129">IsManaged, méthode</span><span class="sxs-lookup"><span data-stu-id="74b5e-129">IsManaged Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-ismanaged-method.md)|<span data-ttu-id="74b5e-130">Obtient une valeur qui indique si cette chaîne est en cours d’exécution du code managé.</span><span class="sxs-lookup"><span data-stu-id="74b5e-130">Gets a value that indicates whether this chain is running managed code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="74b5e-131">Notes</span><span class="sxs-lookup"><span data-stu-id="74b5e-131">Remarks</span></span>  
 <span data-ttu-id="74b5e-132">Les frames de pile dans une chaîne occupent l’espace de pile contigu et partagent les mêmes thread et contexte.</span><span class="sxs-lookup"><span data-stu-id="74b5e-132">The stack frames in a chain occupy contiguous stack space and share the same thread and context.</span></span> <span data-ttu-id="74b5e-133">Une chaîne peut représenter deux chaînes de code managé ou non managé.</span><span class="sxs-lookup"><span data-stu-id="74b5e-133">A chain may represent either managed or unmanaged code chains.</span></span> <span data-ttu-id="74b5e-134">Vide `ICorDebugChain` instance représente une chaîne de code non managé.</span><span class="sxs-lookup"><span data-stu-id="74b5e-134">An empty `ICorDebugChain` instance represents an unmanaged code chain.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="74b5e-135">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="74b5e-135">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="74b5e-136">Spécifications</span><span class="sxs-lookup"><span data-stu-id="74b5e-136">Requirements</span></span>  
 <span data-ttu-id="74b5e-137">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="74b5e-137">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="74b5e-138">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="74b5e-138">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="74b5e-139">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="74b5e-139">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="74b5e-140">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="74b5e-140">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="74b5e-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74b5e-141">See also</span></span>
- [<span data-ttu-id="74b5e-142">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="74b5e-142">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
