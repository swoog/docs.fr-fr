---
title: ICorDebugExceptionDebugEvent, interface
ms.date: 03/30/2017
ms.assetid: f9ba60d8-b54d-417e-bb3e-fde4b41ca44c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2e2a147d46412eb4feb192070ff8420cab842a6c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59156453"
---
# <a name="icordebugexceptiondebugevent-interface"></a><span data-ttu-id="57d6b-102">ICorDebugExceptionDebugEvent, interface</span><span class="sxs-lookup"><span data-stu-id="57d6b-102">ICorDebugExceptionDebugEvent Interface</span></span>
<span data-ttu-id="57d6b-103">Étend la [ICorDebugDebugEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md) interface pour prendre en charge les événements d’exception.</span><span class="sxs-lookup"><span data-stu-id="57d6b-103">Extends the [ICorDebugDebugEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md) interface to support exception events.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="57d6b-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="57d6b-104">Methods</span></span>  
  
|<span data-ttu-id="57d6b-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="57d6b-105">Method</span></span>|<span data-ttu-id="57d6b-106">Description</span><span class="sxs-lookup"><span data-stu-id="57d6b-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="57d6b-107">GetFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="57d6b-107">GetFlags Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-getflags-method.md)|<span data-ttu-id="57d6b-108">Obtient un indicateur qui précise si l'exception peut être interceptée.</span><span class="sxs-lookup"><span data-stu-id="57d6b-108">Gets a flag that indicates whether the exception is can be intercepted.</span></span>|  
|[<span data-ttu-id="57d6b-109">GetNativeIP, méthode</span><span class="sxs-lookup"><span data-stu-id="57d6b-109">GetNativeIP Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-getnativeip-method.md)|<span data-ttu-id="57d6b-110">Obtient le pointeur d'interface natif de cet événement de débogage d'exception.</span><span class="sxs-lookup"><span data-stu-id="57d6b-110">Gets the native interface pointer for this exception debug event.</span></span>|  
|[<span data-ttu-id="57d6b-111">GetStackPointer, méthode</span><span class="sxs-lookup"><span data-stu-id="57d6b-111">GetStackPointer Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-getstackpointer-method.md)|<span data-ttu-id="57d6b-112">Obtient le pointeur de pile de cet événement de débogage d'exception.</span><span class="sxs-lookup"><span data-stu-id="57d6b-112">Gets the stack pointer for this exception debug event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="57d6b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="57d6b-113">Remarks</span></span>  
 <span data-ttu-id="57d6b-114">L'interface `ICorDebugExceptionDebugEvent` est implémentée par les types d'événements suivants :</span><span class="sxs-lookup"><span data-stu-id="57d6b-114">The `ICorDebugExceptionDebugEvent` interface is implemented by the following event types:</span></span>  
  
-   [<span data-ttu-id="57d6b-115">MANAGED_EXCEPTION_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="57d6b-115">MANAGED_EXCEPTION_FIRST_CHANCE</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
-   [<span data-ttu-id="57d6b-116">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="57d6b-116">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
-   [<span data-ttu-id="57d6b-117">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span><span class="sxs-lookup"><span data-stu-id="57d6b-117">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
-   [<span data-ttu-id="57d6b-118">MANAGED_EXCEPTION_UNHANDLED</span><span class="sxs-lookup"><span data-stu-id="57d6b-118">MANAGED_EXCEPTION_UNHANDLED</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
> [!NOTE]
>  <span data-ttu-id="57d6b-119">L'interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="57d6b-119">The interface is available with .NET Native only.</span></span> <span data-ttu-id="57d6b-120">Une tentative d'appel à `QueryInterface` pour récupérer un pointeur d'interface retourne `E_NOINTERFACE` pour les scénarios ICorDebug en dehors de .NET Native.</span><span class="sxs-lookup"><span data-stu-id="57d6b-120">Attempting to call `QueryInterface` to retrieve an interface pointer returns `E_NOINTERFACE` for ICorDebug scenarios outside of .NET Native.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57d6b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57d6b-121">Requirements</span></span>  
 <span data-ttu-id="57d6b-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="57d6b-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="57d6b-123">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="57d6b-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="57d6b-124">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="57d6b-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="57d6b-125">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="57d6b-125">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57d6b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57d6b-126">See also</span></span>

- [<span data-ttu-id="57d6b-127">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="57d6b-127">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="57d6b-128">Débogage</span><span class="sxs-lookup"><span data-stu-id="57d6b-128">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
