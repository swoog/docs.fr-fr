---
title: ICorDebugModuleDebugEvent::GetModule, méthode
ms.date: 03/30/2017
ms.assetid: b1141c35-4253-4e34-b3e4-ed406a9dea4f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0c0cc1305f47f03c8c9b35bab5c980cb23d1b157
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59138435"
---
# <a name="icordebugmoduledebugeventgetmodule-method"></a><span data-ttu-id="405f3-102">ICorDebugModuleDebugEvent::GetModule, méthode</span><span class="sxs-lookup"><span data-stu-id="405f3-102">ICorDebugModuleDebugEvent::GetModule Method</span></span>
<span data-ttu-id="405f3-103">Obtient le module fusionné qui vient d’être chargé ou déchargé.</span><span class="sxs-lookup"><span data-stu-id="405f3-103">Gets the merged module that was just loaded or unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="405f3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="405f3-104">Syntax</span></span>  
  
```  
HRESULT GetModule(  
   [out]ICorDebugModule **ppModule  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="405f3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="405f3-105">Parameters</span></span>  
 `ppModule`  
 <span data-ttu-id="405f3-106">[out] Pointeur vers l’adresse d’un objet ICorDebugModule qui représente le module fusionné qui a été simplement chargé ou déchargé.</span><span class="sxs-lookup"><span data-stu-id="405f3-106">[out] A pointer to the address of an ICorDebugModule object that represents the merged module that was just loaded or unloaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="405f3-107">Notes</span><span class="sxs-lookup"><span data-stu-id="405f3-107">Remarks</span></span>  
 <span data-ttu-id="405f3-108">Vous pouvez appeler la [GetEventKind](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-geteventkind-method.md) méthode pour déterminer si le module a été chargé ou déchargé.</span><span class="sxs-lookup"><span data-stu-id="405f3-108">You can call the [GetEventKind](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-geteventkind-method.md) method to determine whether the module was loaded or unloaded.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="405f3-109">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="405f3-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="405f3-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="405f3-110">Requirements</span></span>  
 <span data-ttu-id="405f3-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="405f3-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="405f3-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="405f3-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="405f3-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="405f3-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="405f3-114">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="405f3-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="405f3-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="405f3-115">See also</span></span>

- [<span data-ttu-id="405f3-116">ICorDebugModuleDebugEvent, interface</span><span class="sxs-lookup"><span data-stu-id="405f3-116">ICorDebugModuleDebugEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmoduledebugevent-interface.md)
- [<span data-ttu-id="405f3-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="405f3-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
