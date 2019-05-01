---
title: ICLRAssemblyIdentityManager, interface
ms.date: 03/30/2017
api_name:
- ICLRAssemblyIdentityManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyIdentityManager
helpviewer_keywords:
- ICLRAssemblyIdentityManager interface [.NET Framework hosting]
ms.assetid: 6a81c6fe-cc22-4062-ae27-d6eeee03a7b9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2b209e568b1e65ed785155d045cd48d1248672da
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61985034"
---
# <a name="iclrassemblyidentitymanager-interface"></a><span data-ttu-id="1a7e1-102">ICLRAssemblyIdentityManager, interface</span><span class="sxs-lookup"><span data-stu-id="1a7e1-102">ICLRAssemblyIdentityManager Interface</span></span>
<span data-ttu-id="1a7e1-103">Fournit des méthodes qui prennent en charge la communication entre l’hôte et le common language runtime (CLR) sur les assemblys.</span><span class="sxs-lookup"><span data-stu-id="1a7e1-103">Provides methods that support communication between the host and the common language runtime (CLR) about assemblies.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1a7e1-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1a7e1-104">Methods</span></span>  
  
|<span data-ttu-id="1a7e1-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="1a7e1-105">Method</span></span>|<span data-ttu-id="1a7e1-106">Description</span><span class="sxs-lookup"><span data-stu-id="1a7e1-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1a7e1-107">GetBindingIdentityFromFile, méthode</span><span class="sxs-lookup"><span data-stu-id="1a7e1-107">GetBindingIdentityFromFile Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-getbindingidentityfromfile-method.md)|<span data-ttu-id="1a7e1-108">Obtient l’identité d’assembly une liaison de données pour l’assembly dans le chemin d’accès de fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="1a7e1-108">Gets the assembly identity binding data for the assembly at the specified file path.</span></span>|  
|[<span data-ttu-id="1a7e1-109">GetBindingIdentityFromStream, méthode</span><span class="sxs-lookup"><span data-stu-id="1a7e1-109">GetBindingIdentityFromStream Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-getbindingidentityfromstream-method.md)|<span data-ttu-id="1a7e1-110">Obtient les données d’identité canonique de l’assembly dans le flux spécifié.</span><span class="sxs-lookup"><span data-stu-id="1a7e1-110">Gets the canonical assembly identity data for the assembly in the specified stream.</span></span>|  
|[<span data-ttu-id="1a7e1-111">GetCLRAssemblyReferenceList, méthode</span><span class="sxs-lookup"><span data-stu-id="1a7e1-111">GetCLRAssemblyReferenceList Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-getclrassemblyreferencelist-method.md)|<span data-ttu-id="1a7e1-112">Obtient un [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) instance à partir de la liste fournie d’identités d’assembly partielles.</span><span class="sxs-lookup"><span data-stu-id="1a7e1-112">Gets an [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) instance from the supplied list of partial assembly identities.</span></span>|  
|[<span data-ttu-id="1a7e1-113">GetProbingAssembliesFromReference, méthode</span><span class="sxs-lookup"><span data-stu-id="1a7e1-113">GetProbingAssembliesFromReference Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-getprobingassembliesfromreference-method.md)|<span data-ttu-id="1a7e1-114">Obtient un [ICLRProbingAssemblyEnum](../../../../docs/framework/unmanaged-api/hosting/iclrprobingassemblyenum-interface.md) énumérateur pour les identités d’assembly référencé par l’assembly avec l’identité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1a7e1-114">Gets an [ICLRProbingAssemblyEnum](../../../../docs/framework/unmanaged-api/hosting/iclrprobingassemblyenum-interface.md) enumerator for the assembly identities referenced by the assembly with the specified identity.</span></span>|  
|[<span data-ttu-id="1a7e1-115">GetReferencedAssembliesFromFile, méthode</span><span class="sxs-lookup"><span data-stu-id="1a7e1-115">GetReferencedAssembliesFromFile Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-getreferencedassembliesfromfile-method.md)|<span data-ttu-id="1a7e1-116">Obtient un [ICLRReferenceAssemblyEnum](../../../../docs/framework/unmanaged-api/hosting/iclrreferenceassemblyenum-interface.md) instance qui contient une liste des assemblys référencés par l’assembly dans le chemin d’accès de fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="1a7e1-116">Gets an [ICLRReferenceAssemblyEnum](../../../../docs/framework/unmanaged-api/hosting/iclrreferenceassemblyenum-interface.md) instance that contains a list of assemblies referenced by the assembly at the specified file path.</span></span>|  
|[<span data-ttu-id="1a7e1-117">GetReferencedAssembliesFromStream, méthode</span><span class="sxs-lookup"><span data-stu-id="1a7e1-117">GetReferencedAssembliesFromStream Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-getreferencedassembliesfromstream-method.md)|<span data-ttu-id="1a7e1-118">Obtient un pointeur vers un `ICLRReferenceAssemblyEnum` objet qui contient les données d’identité pour les assemblys référencés par l’assembly dans le flux spécifié.</span><span class="sxs-lookup"><span data-stu-id="1a7e1-118">Gets a pointer to an `ICLRReferenceAssemblyEnum` object that contains assembly identity data for the assemblies referenced by the assembly in the specified stream.</span></span>|  
|[<span data-ttu-id="1a7e1-119">IsStronglyNamed, méthode</span><span class="sxs-lookup"><span data-stu-id="1a7e1-119">IsStronglyNamed Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-isstronglynamed-method.md)|<span data-ttu-id="1a7e1-120">Obtient une valeur qui indique si l’assembly spécifié est un nom fort.</span><span class="sxs-lookup"><span data-stu-id="1a7e1-120">Gets a value that indicates whether the specified assembly is strongly named.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1a7e1-121">Notes</span><span class="sxs-lookup"><span data-stu-id="1a7e1-121">Remarks</span></span>  
 <span data-ttu-id="1a7e1-122">Utilisez `ICLRAssemblyIdentityManager` pour obtenir des instances de `ICLRAssemblyReferenceList` et énumérer des identités d’assembly.</span><span class="sxs-lookup"><span data-stu-id="1a7e1-122">Use `ICLRAssemblyIdentityManager` to get instances of `ICLRAssemblyReferenceList` and to enumerate assembly identities.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1a7e1-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a7e1-123">Requirements</span></span>  
 <span data-ttu-id="1a7e1-124">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1a7e1-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1a7e1-125">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="1a7e1-125">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1a7e1-126">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1a7e1-126">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1a7e1-127">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1a7e1-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a7e1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a7e1-128">See also</span></span>

- [<span data-ttu-id="1a7e1-129">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="1a7e1-129">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="1a7e1-130">ICLRProbingAssemblyEnum, interface</span><span class="sxs-lookup"><span data-stu-id="1a7e1-130">ICLRProbingAssemblyEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrprobingassemblyenum-interface.md)
- [<span data-ttu-id="1a7e1-131">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="1a7e1-131">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
