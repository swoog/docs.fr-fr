---
title: '&lt;appDomainManagerType&gt; élément'
ms.date: 03/30/2017
helpviewer_keywords:
- appDomainManagerType element
- <appDomainManagerType> element
ms.assetid: ae8d5a7e-e7f7-47f7-98d9-455cc243a322
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8fb771d58a99e42ad53a465008e8848cff0a87fd
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32743483"
---
# <a name="ltappdomainmanagertypegt-element"></a><span data-ttu-id="95d08-102">&lt;appDomainManagerType&gt; élément</span><span class="sxs-lookup"><span data-stu-id="95d08-102">&lt;appDomainManagerType&gt; Element</span></span>
<span data-ttu-id="95d08-103">Spécifie le type qui sert de Gestionnaire de domaine d’application au domaine d’application par défaut.</span><span class="sxs-lookup"><span data-stu-id="95d08-103">Specifies the type that serves as the application domain manager for the default application domain.</span></span>  
  
 <span data-ttu-id="95d08-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="95d08-104">\<configuration></span></span>  
<span data-ttu-id="95d08-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="95d08-105">\<runtime></span></span>  
<span data-ttu-id="95d08-106">\<appDomainManagerType ></span><span class="sxs-lookup"><span data-stu-id="95d08-106">\<appDomainManagerType></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="95d08-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95d08-107">Syntax</span></span>  
  
