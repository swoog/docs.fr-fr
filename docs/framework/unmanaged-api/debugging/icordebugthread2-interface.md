---
title: ICorDebugThread2 Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugThread2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread2
helpviewer_keywords:
- ICorDebugThread2 interface [.NET Framework debugging]
ms.assetid: 678f89f9-cce7-46d1-af87-5e989abaa93c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c348cf28a6330523d1a490c136a3214e37d13f4c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33423047"
---
# <a name="icordebugthread2-interface1"></a><span data-ttu-id="47b44-102">ICorDebugThread2 Interface1</span><span class="sxs-lookup"><span data-stu-id="47b44-102">ICorDebugThread2 Interface1</span></span>
<span data-ttu-id="47b44-103">Sert d’extension logique à l’interface ICorDebugThread.</span><span class="sxs-lookup"><span data-stu-id="47b44-103">Serves as a logical extension to the ICorDebugThread interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="47b44-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="47b44-104">Methods</span></span>  
  
|<span data-ttu-id="47b44-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="47b44-105">Method</span></span>|<span data-ttu-id="47b44-106">Description</span><span class="sxs-lookup"><span data-stu-id="47b44-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="47b44-107">GetActiveFunctions, méthode</span><span class="sxs-lookup"><span data-stu-id="47b44-107">GetActiveFunctions Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-getactivefunctions-method.md)|<span data-ttu-id="47b44-108">Obtient un tableau d’instances COR_ACTIVE_FUNCTION qui contiennent des données sur les fonctions actives dans les frames d’un thread.</span><span class="sxs-lookup"><span data-stu-id="47b44-108">Gets an array of COR_ACTIVE_FUNCTION instances that contain data about the active functions in a thread's frames.</span></span>|  
|[<span data-ttu-id="47b44-109">GetConnectionID, méthode</span><span class="sxs-lookup"><span data-stu-id="47b44-109">GetConnectionID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-getconnectionid-method.md)|<span data-ttu-id="47b44-110">Obtient un identificateur de connexion pour ce `ICorDebugThread2`.</span><span class="sxs-lookup"><span data-stu-id="47b44-110">Gets a connection identifier for this `ICorDebugThread2`.</span></span>|  
|[<span data-ttu-id="47b44-111">GetTaskID, méthode</span><span class="sxs-lookup"><span data-stu-id="47b44-111">GetTaskID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-gettaskid-method.md)|<span data-ttu-id="47b44-112">Obtient un identificateur de tâche pour ce `ICorDebugThread2`.</span><span class="sxs-lookup"><span data-stu-id="47b44-112">Gets a task identifier for this `ICorDebugThread2`.</span></span>|  
|[<span data-ttu-id="47b44-113">GetVolatileOSThreadID, méthode</span><span class="sxs-lookup"><span data-stu-id="47b44-113">GetVolatileOSThreadID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-getvolatileosthreadid-method.md)|<span data-ttu-id="47b44-114">Obtient l’identificateur du thread du système d’exploitation de cet `ICorDebugThread2`.</span><span class="sxs-lookup"><span data-stu-id="47b44-114">Gets the operating system thread identifier for this `ICorDebugThread2`.</span></span>|  
|[<span data-ttu-id="47b44-115">InterceptCurrentException, méthode</span><span class="sxs-lookup"><span data-stu-id="47b44-115">InterceptCurrentException Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-interceptcurrentexception-method.md)|<span data-ttu-id="47b44-116">Permet à un débogueur d’intercepter l’exception en cours sur un thread.</span><span class="sxs-lookup"><span data-stu-id="47b44-116">Allows a debugger to intercept the current exception on a thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="47b44-117">Notes</span><span class="sxs-lookup"><span data-stu-id="47b44-117">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="47b44-118">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="47b44-118">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="47b44-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="47b44-119">Requirements</span></span>  
 <span data-ttu-id="47b44-120">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="47b44-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="47b44-121">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="47b44-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="47b44-122">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="47b44-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="47b44-123">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="47b44-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="47b44-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47b44-124">See Also</span></span>  
 [<span data-ttu-id="47b44-125">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="47b44-125">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
