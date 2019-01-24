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
ms.openlocfilehash: 98a2978b440e0e72b3b4c1ac3065fbaf5d70e508
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54666096"
---
# <a name="iclrhostbindingpolicymanager-interface"></a><span data-ttu-id="bcc8c-102">ICLRHostBindingPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="bcc8c-102">ICLRHostBindingPolicyManager Interface</span></span>
<span data-ttu-id="bcc8c-103">Fournit des méthodes pour l’hôte évaluer la stratégie de liaison actuelle et de communiquer les modifications de stratégie pour un assembly spécifié.</span><span class="sxs-lookup"><span data-stu-id="bcc8c-103">Provides methods for the host to evaluate current binding policy and communicate policy changes for a specified assembly.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="bcc8c-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bcc8c-104">Methods</span></span>  
  
|<span data-ttu-id="bcc8c-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="bcc8c-105">Method</span></span>|<span data-ttu-id="bcc8c-106">Description</span><span class="sxs-lookup"><span data-stu-id="bcc8c-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="bcc8c-107">EvaluatePolicy, méthode</span><span class="sxs-lookup"><span data-stu-id="bcc8c-107">EvaluatePolicy Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-evaluatepolicy-method.md)|<span data-ttu-id="bcc8c-108">Évalue la stratégie de liaison pour le compte de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="bcc8c-108">Evaluates binding policy on behalf of the host.</span></span>|  
|[<span data-ttu-id="bcc8c-109">ModifyApplicationPolicy, méthode</span><span class="sxs-lookup"><span data-stu-id="bcc8c-109">ModifyApplicationPolicy Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-modifyapplicationpolicy-method.md)|<span data-ttu-id="bcc8c-110">Modifie la stratégie de liaison pour l’assembly spécifié et crée une nouvelle version de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="bcc8c-110">Modifies the binding policy for the specified assembly, and creates a new version of the policy.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="bcc8c-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bcc8c-111">Requirements</span></span>  
 <span data-ttu-id="bcc8c-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bcc8c-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bcc8c-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="bcc8c-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bcc8c-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bcc8c-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bcc8c-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bcc8c-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bcc8c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcc8c-116">See also</span></span>
- [<span data-ttu-id="bcc8c-117">ICLRAssemblyIdentityManager, interface</span><span class="sxs-lookup"><span data-stu-id="bcc8c-117">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="bcc8c-118">IHostAssemblyStore, interface</span><span class="sxs-lookup"><span data-stu-id="bcc8c-118">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
- [<span data-ttu-id="bcc8c-119">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="bcc8c-119">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
