---
title: <memoryCache>, élément (Paramètres de cache)
ms.date: 03/30/2017
helpviewer_keywords:
- <memoryCache> element
- caching [.NET Framework], configuration
- memoryCache element
ms.assetid: 182a622f-f7cf-472d-9d0b-451d2fd94525
ms.openlocfilehash: 25e87aa9fa4e56c5042eb25c41f6cfe1b65aea24
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55266375"
---
# <a name="memorycache-element-cache-settings"></a><span data-ttu-id="d25aa-102">\<memoryCache >, élément (paramètres de Cache)</span><span class="sxs-lookup"><span data-stu-id="d25aa-102">\<memoryCache> Element (Cache Settings)</span></span>
<span data-ttu-id="d25aa-103">Définit un élément qui est utilisé pour configurer un cache basé sur la classe <xref:System.Runtime.Caching.MemoryCache> .</span><span class="sxs-lookup"><span data-stu-id="d25aa-103">Defines an element that is used to configure a cache that is based on the <xref:System.Runtime.Caching.MemoryCache> class.</span></span> <span data-ttu-id="d25aa-104">La classe <xref:System.Runtime.Caching.Configuration.MemoryCacheElement> définit un élément [memoryCache](../../../../../docs/framework/configure-apps/file-schema/runtime/memorycache-element-cache-settings.md) que vous pouvez utiliser pour configurer le cache.</span><span class="sxs-lookup"><span data-stu-id="d25aa-104">The <xref:System.Runtime.Caching.Configuration.MemoryCacheElement> class defines a [memoryCache](../../../../../docs/framework/configure-apps/file-schema/runtime/memorycache-element-cache-settings.md) element that you can use to configure the cache.</span></span> <span data-ttu-id="d25aa-105">Vous pouvez utiliser plusieurs instances de la classe <xref:System.Runtime.Caching.MemoryCache> dans une même application.</span><span class="sxs-lookup"><span data-stu-id="d25aa-105">Multiple instances of the <xref:System.Runtime.Caching.MemoryCache> class can be used in a single application.</span></span> <span data-ttu-id="d25aa-106">Chaque élément `memoryCache` dans le fichier de configuration peut contenir des paramètres pour une instance <xref:System.Runtime.Caching.MemoryCache> nommée.</span><span class="sxs-lookup"><span data-stu-id="d25aa-106">Each `memoryCache` element in the configuration file can contain settings for a named <xref:System.Runtime.Caching.MemoryCache> instance.</span></span>  
  
 <span data-ttu-id="d25aa-107">\<configuration></span><span class="sxs-lookup"><span data-stu-id="d25aa-107">\<configuration></span></span>  
<span data-ttu-id="d25aa-108">\<system.runtime.caching></span><span class="sxs-lookup"><span data-stu-id="d25aa-108">\<system.runtime.caching></span></span>  
<span data-ttu-id="d25aa-109">\<memoryCache></span><span class="sxs-lookup"><span data-stu-id="d25aa-109">\<memoryCache></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d25aa-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d25aa-110">Syntax</span></span>  
  
```xml  
<memoryCache>   
    <namedCaches>  
        <!-- child elements -->  
    </namedCaches>   
</memoryCache>  
```  
  
## <a name="type"></a><span data-ttu-id="d25aa-111">Type</span><span class="sxs-lookup"><span data-stu-id="d25aa-111">Type</span></span>  
 <span data-ttu-id="d25aa-112">Classe<xref:System.Runtime.Caching.MemoryCache> .</span><span class="sxs-lookup"><span data-stu-id="d25aa-112"><xref:System.Runtime.Caching.MemoryCache> class.</span></span>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d25aa-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d25aa-113">Attributes and Elements</span></span>  
 <span data-ttu-id="d25aa-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d25aa-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d25aa-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="d25aa-115">Attributes</span></span>  
  
