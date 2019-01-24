---
title: '&lt;filters&gt; de &lt;routing&gt;'
ms.date: 03/30/2017
ms.assetid: 7993cf90-9afd-4c3c-9608-184d5da1105c
ms.openlocfilehash: 468c10bc06b60f80ce93cf413c02582fe3861f70
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54704431"
---
# <a name="ltfiltersgt-of-ltroutinggt"></a><span data-ttu-id="d8397-102">&lt;filters&gt; de &lt;routing&gt;</span><span class="sxs-lookup"><span data-stu-id="d8397-102">&lt;filters&gt; of &lt;routing&gt;</span></span>

<span data-ttu-id="d8397-103">Représente une section de configuration pour définir un ensemble de filtres de routage, déterminant le type de Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> à utiliser lors de l’évaluation des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="d8397-103">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages.</span></span>

<span data-ttu-id="d8397-104">[**\<system.serviceModel>**](system-servicemodel.md) </span><span class="sxs-lookup"><span data-stu-id="d8397-104">[**\<system.serviceModel>**](system-servicemodel.md) </span></span>  
<span data-ttu-id="d8397-105">&nbsp;&nbsp;[**\<routing>**](routing.md) </span><span class="sxs-lookup"><span data-stu-id="d8397-105">&nbsp;&nbsp;[**\<routing>**](routing.md) </span></span>  
<span data-ttu-id="d8397-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<filters>**</span><span class="sxs-lookup"><span data-stu-id="d8397-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<filters>**</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d8397-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8397-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <routing>
    <filters>
      <filter customType="String"
              filterData="String"
              filterType="Action/Address/AddressPrefix/And/Custom/Endpoint/MatchAll/XPath"
              name="String" />
    </filters>
  </routing>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d8397-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d8397-108">Attributes and elements</span></span>

<span data-ttu-id="d8397-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d8397-109">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="d8397-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="d8397-110">Attributes</span></span>

<span data-ttu-id="d8397-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d8397-111">None</span></span>

### <a name="child-elements"></a><span data-ttu-id="d8397-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d8397-112">Child elements</span></span>

|     | <span data-ttu-id="d8397-113">Description</span><span class="sxs-lookup"><span data-stu-id="d8397-113">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="d8397-114">**\<filter>**</span><span class="sxs-lookup"><span data-stu-id="d8397-114">**\<filter>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filter.md) | <span data-ttu-id="d8397-115">Contient un filtre de routage qui détermine le type de Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> sera utilisé lors de l’évaluation des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="d8397-115">Contains a routing filter that determines the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> will be used when evaluating incoming messages.</span></span> |

### <a name="parent-elements"></a><span data-ttu-id="d8397-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d8397-116">Parent elements</span></span>

|     | <span data-ttu-id="d8397-117">Description</span><span class="sxs-lookup"><span data-stu-id="d8397-117">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="d8397-118">**\<routing>**</span><span class="sxs-lookup"><span data-stu-id="d8397-118">**\<routing>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md) | <span data-ttu-id="d8397-119">Représente une section de configuration pour définir un ensemble de filtres de routage, déterminant le type de Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> à utiliser lors de l’évaluation des messages entrants, ainsi que le routage des tables qui définissent les points de terminaison cible à envoyer des messages lorsqu’un filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="d8397-119">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d8397-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8397-120">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.FilterElement?displayProperty=nameWithType>
