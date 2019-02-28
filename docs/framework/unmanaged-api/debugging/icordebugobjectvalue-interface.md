---
title: ICorDebugObjectValue, interface
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
ms.openlocfilehash: 7cae8a695ccf313b846c8860309c3461a821fe38
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56977212"
---
# <a name="icordebugobjectvalue-interface"></a><span data-ttu-id="f70df-102">ICorDebugObjectValue, interface</span><span class="sxs-lookup"><span data-stu-id="f70df-102">ICorDebugObjectValue Interface</span></span>

<span data-ttu-id="f70df-103">Une sous-classe de « ICorDebugValue » qui représente une valeur qui contient un objet.</span><span class="sxs-lookup"><span data-stu-id="f70df-103">A subclass of "ICorDebugValue" that represents a value that contains an object.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f70df-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f70df-104">Methods</span></span>  
  
|<span data-ttu-id="f70df-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="f70df-105">Method</span></span>|<span data-ttu-id="f70df-106">Description</span><span class="sxs-lookup"><span data-stu-id="f70df-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f70df-107">GetClass, méthode</span><span class="sxs-lookup"><span data-stu-id="f70df-107">GetClass Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getclass-method.md)|<span data-ttu-id="f70df-108">Obtient un pointeur d’interface vers le common language runtime (CLR) <xref:System.Type> de l’objet que ce `ICorDebugObjectValue` références.</span><span class="sxs-lookup"><span data-stu-id="f70df-108">Gets an interface pointer to the common language runtime (CLR) <xref:System.Type> of the object that this `ICorDebugObjectValue` references.</span></span>|  
|[<span data-ttu-id="f70df-109">GetContext, méthode</span><span class="sxs-lookup"><span data-stu-id="f70df-109">GetContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getcontext-method.md)|<span data-ttu-id="f70df-110">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="f70df-110">Not implemented.</span></span>|  
|[<span data-ttu-id="f70df-111">GetFieldValue, méthode</span><span class="sxs-lookup"><span data-stu-id="f70df-111">GetFieldValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getfieldvalue-method.md)|<span data-ttu-id="f70df-112">Obtient un pointeur d’interface vers un [ICorDebugValue](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-interface.md) qui représente la valeur du champ spécifié de la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f70df-112">Gets an interface pointer to an [ICorDebugValue](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-interface.md) that represents the value of the specified field of the specified class.</span></span>|  
|[<span data-ttu-id="f70df-113">GetManagedCopy, méthode</span><span class="sxs-lookup"><span data-stu-id="f70df-113">GetManagedCopy Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getmanagedcopy-method.md)|<span data-ttu-id="f70df-114">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="f70df-114">Obsolete.</span></span> <span data-ttu-id="f70df-115">N'appelez pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f70df-115">Do not call this method.</span></span>|  
|[<span data-ttu-id="f70df-116">GetVirtualMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="f70df-116">GetVirtualMethod Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getvirtualmethod-method.md)|<span data-ttu-id="f70df-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="f70df-117">Not implemented.</span></span>|  
|[<span data-ttu-id="f70df-118">IsValueClass, méthode</span><span class="sxs-lookup"><span data-stu-id="f70df-118">IsValueClass Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-isvalueclass-method.md)|<span data-ttu-id="f70df-119">Obtient une valeur qui indique si l’objet référencé par ce `ICorDebugObjectValue` est un type valeur.</span><span class="sxs-lookup"><span data-stu-id="f70df-119">Gets a value that indicates whether the object referenced by this `ICorDebugObjectValue` is a value type.</span></span>|  
|[<span data-ttu-id="f70df-120">SetFromManagedCopy, méthode</span><span class="sxs-lookup"><span data-stu-id="f70df-120">SetFromManagedCopy Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-setfrommanagedcopy-method.md)|<span data-ttu-id="f70df-121">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="f70df-121">Obsolete.</span></span> <span data-ttu-id="f70df-122">N'appelez pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f70df-122">Do not call this method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f70df-123">Notes</span><span class="sxs-lookup"><span data-stu-id="f70df-123">Remarks</span></span>  
 <span data-ttu-id="f70df-124">Un `ICorDebugObjectValue` reste valide jusqu'à ce que le processus en cours de débogage se poursuit.</span><span class="sxs-lookup"><span data-stu-id="f70df-124">An `ICorDebugObjectValue` remains valid until the process being debugged is continued.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f70df-125">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="f70df-125">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f70df-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f70df-126">Requirements</span></span>  
 <span data-ttu-id="f70df-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f70df-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f70df-128">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f70df-128">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f70df-129">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f70df-129">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f70df-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f70df-130">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f70df-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f70df-131">See also</span></span>
- [<span data-ttu-id="f70df-132">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="f70df-132">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)

