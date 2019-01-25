---
title: ICorDebugManagedCallback::LoadClass, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.LoadClass
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::LoadClass
helpviewer_keywords:
- ICorDebugManagedCallback::LoadClass method [.NET Framework debugging]
- LoadClass method [.NET Framework debugging]
ms.assetid: e58dac7b-85c3-41ca-b9aa-3a7fc9ae6680
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f3c430e18864c0352b43641bce9a7d52af69cc80
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54718219"
---
# <a name="icordebugmanagedcallbackloadclass-method"></a><span data-ttu-id="fc748-102">ICorDebugManagedCallback::LoadClass, méthode</span><span class="sxs-lookup"><span data-stu-id="fc748-102">ICorDebugManagedCallback::LoadClass Method</span></span>
<span data-ttu-id="fc748-103">Notifie le débogueur qu’une classe a été chargée.</span><span class="sxs-lookup"><span data-stu-id="fc748-103">Notifies the debugger that a class has been loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fc748-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc748-104">Syntax</span></span>  
  
```  
HRESULT LoadClass (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugClass     *c  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fc748-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc748-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="fc748-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application dans lequel la classe a été chargée.</span><span class="sxs-lookup"><span data-stu-id="fc748-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain into which the class has been loaded.</span></span>  
  
 `c`  
 <span data-ttu-id="fc748-107">[in] Pointeur vers un objet ICorDebugClass qui représente la classe.</span><span class="sxs-lookup"><span data-stu-id="fc748-107">[in] A pointer to an ICorDebugClass object that represents the class.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fc748-108">Notes</span><span class="sxs-lookup"><span data-stu-id="fc748-108">Remarks</span></span>  
 <span data-ttu-id="fc748-109">Ce rappel se produit uniquement si le chargement de classe a été activé pour le module qui contient la classe.</span><span class="sxs-lookup"><span data-stu-id="fc748-109">This callback occurs only if class loading has been enabled for the module that contains the class.</span></span> <span data-ttu-id="fc748-110">Le chargement de classe est toujours activé pour les modules dynamiques.</span><span class="sxs-lookup"><span data-stu-id="fc748-110">Class loading is always enabled for dynamic modules.</span></span>  
  
 <span data-ttu-id="fc748-111">Le `LoadClass` rappel fournit un bon moment pour lier des points d’arrêt pour les classes qui vient d’être générées dans les modules dynamiques.</span><span class="sxs-lookup"><span data-stu-id="fc748-111">The `LoadClass` callback provides an appropriate time to bind breakpoints to newly generated classes in dynamic modules.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fc748-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fc748-112">Requirements</span></span>  
 <span data-ttu-id="fc748-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fc748-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fc748-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fc748-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fc748-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fc748-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fc748-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fc748-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fc748-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc748-117">See also</span></span>
- [<span data-ttu-id="fc748-118">UnloadClass, méthode</span><span class="sxs-lookup"><span data-stu-id="fc748-118">UnloadClass Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-unloadclass-method.md)
- [<span data-ttu-id="fc748-119">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="fc748-119">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
