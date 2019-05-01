---
title: ICorDebugStringValue, interface
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
ms.openlocfilehash: 6709b14ce8e7bc131f9feb7a277fb41851ee4352
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61994264"
---
# <a name="icordebugstringvalue-interface"></a><span data-ttu-id="d8589-102">ICorDebugStringValue, interface</span><span class="sxs-lookup"><span data-stu-id="d8589-102">ICorDebugStringValue Interface</span></span>
<span data-ttu-id="d8589-103">Une sous-classe de ICorDebugHeapValue qui s’applique aux valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="d8589-103">A subclass of ICorDebugHeapValue that applies to string values.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d8589-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d8589-104">Methods</span></span>  
  
|<span data-ttu-id="d8589-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="d8589-105">Method</span></span>|<span data-ttu-id="d8589-106">Description</span><span class="sxs-lookup"><span data-stu-id="d8589-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d8589-107">GetLength, méthode</span><span class="sxs-lookup"><span data-stu-id="d8589-107">GetLength Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstringvalue-getlength-method.md)|<span data-ttu-id="d8589-108">Obtient le nombre de caractères dans la chaîne référencée par ce `ICorDebugStringValue`.</span><span class="sxs-lookup"><span data-stu-id="d8589-108">Gets the number of characters in the string referenced by this `ICorDebugStringValue`.</span></span>|  
|[<span data-ttu-id="d8589-109">GetString, méthode</span><span class="sxs-lookup"><span data-stu-id="d8589-109">GetString Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstringvalue-getstring-method.md)|<span data-ttu-id="d8589-110">Obtient la chaîne référencée par ce `ICorDebugStringValue`.</span><span class="sxs-lookup"><span data-stu-id="d8589-110">Gets the string referenced by this `ICorDebugStringValue`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d8589-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d8589-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d8589-112">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="d8589-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d8589-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8589-113">Requirements</span></span>  
 <span data-ttu-id="d8589-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d8589-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d8589-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d8589-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d8589-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d8589-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d8589-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d8589-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d8589-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8589-118">See also</span></span>

- [<span data-ttu-id="d8589-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d8589-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
