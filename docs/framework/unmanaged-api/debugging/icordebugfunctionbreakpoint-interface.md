---
title: ICorDebugFunctionBreakpoint, interface
ms.date: 03/30/2017
api_name:
- ICorDebugFunctionBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunctionBreakpoint
helpviewer_keywords:
- ICorDebugFunctionBreakpoint interface [.NET Framework debugging]
ms.assetid: 9c149303-14b1-4138-83d7-e8c3e0fcd332
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2c3c11d3b6a6daec7b35377ef24557dd5077af21
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56977719"
---
# <a name="icordebugfunctionbreakpoint-interface"></a><span data-ttu-id="8502a-102">ICorDebugFunctionBreakpoint, interface</span><span class="sxs-lookup"><span data-stu-id="8502a-102">ICorDebugFunctionBreakpoint Interface</span></span>

<span data-ttu-id="8502a-103">Étend l’interface ICorDebugBreakpoint pour prendre en charge des points d’arrêt dans les fonctions.</span><span class="sxs-lookup"><span data-stu-id="8502a-103">Extends the ICorDebugBreakpoint interface to support breakpoints within functions.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8502a-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8502a-104">Methods</span></span>  
  
|<span data-ttu-id="8502a-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="8502a-105">Method</span></span>|<span data-ttu-id="8502a-106">Description</span><span class="sxs-lookup"><span data-stu-id="8502a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8502a-107">GetFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="8502a-107">GetFunction Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugfunctionbreakpoint-getfunction-method.md)|<span data-ttu-id="8502a-108">Obtient un pointeur d’interface ICorDebugFunction qui référence la fonction dans laquelle le point d’arrêt est défini.</span><span class="sxs-lookup"><span data-stu-id="8502a-108">Gets an interface pointer to an ICorDebugFunction that references the function in which the breakpoint is set.</span></span>|  
|[<span data-ttu-id="8502a-109">GetOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="8502a-109">GetOffset Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugfunctionbreakpoint-getoffset-method.md)|<span data-ttu-id="8502a-110">Obtient l’offset du point d’arrêt dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="8502a-110">Gets the offset of the breakpoint within the function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8502a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8502a-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8502a-112">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="8502a-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8502a-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8502a-113">Requirements</span></span>  
 <span data-ttu-id="8502a-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8502a-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8502a-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8502a-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8502a-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8502a-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8502a-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8502a-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8502a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8502a-118">See also</span></span>
- [<span data-ttu-id="8502a-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="8502a-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
