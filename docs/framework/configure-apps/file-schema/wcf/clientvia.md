---
title: '&lt;clientVia&gt;'
ms.date: 03/30/2017
ms.assetid: c27ee94e-babd-459b-9574-2a6d67d11314
ms.openlocfilehash: 6491411d8cfe5c7a5a944f3b1cd728c9f0a4b852
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54641211"
---
# <a name="ltclientviagt"></a><span data-ttu-id="92f1c-102">&lt;clientVia&gt;</span><span class="sxs-lookup"><span data-stu-id="92f1c-102">&lt;clientVia&gt;</span></span>
<span data-ttu-id="92f1c-103">Spécifie l'URI pour lequel le canal de transport doit être créé.</span><span class="sxs-lookup"><span data-stu-id="92f1c-103">Specifies the URI for which the transport channel should be created.</span></span> <span data-ttu-id="92f1c-104">Pour plus d'informations, consultez <xref:System.ServiceModel.Description.ClientViaBehavior>.</span><span class="sxs-lookup"><span data-stu-id="92f1c-104">For more information, see <xref:System.ServiceModel.Description.ClientViaBehavior>.</span></span>  
  
 <span data-ttu-id="92f1c-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="92f1c-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="92f1c-106">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="92f1c-106">\<behaviors></span></span>  
<span data-ttu-id="92f1c-107">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="92f1c-107">\<endpointBehaviors></span></span>  
<span data-ttu-id="92f1c-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="92f1c-108">\<behavior></span></span>  
<span data-ttu-id="92f1c-109">\<clientVia></span><span class="sxs-lookup"><span data-stu-id="92f1c-109">\<clientVia></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="92f1c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92f1c-110">Syntax</span></span>  
  
```xml  
<clientVia viaUri="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="92f1c-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="92f1c-111">Attributes and Elements</span></span>  
 <span data-ttu-id="92f1c-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="92f1c-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="92f1c-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="92f1c-113">Attributes</span></span>  
  
|<span data-ttu-id="92f1c-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="92f1c-114">Attribute</span></span>|<span data-ttu-id="92f1c-115">Description</span><span class="sxs-lookup"><span data-stu-id="92f1c-115">Description</span></span>|  
|---------------|-----------------|  
|`viaUri`|<span data-ttu-id="92f1c-116">Chaîne qui spécifie un URI indiquant l'itinéraire d'un message.</span><span class="sxs-lookup"><span data-stu-id="92f1c-116">A string that specifies a URI that indicates the route a message should take.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="92f1c-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="92f1c-117">Child Elements</span></span>  
 <span data-ttu-id="92f1c-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="92f1c-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="92f1c-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="92f1c-119">Parent Elements</span></span>  
  
|<span data-ttu-id="92f1c-120">Élément</span><span class="sxs-lookup"><span data-stu-id="92f1c-120">Element</span></span>|<span data-ttu-id="92f1c-121">Description</span><span class="sxs-lookup"><span data-stu-id="92f1c-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="92f1c-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="92f1c-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="92f1c-123">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="92f1c-123">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="92f1c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92f1c-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.ClientViaElement>
- <xref:System.ServiceModel.Description.ClientViaBehavior>
