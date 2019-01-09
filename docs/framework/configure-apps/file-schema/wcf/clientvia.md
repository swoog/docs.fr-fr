---
title: '&lt;clientVia&gt;'
ms.date: 03/30/2017
ms.assetid: c27ee94e-babd-459b-9574-2a6d67d11314
ms.openlocfilehash: 48e56b79f47e84122ddd4d7f55d50044510bfa66
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149053"
---
# <a name="ltclientviagt"></a><span data-ttu-id="7e1c9-102">&lt;clientVia&gt;</span><span class="sxs-lookup"><span data-stu-id="7e1c9-102">&lt;clientVia&gt;</span></span>
<span data-ttu-id="7e1c9-103">Spécifie l'URI pour lequel le canal de transport doit être créé.</span><span class="sxs-lookup"><span data-stu-id="7e1c9-103">Specifies the URI for which the transport channel should be created.</span></span> <span data-ttu-id="7e1c9-104">Pour plus d'informations, consultez <xref:System.ServiceModel.Description.ClientViaBehavior>.</span><span class="sxs-lookup"><span data-stu-id="7e1c9-104">For more information, see <xref:System.ServiceModel.Description.ClientViaBehavior>.</span></span>  
  
 <span data-ttu-id="7e1c9-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="7e1c9-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="7e1c9-106">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="7e1c9-106">\<behaviors></span></span>  
<span data-ttu-id="7e1c9-107">\<endpointBehaviors ></span><span class="sxs-lookup"><span data-stu-id="7e1c9-107">\<endpointBehaviors></span></span>  
<span data-ttu-id="7e1c9-108">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="7e1c9-108">\<behavior></span></span>  
<span data-ttu-id="7e1c9-109">\<clientVia ></span><span class="sxs-lookup"><span data-stu-id="7e1c9-109">\<clientVia></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7e1c9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e1c9-110">Syntax</span></span>  
  
```xml  
<clientVia viaUri="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7e1c9-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="7e1c9-111">Attributes and Elements</span></span>  
 <span data-ttu-id="7e1c9-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="7e1c9-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7e1c9-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="7e1c9-113">Attributes</span></span>  
  
|<span data-ttu-id="7e1c9-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="7e1c9-114">Attribute</span></span>|<span data-ttu-id="7e1c9-115">Description</span><span class="sxs-lookup"><span data-stu-id="7e1c9-115">Description</span></span>|  
|---------------|-----------------|  
|`viaUri`|<span data-ttu-id="7e1c9-116">Chaîne qui spécifie un URI indiquant l'itinéraire d'un message.</span><span class="sxs-lookup"><span data-stu-id="7e1c9-116">A string that specifies a URI that indicates the route a message should take.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7e1c9-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7e1c9-117">Child Elements</span></span>  
 <span data-ttu-id="7e1c9-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7e1c9-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7e1c9-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7e1c9-119">Parent Elements</span></span>  
  
|<span data-ttu-id="7e1c9-120">Élément</span><span class="sxs-lookup"><span data-stu-id="7e1c9-120">Element</span></span>|<span data-ttu-id="7e1c9-121">Description</span><span class="sxs-lookup"><span data-stu-id="7e1c9-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7e1c9-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="7e1c9-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="7e1c9-123">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="7e1c9-123">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7e1c9-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e1c9-124">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ClientViaElement>  
 <xref:System.ServiceModel.Description.ClientViaBehavior>
