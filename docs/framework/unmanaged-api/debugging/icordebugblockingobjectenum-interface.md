---
title: ICorDebugBlockingObjectEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugBlockingObjectEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBlockingObjectEnum
helpviewer_keywords:
- ICorDebugBlockingObjectEnum interface [.NET Framework debugging]
ms.assetid: 208e5c2d-3f3f-404e-8b3c-7cccc14ddb16
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5a23d21d0ed8c6a6a226d5e58eafb7bde65a4896
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59161452"
---
# <a name="icordebugblockingobjectenum-interface"></a><span data-ttu-id="3b57e-102">ICorDebugBlockingObjectEnum, interface</span><span class="sxs-lookup"><span data-stu-id="3b57e-102">ICorDebugBlockingObjectEnum Interface</span></span>
<span data-ttu-id="3b57e-103">Fournit un énumérateur pour une liste de [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structures.</span><span class="sxs-lookup"><span data-stu-id="3b57e-103">Provides an enumerator for a list of [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structures.</span></span> <span data-ttu-id="3b57e-104">Cette interface est une sous-classe de l’interface ICorDebugEnum.</span><span class="sxs-lookup"><span data-stu-id="3b57e-104">This interface is a subclass of the ICorDebugEnum interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3b57e-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3b57e-105">Methods</span></span>  
  
|<span data-ttu-id="3b57e-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="3b57e-106">Method</span></span>|<span data-ttu-id="3b57e-107">Description</span><span class="sxs-lookup"><span data-stu-id="3b57e-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3b57e-108">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="3b57e-108">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugblockingobjectenum-next-method.md)|<span data-ttu-id="3b57e-109">Énumère une liste de [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structures.</span><span class="sxs-lookup"><span data-stu-id="3b57e-109">Enumerates through a list of [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structures.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3b57e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3b57e-110">Remarks</span></span>  
 <span data-ttu-id="3b57e-111">Chaque structure `CorDebugBlockingObject` représente un objet qui bloque un thread.</span><span class="sxs-lookup"><span data-stu-id="3b57e-111">Each `CorDebugBlockingObject` structure represents an object that is blocking a thread.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3b57e-112">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="3b57e-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3b57e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b57e-113">Requirements</span></span>  
 <span data-ttu-id="3b57e-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3b57e-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3b57e-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3b57e-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3b57e-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3b57e-116">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="3b57e-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="3b57e-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="3b57e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b57e-118">See also</span></span>

- [<span data-ttu-id="3b57e-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="3b57e-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="3b57e-120">Débogage</span><span class="sxs-lookup"><span data-stu-id="3b57e-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
