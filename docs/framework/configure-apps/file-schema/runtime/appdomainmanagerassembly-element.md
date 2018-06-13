---
title: '&lt;appDomainManagerAssembly&gt; élément'
ms.date: 03/30/2017
helpviewer_keywords:
- <appDomainManagerAssembly> element
- appDomainManagerAssembly element
ms.assetid: c7c56e39-a700-44f5-b94e-411bfce339d9
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7656f4819e8ed6d8c1c87eabcbd5862929d47cdc
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32744848"
---
# <a name="ltappdomainmanagerassemblygt-element"></a><span data-ttu-id="3e0d4-102">&lt;appDomainManagerAssembly&gt; élément</span><span class="sxs-lookup"><span data-stu-id="3e0d4-102">&lt;appDomainManagerAssembly&gt; Element</span></span>
<span data-ttu-id="3e0d4-103">Spécifie l’assembly qui fournit le Gestionnaire du domaine d’application par défaut du processus.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-103">Specifies the assembly that provides the application domain manager for the default application domain in the process.</span></span>  
  
 <span data-ttu-id="3e0d4-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="3e0d4-104">\<configuration></span></span>  
<span data-ttu-id="3e0d4-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="3e0d4-105">\<runtime></span></span>  
<span data-ttu-id="3e0d4-106">\<appDomainManagerAssembly ></span><span class="sxs-lookup"><span data-stu-id="3e0d4-106">\<appDomainManagerAssembly></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e0d4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e0d4-107">Syntax</span></span>  
  
