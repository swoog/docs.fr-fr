---
title: ICorDebugExceptionDebugEvent::GetStackPointer, méthode
ms.date: 03/30/2017
ms.assetid: d8f66a1c-16be-4264-afc5-bc2dfbb4a682
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 89802de31ed6db4ef6532a2b4a90a82c4e9a5c72
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54590849"
---
# <a name="icordebugexceptiondebugeventgetstackpointer-method"></a><span data-ttu-id="0a46e-102">ICorDebugExceptionDebugEvent::GetStackPointer, méthode</span><span class="sxs-lookup"><span data-stu-id="0a46e-102">ICorDebugExceptionDebugEvent::GetStackPointer Method</span></span>
<span data-ttu-id="0a46e-103">Obtient le pointeur de pile de cet événement de débogage d'exception.</span><span class="sxs-lookup"><span data-stu-id="0a46e-103">Gets the stack pointer for this exception debug event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a46e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a46e-104">Syntax</span></span>  
  
```  
HRESULT GetStackPointer(  
   [out]CORDB_ADDRESS *pStackPointer  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0a46e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a46e-105">Parameters</span></span>  
 `pStackPointer`  
 <span data-ttu-id="0a46e-106">[out] Pointeur vers l'adresse du pointeur de pile de cet événement de débogage d'exception.</span><span class="sxs-lookup"><span data-stu-id="0a46e-106">[out] A pointer to the address of the stack pointer for this exception debug event.</span></span> <span data-ttu-id="0a46e-107">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="0a46e-107">See the Remarks section for more information.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0a46e-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0a46e-108">Remarks</span></span>  
 <span data-ttu-id="0a46e-109">La signification de ce pointeur de pile varie selon le type d'événement, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0a46e-109">The meaning of this stack pointer depends on the event type, as shown in the following table.</span></span>  
  
|<span data-ttu-id="0a46e-110">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="0a46e-110">Event type</span></span>|<span data-ttu-id="0a46e-111">Signification de la valeur `pStackPointer`</span><span class="sxs-lookup"><span data-stu-id="0a46e-111">Meaning of `pStackPointer` value</span></span>|  
|----------------|--------------------------------------|  
|[<span data-ttu-id="0a46e-112">MANAGED_EXCEPTION_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="0a46e-112">MANAGED_EXCEPTION_FIRST_CHANCE</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)|<span data-ttu-id="0a46e-113">Pointeur de pile du frame ayant levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="0a46e-113">The stack pointer for the frame that threw the exception.</span></span>|  
|[<span data-ttu-id="0a46e-114">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="0a46e-114">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)|<span data-ttu-id="0a46e-115">Pointeur de pile du frame de code utilisateur le plus proche du point de l'exception levée.</span><span class="sxs-lookup"><span data-stu-id="0a46e-115">The stack pointer for the user-code frame closest to the point of the thrown exception.</span></span>|  
|[<span data-ttu-id="0a46e-116">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span><span class="sxs-lookup"><span data-stu-id="0a46e-116">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)|<span data-ttu-id="0a46e-117">Pointeur de pile du frame contenant le gestionnaire catch.</span><span class="sxs-lookup"><span data-stu-id="0a46e-117">The stack pointer for the frame that contains the catch handler.</span></span>|  
|[<span data-ttu-id="0a46e-118">MANAGED_EXCEPTION_UNHANDLED</span><span class="sxs-lookup"><span data-stu-id="0a46e-118">MANAGED_EXCEPTION_UNHANDLED</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)|<span data-ttu-id="0a46e-119">`pStackPointer` a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="0a46e-119">`pStackPointer` is **null**.</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="0a46e-120">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="0a46e-120">This method is available with .NET Native only.</span></span>  
  
 <span data-ttu-id="0a46e-121">Le type d’événement est disponible à partir de la [ICorDebugDebugEvent::GetEventKind](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-geteventkind-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="0a46e-121">The event type is available from the [ICorDebugDebugEvent::GetEventKind](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-geteventkind-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0a46e-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0a46e-122">Requirements</span></span>  
 <span data-ttu-id="0a46e-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0a46e-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0a46e-124">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0a46e-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0a46e-125">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0a46e-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0a46e-126">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0a46e-126">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0a46e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a46e-127">See also</span></span>
- [<span data-ttu-id="0a46e-128">ICorDebugExceptionDebugEvent, interface</span><span class="sxs-lookup"><span data-stu-id="0a46e-128">ICorDebugExceptionDebugEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-interface.md)
- [<span data-ttu-id="0a46e-129">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="0a46e-129">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
