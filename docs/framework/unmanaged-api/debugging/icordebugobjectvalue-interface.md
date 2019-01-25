---
title: ICorDebugObjectValue Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugObjectValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugObjectValue
helpviewer_keywords:
- ICorDebugObjectValue interface [.NET Framework debugging]
ms.assetid: 937de6a0-6fbf-4ddc-80ea-a6217b73e62b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5cd991049c159b96a0f0717b31d6a2834b250f70
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631986"
---
# <a name="icordebugobjectvalue-interface1"></a><span data-ttu-id="33318-102">ICorDebugObjectValue Interface1</span><span class="sxs-lookup"><span data-stu-id="33318-102">ICorDebugObjectValue Interface1</span></span>
<span data-ttu-id="33318-103">Une sous-classe de « ICorDebugValue » qui représente une valeur qui contient un objet.</span><span class="sxs-lookup"><span data-stu-id="33318-103">A subclass of "ICorDebugValue" that represents a value that contains an object.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="33318-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="33318-104">Methods</span></span>  
  
|<span data-ttu-id="33318-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="33318-105">Method</span></span>|<span data-ttu-id="33318-106">Description</span><span class="sxs-lookup"><span data-stu-id="33318-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="33318-107">GetClass, méthode</span><span class="sxs-lookup"><span data-stu-id="33318-107">GetClass Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getclass-method.md)|<span data-ttu-id="33318-108">Obtient un pointeur d’interface vers le common language runtime (CLR) <xref:System.Type> de l’objet que ce `ICorDebugObjectValue` références.</span><span class="sxs-lookup"><span data-stu-id="33318-108">Gets an interface pointer to the common language runtime (CLR) <xref:System.Type> of the object that this `ICorDebugObjectValue` references.</span></span>|  
|[<span data-ttu-id="33318-109">GetContext, méthode</span><span class="sxs-lookup"><span data-stu-id="33318-109">GetContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getcontext-method.md)|<span data-ttu-id="33318-110">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="33318-110">Not implemented.</span></span>|  
|[<span data-ttu-id="33318-111">GetFieldValue, méthode</span><span class="sxs-lookup"><span data-stu-id="33318-111">GetFieldValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getfieldvalue-method.md)|<span data-ttu-id="33318-112">Obtient un pointeur d’interface vers un [ICorDebugValue](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-interface.md) qui représente la valeur du champ spécifié de la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="33318-112">Gets an interface pointer to an [ICorDebugValue](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-interface.md) that represents the value of the specified field of the specified class.</span></span>|  
|[<span data-ttu-id="33318-113">GetManagedCopy, méthode</span><span class="sxs-lookup"><span data-stu-id="33318-113">GetManagedCopy Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getmanagedcopy-method.md)|<span data-ttu-id="33318-114">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="33318-114">Obsolete.</span></span> <span data-ttu-id="33318-115">N'appelez pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="33318-115">Do not call this method.</span></span>|  
|[<span data-ttu-id="33318-116">GetVirtualMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="33318-116">GetVirtualMethod Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getvirtualmethod-method.md)|<span data-ttu-id="33318-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="33318-117">Not implemented.</span></span>|  
|[<span data-ttu-id="33318-118">IsValueClass, méthode</span><span class="sxs-lookup"><span data-stu-id="33318-118">IsValueClass Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-isvalueclass-method.md)|<span data-ttu-id="33318-119">Obtient une valeur qui indique si l’objet référencé par ce `ICorDebugObjectValue` est un type valeur.</span><span class="sxs-lookup"><span data-stu-id="33318-119">Gets a value that indicates whether the object referenced by this `ICorDebugObjectValue` is a value type.</span></span>|  
|[<span data-ttu-id="33318-120">SetFromManagedCopy, méthode</span><span class="sxs-lookup"><span data-stu-id="33318-120">SetFromManagedCopy Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-setfrommanagedcopy-method.md)|<span data-ttu-id="33318-121">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="33318-121">Obsolete.</span></span> <span data-ttu-id="33318-122">N'appelez pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="33318-122">Do not call this method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="33318-123">Notes</span><span class="sxs-lookup"><span data-stu-id="33318-123">Remarks</span></span>  
 <span data-ttu-id="33318-124">Un `ICorDebugObjectValue` reste valide jusqu'à ce que le processus en cours de débogage se poursuit.</span><span class="sxs-lookup"><span data-stu-id="33318-124">An `ICorDebugObjectValue` remains valid until the process being debugged is continued.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="33318-125">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="33318-125">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="33318-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="33318-126">Requirements</span></span>  
 <span data-ttu-id="33318-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="33318-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="33318-128">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="33318-128">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="33318-129">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="33318-129">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="33318-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="33318-130">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="33318-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33318-131">See also</span></span>
- [<span data-ttu-id="33318-132">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="33318-132">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)

