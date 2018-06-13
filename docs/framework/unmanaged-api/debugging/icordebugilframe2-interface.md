---
title: ICorDebugILFrame2 Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame2
helpviewer_keywords:
- ICorDebugILFrame2 interface [.NET Framework debugging]
ms.assetid: f94b9d53-d8f8-4424-a95e-53a1bfd26e4a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ccb39609b37aff09ac7890df562d6c08e3c3c159
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33412433"
---
# <a name="icordebugilframe2-interface1"></a><span data-ttu-id="20dc6-102">ICorDebugILFrame2 Interface1</span><span class="sxs-lookup"><span data-stu-id="20dc6-102">ICorDebugILFrame2 Interface1</span></span>
<span data-ttu-id="20dc6-103">Extension logique de l’interface ICorDebugILFrame.</span><span class="sxs-lookup"><span data-stu-id="20dc6-103">A logical extension of the ICorDebugILFrame interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="20dc6-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="20dc6-104">Methods</span></span>  
  
|<span data-ttu-id="20dc6-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="20dc6-105">Method</span></span>|<span data-ttu-id="20dc6-106">Description</span><span class="sxs-lookup"><span data-stu-id="20dc6-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="20dc6-107">EnumerateTypeParameters, méthode</span><span class="sxs-lookup"><span data-stu-id="20dc6-107">EnumerateTypeParameters Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe2-enumeratetypeparameters-method.md)|<span data-ttu-id="20dc6-108">Obtient un objet du ICorDebugTypeEnum qui contient le <xref:System.Type> paramètres dans ce frame.</span><span class="sxs-lookup"><span data-stu-id="20dc6-108">Gets an ICorDebugTypeEnum object that contains the <xref:System.Type> parameters in this frame.</span></span>|  
|[<span data-ttu-id="20dc6-109">RemapFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="20dc6-109">RemapFunction Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe2-remapfunction-method.md)|<span data-ttu-id="20dc6-110">Remappe une fonction modifiée en spécifiant le nouvel offset MSIL.</span><span class="sxs-lookup"><span data-stu-id="20dc6-110">Remaps an edited function by specifying the new MSIL offset.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="20dc6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="20dc6-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="20dc6-112">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="20dc6-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="20dc6-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="20dc6-113">Requirements</span></span>  
 <span data-ttu-id="20dc6-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="20dc6-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="20dc6-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="20dc6-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="20dc6-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="20dc6-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="20dc6-117">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="20dc6-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20dc6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20dc6-118">See Also</span></span>  
 [<span data-ttu-id="20dc6-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="20dc6-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
