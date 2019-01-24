---
title: '&lt;servicePrincipalName&gt;'
ms.date: 03/30/2017
ms.assetid: 3f3b85d3-20f2-4cd8-8a6a-ee18befbd165
ms.openlocfilehash: 5d65b5956491e30066ece54a48374f1d7014552e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54657586"
---
# <a name="ltserviceprincipalnamegt"></a><span data-ttu-id="b448b-102">&lt;servicePrincipalName&gt;</span><span class="sxs-lookup"><span data-stu-id="b448b-102">&lt;servicePrincipalName&gt;</span></span>
<span data-ttu-id="b448b-103">Spécifie l'identité d'un service par son nom de principal du service (SPN).</span><span class="sxs-lookup"><span data-stu-id="b448b-103">Specifies the identity of a service by its Service Principal Name (SPN).</span></span>  
  
 <span data-ttu-id="b448b-104">Pour plus d’informations sur la définition du nom SPN, consultez [identité de Service et d’authentification](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="b448b-104">For more information about setting the SPN, see [Service Identity and Authentication](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
 <span data-ttu-id="b448b-105">\<identity></span><span class="sxs-lookup"><span data-stu-id="b448b-105">\<identity></span></span>  
<span data-ttu-id="b448b-106">\<servicePrincipalName></span><span class="sxs-lookup"><span data-stu-id="b448b-106">\<servicePrincipalName></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b448b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b448b-107">Syntax</span></span>  
  
```xml  
<servicePrincipalName value="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b448b-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b448b-108">Attributes and Elements</span></span>  
 <span data-ttu-id="b448b-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b448b-109">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b448b-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="b448b-110">Attributes</span></span>  
  
|<span data-ttu-id="b448b-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="b448b-111">Attribute</span></span>|<span data-ttu-id="b448b-112">Description</span><span class="sxs-lookup"><span data-stu-id="b448b-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b448b-113">par défaut</span><span class="sxs-lookup"><span data-stu-id="b448b-113">value</span></span>|<span data-ttu-id="b448b-114">Nom SPN par lequel un client identifie de manière unique l'instance d'un service.</span><span class="sxs-lookup"><span data-stu-id="b448b-114">The name by which a client uniquely identifies an instance of a service.</span></span> <span data-ttu-id="b448b-115">Si vous installez plusieurs instances d'un service sur les ordinateurs d'une forêt, chaque instance doit posséder son propre SPN.</span><span class="sxs-lookup"><span data-stu-id="b448b-115">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="b448b-116">Une instance de service donnée peut posséder plusieurs noms SPN si les clients peuvent utiliser plusieurs noms pour l'authentification.</span><span class="sxs-lookup"><span data-stu-id="b448b-116">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b448b-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b448b-117">Child Elements</span></span>  
 <span data-ttu-id="b448b-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b448b-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b448b-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b448b-119">Parent Elements</span></span>  
  
|<span data-ttu-id="b448b-120">Élément</span><span class="sxs-lookup"><span data-stu-id="b448b-120">Element</span></span>|<span data-ttu-id="b448b-121">Description</span><span class="sxs-lookup"><span data-stu-id="b448b-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b448b-122">\<identity></span><span class="sxs-lookup"><span data-stu-id="b448b-122">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="b448b-123">Spécifie l'identité du service à authentifier par le client.</span><span class="sxs-lookup"><span data-stu-id="b448b-123">Specifies the identity of the service to be authenticated by the client.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b448b-124">Notes</span><span class="sxs-lookup"><span data-stu-id="b448b-124">Remarks</span></span>  
 <span data-ttu-id="b448b-125">Un client Windows Communication Foundation (WCF) sécurisé qui se connecte à un point de terminaison avec cette identité utilise le SPN lors de l’authentification SSPI avec le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b448b-125">A secure Windows Communication Foundation (WCF) client that connects to an endpoint with this identity uses the SPN when performing SSPI authentication with the endpoint.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b448b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b448b-126">See also</span></span>
- <xref:System.ServiceModel.Configuration.IdentityElement>
- <xref:System.ServiceModel.EndpointAddress>
- <xref:System.ServiceModel.EndpointAddress.Identity%2A>
- <xref:System.ServiceModel.SpnEndpointIdentity>
- [<span data-ttu-id="b448b-127">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="b448b-127">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="b448b-128">\<identity></span><span class="sxs-lookup"><span data-stu-id="b448b-128">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)
