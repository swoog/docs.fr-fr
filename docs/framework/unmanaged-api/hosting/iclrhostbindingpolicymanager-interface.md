---
title: ICLRHostBindingPolicyManager, interface
ms.date: 03/30/2017
api_name:
- ICLRHostBindingPolicyManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRHostBindingPolicyManager
helpviewer_keywords:
- ICLRHostBindingPolicyManager interface [.NET Framework hosting]
ms.assetid: f9da168b-366b-4b2b-bdb9-330b6bad5a6b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e494bbbd08a77329b7b64816216e4bb2e1b724a2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59074194"
---
# <a name="iclrhostbindingpolicymanager-interface"></a><span data-ttu-id="d4e69-102">ICLRHostBindingPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="d4e69-102">ICLRHostBindingPolicyManager Interface</span></span>
<span data-ttu-id="d4e69-103">Fournit des méthodes pour l’hôte évaluer la stratégie de liaison actuelle et de communiquer les modifications de stratégie pour un assembly spécifié.</span><span class="sxs-lookup"><span data-stu-id="d4e69-103">Provides methods for the host to evaluate current binding policy and communicate policy changes for a specified assembly.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d4e69-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d4e69-104">Methods</span></span>  
  
|<span data-ttu-id="d4e69-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="d4e69-105">Method</span></span>|<span data-ttu-id="d4e69-106">Description</span><span class="sxs-lookup"><span data-stu-id="d4e69-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d4e69-107">EvaluatePolicy, méthode</span><span class="sxs-lookup"><span data-stu-id="d4e69-107">EvaluatePolicy Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-evaluatepolicy-method.md)|<span data-ttu-id="d4e69-108">Évalue la stratégie de liaison pour le compte de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="d4e69-108">Evaluates binding policy on behalf of the host.</span></span>|  
|[<span data-ttu-id="d4e69-109">ModifyApplicationPolicy, méthode</span><span class="sxs-lookup"><span data-stu-id="d4e69-109">ModifyApplicationPolicy Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-modifyapplicationpolicy-method.md)|<span data-ttu-id="d4e69-110">Modifie la stratégie de liaison pour l’assembly spécifié et crée une nouvelle version de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="d4e69-110">Modifies the binding policy for the specified assembly, and creates a new version of the policy.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d4e69-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4e69-111">Requirements</span></span>  
 <span data-ttu-id="d4e69-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d4e69-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d4e69-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="d4e69-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d4e69-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d4e69-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d4e69-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d4e69-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d4e69-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4e69-116">See also</span></span>

- [<span data-ttu-id="d4e69-117">ICLRAssemblyIdentityManager, interface</span><span class="sxs-lookup"><span data-stu-id="d4e69-117">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="d4e69-118">IHostAssemblyStore, interface</span><span class="sxs-lookup"><span data-stu-id="d4e69-118">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
- [<span data-ttu-id="d4e69-119">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="d4e69-119">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
