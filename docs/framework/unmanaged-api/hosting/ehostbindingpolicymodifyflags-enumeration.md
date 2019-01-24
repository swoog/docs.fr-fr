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
ms.openlocfilehash: b3aba84f1ae451ee943028d063e91ca7a6d63548
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54504692"
---
# <a name="ehostbindingpolicymodifyflags-enumeration"></a><span data-ttu-id="72126-102">EHostBindingPolicyModifyFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="72126-102">EHostBindingPolicyModifyFlags Enumeration</span></span>
<span data-ttu-id="72126-103">Permet à l’hôte spécifier le type de redirection que le common language runtime (CLR) doit effectuer lors de l’application des changements de stratégie à partir d’un assembly source vers un assembly cible.</span><span class="sxs-lookup"><span data-stu-id="72126-103">Allows the host to specify the type of redirection the common language runtime (CLR) should perform when applying policy modifications from a source assembly to a target assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="72126-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72126-104">Syntax</span></span>  
  
```  
typedef enum _hostBindingPolicyModifyFlags {  
    HOST_BINDING_POLICY_MODIFY_DEFAULT  = 0,  
    HOST_BINDING_POLICY_MODIFY_CHAIN    = 1,  
    HOST_BINDING_POLICY_MODIFY_REMOVE   = 2,  
    HOST_BINDING_POLICY_MODIFY_MAX      = 3  
} EHostBindingPolicyModifyFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="72126-105">Membres</span><span class="sxs-lookup"><span data-stu-id="72126-105">Members</span></span>  
  
|<span data-ttu-id="72126-106">Membre</span><span class="sxs-lookup"><span data-stu-id="72126-106">Member</span></span>|<span data-ttu-id="72126-107">Description</span><span class="sxs-lookup"><span data-stu-id="72126-107">Description</span></span>|  
|------------|-----------------|  
|`HOST_BINDING_POLICY_MODIFY_CHAIN`|<span data-ttu-id="72126-108">Spécifie que le CLR doit chaîner les valeurs de stratégie de l’assembly source vers ceux de l’assembly cible.</span><span class="sxs-lookup"><span data-stu-id="72126-108">Specifies that the CLR will chain policy values of the source assembly onto those of the target assembly.</span></span>|  
|`HOST_BINDING_POLICY_MODIFY_DEFAULT`|<span data-ttu-id="72126-109">Spécifie que le CLR va effectuer l’action par défaut.</span><span class="sxs-lookup"><span data-stu-id="72126-109">Specifies that the CLR will perform the default action.</span></span>|  
|`HOST_BINDING_POLICY_MODIFY_MAX`|<span data-ttu-id="72126-110">Spécifie que le CLR définit les valeurs de stratégie de l’assembly cible pour les valeurs maximales.</span><span class="sxs-lookup"><span data-stu-id="72126-110">Specifies that the CLR will set the policy values of the target assembly to the maximum values.</span></span>|  
|`HOST_BINDING_POLICY_MODIFY_REMOVE`|<span data-ttu-id="72126-111">Spécifie que le CLR doit remplacer les valeurs de stratégie de l’assembly cible avec ceux de l’assembly source.</span><span class="sxs-lookup"><span data-stu-id="72126-111">Specifies that the CLR will replace policy values of the target assembly with those of the source assembly.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="72126-112">Notes</span><span class="sxs-lookup"><span data-stu-id="72126-112">Remarks</span></span>  
 <span data-ttu-id="72126-113">Le [ICLRHostBindingPolicyManager::ModifyApplicationPolicy](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-modifyapplicationpolicy-method.md) méthode prend un paramètre de type `EHostBindingPolicyModifyFlags`.</span><span class="sxs-lookup"><span data-stu-id="72126-113">The [ICLRHostBindingPolicyManager::ModifyApplicationPolicy](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-modifyapplicationpolicy-method.md) method takes a parameter of type `EHostBindingPolicyModifyFlags`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="72126-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="72126-114">Requirements</span></span>  
 <span data-ttu-id="72126-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="72126-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="72126-116">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="72126-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="72126-117">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="72126-117">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="72126-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="72126-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="72126-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72126-119">See also</span></span>
- [<span data-ttu-id="72126-120">ICLRHostBindingPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="72126-120">ICLRHostBindingPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-interface.md)
- [<span data-ttu-id="72126-121">Énumérations d’hébergement</span><span class="sxs-lookup"><span data-stu-id="72126-121">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
