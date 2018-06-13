---
title: ICorDebugManagedCallback::LoadModule, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.LoadModule
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::LoadModule
helpviewer_keywords:
- ICorDebugManagedCallback::LoadModule method [.NET Framework debugging]
- LoadModule method [.NET Framework debugging]
ms.assetid: 66ec04e9-87cb-42ce-9720-81522abb5d5a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cbf538f066058b4f80d8cfd6cdf1a79683c79be9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33413415"
---
# <a name="icordebugmanagedcallbackloadmodule-method"></a><span data-ttu-id="939b5-102">ICorDebugManagedCallback::LoadModule, méthode</span><span class="sxs-lookup"><span data-stu-id="939b5-102">ICorDebugManagedCallback::LoadModule Method</span></span>
<span data-ttu-id="939b5-103">Notifie le débogueur qu’un module du common language runtime (CLR) a été correctement chargé.</span><span class="sxs-lookup"><span data-stu-id="939b5-103">Notifies the debugger that a common language runtime (CLR) module has been successfully loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="939b5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="939b5-104">Syntax</span></span>  
  
```  
HRESULT LoadModule (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugModule    *pModule  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="939b5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="939b5-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="939b5-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application dans lequel le module a été chargé.</span><span class="sxs-lookup"><span data-stu-id="939b5-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain into which the module has been loaded.</span></span>  
  
 `pModule`  
 <span data-ttu-id="939b5-107">[in] Pointeur vers un objet ICorDebugModule qui représente le module CLR.</span><span class="sxs-lookup"><span data-stu-id="939b5-107">[in] A pointer to an ICorDebugModule object that represents the CLR module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="939b5-108">Notes</span><span class="sxs-lookup"><span data-stu-id="939b5-108">Remarks</span></span>  
 <span data-ttu-id="939b5-109">Le `LoadModule` rappel fournit le temps approprié pour examiner les métadonnées pour le module, définir des indicateurs de compilateur juste-à-temps (JIT), ou activer ou désactiver des rappels pour le module de chargement de classe.</span><span class="sxs-lookup"><span data-stu-id="939b5-109">The `LoadModule` callback provides an appropriate time to examine metadata for the module, set just-in-time (JIT) compiler flags, or enable or disable class loading callbacks for the module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="939b5-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="939b5-110">Requirements</span></span>  
 <span data-ttu-id="939b5-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="939b5-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="939b5-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="939b5-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="939b5-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="939b5-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="939b5-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="939b5-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="939b5-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="939b5-115">See Also</span></span>  
 [<span data-ttu-id="939b5-116">UnloadModule, méthode</span><span class="sxs-lookup"><span data-stu-id="939b5-116">UnloadModule Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-unloadmodule-method.md)  
 [<span data-ttu-id="939b5-117">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="939b5-117">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
