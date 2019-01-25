---
title: ICorDebugCode3, interface
ms.date: 03/30/2017
api_name:
- ICorDebugCode3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode3
helpviewer_keywords:
- ICorDebugCode3 interface [.NET Framework debugging]
ms.assetid: 70f07c9e-0614-4bee-ac34-09fe6c51c5a9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7b3b29be2bab2d1b4cea5dcec89e31d4720be769
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54576874"
---
# <a name="icordebugcode3-interface"></a><span data-ttu-id="44d3a-102">ICorDebugCode3, interface</span><span class="sxs-lookup"><span data-stu-id="44d3a-102">ICorDebugCode3 Interface</span></span>
<span data-ttu-id="44d3a-103">Fournit une méthode qui étend les « ICorDebugCode » et « ICorDebugCode2 » pour fournir des informations sur une valeur de retour managée.</span><span class="sxs-lookup"><span data-stu-id="44d3a-103">Provides a method that extends "ICorDebugCode" and "ICorDebugCode2" to provide information about a managed return value.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="44d3a-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="44d3a-104">Methods</span></span>  
  
|<span data-ttu-id="44d3a-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="44d3a-105">Method</span></span>|<span data-ttu-id="44d3a-106">Description</span><span class="sxs-lookup"><span data-stu-id="44d3a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="44d3a-107">GetReturnValueLiveOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="44d3a-107">GetReturnValueLiveOffset Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode3-getreturnvalueliveoffset-method.md)|<span data-ttu-id="44d3a-108">Pour un offset IL spécifié, obtient les offsets natifs où un point d’arrêt doit être placé afin que le débogueur puisse obtenir la valeur de retour d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="44d3a-108">For a specified IL offset, gets the native offsets where a breakpoint should be placed so that the debugger can obtain the return value from a function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="44d3a-109">Notes</span><span class="sxs-lookup"><span data-stu-id="44d3a-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="44d3a-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="44d3a-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="44d3a-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="44d3a-111">Requirements</span></span>  
 <span data-ttu-id="44d3a-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="44d3a-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="44d3a-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="44d3a-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="44d3a-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="44d3a-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="44d3a-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="44d3a-115">**.NET Framework Versions:** [!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44d3a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44d3a-116">See also</span></span>



- [<span data-ttu-id="44d3a-117">ICorDebugILFrame3, interface</span><span class="sxs-lookup"><span data-stu-id="44d3a-117">ICorDebugILFrame3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe3-interface.md)
- [<span data-ttu-id="44d3a-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="44d3a-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
