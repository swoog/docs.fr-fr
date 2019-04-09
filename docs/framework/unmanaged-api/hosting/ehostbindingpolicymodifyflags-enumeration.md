---
title: EHostBindingPolicyModifyFlags, énumération
ms.date: 03/30/2017
api_name:
- EHostBindingPolicyModifyFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EHostBindingPolicyModifyFlags
helpviewer_keywords:
- EHostBindingPolicyModifyFlags enumeration [.NET Framework hosting]
ms.assetid: 0339af16-ee1d-48ec-837d-a79d9a9c89f8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0e8357d20edba993f5a7682f31c04afea4362afd
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59080213"
---
# <a name="ehostbindingpolicymodifyflags-enumeration"></a><span data-ttu-id="5b356-102">EHostBindingPolicyModifyFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="5b356-102">EHostBindingPolicyModifyFlags Enumeration</span></span>
<span data-ttu-id="5b356-103">Permet à l’hôte spécifier le type de redirection que le common language runtime (CLR) doit effectuer lors de l’application des changements de stratégie à partir d’un assembly source vers un assembly cible.</span><span class="sxs-lookup"><span data-stu-id="5b356-103">Allows the host to specify the type of redirection the common language runtime (CLR) should perform when applying policy modifications from a source assembly to a target assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5b356-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b356-104">Syntax</span></span>  
  
```  
typedef enum _hostBindingPolicyModifyFlags {  
    HOST_BINDING_POLICY_MODIFY_DEFAULT  = 0,  
    HOST_BINDING_POLICY_MODIFY_CHAIN    = 1,  
    HOST_BINDING_POLICY_MODIFY_REMOVE   = 2,  
    HOST_BINDING_POLICY_MODIFY_MAX      = 3  
} EHostBindingPolicyModifyFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="5b356-105">Membres</span><span class="sxs-lookup"><span data-stu-id="5b356-105">Members</span></span>  
  
|<span data-ttu-id="5b356-106">Membre</span><span class="sxs-lookup"><span data-stu-id="5b356-106">Member</span></span>|<span data-ttu-id="5b356-107">Description</span><span class="sxs-lookup"><span data-stu-id="5b356-107">Description</span></span>|  
|------------|-----------------|  
|`HOST_BINDING_POLICY_MODIFY_CHAIN`|<span data-ttu-id="5b356-108">Spécifie que le CLR doit chaîner les valeurs de stratégie de l’assembly source vers ceux de l’assembly cible.</span><span class="sxs-lookup"><span data-stu-id="5b356-108">Specifies that the CLR will chain policy values of the source assembly onto those of the target assembly.</span></span>|  
|`HOST_BINDING_POLICY_MODIFY_DEFAULT`|<span data-ttu-id="5b356-109">Spécifie que le CLR va effectuer l’action par défaut.</span><span class="sxs-lookup"><span data-stu-id="5b356-109">Specifies that the CLR will perform the default action.</span></span>|  
|`HOST_BINDING_POLICY_MODIFY_MAX`|<span data-ttu-id="5b356-110">Spécifie que le CLR définit les valeurs de stratégie de l’assembly cible pour les valeurs maximales.</span><span class="sxs-lookup"><span data-stu-id="5b356-110">Specifies that the CLR will set the policy values of the target assembly to the maximum values.</span></span>|  
|`HOST_BINDING_POLICY_MODIFY_REMOVE`|<span data-ttu-id="5b356-111">Spécifie que le CLR doit remplacer les valeurs de stratégie de l’assembly cible avec ceux de l’assembly source.</span><span class="sxs-lookup"><span data-stu-id="5b356-111">Specifies that the CLR will replace policy values of the target assembly with those of the source assembly.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5b356-112">Notes</span><span class="sxs-lookup"><span data-stu-id="5b356-112">Remarks</span></span>  
 <span data-ttu-id="5b356-113">Le [ICLRHostBindingPolicyManager::ModifyApplicationPolicy](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-modifyapplicationpolicy-method.md) méthode prend un paramètre de type `EHostBindingPolicyModifyFlags`.</span><span class="sxs-lookup"><span data-stu-id="5b356-113">The [ICLRHostBindingPolicyManager::ModifyApplicationPolicy](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-modifyapplicationpolicy-method.md) method takes a parameter of type `EHostBindingPolicyModifyFlags`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5b356-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b356-114">Requirements</span></span>  
 <span data-ttu-id="5b356-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5b356-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5b356-116">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="5b356-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5b356-117">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5b356-117">**Library:** MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="5b356-118">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="5b356-118">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="5b356-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b356-119">See also</span></span>

- [<span data-ttu-id="5b356-120">ICLRHostBindingPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="5b356-120">ICLRHostBindingPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-interface.md)
- [<span data-ttu-id="5b356-121">Énumérations d'hébergement</span><span class="sxs-lookup"><span data-stu-id="5b356-121">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
