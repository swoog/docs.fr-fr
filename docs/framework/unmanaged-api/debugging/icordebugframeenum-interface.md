---
title: ICorDebugFrameEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugFrameEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrameEnum
helpviewer_keywords:
- ICorDebugFrameEnum interface [.NET Framework debugging]
ms.assetid: ee3f85d3-044e-46b8-945c-93ebfa5d9e91
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cd24dfa6771ca450e79b4b932735968ecc51fc90
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59093817"
---
# <a name="icordebugframeenum-interface"></a><span data-ttu-id="4793f-102">ICorDebugFrameEnum, interface</span><span class="sxs-lookup"><span data-stu-id="4793f-102">ICorDebugFrameEnum Interface</span></span>

<span data-ttu-id="4793f-103">Implémente les méthodes ICorDebugEnum et énumère des tableaux ICorDebugFrame.</span><span class="sxs-lookup"><span data-stu-id="4793f-103">Implements ICorDebugEnum methods, and enumerates ICorDebugFrame arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4793f-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4793f-104">Methods</span></span>  
  
|<span data-ttu-id="4793f-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="4793f-105">Method</span></span>|<span data-ttu-id="4793f-106">Description</span><span class="sxs-lookup"><span data-stu-id="4793f-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4793f-107">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="4793f-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugframeenum-next-method.md)|<span data-ttu-id="4793f-108">Obtient le nombre spécifié de `ICorDebugFrame` instances à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="4793f-108">Gets the specified number of `ICorDebugFrame` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4793f-109">Notes</span><span class="sxs-lookup"><span data-stu-id="4793f-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4793f-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="4793f-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4793f-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4793f-111">Requirements</span></span>  
 <span data-ttu-id="4793f-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4793f-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4793f-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4793f-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4793f-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4793f-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="4793f-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="4793f-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="4793f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4793f-116">See also</span></span>

- [<span data-ttu-id="4793f-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="4793f-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
