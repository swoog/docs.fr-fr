---
title: ICorDebugValue3, interface
ms.date: 03/30/2017
api_name:
- ICorDebugValue3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue3
helpviewer_keywords:
- ICorDebugValue3 interface [.NET Framework debugging]
ms.assetid: 7d5385d3-f4a5-47c4-8478-a3513b5e9406
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d70a6f5c1df771c514f5f91770b4c53c55fec364
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33420659"
---
# <a name="icordebugvalue3-interface"></a><span data-ttu-id="267d7-102">ICorDebugValue3, interface</span><span class="sxs-lookup"><span data-stu-id="267d7-102">ICorDebugValue3 Interface</span></span>
<span data-ttu-id="267d7-103">Étend les interfaces « ICorDebugValue » et « ICorDebugValue2 » pour prendre en charge pour les tableaux supérieurs à 2 Go.</span><span class="sxs-lookup"><span data-stu-id="267d7-103">Extends the "ICorDebugValue" and "ICorDebugValue2" interfaces to provide support for arrays that are larger than 2 GB.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="267d7-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="267d7-104">Methods</span></span>  
  
|<span data-ttu-id="267d7-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="267d7-105">Method</span></span>|<span data-ttu-id="267d7-106">Description</span><span class="sxs-lookup"><span data-stu-id="267d7-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="267d7-107">GetSize64, méthode</span><span class="sxs-lookup"><span data-stu-id="267d7-107">GetSize64 Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-getsize64-method.md)|<span data-ttu-id="267d7-108">Obtient la taille, en octets, de ce `ICorDebugValue3` objet.</span><span class="sxs-lookup"><span data-stu-id="267d7-108">Gets the size, in bytes, of this `ICorDebugValue3` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="267d7-109">Notes</span><span class="sxs-lookup"><span data-stu-id="267d7-109">Remarks</span></span>  
 <span data-ttu-id="267d7-110">Le [ICorDebugValue::GetSize](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-getsize64-method.md) méthode retourne une taille de l’objet qui s’étend de 0 à 2 147 483 647 octets.</span><span class="sxs-lookup"><span data-stu-id="267d7-110">The [ICorDebugValue::GetSize](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-getsize64-method.md) method returns an object size that ranges from 0 to 2,147,483,647 bytes.</span></span> <span data-ttu-id="267d7-111">Dans la [!INCLUDE[net_v45](../../../../includes/net-v45-md.md)], la taille des tableaux peut dépasser 2 Go.</span><span class="sxs-lookup"><span data-stu-id="267d7-111">In the [!INCLUDE[net_v45](../../../../includes/net-v45-md.md)], the size of arrays can exceed 2 GB.</span></span> <span data-ttu-id="267d7-112">Le `ICorDebugValue3` interface vous permet de déterminer la taille de ces tableaux.</span><span class="sxs-lookup"><span data-stu-id="267d7-112">The `ICorDebugValue3` interface enables you to determine the size of these arrays.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="267d7-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="267d7-113">Requirements</span></span>  
 <span data-ttu-id="267d7-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="267d7-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="267d7-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="267d7-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="267d7-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="267d7-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="267d7-117">**Versions du .NET framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="267d7-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="267d7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="267d7-118">See Also</span></span>  
    
    
 [<span data-ttu-id="267d7-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="267d7-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="267d7-120">Débogage</span><span class="sxs-lookup"><span data-stu-id="267d7-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
