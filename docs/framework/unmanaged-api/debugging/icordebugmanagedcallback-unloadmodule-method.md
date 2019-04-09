---
title: ICorDebugManagedCallback::UnloadModule, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.UnloadModule
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::UnloadModule
helpviewer_keywords:
- ICorDebugManagedCallback::UnloadModule method [.NET Framework debugging]
- UnloadModule method [.NET Framework debugging]
ms.assetid: b12bfcd9-1e29-48bf-9a3d-44bfae5df5e8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 12e42da015864e83663d2f4d74bab2a34052d760
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59083542"
---
# <a name="icordebugmanagedcallbackunloadmodule-method"></a><span data-ttu-id="a5ea5-102">ICorDebugManagedCallback::UnloadModule, méthode</span><span class="sxs-lookup"><span data-stu-id="a5ea5-102">ICorDebugManagedCallback::UnloadModule Method</span></span>
<span data-ttu-id="a5ea5-103">Notifie le débogueur qu’un module du common language runtime (DLL) a été déchargé.</span><span class="sxs-lookup"><span data-stu-id="a5ea5-103">Notifies the debugger that a common language runtime module (DLL) has been unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a5ea5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5ea5-104">Syntax</span></span>  
  
```  
HRESULT UnloadModule (  
    [in] ICorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugModule     *pModule  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a5ea5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5ea5-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="a5ea5-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application qui contenait le module.</span><span class="sxs-lookup"><span data-stu-id="a5ea5-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contained the module.</span></span>  
  
 `pModule`  
 <span data-ttu-id="a5ea5-107">[in] Pointeur vers un objet ICorDebugModule qui représente le module.</span><span class="sxs-lookup"><span data-stu-id="a5ea5-107">[in] A pointer to an ICorDebugModule object that represents the module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a5ea5-108">Notes</span><span class="sxs-lookup"><span data-stu-id="a5ea5-108">Remarks</span></span>  
 <span data-ttu-id="a5ea5-109">Le module ne doit pas être utilisé après cet appel.</span><span class="sxs-lookup"><span data-stu-id="a5ea5-109">The module should not be used after this call.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a5ea5-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5ea5-110">Requirements</span></span>  
 <span data-ttu-id="a5ea5-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a5ea5-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a5ea5-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a5ea5-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a5ea5-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a5ea5-113">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="a5ea5-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="a5ea5-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="a5ea5-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5ea5-115">See also</span></span>

- [<span data-ttu-id="a5ea5-116">LoadModule, méthode</span><span class="sxs-lookup"><span data-stu-id="a5ea5-116">LoadModule Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-loadmodule-method.md)
- [<span data-ttu-id="a5ea5-117">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="a5ea5-117">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
