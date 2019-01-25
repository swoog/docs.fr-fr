---
title: CLR_DEBUGGING_PROCESS_FLAGS, énumération
ms.date: 03/30/2017
api_name:
- CLR_DEBUGGING_PROCESS_FLAGS
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CLR_DEBUGGING_PROCESS_FLAG
helpviewer_keywords:
- CLR_DEBUGGING_PROCESS_FLAGS enumeration [.NET Framework debugging]
ms.assetid: 85b85fde-1f87-490b-ba8d-d604670959c3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 609bb050bb9c5addb5250f65a059a70d3ce32428
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54662242"
---
# <a name="clrdebuggingprocessflags-enumeration"></a><span data-ttu-id="f6d7b-102">CLR_DEBUGGING_PROCESS_FLAGS, énumération</span><span class="sxs-lookup"><span data-stu-id="f6d7b-102">CLR_DEBUGGING_PROCESS_FLAGS Enumeration</span></span>
<span data-ttu-id="f6d7b-103">Fournit des valeurs qui sont utilisées par le [ICLRDebugging::OpenVirtualProcess](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-openvirtualprocess-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="f6d7b-103">Provides values that are used by the [ICLRDebugging::OpenVirtualProcess](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-openvirtualprocess-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6d7b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6d7b-104">Syntax</span></span>  
  
```  
typedef enum CLR_DEBUGGING_PROCESS_FLAGS  
{  
   CLR_DEBUGGING_MANAGED_EVENT_PENDING = 1,  
   CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH = 2  
}  CLR_DEBUGGING_PROCESS_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="f6d7b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="f6d7b-105">Members</span></span>  
  
|<span data-ttu-id="f6d7b-106">Membre</span><span class="sxs-lookup"><span data-stu-id="f6d7b-106">Member</span></span>|<span data-ttu-id="f6d7b-107">Description</span><span class="sxs-lookup"><span data-stu-id="f6d7b-107">Description</span></span>|  
|------------|-----------------|  
|`CLR_DEBUGGING_MANAGED_EVENT_PENDING`|<span data-ttu-id="f6d7b-108">Ce runtime possède un événement de débogueur managé non-catch-up à envoyer.</span><span class="sxs-lookup"><span data-stu-id="f6d7b-108">This runtime has a non-catch-up managed debugger event to send.</span></span> <span data-ttu-id="f6d7b-109">Consultez la section Notes pour la distinction entre les événements de mise à jour et non-catch-up.</span><span class="sxs-lookup"><span data-stu-id="f6d7b-109">See the Remarks section for the distinction between catch-up and non-catch-up events.</span></span>|  
|`CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH`|<span data-ttu-id="f6d7b-110">L’événement géré qui est en attente est un <xref:System.Diagnostics.Debugger.Launch%2A?displayProperty=nameWithType> demande.</span><span class="sxs-lookup"><span data-stu-id="f6d7b-110">The managed event that is pending is a <xref:System.Diagnostics.Debugger.Launch%2A?displayProperty=nameWithType> request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f6d7b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f6d7b-111">Remarks</span></span>  
 <span data-ttu-id="f6d7b-112">Les événements de mise à jour incluent des processus, ce domaine d’application, assembly, module et les notifications de la création du thread qui donnent le débogueur jusqu'à l’état actuel une fois qu’il a attaché à un processus.</span><span class="sxs-lookup"><span data-stu-id="f6d7b-112">Catch-up events include process, application domain, assembly, module, and thread creation notifications that bring the debugger up to the current state after it has attached to a process.</span></span> <span data-ttu-id="f6d7b-113">Les événements de non-catch-up, qui sont indiquées par le `CLR_DEBUGGING_MANAGED_EVENT_PENDING` indicateur, incluez tous les autres événements de débogueur, telles que les exceptions, puis gérés débogage notifications de l’assistant (MDA).</span><span class="sxs-lookup"><span data-stu-id="f6d7b-113">Non-catch-up events, which are indicated by the `CLR_DEBUGGING_MANAGED_EVENT_PENDING` flag, include all other debugger events, such as exceptions and managed debugging assistant (MDA) notifications.</span></span>  
  
 <span data-ttu-id="f6d7b-114">Le `CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH` indicateur permet au runtime de faire la distinction entre une exception de fin et une demande pour attacher un débogueur managé qui peut être annulé.</span><span class="sxs-lookup"><span data-stu-id="f6d7b-114">The `CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH` flag enables the runtime to differentiate between a terminating exception and a request to attach a managed debugger that can be canceled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f6d7b-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f6d7b-115">Requirements</span></span>  
 <span data-ttu-id="f6d7b-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f6d7b-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f6d7b-117">**En-tête :** Metahost.idl, Metahost.h</span><span class="sxs-lookup"><span data-stu-id="f6d7b-117">**Header:** Metahost.idl, Metahost.h</span></span>  
  
 <span data-ttu-id="f6d7b-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f6d7b-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f6d7b-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f6d7b-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6d7b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6d7b-120">See also</span></span>
- [<span data-ttu-id="f6d7b-121">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="f6d7b-121">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
- [<span data-ttu-id="f6d7b-122">Débogage</span><span class="sxs-lookup"><span data-stu-id="f6d7b-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
