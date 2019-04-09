---
title: <webHttp>
ms.date: 03/30/2017
ms.assetid: 1f9d0754-d41e-44ce-a298-e51cb3096c64
ms.openlocfilehash: 795e61b9054d2ea9276970988018c50099bcbe17
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59129647"
---
# <a name="webhttp"></a><span data-ttu-id="1eaff-101">\<webHttp></span><span class="sxs-lookup"><span data-stu-id="1eaff-101">\<webHttp></span></span>
<span data-ttu-id="1eaff-102">Cet élément spécifie le <xref:System.ServiceModel.Description.WebHttpBehavior> d'un point de terminaison via la configuration.</span><span class="sxs-lookup"><span data-stu-id="1eaff-102">This element specifies the <xref:System.ServiceModel.Description.WebHttpBehavior> on an endpoint through configuration.</span></span> <span data-ttu-id="1eaff-103">Ce comportement est utilisé conjointement avec le [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) permet de liaison standard, le modèle de programmation Web pour un service Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="1eaff-103">This behavior, when used in conjunction with the [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) standard binding, enables the Web programming model for a Windows Communication Foundation (WCF) service.</span></span>  
  
 <span data-ttu-id="1eaff-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="1eaff-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="1eaff-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="1eaff-105">\<behaviors></span></span>  
<span data-ttu-id="1eaff-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="1eaff-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="1eaff-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="1eaff-107">\<behavior></span></span>  
<span data-ttu-id="1eaff-108">\<webHttp></span><span class="sxs-lookup"><span data-stu-id="1eaff-108">\<webHttp></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1eaff-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1eaff-109">Syntax</span></span>  
  
```xml  
<webHttp />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1eaff-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1eaff-110">Attributes and Elements</span></span>  
 <span data-ttu-id="1eaff-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1eaff-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1eaff-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="1eaff-112">Attributes</span></span>  
  
|<span data-ttu-id="1eaff-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="1eaff-113">Attribute</span></span>|<span data-ttu-id="1eaff-114">Description</span><span class="sxs-lookup"><span data-stu-id="1eaff-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="1eaff-115">automaticFormatSelectionEnabled</span><span class="sxs-lookup"><span data-stu-id="1eaff-115">automaticFormatSelectionEnabled</span></span>|<span data-ttu-id="1eaff-116">Lorsque cette propriété a la valeur `true`, l'infrastructure WCF détermine le meilleur format à utiliser.</span><span class="sxs-lookup"><span data-stu-id="1eaff-116">When this property is set to `true`, the WCF infrastructure determines the best format to use.</span></span> <span data-ttu-id="1eaff-117">La sélection automatique du format est désactivée par défaut à des fins de compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="1eaff-117">Automatic format selection is disabled by default for backwards compatibility.</span></span> <span data-ttu-id="1eaff-118">La sélection automatique du format peut être activée par programme ou par configuration.</span><span class="sxs-lookup"><span data-stu-id="1eaff-118">Automatic format selection can be enabled programmatically or through configuration.</span></span>|  
|<span data-ttu-id="1eaff-119">defaultBodyStyle</span><span class="sxs-lookup"><span data-stu-id="1eaff-119">defaultBodyStyle</span></span>|<span data-ttu-id="1eaff-120">Spécifie le style du corps par défaut des messages retournés.</span><span class="sxs-lookup"><span data-stu-id="1eaff-120">Specifies the default body style of returned messages.</span></span> <span data-ttu-id="1eaff-121">Pour plus d’informations, consultez <xref:System.ServiceModel.Web.WebMessageBodyStyle> et [mise en forme de WCF Web HTTP](../../../../../docs/framework/wcf/feature-details/wcf-web-http-formatting.md).</span><span class="sxs-lookup"><span data-stu-id="1eaff-121">For more information, see <xref:System.ServiceModel.Web.WebMessageBodyStyle> and [WCF Web HTTP Formatting](../../../../../docs/framework/wcf/feature-details/wcf-web-http-formatting.md).</span></span>|  
|<span data-ttu-id="1eaff-122">defaultOutgoingResponseFormat</span><span class="sxs-lookup"><span data-stu-id="1eaff-122">defaultOutgoingResponseFormat</span></span>|<span data-ttu-id="1eaff-123">Spécifie le format de réponse sortante par défaut des messages.</span><span class="sxs-lookup"><span data-stu-id="1eaff-123">Specifies the default outgoing response format for messages.</span></span> <span data-ttu-id="1eaff-124">Pour plus d’informations, consultez [mise en forme de WCF Web HTTP](../../../../../docs/framework/wcf/feature-details/wcf-web-http-formatting.md).</span><span class="sxs-lookup"><span data-stu-id="1eaff-124">For more information, see [WCF Web HTTP Formatting](../../../../../docs/framework/wcf/feature-details/wcf-web-http-formatting.md).</span></span>|  
|<span data-ttu-id="1eaff-125">faultExceptionEnabled</span><span class="sxs-lookup"><span data-stu-id="1eaff-125">faultExceptionEnabled</span></span>|<span data-ttu-id="1eaff-126">Obtient ou définit l’indicateur qui spécifie si FaultException est généré quand une erreur de serveur interne (code d’état HTTP : 500) se produit.</span><span class="sxs-lookup"><span data-stu-id="1eaff-126">Gets or sets the flag that specifies whether a FaultException is generated when an internal server error (HTTP status code: 500) occurs.</span></span>|  
|<span data-ttu-id="1eaff-127">helpEnabled</span><span class="sxs-lookup"><span data-stu-id="1eaff-127">helpEnabled</span></span>|<span data-ttu-id="1eaff-128">Obtient ou définit une valeur qui détermine si la page d'aide est activée.</span><span class="sxs-lookup"><span data-stu-id="1eaff-128">Gets or sets a value that determines if the Help page is enabled.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1eaff-129">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1eaff-129">Child Elements</span></span>  
 <span data-ttu-id="1eaff-130">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1eaff-130">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1eaff-131">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1eaff-131">Parent Elements</span></span>  
  
|<span data-ttu-id="1eaff-132">Élément</span><span class="sxs-lookup"><span data-stu-id="1eaff-132">Element</span></span>|<span data-ttu-id="1eaff-133">Description</span><span class="sxs-lookup"><span data-stu-id="1eaff-133">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1eaff-134">\<behavior></span><span class="sxs-lookup"><span data-stu-id="1eaff-134">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="1eaff-135">Spécifie le jeu de comportements du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1eaff-135">Specifies the set of endpoint behaviors.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1eaff-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1eaff-136">See also</span></span>

- <xref:System.ServiceModel.Configuration.WebHttpElement>
- <xref:System.ServiceModel.Description.WebHttpBehavior>
- [<span data-ttu-id="1eaff-137">Intégration d'AJAX et prise en charge de JSON</span><span class="sxs-lookup"><span data-stu-id="1eaff-137">AJAX Integration and JSON Support</span></span>](../../../../../docs/framework/wcf/feature-details/ajax-integration-and-json-support.md)
- [<span data-ttu-id="1eaff-138">\<webHttpBinding></span><span class="sxs-lookup"><span data-stu-id="1eaff-138">\<webHttpBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md)
