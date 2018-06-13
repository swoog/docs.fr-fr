---
title: ICorDebugModuleDebugEvent, interface
ms.date: 03/30/2017
ms.assetid: 41950c52-1ac8-4212-b814-c77e20879f91
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f35c26b98521311267a627265f2dae8fa9e333de
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33421838"
---
# <a name="icordebugmoduledebugevent-interface"></a><span data-ttu-id="ac80a-102">ICorDebugModuleDebugEvent, interface</span><span class="sxs-lookup"><span data-stu-id="ac80a-102">ICorDebugModuleDebugEvent Interface</span></span>
<span data-ttu-id="ac80a-103">Étend la [ICorDebugDebugEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md) interface pour prendre en charge les événements au niveau du module.</span><span class="sxs-lookup"><span data-stu-id="ac80a-103">Extends the [ICorDebugDebugEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md) interface to support module-level events.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ac80a-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ac80a-104">Methods</span></span>  
  
|<span data-ttu-id="ac80a-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="ac80a-105">Method</span></span>|<span data-ttu-id="ac80a-106">Description</span><span class="sxs-lookup"><span data-stu-id="ac80a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ac80a-107">GetModule, méthode</span><span class="sxs-lookup"><span data-stu-id="ac80a-107">GetModule Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmoduledebugevent-getmodule-method.md)|<span data-ttu-id="ac80a-108">Obtient le module fusionné qui vient d’être chargé ou déchargé.</span><span class="sxs-lookup"><span data-stu-id="ac80a-108">Gets the merged module that was just loaded or unloaded.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ac80a-109">Notes</span><span class="sxs-lookup"><span data-stu-id="ac80a-109">Remarks</span></span>  
 <span data-ttu-id="ac80a-110">Le [MODULE_LOADED](../../../../docs/framework/unmanaged-api/debugging/cordebugdebugeventkind-enumeration.md) et [MODULE_UNLOADED](../../../../docs/framework/unmanaged-api/debugging/cordebugdebugeventkind-enumeration.md) types d’événements implémentent cette interface.</span><span class="sxs-lookup"><span data-stu-id="ac80a-110">The [MODULE_LOADED](../../../../docs/framework/unmanaged-api/debugging/cordebugdebugeventkind-enumeration.md) and [MODULE_UNLOADED](../../../../docs/framework/unmanaged-api/debugging/cordebugdebugeventkind-enumeration.md) event types implement this interface.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ac80a-111">L'interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="ac80a-111">The interface is available with .NET Native only.</span></span> <span data-ttu-id="ac80a-112">Une tentative d'appel à `QueryInterface` pour récupérer un pointeur d'interface retourne `E_NOINTERFACE` pour les scénarios ICorDebug en dehors de .NET Native.</span><span class="sxs-lookup"><span data-stu-id="ac80a-112">Attempting to call `QueryInterface` to retrieve an interface pointer returns `E_NOINTERFACE` for ICorDebug scenarios outside of .NET Native.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ac80a-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ac80a-113">Requirements</span></span>  
 <span data-ttu-id="ac80a-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ac80a-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ac80a-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ac80a-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ac80a-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ac80a-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ac80a-117">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ac80a-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac80a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac80a-118">See Also</span></span>  
 [<span data-ttu-id="ac80a-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="ac80a-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="ac80a-120">Débogage</span><span class="sxs-lookup"><span data-stu-id="ac80a-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