|<span data-ttu-id="d25aa-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="d25aa-116">Attribute</span></span>|<span data-ttu-id="d25aa-117">Description</span><span class="sxs-lookup"><span data-stu-id="d25aa-117">Description</span></span>|  
|---------------|-----------------|  
|`CacheMemoryLimitMegabytes`|<span data-ttu-id="d25aa-118">Taille de mémoire maximale, en mégaoctets, que peut atteindre une instance d’un objet <xref:System.Runtime.Caching.MemoryCache> .</span><span class="sxs-lookup"><span data-stu-id="d25aa-118">The maximum memory size, in megabytes, that an instance of a <xref:System.Runtime.Caching.MemoryCache> object can grow to.</span></span> <span data-ttu-id="d25aa-119">La valeur par défaut est 0, ce qui signifie que l’heuristique de dimensionnement automatique de la classe <xref:System.Runtime.Caching.MemoryCache> est utilisée par défaut.</span><span class="sxs-lookup"><span data-stu-id="d25aa-119">The default value is 0, which means that the <xref:System.Runtime.Caching.MemoryCache> class's autosize heuristics are used by default.</span></span>|  
|`Name`|<span data-ttu-id="d25aa-120">Nom de la configuration du cache.</span><span class="sxs-lookup"><span data-stu-id="d25aa-120">The name of the cache configuration.</span></span>|  
|`PhysicalMemoryLimitPercentage`|<span data-ttu-id="d25aa-121">Pourcentage de mémoire physique pouvant être utilisé par le cache.</span><span class="sxs-lookup"><span data-stu-id="d25aa-121">The percentage of physical memory that can be used by the cache.</span></span> <span data-ttu-id="d25aa-122">La valeur par défaut est 0, ce qui signifie que l’heuristique de dimensionnement automatique de la classe <xref:System.Runtime.Caching.MemoryCache> est utilisée par défaut.</span><span class="sxs-lookup"><span data-stu-id="d25aa-122">The default value is 0, which means that the <xref:System.Runtime.Caching.MemoryCache> class's autosize heuristics are used by default.</span></span>|  
|`PollingInterval`|<span data-ttu-id="d25aa-123">Valeur qui indique l’intervalle de temps après lequel l’implémentation de cache compare la charge de mémoire actuelle aux limites de mémoire absolue et en pourcentage définies pour l’instance de cache.</span><span class="sxs-lookup"><span data-stu-id="d25aa-123">A value that indicates the time interval after which the cache implementation compares the current memory load against the absolute and percentage-based memory limits that are set for the cache instance.</span></span> <span data-ttu-id="d25aa-124">La valeur est entrée au format « HH:MM:SS ».</span><span class="sxs-lookup"><span data-stu-id="d25aa-124">The value is entered in "HH:MM:SS" format.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d25aa-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d25aa-125">Child Elements</span></span>  
  
|<span data-ttu-id="d25aa-126">Élément</span><span class="sxs-lookup"><span data-stu-id="d25aa-126">Element</span></span>|<span data-ttu-id="d25aa-127">Description</span><span class="sxs-lookup"><span data-stu-id="d25aa-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d25aa-128">\<namedCaches></span><span class="sxs-lookup"><span data-stu-id="d25aa-128">\<namedCaches></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)|<span data-ttu-id="d25aa-129">Contient une collection de paramètres de configuration pour l’instance `namedCache` .</span><span class="sxs-lookup"><span data-stu-id="d25aa-129">Contains a collection of configuration settings for the `namedCache` instance.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d25aa-130">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d25aa-130">Parent Elements</span></span>  
  
|<span data-ttu-id="d25aa-131">Élément</span><span class="sxs-lookup"><span data-stu-id="d25aa-131">Element</span></span>|<span data-ttu-id="d25aa-132">Description</span><span class="sxs-lookup"><span data-stu-id="d25aa-132">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d25aa-133">\<system.runtime.caching></span><span class="sxs-lookup"><span data-stu-id="d25aa-133">\<system.runtime.caching></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/system-runtime-caching-element-cache-settings.md)|<span data-ttu-id="d25aa-134">Contient des types qui vous permettent d’implémenter la mise en cache de sortie dans les applications intégrées au [!INCLUDE[dnprdnshort](../../../../../includes/dnprdnshort-md.md)].</span><span class="sxs-lookup"><span data-stu-id="d25aa-134">Contains types that let you implement output caching in applications that are built into the [!INCLUDE[dnprdnshort](../../../../../includes/dnprdnshort-md.md)].</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d25aa-135">Notes</span><span class="sxs-lookup"><span data-stu-id="d25aa-135">Remarks</span></span>  
 <span data-ttu-id="d25aa-136">La classe <xref:System.Runtime.Caching.MemoryCache> est une implémentation concrète de la classe <xref:System.Runtime.Caching.ObjectCache> abstraite.</span><span class="sxs-lookup"><span data-stu-id="d25aa-136">The <xref:System.Runtime.Caching.MemoryCache> class is a concrete implementation of the abstract <xref:System.Runtime.Caching.ObjectCache> class.</span></span> <span data-ttu-id="d25aa-137">Les instances de la classe <xref:System.Runtime.Caching.MemoryCache> peuvent être fournies avec les informations de configuration tirées des fichiers de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="d25aa-137">Instances of the <xref:System.Runtime.Caching.MemoryCache> class can be supplied with configuration information from application configuration files.</span></span> <span data-ttu-id="d25aa-138">La section de configuration [memoryCache](../../../../../docs/framework/configure-apps/file-schema/runtime/memorycache-element-cache-settings.md) contient une collection de configurations `namedCaches` .</span><span class="sxs-lookup"><span data-stu-id="d25aa-138">The [memoryCache](../../../../../docs/framework/configure-apps/file-schema/runtime/memorycache-element-cache-settings.md) configuration section contains a `namedCaches` configuration collection.</span></span>  
  
 <span data-ttu-id="d25aa-139">Quand un objet cache en mémoire est initialisé, il essaie tout d’abord de trouver une entrée `namedCaches` qui correspond au nom mentionné dans le paramètre passé au constructeur du cache mémoire.</span><span class="sxs-lookup"><span data-stu-id="d25aa-139">When a memory-based cache object is initialized, it first tries to find a `namedCaches` entry that matches the name in the parameter that is passed to the memory cache constructor.</span></span> <span data-ttu-id="d25aa-140">S’il trouve une entrée `namedCaches` , les informations de gestion de la mémoire et d’interrogation sont récupérées à partir du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="d25aa-140">If a `namedCaches` entry is found, the polling and memory-management information are retrieved from the configuration file.</span></span>  
  
 <span data-ttu-id="d25aa-141">Le processus d’initialisation détermine ensuite si des entrées de configuration ont été substituées, en utilisant la collection facultative de paires nom/valeur d’informations de configuration dans le constructeur.</span><span class="sxs-lookup"><span data-stu-id="d25aa-141">The initialization process then determines whether any configuration entries were overridden, by using the optional collection of name/value pairs of configuration information in the constructor.</span></span> <span data-ttu-id="d25aa-142">Si vous passez l’une des valeurs suivantes dans la collection de paires nom/valeur, ces valeurs remplacent les informations obtenues à partir du fichier de configuration :</span><span class="sxs-lookup"><span data-stu-id="d25aa-142">If you pass any one of the following values in the name/value pair collection, these values override information obtained from the configuration file:</span></span>  
  
