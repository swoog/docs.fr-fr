---
title: ICorDebugBreakpoint, interface
ms.date: 03/30/2017
api_name:
- ICorDebugBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBreakpoint
helpviewer_keywords:
- ICorDebugBreakpoint interface [.NET Framework debugging]
ms.assetid: aa5ad3d7-e1bb-42af-99bc-471224e3bcaa
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a7e454c15ddfa977a6d06921a5d80a6c05dca92f
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56973572"
---
# <a name="icordebugbreakpoint-interface"></a><span data-ttu-id="ff128-102">ICorDebugBreakpoint, interface</span><span class="sxs-lookup"><span data-stu-id="ff128-102">ICorDebugBreakpoint Interface</span></span>

<span data-ttu-id="ff128-103">Représente un point d’arrêt dans une fonction ou un point de contrôle sur une valeur.</span><span class="sxs-lookup"><span data-stu-id="ff128-103">Represents a breakpoint in a function, or a watch point on a value.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ff128-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ff128-104">Methods</span></span>  
  
|<span data-ttu-id="ff128-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="ff128-105">Method</span></span>|<span data-ttu-id="ff128-106">Description</span><span class="sxs-lookup"><span data-stu-id="ff128-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ff128-107">Activate, méthode</span><span class="sxs-lookup"><span data-stu-id="ff128-107">Activate Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugbreakpoint-activate-method.md)|<span data-ttu-id="ff128-108">Définit l’état actif de ce `ICorDebugBreakpoint`.</span><span class="sxs-lookup"><span data-stu-id="ff128-108">Sets the active state of this `ICorDebugBreakpoint`.</span></span>|  
|[<span data-ttu-id="ff128-109">IsActive, méthode</span><span class="sxs-lookup"><span data-stu-id="ff128-109">IsActive Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugbreakpoint-isactive-method.md)|<span data-ttu-id="ff128-110">Obtient une valeur qui indique si ce `ICorDebugBreakpoint` est actif.</span><span class="sxs-lookup"><span data-stu-id="ff128-110">Gets a value that indicates whether this `ICorDebugBreakpoint` is active.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ff128-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ff128-111">Remarks</span></span>  
 <span data-ttu-id="ff128-112">Points d’arrêt ne prennent pas directement en charge les expressions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="ff128-112">Breakpoints do not directly support conditional expressions.</span></span> <span data-ttu-id="ff128-113">Si cette fonctionnalité est souhaitée, un débogueur doit implémenter en haut de `ICorDebugBreakpoint`.</span><span class="sxs-lookup"><span data-stu-id="ff128-113">If such functionality is desired, a debugger must implement it on top of `ICorDebugBreakpoint`.</span></span>  
  
 <span data-ttu-id="ff128-114">Étend l’interface ICorDebugFunctionBreakpoint `ICorDebugBreakpoint` pour prendre en charge des points d’arrêt dans les fonctions.</span><span class="sxs-lookup"><span data-stu-id="ff128-114">The ICorDebugFunctionBreakpoint interface extends `ICorDebugBreakpoint` to support breakpoints within functions.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ff128-115">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="ff128-115">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ff128-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ff128-116">Requirements</span></span>  
 <span data-ttu-id="ff128-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ff128-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ff128-118">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ff128-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ff128-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ff128-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ff128-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ff128-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff128-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff128-121">See also</span></span>
- [<span data-ttu-id="ff128-122">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="ff128-122">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
