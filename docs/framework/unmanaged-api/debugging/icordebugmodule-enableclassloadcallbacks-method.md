---
title: ICorDebugModule::EnableClassLoadCallbacks, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.EnableClassLoadCallbacks
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::EnableClassLoadCallbacks
helpviewer_keywords:
- ICorDebugModule::EnableClassLoadCallbacks method [.NET Framework debugging]
- EnableClassLoadCallbacks method [.NET Framework debugging]
ms.assetid: 78dad5e4-8e2e-400f-bec3-92ff0205cd82
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 22a838748414f9d89cdc7ff469f7f5cc5e11b9d4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59108301"
---
# <a name="icordebugmoduleenableclassloadcallbacks-method"></a><span data-ttu-id="0d784-102">ICorDebugModule::EnableClassLoadCallbacks, méthode</span><span class="sxs-lookup"><span data-stu-id="0d784-102">ICorDebugModule::EnableClassLoadCallbacks Method</span></span>
<span data-ttu-id="0d784-103">Contrôles si le [ICorDebugManagedCallback::LoadClass](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-loadclass-method.md) et [ICorDebugManagedCallback::UnloadClass](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-unloadclass-method.md) sont appelés pour ce module.</span><span class="sxs-lookup"><span data-stu-id="0d784-103">Controls whether the [ICorDebugManagedCallback::LoadClass](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-loadclass-method.md) and [ICorDebugManagedCallback::UnloadClass](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-unloadclass-method.md) callbacks are called for this module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0d784-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d784-104">Syntax</span></span>  
  
```  
HRESULT EnableClassLoadCallbacks(  
    [in] BOOL bClassLoadCallbacks  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0d784-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d784-105">Parameters</span></span>  
 `bClassLoadCallbacks`  
 <span data-ttu-id="0d784-106">[in] Définissez cette valeur sur `true` pour activer le common language runtime (CLR) pour appeler le `ICorDebugManagedCallback::LoadClass` et `ICorDebugManagedCallback::UnloadClass` méthodes lorsque leurs événements associés se produisent.</span><span class="sxs-lookup"><span data-stu-id="0d784-106">[in] Set this value to `true` to enable the common language runtime (CLR) to call the `ICorDebugManagedCallback::LoadClass` and `ICorDebugManagedCallback::UnloadClass` methods when their associated events occur.</span></span>  
  
 <span data-ttu-id="0d784-107">La valeur par défaut est `false` pour les modules non dynamiques.</span><span class="sxs-lookup"><span data-stu-id="0d784-107">The default value is `false` for non-dynamic modules.</span></span> <span data-ttu-id="0d784-108">La valeur est toujours `true` pour les modules dynamiques et ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="0d784-108">The value is always `true` for dynamic modules and cannot be changed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0d784-109">Notes</span><span class="sxs-lookup"><span data-stu-id="0d784-109">Remarks</span></span>  
 <span data-ttu-id="0d784-110">Le `ICorDebugManagedCallback::LoadClass` et `ICorDebugManagedCallback::UnloadClass` rappels sont toujours activées pour les modules dynamiques et ne peut pas être désactivées.</span><span class="sxs-lookup"><span data-stu-id="0d784-110">The `ICorDebugManagedCallback::LoadClass` and `ICorDebugManagedCallback::UnloadClass` callbacks are always enabled for dynamic modules and cannot be disabled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0d784-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d784-111">Requirements</span></span>  
 <span data-ttu-id="0d784-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0d784-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0d784-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0d784-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0d784-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0d784-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="0d784-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="0d784-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0d784-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d784-116">See also</span></span>
