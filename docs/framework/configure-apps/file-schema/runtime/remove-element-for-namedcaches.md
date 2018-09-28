---
title: '&lt;supprimer&gt; élément pour &lt;namedCaches&gt;'
ms.date: 03/30/2017
helpviewer_keywords:
- remove element for namedCaches
- <remove> element for namedCaches
ms.assetid: 24211ea5-163e-4fe5-aed8-004d8499760c
author: mcleblanc
ms.author: markl
ms.openlocfilehash: f885416629ae58949cc688f4e6fbd41e77e872aa
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2018
ms.locfileid: "47425808"
---
# <a name="ltremovegt-element-for-ltnamedcachesgt"></a><span data-ttu-id="b1aab-102">&lt;supprimer&gt; élément pour &lt;namedCaches&gt;</span><span class="sxs-lookup"><span data-stu-id="b1aab-102">&lt;remove&gt; Element for &lt;namedCaches&gt;</span></span>
<span data-ttu-id="b1aab-103">Supprime une entité de cache nommé de la collection `namedCaches` d’un cache mémoire.</span><span class="sxs-lookup"><span data-stu-id="b1aab-103">Removes a named cache entry from the `namedCaches` collection for a memory cache.</span></span>  
  
 <span data-ttu-id="b1aab-104">\<system.runtime.caching></span><span class="sxs-lookup"><span data-stu-id="b1aab-104">\<system.runtime.caching></span></span>  
<span data-ttu-id="b1aab-105">\<memoryCache></span><span class="sxs-lookup"><span data-stu-id="b1aab-105">\<memoryCache></span></span>  
<span data-ttu-id="b1aab-106">\<namedCaches ></span><span class="sxs-lookup"><span data-stu-id="b1aab-106">\<namedCaches></span></span>  
<span data-ttu-id="b1aab-107">\<remove></span><span class="sxs-lookup"><span data-stu-id="b1aab-107">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1aab-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1aab-108">Syntax</span></span>  
  
```xml  
<namedCaches>  
    <remove name="default" />  
    <!-- child elements -->  
 </namedCaches>  
```  
  
## <a name="type"></a><span data-ttu-id="b1aab-109">Type</span><span class="sxs-lookup"><span data-stu-id="b1aab-109">Type</span></span>  
 `None`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b1aab-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b1aab-110">Attributes and Elements</span></span>  
 <span data-ttu-id="b1aab-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b1aab-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b1aab-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="b1aab-112">Attributes</span></span>  
 `None`  
  
### <a name="child-elements"></a><span data-ttu-id="b1aab-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b1aab-113">Child Elements</span></span>  
 `None`  
  
### <a name="parent-elements"></a><span data-ttu-id="b1aab-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b1aab-114">Parent Elements</span></span>  
  
|<span data-ttu-id="b1aab-115">Élément</span><span class="sxs-lookup"><span data-stu-id="b1aab-115">Element</span></span>|<span data-ttu-id="b1aab-116">Description</span><span class="sxs-lookup"><span data-stu-id="b1aab-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b1aab-117">\<namedCaches></span><span class="sxs-lookup"><span data-stu-id="b1aab-117">\<namedCaches></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)|<span data-ttu-id="b1aab-118">Contient une collection de paramètres de configuration pour l’élément nommé <xref:System.Runtime.Caching.MemoryCache> instances.</span><span class="sxs-lookup"><span data-stu-id="b1aab-118">Contains a collection of configuration settings for the named <xref:System.Runtime.Caching.MemoryCache> instances.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b1aab-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b1aab-119">Remarks</span></span>  
 <span data-ttu-id="b1aab-120">Le `remove` élément supprime un `namedCache` entrée à partir de la collection de cache nommé pour un cache mémoire.</span><span class="sxs-lookup"><span data-stu-id="b1aab-120">The `remove` element removes a `namedCache` entry from the named cache collection for a memory cache.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1aab-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1aab-121">See Also</span></span>  
 [<span data-ttu-id="b1aab-122">\<namedCaches >, élément (paramètres de Cache)</span><span class="sxs-lookup"><span data-stu-id="b1aab-122">\<namedCaches> Element (Cache Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)
