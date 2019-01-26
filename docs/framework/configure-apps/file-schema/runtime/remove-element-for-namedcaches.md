---
title: '&lt;supprimer&gt; élément pour &lt;namedCaches&gt;'
ms.date: 03/30/2017
helpviewer_keywords:
- remove element for namedCaches
- <remove> element for namedCaches
ms.assetid: 24211ea5-163e-4fe5-aed8-004d8499760c
ms.openlocfilehash: ceeef00cb688c725cc595582fb6845b9e3fa9b92
ms.sourcegitcommit: b351b0781a035616c90c68ccae6dd60aae66a953
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2019
ms.locfileid: "55083390"
---
# <a name="ltremovegt-element-for-ltnamedcachesgt"></a><span data-ttu-id="6c74f-102">&lt;supprimer&gt; élément pour &lt;namedCaches&gt;</span><span class="sxs-lookup"><span data-stu-id="6c74f-102">&lt;remove&gt; Element for &lt;namedCaches&gt;</span></span>
<span data-ttu-id="6c74f-103">Supprime une entité de cache nommé de la collection `namedCaches` d’un cache mémoire.</span><span class="sxs-lookup"><span data-stu-id="6c74f-103">Removes a named cache entry from the `namedCaches` collection for a memory cache.</span></span>  
  
 <span data-ttu-id="6c74f-104">\<system.runtime.caching></span><span class="sxs-lookup"><span data-stu-id="6c74f-104">\<system.runtime.caching></span></span>  
<span data-ttu-id="6c74f-105">\<memoryCache></span><span class="sxs-lookup"><span data-stu-id="6c74f-105">\<memoryCache></span></span>  
<span data-ttu-id="6c74f-106">\<namedCaches></span><span class="sxs-lookup"><span data-stu-id="6c74f-106">\<namedCaches></span></span>  
<span data-ttu-id="6c74f-107">\<remove></span><span class="sxs-lookup"><span data-stu-id="6c74f-107">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c74f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c74f-108">Syntax</span></span>  
  
```xml  
<namedCaches>  
    <remove name="default" />  
    <!-- child elements -->  
 </namedCaches>  
```  
  
## <a name="type"></a><span data-ttu-id="6c74f-109">Type</span><span class="sxs-lookup"><span data-stu-id="6c74f-109">Type</span></span>  
 `None`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6c74f-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6c74f-110">Attributes and Elements</span></span>  
 <span data-ttu-id="6c74f-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6c74f-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6c74f-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="6c74f-112">Attributes</span></span>  
 `None`  
  
### <a name="child-elements"></a><span data-ttu-id="6c74f-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6c74f-113">Child Elements</span></span>  
 `None`  
  
### <a name="parent-elements"></a><span data-ttu-id="6c74f-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6c74f-114">Parent Elements</span></span>  
  
|<span data-ttu-id="6c74f-115">Élément</span><span class="sxs-lookup"><span data-stu-id="6c74f-115">Element</span></span>|<span data-ttu-id="6c74f-116">Description</span><span class="sxs-lookup"><span data-stu-id="6c74f-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6c74f-117">\<namedCaches></span><span class="sxs-lookup"><span data-stu-id="6c74f-117">\<namedCaches></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)|<span data-ttu-id="6c74f-118">Contient une collection de paramètres de configuration pour l’élément nommé <xref:System.Runtime.Caching.MemoryCache> instances.</span><span class="sxs-lookup"><span data-stu-id="6c74f-118">Contains a collection of configuration settings for the named <xref:System.Runtime.Caching.MemoryCache> instances.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6c74f-119">Notes</span><span class="sxs-lookup"><span data-stu-id="6c74f-119">Remarks</span></span>  
 <span data-ttu-id="6c74f-120">Le `remove` élément supprime un `namedCache` entrée à partir de la collection de cache nommé pour un cache mémoire.</span><span class="sxs-lookup"><span data-stu-id="6c74f-120">The `remove` element removes a `namedCache` entry from the named cache collection for a memory cache.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c74f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c74f-121">See also</span></span>
- [<span data-ttu-id="6c74f-122">\<namedCaches >, élément (paramètres de Cache)</span><span class="sxs-lookup"><span data-stu-id="6c74f-122">\<namedCaches> Element (Cache Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)
