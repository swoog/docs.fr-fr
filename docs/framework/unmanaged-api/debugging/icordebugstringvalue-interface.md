---
title: ICorDebugStringValue Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugStringValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStringValue
helpviewer_keywords:
- ICorDebugStringValue interface [.NET Framework debugging]
ms.assetid: bf84d0af-53e1-4c04-bc5b-7e5f81ba2cc2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b9160b9013481de294e6c8dd032cfa2d0ebb405d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54596837"
---
# <a name="icordebugstringvalue-interface1"></a><span data-ttu-id="29a6e-102">ICorDebugStringValue Interface1</span><span class="sxs-lookup"><span data-stu-id="29a6e-102">ICorDebugStringValue Interface1</span></span>
<span data-ttu-id="29a6e-103">Une sous-classe de ICorDebugHeapValue qui s’applique aux valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="29a6e-103">A subclass of ICorDebugHeapValue that applies to string values.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="29a6e-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="29a6e-104">Methods</span></span>  
  
|<span data-ttu-id="29a6e-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="29a6e-105">Method</span></span>|<span data-ttu-id="29a6e-106">Description</span><span class="sxs-lookup"><span data-stu-id="29a6e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="29a6e-107">GetLength, méthode</span><span class="sxs-lookup"><span data-stu-id="29a6e-107">GetLength Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstringvalue-getlength-method.md)|<span data-ttu-id="29a6e-108">Obtient le nombre de caractères dans la chaîne référencée par ce `ICorDebugStringValue`.</span><span class="sxs-lookup"><span data-stu-id="29a6e-108">Gets the number of characters in the string referenced by this `ICorDebugStringValue`.</span></span>|  
|[<span data-ttu-id="29a6e-109">GetString, méthode</span><span class="sxs-lookup"><span data-stu-id="29a6e-109">GetString Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstringvalue-getstring-method.md)|<span data-ttu-id="29a6e-110">Obtient la chaîne référencée par ce `ICorDebugStringValue`.</span><span class="sxs-lookup"><span data-stu-id="29a6e-110">Gets the string referenced by this `ICorDebugStringValue`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="29a6e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="29a6e-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="29a6e-112">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="29a6e-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="29a6e-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="29a6e-113">Requirements</span></span>  
 <span data-ttu-id="29a6e-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="29a6e-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="29a6e-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="29a6e-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="29a6e-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="29a6e-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="29a6e-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="29a6e-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="29a6e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29a6e-118">See also</span></span>
- [<span data-ttu-id="29a6e-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="29a6e-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
