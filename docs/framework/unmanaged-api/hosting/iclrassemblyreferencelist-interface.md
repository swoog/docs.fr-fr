---
title: ICLRAssemblyReferenceList, interface
ms.date: 03/30/2017
api_name:
- ICLRAssemblyReferenceList
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyReferenceList
helpviewer_keywords:
- ICLRAssemblyReferenceList interface [.NET Framework hosting]
ms.assetid: 5f890fdf-d22a-429e-a35f-135273d1a636
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 388b26a5559435ea57300751987d14bc5cb9d50c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33435295"
---
# <a name="iclrassemblyreferencelist-interface"></a><span data-ttu-id="cf744-102">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="cf744-102">ICLRAssemblyReferenceList Interface</span></span>
<span data-ttu-id="cf744-103">Gère une liste d’assemblys qui sont chargés par le common language runtime (CLR) et non par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="cf744-103">Manages a list of assemblies that are loaded by the common language runtime (CLR) and not by the host.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="cf744-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cf744-104">Methods</span></span>  
  
|<span data-ttu-id="cf744-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="cf744-105">Method</span></span>|<span data-ttu-id="cf744-106">Description</span><span class="sxs-lookup"><span data-stu-id="cf744-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="cf744-107">IsAssemblyReferenceInList, méthode</span><span class="sxs-lookup"><span data-stu-id="cf744-107">IsAssemblyReferenceInList Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-isassemblyreferenceinlist-method.md)|<span data-ttu-id="cf744-108">Obtient une valeur qui indique si le pointeur fourni fait référence à un assembly dans la liste.</span><span class="sxs-lookup"><span data-stu-id="cf744-108">Gets a value that indicates whether the supplied pointer references an assembly in the list.</span></span>|  
|[<span data-ttu-id="cf744-109">IsStringAssemblyReferenceInList, méthode</span><span class="sxs-lookup"><span data-stu-id="cf744-109">IsStringAssemblyReferenceInList Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-isstringassemblyreferenceinlist-method.md)|<span data-ttu-id="cf744-110">Obtient une valeur qui indique si le nom fourni correspond au nom d’un assembly dans la liste.</span><span class="sxs-lookup"><span data-stu-id="cf744-110">Gets a value that indicates whether the supplied name matches the name of an assembly in the list.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cf744-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cf744-111">Remarks</span></span>  
 <span data-ttu-id="cf744-112">Appelez le [ICLRAssemblyIdentityManager::GetCLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-getclrassemblyreferencelist-method.md) pour obtenir un pointeur vers une instance de méthode `ICLRAssemblyReferenceList`.</span><span class="sxs-lookup"><span data-stu-id="cf744-112">Call the [ICLRAssemblyIdentityManager::GetCLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-getclrassemblyreferencelist-method.md) method to get a pointer to an instance of `ICLRAssemblyReferenceList`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cf744-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cf744-113">Requirements</span></span>  
 <span data-ttu-id="cf744-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cf744-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cf744-115">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="cf744-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="cf744-116">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cf744-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cf744-117">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cf744-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cf744-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf744-118">See Also</span></span>  
 [<span data-ttu-id="cf744-119">ICLRAssemblyIdentityManager, interface</span><span class="sxs-lookup"><span data-stu-id="cf744-119">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)  
 [<span data-ttu-id="cf744-120">IHostAssemblyStore, interface</span><span class="sxs-lookup"><span data-stu-id="cf744-120">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)  
 [<span data-ttu-id="cf744-121">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="cf744-121">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
