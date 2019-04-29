---
title: METAHOST_CONFIG_FLAGS, énumération
ms.date: 03/30/2017
api_name:
- METAHOST_CONFIG_FLAGS
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- METAHOST_CONFIG_FLAGS
helpviewer_keywords:
- METAHOST_CONFIG_FLAGS enumeration [.NET Framework hosting]
ms.assetid: 6f1e389f-ed99-4d6a-a0ba-72d7d869a01d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6e322f5c7119d13c8a872bd87d00c1e55324b581
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61765191"
---
# <a name="metahostconfigflags-enumeration"></a><span data-ttu-id="ffabe-102">METAHOST_CONFIG_FLAGS, énumération</span><span class="sxs-lookup"><span data-stu-id="ffabe-102">METAHOST_CONFIG_FLAGS Enumeration</span></span>
<span data-ttu-id="ffabe-103">Décrit les indicateurs possibles retournés dans le `pdwConfigFlags` paramètre de la [ICLRMetaHostPolicy::GetRequestedRuntime](../../../../docs/framework/unmanaged-api/hosting/iclrmetahostpolicy-getrequestedruntime-method.md) (méthode), indiquant la présence et le paramètre de la `useLegacyV2RuntimeActivationPolicy` d’attribut dans le [ \<démarrage > élément](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md) du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="ffabe-103">Describes the possible flags returned in the `pdwConfigFlags` parameter of the [ICLRMetaHostPolicy::GetRequestedRuntime](../../../../docs/framework/unmanaged-api/hosting/iclrmetahostpolicy-getrequestedruntime-method.md) method, indicating the presence and setting of the `useLegacyV2RuntimeActivationPolicy` attribute in the [\<startup> element](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md) of the configuration file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ffabe-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffabe-104">Syntax</span></span>  
  
```  
typedef enum {  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_UNSET  = 0x00,  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_TRUE   = 0x01,  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_FALSE  = 0x02,  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_MASK   = 0x03  
} METAHOST_CONFIG_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="ffabe-105">Membres</span><span class="sxs-lookup"><span data-stu-id="ffabe-105">Members</span></span>  
  
|<span data-ttu-id="ffabe-106">Membre</span><span class="sxs-lookup"><span data-stu-id="ffabe-106">Member</span></span>|<span data-ttu-id="ffabe-107">Description</span><span class="sxs-lookup"><span data-stu-id="ffabe-107">Description</span></span>|  
|------------|-----------------|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_UNSET`|<span data-ttu-id="ffabe-108">Le `useLegacyV2RuntimeActivationPolicy` attribut n’était pas présent dans le [ \<démarrage > élément](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md).</span><span class="sxs-lookup"><span data-stu-id="ffabe-108">The `useLegacyV2RuntimeActivationPolicy` attribute was not present in the [\<startup> Element](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md).</span></span>|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_TRUE`|<span data-ttu-id="ffabe-109">Le `useLegacyV2RuntimeActivationPolicy` attribut était présent et défini à `true`.</span><span class="sxs-lookup"><span data-stu-id="ffabe-109">The `useLegacyV2RuntimeActivationPolicy` attribute was present and set to `true`.</span></span>|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_FALSE`|<span data-ttu-id="ffabe-110">Le `useLegacyV2RuntimeActivationPolicy` attribut était présent et défini à `false`.</span><span class="sxs-lookup"><span data-stu-id="ffabe-110">The `useLegacyV2RuntimeActivationPolicy` attribute was present and set to `false`.</span></span>|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_MASK`|<span data-ttu-id="ffabe-111">Appliquez ce masque à la valeur retournée dans `pdwConfigFlags` pour obtenir les valeurs pertinentes à `useLegacyV2RuntimeActivationPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ffabe-111">Apply this mask to the value returned in `pdwConfigFlags` to get the values relevant to `useLegacyV2RuntimeActivationPolicy`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ffabe-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ffabe-112">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ffabe-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffabe-113">Requirements</span></span>  
 <span data-ttu-id="ffabe-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ffabe-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ffabe-115">**En-tête :** Metahost.h</span><span class="sxs-lookup"><span data-stu-id="ffabe-115">**Header:** Metahost.h</span></span>  
  
 <span data-ttu-id="ffabe-116">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ffabe-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ffabe-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ffabe-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ffabe-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffabe-118">See also</span></span>

- [<span data-ttu-id="ffabe-119">Énumérations d’hébergement</span><span class="sxs-lookup"><span data-stu-id="ffabe-119">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
- [<span data-ttu-id="ffabe-120">GetRequestedRuntime, méthode</span><span class="sxs-lookup"><span data-stu-id="ffabe-120">GetRequestedRuntime Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahostpolicy-getrequestedruntime-method.md)
- [<span data-ttu-id="ffabe-121">\<startup>, élément</span><span class="sxs-lookup"><span data-stu-id="ffabe-121">\<startup> Element</span></span>](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md)
