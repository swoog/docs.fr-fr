---
title: '&lt;webHttpEndpoint&gt;'
ms.date: 03/30/2017
ms.assetid: ecaaeb6f-ebd0-411d-8b53-92477cd45347
ms.openlocfilehash: b69ace451e90c824cdf8b911d596fdd158eb3f73
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491717"
---
# <a name="ltwebhttpendpointgt"></a><span data-ttu-id="3e7ef-102">&lt;webHttpEndpoint&gt;</span><span class="sxs-lookup"><span data-stu-id="3e7ef-102">&lt;webHttpEndpoint&gt;</span></span>
<span data-ttu-id="3e7ef-103">Cet élément de configuration définit un point de terminaison standard avec fixe [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) automatiquement une liaison qui ajoute le [ \<webHttp >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md) comportement.</span><span class="sxs-lookup"><span data-stu-id="3e7ef-103">This configuration element defines a standard endpoint with a fixed [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) binding that automatically adds the [\<webHttp>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md) behavior.</span></span> <span data-ttu-id="3e7ef-104">Utilisez ce point de terminaison lors de l'écriture d'un service REST.</span><span class="sxs-lookup"><span data-stu-id="3e7ef-104">Use this endpoint when writing a REST service.</span></span>  
  
<span data-ttu-id="3e7ef-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="3e7ef-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="3e7ef-106">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="3e7ef-106">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e7ef-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e7ef-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <webHttpEndpoint>
      <standardEndpoint automaticFormatSelectionEnabled="String"
                        defaultOutgoingResponseFormat="Xml/Json"
                        helpEnabled="Boolean"
                        webEndpointType="String" />
    </webHttpEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3e7ef-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3e7ef-108">Attributes and Elements</span></span>  
 <span data-ttu-id="3e7ef-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3e7ef-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3e7ef-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="3e7ef-110">Attributes</span></span>  
  
|<span data-ttu-id="3e7ef-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="3e7ef-111">Attribute</span></span>|<span data-ttu-id="3e7ef-112">Description</span><span class="sxs-lookup"><span data-stu-id="3e7ef-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="3e7ef-113">automaticFormatSelectionEnabled</span><span class="sxs-lookup"><span data-stu-id="3e7ef-113">automaticFormatSelectionEnabled</span></span>|<span data-ttu-id="3e7ef-114">Valeur booléenne qui indique si la sélection automatique du format est activée.</span><span class="sxs-lookup"><span data-stu-id="3e7ef-114">A Boolean value that indicates whether automatic format selection is enabled.</span></span><br /><br /> <span data-ttu-id="3e7ef-115">Lorsque la sélection automatique du format est activée, l'infrastructure analyse l'en-tête `Accept` du message de demande et détermine le format de réponse le plus approprié.</span><span class="sxs-lookup"><span data-stu-id="3e7ef-115">When automatic format selection is enabled, the infrastructure parses the `Accept` header of the request message and determines the most appropriate response format.</span></span> <span data-ttu-id="3e7ef-116">Si l'en-tête `Accept` ne spécifie pas de format de réponse approprié, l'infrastructure utilise le `Content-Type` du message de demande ou le format de réponse par défaut de l'opération.</span><span class="sxs-lookup"><span data-stu-id="3e7ef-116">If the `Accept` header does not specify a suitable response format, the infrastructure uses the `Content-Type` of the request message or the default response format of the operation.</span></span>|  
|<span data-ttu-id="3e7ef-117">defaultOutgoingResponseFormat</span><span class="sxs-lookup"><span data-stu-id="3e7ef-117">defaultOutgoingResponseFormat</span></span>|<span data-ttu-id="3e7ef-118">Attribut qui spécifie le format de réponse sortant par défaut.</span><span class="sxs-lookup"><span data-stu-id="3e7ef-118">An attribute that specifies the default outgoing response format.</span></span> <span data-ttu-id="3e7ef-119">Cet attribut est de type <xref:System.ServiceModel.Web.WebMessageFormat>.</span><span class="sxs-lookup"><span data-stu-id="3e7ef-119">This attribute is of the <xref:System.ServiceModel.Web.WebMessageFormat> type</span></span>|  
|<span data-ttu-id="3e7ef-120">helpEnabled</span><span class="sxs-lookup"><span data-stu-id="3e7ef-120">helpEnabled</span></span>|<span data-ttu-id="3e7ef-121">Valeur booléenne qui indique si la page d'aide HTTP est activée pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="3e7ef-121">A Boolean value that indicates whether the HTTP help page is enabled for the endpoint.</span></span>|  
|<span data-ttu-id="3e7ef-122">webEndpointType</span><span class="sxs-lookup"><span data-stu-id="3e7ef-122">webEndpointType</span></span>|<span data-ttu-id="3e7ef-123">Chaîne qui spécifie le type du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="3e7ef-123">A string that specifies the type of the endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3e7ef-124">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3e7ef-124">Child Elements</span></span>  
 <span data-ttu-id="3e7ef-125">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3e7ef-125">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3e7ef-126">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3e7ef-126">Parent Elements</span></span>  
  
|<span data-ttu-id="3e7ef-127">Élément</span><span class="sxs-lookup"><span data-stu-id="3e7ef-127">Element</span></span>|<span data-ttu-id="3e7ef-128">Description</span><span class="sxs-lookup"><span data-stu-id="3e7ef-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3e7ef-129">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="3e7ef-129">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="3e7ef-130">Collection de points de terminaison standard qui sont des points de terminaison prédéfinis dont une ou plusieurs propriétés (adresse, liaison, contrat) sont fixes.</span><span class="sxs-lookup"><span data-stu-id="3e7ef-130">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3e7ef-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e7ef-131">See also</span></span>
- <xref:System.ServiceModel.Description.WebHttpEndpoint>
- <xref:System.ServiceModel.Configuration.WebHttpEndpointElement>
