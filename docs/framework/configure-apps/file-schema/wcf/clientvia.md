---
title: <clientVia>
ms.date: 03/30/2017
ms.assetid: c27ee94e-babd-459b-9574-2a6d67d11314
ms.openlocfilehash: b8864760c1700cd785922b922346204d194f56cc
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59176811"
---
# <a name="clientvia"></a><span data-ttu-id="cfc14-101">\<clientVia></span><span class="sxs-lookup"><span data-stu-id="cfc14-101">\<clientVia></span></span>
<span data-ttu-id="cfc14-102">Spécifie l'URI pour lequel le canal de transport doit être créé.</span><span class="sxs-lookup"><span data-stu-id="cfc14-102">Specifies the URI for which the transport channel should be created.</span></span> <span data-ttu-id="cfc14-103">Pour plus d'informations, consultez <xref:System.ServiceModel.Description.ClientViaBehavior>.</span><span class="sxs-lookup"><span data-stu-id="cfc14-103">For more information, see <xref:System.ServiceModel.Description.ClientViaBehavior>.</span></span>  
  
 <span data-ttu-id="cfc14-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="cfc14-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="cfc14-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="cfc14-105">\<behaviors></span></span>  
<span data-ttu-id="cfc14-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="cfc14-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="cfc14-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="cfc14-107">\<behavior></span></span>  
<span data-ttu-id="cfc14-108">\<clientVia></span><span class="sxs-lookup"><span data-stu-id="cfc14-108">\<clientVia></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cfc14-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfc14-109">Syntax</span></span>  
  
```xml  
<clientVia viaUri="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cfc14-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="cfc14-110">Attributes and Elements</span></span>  
 <span data-ttu-id="cfc14-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="cfc14-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cfc14-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="cfc14-112">Attributes</span></span>  
  
|<span data-ttu-id="cfc14-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="cfc14-113">Attribute</span></span>|<span data-ttu-id="cfc14-114">Description</span><span class="sxs-lookup"><span data-stu-id="cfc14-114">Description</span></span>|  
|---------------|-----------------|  
|`viaUri`|<span data-ttu-id="cfc14-115">Chaîne qui spécifie un URI indiquant l'itinéraire d'un message.</span><span class="sxs-lookup"><span data-stu-id="cfc14-115">A string that specifies a URI that indicates the route a message should take.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cfc14-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cfc14-116">Child Elements</span></span>  
 <span data-ttu-id="cfc14-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cfc14-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="cfc14-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="cfc14-118">Parent Elements</span></span>  
  
|<span data-ttu-id="cfc14-119">Élément</span><span class="sxs-lookup"><span data-stu-id="cfc14-119">Element</span></span>|<span data-ttu-id="cfc14-120">Description</span><span class="sxs-lookup"><span data-stu-id="cfc14-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cfc14-121">\<behavior></span><span class="sxs-lookup"><span data-stu-id="cfc14-121">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="cfc14-122">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="cfc14-122">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="cfc14-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfc14-123">See also</span></span>

- <xref:System.ServiceModel.Configuration.ClientViaElement>
- <xref:System.ServiceModel.Description.ClientViaBehavior>
