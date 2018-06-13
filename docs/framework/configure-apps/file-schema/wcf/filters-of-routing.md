---
title: '&lt;filters&gt; de &lt;routing&gt;'
ms.date: 03/30/2017
ms.assetid: 7993cf90-9afd-4c3c-9608-184d5da1105c
ms.openlocfilehash: 9f0fa9bf51d264346738172f57a8efca7950fdb7
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32753113"
---
# <a name="ltfiltersgt-of-ltroutinggt"></a><span data-ttu-id="14cb0-102">&lt;filters&gt; de &lt;routing&gt;</span><span class="sxs-lookup"><span data-stu-id="14cb0-102">&lt;filters&gt; of &lt;routing&gt;</span></span>

<span data-ttu-id="14cb0-103">Représente une section de configuration pour définir un ensemble de filtres de routage, qui détermine le type de Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> à utiliser lors de l’évaluation des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="14cb0-103">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages.</span></span>

<span data-ttu-id="14cb0-104">[**\<system.serviceModel >**](system-servicemodel.md) </span><span class="sxs-lookup"><span data-stu-id="14cb0-104">[**\<system.serviceModel>**](system-servicemodel.md) </span></span>  
<span data-ttu-id="14cb0-105">&nbsp;&nbsp;[**\<routage >**](routing.md) </span><span class="sxs-lookup"><span data-stu-id="14cb0-105">&nbsp;&nbsp;[**\<routing>**](routing.md) </span></span>  
<span data-ttu-id="14cb0-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<filtres >**</span><span class="sxs-lookup"><span data-stu-id="14cb0-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<filters>**</span></span>

## <a name="syntax"></a><span data-ttu-id="14cb0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14cb0-107">Syntax</span></span>

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

## <a name="attributes-and-elements"></a><span data-ttu-id="14cb0-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="14cb0-108">Attributes and elements</span></span>

<span data-ttu-id="14cb0-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="14cb0-109">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="14cb0-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="14cb0-110">Attributes</span></span>

<span data-ttu-id="14cb0-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="14cb0-111">None</span></span>

### <a name="child-elements"></a><span data-ttu-id="14cb0-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="14cb0-112">Child elements</span></span>

|     | <span data-ttu-id="14cb0-113">Description</span><span class="sxs-lookup"><span data-stu-id="14cb0-113">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="14cb0-114">**\<Filtre >**</span><span class="sxs-lookup"><span data-stu-id="14cb0-114">**\<filter>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filter.md) | <span data-ttu-id="14cb0-115">Contient un filtre de routage qui détermine le type de Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> sera utilisé lors de l’évaluation des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="14cb0-115">Contains a routing filter that determines the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> will be used when evaluating incoming messages.</span></span> |

### <a name="parent-elements"></a><span data-ttu-id="14cb0-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="14cb0-116">Parent elements</span></span>

|     | <span data-ttu-id="14cb0-117">Description</span><span class="sxs-lookup"><span data-stu-id="14cb0-117">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="14cb0-118">**\<routage >**</span><span class="sxs-lookup"><span data-stu-id="14cb0-118">**\<routing>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md) | <span data-ttu-id="14cb0-119">Représente une section de configuration pour définir un ensemble de filtres de routage, qui détermine le type de Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> à utiliser lors de l’évaluation des messages entrants, ainsi que le routage des tables qui définissent les points de terminaison cible à envoyer des messages lorsqu’un filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="14cb0-119">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span> |

## <a name="see-also"></a><span data-ttu-id="14cb0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14cb0-120">See also</span></span>

<xref:System.ServiceModel.Routing.Configuration.FilterElement?displayProperty=nameWithType>
