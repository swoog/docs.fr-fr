---
title: ICorDebugProcess, interface
ms.date: 03/30/2017
api_name:
- ICorDebugProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess
helpviewer_keywords:
- ICorDebugProcess interface [.NET Framework debugging]
ms.assetid: be86f4b5-418a-4c5c-a67c-97148c65ed8c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 46d96d66f16cd956d8fab1afe00486d564e37953
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59216793"
---
# <a name="icordebugprocess-interface"></a><span data-ttu-id="2d759-102">ICorDebugProcess, interface</span><span class="sxs-lookup"><span data-stu-id="2d759-102">ICorDebugProcess Interface</span></span>
<span data-ttu-id="2d759-103">Représente un processus qui exécute le code managé.</span><span class="sxs-lookup"><span data-stu-id="2d759-103">Represents a process that is executing managed code.</span></span> <span data-ttu-id="2d759-104">Cette interface est une sous-classe de ICorDebugController.</span><span class="sxs-lookup"><span data-stu-id="2d759-104">This interface is a subclass of ICorDebugController.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="2d759-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2d759-105">Methods</span></span>  
  
|<span data-ttu-id="2d759-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-106">Method</span></span>|<span data-ttu-id="2d759-107">Description</span><span class="sxs-lookup"><span data-stu-id="2d759-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="2d759-108">ClearCurrentException, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-108">ClearCurrentException Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-clearcurrentexception-method.md)|<span data-ttu-id="2d759-109">Efface l’exception non managée actuelle sur le thread donné.</span><span class="sxs-lookup"><span data-stu-id="2d759-109">Clears the current unmanaged exception on the given thread.</span></span>|  
|[<span data-ttu-id="2d759-110">EnableLogMessages, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-110">EnableLogMessages Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-enablelogmessages-method.md)|<span data-ttu-id="2d759-111">Active et désactive l’envoi de messages de journal au débogueur.</span><span class="sxs-lookup"><span data-stu-id="2d759-111">Enables and disables the sending of log messages to the debugger.</span></span>|  
|[<span data-ttu-id="2d759-112">EnumerateAppDomains, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-112">EnumerateAppDomains Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-enumerateappdomains-method.md)|<span data-ttu-id="2d759-113">Énumère tous les domaines d’application dans le processus.</span><span class="sxs-lookup"><span data-stu-id="2d759-113">Enumerates all of the application domains in the process.</span></span>|  
|[<span data-ttu-id="2d759-114">EnumerateObjects, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-114">EnumerateObjects Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-enumerateobjects-method.md)|<span data-ttu-id="2d759-115">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="2d759-115">Not implemented.</span></span>|  
|[<span data-ttu-id="2d759-116">GetHandle, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-116">GetHandle Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-gethandle-method.md)|<span data-ttu-id="2d759-117">Obtient un handle vers le processus.</span><span class="sxs-lookup"><span data-stu-id="2d759-117">Gets a handle to the process.</span></span>|  
|[<span data-ttu-id="2d759-118">GetHelperThreadID, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-118">GetHelperThreadID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-gethelperthreadid-method.md)|<span data-ttu-id="2d759-119">Obtient l’ID de thread de système d’exploitation (OS) pour le thread d’assistance interne du débogueur.</span><span class="sxs-lookup"><span data-stu-id="2d759-119">Gets the operating system (OS) thread ID for the debugger's internal helper thread.</span></span>|  
|[<span data-ttu-id="2d759-120">GetID, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-120">GetID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-getid-method.md)|<span data-ttu-id="2d759-121">Obtient l’ID de système d’exploitation (se) du processus.</span><span class="sxs-lookup"><span data-stu-id="2d759-121">Gets the operating system (OS) ID of the process.</span></span>|  
|[<span data-ttu-id="2d759-122">GetObject, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-122">GetObject Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-getobject-method.md)|<span data-ttu-id="2d759-123">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="2d759-123">Not implemented.</span></span>|  
|[<span data-ttu-id="2d759-124">GetThread, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-124">GetThread Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-getthread-method.md)|<span data-ttu-id="2d759-125">Obtient l’instance ICorDebugThread qui a le thread de système d’exploitation spécifié ID.</span><span class="sxs-lookup"><span data-stu-id="2d759-125">Gets the ICorDebugThread instance that has the specified OS thread ID.</span></span>|  
|[<span data-ttu-id="2d759-126">GetThreadContext, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-126">GetThreadContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-getthreadcontext-method.md)|<span data-ttu-id="2d759-127">Obtient le contexte pour le thread donné.</span><span class="sxs-lookup"><span data-stu-id="2d759-127">Gets the context for the given thread.</span></span>|  
|[<span data-ttu-id="2d759-128">IsOSSuspended, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-128">IsOSSuspended Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-isossuspended-method.md)|<span data-ttu-id="2d759-129">Détermine si le thread a été interrompu à la suite du débogueur qui arrête le processus.</span><span class="sxs-lookup"><span data-stu-id="2d759-129">Determines whether the thread has been suspended as a result of the debugger stopping the process.</span></span>|  
|[<span data-ttu-id="2d759-130">IsTransitionStub, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-130">IsTransitionStub Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-istransitionstub-method.md)|<span data-ttu-id="2d759-131">Détermine si une adresse est à l’intérieur d’un stub qui provoquera une transition vers du code managé.</span><span class="sxs-lookup"><span data-stu-id="2d759-131">Determines whether an address is inside a stub that will cause a transition to managed code.</span></span>|  
|[<span data-ttu-id="2d759-132">ModifyLogSwitch, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-132">ModifyLogSwitch Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-modifylogswitch-method.md)|<span data-ttu-id="2d759-133">Définit le niveau de gravité du commutateur de journal spécifié.</span><span class="sxs-lookup"><span data-stu-id="2d759-133">Sets the severity level of the specified log switch.</span></span>|  
|[<span data-ttu-id="2d759-134">ReadMemory, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-134">ReadMemory Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-readmemory-method.md)|<span data-ttu-id="2d759-135">Lit la mémoire du processus.</span><span class="sxs-lookup"><span data-stu-id="2d759-135">Reads memory from the process.</span></span>|  
|[<span data-ttu-id="2d759-136">SetThreadContext, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-136">SetThreadContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-setthreadcontext-method.md)|<span data-ttu-id="2d759-137">Définit le contexte pour le thread donné.</span><span class="sxs-lookup"><span data-stu-id="2d759-137">Sets the context for the given thread.</span></span>|  
|[<span data-ttu-id="2d759-138">ThreadForFiberCookie, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-138">ThreadForFiberCookie Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-threadforfibercookie-method.md)|<span data-ttu-id="2d759-139">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="2d759-139">Deprecated.</span></span>|  
|[<span data-ttu-id="2d759-140">WriteMemory, méthode</span><span class="sxs-lookup"><span data-stu-id="2d759-140">WriteMemory Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-writememory-method.md)|<span data-ttu-id="2d759-141">Écrit des données dans une zone de mémoire dans le processus.</span><span class="sxs-lookup"><span data-stu-id="2d759-141">Writes data to an area of memory in the process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2d759-142">Notes</span><span class="sxs-lookup"><span data-stu-id="2d759-142">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2d759-143">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="2d759-143">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2d759-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d759-144">Requirements</span></span>  
 <span data-ttu-id="2d759-145">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2d759-145">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2d759-146">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2d759-146">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2d759-147">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2d759-147">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2d759-148">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2d759-148">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d759-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d759-149">See also</span></span>

- [<span data-ttu-id="2d759-150">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="2d759-150">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
- [<span data-ttu-id="2d759-151">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="2d759-151">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
