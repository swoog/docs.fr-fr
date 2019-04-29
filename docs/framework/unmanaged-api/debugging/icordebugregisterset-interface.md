---
title: ICorDebugRegisterSet, interface
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet
helpviewer_keywords:
- ICorDebugRegisterSet interface [.NET Framework debugging]
ms.assetid: d3d9676d-0b87-4bc3-b679-7bbc7a186c88
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7b0a5d80d984a3c696b178c4d8c936bd47354945
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61782874"
---
# <a name="icordebugregisterset-interface"></a><span data-ttu-id="d855e-102">ICorDebugRegisterSet, interface</span><span class="sxs-lookup"><span data-stu-id="d855e-102">ICorDebugRegisterSet Interface</span></span>
<span data-ttu-id="d855e-103">Représente le jeu de registres disponibles sur l’ordinateur qui exécute actuellement le code.</span><span class="sxs-lookup"><span data-stu-id="d855e-103">Represents the set of registers available on the computer that is currently executing code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d855e-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d855e-104">Methods</span></span>  
  
|<span data-ttu-id="d855e-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="d855e-105">Method</span></span>|<span data-ttu-id="d855e-106">Description</span><span class="sxs-lookup"><span data-stu-id="d855e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d855e-107">GetRegisters, méthode</span><span class="sxs-lookup"><span data-stu-id="d855e-107">GetRegisters Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-getregisters-method.md)|<span data-ttu-id="d855e-108">Obtient la valeur de chaque registre (sur l’ordinateur qui exécute actuellement le code) qui est spécifié par le masque de bits.</span><span class="sxs-lookup"><span data-stu-id="d855e-108">Gets the value of each register (on the computer that is currently executing code) that is specified by the bit mask.</span></span>|  
|[<span data-ttu-id="d855e-109">GetRegistersAvailable, méthode</span><span class="sxs-lookup"><span data-stu-id="d855e-109">GetRegistersAvailable Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-getregistersavailable-method.md)|<span data-ttu-id="d855e-110">Obtient un masque de bits indiquant les registres dans ce `ICorDebugRegisterSet` sont actuellement disponibles.</span><span class="sxs-lookup"><span data-stu-id="d855e-110">Gets a bit mask indicating which registers in this `ICorDebugRegisterSet` are currently available.</span></span>|  
|[<span data-ttu-id="d855e-111">GetThreadContext, méthode</span><span class="sxs-lookup"><span data-stu-id="d855e-111">GetThreadContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-getthreadcontext-method.md)|<span data-ttu-id="d855e-112">Obtient le contexte du thread actuel.</span><span class="sxs-lookup"><span data-stu-id="d855e-112">Gets the context of the current thread.</span></span>|  
|[<span data-ttu-id="d855e-113">SetRegisters, méthode</span><span class="sxs-lookup"><span data-stu-id="d855e-113">SetRegisters Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-setregisters-method.md)|<span data-ttu-id="d855e-114">Non implémenté pour le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="d855e-114">Not implemented for the .NET Framework version 2.0.</span></span>|  
|[<span data-ttu-id="d855e-115">SetThreadContext, méthode</span><span class="sxs-lookup"><span data-stu-id="d855e-115">SetThreadContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-setthreadcontext-method.md)|<span data-ttu-id="d855e-116">Non implémenté pour le .NET Framework 2.0.</span><span class="sxs-lookup"><span data-stu-id="d855e-116">Not implemented for the .NET Framework 2.0.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d855e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d855e-117">Remarks</span></span>  
 <span data-ttu-id="d855e-118">Le `ICorDebugRegisterSet` interface prend en charge les registres 32 bits uniquement.</span><span class="sxs-lookup"><span data-stu-id="d855e-118">The `ICorDebugRegisterSet` interface supports only 32-bit registers.</span></span> <span data-ttu-id="d855e-119">Utilisez le [ICorDebugRegisterSet2](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md) interface sur les plateformes IA-64 qui requièrent des registres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d855e-119">Use the [ICorDebugRegisterSet2](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md) interface on platforms such as IA-64 that require additional registers.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d855e-120">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="d855e-120">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d855e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d855e-121">Requirements</span></span>  
 <span data-ttu-id="d855e-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d855e-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d855e-123">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d855e-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d855e-124">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d855e-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d855e-125">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d855e-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d855e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d855e-126">See also</span></span>

- [<span data-ttu-id="d855e-127">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d855e-127">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="d855e-128">ICorDebugRegisterSet2, interface</span><span class="sxs-lookup"><span data-stu-id="d855e-128">ICorDebugRegisterSet2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md)
