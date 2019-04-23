---
title: <webHttpEndpoint>
ms.date: 03/30/2017
ms.assetid: ecaaeb6f-ebd0-411d-8b53-92477cd45347
ms.openlocfilehash: 6fb31fca6ac38f6cb92ef087cc277a4d5066521c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59182453"
---
# <a name="webhttpendpoint"></a><span data-ttu-id="eabd3-101">\<webHttpEndpoint></span><span class="sxs-lookup"><span data-stu-id="eabd3-101">\<webHttpEndpoint></span></span>
<span data-ttu-id="eabd3-102">Cet élément de configuration définit un point de terminaison standard avec fixe [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) automatiquement une liaison qui ajoute le [ \<webHttp >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md) comportement.</span><span class="sxs-lookup"><span data-stu-id="eabd3-102">This configuration element defines a standard endpoint with a fixed [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) binding that automatically adds the [\<webHttp>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md) behavior.</span></span> <span data-ttu-id="eabd3-103">Utilisez ce point de terminaison lors de l'écriture d'un service REST.</span><span class="sxs-lookup"><span data-stu-id="eabd3-103">Use this endpoint when writing a REST service.</span></span>  
  
<span data-ttu-id="eabd3-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="eabd3-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="eabd3-105">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="eabd3-105">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eabd3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eabd3-106">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="eabd3-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="eabd3-107">Attributes and Elements</span></span>  
 <span data-ttu-id="eabd3-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="eabd3-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="eabd3-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="eabd3-109">Attributes</span></span>  
  
|<span data-ttu-id="eabd3-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="eabd3-110">Attribute</span></span>|<span data-ttu-id="eabd3-111">Description</span><span class="sxs-lookup"><span data-stu-id="eabd3-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="eabd3-112">automaticFormatSelectionEnabled</span><span class="sxs-lookup"><span data-stu-id="eabd3-112">automaticFormatSelectionEnabled</span></span>|<span data-ttu-id="eabd3-113">Valeur booléenne qui indique si la sélection automatique du format est activée.</span><span class="sxs-lookup"><span data-stu-id="eabd3-113">A Boolean value that indicates whether automatic format selection is enabled.</span></span><br /><br /> <span data-ttu-id="eabd3-114">Lorsque la sélection automatique du format est activée, l'infrastructure analyse l'en-tête `Accept` du message de demande et détermine le format de réponse le plus approprié.</span><span class="sxs-lookup"><span data-stu-id="eabd3-114">When automatic format selection is enabled, the infrastructure parses the `Accept` header of the request message and determines the most appropriate response format.</span></span> <span data-ttu-id="eabd3-115">Si l'en-tête `Accept` ne spécifie pas de format de réponse approprié, l'infrastructure utilise le `Content-Type` du message de demande ou le format de réponse par défaut de l'opération.</span><span class="sxs-lookup"><span data-stu-id="eabd3-115">If the `Accept` header does not specify a suitable response format, the infrastructure uses the `Content-Type` of the request message or the default response format of the operation.</span></span>|  
|<span data-ttu-id="eabd3-116">defaultOutgoingResponseFormat</span><span class="sxs-lookup"><span data-stu-id="eabd3-116">defaultOutgoingResponseFormat</span></span>|<span data-ttu-id="eabd3-117">Attribut qui spécifie le format de réponse sortant par défaut.</span><span class="sxs-lookup"><span data-stu-id="eabd3-117">An attribute that specifies the default outgoing response format.</span></span> <span data-ttu-id="eabd3-118">Cet attribut est de type <xref:System.ServiceModel.Web.WebMessageFormat>.</span><span class="sxs-lookup"><span data-stu-id="eabd3-118">This attribute is of the <xref:System.ServiceModel.Web.WebMessageFormat> type</span></span>|  
|<span data-ttu-id="eabd3-119">helpEnabled</span><span class="sxs-lookup"><span data-stu-id="eabd3-119">helpEnabled</span></span>|<span data-ttu-id="eabd3-120">Valeur booléenne qui indique si la page d'aide HTTP est activée pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="eabd3-120">A Boolean value that indicates whether the HTTP help page is enabled for the endpoint.</span></span>|  
|<span data-ttu-id="eabd3-121">webEndpointType</span><span class="sxs-lookup"><span data-stu-id="eabd3-121">webEndpointType</span></span>|<span data-ttu-id="eabd3-122">Chaîne qui spécifie le type du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="eabd3-122">A string that specifies the type of the endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="eabd3-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eabd3-123">Child Elements</span></span>  
 <span data-ttu-id="eabd3-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="eabd3-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="eabd3-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="eabd3-125">Parent Elements</span></span>  
  
|<span data-ttu-id="eabd3-126">Élément</span><span class="sxs-lookup"><span data-stu-id="eabd3-126">Element</span></span>|<span data-ttu-id="eabd3-127">Description</span><span class="sxs-lookup"><span data-stu-id="eabd3-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="eabd3-128">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="eabd3-128">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="eabd3-129">Collection de points de terminaison standard qui sont des points de terminaison prédéfinis dont une ou plusieurs propriétés (adresse, liaison, contrat) sont fixes.</span><span class="sxs-lookup"><span data-stu-id="eabd3-129">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="eabd3-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eabd3-130">See also</span></span>

- <xref:System.ServiceModel.Description.WebHttpEndpoint>
- <xref:System.ServiceModel.Configuration.WebHttpEndpointElement>
