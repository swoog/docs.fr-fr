---
title: <enableWebScript>
ms.date: 03/30/2017
ms.assetid: 9c7e96e1-af70-4e6e-ac5c-d67929dddbaa
ms.openlocfilehash: b2cdd29cda7f82ce555b0f6c1a963567b41ff81b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59212997"
---
# <a name="enablewebscript"></a><span data-ttu-id="eabf2-101">\<enableWebScript></span><span class="sxs-lookup"><span data-stu-id="eabf2-101">\<enableWebScript></span></span>
<span data-ttu-id="eabf2-102">Cet élément active le comportement de point de terminaison qui permet de consommer le service à partir de pages web ASP.NET AJAX.</span><span class="sxs-lookup"><span data-stu-id="eabf2-102">This element enables the endpoint behavior that makes it possible to consume the service from ASP.NET AJAX web pages.</span></span>  
  
 <span data-ttu-id="eabf2-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="eabf2-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="eabf2-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="eabf2-104">\<behaviors></span></span>  
<span data-ttu-id="eabf2-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="eabf2-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="eabf2-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="eabf2-106">\<behavior></span></span>  
<span data-ttu-id="eabf2-107">\<enableWebScript></span><span class="sxs-lookup"><span data-stu-id="eabf2-107">\<enableWebScript></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eabf2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eabf2-108">Syntax</span></span>  
  
```xml  
<enableWebScript />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="eabf2-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="eabf2-109">Attributes and Elements</span></span>  
 <span data-ttu-id="eabf2-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="eabf2-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="eabf2-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="eabf2-111">Attributes</span></span>  
 <span data-ttu-id="eabf2-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="eabf2-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="eabf2-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eabf2-113">Child Elements</span></span>  
 <span data-ttu-id="eabf2-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="eabf2-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="eabf2-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="eabf2-115">Parent Elements</span></span>  
  
|<span data-ttu-id="eabf2-116">Élément</span><span class="sxs-lookup"><span data-stu-id="eabf2-116">Element</span></span>|<span data-ttu-id="eabf2-117">Description</span><span class="sxs-lookup"><span data-stu-id="eabf2-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="eabf2-118">\<behavior></span><span class="sxs-lookup"><span data-stu-id="eabf2-118">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="eabf2-119">Spécifie le jeu de comportements du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="eabf2-119">Specifies the set of endpoint behaviors.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="eabf2-120">Notes</span><span class="sxs-lookup"><span data-stu-id="eabf2-120">Remarks</span></span>  
 <span data-ttu-id="eabf2-121">Ce comportement doit uniquement être utilisé conjointement avec soit le [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) liaison standard, ou le [ \<webMessageEncoding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webmessageencoding.md) élément de liaison.</span><span class="sxs-lookup"><span data-stu-id="eabf2-121">This behavior should only be used in conjunction with either the [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) standard binding, or the [\<webMessageEncoding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webmessageencoding.md) binding element.</span></span>  <span data-ttu-id="eabf2-122">Pour plus d'informations sur ce comportement, consultez <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>.</span><span class="sxs-lookup"><span data-stu-id="eabf2-122">For more information on this behavior, see <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eabf2-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eabf2-123">See also</span></span>

- <xref:System.ServiceModel.Configuration.WebScriptEnablingElement>
- <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>
- [<span data-ttu-id="eabf2-124">Intégration d’AJAX et prise en charge de JSON</span><span class="sxs-lookup"><span data-stu-id="eabf2-124">AJAX Integration and JSON Support</span></span>](../../../../../docs/framework/wcf/feature-details/ajax-integration-and-json-support.md)
- [<span data-ttu-id="eabf2-125">\<webHttp></span><span class="sxs-lookup"><span data-stu-id="eabf2-125">\<webHttp></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md)
