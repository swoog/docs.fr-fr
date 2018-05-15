---
title: '&lt;Nom principal de service&gt;'
ms.date: 03/30/2017
ms.assetid: 3f3b85d3-20f2-4cd8-8a6a-ee18befbd165
ms.openlocfilehash: e5c1f5a6986d57d20180560b12f5c7c5540a590d
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltserviceprincipalnamegt"></a><span data-ttu-id="5bd77-102">&lt;Nom principal de service&gt;</span><span class="sxs-lookup"><span data-stu-id="5bd77-102">&lt;servicePrincipalName&gt;</span></span>
<span data-ttu-id="5bd77-103">Spécifie l'identité d'un service par son nom de principal du service (SPN).</span><span class="sxs-lookup"><span data-stu-id="5bd77-103">Specifies the identity of a service by its Service Principal Name (SPN).</span></span>  
  
 <span data-ttu-id="5bd77-104">Pour plus d’informations sur la configuration du SPN, consultez [l’identité du Service et l’authentification](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="5bd77-104">For more information about setting the SPN, see [Service Identity and Authentication](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
 <span data-ttu-id="5bd77-105">\<identité ></span><span class="sxs-lookup"><span data-stu-id="5bd77-105">\<identity></span></span>  
<span data-ttu-id="5bd77-106">\<servicePrincipalName ></span><span class="sxs-lookup"><span data-stu-id="5bd77-106">\<servicePrincipalName></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5bd77-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bd77-107">Syntax</span></span>  
  
```xml  
<servicePrincipalName value = "String" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5bd77-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5bd77-108">Attributes and Elements</span></span>  
 <span data-ttu-id="5bd77-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5bd77-109">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5bd77-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="5bd77-110">Attributes</span></span>  
  
|<span data-ttu-id="5bd77-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="5bd77-111">Attribute</span></span>|<span data-ttu-id="5bd77-112">Description</span><span class="sxs-lookup"><span data-stu-id="5bd77-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5bd77-113">par défaut</span><span class="sxs-lookup"><span data-stu-id="5bd77-113">value</span></span>|<span data-ttu-id="5bd77-114">Nom SPN par lequel un client identifie de manière unique l'instance d'un service.</span><span class="sxs-lookup"><span data-stu-id="5bd77-114">The name by which a client uniquely identifies an instance of a service.</span></span> <span data-ttu-id="5bd77-115">Si vous installez plusieurs instances d'un service sur les ordinateurs d'une forêt, chaque instance doit posséder son propre SPN.</span><span class="sxs-lookup"><span data-stu-id="5bd77-115">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="5bd77-116">Une instance de service donnée peut posséder plusieurs noms SPN si les clients peuvent utiliser plusieurs noms pour l'authentification.</span><span class="sxs-lookup"><span data-stu-id="5bd77-116">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5bd77-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5bd77-117">Child Elements</span></span>  
 <span data-ttu-id="5bd77-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5bd77-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5bd77-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5bd77-119">Parent Elements</span></span>  
  
|<span data-ttu-id="5bd77-120">Élément</span><span class="sxs-lookup"><span data-stu-id="5bd77-120">Element</span></span>|<span data-ttu-id="5bd77-121">Description</span><span class="sxs-lookup"><span data-stu-id="5bd77-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5bd77-122">\<identité ></span><span class="sxs-lookup"><span data-stu-id="5bd77-122">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="5bd77-123">Spécifie l'identité du service à authentifier par le client.</span><span class="sxs-lookup"><span data-stu-id="5bd77-123">Specifies the identity of the service to be authenticated by the client.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5bd77-124">Notes</span><span class="sxs-lookup"><span data-stu-id="5bd77-124">Remarks</span></span>  
 <span data-ttu-id="5bd77-125">Un client Windows Communication Foundation (WCF) sécurisé qui se connecte à un point de terminaison avec cette identité utilise le SPN lors de l’authentification SSPI avec le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5bd77-125">A secure Windows Communication Foundation (WCF) client that connects to an endpoint with this identity uses the SPN when performing SSPI authentication with the endpoint.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5bd77-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bd77-126">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.IdentityElement>  
 <xref:System.ServiceModel.EndpointAddress>  
 <xref:System.ServiceModel.EndpointAddress.Identity%2A>  
 <xref:System.ServiceModel.SpnEndpointIdentity>  
 [<span data-ttu-id="5bd77-127">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="5bd77-127">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="5bd77-128">\<identité ></span><span class="sxs-lookup"><span data-stu-id="5bd77-128">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)
