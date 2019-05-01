---
title: ICorDebugManagedCallback::ExitProcess, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.ExitProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::ExitProcess
helpviewer_keywords:
- ExitProcess method, ICorDebugManagedCallback interface [.NET Framework debugging]
- ICorDebugManagedCallback::ExitProcess method [.NET Framework debugging]
ms.assetid: 63a7d47a-0d54-4e29-9767-9f09feaa38b7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 51162bfb6f9763d2ab4ac1f86e0ccdc15b601271
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61995226"
---
# <a name="icordebugmanagedcallbackexitprocess-method"></a><span data-ttu-id="40e4a-102">ICorDebugManagedCallback::ExitProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="40e4a-102">ICorDebugManagedCallback::ExitProcess Method</span></span>
<span data-ttu-id="40e4a-103">Notifie le débogueur qu’un processus s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="40e4a-103">Notifies the debugger that a process has exited.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="40e4a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40e4a-104">Syntax</span></span>  
  
```  
HRESULT ExitProcess (  
    [in] ICorDebugProcess *pProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="40e4a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40e4a-105">Parameters</span></span>  
 `pProcess`  
 <span data-ttu-id="40e4a-106">[in] Pointeur vers un objet ICorDebugProcess qui représente le processus.</span><span class="sxs-lookup"><span data-stu-id="40e4a-106">[in] A pointer to an ICorDebugProcess object that represents the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="40e4a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="40e4a-107">Remarks</span></span>  
 <span data-ttu-id="40e4a-108">Vous ne pouvez pas continuer à partir d’un `ExitProcess` événement.</span><span class="sxs-lookup"><span data-stu-id="40e4a-108">You cannot continue from an `ExitProcess` event.</span></span> <span data-ttu-id="40e4a-109">Cet événement peut se déclencher en mode asynchrone et d’autres événements alors que le processus semble être arrêté.</span><span class="sxs-lookup"><span data-stu-id="40e4a-109">This event may fire asynchronously to other events while the process appears to be stopped.</span></span> <span data-ttu-id="40e4a-110">Cela peut se produire si le processus se termine lorsque l’état arrêté, généralement en raison d’une force externe.</span><span class="sxs-lookup"><span data-stu-id="40e4a-110">This can occur if the process terminates while stopped, usually due to some external force.</span></span>  
  
 <span data-ttu-id="40e4a-111">Si le common language runtime (CLR) distribue déjà un rappel managé, cet événement sera différé jusqu'à une fois ce rappel a retourné.</span><span class="sxs-lookup"><span data-stu-id="40e4a-111">If the common language runtime (CLR) is already dispatching a managed callback, this event will be delayed until after that callback has returned.</span></span>  
  
 <span data-ttu-id="40e4a-112">Le `ExitProcess` événement est le seul événement de sortie/déchargement appel lors de l’arrêt est garanti.</span><span class="sxs-lookup"><span data-stu-id="40e4a-112">The `ExitProcess` event is the only exit/unload event that is guaranteed to get called on shutdown.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="40e4a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40e4a-113">Requirements</span></span>  
 <span data-ttu-id="40e4a-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="40e4a-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="40e4a-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="40e4a-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="40e4a-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="40e4a-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="40e4a-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="40e4a-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="40e4a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40e4a-118">See also</span></span>

- [<span data-ttu-id="40e4a-119">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="40e4a-119">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
