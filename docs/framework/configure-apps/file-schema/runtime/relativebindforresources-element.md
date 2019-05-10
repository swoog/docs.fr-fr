---
title: Élément <relativeBindForResources>
ms.date: 03/30/2017
helpviewer_keywords:
- RelativeBindForResources element
- <relativeBindForResources> element
ms.assetid: 846ffa47-7257-4ce3-8cac-7ff627e0e34f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 15156eaf883fc9ec162e0a85525564d49522b01d
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64592670"
---
# <a name="relativebindforresources-element"></a><span data-ttu-id="6f0be-102">\<relativeBindForResources > élément</span><span class="sxs-lookup"><span data-stu-id="6f0be-102">\<relativeBindForResources> Element</span></span>
<span data-ttu-id="6f0be-103">Optimise la sonde pour les assemblys satellites.</span><span class="sxs-lookup"><span data-stu-id="6f0be-103">Optimizes the probe for satellite assemblies.</span></span>  
  
 <span data-ttu-id="6f0be-104">\<configuration > élément</span><span class="sxs-lookup"><span data-stu-id="6f0be-104">\<configuration> Element</span></span>  
<span data-ttu-id="6f0be-105">\<runtime > élément</span><span class="sxs-lookup"><span data-stu-id="6f0be-105">\<runtime> Element</span></span>  
<span data-ttu-id="6f0be-106">\<relativeBindForResources > élément</span><span class="sxs-lookup"><span data-stu-id="6f0be-106">\<relativeBindForResources> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6f0be-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f0be-107">Syntax</span></span>  
  
