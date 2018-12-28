---
title: '&lt;System.Runtime.Caching&gt; , élément (paramètres de Cache)'
ms.date: 03/30/2017
helpviewer_keywords:
- <system.runtime.caching> element
- caching [.NET Framework], configuration
- system.runtime.caching element
ms.assetid: 9b44daee-874a-4bd1-954e-83bf53565590
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: daa08bb8a92a13941093a77f580318558dc14e9c
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53610370"
---
# <a name="ltsystemruntimecachinggt-element-cache-settings"></a><span data-ttu-id="26a4c-102">&lt;System.Runtime.Caching&gt; , élément (paramètres de Cache)</span><span class="sxs-lookup"><span data-stu-id="26a4c-102">&lt;system.runtime.caching&gt; Element (Cache Settings)</span></span>
<span data-ttu-id="26a4c-103">Fournit la configuration pour l’implémentation de <xref:System.Runtime.Caching.ObjectCache> en mémoire par défaut via l’entrée `memoryCache` dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="26a4c-103">Provides configuration for the default in-memory <xref:System.Runtime.Caching.ObjectCache> implementation through the `memoryCache` entry in the configuration file.</span></span>  
  
 <span data-ttu-id="26a4c-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="26a4c-104">\<configuration></span></span>  
<span data-ttu-id="26a4c-105">\<system.runtime.caching></span><span class="sxs-lookup"><span data-stu-id="26a4c-105">\<system.runtime.caching></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26a4c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26a4c-106">Syntax</span></span>  
  
```xml  
<system.runtime.caching >  
   <!-- child elements -->  
</system.runtime.caching >  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="26a4c-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="26a4c-107">Attributes and Elements</span></span>  
 <span data-ttu-id="26a4c-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="26a4c-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="26a4c-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="26a4c-109">Attributes</span></span>  
 `None`  
  
### <a name="child-elements"></a><span data-ttu-id="26a4c-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="26a4c-110">Child Elements</span></span>  
  
|<span data-ttu-id="26a4c-111">Élément</span><span class="sxs-lookup"><span data-stu-id="26a4c-111">Element</span></span>|<span data-ttu-id="26a4c-112">Description</span><span class="sxs-lookup"><span data-stu-id="26a4c-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="26a4c-113">\<memoryCache></span><span class="sxs-lookup"><span data-stu-id="26a4c-113">\<memoryCache></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/memorycache-element-cache-settings.md)|<span data-ttu-id="26a4c-114">Définit un élément qui est utilisé pour configurer un cache basé sur la classe <xref:System.Runtime.Caching.MemoryCache> .</span><span class="sxs-lookup"><span data-stu-id="26a4c-114">Defines an element that is used to configure a cache that is based on the <xref:System.Runtime.Caching.MemoryCache> class.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="26a4c-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="26a4c-115">Parent Elements</span></span>  
  
|<span data-ttu-id="26a4c-116">Élément</span><span class="sxs-lookup"><span data-stu-id="26a4c-116">Element</span></span>|<span data-ttu-id="26a4c-117">Description</span><span class="sxs-lookup"><span data-stu-id="26a4c-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="26a4c-118">\<configuration></span><span class="sxs-lookup"><span data-stu-id="26a4c-118">\<configuration></span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|<span data-ttu-id="26a4c-119">Spécifie l’élément racine dans chaque fichier de configuration utilisé par le Common Language Runtime et les applications [!INCLUDE[dnprdnshort](../../../../../includes/dnprdnshort-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="26a4c-119">Specifies the root element in every configuration file that is used by the common language runtime and [!INCLUDE[dnprdnshort](../../../../../includes/dnprdnshort-md.md)] applications.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="26a4c-120">Notes</span><span class="sxs-lookup"><span data-stu-id="26a4c-120">Remarks</span></span>  
 <span data-ttu-id="26a4c-121">Les classes de cet espace de noms fournissent un moyen d’utiliser des fonctionnalités de mise en cache comme celles d’ASP.NET, mais sans dépendance de l’assembly `System.Web` .</span><span class="sxs-lookup"><span data-stu-id="26a4c-121">The classes in this namespace provide a way to use caching facilities like those in ASP.NET, but without a dependency on the `System.Web` assembly.</span></span> <span data-ttu-id="26a4c-122">Pour plus d'informations, consultez [Caching in .NET Framework Applications](../../../../../docs/framework/performance/caching-in-net-framework-applications.md).</span><span class="sxs-lookup"><span data-stu-id="26a4c-122">For more information, see [Caching in .NET Framework Applications](../../../../../docs/framework/performance/caching-in-net-framework-applications.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="26a4c-123">Les fonctionnalités et les types de mise en cache en sortie dans l’espace de noms <xref:System.Runtime.Caching> sont nouveaux dans [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="26a4c-123">The output caching functionality and types in the <xref:System.Runtime.Caching> namespace are new in [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="example"></a><span data-ttu-id="26a4c-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="26a4c-124">Example</span></span>  
 <span data-ttu-id="26a4c-125">L’exemple suivant montre comment configurer un cache basé sur la classe <xref:System.Runtime.Caching.MemoryCache> .</span><span class="sxs-lookup"><span data-stu-id="26a4c-125">The following example shows how to configure a cache that is based on the <xref:System.Runtime.Caching.MemoryCache> class.</span></span> <span data-ttu-id="26a4c-126">L’exemple montre comment configurer une instance de l’entrée `namedCaches` pour le cache mémoire.</span><span class="sxs-lookup"><span data-stu-id="26a4c-126">The example shows how to configure an instance of the `namedCaches` entry for memory cache.</span></span> <span data-ttu-id="26a4c-127">Le nom du cache est défini sur le nom de l’entrée du cache par défaut en définissant l’attribut `name` sur « default ».</span><span class="sxs-lookup"><span data-stu-id="26a4c-127">The name of the cache is set to the default cache entry name by setting the `name` attribute to "default".</span></span>  
  
 <span data-ttu-id="26a4c-128">Les attributs `cacheMemoryLimitMegabytes` et `physicalMemoryPercentage` sont définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="26a4c-128">The `cacheMemoryLimitMegabytes` attribute and the `physicalMemoryPercentage` attribute are set to zero.</span></span> <span data-ttu-id="26a4c-129">La définition de ces attributs sur zéro signifie que les heuristiques à dimensionnement automatique de <xref:System.Runtime.Caching.MemoryCache> sont utilisées par défaut.</span><span class="sxs-lookup"><span data-stu-id="26a4c-129">Setting these attributes to zero means that the <xref:System.Runtime.Caching.MemoryCache> autosizing heuristics are used by default.</span></span> <span data-ttu-id="26a4c-130">L’implémentation du cache doit comparer la charge de mémoire actuelle aux limites de mémoire en valeur absolue et en pourcentage toutes les deux minutes.</span><span class="sxs-lookup"><span data-stu-id="26a4c-130">The cache implementation should compare the current memory load against the absolute and percentage-based memory limits every two minutes.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="26a4c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26a4c-131">See Also</span></span>  
- [<span data-ttu-id="26a4c-132">\<memoryCache >, élément (paramètres de Cache)</span><span class="sxs-lookup"><span data-stu-id="26a4c-132">\<memoryCache> Element (Cache Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/memorycache-element-cache-settings.md)
