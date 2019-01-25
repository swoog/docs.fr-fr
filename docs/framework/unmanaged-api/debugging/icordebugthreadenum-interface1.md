---
title: ICorDebugThreadEnum Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugThreadEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThreadEnum
helpviewer_keywords:
- ICorDebugThreadEnum interface [.NET Framework debugging]
ms.assetid: 796de687-7dd4-4b7b-a10b-8bf22dc7779f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 100dc6c83c7c1d45ddb2ea0396c5115c4d79a7f8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54560358"
---
# <a name="icordebugthreadenum-interface1"></a><span data-ttu-id="90679-102">ICorDebugThreadEnum Interface1</span><span class="sxs-lookup"><span data-stu-id="90679-102">ICorDebugThreadEnum Interface1</span></span>
<span data-ttu-id="90679-103">Implémente les méthodes ICorDebugEnum et énumère des tableaux ICorDebugThread.</span><span class="sxs-lookup"><span data-stu-id="90679-103">Implements ICorDebugEnum methods and enumerates ICorDebugThread arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="90679-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="90679-104">Methods</span></span>  
  
|<span data-ttu-id="90679-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="90679-105">Method</span></span>|<span data-ttu-id="90679-106">Description</span><span class="sxs-lookup"><span data-stu-id="90679-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="90679-107">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="90679-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthreadenum-next-method.md)|<span data-ttu-id="90679-108">Obtient le nombre spécifié de `ICorDebugThread` instances à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="90679-108">Gets the specified number of `ICorDebugThread` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="90679-109">Notes</span><span class="sxs-lookup"><span data-stu-id="90679-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="90679-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="90679-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="90679-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="90679-111">Requirements</span></span>  
 <span data-ttu-id="90679-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="90679-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="90679-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="90679-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="90679-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="90679-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="90679-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="90679-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="90679-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90679-116">See also</span></span>
- [<span data-ttu-id="90679-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="90679-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
