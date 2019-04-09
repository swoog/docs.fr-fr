---
title: <add> de <namespaceTable>
ms.date: 03/30/2017
ms.assetid: cf7b5b75-63bd-49a6-abac-4bfdab377e36
ms.openlocfilehash: 7e65b66170465a8b3bb60754feebb7730b959d9d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59089716"
---
# <a name="add-of-namespacetable"></a><span data-ttu-id="2b4fb-102">\<Ajouter > de \<namespaceTable ></span><span class="sxs-lookup"><span data-stu-id="2b4fb-102">\<add> of \<namespaceTable></span></span>
<span data-ttu-id="2b4fb-103">Représente un élément de configuration qui contient un mappage espace de noms-préfixe à utiliser dans des filtres XPath pour le routage.</span><span class="sxs-lookup"><span data-stu-id="2b4fb-103">Represents a configuration element that contains a namespace to prefix mapping that can then be used in XPath filters for routing.</span></span>  
  
 <span data-ttu-id="2b4fb-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="2b4fb-104">\<system.serviceModel></span></span>  
<span data-ttu-id="2b4fb-105">\<routing></span><span class="sxs-lookup"><span data-stu-id="2b4fb-105">\<routing></span></span>  
<span data-ttu-id="2b4fb-106">\<namespaceTable></span><span class="sxs-lookup"><span data-stu-id="2b4fb-106">\<namespaceTable></span></span>  
<span data-ttu-id="2b4fb-107">\<add></span><span class="sxs-lookup"><span data-stu-id="2b4fb-107">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b4fb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b4fb-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2b4fb-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="2b4fb-109">Attributes and Elements</span></span>  
 <span data-ttu-id="2b4fb-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="2b4fb-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2b4fb-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="2b4fb-111">Attributes</span></span>  
  
|<span data-ttu-id="2b4fb-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="2b4fb-112">Attribute</span></span>|<span data-ttu-id="2b4fb-113">Description</span><span class="sxs-lookup"><span data-stu-id="2b4fb-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="2b4fb-114">namespace</span><span class="sxs-lookup"><span data-stu-id="2b4fb-114">namespace</span></span>|<span data-ttu-id="2b4fb-115">Chaîne qui contient l'espace de noms.</span><span class="sxs-lookup"><span data-stu-id="2b4fb-115">A string containing the namespace.</span></span>|  
|<span data-ttu-id="2b4fb-116">prefix</span><span class="sxs-lookup"><span data-stu-id="2b4fb-116">prefix</span></span>|<span data-ttu-id="2b4fb-117">Chaîne qui contient le préfixe de cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="2b4fb-117">A string containing the prefix for this namespace.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2b4fb-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2b4fb-118">Child Elements</span></span>  
 <span data-ttu-id="2b4fb-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2b4fb-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2b4fb-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2b4fb-120">Parent Elements</span></span>  
  
|<span data-ttu-id="2b4fb-121">Élément</span><span class="sxs-lookup"><span data-stu-id="2b4fb-121">Element</span></span>|<span data-ttu-id="2b4fb-122">Description</span><span class="sxs-lookup"><span data-stu-id="2b4fb-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2b4fb-123">\<namespaceTable></span><span class="sxs-lookup"><span data-stu-id="2b4fb-123">\<namespaceTable></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/namespacetable.md)|<span data-ttu-id="2b4fb-124">Représente une section de configuration qui permet de définir un ensemble d’éléments contenant des mappages espace de noms-préfixe qui peuvent ensuite être utilisés dans des filtres XPath pour le routage.</span><span class="sxs-lookup"><span data-stu-id="2b4fb-124">Represents a configuration section for defining a set of elements that contain namespace to prefix mappings that can then be used in XPath filters for routing.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="2b4fb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b4fb-125">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.NamespaceElement?displayProperty=nameWithType>
