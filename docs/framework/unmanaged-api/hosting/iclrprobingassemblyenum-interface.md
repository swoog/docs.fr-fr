---
title: ICLRProbingAssemblyEnum, interface
ms.date: 03/30/2017
api_name:
- ICLRProbingAssemblyEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRProbingAssemblyEnum
helpviewer_keywords:
- ICLRProbingAssemblyEnum interface [.NET Framework hosting]
ms.assetid: e7d3ccab-b0f0-4872-8935-0ed72920171b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 118345f246de3d7ee68d51cf37e8cdea9de1fdba
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61638526"
---
# <a name="iclrprobingassemblyenum-interface"></a><span data-ttu-id="8739e-102">ICLRProbingAssemblyEnum, interface</span><span class="sxs-lookup"><span data-stu-id="8739e-102">ICLRProbingAssemblyEnum Interface</span></span>
<span data-ttu-id="8739e-103">Fournit des méthodes qui permettent à l’hôte obtenir les identités d’identification d’un assembly à l’aide des informations d’identité de l’assembly qui est internes pour le common language runtime (CLR), sans avoir à créer ou à comprendre cette identité.</span><span class="sxs-lookup"><span data-stu-id="8739e-103">Provides methods that enable the host to get the probing identities of an assembly by using the assembly's identity information that is internal to the common language runtime (CLR), without needing to create or understand that identity.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8739e-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8739e-104">Methods</span></span>  
  
|<span data-ttu-id="8739e-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="8739e-105">Method</span></span>|<span data-ttu-id="8739e-106">Description</span><span class="sxs-lookup"><span data-stu-id="8739e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8739e-107">Get, méthode</span><span class="sxs-lookup"><span data-stu-id="8739e-107">Get Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrprobingassemblyenum-get-method.md)|<span data-ttu-id="8739e-108">Obtient l’identité d’assembly à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="8739e-108">Gets the assembly identity at the specified index.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8739e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="8739e-109">Remarks</span></span>  
 <span data-ttu-id="8739e-110">Méthodes telles que [ICLRAssemblyIdentityManager::GetProbingAssembliesFromReference](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-getprobingassembliesfromreference-method.md) retourner un `ICLRProbingAssemblyEnum` instance.</span><span class="sxs-lookup"><span data-stu-id="8739e-110">Methods such as [ICLRAssemblyIdentityManager::GetProbingAssembliesFromReference](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-getprobingassembliesfromreference-method.md) return an `ICLRProbingAssemblyEnum` instance.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8739e-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8739e-111">Requirements</span></span>  
 <span data-ttu-id="8739e-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8739e-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8739e-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="8739e-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8739e-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8739e-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8739e-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8739e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8739e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8739e-116">See also</span></span>

- [<span data-ttu-id="8739e-117">ICLRAssemblyIdentityManager, interface</span><span class="sxs-lookup"><span data-stu-id="8739e-117">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="8739e-118">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="8739e-118">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="8739e-119">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="8739e-119">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
