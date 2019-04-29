---
title: ICorDebugObjectEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugObjectEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugObjectEnum
helpviewer_keywords:
- ICorDebugObjectEnum interface [.NET Framework debugging]
ms.assetid: 9ffb4498-7719-49d3-8890-df2c22248a0c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0144539987f14bed83bfc9eab2f5ca26d2a609ae
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61942387"
---
# <a name="icordebugobjectenum-interface"></a><span data-ttu-id="6574e-102">ICorDebugObjectEnum, interface</span><span class="sxs-lookup"><span data-stu-id="6574e-102">ICorDebugObjectEnum Interface</span></span>

<span data-ttu-id="6574e-103">Implémente les méthodes ICorDebugEnum et énumère des tableaux d’objets par leurs adresses virtuelles relatives (RVA).</span><span class="sxs-lookup"><span data-stu-id="6574e-103">Implements ICorDebugEnum methods, and enumerates arrays of objects by their relative virtual addresses (RVAs).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="6574e-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6574e-104">Methods</span></span>  
  
|<span data-ttu-id="6574e-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="6574e-105">Method</span></span>|<span data-ttu-id="6574e-106">Description</span><span class="sxs-lookup"><span data-stu-id="6574e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6574e-107">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="6574e-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectenum-next-method.md)|<span data-ttu-id="6574e-108">Obtient les adresses virtuelles relatives du nombre spécifié d’objets à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="6574e-108">Gets the RVAs of the specified number of objects from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6574e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="6574e-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6574e-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="6574e-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6574e-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6574e-111">Requirements</span></span>  
 <span data-ttu-id="6574e-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6574e-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6574e-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6574e-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6574e-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6574e-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6574e-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6574e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6574e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6574e-116">See also</span></span>

- [<span data-ttu-id="6574e-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="6574e-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
