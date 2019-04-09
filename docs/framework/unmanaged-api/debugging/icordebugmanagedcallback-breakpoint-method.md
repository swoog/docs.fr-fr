---
title: ICorDebugManagedCallback::Breakpoint, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.Breakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::Breakpoint
helpviewer_keywords:
- ICorDebugManagedCallback::Breakpoint method [.NET Framework debugging]
- Breakpoint method [.NET Framework debugging]
ms.assetid: 60b279b0-a726-46d2-8c53-76986a007ebb
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8591cb7f8eec3d92100b49db553ed1b5b6533c17
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59131071"
---
# <a name="icordebugmanagedcallbackbreakpoint-method"></a><span data-ttu-id="097dc-102">ICorDebugManagedCallback::Breakpoint, méthode</span><span class="sxs-lookup"><span data-stu-id="097dc-102">ICorDebugManagedCallback::Breakpoint Method</span></span>
<span data-ttu-id="097dc-103">Notifie le débogueur lorsqu’un point d’arrêt est rencontré.</span><span class="sxs-lookup"><span data-stu-id="097dc-103">Notifies the debugger when a breakpoint is encountered.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="097dc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="097dc-104">Syntax</span></span>  
  
```  
HRESULT Breakpoint (  
    [in] ICorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugThread     *pThread,  
    [in] ICorDebugBreakpoint *pBreakpoint  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="097dc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="097dc-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="097dc-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application qui contient le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="097dc-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contains the breakpoint.</span></span>  
  
 `pThread`  
 <span data-ttu-id="097dc-107">[in] Pointeur vers un objet ICorDebugThread qui représente le thread qui contient le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="097dc-107">[in] A pointer to an ICorDebugThread object that represents the thread that contains the breakpoint.</span></span>  
  
 `pBreakpoint`  
 <span data-ttu-id="097dc-108">[in] Pointeur vers un objet ICorDebugBreakpoint qui représente le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="097dc-108">[in] A pointer to an ICorDebugBreakpoint object that represents the breakpoint.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="097dc-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="097dc-109">Requirements</span></span>  
 <span data-ttu-id="097dc-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="097dc-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="097dc-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="097dc-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="097dc-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="097dc-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="097dc-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="097dc-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="097dc-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="097dc-114">See also</span></span>

- [<span data-ttu-id="097dc-115">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="097dc-115">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
