---
title: ICorDebugHeapValue Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue
helpviewer_keywords:
- ICorDebugHeapValue interface [.NET Framework debugging]
ms.assetid: 1bca66db-0359-4ae8-846e-e35f7e547e8b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a87790647ed8896f072aa8e943e31fa1980e3f62
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54622856"
---
# <a name="icordebugheapvalue-interface1"></a><span data-ttu-id="3b880-102">ICorDebugHeapValue Interface1</span><span class="sxs-lookup"><span data-stu-id="3b880-102">ICorDebugHeapValue Interface1</span></span>
<span data-ttu-id="3b880-103">Une sous-classe de « ICorDebugValue » qui représente un objet qui a été collecté par le garbage collector du common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="3b880-103">A subclass of "ICorDebugValue" that represents an object that has been collected by the common language runtime (CLR) garbage collector.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3b880-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3b880-104">Methods</span></span>  
  
|<span data-ttu-id="3b880-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="3b880-105">Method</span></span>|<span data-ttu-id="3b880-106">Description</span><span class="sxs-lookup"><span data-stu-id="3b880-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3b880-107">CreateRelocBreakpoint, méthode</span><span class="sxs-lookup"><span data-stu-id="3b880-107">CreateRelocBreakpoint Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugheapvalue-createrelocbreakpoint-method.md)|<span data-ttu-id="3b880-108">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="3b880-108">Not implemented.</span></span>|  
|[<span data-ttu-id="3b880-109">IsValid, méthode</span><span class="sxs-lookup"><span data-stu-id="3b880-109">IsValid Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugheapvalue-isvalid-method.md)|<span data-ttu-id="3b880-110">Obtient une valeur qui indique si l’objet représenté par cet `ICorDebugHeapValue` est valide, ou a été récupéré par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="3b880-110">Gets a value that indicates whether the object represented by this `ICorDebugHeapValue` is valid, or has been reclaimed by the garbage collector.</span></span> <span data-ttu-id="3b880-111">Cette méthode a été déconseillée dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="3b880-111">This method has been deprecated in the .NET Framework version 2.0.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3b880-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3b880-112">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3b880-113">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="3b880-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3b880-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3b880-114">Requirements</span></span>  
 <span data-ttu-id="3b880-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3b880-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3b880-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3b880-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3b880-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3b880-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3b880-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3b880-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b880-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b880-119">See also</span></span>



- [<span data-ttu-id="3b880-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="3b880-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
