---
title: '&lt;clientVia&gt;'
ms.date: 03/30/2017
ms.assetid: c27ee94e-babd-459b-9574-2a6d67d11314
ms.openlocfilehash: 6218bb3f205f2825eb3f10fabf834cfd0396ac87
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32754130"
---
# <a name="ltclientviagt"></a><span data-ttu-id="7406d-102">&lt;clientVia&gt;</span><span class="sxs-lookup"><span data-stu-id="7406d-102">&lt;clientVia&gt;</span></span>
<span data-ttu-id="7406d-103">Spécifie l'URI pour lequel le canal de transport doit être créé.</span><span class="sxs-lookup"><span data-stu-id="7406d-103">Specifies the URI for which the transport channel should be created.</span></span> <span data-ttu-id="7406d-104">Pour plus d'informations, consultez <xref:System.ServiceModel.Description.ClientViaBehavior>.</span><span class="sxs-lookup"><span data-stu-id="7406d-104">For more information, see <xref:System.ServiceModel.Description.ClientViaBehavior>.</span></span>  
  
 <span data-ttu-id="7406d-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="7406d-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="7406d-106">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="7406d-106">\<behaviors></span></span>  
<span data-ttu-id="7406d-107">\<endpointBehaviors ></span><span class="sxs-lookup"><span data-stu-id="7406d-107">\<endpointBehaviors></span></span>  
<span data-ttu-id="7406d-108">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="7406d-108">\<behavior></span></span>  
<span data-ttu-id="7406d-109">\<clientVia ></span><span class="sxs-lookup"><span data-stu-id="7406d-109">\<clientVia></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7406d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7406d-110">Syntax</span></span>  
  
```xml  
<clientVia viaUri="String"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7406d-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="7406d-111">Attributes and Elements</span></span>  
 <span data-ttu-id="7406d-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="7406d-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7406d-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="7406d-113">Attributes</span></span>  
  
|<span data-ttu-id="7406d-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="7406d-114">Attribute</span></span>|<span data-ttu-id="7406d-115">Description</span><span class="sxs-lookup"><span data-stu-id="7406d-115">Description</span></span>|  
|---------------|-----------------|  
|`viaUri`|<span data-ttu-id="7406d-116">Chaîne qui spécifie un URI indiquant l'itinéraire d'un message.</span><span class="sxs-lookup"><span data-stu-id="7406d-116">A string that specifies a URI that indicates the route a message should take.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7406d-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7406d-117">Child Elements</span></span>  
 <span data-ttu-id="7406d-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="7406d-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7406d-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7406d-119">Parent Elements</span></span>  
  
|<span data-ttu-id="7406d-120">Élément</span><span class="sxs-lookup"><span data-stu-id="7406d-120">Element</span></span>|<span data-ttu-id="7406d-121">Description</span><span class="sxs-lookup"><span data-stu-id="7406d-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7406d-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="7406d-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="7406d-123">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="7406d-123">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7406d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7406d-124">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ClientViaElement>  
 <xref:System.ServiceModel.Description.ClientViaBehavior>
