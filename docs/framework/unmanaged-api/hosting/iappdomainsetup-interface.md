---
title: IAppDomainSetup, interface
ms.date: 03/30/2017
api_name:
- IAppDomainSetup
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IAppDomainSetup
helpviewer_keywords:
- IAppDomainSetup interface [.NET Framework hosting]
ms.assetid: 1844da85-c031-40bf-bea4-1a3d12a36c8c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cbcbc446eabcfcbc28c830f8860bde726c8eb6e3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33434766"
---
# <a name="iappdomainsetup-interface"></a><span data-ttu-id="516e2-102">IAppDomainSetup, interface</span><span class="sxs-lookup"><span data-stu-id="516e2-102">IAppDomainSetup Interface</span></span>
<span data-ttu-id="516e2-103">Fournit des propriétés qui permettent à l’hôte configurer un <xref:System.AppDomain?displayProperty=nameWithType> type avant d’appeler le [ICorRuntimeHost::CreateDomainEx](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-createdomainex-method.md) méthode pour le créer.</span><span class="sxs-lookup"><span data-stu-id="516e2-103">Provides properties that allow the host to configure an <xref:System.AppDomain?displayProperty=nameWithType> type before calling the [ICorRuntimeHost::CreateDomainEx](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-createdomainex-method.md) method to create it.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="516e2-104">Propriétés</span><span class="sxs-lookup"><span data-stu-id="516e2-104">Properties</span></span>  
  
|<span data-ttu-id="516e2-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="516e2-105">Property</span></span>|<span data-ttu-id="516e2-106">Description</span><span class="sxs-lookup"><span data-stu-id="516e2-106">Description</span></span>|  
|--------------|-----------------|  
|<xref:System.AppDomainSetup.ApplicationBase%2A>|<span data-ttu-id="516e2-107">Obtient ou définit le nom du répertoire qui contient l’application.</span><span class="sxs-lookup"><span data-stu-id="516e2-107">Gets or sets the name of the directory that contains the application.</span></span>|  
|<xref:System.AppDomainSetup.ApplicationName%2A>|<span data-ttu-id="516e2-108">Obtient ou définit le nom de l'application.</span><span class="sxs-lookup"><span data-stu-id="516e2-108">Gets or sets the name of the application.</span></span>|  
|<xref:System.AppDomainSetup.CachePath%2A>|<span data-ttu-id="516e2-109">Obtient ou définit le nom d’une zone spécifique à l’application où les fichiers sont copiés de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="516e2-109">Gets or sets the name of an area specific to the application where files are shadow-copied.</span></span>|  
|<xref:System.AppDomainSetup.ConfigurationFile%2A>|<span data-ttu-id="516e2-110">Obtient ou définit le nom du fichier de configuration pour une application.</span><span class="sxs-lookup"><span data-stu-id="516e2-110">Gets or sets the name of the configuration file for an application.</span></span>|  
|<xref:System.AppDomainSetup.DynamicBase%2A>|<span data-ttu-id="516e2-111">Obtient ou définit le nom du répertoire où les fichiers générés de manière dynamique sont stockés et accessibles.</span><span class="sxs-lookup"><span data-stu-id="516e2-111">Gets or sets the name of the directory where dynamically generated files are stored and accessed.</span></span>|  
|<xref:System.AppDomainSetup.LicenseFile%2A>|<span data-ttu-id="516e2-112">Obtient ou définit le chemin d’accès du fichier de licence associé à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="516e2-112">Gets or sets the path to the license file that is associated with this domain.</span></span>|  
|<xref:System.AppDomainSetup.PrivateBinPath%2A>|<span data-ttu-id="516e2-113">Obtient ou définit la liste des répertoires associés la <xref:System.AppDomainSetup.ApplicationBase%2A> active pour détecter les assemblys privés.</span><span class="sxs-lookup"><span data-stu-id="516e2-113">Gets or sets the list of directories combined with the <xref:System.AppDomainSetup.ApplicationBase%2A> directory to probe for private assemblies.</span></span>|  
|<xref:System.AppDomainSetup.PrivateBinPathProbe%2A>|<span data-ttu-id="516e2-114">Obtient ou définit une valeur de chaîne qui inclut ou exclut <xref:System.AppDomainSetup.ApplicationBase%2A> du chemin de recherche pour l’application.</span><span class="sxs-lookup"><span data-stu-id="516e2-114">Gets or sets a string value that includes or excludes <xref:System.AppDomainSetup.ApplicationBase%2A> from the search path for the application.</span></span>|  
|<xref:System.AppDomainSetup.ShadowCopyDirectories%2A>|<span data-ttu-id="516e2-115">Obtient ou définit les noms des répertoires qui contiennent des assemblys pour être le cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="516e2-115">Gets or sets the names of the directories that contain assemblies to be shadow-copied.</span></span>|  
|<xref:System.AppDomainSetup.ShadowCopyFiles%2A>|<span data-ttu-id="516e2-116">Obtient ou définit une chaîne qui indique si la copie de clichés instantanés est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="516e2-116">Gets or sets a string that indicates whether shadow-copying is turned on or off.</span></span> <span data-ttu-id="516e2-117">Les valeurs valides sont « true » ou « false ».</span><span class="sxs-lookup"><span data-stu-id="516e2-117">Valid values are "true" or "false".</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="516e2-118">Notes</span><span class="sxs-lookup"><span data-stu-id="516e2-118">Remarks</span></span>  
 <span data-ttu-id="516e2-119">Le `IAppDomainSetup` interface correspond à managé <xref:System.IAppDomainSetup> d’interface, ce qui le <xref:System.AppDomainSetup> type implémente.</span><span class="sxs-lookup"><span data-stu-id="516e2-119">The `IAppDomainSetup` interface corresponds to the managed <xref:System.IAppDomainSetup> interface, which the <xref:System.AppDomainSetup> type implements.</span></span> <span data-ttu-id="516e2-120">Consultez <xref:System.IAppDomainSetup?displayProperty=nameWithType> pour une description détaillée de ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="516e2-120">See <xref:System.IAppDomainSetup?displayProperty=nameWithType> for detailed descriptions of its properties.</span></span>  
  
 <span data-ttu-id="516e2-121">`IAppDomainSetup` représente des informations de liaison d’assembly qui peuvent être ajoutées à un <xref:System.AppDomain> instance avant sa création.</span><span class="sxs-lookup"><span data-stu-id="516e2-121">`IAppDomainSetup` represents assembly binding information that can be added to an <xref:System.AppDomain> instance before its creation.</span></span> <span data-ttu-id="516e2-122">Par exemple, un hôte peut définir le <xref:System.AppDomainSetup.ApplicationBase%2A> propriété pour définir un répertoire racine dans lequel le common language runtime (CLR) recherche des assemblys managés.</span><span class="sxs-lookup"><span data-stu-id="516e2-122">For example, a host can set the <xref:System.AppDomainSetup.ApplicationBase%2A> property to establish a root directory, which the common language runtime (CLR) probes for managed assemblies.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="516e2-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="516e2-123">Requirements</span></span>  
 <span data-ttu-id="516e2-124">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="516e2-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="516e2-125">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="516e2-125">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="516e2-126">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="516e2-126">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="516e2-127">**Versions du .NET framework :** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="516e2-127">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="516e2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="516e2-128">See Also</span></span>  
 <xref:System.AppDomain>  
 <xref:System.AppDomainSetup>  
 <xref:System.IAppDomainSetup>  
 [<span data-ttu-id="516e2-129">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="516e2-129">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
