---
title: <routing>
ms.date: 03/30/2017
ms.assetid: a210c209-3940-4288-9a8e-39b1e62606bc
ms.openlocfilehash: cc7c1a64f9481a7ab41cf35241ade04bd690dae0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61786384"
---
# <a name="routing"></a><span data-ttu-id="9883f-101">\<routing></span><span class="sxs-lookup"><span data-stu-id="9883f-101">\<routing></span></span>

<span data-ttu-id="9883f-102">Représente une section de configuration pour définir un ensemble de filtres de routage, déterminant le type de Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> à utiliser lors de l’évaluation des messages entrants, ainsi que le routage des tables qui définissent les points de terminaison cible à envoyer des messages lorsqu’un filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="9883f-102">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span>

<span data-ttu-id="9883f-103">[**\<system.serviceModel>**](system-servicemodel.md) </span><span class="sxs-lookup"><span data-stu-id="9883f-103">[**\<system.serviceModel>**](system-servicemodel.md) </span></span>  
<span data-ttu-id="9883f-104">&nbsp;&nbsp;**\<routing>**</span><span class="sxs-lookup"><span data-stu-id="9883f-104">&nbsp;&nbsp;**\<routing>**</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9883f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9883f-105">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <routing>
    <filters>
      <filter customType="String"
              filterData="String"
              filterType="Action/Address/AddressPrefix/And/Custom/Endpoint/MatchAll/XPath"
              name="String" />
    </filters>
    <routingTables>
      <table name="String">
        <entries>
          <add endpoint="String"
               filterName="String"
               priority="Integer" />
        </entries>
      </table>
    </routingTables>
  </routing>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9883f-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9883f-106">Attributes and elements</span></span>

<span data-ttu-id="9883f-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9883f-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="9883f-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="9883f-108">Attributes</span></span>

<span data-ttu-id="9883f-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9883f-109">None</span></span>

### <a name="child-elements"></a><span data-ttu-id="9883f-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9883f-110">Child elements</span></span>

|     | <span data-ttu-id="9883f-111">Description</span><span class="sxs-lookup"><span data-stu-id="9883f-111">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="9883f-112">**\<filters>**</span><span class="sxs-lookup"><span data-stu-id="9883f-112">**\<filters>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md) | <span data-ttu-id="9883f-113">Contient un ensemble de filtres de routage qui déterminent que le type de MessageFilter de Windows Communication Foundation (WCF) sera utilisé lors de l’évaluation des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="9883f-113">Contains a set of routing filters that determine the type of Windows Communication Foundation (WCF) MessageFilter will be used when evaluating incoming messages.</span></span> |
| [<span data-ttu-id="9883f-114">**\<filterTables>**</span><span class="sxs-lookup"><span data-stu-id="9883f-114">**\<filterTables>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filtertables.md) | <span data-ttu-id="9883f-115">Contient les mappages entre les filtres de routage et les points de terminaison cibles permettant de spécifier le point de terminaison à utiliser lorsque le filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="9883f-115">Contains mappings between the routing filters and the target endpoints to specify which endpoint to use when the filter matches.</span></span> |

### <a name="parent-elements"></a><span data-ttu-id="9883f-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9883f-116">Parent elements</span></span>

|     | <span data-ttu-id="9883f-117">Description</span><span class="sxs-lookup"><span data-stu-id="9883f-117">Description</span></span> |
| --- | ----------- |
| <span data-ttu-id="9883f-118">**\<system.ServiceModel>**</span><span class="sxs-lookup"><span data-stu-id="9883f-118">**\<system.ServiceModel>**</span></span> | <span data-ttu-id="9883f-119">Élément racine de tous les éléments de configuration WCF.</span><span class="sxs-lookup"><span data-stu-id="9883f-119">The root element of all WCF configuration elements.</span></span> |

## <a name="see-also"></a><span data-ttu-id="9883f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9883f-120">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