```xml  
<appDomainManagerAssembly   
   value="assembly display name" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3e0d4-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3e0d4-108">Attributes and Elements</span></span>  
 <span data-ttu-id="3e0d4-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3e0d4-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="3e0d4-110">Attributes</span></span>  
  
|<span data-ttu-id="3e0d4-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="3e0d4-111">Attribute</span></span>|<span data-ttu-id="3e0d4-112">Description</span><span class="sxs-lookup"><span data-stu-id="3e0d4-112">Description</span></span>|  
|---------------|-----------------|  
|`value`|<span data-ttu-id="3e0d4-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-113">Required attribute.</span></span> <span data-ttu-id="3e0d4-114">Spécifie le nom complet de l’assembly qui fournit le Gestionnaire de domaine d’application pour le domaine d’application par défaut dans le processus.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-114">Specifies the display name of the assembly that provides the application domain manager for the default application domain in the process.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3e0d4-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3e0d4-115">Child Elements</span></span>  
 <span data-ttu-id="3e0d4-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3e0d4-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3e0d4-117">Parent Elements</span></span>  
  
|<span data-ttu-id="3e0d4-118">Élément</span><span class="sxs-lookup"><span data-stu-id="3e0d4-118">Element</span></span>|<span data-ttu-id="3e0d4-119">Description</span><span class="sxs-lookup"><span data-stu-id="3e0d4-119">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="3e0d4-120">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="3e0d4-121">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-121">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3e0d4-122">Notes</span><span class="sxs-lookup"><span data-stu-id="3e0d4-122">Remarks</span></span>  
 <span data-ttu-id="3e0d4-123">Pour spécifier le type du Gestionnaire de domaine d’application, vous devez spécifier cet élément et la [ \<appDomainManagerType >](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagertype-element.md) élément.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-123">To specify the type of the application domain manager, you must specify both this element and the [\<appDomainManagerType>](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagertype-element.md) element.</span></span> <span data-ttu-id="3e0d4-124">Si un de ces éléments n’est pas spécifié, l’autre est ignorée.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-124">If either of these elements is not specified, the other is ignored.</span></span>  
  
 <span data-ttu-id="3e0d4-125">Lorsque le domaine d’application par défaut est chargé, <xref:System.TypeLoadException> est levée si l’assembly spécifié n’existe pas ou si l’assembly ne contient pas le type spécifié par le [ \<appDomainManagerType >](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagertype-element.md) élément ; et le processus ne parvient pas à démarrer.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-125">When the default application domain is loaded, <xref:System.TypeLoadException> is thrown if the specified assembly does not exist or if the assembly does not contain the type specified by the [\<appDomainManagerType>](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagertype-element.md) element; and the process fails to start.</span></span> <span data-ttu-id="3e0d4-126">Si l’assembly est trouvé, mais les informations de version ne correspondent pas, un <xref:System.IO.FileLoadException> est levée.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-126">If the assembly is found but the version information does not match, a <xref:System.IO.FileLoadException> is thrown.</span></span>  
  
 <span data-ttu-id="3e0d4-127">Lorsque vous spécifiez le type de gestionnaire de domaine application pour le domaine d’application par défaut, le type de gestionnaire de domaine application héritent des autres domaines d’application créés à partir du domaine d’application par défaut.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-127">When you specify the application domain manager type for the default application domain, other application domains created from the default application domain inherit the application domain manager type.</span></span> <span data-ttu-id="3e0d4-128">Utilisez le <xref:System.AppDomainSetup.AppDomainManagerType%2A?displayProperty=nameWithType> et <xref:System.AppDomainSetup.AppDomainManagerAssembly%2A?displayProperty=nameWithType> des propriétés pour spécifier un type de gestionnaire de domaine d’application pour un domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-128">Use the <xref:System.AppDomainSetup.AppDomainManagerType%2A?displayProperty=nameWithType> and <xref:System.AppDomainSetup.AppDomainManagerAssembly%2A?displayProperty=nameWithType> properties to specify a different application domain manager type for a new application domain.</span></span>  
  
 <span data-ttu-id="3e0d4-129">En spécifiant le type de gestionnaire de domaine application nécessite que l’application d’avoir une confiance totale.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-129">Specifying the application domain manager type requires the application to have full trust.</span></span> <span data-ttu-id="3e0d4-130">(Par exemple, une application en cours d’exécution sur le bureau a une confiance totale.) Si l’application n’a pas d’une confiance totale, un <xref:System.TypeLoadException> est levée.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-130">(For example, an application running on the desktop has full trust.) If the application does not have full trust, a <xref:System.TypeLoadException> is thrown.</span></span>  
  
 <span data-ttu-id="3e0d4-131">Pour le format du nom complet d’assembly, consultez la <xref:System.Reflection.Assembly.FullName%2A?displayProperty=nameWithType> propriété.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-131">For the format of the assembly display name, see the <xref:System.Reflection.Assembly.FullName%2A?displayProperty=nameWithType> property.</span></span>  
  
 <span data-ttu-id="3e0d4-132">Cet élément de configuration est uniquement disponible dans le [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)] et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-132">This configuration element is available only in the [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)] and later.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3e0d4-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="3e0d4-133">Example</span></span>  
 <span data-ttu-id="3e0d4-134">L’exemple suivant montre comment spécifier que le Gestionnaire de domaine d’application pour le domaine d’application par défaut d’un processus est le `MyMgr` de type dans le `AdMgrExample` assembly.</span><span class="sxs-lookup"><span data-stu-id="3e0d4-134">The following example shows how to specify that the application domain manager for the default application domain of a process is the `MyMgr` type in the `AdMgrExample` assembly.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <appDomainManagerType value="MyMgr" />  
      <appDomainManagerAssembly   
         value="AdMgrExample, Version=1.0.0.0, Culture=neutral, PublicKeyToken=6856bccf150f00b3" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="3e0d4-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e0d4-135">See Also</span></span>  
 <xref:System.AppDomainSetup.AppDomainManagerType%2A?displayProperty=nameWithType>  
 <xref:System.AppDomainSetup.AppDomainManagerAssembly%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="3e0d4-136">\<appDomainManagerType > élément</span><span class="sxs-lookup"><span data-stu-id="3e0d4-136">\<appDomainManagerType> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagertype-element.md)  
 [<span data-ttu-id="3e0d4-137">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="3e0d4-137">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [<span data-ttu-id="3e0d4-138">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="3e0d4-138">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="3e0d4-139">SetAppDomainManagerType, méthode</span><span class="sxs-lookup"><span data-stu-id="3e0d4-139">SetAppDomainManagerType Method</span></span>](../../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-setappdomainmanagertype-method.md)
