---
title: ICorDebugManagedCallback::Break, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.Break
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::Break
helpviewer_keywords:
- Break method [.NET Framework debugging]
- ICorDebugManagedCallback::Break method [.NET Framework debugging]
ms.assetid: 7d78a301-82b3-43b2-9d65-3cda3285ae97
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 83524b24fd05969fa4f45fd742d1df955c441d44
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54732386"
---
# <a name="icordebugmanagedcallbackbreak-method"></a><span data-ttu-id="2e4f6-102">ICorDebugManagedCallback::Break, méthode</span><span class="sxs-lookup"><span data-stu-id="2e4f6-102">ICorDebugManagedCallback::Break Method</span></span>
<span data-ttu-id="2e4f6-103">Notifie le débogueur lorsqu’une <xref:System.Reflection.Emit.OpCodes.Break> instruction dans le flux de code est exécutée.</span><span class="sxs-lookup"><span data-stu-id="2e4f6-103">Notifies the debugger when a <xref:System.Reflection.Emit.OpCodes.Break> instruction in the code stream is executed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2e4f6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e4f6-104">Syntax</span></span>  
  
```  
HRESULT Break (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *thread  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2e4f6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e4f6-105">Parameters</span></span>  
 `pAppDOmain`  
 <span data-ttu-id="2e4f6-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application qui contient l’instruction de saut.</span><span class="sxs-lookup"><span data-stu-id="2e4f6-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contains the break instruction.</span></span>  
  
 `thread`  
 <span data-ttu-id="2e4f6-107">[in] Pointeur vers un objet ICorDebugThread qui représente le thread qui contient l’instruction de saut.</span><span class="sxs-lookup"><span data-stu-id="2e4f6-107">[in] A pointer to an ICorDebugThread object that represents the thread that contains the break instruction.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2e4f6-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2e4f6-108">Requirements</span></span>  
 <span data-ttu-id="2e4f6-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2e4f6-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2e4f6-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2e4f6-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2e4f6-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2e4f6-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2e4f6-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2e4f6-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2e4f6-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e4f6-113">See also</span></span>
- [<span data-ttu-id="2e4f6-114">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="2e4f6-114">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
