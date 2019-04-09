---
title: ICorDebugThreadEnum, interface
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
ms.openlocfilehash: 7edf103e397c6e3e1577b5ed4bc8fc0df264b843
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59137993"
---
# <a name="icordebugthreadenum-interface"></a><span data-ttu-id="8dfec-102">ICorDebugThreadEnum, interface</span><span class="sxs-lookup"><span data-stu-id="8dfec-102">ICorDebugThreadEnum Interface</span></span>
<span data-ttu-id="8dfec-103">Implémente les méthodes ICorDebugEnum et énumère des tableaux ICorDebugThread.</span><span class="sxs-lookup"><span data-stu-id="8dfec-103">Implements ICorDebugEnum methods and enumerates ICorDebugThread arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8dfec-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8dfec-104">Methods</span></span>  
  
|<span data-ttu-id="8dfec-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="8dfec-105">Method</span></span>|<span data-ttu-id="8dfec-106">Description</span><span class="sxs-lookup"><span data-stu-id="8dfec-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8dfec-107">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="8dfec-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthreadenum-next-method.md)|<span data-ttu-id="8dfec-108">Obtient le nombre spécifié de `ICorDebugThread` instances à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="8dfec-108">Gets the specified number of `ICorDebugThread` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8dfec-109">Notes</span><span class="sxs-lookup"><span data-stu-id="8dfec-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8dfec-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="8dfec-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8dfec-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8dfec-111">Requirements</span></span>  
 <span data-ttu-id="8dfec-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8dfec-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8dfec-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8dfec-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8dfec-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8dfec-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="8dfec-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="8dfec-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="8dfec-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dfec-116">See also</span></span>

- [<span data-ttu-id="8dfec-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="8dfec-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
