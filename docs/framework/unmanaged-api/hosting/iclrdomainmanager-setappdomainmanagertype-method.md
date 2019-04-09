---
title: ICLRDomainManager::SetAppDomainManagerType, méthode
ms.date: 03/30/2017
api_name:
- ICLRDomainManager.SetAppDomainManagerType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDomainManager::SetAppDomainManagerType
helpviewer_keywords:
- SetAppDomainManagerType method, ICLRDomainManager interface [.NET Framework hosting]
- ICLRDomainManager::SetAppDomainManagerType method [.NET Framework hosting]
ms.assetid: ee91abb0-cb74-41dd-927b-e117fb8ffdf4
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6cfef7d929d40996716a02a4db51630827011a68
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59183246"
---
# <a name="iclrdomainmanagersetappdomainmanagertype-method"></a><span data-ttu-id="62c9c-102">ICLRDomainManager::SetAppDomainManagerType, méthode</span><span class="sxs-lookup"><span data-stu-id="62c9c-102">ICLRDomainManager::SetAppDomainManagerType Method</span></span>
<span data-ttu-id="62c9c-103">Spécifie le type, dérivé de la <xref:System.AppDomainManager?displayProperty=nameWithType> classe, du Gestionnaire de domaine qui sera utilisé pour initialiser le domaine d’application par défaut.</span><span class="sxs-lookup"><span data-stu-id="62c9c-103">Specifies the type, derived from the <xref:System.AppDomainManager?displayProperty=nameWithType> class, of the application domain manager that will be used to initialize the default application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="62c9c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62c9c-104">Syntax</span></span>  
  
```  
HRESULT SetAppDomainManagerType(  
    [in] LPCWSTR wszAppDomainManagerAssembly,  
    [in] LPCWSTR wszAppDomainManagerType,  
    [in] EInitializeNewDomainFlags dwInitializeDomainFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="62c9c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62c9c-105">Parameters</span></span>  
 `wszAppDomainManagerAssembly`  
 <span data-ttu-id="62c9c-106">[in] Le nom complet de l’assembly qui contient le type de gestionnaire de domaine application ; par exemple : "AdMgrExample, Version=1.0.0.0, Culture=neutral, PublicKeyToken=6856bccf150f00b3".</span><span class="sxs-lookup"><span data-stu-id="62c9c-106">[in] The display name of the assembly that contains the application domain manager type; for example: "AdMgrExample, Version=1.0.0.0, Culture=neutral, PublicKeyToken=6856bccf150f00b3".</span></span>  
  
 `wszAppDomainManagerType`  
 <span data-ttu-id="62c9c-107">[in] Le nom de type du Gestionnaire de domaine, y compris l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="62c9c-107">[in] The type name of the application domain manager, including the namespace.</span></span>  
  
 `dwInitializeDomainFlags`  
 <span data-ttu-id="62c9c-108">[in] Une combinaison de [EInitializeNewDomainFlags](../../../../docs/framework/unmanaged-api/hosting/einitializenewdomainflags-enumeration.md) valeurs d’énumération qui fournissent des informations sur le Gestionnaire de domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="62c9c-108">[in] A combination of [EInitializeNewDomainFlags](../../../../docs/framework/unmanaged-api/hosting/einitializenewdomainflags-enumeration.md) enumeration values that provide information about the application domain manager.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="62c9c-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="62c9c-109">Return Value</span></span>  
 <span data-ttu-id="62c9c-110">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="62c9c-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="62c9c-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="62c9c-111">HRESULT</span></span>|<span data-ttu-id="62c9c-112">Description</span><span class="sxs-lookup"><span data-stu-id="62c9c-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="62c9c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="62c9c-113">S_OK</span></span>|<span data-ttu-id="62c9c-114">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="62c9c-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="62c9c-115">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="62c9c-115">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="62c9c-116">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="62c9c-116">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="62c9c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="62c9c-117">Remarks</span></span>  
 <span data-ttu-id="62c9c-118">Actuellement, la seule valeur définie pour `dwInitializeDomainFlags` est `eInitializeNewDomainFlags_NoSecurityChanges`, ce qui indique le common language runtime (CLR) que le Gestionnaire de domaine d’application ne modifiera pas de paramètres de sécurité pendant l’exécution de la <xref:System.AppDomainManager.InitializeNewDomain%2A?displayProperty=nameWithType> (méthode).</span><span class="sxs-lookup"><span data-stu-id="62c9c-118">Currently, the only defined value for `dwInitializeDomainFlags` is `eInitializeNewDomainFlags_NoSecurityChanges`, which tells the common language runtime (CLR) that the application domain manager will not modify security settings during the execution of the <xref:System.AppDomainManager.InitializeNewDomain%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="62c9c-119">Cela permet au CLR d’optimiser le chargement d’assemblys qui ont l’instruction conditionnelle <xref:System.Security.AllowPartiallyTrustedCallersAttribute> attribut (APTCA).</span><span class="sxs-lookup"><span data-stu-id="62c9c-119">This allows the CLR to optimize the loading of assemblies that have the conditional <xref:System.Security.AllowPartiallyTrustedCallersAttribute> (APTCA) attribute.</span></span> <span data-ttu-id="62c9c-120">Si la fermeture transitive de cet ensemble d’assemblys est importante, cela peut entraîner une amélioration significative du temps de démarrage.</span><span class="sxs-lookup"><span data-stu-id="62c9c-120">This can result in a significant improvement in startup time if the transitive closure of this set of assemblies is large.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="62c9c-121">Si l’hôte spécifie `eInitializeNewDomainFlags_NoSecurityChanges` pour le Gestionnaire de domaine d’application, un <xref:System.InvalidOperationException> est levée si une tentative est faite pour modifier la sécurité du domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="62c9c-121">If the host specifies `eInitializeNewDomainFlags_NoSecurityChanges` for the application domain manager, an <xref:System.InvalidOperationException> is thrown if any attempt is made to modify the security of the application domain.</span></span>  
  
 <span data-ttu-id="62c9c-122">Appel de la [ICLRControl::SetAppDomainManagerType](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-setappdomainmanagertype-method.md)méthode revient à appeler `ICLRDomainManager::SetAppDomainManagerType` avec `eInitializeNewDomainFlags_None`.</span><span class="sxs-lookup"><span data-stu-id="62c9c-122">Calling the [ICLRControl::SetAppDomainManagerType](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-setappdomainmanagertype-method.md)method is equivalent to calling `ICLRDomainManager::SetAppDomainManagerType` with `eInitializeNewDomainFlags_None`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="62c9c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62c9c-123">Requirements</span></span>  
 <span data-ttu-id="62c9c-124">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="62c9c-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="62c9c-125">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="62c9c-125">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="62c9c-126">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="62c9c-126">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="62c9c-127">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="62c9c-127">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="62c9c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62c9c-128">See also</span></span>

- [<span data-ttu-id="62c9c-129">Hébergement</span><span class="sxs-lookup"><span data-stu-id="62c9c-129">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
- [<span data-ttu-id="62c9c-130">ICLRDomainManager, interface</span><span class="sxs-lookup"><span data-stu-id="62c9c-130">ICLRDomainManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdomainmanager-interface.md)
- [<span data-ttu-id="62c9c-131">EInitializeNewDomainFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="62c9c-131">EInitializeNewDomainFlags Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/einitializenewdomainflags-enumeration.md)
