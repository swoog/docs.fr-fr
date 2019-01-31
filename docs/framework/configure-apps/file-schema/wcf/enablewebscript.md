---
title: <enableWebScript>
ms.date: 03/30/2017
ms.assetid: 9c7e96e1-af70-4e6e-ac5c-d67929dddbaa
ms.openlocfilehash: 9c9bbb9ccc7879510ae3e2bee2fabd604fd52f65
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55266648"
---
# <a name="enablewebscript"></a><span data-ttu-id="4b5de-101">\<enableWebScript></span><span class="sxs-lookup"><span data-stu-id="4b5de-101">\<enableWebScript></span></span>
<span data-ttu-id="4b5de-102">Cet élément active le comportement de point de terminaison qui permet de consommer le service à partir de pages web ASP.NET AJAX.</span><span class="sxs-lookup"><span data-stu-id="4b5de-102">This element enables the endpoint behavior that makes it possible to consume the service from ASP.NET AJAX web pages.</span></span>  
  
 <span data-ttu-id="4b5de-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="4b5de-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="4b5de-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="4b5de-104">\<behaviors></span></span>  
<span data-ttu-id="4b5de-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="4b5de-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="4b5de-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="4b5de-106">\<behavior></span></span>  
<span data-ttu-id="4b5de-107">\<enableWebScript></span><span class="sxs-lookup"><span data-stu-id="4b5de-107">\<enableWebScript></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b5de-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b5de-108">Syntax</span></span>  
  
```xml  
<enableWebScript />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4b5de-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4b5de-109">Attributes and Elements</span></span>  
 <span data-ttu-id="4b5de-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4b5de-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4b5de-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="4b5de-111">Attributes</span></span>  
 <span data-ttu-id="4b5de-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4b5de-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4b5de-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4b5de-113">Child Elements</span></span>  
 <span data-ttu-id="4b5de-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4b5de-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4b5de-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4b5de-115">Parent Elements</span></span>  
  
|<span data-ttu-id="4b5de-116">Élément</span><span class="sxs-lookup"><span data-stu-id="4b5de-116">Element</span></span>|<span data-ttu-id="4b5de-117">Description</span><span class="sxs-lookup"><span data-stu-id="4b5de-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4b5de-118">\<behavior></span><span class="sxs-lookup"><span data-stu-id="4b5de-118">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="4b5de-119">Spécifie le jeu de comportements du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="4b5de-119">Specifies the set of endpoint behaviors.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4b5de-120">Notes</span><span class="sxs-lookup"><span data-stu-id="4b5de-120">Remarks</span></span>  
 <span data-ttu-id="4b5de-121">Ce comportement doit uniquement être utilisé conjointement avec soit le [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) liaison standard, ou le [ \<webMessageEncoding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webmessageencoding.md) élément de liaison.</span><span class="sxs-lookup"><span data-stu-id="4b5de-121">This behavior should only be used in conjunction with either the [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) standard binding, or the [\<webMessageEncoding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webmessageencoding.md) binding element.</span></span>  <span data-ttu-id="4b5de-122">Pour plus d'informations sur ce comportement, consultez <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>.</span><span class="sxs-lookup"><span data-stu-id="4b5de-122">For more information on this behavior, see <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b5de-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b5de-123">See also</span></span>
- <xref:System.ServiceModel.Configuration.WebScriptEnablingElement>
- <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>
- [<span data-ttu-id="4b5de-124">Intégration d’AJAX et prise en charge de JSON</span><span class="sxs-lookup"><span data-stu-id="4b5de-124">AJAX Integration and JSON Support</span></span>](../../../../../docs/framework/wcf/feature-details/ajax-integration-and-json-support.md)
- [<span data-ttu-id="4b5de-125">\<webHttp></span><span class="sxs-lookup"><span data-stu-id="4b5de-125">\<webHttp></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md)
