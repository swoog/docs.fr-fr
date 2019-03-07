---
title: ICorDebugManagedCallback2::FunctionRemapComplete, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback2.FunctionRemapComplete
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback2::FunctionRemapComplete
helpviewer_keywords:
- FunctionRemapComplete method [.NET Framework debugging]
- ICorDebugManagedCallback2::FunctionRemapComplete method [.NET Framework debugging]
ms.assetid: 5396c4c3-4ec3-4e3a-a38d-d65b21f0a2fc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a5f4c9b6afd9b0a7a43c279c9a070740100d8f86
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57478620"
---
# <a name="icordebugmanagedcallback2functionremapcomplete-method"></a><span data-ttu-id="46e05-102">ICorDebugManagedCallback2::FunctionRemapComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="46e05-102">ICorDebugManagedCallback2::FunctionRemapComplete Method</span></span>
<span data-ttu-id="46e05-103">Notifie le débogueur que l’exécution de code a basculé vers une nouvelle version d’une fonction modifiée.</span><span class="sxs-lookup"><span data-stu-id="46e05-103">Notifies the debugger that code execution has switched to a new version of an edited function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46e05-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46e05-104">Syntax</span></span>  
  
```  
HRESULT FunctionRemapComplete (  
    [in] ICorDebugAppDomain   *pAppDomain,  
    [in] ICorDebugThread      *pThread,  
    [in] ICorDebugFunction    *pFunction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="46e05-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46e05-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="46e05-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application contenant la fonction modifiée.</span><span class="sxs-lookup"><span data-stu-id="46e05-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain containing the edited function.</span></span>  
  
 `pThread`  
 <span data-ttu-id="46e05-107">[in] Pointeur vers un objet ICorDebugThread qui représente le thread sur lequel le point d’arrêt de remappage a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="46e05-107">[in] A pointer to an ICorDebugThread object that represents the thread on which the remap breakpoint was encountered.</span></span>  
  
 `pFunction`  
 <span data-ttu-id="46e05-108">[in] Pointeur vers un objet ICorDebugFunction qui représente la version de la fonction en cours d’exécution sur le thread.</span><span class="sxs-lookup"><span data-stu-id="46e05-108">[in] A pointer to an ICorDebugFunction object that represents the version of the function currently running on the thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="46e05-109">Notes</span><span class="sxs-lookup"><span data-stu-id="46e05-109">Remarks</span></span>  
 <span data-ttu-id="46e05-110">Ce rappel permet au débogueur une opportunité pour recréer les exécutions pas à pas qui existait précédemment.</span><span class="sxs-lookup"><span data-stu-id="46e05-110">This callback gives the debugger an opportunity to recreate any steppers that previously existed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="46e05-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="46e05-111">Requirements</span></span>  
 <span data-ttu-id="46e05-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="46e05-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="46e05-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="46e05-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="46e05-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="46e05-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="46e05-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="46e05-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46e05-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46e05-116">See also</span></span>
- [<span data-ttu-id="46e05-117">ICorDebugManagedCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="46e05-117">ICorDebugManagedCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md)
- [<span data-ttu-id="46e05-118">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="46e05-118">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
