---
title: '&lt;filter&gt;'
ms.date: 03/30/2017
ms.assetid: 3266700b-904b-44e4-93a7-e06a1a445100
ms.openlocfilehash: 9fae9a599299fdd8cf1e996593514fc0ef38b6ce
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54645507"
---
# <a name="ltfiltergt"></a><span data-ttu-id="fc7ef-102">&lt;filter&gt;</span><span class="sxs-lookup"><span data-stu-id="fc7ef-102">&lt;filter&gt;</span></span>

<span data-ttu-id="fc7ef-103">Définit un filtre de routage, qui détermine le type de Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> à utiliser lors de l’évaluation des messages entrants, en tant qu’ainsi les données ou les paramètres requis par le filtre de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-103">Defines a routing filter, which determines the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well any supporting data or parameters required by the filter.</span></span>

<span data-ttu-id="fc7ef-104">\<system.serviceModel> \<routing> \<filters> \<filter></span><span class="sxs-lookup"><span data-stu-id="fc7ef-104">\<system.serviceModel> \<routing> \<filters> \<filter></span></span>
  
## <a name="syntax"></a><span data-ttu-id="fc7ef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc7ef-105">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fc7ef-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="fc7ef-106">Attributes and elements</span></span>

<span data-ttu-id="fc7ef-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="fc7ef-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="fc7ef-108">Attributes</span></span>

| <span data-ttu-id="fc7ef-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="fc7ef-109">Attribute</span></span>  | <span data-ttu-id="fc7ef-110">Description</span><span class="sxs-lookup"><span data-stu-id="fc7ef-110">Description</span></span> |
| ---------- | ----------- |
| <span data-ttu-id="fc7ef-111">customType</span><span class="sxs-lookup"><span data-stu-id="fc7ef-111">customType</span></span> | <span data-ttu-id="fc7ef-112">Chaîne qui contient le nom qualifié complet du type personnalisé à utiliser comme filtre.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-112">A string containing the fully qualified type name of the custom type to be used as a filter.</span></span> <span data-ttu-id="fc7ef-113">Si `filterType` a la valeur `custom`, cet attribut contient le nom de type qualifié complet de la classe à créer.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-113">If `filterType` is set to `custom`, this attribute contains the fully qualified type name of the class to create.</span></span>  <span data-ttu-id="fc7ef-114">`filterData` peut également contenir des valeurs à utiliser lors de l’évaluation du filtre de type personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-114">`filterData` may also contain values to be used during evaluation of the custom type filter.</span></span> |
| <span data-ttu-id="fc7ef-115">filterData</span><span class="sxs-lookup"><span data-stu-id="fc7ef-115">filterData</span></span> | <span data-ttu-id="fc7ef-116">Chaîne qui contient la données de filtre.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-116">A string containing the filter data.</span></span> <span data-ttu-id="fc7ef-117">Pour plus d'informations sur la spécification de cet attribut, consultez <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-117">For more information on how to specify this attribute, see <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>.</span></span> |
| <span data-ttu-id="fc7ef-118">filterType</span><span class="sxs-lookup"><span data-stu-id="fc7ef-118">filterType</span></span> | <span data-ttu-id="fc7ef-119">Chaîne qui contient le type de filtre.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-119">A string containing the filter type.</span></span> <span data-ttu-id="fc7ef-120">Cet attribut est de type <xref:System.ServiceModel.Routing.Configuration.FilterType>.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-120">This attribute is of <xref:System.ServiceModel.Routing.Configuration.FilterType> type.</span></span>  <span data-ttu-id="fc7ef-121">Pour plus d'informations sur l'utilisation de cet attribut avec l'attribut `filterData`, consultez <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-121">For more information on how this works with the `filterData` attribute, see <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A>.</span></span> |
| <span data-ttu-id="fc7ef-122">name</span><span class="sxs-lookup"><span data-stu-id="fc7ef-122">name</span></span>       | <span data-ttu-id="fc7ef-123">Chaîne qui contient le nom unique de cet élément de filtre.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-123">A string containing the unique name of this filter element.</span></span> |

### <a name="child-elements"></a><span data-ttu-id="fc7ef-124">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fc7ef-124">Child elements</span></span>

<span data-ttu-id="fc7ef-125">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-125">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="fc7ef-126">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fc7ef-126">Parent elements</span></span>

| <span data-ttu-id="fc7ef-127">Élément</span><span class="sxs-lookup"><span data-stu-id="fc7ef-127">Element</span></span> | <span data-ttu-id="fc7ef-128">Description</span><span class="sxs-lookup"><span data-stu-id="fc7ef-128">Description</span></span> |
| ------- | ----------- |
| [<span data-ttu-id="fc7ef-129">\<routing></span><span class="sxs-lookup"><span data-stu-id="fc7ef-129">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md) | <span data-ttu-id="fc7ef-130">Une section de configuration pour définir un ensemble de filtres de routage, déterminant le type de Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> à utiliser lors de l’évaluation des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-130">A configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages.</span></span> |

## <a name="see-also"></a><span data-ttu-id="fc7ef-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc7ef-131">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.FilterElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterType?displayProperty=nameWithType>
