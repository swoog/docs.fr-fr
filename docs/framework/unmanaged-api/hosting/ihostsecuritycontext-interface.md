---
title: IHostSecurityContext, interface
ms.date: 03/30/2017
api_name:
- IHostSecurityContext
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityContext
helpviewer_keywords:
- IHostSecurityContext interface [.NET Framework hosting]
ms.assetid: 88e2eac0-8ccb-404f-abbc-287d55159842
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2c2500f013584ef4722ceaaaee91d5db54991639
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33439297"
---
# <a name="ihostsecuritycontext-interface"></a><span data-ttu-id="a24f9-102">IHostSecurityContext, interface</span><span class="sxs-lookup"><span data-stu-id="a24f9-102">IHostSecurityContext Interface</span></span>
<span data-ttu-id="a24f9-103">Permet le common language runtime (CLR) pour gérer les informations de contexte de sécurité implémentées par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="a24f9-103">Allows the common language runtime (CLR) to maintain security context information implemented by the host.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a24f9-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a24f9-104">Methods</span></span>  
  
|<span data-ttu-id="a24f9-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="a24f9-105">Method</span></span>|<span data-ttu-id="a24f9-106">Description</span><span class="sxs-lookup"><span data-stu-id="a24f9-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a24f9-107">Capture, méthode</span><span class="sxs-lookup"><span data-stu-id="a24f9-107">Capture Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-capture-method.md)|<span data-ttu-id="a24f9-108">Obtient un clone de le `IHostSecurityContext` instance retournée à partir d’un appel à [IHostSecurityManager::GetSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-getsecuritycontext-method.md).</span><span class="sxs-lookup"><span data-stu-id="a24f9-108">Gets a clone of the `IHostSecurityContext` instance returned from a call to [IHostSecurityManager::GetSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-getsecuritycontext-method.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a24f9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a24f9-109">Remarks</span></span>  
 <span data-ttu-id="a24f9-110">Un hôte peut contrôler tous les accès du code aux jetons de threads par le CLR et l’utilisateur du code.</span><span class="sxs-lookup"><span data-stu-id="a24f9-110">A host can control all code access to thread tokens by both the CLR and user code.</span></span> <span data-ttu-id="a24f9-111">Il peut également garantir que la sécurité complète les informations de contexte sont passées aux opérations asynchrones ou des points de code avec accès restreint au code.</span><span class="sxs-lookup"><span data-stu-id="a24f9-111">It can also ensure that complete security context information is passed across asynchronous operations or code points with restricted code access.</span></span> <span data-ttu-id="a24f9-112">`IHostSecurityContext` encapsule ces informations de contexte de sécurité, qui sont opaques pour le runtime.</span><span class="sxs-lookup"><span data-stu-id="a24f9-112">`IHostSecurityContext` encapsulates this security context information, which is opaque to the runtime.</span></span> <span data-ttu-id="a24f9-113">Le runtime intercepte cette information à l’aide de `Capture`, et les déplace dans la répartition d’élément de travail de pool de threads, l’exécution du finaliseur et les constructeurs de module et de classe.</span><span class="sxs-lookup"><span data-stu-id="a24f9-113">The runtime captures this information using `Capture`, and moves it across thread pool worker item dispatch, finalizer execution, and module and class constructors.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a24f9-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a24f9-114">Requirements</span></span>  
 <span data-ttu-id="a24f9-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a24f9-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a24f9-116">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a24f9-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a24f9-117">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a24f9-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a24f9-118">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a24f9-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a24f9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a24f9-119">See Also</span></span>  
 [<span data-ttu-id="a24f9-120">ICLRHostProtectionManager, interface</span><span class="sxs-lookup"><span data-stu-id="a24f9-120">ICLRHostProtectionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-interface.md)  
 [<span data-ttu-id="a24f9-121">IHostSecurityManager, interface</span><span class="sxs-lookup"><span data-stu-id="a24f9-121">IHostSecurityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-interface.md)  
 [<span data-ttu-id="a24f9-122">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="a24f9-122">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
