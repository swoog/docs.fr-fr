---
title: ICorDebugValueEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugValueEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValueEnum
helpviewer_keywords:
- ICorDebugValueEnum interface [.NET Framework debugging]
ms.assetid: 88989482-a09f-4bd0-9adb-16f47b0291fd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9484f211ff31c4fa71692db646ef3c556df0acad
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59171936"
---
# <a name="icordebugvalueenum-interface"></a><span data-ttu-id="bd664-102">ICorDebugValueEnum, interface</span><span class="sxs-lookup"><span data-stu-id="bd664-102">ICorDebugValueEnum Interface</span></span>
<span data-ttu-id="bd664-103">Implémente les méthodes « ICorDebugEnum » et énumère des tableaux de « ICorDebugValue ».</span><span class="sxs-lookup"><span data-stu-id="bd664-103">Implements "ICorDebugEnum" methods and enumerates "ICorDebugValue" arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="bd664-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bd664-104">Methods</span></span>  
  
|<span data-ttu-id="bd664-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="bd664-105">Method</span></span>|<span data-ttu-id="bd664-106">Description</span><span class="sxs-lookup"><span data-stu-id="bd664-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="bd664-107">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="bd664-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalueenum-next-method.md)|<span data-ttu-id="bd664-108">Obtient le nombre spécifié de `ICorDebugValue` instances à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="bd664-108">Gets the specified number of `ICorDebugValue` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bd664-109">Notes</span><span class="sxs-lookup"><span data-stu-id="bd664-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="bd664-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="bd664-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bd664-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd664-111">Requirements</span></span>  
 <span data-ttu-id="bd664-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bd664-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bd664-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bd664-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bd664-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bd664-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bd664-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bd664-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bd664-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd664-116">See also</span></span>

- [<span data-ttu-id="bd664-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="bd664-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
