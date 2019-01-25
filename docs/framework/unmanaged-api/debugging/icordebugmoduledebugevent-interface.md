---
title: ICorDebugModuleDebugEvent, interface
ms.date: 03/30/2017
ms.assetid: 41950c52-1ac8-4212-b814-c77e20879f91
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 399f27db0a2d18e3bcd90b87f4470a77cb50595d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54646854"
---
# <a name="icordebugmoduledebugevent-interface"></a><span data-ttu-id="9dbb1-102">ICorDebugModuleDebugEvent, interface</span><span class="sxs-lookup"><span data-stu-id="9dbb1-102">ICorDebugModuleDebugEvent Interface</span></span>
<span data-ttu-id="9dbb1-103">Étend la [ICorDebugDebugEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md) interface pour prendre en charge les événements au niveau du module.</span><span class="sxs-lookup"><span data-stu-id="9dbb1-103">Extends the [ICorDebugDebugEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md) interface to support module-level events.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9dbb1-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9dbb1-104">Methods</span></span>  
  
|<span data-ttu-id="9dbb1-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="9dbb1-105">Method</span></span>|<span data-ttu-id="9dbb1-106">Description</span><span class="sxs-lookup"><span data-stu-id="9dbb1-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9dbb1-107">GetModule, méthode</span><span class="sxs-lookup"><span data-stu-id="9dbb1-107">GetModule Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmoduledebugevent-getmodule-method.md)|<span data-ttu-id="9dbb1-108">Obtient le module fusionné qui vient d’être chargé ou déchargé.</span><span class="sxs-lookup"><span data-stu-id="9dbb1-108">Gets the merged module that was just loaded or unloaded.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9dbb1-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9dbb1-109">Remarks</span></span>  
 <span data-ttu-id="9dbb1-110">Le [MODULE_LOADED](../../../../docs/framework/unmanaged-api/debugging/cordebugdebugeventkind-enumeration.md) et [MODULE_UNLOADED](../../../../docs/framework/unmanaged-api/debugging/cordebugdebugeventkind-enumeration.md) types d’événements implémentent cette interface.</span><span class="sxs-lookup"><span data-stu-id="9dbb1-110">The [MODULE_LOADED](../../../../docs/framework/unmanaged-api/debugging/cordebugdebugeventkind-enumeration.md) and [MODULE_UNLOADED](../../../../docs/framework/unmanaged-api/debugging/cordebugdebugeventkind-enumeration.md) event types implement this interface.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9dbb1-111">L'interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="9dbb1-111">The interface is available with .NET Native only.</span></span> <span data-ttu-id="9dbb1-112">Une tentative d'appel à `QueryInterface` pour récupérer un pointeur d'interface retourne `E_NOINTERFACE` pour les scénarios ICorDebug en dehors de .NET Native.</span><span class="sxs-lookup"><span data-stu-id="9dbb1-112">Attempting to call `QueryInterface` to retrieve an interface pointer returns `E_NOINTERFACE` for ICorDebug scenarios outside of .NET Native.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9dbb1-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9dbb1-113">Requirements</span></span>  
 <span data-ttu-id="9dbb1-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9dbb1-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9dbb1-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9dbb1-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9dbb1-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9dbb1-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9dbb1-117">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9dbb1-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9dbb1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dbb1-118">See also</span></span>
- [<span data-ttu-id="9dbb1-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="9dbb1-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="9dbb1-120">Débogage</span><span class="sxs-lookup"><span data-stu-id="9dbb1-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
