---
title: ICorDebugInternalFrame2, interface
ms.date: 03/30/2017
api_name:
- ICorDebugInternalFrame2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugInternalFrame2
helpviewer_keywords:
- ICorDebugInternalFrame2 interface [.NET Framework debugging]
ms.assetid: d4755569-85b8-4ff4-bf50-0e608e76429f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f4082c4204b85aba97651419db15ba8eb4c3d54e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33415160"
---
# <a name="icordebuginternalframe2-interface"></a><span data-ttu-id="e44ee-102">ICorDebugInternalFrame2, interface</span><span class="sxs-lookup"><span data-stu-id="e44ee-102">ICorDebugInternalFrame2 Interface</span></span>
<span data-ttu-id="e44ee-103">Fournit des informations sur les frames internes, notamment l’adresse de la pile et la position par rapport aux objets ICorDebugFrame.</span><span class="sxs-lookup"><span data-stu-id="e44ee-103">Provides information about internal frames, including stack address and position in relation to ICorDebugFrame objects.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e44ee-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e44ee-104">Methods</span></span>  
  
|<span data-ttu-id="e44ee-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="e44ee-105">Method</span></span>|<span data-ttu-id="e44ee-106">Description</span><span class="sxs-lookup"><span data-stu-id="e44ee-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e44ee-107">GetFrameAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="e44ee-107">GetFrameAddress Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginternalframe2-getframeaddress-method.md)|<span data-ttu-id="e44ee-108">Retourne l’adresse de la pile du frame interne.</span><span class="sxs-lookup"><span data-stu-id="e44ee-108">Returns the stack address of the internal frame.</span></span>|  
|[<span data-ttu-id="e44ee-109">IsCloserToLeaf, méthode</span><span class="sxs-lookup"><span data-stu-id="e44ee-109">IsCloserToLeaf Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginternalframe2-isclosertoleaf-method.md)|<span data-ttu-id="e44ee-110">Vérifie si le `this` frame interne est proche de la feuille de l’objet ICorDebugFrame spécifié.</span><span class="sxs-lookup"><span data-stu-id="e44ee-110">Checks whether the `this` internal frame is closer to the leaf than the specified ICorDebugFrame object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e44ee-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e44ee-111">Remarks</span></span>  
 <span data-ttu-id="e44ee-112">Cette interface étend l’interface ICorDebugInternalFrame.</span><span class="sxs-lookup"><span data-stu-id="e44ee-112">This interface extends the ICorDebugInternalFrame interface.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e44ee-113">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="e44ee-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e44ee-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e44ee-114">Requirements</span></span>  
 <span data-ttu-id="e44ee-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e44ee-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e44ee-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e44ee-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e44ee-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e44ee-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e44ee-118">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e44ee-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e44ee-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e44ee-119">See Also</span></span>  
 [<span data-ttu-id="e44ee-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="e44ee-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="e44ee-121">Débogage</span><span class="sxs-lookup"><span data-stu-id="e44ee-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
