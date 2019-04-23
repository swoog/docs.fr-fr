---
title: <xmlElement>
ms.date: 03/30/2017
ms.assetid: 395205c2-d8c0-4a5e-90f3-7ce3c085fccd
ms.openlocfilehash: a72641b438801cfd493c322297e7c384e83e687c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59230497"
---
# <a name="xmlelement"></a><span data-ttu-id="f2904-101">\<xmlElement></span><span class="sxs-lookup"><span data-stu-id="f2904-101">\<xmlElement></span></span>
<span data-ttu-id="f2904-102">Spécifie un élément XML qui est envoyé dans le corps du message au service d'émission de jeton de sécurité (STS) lors de la demande d'un jeton.</span><span class="sxs-lookup"><span data-stu-id="f2904-102">Specifies an XML element that is sent in the message body to the Security Token Service when requesting a token.</span></span>  
  
 <span data-ttu-id="f2904-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="f2904-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="f2904-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="f2904-104">\<bindings></span></span>  
<span data-ttu-id="f2904-105">\<wsFederatedBinding></span><span class="sxs-lookup"><span data-stu-id="f2904-105">\<wsFederatedBinding></span></span>  
<span data-ttu-id="f2904-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="f2904-106">\<binding></span></span>  
<span data-ttu-id="f2904-107">\<security></span><span class="sxs-lookup"><span data-stu-id="f2904-107">\<security></span></span>  
<span data-ttu-id="f2904-108">\<message></span><span class="sxs-lookup"><span data-stu-id="f2904-108">\<message></span></span>  
<span data-ttu-id="f2904-109">\<tokenRequestParameters></span><span class="sxs-lookup"><span data-stu-id="f2904-109">\<tokenRequestParameters></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2904-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2904-110">Syntax</span></span>  
  
```xml  
<tokenRequestParameters>
  <xmlElement xmlElement="String" />
</tokenRequestParameters>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f2904-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f2904-111">Attributes and Elements</span></span>  
 <span data-ttu-id="f2904-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f2904-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f2904-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="f2904-113">Attributes</span></span>  
  
|<span data-ttu-id="f2904-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="f2904-114">Attribute</span></span>|<span data-ttu-id="f2904-115">Description</span><span class="sxs-lookup"><span data-stu-id="f2904-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f2904-116">xmlElement</span><span class="sxs-lookup"><span data-stu-id="f2904-116">xmlElement</span></span>|<span data-ttu-id="f2904-117">Chaîne spécifiant un élément XML qui est envoyé dans le corps du message au service d'émission de jeton de sécurité (STS) lors de la demande d'un jeton.</span><span class="sxs-lookup"><span data-stu-id="f2904-117">A string specifying an XML element that is sent in the message body to the Security Token Service when requesting a token.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f2904-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f2904-118">Child Elements</span></span>  
 <span data-ttu-id="f2904-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f2904-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f2904-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f2904-120">Parent Elements</span></span>  
  
|<span data-ttu-id="f2904-121">Élément</span><span class="sxs-lookup"><span data-stu-id="f2904-121">Element</span></span>|<span data-ttu-id="f2904-122">Description</span><span class="sxs-lookup"><span data-stu-id="f2904-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f2904-123">\<tokenRequestParameters></span><span class="sxs-lookup"><span data-stu-id="f2904-123">\<tokenRequestParameters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/tokenrequestparameters.md)|<span data-ttu-id="f2904-124">Collection de paramètres de demande de jeton.</span><span class="sxs-lookup"><span data-stu-id="f2904-124">A collection of token request parameters.</span></span> <span data-ttu-id="f2904-125">Chaque paramètre est un élément XML.</span><span class="sxs-lookup"><span data-stu-id="f2904-125">Each parameter is an XML element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f2904-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2904-126">See also</span></span>

- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.TokenRequestParameters%2A>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.TokenRequestParameters%2A>
- [<span data-ttu-id="f2904-127">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="f2904-127">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="f2904-128">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="f2904-128">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="f2904-129">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="f2904-129">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="f2904-130">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="f2904-130">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="f2904-131">Liaisons</span><span class="sxs-lookup"><span data-stu-id="f2904-131">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
