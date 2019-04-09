---
title: IHostControl, interface
ms.date: 03/30/2017
api_name:
- IHostControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostControl
helpviewer_keywords:
- IHostControl interface [.NET Framework hosting]
ms.assetid: a4ae0d1f-ade9-4b0a-a122-93ed11a5e6b3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 014e5c9951091046ae07374794743e82affcd5ad
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59122263"
---
# <a name="ihostcontrol-interface"></a><span data-ttu-id="04520-102">IHostControl, interface</span><span class="sxs-lookup"><span data-stu-id="04520-102">IHostControl Interface</span></span>
<span data-ttu-id="04520-103">Fournit des méthodes pour configurer le chargement d’assemblys et pour déterminer quelles interfaces d’hébergement le prend en charge de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="04520-103">Provides methods for configuring the loading of assemblies, and for determining which hosting interfaces the host supports.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="04520-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="04520-104">Methods</span></span>  
  
|<span data-ttu-id="04520-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="04520-105">Method</span></span>|<span data-ttu-id="04520-106">Description</span><span class="sxs-lookup"><span data-stu-id="04520-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="04520-107">GetHostManager, méthode</span><span class="sxs-lookup"><span data-stu-id="04520-107">GetHostManager Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-gethostmanager-method.md)|<span data-ttu-id="04520-108">Obtient un pointeur d’interface vers l’implémentation de l’hôte de l’interface avec la valeur `IID`.</span><span class="sxs-lookup"><span data-stu-id="04520-108">Gets an interface pointer to the host's implementation of the interface with the specified `IID`.</span></span>|  
|[<span data-ttu-id="04520-109">SetAppDomainManager, méthode</span><span class="sxs-lookup"><span data-stu-id="04520-109">SetAppDomainManager Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-setappdomainmanager-method.md)|<span data-ttu-id="04520-110">Avertit l’hôte qu’un domaine d’application a été créé.</span><span class="sxs-lookup"><span data-stu-id="04520-110">Notifies the host that an application domain has been created.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="04520-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04520-111">Requirements</span></span>  
 <span data-ttu-id="04520-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="04520-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="04520-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="04520-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="04520-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="04520-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="04520-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="04520-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="04520-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04520-116">See also</span></span>

- <xref:System.AppDomainManager>
- [<span data-ttu-id="04520-117">ICLRRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="04520-117">ICLRRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)
- [<span data-ttu-id="04520-118">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="04520-118">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
- [<span data-ttu-id="04520-119">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="04520-119">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
