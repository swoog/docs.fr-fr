---
title: ICorDebugInternalFrame, interface
ms.date: 03/30/2017
api_name:
- ICorDebugInternalFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugInternalFrame
helpviewer_keywords:
- ICorDebugInternalFrame interface [.NET Framework debugging]
ms.assetid: bb4772ca-0d54-4185-b738-7a6ffe9ea85a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2f16b4628215bee2410708edeb337b41fbdc0311
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59109822"
---
# <a name="icordebuginternalframe-interface"></a><span data-ttu-id="0288a-102">ICorDebugInternalFrame, interface</span><span class="sxs-lookup"><span data-stu-id="0288a-102">ICorDebugInternalFrame Interface</span></span>

<span data-ttu-id="0288a-103">Représente un frame interne d’exécution sur la pile.</span><span class="sxs-lookup"><span data-stu-id="0288a-103">Represents a runtime-internal frame on the stack.</span></span> <span data-ttu-id="0288a-104">Cette interface est une sous-classe de l’interface ICorDebugFrame.</span><span class="sxs-lookup"><span data-stu-id="0288a-104">This interface is a subclass of the ICorDebugFrame interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0288a-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0288a-105">Methods</span></span>  
  
|<span data-ttu-id="0288a-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="0288a-106">Method</span></span>|<span data-ttu-id="0288a-107">Description</span><span class="sxs-lookup"><span data-stu-id="0288a-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0288a-108">GetFrameType, méthode</span><span class="sxs-lookup"><span data-stu-id="0288a-108">GetFrameType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginternalframe-getframetype-method.md)|<span data-ttu-id="0288a-109">Obtient le type de ce frame interne.</span><span class="sxs-lookup"><span data-stu-id="0288a-109">Gets the type of this internal frame.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0288a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0288a-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0288a-111">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="0288a-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0288a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0288a-112">Requirements</span></span>  
 <span data-ttu-id="0288a-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0288a-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0288a-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0288a-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0288a-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0288a-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="0288a-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="0288a-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0288a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0288a-117">See also</span></span>

- [<span data-ttu-id="0288a-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="0288a-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
