---
title: ICorDebugManagedCallback::CreateThread, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.CreateThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::CreateThread method
helpviewer_keywords:
- ICorDebugManagedCallback::CreateThread method [.NET Framework debugging]
- CreateThread method [.NET Framework debugging]
ms.assetid: 6b961728-21c4-4e8d-ae81-197458be62f4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9721d88c8ce138b19c98f113d9eb034c5e1c55dd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33417688"
---
# <a name="icordebugmanagedcallbackcreatethread-method"></a><span data-ttu-id="f0413-102">ICorDebugManagedCallback::CreateThread, méthode</span><span class="sxs-lookup"><span data-stu-id="f0413-102">ICorDebugManagedCallback::CreateThread Method</span></span>
<span data-ttu-id="f0413-103">Notifie le débogueur qu’un thread a démarré l’exécution du code managé.</span><span class="sxs-lookup"><span data-stu-id="f0413-103">Notifies the debugger that a thread has started executing managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0413-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0413-104">Syntax</span></span>  
  
```  
HRESULT CreateThread (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *thread  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f0413-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0413-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="f0413-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application qui contient le thread.</span><span class="sxs-lookup"><span data-stu-id="f0413-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contains the thread.</span></span>  
  
 `thread`  
 <span data-ttu-id="f0413-107">[in] Pointeur vers un objet ICorDebugThread qui représente le thread.</span><span class="sxs-lookup"><span data-stu-id="f0413-107">[in] A pointer to an ICorDebugThread object that represents the thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f0413-108">Notes</span><span class="sxs-lookup"><span data-stu-id="f0413-108">Remarks</span></span>  
 <span data-ttu-id="f0413-109">Le thread sera positionné à la première instruction de code managé à exécuter.</span><span class="sxs-lookup"><span data-stu-id="f0413-109">The thread will be positioned at the first managed code instruction to be executed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f0413-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f0413-110">Requirements</span></span>  
 <span data-ttu-id="f0413-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f0413-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f0413-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f0413-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f0413-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f0413-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f0413-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0413-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0413-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0413-115">See Also</span></span>  
 [<span data-ttu-id="f0413-116">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="f0413-116">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
