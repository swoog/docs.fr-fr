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
ms.openlocfilehash: dff6b245c80050a5e85561b8bba6aa9ba8199ba8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33407064"
---
# <a name="clrdebuggingprocessflags-enumeration"></a><span data-ttu-id="26041-102">CLR_DEBUGGING_PROCESS_FLAGS, énumération</span><span class="sxs-lookup"><span data-stu-id="26041-102">CLR_DEBUGGING_PROCESS_FLAGS Enumeration</span></span>
<span data-ttu-id="26041-103">Fournit des valeurs qui sont utilisées par le [ICLRDebugging::OpenVirtualProcess](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-openvirtualprocess-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="26041-103">Provides values that are used by the [ICLRDebugging::OpenVirtualProcess](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-openvirtualprocess-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26041-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26041-104">Syntax</span></span>  
  
```  
typedef enum CLR_DEBUGGING_PROCESS_FLAGS  
{  
   CLR_DEBUGGING_MANAGED_EVENT_PENDING = 1,  
   CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH = 2  
}  CLR_DEBUGGING_PROCESS_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="26041-105">Membres</span><span class="sxs-lookup"><span data-stu-id="26041-105">Members</span></span>  
  
|<span data-ttu-id="26041-106">Membre</span><span class="sxs-lookup"><span data-stu-id="26041-106">Member</span></span>|<span data-ttu-id="26041-107">Description</span><span class="sxs-lookup"><span data-stu-id="26041-107">Description</span></span>|  
|------------|-----------------|  
|`CLR_DEBUGGING_MANAGED_EVENT_PENDING`|<span data-ttu-id="26041-108">Cette exécution a un événement du débogueur managé non-catch-up à envoyer.</span><span class="sxs-lookup"><span data-stu-id="26041-108">This runtime has a non-catch-up managed debugger event to send.</span></span> <span data-ttu-id="26041-109">Consultez la section Notes de la distinction entre les événements de rattrapage et non-catch-up.</span><span class="sxs-lookup"><span data-stu-id="26041-109">See the Remarks section for the distinction between catch-up and non-catch-up events.</span></span>|  
|`CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH`|<span data-ttu-id="26041-110">L’événement managé qui est en attente est un <xref:System.Diagnostics.Debugger.Launch%2A?displayProperty=nameWithType> demande.</span><span class="sxs-lookup"><span data-stu-id="26041-110">The managed event that is pending is a <xref:System.Diagnostics.Debugger.Launch%2A?displayProperty=nameWithType> request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="26041-111">Notes</span><span class="sxs-lookup"><span data-stu-id="26041-111">Remarks</span></span>  
 <span data-ttu-id="26041-112">Événements de rattrapage incluent des processus, domaine d’application, assembly, module et les notifications de la création du thread que le débogueur passe à l’état actuel une fois qu’il a joint à un processus.</span><span class="sxs-lookup"><span data-stu-id="26041-112">Catch-up events include process, application domain, assembly, module, and thread creation notifications that bring the debugger up to the current state after it has attached to a process.</span></span> <span data-ttu-id="26041-113">Les événements de non-catch-up, qui sont indiquées par le `CLR_DEBUGGING_MANAGED_EVENT_PENDING` indicateur, inclure tous les autres événements de débogueur, telles que les exceptions et de débogage des notifications de l’assistant (MDA).</span><span class="sxs-lookup"><span data-stu-id="26041-113">Non-catch-up events, which are indicated by the `CLR_DEBUGGING_MANAGED_EVENT_PENDING` flag, include all other debugger events, such as exceptions and managed debugging assistant (MDA) notifications.</span></span>  
  
 <span data-ttu-id="26041-114">Le `CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH` indicateur permet à l’exécution différencier une exception de fin et une demande d’attachement d’un débogueur managé qui peut être annulé.</span><span class="sxs-lookup"><span data-stu-id="26041-114">The `CLR_DEBUGGING_MANAGED_EVENT_DEBUGGER_LAUNCH` flag enables the runtime to differentiate between a terminating exception and a request to attach a managed debugger that can be canceled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="26041-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="26041-115">Requirements</span></span>  
 <span data-ttu-id="26041-116">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="26041-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="26041-117">**En-tête :** Metahost.idl, Metahost.h</span><span class="sxs-lookup"><span data-stu-id="26041-117">**Header:** Metahost.idl, Metahost.h</span></span>  
  
 <span data-ttu-id="26041-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="26041-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="26041-119">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="26041-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26041-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26041-120">See Also</span></span>  
 [<span data-ttu-id="26041-121">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="26041-121">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)  
 [<span data-ttu-id="26041-122">Débogage</span><span class="sxs-lookup"><span data-stu-id="26041-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