```xml  
<appDomainManagerAssembly   
   value="type name" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="95d08-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="95d08-108">Attributes and Elements</span></span>  
 <span data-ttu-id="95d08-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="95d08-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="95d08-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="95d08-110">Attributes</span></span>  
  
|<span data-ttu-id="95d08-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="95d08-111">Attribute</span></span>|<span data-ttu-id="95d08-112">Description</span><span class="sxs-lookup"><span data-stu-id="95d08-112">Description</span></span>|  
|---------------|-----------------|  
|`value`|<span data-ttu-id="95d08-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="95d08-113">Required attribute.</span></span> <span data-ttu-id="95d08-114">Spécifie le nom du type, y compris l’espace de noms, qui sert le Gestionnaire de domaine d’application pour le domaine d’application par défaut dans le processus.</span><span class="sxs-lookup"><span data-stu-id="95d08-114">Specifies the name of the type, including the namespace, that serves as the application domain manager for the default application domain in the process.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="95d08-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="95d08-115">Child Elements</span></span>  
 <span data-ttu-id="95d08-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="95d08-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="95d08-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="95d08-117">Parent Elements</span></span>  
  
|<span data-ttu-id="95d08-118">Élément</span><span class="sxs-lookup"><span data-stu-id="95d08-118">Element</span></span>|<span data-ttu-id="95d08-119">Description</span><span class="sxs-lookup"><span data-stu-id="95d08-119">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="95d08-120">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="95d08-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="95d08-121">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="95d08-121">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="95d08-122">Notes</span><span class="sxs-lookup"><span data-stu-id="95d08-122">Remarks</span></span>  
 <span data-ttu-id="95d08-123">Pour spécifier le type du Gestionnaire de domaine d’application, vous devez spécifier cet élément et la [ \<appDomainManagerAssembly >](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagerassembly-element.md) élément.</span><span class="sxs-lookup"><span data-stu-id="95d08-123">To specify the type of the application domain manager, you must specify both this element and the [\<appDomainManagerAssembly>](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagerassembly-element.md) element.</span></span> <span data-ttu-id="95d08-124">Si un de ces éléments n’est pas spécifié, l’autre est ignorée.</span><span class="sxs-lookup"><span data-stu-id="95d08-124">If either of these elements is not specified, the other is ignored.</span></span>  
  
 <span data-ttu-id="95d08-125">Lorsque le domaine d’application par défaut est chargé, <xref:System.TypeLoadException> est levée si le type spécifié n’existe pas dans l’assembly spécifié par le [ \<appDomainManagerAssembly >](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagerassembly-element.md) élément ; et Échec de la procédure Démarrer.</span><span class="sxs-lookup"><span data-stu-id="95d08-125">When the default application domain is loaded, <xref:System.TypeLoadException> is thrown if the specified type does not exist in the assembly that is specified by the [\<appDomainManagerAssembly>](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagerassembly-element.md) element; and the process fails to start.</span></span>  
  
 <span data-ttu-id="95d08-126">Lorsque vous spécifiez le type de gestionnaire de domaine application pour le domaine d’application par défaut, le type de gestionnaire de domaine application héritent des autres domaines d’application créés à partir du domaine d’application par défaut.</span><span class="sxs-lookup"><span data-stu-id="95d08-126">When you specify the application domain manager type for the default application domain, other application domains created from the default application domain inherit the application domain manager type.</span></span> <span data-ttu-id="95d08-127">Utilisez le <xref:System.AppDomainSetup.AppDomainManagerType%2A?displayProperty=nameWithType> et <xref:System.AppDomainSetup.AppDomainManagerAssembly%2A?displayProperty=nameWithType> des propriétés pour spécifier un type de gestionnaire de domaine d’application pour un domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="95d08-127">Use the <xref:System.AppDomainSetup.AppDomainManagerType%2A?displayProperty=nameWithType> and <xref:System.AppDomainSetup.AppDomainManagerAssembly%2A?displayProperty=nameWithType> properties to specify a different application domain manager type for a new application domain.</span></span>  
  
 <span data-ttu-id="95d08-128">En spécifiant le type de gestionnaire de domaine application nécessite que l’application d’avoir une confiance totale.</span><span class="sxs-lookup"><span data-stu-id="95d08-128">Specifying the application domain manager type requires the application to have full trust.</span></span> <span data-ttu-id="95d08-129">(Par exemple, une application en cours d’exécution sur le bureau a une confiance totale.) Si l’application n’a pas d’une confiance totale, un <xref:System.TypeLoadException> est levée.</span><span class="sxs-lookup"><span data-stu-id="95d08-129">(For example, an application running on the desktop has full trust.) If the application does not have full trust, a <xref:System.TypeLoadException> is thrown.</span></span>  
  
 <span data-ttu-id="95d08-130">Le format du type et de l’espace de noms est le même format que celui qui est utilisé pour le <xref:System.Type.FullName%2A?displayProperty=nameWithType> propriété.</span><span class="sxs-lookup"><span data-stu-id="95d08-130">The format of the type and namespace is the same format that is used for the <xref:System.Type.FullName%2A?displayProperty=nameWithType> property.</span></span>  
  
 <span data-ttu-id="95d08-131">Cet élément de configuration est uniquement disponible dans le [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)] et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="95d08-131">This configuration element is available only in the [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)] and later.</span></span>  
  
## <a name="example"></a><span data-ttu-id="95d08-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="95d08-132">Example</span></span>  
 <span data-ttu-id="95d08-133">L’exemple suivant montre comment spécifier que le Gestionnaire de domaine d’application pour le domaine d’application par défaut d’un processus est le `MyMgr` de type dans le `AdMgrExample` assembly.</span><span class="sxs-lookup"><span data-stu-id="95d08-133">The following example shows how to specify that the application domain manager for the default application domain of a process is the `MyMgr` type in the `AdMgrExample` assembly.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <appDomainManagerType value="MyMgr" />  
      <appDomainManagerAssembly   
         value="AdMgrExample, Version=1.0.0.0, Culture=neutral, PublicKeyToken=6856bccf150f00b3" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="95d08-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95d08-134">See Also</span></span>  
 <xref:System.AppDomainSetup.AppDomainManagerType%2A?displayProperty=nameWithType>  
 <xref:System.AppDomainSetup.AppDomainManagerAssembly%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="95d08-135">\<appDomainManagerAssembly > élément</span><span class="sxs-lookup"><span data-stu-id="95d08-135">\<appDomainManagerAssembly> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagerassembly-element.md)  
 [<span data-ttu-id="95d08-136">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="95d08-136">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [<span data-ttu-id="95d08-137">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="95d08-137">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="95d08-138">SetAppDomainManagerType, méthode</span><span class="sxs-lookup"><span data-stu-id="95d08-138">SetAppDomainManagerType Method</span></span>](../../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-setappdomainmanagertype-method.md)
