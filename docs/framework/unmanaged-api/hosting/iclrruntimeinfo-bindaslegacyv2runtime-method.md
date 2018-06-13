---
title: ICLRRuntimeInfo::BindAsLegacyV2Runtime, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.BindAsLegacyV2Runtime
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::BindAsLegacyV2Runtime
helpviewer_keywords:
- ICLRRuntimeInfo::BindAsLegacyV2Runtime method [.NET Framework hosting]
- BindAsLegacyV2Runtime method [.NET Framework hosting]
ms.assetid: 65fd55ac-4a24-4479-9384-a2e8013bfb2b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 690287bf54f98c19298504ee3058a59ef88a87f9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33433159"
---
# <a name="iclrruntimeinfobindaslegacyv2runtime-method"></a><span data-ttu-id="a2eaf-102">ICLRRuntimeInfo::BindAsLegacyV2Runtime, méthode</span><span class="sxs-lookup"><span data-stu-id="a2eaf-102">ICLRRuntimeInfo::BindAsLegacyV2Runtime Method</span></span>
<span data-ttu-id="a2eaf-103">Lie l’exécution actuelle pour tous les hérité common language runtime (CLR) version 2 d’activation aux décisions de stratégie.</span><span class="sxs-lookup"><span data-stu-id="a2eaf-103">Binds the current runtime for all legacy common language runtime (CLR) version 2 activation policy decisions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a2eaf-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2eaf-104">Syntax</span></span>  
  
```  
HRESULT BindAsLegacyV2Runtime ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="a2eaf-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a2eaf-105">Return Value</span></span>  
 <span data-ttu-id="a2eaf-106">Cette méthode retourne les HRESULT spécifiques suivants :</span><span class="sxs-lookup"><span data-stu-id="a2eaf-106">This method returns the following specific HRESULTs:</span></span>  
  
|<span data-ttu-id="a2eaf-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a2eaf-107">HRESULT</span></span>|<span data-ttu-id="a2eaf-108">Description</span><span class="sxs-lookup"><span data-stu-id="a2eaf-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a2eaf-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="a2eaf-109">S_OK</span></span>|<span data-ttu-id="a2eaf-110">Liaison a réussi, ou cette exécution a déjà été liée en tant que le runtime de stratégie CLR version 2 d’activation hérité.</span><span class="sxs-lookup"><span data-stu-id="a2eaf-110">Either binding succeeded, or this runtime was already bound as the legacy CLR version 2 activation policy runtime.</span></span>|  
|<span data-ttu-id="a2eaf-111">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span><span class="sxs-lookup"><span data-stu-id="a2eaf-111">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span></span>|<span data-ttu-id="a2eaf-112">Une exécution différente a déjà été liée à la stratégie d’activation 2 de version CLR héritée.</span><span class="sxs-lookup"><span data-stu-id="a2eaf-112">A different runtime was already bound to the legacy CLR version 2 activation policy.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a2eaf-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a2eaf-113">Remarks</span></span>  
 <span data-ttu-id="a2eaf-114">Si le runtime actuel est déjà lié à toutes les décisions de stratégie CLR version 2 d’activation héritées (par exemple, à l’aide de la `useLegacyV2RuntimeActivationPolicy` de l’attribut le [ \<démarrage > élément](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md) dans le fichier de configuration), cette méthode ne retourne pas de résultat d’erreur ; au lieu de cela, le résultat est S_OK, tout comme il le serait si la méthode avait été liée à une stratégie d’activation héritée.</span><span class="sxs-lookup"><span data-stu-id="a2eaf-114">If the current runtime is already bound for all legacy CLR version 2 activation policy decisions (for example, by using the `useLegacyV2RuntimeActivationPolicy` attribute on the [\<startup> element](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md) in the configuration file), this method does not return an error result; instead, the result is S_OK, just as it would be if the method had successfully bound legacy activation policy.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a2eaf-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a2eaf-115">Requirements</span></span>  
 <span data-ttu-id="a2eaf-116">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a2eaf-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a2eaf-117">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="a2eaf-117">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="a2eaf-118">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a2eaf-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a2eaf-119">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a2eaf-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2eaf-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2eaf-120">See Also</span></span>  
 [<span data-ttu-id="a2eaf-121">ICLRRuntimeInfo, interface</span><span class="sxs-lookup"><span data-stu-id="a2eaf-121">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)  
 [<span data-ttu-id="a2eaf-122">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="a2eaf-122">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [<span data-ttu-id="a2eaf-123">Hébergement</span><span class="sxs-lookup"><span data-stu-id="a2eaf-123">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)  
 [<span data-ttu-id="a2eaf-124">\<startup>, élément</span><span class="sxs-lookup"><span data-stu-id="a2eaf-124">\<startup> Element</span></span>](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md)
