---
title: ICorDebugModuleEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugModuleEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModuleEnum
helpviewer_keywords:
- ICorDebugModuleEnum interface [.NET Framework debugging]
ms.assetid: 2fb93cd6-6d47-4fdc-a9a0-047726fd03a1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 26efb3e43642b6d1fd10b084c2b321609c89d89b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59146508"
---
# <a name="icordebugmoduleenum-interface"></a><span data-ttu-id="c41f3-102">ICorDebugModuleEnum, interface</span><span class="sxs-lookup"><span data-stu-id="c41f3-102">ICorDebugModuleEnum Interface</span></span>

<span data-ttu-id="c41f3-103">Implémente les méthodes ICorDebugEnum et énumère des tableaux de ICorDebugModule.</span><span class="sxs-lookup"><span data-stu-id="c41f3-103">Implements ICorDebugEnum methods, and enumerates ICorDebugModule arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c41f3-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c41f3-104">Methods</span></span>  
  
|<span data-ttu-id="c41f3-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="c41f3-105">Method</span></span>|<span data-ttu-id="c41f3-106">Description</span><span class="sxs-lookup"><span data-stu-id="c41f3-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c41f3-107">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="c41f3-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmoduleenum-next-method.md)|<span data-ttu-id="c41f3-108">Obtient le nombre spécifié de `ICorDebugModule` instances à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="c41f3-108">Gets the specified number of `ICorDebugModule` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c41f3-109">Notes</span><span class="sxs-lookup"><span data-stu-id="c41f3-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c41f3-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="c41f3-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c41f3-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c41f3-111">Requirements</span></span>  
 <span data-ttu-id="c41f3-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c41f3-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c41f3-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c41f3-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c41f3-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c41f3-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="c41f3-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="c41f3-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="c41f3-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c41f3-116">See also</span></span>

- [<span data-ttu-id="c41f3-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="c41f3-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
