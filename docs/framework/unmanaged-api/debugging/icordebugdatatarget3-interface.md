---
title: ICorDebugDataTarget3 (interface)
ms.date: 03/30/2017
ms.assetid: f477af85-994f-4df0-ae78-404ed252bf49
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8f97a6819c413c79eb8431c9a101249d459b0155
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54545249"
---
# <a name="icordebugdatatarget3-interface"></a><span data-ttu-id="0fecd-102">ICorDebugDataTarget3 (interface)</span><span class="sxs-lookup"><span data-stu-id="0fecd-102">ICorDebugDataTarget3 Interface</span></span>
<span data-ttu-id="0fecd-103">Étend logiquement le [ICorDebugDataTarget](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-interface.md) interface pour fournir des informations sur les modules chargés.</span><span class="sxs-lookup"><span data-stu-id="0fecd-103">Logically extends the [ICorDebugDataTarget](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-interface.md) interface to provide information about loaded modules.</span></span>  
  
## <a name="method"></a><span data-ttu-id="0fecd-104">Méthode</span><span class="sxs-lookup"><span data-stu-id="0fecd-104">Method</span></span>  
  
|<span data-ttu-id="0fecd-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="0fecd-105">Method</span></span>|<span data-ttu-id="0fecd-106">Description</span><span class="sxs-lookup"><span data-stu-id="0fecd-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0fecd-107">GetLoadedModules, méthode</span><span class="sxs-lookup"><span data-stu-id="0fecd-107">GetLoadedModules Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget3-getloadedmodules-method.md)|<span data-ttu-id="0fecd-108">Obtient la liste des modules qui ont été chargés jusqu'à présent.</span><span class="sxs-lookup"><span data-stu-id="0fecd-108">Gets a list of the modules that have been loaded so far.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0fecd-109">Notes</span><span class="sxs-lookup"><span data-stu-id="0fecd-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0fecd-110">Cette interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="0fecd-110">This interface is available with .NET Native only.</span></span> <span data-ttu-id="0fecd-111">Si vous implémentez cette interface pour des scénarios ICorDebug en dehors de .NET Native, le Common Language Runtime ignore cette interface.</span><span class="sxs-lookup"><span data-stu-id="0fecd-111">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0fecd-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0fecd-112">Requirements</span></span>  
 <span data-ttu-id="0fecd-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0fecd-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0fecd-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0fecd-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0fecd-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0fecd-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0fecd-116">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0fecd-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0fecd-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fecd-117">See also</span></span>
- [<span data-ttu-id="0fecd-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="0fecd-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="0fecd-119">Débogage</span><span class="sxs-lookup"><span data-stu-id="0fecd-119">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
