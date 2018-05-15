---
title: '&lt;assemblyBinding&gt; , élément pour &lt;runtime&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding
helpviewer_keywords:
- <assemblyBinding> element
- assemblyBinding element
- container tags, <assemblyBinding> element
ms.assetid: 964cbb35-ab49-4498-8471-209689e5dada
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d84c134b8e2b048f39836bbc10af06039e96719e
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltassemblybindinggt-element-for-ltruntimegt"></a><span data-ttu-id="61d74-102">&lt;assemblyBinding&gt; , élément pour &lt;runtime&gt;</span><span class="sxs-lookup"><span data-stu-id="61d74-102">&lt;assemblyBinding&gt; Element for &lt;runtime&gt;</span></span>
<span data-ttu-id="61d74-103">Contient des informations à propos de la redirection des versions d'assemblys et de l'emplacement de ces derniers.</span><span class="sxs-lookup"><span data-stu-id="61d74-103">Contains information about assembly version redirection and the locations of assemblies.</span></span>  
  
 <span data-ttu-id="61d74-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="61d74-104">\<configuration></span></span>  
<span data-ttu-id="61d74-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="61d74-105">\<runtime></span></span>  
<span data-ttu-id="61d74-106">\<assemblyBinding ></span><span class="sxs-lookup"><span data-stu-id="61d74-106">\<assemblyBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61d74-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61d74-107">Syntax</span></span>  
  
