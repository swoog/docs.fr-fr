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
ms.openlocfilehash: 43c40e833e3a250239e9e90667196a2a74a96e0b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59187653"
---
# <a name="iclrassemblyreferencelist-interface"></a><span data-ttu-id="a188f-102">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="a188f-102">ICLRAssemblyReferenceList Interface</span></span>
<span data-ttu-id="a188f-103">Gère une liste d’assemblys qui sont chargés par le common language runtime (CLR) et non par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="a188f-103">Manages a list of assemblies that are loaded by the common language runtime (CLR) and not by the host.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a188f-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a188f-104">Methods</span></span>  
  
|<span data-ttu-id="a188f-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="a188f-105">Method</span></span>|<span data-ttu-id="a188f-106">Description</span><span class="sxs-lookup"><span data-stu-id="a188f-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a188f-107">IsAssemblyReferenceInList, méthode</span><span class="sxs-lookup"><span data-stu-id="a188f-107">IsAssemblyReferenceInList Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-isassemblyreferenceinlist-method.md)|<span data-ttu-id="a188f-108">Obtient une valeur qui indique si le pointeur fourni fait référence à un assembly dans la liste.</span><span class="sxs-lookup"><span data-stu-id="a188f-108">Gets a value that indicates whether the supplied pointer references an assembly in the list.</span></span>|  
|[<span data-ttu-id="a188f-109">IsStringAssemblyReferenceInList, méthode</span><span class="sxs-lookup"><span data-stu-id="a188f-109">IsStringAssemblyReferenceInList Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-isstringassemblyreferenceinlist-method.md)|<span data-ttu-id="a188f-110">Obtient une valeur qui indique si le nom fourni correspond au nom d’un assembly dans la liste.</span><span class="sxs-lookup"><span data-stu-id="a188f-110">Gets a value that indicates whether the supplied name matches the name of an assembly in the list.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a188f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a188f-111">Remarks</span></span>  
 <span data-ttu-id="a188f-112">Appelez le [ICLRAssemblyIdentityManager::GetCLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-getclrassemblyreferencelist-method.md) méthode pour obtenir un pointeur vers une instance de `ICLRAssemblyReferenceList`.</span><span class="sxs-lookup"><span data-stu-id="a188f-112">Call the [ICLRAssemblyIdentityManager::GetCLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-getclrassemblyreferencelist-method.md) method to get a pointer to an instance of `ICLRAssemblyReferenceList`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a188f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a188f-113">Requirements</span></span>  
 <span data-ttu-id="a188f-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a188f-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a188f-115">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a188f-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a188f-116">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a188f-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="a188f-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="a188f-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="a188f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a188f-118">See also</span></span>

- [<span data-ttu-id="a188f-119">ICLRAssemblyIdentityManager, interface</span><span class="sxs-lookup"><span data-stu-id="a188f-119">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="a188f-120">IHostAssemblyStore, interface</span><span class="sxs-lookup"><span data-stu-id="a188f-120">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
- [<span data-ttu-id="a188f-121">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="a188f-121">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