-   <xref:System.Runtime.Caching.Configuration.MemoryCacheElement.CacheMemoryLimitMegabytes%2A>  
  
-   <xref:System.Runtime.Caching.Configuration.MemoryCacheElement.PhysicalMemoryLimitPercentage%2A>  
  
-   <xref:System.Runtime.Caching.MemoryCache.PollingInterval%2A>  
  
## <a name="example"></a><span data-ttu-id="d25aa-143">Exemple</span><span class="sxs-lookup"><span data-stu-id="d25aa-143">Example</span></span>  
 <span data-ttu-id="d25aa-144">L’exemple suivant montre comment affecter le nom d’objet cache par défaut comme nom de l’objet <xref:System.Runtime.Caching.MemoryCache> en affectant la valeur « default » à l’attribut `name` .</span><span class="sxs-lookup"><span data-stu-id="d25aa-144">The following example shows how to set the name of the <xref:System.Runtime.Caching.MemoryCache> object to the default cache object name by setting the `name` attribute to "default".</span></span>  
  
 <span data-ttu-id="d25aa-145">Les attributs `cacheMemoryLimitMegabytes` et `physicalMemoryLimitPercentage` sont définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="d25aa-145">The `cacheMemoryLimitMegabytes` attribute and the `physicalMemoryLimitPercentage` attribute are set to zero.</span></span> <span data-ttu-id="d25aa-146">La définition de ces attributs sur zéro signifie que les heuristiques à dimensionnement automatique de <xref:System.Runtime.Caching.MemoryCache> sont utilisées par défaut.</span><span class="sxs-lookup"><span data-stu-id="d25aa-146">Setting these attributes to zero means that the <xref:System.Runtime.Caching.MemoryCache> autosizing heuristics are used by default.</span></span> <span data-ttu-id="d25aa-147">L’implémentation du cache doit comparer la charge de mémoire actuelle aux limites de mémoire en valeur absolue et en pourcentage toutes les deux minutes.</span><span class="sxs-lookup"><span data-stu-id="d25aa-147">The cache implementation should compare the current memory load against the absolute and percentage-based memory limits every two minutes.</span></span>  
  
```xml  
<configuration>  
  <system.runtime.caching>  
    <memoryCache>  
      <namedCaches>  
          <add name="default"   
               cacheMemoryLimitMegabytes="0"   
               physicalMemoryLimitPercentage="0"  
               pollingInterval="00:02:00" />  
      </namedCaches>  
    </memoryCache>  
  </system.runtime.caching>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="d25aa-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d25aa-148">See also</span></span>
- <xref:System.Runtime.Caching.MemoryCache>
- [<span data-ttu-id="d25aa-149">\<System.Runtime.Caching >, élément (paramètres de Cache)</span><span class="sxs-lookup"><span data-stu-id="d25aa-149">\<system.runtime.caching> Element (Cache Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/system-runtime-caching-element-cache-settings.md)
- [<span data-ttu-id="d25aa-150">\<namedCaches >, élément (paramètres de Cache)</span><span class="sxs-lookup"><span data-stu-id="d25aa-150">\<namedCaches> Element (Cache Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)
