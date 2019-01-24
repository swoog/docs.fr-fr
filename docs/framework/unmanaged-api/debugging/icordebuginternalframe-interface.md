---
title: ICorDebugInternalFrame Interface1
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
ms.openlocfilehash: 1fab8221bd160a74bb44c3ed0721ad4620e93419
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54692793"
---
# <a name="icordebuginternalframe-interface1"></a><span data-ttu-id="07552-102">ICorDebugInternalFrame Interface1</span><span class="sxs-lookup"><span data-stu-id="07552-102">ICorDebugInternalFrame Interface1</span></span>
<span data-ttu-id="07552-103">Représente un frame interne d’exécution sur la pile.</span><span class="sxs-lookup"><span data-stu-id="07552-103">Represents a runtime-internal frame on the stack.</span></span> <span data-ttu-id="07552-104">Cette interface est une sous-classe de l’interface ICorDebugFrame.</span><span class="sxs-lookup"><span data-stu-id="07552-104">This interface is a subclass of the ICorDebugFrame interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="07552-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="07552-105">Methods</span></span>  
  
|<span data-ttu-id="07552-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="07552-106">Method</span></span>|<span data-ttu-id="07552-107">Description</span><span class="sxs-lookup"><span data-stu-id="07552-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="07552-108">GetFrameType, méthode</span><span class="sxs-lookup"><span data-stu-id="07552-108">GetFrameType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginternalframe-getframetype-method.md)|<span data-ttu-id="07552-109">Obtient le type de ce frame interne.</span><span class="sxs-lookup"><span data-stu-id="07552-109">Gets the type of this internal frame.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="07552-110">Notes</span><span class="sxs-lookup"><span data-stu-id="07552-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="07552-111">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="07552-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="07552-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="07552-112">Requirements</span></span>  
 <span data-ttu-id="07552-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="07552-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="07552-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="07552-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="07552-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="07552-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="07552-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="07552-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="07552-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07552-117">See also</span></span>
- [<span data-ttu-id="07552-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="07552-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
