---
title: Élément <clear> pour <namedCaches>
ms.date: 03/30/2017
helpviewer_keywords:
- <clear> element for <namedCaches>
- clear element for <namedCaches>
ms.assetid: ea01a858-65da-4348-800f-5e3df59d4d79
ms.openlocfilehash: eb0a50919e163a795abc70d132bd45f1d05192ec
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59146859"
---
# <a name="clear-element-for-namedcaches"></a><span data-ttu-id="ae4b8-102">\<Désactivez >, élément pour \<namedCaches ></span><span class="sxs-lookup"><span data-stu-id="ae4b8-102">\<clear> Element for \<namedCaches></span></span>
<span data-ttu-id="ae4b8-103">Efface tous les `namedCache` entrées dans le `namedCaches` collection pour un cache mémoire.</span><span class="sxs-lookup"><span data-stu-id="ae4b8-103">Clears all `namedCache` entries in the `namedCaches` collection for a memory cache.</span></span>  
  
 <span data-ttu-id="ae4b8-104">\<system.runtime.caching></span><span class="sxs-lookup"><span data-stu-id="ae4b8-104">\<system.runtime.caching></span></span>  
<span data-ttu-id="ae4b8-105">\<memoryCache></span><span class="sxs-lookup"><span data-stu-id="ae4b8-105">\<memoryCache></span></span>  
<span data-ttu-id="ae4b8-106">\<namedCaches></span><span class="sxs-lookup"><span data-stu-id="ae4b8-106">\<namedCaches></span></span>  
<span data-ttu-id="ae4b8-107">\<add></span><span class="sxs-lookup"><span data-stu-id="ae4b8-107">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae4b8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae4b8-108">Syntax</span></span>  
  
```xml  
<namedCaches>  
    <clear name="default" />  
    <!-- child elements -->  
 </namedCaches>  
```  
  
## <a name="type"></a><span data-ttu-id="ae4b8-109">Type</span><span class="sxs-lookup"><span data-stu-id="ae4b8-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ae4b8-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ae4b8-110">Attributes and Elements</span></span>  
 <span data-ttu-id="ae4b8-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ae4b8-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ae4b8-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="ae4b8-112">Attributes</span></span>  
 `None`  
  
### <a name="child-elements"></a><span data-ttu-id="ae4b8-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ae4b8-113">Child Elements</span></span>  
 `None`  
  
### <a name="parent-elements"></a><span data-ttu-id="ae4b8-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ae4b8-114">Parent Elements</span></span>  
  
|<span data-ttu-id="ae4b8-115">Élément</span><span class="sxs-lookup"><span data-stu-id="ae4b8-115">Element</span></span>|<span data-ttu-id="ae4b8-116">Description</span><span class="sxs-lookup"><span data-stu-id="ae4b8-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ae4b8-117">\<namedCaches></span><span class="sxs-lookup"><span data-stu-id="ae4b8-117">\<namedCaches></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)|<span data-ttu-id="ae4b8-118">Contient une collection de paramètres de configuration pour l’élément nommé <xref:System.Runtime.Caching.MemoryCache> instances.</span><span class="sxs-lookup"><span data-stu-id="ae4b8-118">Contains a collection of configuration settings for the named <xref:System.Runtime.Caching.MemoryCache> instances.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ae4b8-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ae4b8-119">Remarks</span></span>  
 <span data-ttu-id="ae4b8-120">Le `clear` élément efface tous les `namedCache` entrées dans la collection de cache nommé pour un cache mémoire.</span><span class="sxs-lookup"><span data-stu-id="ae4b8-120">The `clear` element clears all `namedCache` entries in the named cache collection for a memory cache.</span></span> <span data-ttu-id="ae4b8-121">Vous pouvez utiliser la `clear` élément avant d’utiliser le `add` élément à ajouter une nouvelle entrée de cache nommé afin d’être certain qu’il n’existe aucun autre cache nommé dans la collection.</span><span class="sxs-lookup"><span data-stu-id="ae4b8-121">You can use the `clear` element before you use the `add` element to add a new named cache entry in order to be certain there are no other named caches in the collection.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae4b8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae4b8-122">See also</span></span>

- [<span data-ttu-id="ae4b8-123">\<namedCaches >, élément (paramètres de Cache)</span><span class="sxs-lookup"><span data-stu-id="ae4b8-123">\<namedCaches> Element (Cache Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)
