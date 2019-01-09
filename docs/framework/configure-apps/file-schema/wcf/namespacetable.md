---
title: '&lt;namespaceTable&gt;'
ms.date: 03/30/2017
ms.assetid: 64801766-01b7-4c65-9ce6-70ad5af67689
ms.openlocfilehash: 55b5565ffe9d3e9e7ea41d2a2e2f380490be1781
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151421"
---
# <a name="ltnamespacetablegt"></a><span data-ttu-id="931af-102">&lt;namespaceTable&gt;</span><span class="sxs-lookup"><span data-stu-id="931af-102">&lt;namespaceTable&gt;</span></span>

<span data-ttu-id="931af-103">Représente une section de configuration qui permet de définir un ensemble d’éléments contenant des mappages espace de noms-préfixe qui peuvent ensuite être utilisés dans des filtres XPath pour le routage.</span><span class="sxs-lookup"><span data-stu-id="931af-103">Represents a configuration section for defining a set of elements that contain namespace to prefix mappings that can then be used in XPath filters for routing.</span></span>

<span data-ttu-id="931af-104">**\<system.serviceModel >** </span><span class="sxs-lookup"><span data-stu-id="931af-104">**\<system.serviceModel>** </span></span>  
<span data-ttu-id="931af-105">&nbsp;&nbsp;**\<routage >** </span><span class="sxs-lookup"><span data-stu-id="931af-105">&nbsp;&nbsp;**\<routing>** </span></span>  
<span data-ttu-id="931af-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<namespaceTable >**</span><span class="sxs-lookup"><span data-stu-id="931af-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<namespaceTable>**</span></span>
  
## <a name="syntax"></a><span data-ttu-id="931af-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="931af-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <routing>
    <namespaceTable>
      <add namespace="String"
           prefix="String" />
    </namespaceTable>
  </routing>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="931af-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="931af-108">Attributes and elements</span></span>

<span data-ttu-id="931af-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="931af-109">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="931af-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="931af-110">Attributes</span></span>

<span data-ttu-id="931af-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="931af-111">None</span></span>

### <a name="child-elements"></a><span data-ttu-id="931af-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="931af-112">Child elements</span></span>

|     | <span data-ttu-id="931af-113">Description</span><span class="sxs-lookup"><span data-stu-id="931af-113">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="931af-114">**\<Filtre >**</span><span class="sxs-lookup"><span data-stu-id="931af-114">**\<filter>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filter.md) | <span data-ttu-id="931af-115">Définit un mappage préfixe-espace de noms utilisé pour les expressions XPath.</span><span class="sxs-lookup"><span data-stu-id="931af-115">Defines a namespace prefix mapping used for XPath expressions.</span></span> |

### <a name="parent-elements"></a><span data-ttu-id="931af-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="931af-116">Parent elements</span></span>

|     | <span data-ttu-id="931af-117">Description</span><span class="sxs-lookup"><span data-stu-id="931af-117">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="931af-118">**\<routage >**</span><span class="sxs-lookup"><span data-stu-id="931af-118">**\<routing>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md) | <span data-ttu-id="931af-119">Représente une section de configuration pour définir un ensemble de filtres de routage, déterminant le type de Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> à utiliser lors de l’évaluation des messages entrants, ainsi que le routage des tables qui définissent les points de terminaison cible à envoyer des messages lorsqu’un filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="931af-119">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span> |

## <a name="see-also"></a><span data-ttu-id="931af-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="931af-120">See also</span></span>

<xref:System.ServiceModel.Routing.Configuration.NamespaceElementCollection?displayProperty=nameWithType>
