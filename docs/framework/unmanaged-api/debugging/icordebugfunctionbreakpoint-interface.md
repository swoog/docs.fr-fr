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
ms.openlocfilehash: 0f15b9f5961699f905e765426576bdf6f3416793
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61651647"
---
# <a name="icordebugfunctionbreakpoint-interface"></a><span data-ttu-id="9db2e-102">ICorDebugFunctionBreakpoint, interface</span><span class="sxs-lookup"><span data-stu-id="9db2e-102">ICorDebugFunctionBreakpoint Interface</span></span>

<span data-ttu-id="9db2e-103">Étend l’interface ICorDebugBreakpoint pour prendre en charge des points d’arrêt dans les fonctions.</span><span class="sxs-lookup"><span data-stu-id="9db2e-103">Extends the ICorDebugBreakpoint interface to support breakpoints within functions.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9db2e-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9db2e-104">Methods</span></span>  
  
|<span data-ttu-id="9db2e-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="9db2e-105">Method</span></span>|<span data-ttu-id="9db2e-106">Description</span><span class="sxs-lookup"><span data-stu-id="9db2e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9db2e-107">GetFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="9db2e-107">GetFunction Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugfunctionbreakpoint-getfunction-method.md)|<span data-ttu-id="9db2e-108">Obtient un pointeur d’interface ICorDebugFunction qui référence la fonction dans laquelle le point d’arrêt est défini.</span><span class="sxs-lookup"><span data-stu-id="9db2e-108">Gets an interface pointer to an ICorDebugFunction that references the function in which the breakpoint is set.</span></span>|  
|[<span data-ttu-id="9db2e-109">GetOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="9db2e-109">GetOffset Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugfunctionbreakpoint-getoffset-method.md)|<span data-ttu-id="9db2e-110">Obtient l’offset du point d’arrêt dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="9db2e-110">Gets the offset of the breakpoint within the function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9db2e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9db2e-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9db2e-112">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="9db2e-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9db2e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9db2e-113">Requirements</span></span>  
 <span data-ttu-id="9db2e-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9db2e-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9db2e-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9db2e-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9db2e-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9db2e-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9db2e-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9db2e-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9db2e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9db2e-118">See also</span></span>

- [<span data-ttu-id="9db2e-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="9db2e-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
