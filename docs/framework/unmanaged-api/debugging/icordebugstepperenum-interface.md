---
title: ICorDebugStepperEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugStepperEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepperEnum
helpviewer_keywords:
- ICorDebugStepperEnum interface [.NET Framework debugging]
ms.assetid: 988718c1-1a4a-40f2-a04c-7d67e5cfe1e2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 89552a099241f1bec61f9aa8a8321ef9932e886c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59173223"
---
# <a name="icordebugstepperenum-interface"></a><span data-ttu-id="035fd-102">ICorDebugStepperEnum, interface</span><span class="sxs-lookup"><span data-stu-id="035fd-102">ICorDebugStepperEnum Interface</span></span>
<span data-ttu-id="035fd-103">Implémente les méthodes ICorDebugEnum et énumère des tableaux de ICorDebugStepper.</span><span class="sxs-lookup"><span data-stu-id="035fd-103">Implements ICorDebugEnum methods, and enumerates ICorDebugStepper arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="035fd-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="035fd-104">Methods</span></span>  
  
|<span data-ttu-id="035fd-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="035fd-105">Method</span></span>|<span data-ttu-id="035fd-106">Description</span><span class="sxs-lookup"><span data-stu-id="035fd-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="035fd-107">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="035fd-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstepperenum-next-method.md)|<span data-ttu-id="035fd-108">Obtient le nombre spécifié de `ICorDebugStepper` instances à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="035fd-108">Gets the specified number of `ICorDebugStepper` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="035fd-109">Notes</span><span class="sxs-lookup"><span data-stu-id="035fd-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="035fd-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="035fd-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="035fd-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="035fd-111">Requirements</span></span>  
 <span data-ttu-id="035fd-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="035fd-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="035fd-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="035fd-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="035fd-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="035fd-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="035fd-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="035fd-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="035fd-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="035fd-116">See also</span></span>

- [<span data-ttu-id="035fd-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="035fd-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
