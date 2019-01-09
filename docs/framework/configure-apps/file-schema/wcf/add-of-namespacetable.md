---
title: '&lt;add&gt; de &lt;namespaceTable&gt;'
ms.date: 03/30/2017
ms.assetid: cf7b5b75-63bd-49a6-abac-4bfdab377e36
ms.openlocfilehash: ef4f1c46a0ee3b94e5548b752e4e0a6a759fd45b
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149512"
---
# <a name="ltaddgt-of-ltnamespacetablegt"></a><span data-ttu-id="49e3a-102">&lt;add&gt; de &lt;namespaceTable&gt;</span><span class="sxs-lookup"><span data-stu-id="49e3a-102">&lt;add&gt; of &lt;namespaceTable&gt;</span></span>
<span data-ttu-id="49e3a-103">Représente un élément de configuration qui contient un mappage espace de noms-préfixe à utiliser dans des filtres XPath pour le routage.</span><span class="sxs-lookup"><span data-stu-id="49e3a-103">Represents a configuration element that contains a namespace to prefix mapping that can then be used in XPath filters for routing.</span></span>  
  
 <span data-ttu-id="49e3a-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="49e3a-104">\<system.serviceModel></span></span>  
<span data-ttu-id="49e3a-105">\<routage ></span><span class="sxs-lookup"><span data-stu-id="49e3a-105">\<routing></span></span>  
<span data-ttu-id="49e3a-106">\<namespaceTable ></span><span class="sxs-lookup"><span data-stu-id="49e3a-106">\<namespaceTable></span></span>  
<span data-ttu-id="49e3a-107">\<add></span><span class="sxs-lookup"><span data-stu-id="49e3a-107">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="49e3a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49e3a-108">Syntax</span></span>  
  
```xml  
<routing>
  <namespaceTable>
    <add namespace="String"
         prefix="String" />
  </namespaceTable>
</routing>
```  
  
```csharp  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="49e3a-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="49e3a-109">Attributes and Elements</span></span>  
 <span data-ttu-id="49e3a-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="49e3a-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="49e3a-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="49e3a-111">Attributes</span></span>  
  
|<span data-ttu-id="49e3a-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="49e3a-112">Attribute</span></span>|<span data-ttu-id="49e3a-113">Description</span><span class="sxs-lookup"><span data-stu-id="49e3a-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="49e3a-114">namespace</span><span class="sxs-lookup"><span data-stu-id="49e3a-114">namespace</span></span>|<span data-ttu-id="49e3a-115">Chaîne qui contient l'espace de noms.</span><span class="sxs-lookup"><span data-stu-id="49e3a-115">A string containing the namespace.</span></span>|  
|<span data-ttu-id="49e3a-116">prefix</span><span class="sxs-lookup"><span data-stu-id="49e3a-116">prefix</span></span>|<span data-ttu-id="49e3a-117">Chaîne qui contient le préfixe de cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="49e3a-117">A string containing the prefix for this namespace.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="49e3a-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="49e3a-118">Child Elements</span></span>  
 <span data-ttu-id="49e3a-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="49e3a-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="49e3a-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="49e3a-120">Parent Elements</span></span>  
  
|<span data-ttu-id="49e3a-121">Élément</span><span class="sxs-lookup"><span data-stu-id="49e3a-121">Element</span></span>|<span data-ttu-id="49e3a-122">Description</span><span class="sxs-lookup"><span data-stu-id="49e3a-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="49e3a-123">\<namespaceTable ></span><span class="sxs-lookup"><span data-stu-id="49e3a-123">\<namespaceTable></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/namespacetable.md)|<span data-ttu-id="49e3a-124">Représente une section de configuration qui permet de définir un ensemble d’éléments contenant des mappages espace de noms-préfixe qui peuvent ensuite être utilisés dans des filtres XPath pour le routage.</span><span class="sxs-lookup"><span data-stu-id="49e3a-124">Represents a configuration section for defining a set of elements that contain namespace to prefix mappings that can then be used in XPath filters for routing.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="49e3a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49e3a-125">See Also</span></span>  
 <xref:System.ServiceModel.Routing.Configuration.NamespaceElement?displayProperty=nameWithType>    
