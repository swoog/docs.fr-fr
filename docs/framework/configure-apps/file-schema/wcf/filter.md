---
title: <filter>
ms.date: 03/30/2017
ms.assetid: 3266700b-904b-44e4-93a7-e06a1a445100
ms.openlocfilehash: bff19f106d86c73dea80b8b57bb73442eaa2cf9f
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55278783"
---
# <a name="filter"></a><span data-ttu-id="3a666-101">\<filter></span><span class="sxs-lookup"><span data-stu-id="3a666-101">\<filter></span></span>

<span data-ttu-id="3a666-102">Définit un filtre de routage, qui détermine le type de Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> à utiliser lors de l’évaluation des messages entrants, en tant qu’ainsi les données ou les paramètres requis par le filtre de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="3a666-102">Defines a routing filter, which determines the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well any supporting data or parameters required by the filter.</span></span>

<span data-ttu-id="3a666-103">\<system.serviceModel> \<routing> \<filters> \<filter></span><span class="sxs-lookup"><span data-stu-id="3a666-103">\<system.serviceModel> \<routing> \<filters> \<filter></span></span>
  
## <a name="syntax"></a><span data-ttu-id="3a666-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a666-104">Syntax</span></span>  
  
```xml  
<routing>
  <filters>
    <filter customType="String"
            filterData="String"
            filterType="Action/Address/AddressPrefix/And/Custom/Endpoint/MatchAll/XPath"
            name="String" />
  </filters>
</routing>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3a666-105">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3a666-105">Attributes and elements</span></span>

<span data-ttu-id="3a666-106">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3a666-106">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="3a666-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="3a666-107">Attributes</span></span>

| <span data-ttu-id="3a666-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="3a666-108">Attribute</span></span>  | <span data-ttu-id="3a666-109">Description</span><span class="sxs-lookup"><span data-stu-id="3a666-109">Description</span></span> |
| ---------- | ----------- |
| <span data-ttu-id="3a666-110">customType</span><span class="sxs-lookup"><span data-stu-id="3a666-110">customType</span></span> | <span data-ttu-id="3a666-111">Chaîne qui contient le nom qualifié complet du type personnalisé à utiliser comme filtre.</span><span class="sxs-lookup"><span data-stu-id="3a666-111">A string containing the fully qualified type name of the custom type to be used as a filter.</span></span> <span data-ttu-id="3a666-112">Si `filterType` a la valeur `custom`, cet attribut contient le nom de type qualifié complet de la classe à créer.</span><span class="sxs-lookup"><span data-stu-id="3a666-112">If `filterType` is set to `custom`, this attribute contains the fully qualified type name of the class to create.</span></span>  <span data-ttu-id="3a666-113">`filterData` peut également contenir des valeurs à utiliser lors de l’évaluation du filtre de type personnalisé.</span><span class="sxs-lookup"><span data-stu-id="3a666-113">`filterData` may also contain values to be used during evaluation of the custom type filter.</span></span> |
| <span data-ttu-id="3a666-114">filterData</span><span class="sxs-lookup"><span data-stu-id="3a666-114">filterData</span></span> | <span data-ttu-id="3a666-115">Chaîne qui contient la données de filtre.</span><span class="sxs-lookup"><span data-stu-id="3a666-115">A string containing the filter data.</span></span> <span data-ttu-id="3a666-116">Pour plus d'informations sur la spécification de cet attribut, consultez <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>.</span><span class="sxs-lookup"><span data-stu-id="3a666-116">For more information on how to specify this attribute, see <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>.</span></span> |
| <span data-ttu-id="3a666-117">filterType</span><span class="sxs-lookup"><span data-stu-id="3a666-117">filterType</span></span> | <span data-ttu-id="3a666-118">Chaîne qui contient le type de filtre.</span><span class="sxs-lookup"><span data-stu-id="3a666-118">A string containing the filter type.</span></span> <span data-ttu-id="3a666-119">Cet attribut est de type <xref:System.ServiceModel.Routing.Configuration.FilterType>.</span><span class="sxs-lookup"><span data-stu-id="3a666-119">This attribute is of <xref:System.ServiceModel.Routing.Configuration.FilterType> type.</span></span>  <span data-ttu-id="3a666-120">Pour plus d'informations sur l'utilisation de cet attribut avec l'attribut `filterData`, consultez <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>.</span><span class="sxs-lookup"><span data-stu-id="3a666-120">For more information on how this works with the `filterData` attribute, see <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>.</span></span> |
| <span data-ttu-id="3a666-121">name</span><span class="sxs-lookup"><span data-stu-id="3a666-121">name</span></span>       | <span data-ttu-id="3a666-122">Chaîne qui contient le nom unique de cet élément de filtre.</span><span class="sxs-lookup"><span data-stu-id="3a666-122">A string containing the unique name of this filter element.</span></span> |

### <a name="child-elements"></a><span data-ttu-id="3a666-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3a666-123">Child elements</span></span>

<span data-ttu-id="3a666-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3a666-124">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="3a666-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3a666-125">Parent elements</span></span>

| <span data-ttu-id="3a666-126">Élément</span><span class="sxs-lookup"><span data-stu-id="3a666-126">Element</span></span> | <span data-ttu-id="3a666-127">Description</span><span class="sxs-lookup"><span data-stu-id="3a666-127">Description</span></span> |
| ------- | ----------- |
| [<span data-ttu-id="3a666-128">\<routing></span><span class="sxs-lookup"><span data-stu-id="3a666-128">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md) | <span data-ttu-id="3a666-129">Une section de configuration pour définir un ensemble de filtres de routage, déterminant le type de Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> à utiliser lors de l’évaluation des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="3a666-129">A configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3a666-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a666-130">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.FilterElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterType?displayProperty=nameWithType>
