---
title: Élément <forcePerformanceCounterUniqueSharedMemoryReads>
ms.date: 03/30/2017
helpviewer_keywords:
- forcePerformanceCounterUniqueSharedMemoryReads element
- <forcePerformanceCounterUniqueSharedMemoryReads> element
ms.assetid: 91149858-4810-4f65-9b48-468488172c9b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1d4a205f643c844b2fe77d3aa5211b4bc1f322fd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59186964"
---
# <a name="forceperformancecounteruniquesharedmemoryreads-element"></a><span data-ttu-id="e020e-102">\<forcePerformanceCounterUniqueSharedMemoryReads> Element</span><span class="sxs-lookup"><span data-stu-id="e020e-102">\<forcePerformanceCounterUniqueSharedMemoryReads> Element</span></span>
<span data-ttu-id="e020e-103">Indique si PerfCounter.dll utilise le paramètre de Registre CategoryOptions dans une application.NET Framework version 1.1 pour déterminer s’il faut charger des données du compteur de performance à partir de la mémoire globale ou de la mémoire partagée propre à la catégorie.</span><span class="sxs-lookup"><span data-stu-id="e020e-103">Specifies whether PerfCounter.dll uses the CategoryOptions registry setting in a .NET Framework version 1.1 application to determine whether to load performance counter data from category-specific shared memory or global memory.</span></span>  
  
 <span data-ttu-id="e020e-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="e020e-104">\<configuration></span></span>  
<span data-ttu-id="e020e-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="e020e-105">\<runtime></span></span>  
<span data-ttu-id="e020e-106">\<forcePerformanceCounterUniqueSharedMemoryReads></span><span class="sxs-lookup"><span data-stu-id="e020e-106">\<forcePerformanceCounterUniqueSharedMemoryReads></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e020e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e020e-107">Syntax</span></span>  
  
