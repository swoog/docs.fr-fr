---
title: ICorDebugBreakpointEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugBreakpointEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBreakpointEnum
helpviewer_keywords:
- ICorDebugBreakpointEnum interface [.NET Framework debugging]
ms.assetid: 4c6f4f6e-52cc-402e-881b-7b8526544c90
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7fd42f13f699b0b79fd69311186f2b2ca0c9998a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59149069"
---
# <a name="icordebugbreakpointenum-interface"></a><span data-ttu-id="d08bc-102">ICorDebugBreakpointEnum, interface</span><span class="sxs-lookup"><span data-stu-id="d08bc-102">ICorDebugBreakpointEnum Interface</span></span>

<span data-ttu-id="d08bc-103">Implémente les méthodes ICorDebugEnum et énumère des tableaux ICorDebugBreakpoint.</span><span class="sxs-lookup"><span data-stu-id="d08bc-103">Implements ICorDebugEnum methods, and enumerates ICorDebugBreakpoint arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d08bc-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d08bc-104">Methods</span></span>  
  
|<span data-ttu-id="d08bc-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="d08bc-105">Method</span></span>|<span data-ttu-id="d08bc-106">Description</span><span class="sxs-lookup"><span data-stu-id="d08bc-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d08bc-107">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="d08bc-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugbreakpointenum-next-method.md)|<span data-ttu-id="d08bc-108">Obtient le nombre spécifié de `ICorDebugBreakpoint` instances à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="d08bc-108">Gets the specified number of `ICorDebugBreakpoint` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d08bc-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d08bc-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d08bc-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="d08bc-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d08bc-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d08bc-111">Requirements</span></span>  
 <span data-ttu-id="d08bc-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d08bc-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d08bc-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d08bc-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d08bc-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d08bc-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="d08bc-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="d08bc-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="d08bc-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d08bc-116">See also</span></span>

- [<span data-ttu-id="d08bc-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d08bc-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
