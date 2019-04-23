---
title: ICLRDomainManager::SetPropertiesForDefaultAppDomain, méthode
ms.date: 03/30/2017
api_name:
- ICLRDomainManager.SetPropertiesForDefaultAppDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDomainManager::SetPropertiesForDefaultAppDomain
helpviewer_keywords:
- ICLRDomainManager::SetPropertiesForDefaultAppDomain method [.NET Framework hosting]
- SetPropertiesForDefaultAppDomain method [.NET Framework hosting]
ms.assetid: 43e61c4b-c435-45ec-9ef6-c68403aa4200
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4c42297e848844617ffdc6c85c81846b5805eb4b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59181331"
---
# <a name="iclrdomainmanagersetpropertiesfordefaultappdomain-method"></a><span data-ttu-id="52f9d-102">ICLRDomainManager::SetPropertiesForDefaultAppDomain, méthode</span><span class="sxs-lookup"><span data-stu-id="52f9d-102">ICLRDomainManager::SetPropertiesForDefaultAppDomain Method</span></span>
<span data-ttu-id="52f9d-103">Définit les propriétés qui seront utilisées pour initialiser le domaine d’application par défaut.</span><span class="sxs-lookup"><span data-stu-id="52f9d-103">Sets properties that will be used to initialize the default application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="52f9d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52f9d-104">Syntax</span></span>  
  
```  
HRESULT SetPropertiesForDefaultAppDomain(  
    [in] DWORD nProperties,  
    [in] LPCWSTR *pwszPropertyNames,  
    [in] LPCWSTR *pwszPropertyValues  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="52f9d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52f9d-105">Parameters</span></span>  
 `nProperties`  
 <span data-ttu-id="52f9d-106">[in] Le nombre d’entrées dans `pwszPropertyNames` et `pwszPropertyValues`.</span><span class="sxs-lookup"><span data-stu-id="52f9d-106">[in] The number of entries in `pwszPropertyNames` and `pwszPropertyValues`.</span></span>  
  
 `pwszPropertyNames`  
 <span data-ttu-id="52f9d-107">[in] Tableau de noms de propriété, ou null si aucune propriété.</span><span class="sxs-lookup"><span data-stu-id="52f9d-107">[in] An array of property names, or null if there are no properties.</span></span> <span data-ttu-id="52f9d-108">Actuellement, le seul nom de propriété qui est reconnu par cette méthode est « PARTIAL_TRUST_VISIBLE_ASSEMBLIES ».</span><span class="sxs-lookup"><span data-stu-id="52f9d-108">Currently, the only property name that is recognized by this method is "PARTIAL_TRUST_VISIBLE_ASSEMBLIES".</span></span>  
  
 `pwszPropertyValues`  
 <span data-ttu-id="52f9d-109">[in] Un tableau de valeurs de propriété, ou null si aucune propriété.</span><span class="sxs-lookup"><span data-stu-id="52f9d-109">[in] An array of property values, or null if there are no properties.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="52f9d-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="52f9d-110">Return Value</span></span>  
 <span data-ttu-id="52f9d-111">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="52f9d-111">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="52f9d-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="52f9d-112">HRESULT</span></span>|<span data-ttu-id="52f9d-113">Description</span><span class="sxs-lookup"><span data-stu-id="52f9d-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="52f9d-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="52f9d-114">S_OK</span></span>|<span data-ttu-id="52f9d-115">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="52f9d-115">The method completed successfully.</span></span>|  
|<span data-ttu-id="52f9d-116">HRESULT_FROM_WIN32(ERROR_UNKNOWN_PROPERTY)</span><span class="sxs-lookup"><span data-stu-id="52f9d-116">HRESULT_FROM_WIN32(ERROR_UNKNOWN_PROPERTY)</span></span>|<span data-ttu-id="52f9d-117">`pwszPropertyNames` inclut un nom de propriété qui n’est pas reconnu par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="52f9d-117">`pwszPropertyNames` includes a property name that is not recognized by this method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="52f9d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="52f9d-118">Remarks</span></span>  
 <span data-ttu-id="52f9d-119">La valeur de propriété pour « PARTIAL_TRUST_VISIBLE_ASSEMBLIES » est une liste d’assemblys qui ont l’instruction conditionnelle <xref:System.Security.AllowPartiallyTrustedCallersAttribute> attribut (APTCA) avec le <xref:System.Security.PartialTrustVisibilityLevel.NotVisibleByDefault?displayProperty=nameWithType> indicateur, qui doivent être visibles aux appelants partiellement approuvés dans l’application par défaut domaine.</span><span class="sxs-lookup"><span data-stu-id="52f9d-119">The property value for "PARTIAL_TRUST_VISIBLE_ASSEMBLIES" is a list of assemblies that have the conditional <xref:System.Security.AllowPartiallyTrustedCallersAttribute> (APTCA) attribute with the <xref:System.Security.PartialTrustVisibilityLevel.NotVisibleByDefault?displayProperty=nameWithType> flag, which are to be made visible to partially trusted callers in the default application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="52f9d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52f9d-120">Requirements</span></span>  
 <span data-ttu-id="52f9d-121">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="52f9d-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="52f9d-122">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="52f9d-122">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="52f9d-123">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="52f9d-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="52f9d-124">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="52f9d-124">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="52f9d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52f9d-125">See also</span></span>

- [<span data-ttu-id="52f9d-126">Hébergement</span><span class="sxs-lookup"><span data-stu-id="52f9d-126">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
- [<span data-ttu-id="52f9d-127">ICLRDomainManager, interface</span><span class="sxs-lookup"><span data-stu-id="52f9d-127">ICLRDomainManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdomainmanager-interface.md)
