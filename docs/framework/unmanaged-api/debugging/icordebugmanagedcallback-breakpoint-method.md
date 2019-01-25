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
ms.openlocfilehash: a1df57e82309d42092c38dfcdd8b65ccc2797f9a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54743281"
---
# <a name="icordebugmanagedcallbackbreakpoint-method"></a><span data-ttu-id="4cfa3-102">ICorDebugManagedCallback::Breakpoint, méthode</span><span class="sxs-lookup"><span data-stu-id="4cfa3-102">ICorDebugManagedCallback::Breakpoint Method</span></span>
<span data-ttu-id="4cfa3-103">Notifie le débogueur lorsqu’un point d’arrêt est rencontré.</span><span class="sxs-lookup"><span data-stu-id="4cfa3-103">Notifies the debugger when a breakpoint is encountered.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4cfa3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cfa3-104">Syntax</span></span>  
  
```  
HRESULT Breakpoint (  
    [in] ICorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugThread     *pThread,  
    [in] ICorDebugBreakpoint *pBreakpoint  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4cfa3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4cfa3-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="4cfa3-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application qui contient le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="4cfa3-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contains the breakpoint.</span></span>  
  
 `pThread`  
 <span data-ttu-id="4cfa3-107">[in] Pointeur vers un objet ICorDebugThread qui représente le thread qui contient le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="4cfa3-107">[in] A pointer to an ICorDebugThread object that represents the thread that contains the breakpoint.</span></span>  
  
 `pBreakpoint`  
 <span data-ttu-id="4cfa3-108">[in] Pointeur vers un objet ICorDebugBreakpoint qui représente le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="4cfa3-108">[in] A pointer to an ICorDebugBreakpoint object that represents the breakpoint.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4cfa3-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4cfa3-109">Requirements</span></span>  
 <span data-ttu-id="4cfa3-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4cfa3-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4cfa3-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4cfa3-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4cfa3-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4cfa3-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4cfa3-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4cfa3-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4cfa3-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cfa3-114">See also</span></span>
- [<span data-ttu-id="4cfa3-115">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="4cfa3-115">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
