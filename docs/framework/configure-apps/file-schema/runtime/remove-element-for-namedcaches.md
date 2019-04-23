---
title: Élément <remove> pour <namedCaches>
ms.date: 03/30/2017
helpviewer_keywords:
- remove element for namedCaches
- <remove> element for namedCaches
ms.assetid: 24211ea5-163e-4fe5-aed8-004d8499760c
ms.openlocfilehash: 053e2776153489dfdd61547fdc039980646ae697
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59229769"
---
# <a name="remove-element-for-namedcaches"></a><span data-ttu-id="df223-102">\<Supprimer >, élément pour \<namedCaches ></span><span class="sxs-lookup"><span data-stu-id="df223-102">\<remove> Element for \<namedCaches></span></span>
<span data-ttu-id="df223-103">Supprime une entité de cache nommé de la collection `namedCaches` d’un cache mémoire.</span><span class="sxs-lookup"><span data-stu-id="df223-103">Removes a named cache entry from the `namedCaches` collection for a memory cache.</span></span>  
  
 <span data-ttu-id="df223-104">\<system.runtime.caching></span><span class="sxs-lookup"><span data-stu-id="df223-104">\<system.runtime.caching></span></span>  
<span data-ttu-id="df223-105">\<memoryCache></span><span class="sxs-lookup"><span data-stu-id="df223-105">\<memoryCache></span></span>  
<span data-ttu-id="df223-106">\<namedCaches></span><span class="sxs-lookup"><span data-stu-id="df223-106">\<namedCaches></span></span>  
<span data-ttu-id="df223-107">\<remove></span><span class="sxs-lookup"><span data-stu-id="df223-107">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="df223-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df223-108">Syntax</span></span>  
  
```xml  
<namedCaches>  
    <remove name="default" />  
    <!-- child elements -->  
 </namedCaches>  
```  
  
## <a name="type"></a><span data-ttu-id="df223-109">Type</span><span class="sxs-lookup"><span data-stu-id="df223-109">Type</span></span>  
 `None`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="df223-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="df223-110">Attributes and Elements</span></span>  
 <span data-ttu-id="df223-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="df223-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="df223-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="df223-112">Attributes</span></span>  
 `None`  
  
### <a name="child-elements"></a><span data-ttu-id="df223-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="df223-113">Child Elements</span></span>  
 `None`  
  
### <a name="parent-elements"></a><span data-ttu-id="df223-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="df223-114">Parent Elements</span></span>  
  
|<span data-ttu-id="df223-115">Élément</span><span class="sxs-lookup"><span data-stu-id="df223-115">Element</span></span>|<span data-ttu-id="df223-116">Description</span><span class="sxs-lookup"><span data-stu-id="df223-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="df223-117">\<namedCaches></span><span class="sxs-lookup"><span data-stu-id="df223-117">\<namedCaches></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)|<span data-ttu-id="df223-118">Contient une collection de paramètres de configuration pour l’élément nommé <xref:System.Runtime.Caching.MemoryCache> instances.</span><span class="sxs-lookup"><span data-stu-id="df223-118">Contains a collection of configuration settings for the named <xref:System.Runtime.Caching.MemoryCache> instances.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="df223-119">Notes</span><span class="sxs-lookup"><span data-stu-id="df223-119">Remarks</span></span>  
 <span data-ttu-id="df223-120">Le `remove` élément supprime un `namedCache` entrée à partir de la collection de cache nommé pour un cache mémoire.</span><span class="sxs-lookup"><span data-stu-id="df223-120">The `remove` element removes a `namedCache` entry from the named cache collection for a memory cache.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df223-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df223-121">See also</span></span>

- [<span data-ttu-id="df223-122">\<namedCaches >, élément (paramètres de Cache)</span><span class="sxs-lookup"><span data-stu-id="df223-122">\<namedCaches> Element (Cache Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)
