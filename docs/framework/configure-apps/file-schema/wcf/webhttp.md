---
title: '&lt;webHttp&gt;'
ms.date: 03/30/2017
ms.assetid: 1f9d0754-d41e-44ce-a298-e51cb3096c64
ms.openlocfilehash: 9ba54dc1744751efe4efad04f829cccce1244e0d
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145669"
---
# <a name="ltwebhttpgt"></a><span data-ttu-id="9fa04-102">&lt;webHttp&gt;</span><span class="sxs-lookup"><span data-stu-id="9fa04-102">&lt;webHttp&gt;</span></span>
<span data-ttu-id="9fa04-103">Cet élément spécifie le <xref:System.ServiceModel.Description.WebHttpBehavior> d'un point de terminaison via la configuration.</span><span class="sxs-lookup"><span data-stu-id="9fa04-103">This element specifies the <xref:System.ServiceModel.Description.WebHttpBehavior> on an endpoint through configuration.</span></span> <span data-ttu-id="9fa04-104">Ce comportement est utilisé conjointement avec le [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) permet de liaison standard, le modèle de programmation Web pour un service Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="9fa04-104">This behavior, when used in conjunction with the [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) standard binding, enables the Web programming model for a Windows Communication Foundation (WCF) service.</span></span>  
  
 <span data-ttu-id="9fa04-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="9fa04-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="9fa04-106">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="9fa04-106">\<behaviors></span></span>  
<span data-ttu-id="9fa04-107">\<endpointBehaviors ></span><span class="sxs-lookup"><span data-stu-id="9fa04-107">\<endpointBehaviors></span></span>  
<span data-ttu-id="9fa04-108">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="9fa04-108">\<behavior></span></span>  
<span data-ttu-id="9fa04-109">\<webHttp ></span><span class="sxs-lookup"><span data-stu-id="9fa04-109">\<webHttp></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9fa04-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fa04-110">Syntax</span></span>  
  
```xml  
<webHttp />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9fa04-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9fa04-111">Attributes and Elements</span></span>  
 <span data-ttu-id="9fa04-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9fa04-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9fa04-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="9fa04-113">Attributes</span></span>  
  
|<span data-ttu-id="9fa04-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="9fa04-114">Attribute</span></span>|<span data-ttu-id="9fa04-115">Description</span><span class="sxs-lookup"><span data-stu-id="9fa04-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9fa04-116">automaticFormatSelectionEnabled</span><span class="sxs-lookup"><span data-stu-id="9fa04-116">automaticFormatSelectionEnabled</span></span>|<span data-ttu-id="9fa04-117">Lorsque cette propriété a la valeur `true`, l'infrastructure WCF détermine le meilleur format à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9fa04-117">When this property is set to `true`, the WCF infrastructure determines the best format to use.</span></span> <span data-ttu-id="9fa04-118">La sélection automatique du format est désactivée par défaut à des fins de compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="9fa04-118">Automatic format selection is disabled by default for backwards compatibility.</span></span> <span data-ttu-id="9fa04-119">La sélection automatique du format peut être activée par programme ou par configuration.</span><span class="sxs-lookup"><span data-stu-id="9fa04-119">Automatic format selection can be enabled programmatically or through configuration.</span></span>|  
|<span data-ttu-id="9fa04-120">defaultBodyStyle</span><span class="sxs-lookup"><span data-stu-id="9fa04-120">defaultBodyStyle</span></span>|<span data-ttu-id="9fa04-121">Spécifie le style du corps par défaut des messages retournés.</span><span class="sxs-lookup"><span data-stu-id="9fa04-121">Specifies the default body style of returned messages.</span></span> <span data-ttu-id="9fa04-122">Pour plus d’informations, consultez <xref:System.ServiceModel.Web.WebMessageBodyStyle> et [mise en forme de WCF Web HTTP](../../../../../docs/framework/wcf/feature-details/wcf-web-http-formatting.md).</span><span class="sxs-lookup"><span data-stu-id="9fa04-122">For more information, see <xref:System.ServiceModel.Web.WebMessageBodyStyle> and [WCF Web HTTP Formatting](../../../../../docs/framework/wcf/feature-details/wcf-web-http-formatting.md).</span></span>|  
|<span data-ttu-id="9fa04-123">defaultOutgoingResponseFormat</span><span class="sxs-lookup"><span data-stu-id="9fa04-123">defaultOutgoingResponseFormat</span></span>|<span data-ttu-id="9fa04-124">Spécifie le format de réponse sortante par défaut des messages.</span><span class="sxs-lookup"><span data-stu-id="9fa04-124">Specifies the default outgoing response format for messages.</span></span> <span data-ttu-id="9fa04-125">Pour plus d’informations, consultez [mise en forme de WCF Web HTTP](../../../../../docs/framework/wcf/feature-details/wcf-web-http-formatting.md).</span><span class="sxs-lookup"><span data-stu-id="9fa04-125">For more information, see [WCF Web HTTP Formatting](../../../../../docs/framework/wcf/feature-details/wcf-web-http-formatting.md).</span></span>|  
|<span data-ttu-id="9fa04-126">faultExceptionEnabled</span><span class="sxs-lookup"><span data-stu-id="9fa04-126">faultExceptionEnabled</span></span>|<span data-ttu-id="9fa04-127">Obtient ou définit l’indicateur qui spécifie si FaultException est généré quand une erreur de serveur interne (code d’état HTTP : 500) se produit.</span><span class="sxs-lookup"><span data-stu-id="9fa04-127">Gets or sets the flag that specifies whether a FaultException is generated when an internal server error (HTTP status code: 500) occurs.</span></span>|  
|<span data-ttu-id="9fa04-128">helpEnabled</span><span class="sxs-lookup"><span data-stu-id="9fa04-128">helpEnabled</span></span>|<span data-ttu-id="9fa04-129">Obtient ou définit une valeur qui détermine si la page d'aide est activée.</span><span class="sxs-lookup"><span data-stu-id="9fa04-129">Gets or sets a value that determines if the Help page is enabled.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9fa04-130">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9fa04-130">Child Elements</span></span>  
 <span data-ttu-id="9fa04-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9fa04-131">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9fa04-132">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9fa04-132">Parent Elements</span></span>  
  
|<span data-ttu-id="9fa04-133">Élément</span><span class="sxs-lookup"><span data-stu-id="9fa04-133">Element</span></span>|<span data-ttu-id="9fa04-134">Description</span><span class="sxs-lookup"><span data-stu-id="9fa04-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9fa04-135">\<behavior></span><span class="sxs-lookup"><span data-stu-id="9fa04-135">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="9fa04-136">Spécifie le jeu de comportements du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="9fa04-136">Specifies the set of endpoint behaviors.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9fa04-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fa04-137">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.WebHttpElement>  
 <xref:System.ServiceModel.Description.WebHttpBehavior>  
 [<span data-ttu-id="9fa04-138">Intégration d’AJAX et prise en charge de JSON</span><span class="sxs-lookup"><span data-stu-id="9fa04-138">AJAX Integration and JSON Support</span></span>](../../../../../docs/framework/wcf/feature-details/ajax-integration-and-json-support.md)  
 [<span data-ttu-id="9fa04-139">\<webHttpBinding></span><span class="sxs-lookup"><span data-stu-id="9fa04-139">\<webHttpBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md)
