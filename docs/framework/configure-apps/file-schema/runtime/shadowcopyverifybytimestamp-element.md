---
title: Élément <shadowCopyVerifyByTimestamp>
ms.date: 03/30/2017
helpviewer_keywords:
- <shadowCopyTimeStampVerification> element
- shadowCopyTimeStampVerification element
ms.assetid: 2f1648e5-997b-435e-a4f9-d236c574c66c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4ad61b3824b8155cf3f68f61865891c023b4cf32
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59216412"
---
# <a name="shadowcopyverifybytimestamp-element"></a><span data-ttu-id="e1b84-102">\<shadowCopyVerifyByTimestamp> Element</span><span class="sxs-lookup"><span data-stu-id="e1b84-102">\<shadowCopyVerifyByTimestamp> Element</span></span>
<span data-ttu-id="e1b84-103">Indique si les clichés instantanés utilisent le comportement de démarrage par défaut introduit dans le [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)], ou reviennent au comportement de démarrage des versions précédentes du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e1b84-103">Specifies whether shadow copying uses the default startup behavior introduced in the [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)], or reverts to the startup behavior of earlier versions of the .NET Framework.</span></span>  
  
 <span data-ttu-id="e1b84-104">\<configuration > élément</span><span class="sxs-lookup"><span data-stu-id="e1b84-104">\<configuration> Element</span></span>  
<span data-ttu-id="e1b84-105">\<runtime > élément</span><span class="sxs-lookup"><span data-stu-id="e1b84-105">\<runtime> Element</span></span>  
<span data-ttu-id="e1b84-106">\<shadowCopyVerifyByTimestamp> Element</span><span class="sxs-lookup"><span data-stu-id="e1b84-106">\<shadowCopyVerifyByTimestamp> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e1b84-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1b84-107">Syntax</span></span>  
  
```xml  
<shadowCopyVerifyByTimestamp enabled="true|false" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e1b84-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e1b84-108">Attributes and Elements</span></span>  
 <span data-ttu-id="e1b84-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e1b84-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e1b84-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="e1b84-110">Attributes</span></span>  
  
|<span data-ttu-id="e1b84-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="e1b84-111">Attribute</span></span>|<span data-ttu-id="e1b84-112">Description</span><span class="sxs-lookup"><span data-stu-id="e1b84-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e1b84-113">enabled</span><span class="sxs-lookup"><span data-stu-id="e1b84-113">enabled</span></span>|<span data-ttu-id="e1b84-114">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="e1b84-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="e1b84-115">Spécifie si les domaines d’application qui utilisent les clichés instantanés comparer les horodatages d’assembly au démarrage, afin de déterminer si un assembly a été mis à jour avant de l’assembly les clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="e1b84-115">Specifies whether application domains that use shadow copying compare assembly time stamps when starting up, to determine whether an assembly has been updated before shadow copying the assembly.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="e1b84-116">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="e1b84-116">enabled Attribute</span></span>  
  
|<span data-ttu-id="e1b84-117">Value</span><span class="sxs-lookup"><span data-stu-id="e1b84-117">Value</span></span>|<span data-ttu-id="e1b84-118">Description</span><span class="sxs-lookup"><span data-stu-id="e1b84-118">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="e1b84-119">true</span><span class="sxs-lookup"><span data-stu-id="e1b84-119">true</span></span>|<span data-ttu-id="e1b84-120">Au démarrage, copie uniquement les assemblys qui ont été mis à jour dans la mesure où ils ont été dernière copiés dans le répertoire des clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="e1b84-120">At startup, copies only assemblies that have been updated since they were last copied to the shadow copy directory.</span></span> <span data-ttu-id="e1b84-121">Il s’agit par défaut pour le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)].</span><span class="sxs-lookup"><span data-stu-id="e1b84-121">This is the default for the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)].</span></span>|  
|<span data-ttu-id="e1b84-122">False</span><span class="sxs-lookup"><span data-stu-id="e1b84-122">false</span></span>|<span data-ttu-id="e1b84-123">Rétablit le comportement de démarrage des versions antérieures du .NET Framework, qui consiste à copier tous les fichiers au démarrage.</span><span class="sxs-lookup"><span data-stu-id="e1b84-123">Reverts to the startup behavior of previous versions of the .NET Framework, which was to copy all files at startup.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e1b84-124">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e1b84-124">Child Elements</span></span>  
 <span data-ttu-id="e1b84-125">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e1b84-125">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e1b84-126">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e1b84-126">Parent Elements</span></span>  
  
|<span data-ttu-id="e1b84-127">Élément</span><span class="sxs-lookup"><span data-stu-id="e1b84-127">Element</span></span>|<span data-ttu-id="e1b84-128">Description</span><span class="sxs-lookup"><span data-stu-id="e1b84-128">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="e1b84-129">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e1b84-129">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="e1b84-130">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="e1b84-130">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e1b84-131">Notes</span><span class="sxs-lookup"><span data-stu-id="e1b84-131">Remarks</span></span>  
 <span data-ttu-id="e1b84-132">En commençant par le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], les assemblys sont des clichés instantanés uniquement si leurs horodatages indiquent qu’ils ont été modifiés depuis leur dernière copie dans le répertoire des clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="e1b84-132">Starting with the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], assemblies are shadow copied only if their time stamps indicate that they have changed since they were last copied to the shadow copy directory.</span></span> <span data-ttu-id="e1b84-133">Cela améliore les temps de démarrage pour de nombreuses applications qui utilisent les clichés instantanés, comme décrit dans [clichés instantanés d’assemblys](../../../../../docs/framework/app-domains/shadow-copy-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="e1b84-133">This improves startup times for many applications that use shadow copying, as described in [Shadow Copying Assemblies](../../../../../docs/framework/app-domains/shadow-copy-assemblies.md).</span></span> <span data-ttu-id="e1b84-134">Les applications qui ont un pourcentage élevé et la fréquence des mises à jour de l’assembly ne sera peut-être pas avantageux à partir de ce changement de comportement.</span><span class="sxs-lookup"><span data-stu-id="e1b84-134">Applications that have a high percentage and frequency of assembly updates might not benefit from this change in behavior.</span></span> <span data-ttu-id="e1b84-135">Dans ce cas, vous pouvez utiliser cet élément pour restaurer le comportement des versions antérieures du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e1b84-135">In that case, you can use this element to restore the behavior of previous versions of the .NET Framework.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e1b84-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="e1b84-136">Example</span></span>  
 <span data-ttu-id="e1b84-137">L’exemple suivant montre comment désactiver le comportement de démarrage par défaut des clichés instantanés dans le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)]et rétablir le comportement de démarrage des versions antérieures du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e1b84-137">The following example shows how to disable the default startup behavior of shadow copying in the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], and revert to the startup behavior of previous versions of the .NET Framework.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <shadowCopyVerifyByTimestamp enabled="false" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="e1b84-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1b84-138">See also</span></span>

- [<span data-ttu-id="e1b84-139">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="e1b84-139">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="e1b84-140">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="e1b84-140">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="e1b84-141">Clichés instantanés d'assemblys</span><span class="sxs-lookup"><span data-stu-id="e1b84-141">Shadow Copying Assemblies</span></span>](../../../../../docs/framework/app-domains/shadow-copy-assemblies.md)
