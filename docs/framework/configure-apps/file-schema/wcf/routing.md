---
title: '&lt;Routage&gt;'
ms.date: 03/30/2017
ms.assetid: a210c209-3940-4288-9a8e-39b1e62606bc
ms.openlocfilehash: 220c18ab8ea6222fcf7d9fb8a93950281c9de796
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145144"
---
# <a name="ltroutinggt"></a><span data-ttu-id="8df7d-102">&lt;Routage&gt;</span><span class="sxs-lookup"><span data-stu-id="8df7d-102">&lt;routing&gt;</span></span>

<span data-ttu-id="8df7d-103">Représente une section de configuration pour définir un ensemble de filtres de routage, déterminant le type de Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> à utiliser lors de l’évaluation des messages entrants, ainsi que le routage des tables qui définissent les points de terminaison cible à envoyer des messages lorsqu’un filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="8df7d-103">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span>

<span data-ttu-id="8df7d-104">[**\<system.serviceModel >**](system-servicemodel.md) </span><span class="sxs-lookup"><span data-stu-id="8df7d-104">[**\<system.serviceModel>**](system-servicemodel.md) </span></span>  
<span data-ttu-id="8df7d-105">&nbsp;&nbsp;**\<routage >**</span><span class="sxs-lookup"><span data-stu-id="8df7d-105">&nbsp;&nbsp;**\<routing>**</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8df7d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8df7d-106">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8df7d-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="8df7d-107">Attributes and elements</span></span>

<span data-ttu-id="8df7d-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="8df7d-108">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="8df7d-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="8df7d-109">Attributes</span></span>

<span data-ttu-id="8df7d-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8df7d-110">None</span></span>

### <a name="child-elements"></a><span data-ttu-id="8df7d-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8df7d-111">Child elements</span></span>

|     | <span data-ttu-id="8df7d-112">Description</span><span class="sxs-lookup"><span data-stu-id="8df7d-112">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="8df7d-113">**\<filtres >**</span><span class="sxs-lookup"><span data-stu-id="8df7d-113">**\<filters>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md) | <span data-ttu-id="8df7d-114">Contient un ensemble de filtres de routage qui déterminent que le type de MessageFilter de Windows Communication Foundation (WCF) sera utilisé lors de l’évaluation des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="8df7d-114">Contains a set of routing filters that determine the type of Windows Communication Foundation (WCF) MessageFilter will be used when evaluating incoming messages.</span></span> |
| [<span data-ttu-id="8df7d-115">**\<filterTables >**</span><span class="sxs-lookup"><span data-stu-id="8df7d-115">**\<filterTables>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filtertables.md) | <span data-ttu-id="8df7d-116">Contient les mappages entre les filtres de routage et les points de terminaison cibles permettant de spécifier le point de terminaison à utiliser lorsque le filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="8df7d-116">Contains mappings between the routing filters and the target endpoints to specify which endpoint to use when the filter matches.</span></span> |

### <a name="parent-elements"></a><span data-ttu-id="8df7d-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8df7d-117">Parent elements</span></span>

|     | <span data-ttu-id="8df7d-118">Description</span><span class="sxs-lookup"><span data-stu-id="8df7d-118">Description</span></span> |
| --- | ----------- |
| <span data-ttu-id="8df7d-119">**\<système. ServiceModel >**</span><span class="sxs-lookup"><span data-stu-id="8df7d-119">**\<system.ServiceModel>**</span></span> | <span data-ttu-id="8df7d-120">Élément racine de tous les éléments de configuration WCF.</span><span class="sxs-lookup"><span data-stu-id="8df7d-120">The root element of all WCF configuration elements.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8df7d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8df7d-121">See also</span></span>

<xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
