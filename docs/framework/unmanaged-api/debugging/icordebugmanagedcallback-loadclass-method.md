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
ms.openlocfilehash: 39ce3e8329c4ff32b55341127f68a800246677df
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59169947"
---
# <a name="icordebugmanagedcallbackloadclass-method"></a><span data-ttu-id="1ef0b-102">ICorDebugManagedCallback::LoadClass, méthode</span><span class="sxs-lookup"><span data-stu-id="1ef0b-102">ICorDebugManagedCallback::LoadClass Method</span></span>
<span data-ttu-id="1ef0b-103">Notifie le débogueur qu’une classe a été chargée.</span><span class="sxs-lookup"><span data-stu-id="1ef0b-103">Notifies the debugger that a class has been loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ef0b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ef0b-104">Syntax</span></span>  
  
```  
HRESULT LoadClass (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugClass     *c  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1ef0b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ef0b-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="1ef0b-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application dans lequel la classe a été chargée.</span><span class="sxs-lookup"><span data-stu-id="1ef0b-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain into which the class has been loaded.</span></span>  
  
 `c`  
 <span data-ttu-id="1ef0b-107">[in] Pointeur vers un objet ICorDebugClass qui représente la classe.</span><span class="sxs-lookup"><span data-stu-id="1ef0b-107">[in] A pointer to an ICorDebugClass object that represents the class.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1ef0b-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1ef0b-108">Remarks</span></span>  
 <span data-ttu-id="1ef0b-109">Ce rappel se produit uniquement si le chargement de classe a été activé pour le module qui contient la classe.</span><span class="sxs-lookup"><span data-stu-id="1ef0b-109">This callback occurs only if class loading has been enabled for the module that contains the class.</span></span> <span data-ttu-id="1ef0b-110">Le chargement de classe est toujours activé pour les modules dynamiques.</span><span class="sxs-lookup"><span data-stu-id="1ef0b-110">Class loading is always enabled for dynamic modules.</span></span>  
  
 <span data-ttu-id="1ef0b-111">Le `LoadClass` rappel fournit un bon moment pour lier des points d’arrêt pour les classes qui vient d’être générées dans les modules dynamiques.</span><span class="sxs-lookup"><span data-stu-id="1ef0b-111">The `LoadClass` callback provides an appropriate time to bind breakpoints to newly generated classes in dynamic modules.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1ef0b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ef0b-112">Requirements</span></span>  
 <span data-ttu-id="1ef0b-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1ef0b-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1ef0b-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1ef0b-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1ef0b-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1ef0b-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1ef0b-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1ef0b-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1ef0b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ef0b-117">See also</span></span>

- [<span data-ttu-id="1ef0b-118">UnloadClass, méthode</span><span class="sxs-lookup"><span data-stu-id="1ef0b-118">UnloadClass Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-unloadclass-method.md)
- [<span data-ttu-id="1ef0b-119">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="1ef0b-119">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
