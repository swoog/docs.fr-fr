---
title: CorDebugThreadState, énumération
ms.date: 03/30/2017
api_name:
- CorDebugThreadState
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugThreadState
helpviewer_keywords:
- CorDebugThreadState enumeration [.NET Framework debugging]
ms.assetid: a3ccdf18-4ec6-494d-9024-48e5c8c724f5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2296f6e386f35aed91a8aea4392a9cd00ec27ccb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54724357"
---
# <a name="cordebugthreadstate-enumeration"></a><span data-ttu-id="4be9c-102">CorDebugThreadState, énumération</span><span class="sxs-lookup"><span data-stu-id="4be9c-102">CorDebugThreadState Enumeration</span></span>
<span data-ttu-id="4be9c-103">Spécifie l'état d'un thread pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="4be9c-103">Specifies the state of a thread for debugging.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4be9c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4be9c-104">Syntax</span></span>  
  
```  
typedef enum CorDebugThreadState {  
    THREAD_RUN,  
    THREAD_SUSPEND  
} CorDebugThreadState;  
```  
  
## <a name="members"></a><span data-ttu-id="4be9c-105">Membres</span><span class="sxs-lookup"><span data-stu-id="4be9c-105">Members</span></span>  
  
|<span data-ttu-id="4be9c-106">Membre</span><span class="sxs-lookup"><span data-stu-id="4be9c-106">Member</span></span>|<span data-ttu-id="4be9c-107">Description</span><span class="sxs-lookup"><span data-stu-id="4be9c-107">Description</span></span>|  
|------------|-----------------|  
|`THREAD_RUN`|<span data-ttu-id="4be9c-108">Le thread exécute librement, sauf si un événement de débogage se produit.</span><span class="sxs-lookup"><span data-stu-id="4be9c-108">The thread runs freely, unless a debug event occurs.</span></span>|  
|`THREAD_SUSPEND`|<span data-ttu-id="4be9c-109">Le thread ne peut pas s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="4be9c-109">The thread cannot run.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4be9c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4be9c-110">Remarks</span></span>  
 <span data-ttu-id="4be9c-111">Le débogueur utilise la `CorDebugThreadState` énumération pour contrôler l’exécution d’un thread.</span><span class="sxs-lookup"><span data-stu-id="4be9c-111">The debugger uses the `CorDebugThreadState` enumeration to control a thread's execution.</span></span> <span data-ttu-id="4be9c-112">L’état d’un thread peut être défini à l’aide de la [ICorDebugThread::SetDebugState](../../../../docs/framework/unmanaged-api/debugging/icordebugthread-setdebugstate-method.md) ou [ICorDebugController::SetAllThreadsDebugState](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-setallthreadsdebugstate-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="4be9c-112">The state of a thread can be set by using the [ICorDebugThread::SetDebugState](../../../../docs/framework/unmanaged-api/debugging/icordebugthread-setdebugstate-method.md) or [ICorDebugController::SetAllThreadsDebugState](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-setallthreadsdebugstate-method.md) method.</span></span>  
  
 <span data-ttu-id="4be9c-113">Un rappel fourni à la [API d’hébergement](../../../../docs/framework/unmanaged-api/hosting/index.md) permet le pompage de messages, un état interrompu est donc pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4be9c-113">A callback provided to the [hosting API](../../../../docs/framework/unmanaged-api/hosting/index.md) enables message pumping, so an interrupted state is not needed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4be9c-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4be9c-114">Requirements</span></span>  
 <span data-ttu-id="4be9c-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4be9c-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4be9c-116">**En-tête :** CorDebug.idl, CorDegug.h</span><span class="sxs-lookup"><span data-stu-id="4be9c-116">**Header:** CorDebug.idl, CorDegug.h</span></span>  
  
 <span data-ttu-id="4be9c-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4be9c-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4be9c-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4be9c-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4be9c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4be9c-119">See also</span></span>
- [<span data-ttu-id="4be9c-120">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="4be9c-120">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
