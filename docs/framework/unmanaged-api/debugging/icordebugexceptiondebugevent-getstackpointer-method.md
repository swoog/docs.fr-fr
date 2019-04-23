---
title: ICorDebugExceptionDebugEvent::GetStackPointer, méthode
ms.date: 03/30/2017
ms.assetid: d8f66a1c-16be-4264-afc5-bc2dfbb4a682
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d9d4c0a1938edd3e2fe88ea6e418b3430f1b5cb8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59163200"
---
# <a name="icordebugexceptiondebugeventgetstackpointer-method"></a><span data-ttu-id="ba49e-102">ICorDebugExceptionDebugEvent::GetStackPointer, méthode</span><span class="sxs-lookup"><span data-stu-id="ba49e-102">ICorDebugExceptionDebugEvent::GetStackPointer Method</span></span>
<span data-ttu-id="ba49e-103">Obtient le pointeur de pile de cet événement de débogage d'exception.</span><span class="sxs-lookup"><span data-stu-id="ba49e-103">Gets the stack pointer for this exception debug event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ba49e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba49e-104">Syntax</span></span>  
  
```  
HRESULT GetStackPointer(  
   [out]CORDB_ADDRESS *pStackPointer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ba49e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba49e-105">Parameters</span></span>  
 `pStackPointer`  
 <span data-ttu-id="ba49e-106">[out] Pointeur vers l'adresse du pointeur de pile de cet événement de débogage d'exception.</span><span class="sxs-lookup"><span data-stu-id="ba49e-106">[out] A pointer to the address of the stack pointer for this exception debug event.</span></span> <span data-ttu-id="ba49e-107">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="ba49e-107">See the Remarks section for more information.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ba49e-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ba49e-108">Remarks</span></span>  
 <span data-ttu-id="ba49e-109">La signification de ce pointeur de pile varie selon le type d'événement, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ba49e-109">The meaning of this stack pointer depends on the event type, as shown in the following table.</span></span>  
  
|<span data-ttu-id="ba49e-110">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="ba49e-110">Event type</span></span>|<span data-ttu-id="ba49e-111">Signification de la valeur `pStackPointer`</span><span class="sxs-lookup"><span data-stu-id="ba49e-111">Meaning of `pStackPointer` value</span></span>|  
|----------------|--------------------------------------|  
|[<span data-ttu-id="ba49e-112">MANAGED_EXCEPTION_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="ba49e-112">MANAGED_EXCEPTION_FIRST_CHANCE</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)|<span data-ttu-id="ba49e-113">Pointeur de pile du frame ayant levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="ba49e-113">The stack pointer for the frame that threw the exception.</span></span>|  
|[<span data-ttu-id="ba49e-114">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="ba49e-114">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)|<span data-ttu-id="ba49e-115">Pointeur de pile du frame de code utilisateur le plus proche du point de l'exception levée.</span><span class="sxs-lookup"><span data-stu-id="ba49e-115">The stack pointer for the user-code frame closest to the point of the thrown exception.</span></span>|  
|[<span data-ttu-id="ba49e-116">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span><span class="sxs-lookup"><span data-stu-id="ba49e-116">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)|<span data-ttu-id="ba49e-117">Pointeur de pile du frame contenant le gestionnaire catch.</span><span class="sxs-lookup"><span data-stu-id="ba49e-117">The stack pointer for the frame that contains the catch handler.</span></span>|  
|[<span data-ttu-id="ba49e-118">MANAGED_EXCEPTION_UNHANDLED</span><span class="sxs-lookup"><span data-stu-id="ba49e-118">MANAGED_EXCEPTION_UNHANDLED</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)|<span data-ttu-id="ba49e-119">`pStackPointer` a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="ba49e-119">`pStackPointer` is **null**.</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="ba49e-120">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="ba49e-120">This method is available with .NET Native only.</span></span>  
  
 <span data-ttu-id="ba49e-121">Le type d’événement est disponible à partir de la [ICorDebugDebugEvent::GetEventKind](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-geteventkind-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="ba49e-121">The event type is available from the [ICorDebugDebugEvent::GetEventKind](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-geteventkind-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ba49e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba49e-122">Requirements</span></span>  
 <span data-ttu-id="ba49e-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ba49e-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ba49e-124">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ba49e-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ba49e-125">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ba49e-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ba49e-126">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ba49e-126">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ba49e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba49e-127">See also</span></span>

- [<span data-ttu-id="ba49e-128">ICorDebugExceptionDebugEvent, interface</span><span class="sxs-lookup"><span data-stu-id="ba49e-128">ICorDebugExceptionDebugEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-interface.md)
- [<span data-ttu-id="ba49e-129">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="ba49e-129">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
