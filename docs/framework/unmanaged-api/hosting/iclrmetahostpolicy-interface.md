---
title: ICLRMetaHostPolicy, interface
ms.date: 03/30/2017
api_name:
- ICLRMetaHostPolicy
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHostPolicy
helpviewer_keywords:
- ICLRMetaHostPolicy interface [.NET Framework hosting]
ms.assetid: 1bdeccb6-0698-4c97-ad69-eae2b69e59f1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f9a70cf0812f84908630f109ef06aafa4b4f7525
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33434420"
---
# <a name="iclrmetahostpolicy-interface"></a><span data-ttu-id="2fcf1-102">ICLRMetaHostPolicy, interface</span><span class="sxs-lookup"><span data-stu-id="2fcf1-102">ICLRMetaHostPolicy Interface</span></span>
<span data-ttu-id="2fcf1-103">Fournit la [GetRequestedRuntime](../../../../docs/framework/unmanaged-api/hosting/iclrmetahostpolicy-getrequestedruntime-method.md) méthode, qui retourne un pointeur vers une interface du common language runtime (CLR) selon un critère de stratégie, managé fichier de configuration, de la version et de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="2fcf1-103">Provides the [GetRequestedRuntime](../../../../docs/framework/unmanaged-api/hosting/iclrmetahostpolicy-getrequestedruntime-method.md) method, which returns a pointer to a common language runtime (CLR) interface based on a policy criteria, managed assembly, version and configuration file.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="2fcf1-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2fcf1-104">Methods</span></span>  
  
|<span data-ttu-id="2fcf1-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="2fcf1-105">Method</span></span>|<span data-ttu-id="2fcf1-106">Description</span><span class="sxs-lookup"><span data-stu-id="2fcf1-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="2fcf1-107">GetRequestedRuntime, méthode</span><span class="sxs-lookup"><span data-stu-id="2fcf1-107">GetRequestedRuntime Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahostpolicy-getrequestedruntime-method.md)|<span data-ttu-id="2fcf1-108">Fournit une interface CLR par défaut selon un critère de stratégie, géré de fichier d’assembly, version et la configuration.</span><span class="sxs-lookup"><span data-stu-id="2fcf1-108">Provides a preferred CLR interface based on a policy criteria, managed assembly, version, and configuration file.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2fcf1-109">Notes</span><span class="sxs-lookup"><span data-stu-id="2fcf1-109">Remarks</span></span>  
 <span data-ttu-id="2fcf1-110">Vous pouvez obtenir une référence à cette interface en appelant le [CLRCreateInstance](../../../../docs/framework/unmanaged-api/hosting/clrcreateinstance-function.md) fonctionne comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="2fcf1-110">You can get a reference to this interface by calling the [CLRCreateInstance](../../../../docs/framework/unmanaged-api/hosting/clrcreateinstance-function.md) function as shown in the following code:</span></span>  
  
```  
ICLRMetaHostPolicy *pMetaHostPolicy = NULL;  
HRESULT hr = CLRCreateInstance(CLSID_CLRMetaHostPolicy,  
                   IID_ICLRMetaHostPolicy, (LPVOID*)&pMetaHostPolicy);  
```  
  
> [!NOTE]
>  <span data-ttu-id="2fcf1-111">Cette interface ne prend pas réellement charger et activer le CLR, mais retourne simplement la version CLR par défaut selon les versions disponibles qui sont installées ou chargées.</span><span class="sxs-lookup"><span data-stu-id="2fcf1-111">This interface does not actually load or activate the CLR, but simply returns the preferred CLR version based on the available versions that are installed or loaded.</span></span>  
  
 <span data-ttu-id="2fcf1-112">Le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)] API d’hébergement consolide les stratégies de sorte que les hôtes avec des besoins spécifiques puissent utiliser les fonctionnalités de base sans encourir des pénalités imprévues.</span><span class="sxs-lookup"><span data-stu-id="2fcf1-112">The [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)] hosting API consolidates policies so that hosts with specific needs may use basic functionality without incurring unintended penalties.</span></span> <span data-ttu-id="2fcf1-113">Par exemple, la plupart des exportations MSCorEE.dll liera à un CLR spécifique, bien qu’une méthode peut logiquement impose pas.</span><span class="sxs-lookup"><span data-stu-id="2fcf1-113">For example, many of the MSCorEE.dll exports will bind to a specific CLR, although a method might not logically require it.</span></span> <span data-ttu-id="2fcf1-114">Le [METAHOST_POLICY_FLAGS](../../../../docs/framework/unmanaged-api/hosting/metahost-policy-flags-enumeration.md) énumération fournit des stratégies de liaison qui sont communes à la majorité des ordinateurs hôtes.</span><span class="sxs-lookup"><span data-stu-id="2fcf1-114">The [METAHOST_POLICY_FLAGS](../../../../docs/framework/unmanaged-api/hosting/metahost-policy-flags-enumeration.md) enumeration provides binding policies that are common to the majority of hosts.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2fcf1-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2fcf1-115">Requirements</span></span>  
 <span data-ttu-id="2fcf1-116">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2fcf1-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2fcf1-117">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="2fcf1-117">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="2fcf1-118">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2fcf1-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2fcf1-119">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2fcf1-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2fcf1-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fcf1-120">See Also</span></span>  
 [<span data-ttu-id="2fcf1-121">Interfaces d’hébergement CLR ajoutées dans .NET Framework 4 et 4.5</span><span class="sxs-lookup"><span data-stu-id="2fcf1-121">CLR Hosting Interfaces Added in the .NET Framework 4 and 4.5</span></span>](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)  
 [<span data-ttu-id="2fcf1-122">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="2fcf1-122">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [<span data-ttu-id="2fcf1-123">Hébergement</span><span class="sxs-lookup"><span data-stu-id="2fcf1-123">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