```xml
<relativeBindForResources    
   enabled="true|false" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6f0be-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6f0be-108">Attributes and Elements</span></span>  
 <span data-ttu-id="6f0be-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6f0be-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6f0be-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="6f0be-110">Attributes</span></span>  
  
|<span data-ttu-id="6f0be-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="6f0be-111">Attribute</span></span>|<span data-ttu-id="6f0be-112">Description</span><span class="sxs-lookup"><span data-stu-id="6f0be-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="6f0be-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="6f0be-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="6f0be-114">Spécifie si le common language runtime optimise la sonde pour les assemblys satellites.</span><span class="sxs-lookup"><span data-stu-id="6f0be-114">Specifies whether the common language runtime optimizes the probe for satellite assemblies.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="6f0be-115">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="6f0be-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="6f0be-116">Value</span><span class="sxs-lookup"><span data-stu-id="6f0be-116">Value</span></span>|<span data-ttu-id="6f0be-117">Description</span><span class="sxs-lookup"><span data-stu-id="6f0be-117">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="6f0be-118">Le runtime n’optimise pas la sonde pour les assemblys satellites.</span><span class="sxs-lookup"><span data-stu-id="6f0be-118">The runtime does not optimize the probe for satellite assemblies.</span></span> <span data-ttu-id="6f0be-119">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="6f0be-119">This is the default value.</span></span>|  
|`true`|<span data-ttu-id="6f0be-120">Le runtime optimise la sonde pour les assemblys satellites.</span><span class="sxs-lookup"><span data-stu-id="6f0be-120">The runtime optimizes the probe for satellite assemblies.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6f0be-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6f0be-121">Child Elements</span></span>  
 <span data-ttu-id="6f0be-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6f0be-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6f0be-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6f0be-123">Parent Elements</span></span>  
  
|<span data-ttu-id="6f0be-124">Élément</span><span class="sxs-lookup"><span data-stu-id="6f0be-124">Element</span></span>|<span data-ttu-id="6f0be-125">Description</span><span class="sxs-lookup"><span data-stu-id="6f0be-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="6f0be-126">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="6f0be-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="6f0be-127">Contient des informations sur les options d'initialisation du runtime.</span><span class="sxs-lookup"><span data-stu-id="6f0be-127">Contains information about runtime initialization options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6f0be-128">Notes</span><span class="sxs-lookup"><span data-stu-id="6f0be-128">Remarks</span></span>  
 <span data-ttu-id="6f0be-129">En règle générale, Resource Manager tente de détecter des ressources, comme indiqué dans le [Packaging and Deploying Resources](../../../../../docs/framework/resources/packaging-and-deploying-resources-in-desktop-apps.md) rubrique.</span><span class="sxs-lookup"><span data-stu-id="6f0be-129">In general, Resource Manager probes for resources, as documented in the [Packaging and Deploying Resources](../../../../../docs/framework/resources/packaging-and-deploying-resources-in-desktop-apps.md) topic.</span></span> <span data-ttu-id="6f0be-130">Cela signifie que lorsque Resource Manager tente de détecter une version localisée particulière d’une ressource, il peut rechercher dans le global assembly cache, de rechercher dans un dossier spécifique à la culture dans la requête de base, de code de l’application Windows Installer pour les assemblys satellites et déclencher le <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> événement.</span><span class="sxs-lookup"><span data-stu-id="6f0be-130">This means that when Resource Manager probes for a particular localized version of a resource, it may look in the global assembly cache, look in a culture-specific folder in the application's code base, query Windows Installer for satellite assemblies, and raise the <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> event.</span></span> <span data-ttu-id="6f0be-131">Le `<relativeBindForResources>` élément optimise celle dans laquelle Resource Manager tente de détecter les assemblys satellites.</span><span class="sxs-lookup"><span data-stu-id="6f0be-131">The `<relativeBindForResources>` element optimizes the way in which Resource Manager probes for satellite assemblies.</span></span> <span data-ttu-id="6f0be-132">Elle peut améliorer les performances lors de la détection pour les ressources dans les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f0be-132">It can improve performance when probing for resources under the following conditions:</span></span>  
  
- <span data-ttu-id="6f0be-133">Lorsque l’assembly satellite est déployé dans le même emplacement que l’assembly de code.</span><span class="sxs-lookup"><span data-stu-id="6f0be-133">When the satellite assembly is deployed in the same location as the code assembly.</span></span> <span data-ttu-id="6f0be-134">En d’autres termes, si l’assembly de code est installé dans le global assembly cache, les assemblys satellites doivent également être installés il.</span><span class="sxs-lookup"><span data-stu-id="6f0be-134">In other words, if the code assembly is installed in the global assembly cache, the satellite assemblies must also be installed there.</span></span> <span data-ttu-id="6f0be-135">Si l’assembly de code est installé dans la base de code de l’application, les assemblys satellites doivent également être installés dans un dossier spécifique à la culture dans la base de code.</span><span class="sxs-lookup"><span data-stu-id="6f0be-135">If the code assembly is installed in the application's code base, the satellite assemblies must also be installed in a culture-specific folder in the code base.</span></span>  
  
- <span data-ttu-id="6f0be-136">Lorsque le programme d’installation de Windows n’est pas utilisé ou est rarement utilisé pour l’installation à la demande des assemblys satellites.</span><span class="sxs-lookup"><span data-stu-id="6f0be-136">When Windows Installer is not used or is used only rarely for on-demand installation of satellite assemblies.</span></span>  
  
- <span data-ttu-id="6f0be-137">Lorsque le code d’application ne gère pas la <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> événement.</span><span class="sxs-lookup"><span data-stu-id="6f0be-137">When application code does not handle the <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> event.</span></span>  
  
 <span data-ttu-id="6f0be-138">Définition de la `enabled` attribut de la `<relativeBindForResources>` élément à `true` optimise la sonde du Gestionnaire de ressources pour les assemblys satellites comme suit :</span><span class="sxs-lookup"><span data-stu-id="6f0be-138">Setting the `enabled` attribute of the `<relativeBindForResources>` element to `true` optimizes Resource Manager's probe for satellite assemblies as follows:</span></span>  
  
- <span data-ttu-id="6f0be-139">Il utilise l’emplacement de l’assembly de code parent pour détecter l’assembly satellite.</span><span class="sxs-lookup"><span data-stu-id="6f0be-139">It uses the location of the parent code assembly to probe for the satellite assembly.</span></span>  
  
- <span data-ttu-id="6f0be-140">Il n’interroge pas le programme d’installation de Windows pour les assemblys satellites.</span><span class="sxs-lookup"><span data-stu-id="6f0be-140">It does not query Windows Installer for satellite assemblies.</span></span>  
  
- <span data-ttu-id="6f0be-141">Elle ne déclenche pas le <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> événement.</span><span class="sxs-lookup"><span data-stu-id="6f0be-141">It does not raise the <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> event.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6f0be-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f0be-142">See also</span></span>

- [<span data-ttu-id="6f0be-143">Empaquetage et déploiement de ressources</span><span class="sxs-lookup"><span data-stu-id="6f0be-143">Packaging and Deploying Resources</span></span>](../../../../../docs/framework/resources/packaging-and-deploying-resources-in-desktop-apps.md)
- [<span data-ttu-id="6f0be-144">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="6f0be-144">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="6f0be-145">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="6f0be-145">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
