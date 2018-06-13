---
title: ICorDebugVirtualUnwinder (interface)
ms.date: 03/30/2017
ms.assetid: a09e9ccc-0b37-43e3-95c1-bc5fa7ee5f42
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bb04ac42b3cc77db3af53c87efb0d1f1f75da928
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33421283"
---
# <a name="icordebugvirtualunwinder-interface"></a><span data-ttu-id="18f42-102">ICorDebugVirtualUnwinder (interface)</span><span class="sxs-lookup"><span data-stu-id="18f42-102">ICorDebugVirtualUnwinder Interface</span></span>
<span data-ttu-id="18f42-103">Fournit des méthodes pour faciliter le déroulement de la pile.</span><span class="sxs-lookup"><span data-stu-id="18f42-103">Provides methods to help in stack unwinding.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="18f42-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="18f42-104">Methods</span></span>  
  
|<span data-ttu-id="18f42-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="18f42-105">Method</span></span>|<span data-ttu-id="18f42-106">Name</span><span class="sxs-lookup"><span data-stu-id="18f42-106">Name</span></span>|  
|------------|----------|  
|[<span data-ttu-id="18f42-107">GetContext, méthode</span><span class="sxs-lookup"><span data-stu-id="18f42-107">GetContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvirtualunwinder-getcontext-method.md)|<span data-ttu-id="18f42-108">Obtient le contexte actuel de ce dérouleur.</span><span class="sxs-lookup"><span data-stu-id="18f42-108">Gets the current context of this unwinder.</span></span>|  
|[<span data-ttu-id="18f42-109">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="18f42-109">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvirtualunwinder-next-method.md)|<span data-ttu-id="18f42-110">Avance jusqu'au contexte de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="18f42-110">Advances to the caller's context.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="18f42-111">Notes</span><span class="sxs-lookup"><span data-stu-id="18f42-111">Remarks</span></span>  
 <span data-ttu-id="18f42-112">Les membres de l'interface `ICorDebugVirtualUnwinder` sont implémentés par le débogueur pour faciliter le déroulement de la pile.</span><span class="sxs-lookup"><span data-stu-id="18f42-112">The members of the `ICorDebugVirtualUnwinder` interface are implemented by the debugger to help in stack unwinding.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="18f42-113">Cette interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="18f42-113">This interface is available with .NET Native only.</span></span> <span data-ttu-id="18f42-114">Si vous implémentez cette interface pour des scénarios ICorDebug en dehors de .NET Native, le Common Language Runtime ignore cette interface.</span><span class="sxs-lookup"><span data-stu-id="18f42-114">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="18f42-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="18f42-115">Requirements</span></span>  
 <span data-ttu-id="18f42-116">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="18f42-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="18f42-117">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="18f42-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="18f42-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="18f42-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="18f42-119">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="18f42-119">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="18f42-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18f42-120">See Also</span></span>  
 [<span data-ttu-id="18f42-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="18f42-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="18f42-122">Débogage</span><span class="sxs-lookup"><span data-stu-id="18f42-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
