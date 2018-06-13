---
title: ICorDebug::SetManagedHandler, méthode
ms.date: 03/30/2017
api_name:
- ICorDebug.SetManagedHandler
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::SetManagedHandler
helpviewer_keywords:
- ICorDebug::SetManagedHandler method [.NET Framework debugging]
- SetManagedHandler method [.NET Framework debugging]
ms.assetid: d079131b-685b-4869-95be-826b88d28bd2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bcf97f9fffabb9ae9579016517cfc335e6f783a6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33404571"
---
# <a name="icordebugsetmanagedhandler-method"></a><span data-ttu-id="99f3b-102">ICorDebug::SetManagedHandler, méthode</span><span class="sxs-lookup"><span data-stu-id="99f3b-102">ICorDebug::SetManagedHandler Method</span></span>
<span data-ttu-id="99f3b-103">Spécifie l’objet de gestionnaire d’événements pour les événements managés.</span><span class="sxs-lookup"><span data-stu-id="99f3b-103">Specifies the event handler object for managed events.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="99f3b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99f3b-104">Syntax</span></span>  
  
```  
HRESULT SetManagedHandler (  
    [in] ICorDebugManagedCallback     *pCallback  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="99f3b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99f3b-105">Parameters</span></span>  
 `pCallback`  
 <span data-ttu-id="99f3b-106">[in] Un pointeur vers un [ICorDebugManagedCallback](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md) objet, qui est l’objet de gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="99f3b-106">[in] A pointer to an [ICorDebugManagedCallback](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md) object, which is the event handler object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="99f3b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="99f3b-107">Remarks</span></span>  
 <span data-ttu-id="99f3b-108">`SetManagedHandler` doit être appelée au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="99f3b-108">`SetManagedHandler` must be called at creation time.</span></span>  
  
 <span data-ttu-id="99f3b-109">Si le `ICorDebugManagedCallback` implémentation ne contient pas suffisamment d’interfaces pour gérer les événements de débogage de l’application est en cours de débogage, `SetManagedHandler` retourne un HRESULT d’E_NOINTERFACE.</span><span class="sxs-lookup"><span data-stu-id="99f3b-109">If the `ICorDebugManagedCallback` implementation does not contain sufficient interfaces to handle debugging events for the application that is being debugged, `SetManagedHandler` returns an HRESULT of E_NOINTERFACE.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="99f3b-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="99f3b-110">Requirements</span></span>  
 <span data-ttu-id="99f3b-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="99f3b-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="99f3b-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="99f3b-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="99f3b-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="99f3b-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="99f3b-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="99f3b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99f3b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99f3b-115">See Also</span></span>  
 [<span data-ttu-id="99f3b-116">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="99f3b-116">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
