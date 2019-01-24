---
title: ICLRDomainManager, interface
ms.date: 03/30/2017
api_name:
- ICLRDomainManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDomainManager
helpviewer_keywords:
- ICLRDomainManager interface [.NET Framework hosting]
ms.assetid: f08b2390-d872-4521-a815-e9c237c4c45d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 797b6031449672e8b610b2a53e77497e5835ea6a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54657426"
---
# <a name="iclrdomainmanager-interface"></a><span data-ttu-id="dce1d-102">ICLRDomainManager, interface</span><span class="sxs-lookup"><span data-stu-id="dce1d-102">ICLRDomainManager Interface</span></span>
<span data-ttu-id="dce1d-103">Permet à l’hôte spécifier le Gestionnaire de domaine d’application qui sera utilisé pour initialiser le domaine d’application par défaut et pour spécifier les propriétés d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="dce1d-103">Enables the host to specify the application domain manager that will be used to initialize the default application domain, and to specify initialization properties.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="dce1d-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dce1d-104">Methods</span></span>  
  
|<span data-ttu-id="dce1d-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="dce1d-105">Method</span></span>|<span data-ttu-id="dce1d-106">Description</span><span class="sxs-lookup"><span data-stu-id="dce1d-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="dce1d-107">SetAppDomainManagerType, méthode</span><span class="sxs-lookup"><span data-stu-id="dce1d-107">SetAppDomainManagerType Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdomainmanager-setappdomainmanagertype-method.md)|<span data-ttu-id="dce1d-108">Spécifie le type, dérivé de la <xref:System.AppDomainManager?displayProperty=nameWithType> classe, du Gestionnaire de domaine qui sera utilisé pour initialiser le domaine d’application par défaut.</span><span class="sxs-lookup"><span data-stu-id="dce1d-108">Specifies the type, derived from the <xref:System.AppDomainManager?displayProperty=nameWithType> class, of the application domain manager that will be used to initialize the default application domain.</span></span>|  
|[<span data-ttu-id="dce1d-109">SetPropertiesForDefaultAppDomain, méthode</span><span class="sxs-lookup"><span data-stu-id="dce1d-109">SetPropertiesForDefaultAppDomain Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdomainmanager-setpropertiesfordefaultappdomain-method.md)|<span data-ttu-id="dce1d-110">Définit les propriétés qui seront utilisées pour initialiser le domaine d’application par défaut.</span><span class="sxs-lookup"><span data-stu-id="dce1d-110">Sets properties that will be used to initialize the default application domain.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dce1d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="dce1d-111">Remarks</span></span>  
 <span data-ttu-id="dce1d-112">Pour obtenir une instance de cette interface, appelez le [ICLRControl::GetCLRManager](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md) méthode avec le type de gestionnaire IID `IID_ICLRDomainManager`.</span><span class="sxs-lookup"><span data-stu-id="dce1d-112">To get an instance of this interface, call the [ICLRControl::GetCLRManager](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md) method with the manager type IID `IID_ICLRDomainManager`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dce1d-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dce1d-113">Requirements</span></span>  
 <span data-ttu-id="dce1d-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dce1d-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dce1d-115">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="dce1d-115">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="dce1d-116">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="dce1d-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="dce1d-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dce1d-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dce1d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dce1d-118">See also</span></span>
- [<span data-ttu-id="dce1d-119">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="dce1d-119">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="dce1d-120">Hébergement</span><span class="sxs-lookup"><span data-stu-id="dce1d-120">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