```xml  
<forcePerformanceCounterUniqueSharedMemoryReads   
enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e020e-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e020e-108">Attributes and Elements</span></span>  
 <span data-ttu-id="e020e-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e020e-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e020e-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="e020e-110">Attributes</span></span>  
  
|<span data-ttu-id="e020e-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="e020e-111">Attribute</span></span>|<span data-ttu-id="e020e-112">Description</span><span class="sxs-lookup"><span data-stu-id="e020e-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="e020e-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="e020e-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="e020e-114">Indique si PerfCounter.dll utilise le paramètre de Registre CategoryOptions pour déterminer s’il faut charger des données de compteur de performances à partir de la mémoire partagée spécifique à la catégorie ou de la mémoire globale.</span><span class="sxs-lookup"><span data-stu-id="e020e-114">Indicates whether PerfCounter.dll uses the CategoryOptions registry setting to determine whether to load performance counter data from category-specific shared memory or global memory.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="e020e-115">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="e020e-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="e020e-116">Value</span><span class="sxs-lookup"><span data-stu-id="e020e-116">Value</span></span>|<span data-ttu-id="e020e-117">Description</span><span class="sxs-lookup"><span data-stu-id="e020e-117">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="e020e-118">PerfCounter.dll n’utilise pas les CategoryOptions ce paramètre de Registre est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e020e-118">PerfCounter.dll does not use the CategoryOptions registry setting This is the default.</span></span>|  
|`true`|<span data-ttu-id="e020e-119">PerfCounter.dll n’utilise pas le paramètre de Registre CategoryOptions.</span><span class="sxs-lookup"><span data-stu-id="e020e-119">PerfCounter.dll does use the CategoryOptions registry setting.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e020e-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e020e-120">Child Elements</span></span>  
 <span data-ttu-id="e020e-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e020e-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e020e-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e020e-122">Parent Elements</span></span>  
  
|<span data-ttu-id="e020e-123">Élément</span><span class="sxs-lookup"><span data-stu-id="e020e-123">Element</span></span>|<span data-ttu-id="e020e-124">Description</span><span class="sxs-lookup"><span data-stu-id="e020e-124">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="e020e-125">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e020e-125">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="e020e-126">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="e020e-126">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e020e-127">Notes</span><span class="sxs-lookup"><span data-stu-id="e020e-127">Remarks</span></span>  
 <span data-ttu-id="e020e-128">Dans les versions du .NET Framework avant le [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)], la version de PerfCounter.dll chargée correspondait à l’exécution qui a été chargée dans le processus.</span><span class="sxs-lookup"><span data-stu-id="e020e-128">In versions of the .NET Framework before the [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)], the version of PerfCounter.dll that was loaded corresponded to the runtime that was loaded in the process.</span></span> <span data-ttu-id="e020e-129">Si un ordinateur avait à la fois le .NET Framework version 1.1 et le [!INCLUDE[dnprdnlong](../../../../../includes/dnprdnlong-md.md)] installé, une application .NET Framework 1.1 chargerait le .NET Framework version 1.1 de PerfCounter.dll.</span><span class="sxs-lookup"><span data-stu-id="e020e-129">If a computer had both the .NET Framework version 1.1 and the [!INCLUDE[dnprdnlong](../../../../../includes/dnprdnlong-md.md)] installed, a .NET Framework 1.1 application would load the .NET Framework 1.1 version of PerfCounter.dll.</span></span> <span data-ttu-id="e020e-130">En commençant par le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], la dernière version installée de PerfCounter.dll est chargée.</span><span class="sxs-lookup"><span data-stu-id="e020e-130">Starting with the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], the newest installed version of PerfCounter.dll is loaded.</span></span> <span data-ttu-id="e020e-131">Cela signifie qu’une application .NET Framework 1.1 chargera le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] version de PerfCounter.dll si le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] est installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e020e-131">This means that a .NET Framework 1.1 application will load the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] version of PerfCounter.dll if the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] is installed on the computer.</span></span>  
  
 <span data-ttu-id="e020e-132">En commençant par le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], lors de l’utilisation des compteurs de performance, PerfCounter.dll vérifie l’entrée de Registre CategoryOptions pour chaque fournisseur pour déterminer s’il doit lire à partir de la mémoire partagée spécifique à la catégorie ou de la mémoire partagée globale.</span><span class="sxs-lookup"><span data-stu-id="e020e-132">Starting with the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], when consuming performance counters, PerfCounter.dll checks the CategoryOptions registry entry for each provider to determine whether it should read from category-specific shared memory or global shared memory.</span></span> <span data-ttu-id="e020e-133">Le PerfCounter.dll .NET Framework 1.1 ne lit pas cette entrée de Registre, car elle n’a pas connaissance de la mémoire partagée spécifique à la catégorie ; Il lit toujours à partir de la mémoire partagée globale.</span><span class="sxs-lookup"><span data-stu-id="e020e-133">The .NET Framework 1.1 PerfCounter.dll does not read that registry entry, because it is not aware of category-specific shared memory; it always reads from global shared memory.</span></span>  
  
 <span data-ttu-id="e020e-134">Pour la compatibilité descendante, le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] PerfCounter.dll ne vérifie pas l’entrée de Registre CategoryOptions lors de l’exécution dans une application .NET Framework 1.1.</span><span class="sxs-lookup"><span data-stu-id="e020e-134">For backward compatibility, the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] PerfCounter.dll does not check the CategoryOptions registry entry when running in a .NET Framework 1.1 application.</span></span> <span data-ttu-id="e020e-135">Elle utilise simplement la mémoire partagée globale, comme le PerfCounter.dll .NET Framework 1.1.</span><span class="sxs-lookup"><span data-stu-id="e020e-135">It simply uses global shared memory, just like the .NET Framework 1.1 PerfCounter.dll.</span></span> <span data-ttu-id="e020e-136">Toutefois, vous pouvez indiquer le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] PerfCounter.dll pour vérifier le paramètre de Registre en activant le `<forcePerformanceCounterUniqueSharedMemoryReads>` élément.</span><span class="sxs-lookup"><span data-stu-id="e020e-136">However, you can instruct the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] PerfCounter.dll to check the registry setting by enabling the `<forcePerformanceCounterUniqueSharedMemoryReads>` element.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e020e-137">L’activation de la `<forcePerformanceCounterUniqueSharedMemoryReads>` élément ne garantit pas que la mémoire partagée spécifique à la catégorie sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="e020e-137">Enabling the `<forcePerformanceCounterUniqueSharedMemoryReads>` element does not guarantee that category-specific shared memory will be used.</span></span> <span data-ttu-id="e020e-138">Paramètre est activé à `true` uniquement, PerfCounter.dll référence le paramètre du Registre CategoryOptions.</span><span class="sxs-lookup"><span data-stu-id="e020e-138">Setting enabled to `true` only causes PerfCounter.dll to reference the CategoryOptions registry setting.</span></span> <span data-ttu-id="e020e-139">Le paramètre par défaut CategoryOptions consiste à utiliser la mémoire partagée spécifique à la catégorie ; Toutefois, vous pouvez modifier CategoryOptions pour indiquer que la mémoire partagée globale doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="e020e-139">The default setting for CategoryOptions is to use category-specific shared memory; however, you can change CategoryOptions to indicate that global shared memory should be used.</span></span>  
  
 <span data-ttu-id="e020e-140">La clé de Registre qui contient le paramètre CategoryOptions est HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\\< categoryName\>\Performance.</span><span class="sxs-lookup"><span data-stu-id="e020e-140">The registry key that contains the CategoryOptions setting is HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\\<categoryName\>\Performance.</span></span> <span data-ttu-id="e020e-141">Par défaut, CategoryOptions a la valeur 3, qui indique à PerfCounter.dll d’utiliser la mémoire partagée spécifique à la catégorie.</span><span class="sxs-lookup"><span data-stu-id="e020e-141">By default, CategoryOptions is set to 3, which instructs PerfCounter.dll to use category-specific shared memory.</span></span> <span data-ttu-id="e020e-142">Si CategoryOptions est définie sur 0, PerfCounter.dll utilise la mémoire partagée globale.</span><span class="sxs-lookup"><span data-stu-id="e020e-142">If CategoryOptions is set to 0, PerfCounter.dll uses global shared memory.</span></span> <span data-ttu-id="e020e-143">Données d’instance seront réutilisées uniquement si le nom de l’instance en cours de création est identique à l’instance est réutilisé.</span><span class="sxs-lookup"><span data-stu-id="e020e-143">Instance data will be reused only if the name of the instance being created is identical to the instance being reused.</span></span> <span data-ttu-id="e020e-144">Toutes les versions seront en mesure d’écrire à la catégorie.</span><span class="sxs-lookup"><span data-stu-id="e020e-144">All versions will be able to write to the category.</span></span> <span data-ttu-id="e020e-145">Si CategoryOptions est définie sur 1, mémoire partagée globale est utilisée, mais les données d’instance peuvent être réutilisées si le nom de catégorie est la même longueur que la catégorie est réutilisée.</span><span class="sxs-lookup"><span data-stu-id="e020e-145">If CategoryOptions is set to 1, global shared memory is used, but instance data can be reused if the category name is the same length as the category being reused.</span></span>  
  
 <span data-ttu-id="e020e-146">Les paramètres 0 et 1 peuvent entraîner des fuites de mémoire et la saturation de mémoire de compteur de performances.</span><span class="sxs-lookup"><span data-stu-id="e020e-146">The settings 0 and 1 can lead to memory leaks and the filling up of performance counter memory.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e020e-147">Exemple</span><span class="sxs-lookup"><span data-stu-id="e020e-147">Example</span></span>  
 <span data-ttu-id="e020e-148">L’exemple suivant montre comment spécifier que PerfCounter.dll doit référencer l’entrée de Registre CategoryOptions pour déterminer s’il doit utiliser la mémoire partagée spécifique à la catégorie.</span><span class="sxs-lookup"><span data-stu-id="e020e-148">The following example shows how to specify that PerfCounter.dll should reference the CategoryOptions registry entry to determine whether it should use category-specific shared memory.</span></span>  
  
```xml  
<configuration>  
  <runtime>  
    <forcePerformanceCounterUniqueSharedMemoryReads enabled="true"/>  
  </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="e020e-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e020e-149">See also</span></span>

- [<span data-ttu-id="e020e-150">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="e020e-150">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="e020e-151">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="e020e-151">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
