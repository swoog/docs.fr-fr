---
title: ICLRGCManager2, interface
ms.date: 03/30/2017
api_name:
- ICLRGCManager2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRGCManager2
helpviewer_keywords:
- ICLRGCManager2 interface [.NET Framework hosting]
ms.assetid: 4b5ffd7b-9ad7-41cd-9bba-34030ae3da7e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a89a7ef34418163d790fd055de681c1cdf989e57
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59226909"
---
# <a name="iclrgcmanager2-interface"></a><span data-ttu-id="4c97b-102">ICLRGCManager2, interface</span><span class="sxs-lookup"><span data-stu-id="4c97b-102">ICLRGCManager2 Interface</span></span>
<span data-ttu-id="4c97b-103">Fournit des méthodes qui permettent à un hôte d’interagir avec le système de garbage collection du common language runtime.</span><span class="sxs-lookup"><span data-stu-id="4c97b-103">Provides methods that allow a host to interact with the common language runtime's garbage collection system.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4c97b-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4c97b-104">Methods</span></span>  
  
|<span data-ttu-id="4c97b-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="4c97b-105">Method</span></span>|<span data-ttu-id="4c97b-106">Description</span><span class="sxs-lookup"><span data-stu-id="4c97b-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4c97b-107">SetGCStartupLimitsEx, méthode</span><span class="sxs-lookup"><span data-stu-id="4c97b-107">SetGCStartupLimitsEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager2-setgcstartuplimitsex-method.md)|<span data-ttu-id="4c97b-108">Définit la taille d’un segment de garbage collection et la taille maximale de la génération du système de nettoyage 0.</span><span class="sxs-lookup"><span data-stu-id="4c97b-108">Sets the size of a garbage collection segment and the maximum size of the garbage collection system's generation 0.</span></span> <span data-ttu-id="4c97b-109">Permet la génération 0 et les tailles de segment supérieures à `DWORD`.</span><span class="sxs-lookup"><span data-stu-id="4c97b-109">Enables generation 0 and segment sizes larger than `DWORD`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4c97b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4c97b-110">Remarks</span></span>  
 <span data-ttu-id="4c97b-111">Cette interface hérite le [ICLRGCManager, Interface](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager-interface.md).</span><span class="sxs-lookup"><span data-stu-id="4c97b-111">This interface inherits from the [ICLRGCManager Interface](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager-interface.md).</span></span>  
  
 <span data-ttu-id="4c97b-112">Le common language runtime (CLR) implémente son mécanisme de garbage collection avec managé <xref:System.GC> type.</span><span class="sxs-lookup"><span data-stu-id="4c97b-112">The common language runtime (CLR) implements its garbage collection mechanism with the managed <xref:System.GC> type.</span></span> <span data-ttu-id="4c97b-113">Pour plus d’informations sur le système de garbage collection, consultez [Garbage Collection](../../../../docs/standard/garbage-collection/index.md).</span><span class="sxs-lookup"><span data-stu-id="4c97b-113">For more information about the garbage collection system, see [Garbage Collection](../../../../docs/standard/garbage-collection/index.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4c97b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c97b-114">Requirements</span></span>  
 <span data-ttu-id="4c97b-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4c97b-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4c97b-116">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="4c97b-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="4c97b-117">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4c97b-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4c97b-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4c97b-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c97b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c97b-119">See also</span></span>

- [<span data-ttu-id="4c97b-120">Gestion automatique de la mémoire</span><span class="sxs-lookup"><span data-stu-id="4c97b-120">Automatic Memory Management</span></span>](../../../../docs/standard/automatic-memory-management.md)
- [<span data-ttu-id="4c97b-121">COR_GC_STATS, structure</span><span class="sxs-lookup"><span data-stu-id="4c97b-121">COR_GC_STATS Structure</span></span>](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md)
- [<span data-ttu-id="4c97b-122">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="4c97b-122">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
- [<span data-ttu-id="4c97b-123">Interfaces d’hébergement CLR ajoutées dans .NET Framework 4 et 4.5</span><span class="sxs-lookup"><span data-stu-id="4c97b-123">CLR Hosting Interfaces Added in the .NET Framework 4 and 4.5</span></span>](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)
- [<span data-ttu-id="4c97b-124">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="4c97b-124">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="4c97b-125">Hébergement</span><span class="sxs-lookup"><span data-stu-id="4c97b-125">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
