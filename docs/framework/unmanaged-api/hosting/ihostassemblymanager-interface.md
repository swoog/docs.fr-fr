---
title: IHostAssemblyManager, interface
ms.date: 03/30/2017
api_name:
- IHostAssemblyManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAssemblyManager
helpviewer_keywords:
- IHostAssemblyManager interface [.NET Framework hosting]
ms.assetid: dfec05bb-3cd7-4bd5-b396-a4f097c3a636
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2e300d4645939a131ceb8206999d95056b96a678
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59118948"
---
# <a name="ihostassemblymanager-interface"></a><span data-ttu-id="c4658-102">IHostAssemblyManager, interface</span><span class="sxs-lookup"><span data-stu-id="c4658-102">IHostAssemblyManager Interface</span></span>
<span data-ttu-id="c4658-103">Fournit des méthodes qui permettent à un hôte spécifier des ensembles d’assemblys qui doivent être chargés par le common language runtime (CLR) ou par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="c4658-103">Provides methods that allow a host to specify sets of assemblies that should be loaded by the common language runtime (CLR) or by the host.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c4658-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c4658-104">Methods</span></span>  
  
|<span data-ttu-id="c4658-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="c4658-105">Method</span></span>|<span data-ttu-id="c4658-106">Description</span><span class="sxs-lookup"><span data-stu-id="c4658-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c4658-107">GetAssemblyStore, méthode</span><span class="sxs-lookup"><span data-stu-id="c4658-107">GetAssemblyStore Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-getassemblystore-method.md)|<span data-ttu-id="c4658-108">Obtient un pointeur d’interface vers un [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md) qui représente la liste des assemblys chargés par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="c4658-108">Gets an interface pointer to an [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md) that represents the list of assemblies loaded by the host.</span></span>|  
|[<span data-ttu-id="c4658-109">GetNonHostStoreAssemblies, méthode</span><span class="sxs-lookup"><span data-stu-id="c4658-109">GetNonHostStoreAssemblies Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-getnonhoststoreassemblies-method.md)|<span data-ttu-id="c4658-110">Obtient un pointeur d’interface vers un [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) qui représente la liste des assemblys CLR à charger que l’hôte attend.</span><span class="sxs-lookup"><span data-stu-id="c4658-110">Gets an interface pointer to an [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) that represents the list of assemblies that the host expects the CLR to load.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c4658-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c4658-111">Remarks</span></span>  
 <span data-ttu-id="c4658-112">L’hôte n’est pas nécessaire d’implémenter `IHostAssemblyManager` ou `IHostAssemblyStore`.</span><span class="sxs-lookup"><span data-stu-id="c4658-112">The host is not required to implement `IHostAssemblyManager` or `IHostAssemblyStore`.</span></span> <span data-ttu-id="c4658-113">Si l’hôte n’implémente pas `IHostAssemblyManager`, il doit également implémenter `IHostAssemblyStore`.</span><span class="sxs-lookup"><span data-stu-id="c4658-113">If the host does implement `IHostAssemblyManager`, it must also implement `IHostAssemblyStore`.</span></span>  
  
 <span data-ttu-id="c4658-114">Le runtime interroge pour un `IHostAssemblyManager` en appelant [IHostControl::GetHostManager](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-gethostmanager-method.md) lors de l’initialisation avec un `IID` d’IID_IHostAssemblyManager.</span><span class="sxs-lookup"><span data-stu-id="c4658-114">The runtime queries for an `IHostAssemblyManager` by calling [IHostControl::GetHostManager](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-gethostmanager-method.md) upon initialization with an `IID` of IID_IHostAssemblyManager.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c4658-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4658-115">Requirements</span></span>  
 <span data-ttu-id="c4658-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c4658-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c4658-117">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="c4658-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c4658-118">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c4658-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="c4658-119">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="c4658-119">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="c4658-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4658-120">See also</span></span>

- [<span data-ttu-id="c4658-121">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="c4658-121">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="c4658-122">IHostAssemblyStore, interface</span><span class="sxs-lookup"><span data-stu-id="c4658-122">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
- [<span data-ttu-id="c4658-123">IHostControl, interface</span><span class="sxs-lookup"><span data-stu-id="c4658-123">IHostControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)
- [<span data-ttu-id="c4658-124">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="c4658-124">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
