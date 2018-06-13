---
title: ICorDebugAppDomain3, interface
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain3
helpviewer_keywords:
- ICorDebugAppDomain3 interface [.NET Framework debugging]
ms.assetid: 875ef5be-c1e7-4d95-97e9-d3a667aeaba0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7c130b92fd5114d067730da3b7cd138d98cf0577
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33407403"
---
# <a name="icordebugappdomain3-interface"></a><span data-ttu-id="4db49-102">ICorDebugAppDomain3, interface</span><span class="sxs-lookup"><span data-stu-id="4db49-102">ICorDebugAppDomain3 Interface</span></span>
<span data-ttu-id="4db49-103">Fournit des méthodes pour récupérer des informations sur les représentations managées de [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types actuellement chargés dans un domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="4db49-103">Provides methods to retrieve information about the managed representations of [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types currently loaded in an application domain.</span></span> <span data-ttu-id="4db49-104">Cette interface est une extension des interfaces ICorDebugAppDomain et ICorDebugAppDomain2.</span><span class="sxs-lookup"><span data-stu-id="4db49-104">This interface is an extension of the ICorDebugAppDomain and ICorDebugAppDomain2 interfaces.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4db49-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4db49-105">Methods</span></span>  
  
|<span data-ttu-id="4db49-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="4db49-106">Method</span></span>|<span data-ttu-id="4db49-107">Description</span><span class="sxs-lookup"><span data-stu-id="4db49-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4db49-108">ICorDebugAppDomain3::GetCachedWinRTTypes</span><span class="sxs-lookup"><span data-stu-id="4db49-108">ICorDebugAppDomain3::GetCachedWinRTTypes</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain3-getcachedwinrttypes-method.md)|<span data-ttu-id="4db49-109">Obtient un énumérateur pour toutes les mises en cache [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types.</span><span class="sxs-lookup"><span data-stu-id="4db49-109">Gets an enumerator for all cached [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types.</span></span>|  
|[<span data-ttu-id="4db49-110">ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs</span><span class="sxs-lookup"><span data-stu-id="4db49-110">ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain3-getcachedwinrttypesforiids-method.md)|<span data-ttu-id="4db49-111">Obtient un énumérateur pour la mise en cache [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types dans un domaine d’application en fonction de leurs identificateurs de l’interface.</span><span class="sxs-lookup"><span data-stu-id="4db49-111">Gets an enumerator for cached [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types in an application domain based on their interface identifiers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4db49-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4db49-112">Remarks</span></span>  
 <span data-ttu-id="4db49-113">Cette interface est destinée à être utilisée par un débogueur conjointement avec un appel de l’évaluation de fonction à `M:System.Runtime.InteropServices.Marshal.GetInspectableIIDs(System.Object)`.</span><span class="sxs-lookup"><span data-stu-id="4db49-113">This interface is meant to be used by a debugger in conjunction with a function evaluation call to `M:System.Runtime.InteropServices.Marshal.GetInspectableIIDs(System.Object)`.</span></span> <span data-ttu-id="4db49-114">Lorsque la méthode récupère les identificateurs d’interface pris en charge par un [!INCLUDE[wrt](../../../../includes/wrt-md.md)] l’objet serveur, le débogueur peut utiliser les méthodes définies dans cette interface pour le mappage des types managés qui correspondent à ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="4db49-114">When the method retrieves the interface identifiers supported by a [!INCLUDE[wrt](../../../../includes/wrt-md.md)] server object, the debugger may use the methods defined in this interface to map them to managed types that correspond to those interfaces.</span></span>  
  
 <span data-ttu-id="4db49-115">Pour récupérer une instance de cette interface, vous devez exécuter `QueryInterface` sur une instance de l’interface ICorDebugAppDomain ou ICorDebugAppDomain2.</span><span class="sxs-lookup"><span data-stu-id="4db49-115">To retrieve an instance of this interface, run `QueryInterface` on an instance of the ICorDebugAppDomain or ICorDebugAppDomain2 interface.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4db49-116">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="4db49-116">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4db49-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4db49-117">Requirements</span></span>  
 <span data-ttu-id="4db49-118">**Plateformes :** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4db49-118">**Platforms:** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]</span></span>  
  
 <span data-ttu-id="4db49-119">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4db49-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4db49-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4db49-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4db49-121">**Versions du .NET framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4db49-121">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4db49-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4db49-122">See Also</span></span>  
 [<span data-ttu-id="4db49-123">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="4db49-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