```xml  
      <assemblyBinding    
   xmlns="urn:schemas-microsoft-com:asm.v1" appliesTo="v1.0.3705">  
</assemblyBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="61d74-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="61d74-108">Attributes and Elements</span></span>  
 <span data-ttu-id="61d74-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="61d74-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="61d74-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="61d74-110">Attributes</span></span>  
  
|<span data-ttu-id="61d74-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="61d74-111">Attribute</span></span>|<span data-ttu-id="61d74-112">Description</span><span class="sxs-lookup"><span data-stu-id="61d74-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="61d74-113">**xmlns**</span><span class="sxs-lookup"><span data-stu-id="61d74-113">**xmlns**</span></span>|<span data-ttu-id="61d74-114">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="61d74-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="61d74-115">Spécifie l'espace de noms XML requis pour la liaison d'assembly.</span><span class="sxs-lookup"><span data-stu-id="61d74-115">Specifies the XML namespace required for assembly binding.</span></span> <span data-ttu-id="61d74-116">Utilisez la chaîne « urn:schemas-microsoft-com:asm.v1 » comme valeur.</span><span class="sxs-lookup"><span data-stu-id="61d74-116">Use the string "urn:schemas-microsoft-com:asm.v1" as the value.</span></span>|  
|<span data-ttu-id="61d74-117">**appliesTo**</span><span class="sxs-lookup"><span data-stu-id="61d74-117">**appliesTo**</span></span>|<span data-ttu-id="61d74-118">Spécifie la version du runtime à laquelle s'applique la redirection d'assembly .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="61d74-118">Specifies the runtime version the .NET Framework assembly redirection applies to.</span></span> <span data-ttu-id="61d74-119">Cet attribut facultatif utilise un numéro de version .NET Framework pour indiquer la version à laquelle il s'applique.</span><span class="sxs-lookup"><span data-stu-id="61d74-119">This optional attribute uses a .NET Framework version number to indicate what version it applies to.</span></span> <span data-ttu-id="61d74-120">Si l’attribut **appliesTo** n’est pas spécifié, l’élément **\<assemblyBinding>** s’applique à toutes les versions du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="61d74-120">If no **appliesTo** attribute is specified, the **\<assemblyBinding>** element applies to all versions of the .NET Framework.</span></span> <span data-ttu-id="61d74-121">Le **appliesTo** attribut a été introduit dans .NET Framework version 1.1 ; il est ignoré par le .NET Framework version 1.0.</span><span class="sxs-lookup"><span data-stu-id="61d74-121">The **appliesTo** attribute was introduced in .NET Framework version 1.1; it is ignored by the .NET Framework version 1.0.</span></span> <span data-ttu-id="61d74-122">Cela signifie que tous les éléments **\<assemblyBinding>** sont appliqués lors de l’utilisation du .NET Framework 1.0, même si un attribut **appliesTo** est spécifié.</span><span class="sxs-lookup"><span data-stu-id="61d74-122">This means that all **\<assemblyBinding>** elements are applied when using the .NET Framework version 1.0, even if an **appliesTo** attribute is specified.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="61d74-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="61d74-123">Child Elements</span></span>  
  
|<span data-ttu-id="61d74-124">Élément</span><span class="sxs-lookup"><span data-stu-id="61d74-124">Element</span></span>|<span data-ttu-id="61d74-125">Description</span><span class="sxs-lookup"><span data-stu-id="61d74-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="61d74-126">\<dependentAssembly></span><span class="sxs-lookup"><span data-stu-id="61d74-126">\<dependentAssembly></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/dependentassembly-element.md)|<span data-ttu-id="61d74-127">Encapsule la stratégie de liaison et l’emplacement d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="61d74-127">Encapsulates binding policy and assembly location for an assembly.</span></span> <span data-ttu-id="61d74-128">Utilisez une  **\<dependentAssembly >** balise pour chaque assembly.</span><span class="sxs-lookup"><span data-stu-id="61d74-128">Use one **\<dependentAssembly>** tag for each assembly.</span></span>|  
|[<span data-ttu-id="61d74-129">\<probing></span><span class="sxs-lookup"><span data-stu-id="61d74-129">\<probing></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/probing-element.md)|<span data-ttu-id="61d74-130">Spécifie les sous-répertoires interrogés par le Common Language Runtime lors du chargement des assemblys.</span><span class="sxs-lookup"><span data-stu-id="61d74-130">Specifies subdirectories the common language runtime searches when loading assemblies.</span></span>|  
|[<span data-ttu-id="61d74-131">\<publisherPolicy></span><span class="sxs-lookup"><span data-stu-id="61d74-131">\<publisherPolicy></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/publisherpolicy-element.md)|<span data-ttu-id="61d74-132">Spécifie si le runtime applique la stratégie de l'éditeur.</span><span class="sxs-lookup"><span data-stu-id="61d74-132">Specifies whether the runtime applies publisher policy.</span></span>|  
|[<span data-ttu-id="61d74-133">\<qualifyAssembly></span><span class="sxs-lookup"><span data-stu-id="61d74-133">\<qualifyAssembly></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/qualifyassembly-element.md)|<span data-ttu-id="61d74-134">Spécifie le nom complet de l'assembly qui doit être chargé dynamiquement quand un nom partiel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="61d74-134">Specifies the full name of the assembly that should be dynamically loaded when a partial name is used.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="61d74-135">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="61d74-135">Parent Elements</span></span>  
  
|<span data-ttu-id="61d74-136">Élément</span><span class="sxs-lookup"><span data-stu-id="61d74-136">Element</span></span>|<span data-ttu-id="61d74-137">Description</span><span class="sxs-lookup"><span data-stu-id="61d74-137">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="61d74-138">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="61d74-138">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="61d74-139">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="61d74-139">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="61d74-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="61d74-140">Example</span></span>  
 <span data-ttu-id="61d74-141">L'exemple suivant montre comment rediriger une version d'assembly vers une autre et fournir une base de code.</span><span class="sxs-lookup"><span data-stu-id="61d74-141">The following example shows how to redirect one assembly version to another and provide a codebase.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <dependentAssembly>  
            <assemblyIdentity name="myAssembly"  
                              publicKeyToken="32ab4ba45e0a69a1"  
                              culture="neutral" />  
            <bindingRedirect oldVersion="1.0.0.0"  
                             newVersion="2.0.0.0"/>  
            <codeBase version="2.0.0.0"  
                      href="http://www.litwareinc.com/myAssembly.dll"/>  
         </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
 <span data-ttu-id="61d74-142">L’exemple suivant montre comment utiliser le **appliesTo** attribut pour rediriger la liaison d’un assembly .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="61d74-142">The following example shows how to use the **appliesTo** attribute to redirect binding of a .NET Framework assembly.</span></span>  
  
```xml  
<runtime>  
   <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1" appliesTo="v1.0.3705">  
      <dependentAssembly>   
         <assemblyIdentity name="mscorcfg" publicKeyToken="b03f5f7f11d50a3a" culture=""/>  
         <bindingRedirect oldVersion="0.0.0.0-65535.65535.65535.65535" newVersion="1.0.3300.0"/>  
      </dependentAssembly>  
   </assemblyBinding>  
</runtime>  
```  
  
## <a name="see-also"></a><span data-ttu-id="61d74-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61d74-143">See Also</span></span>  
 [<span data-ttu-id="61d74-144">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="61d74-144">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [<span data-ttu-id="61d74-145">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="61d74-145">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="61d74-146">Redirection des versions d'assemblys</span><span class="sxs-lookup"><span data-stu-id="61d74-146">Redirecting Assembly Versions</span></span>](../../../../../docs/framework/configure-apps/redirect-assembly-versions.md)
