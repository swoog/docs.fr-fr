---
title: '&lt;userPrincipalName&gt;'
ms.date: 03/30/2017
ms.assetid: 68032f69-149e-4613-bae4-18314d4fd294
ms.openlocfilehash: 1bb0c8ac4cbe11cdfa31beb16b00b3863acabf92
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33358675"
---
# <a name="ltuserprincipalnamegt"></a><span data-ttu-id="6eeae-102">&lt;userPrincipalName&gt;</span><span class="sxs-lookup"><span data-stu-id="6eeae-102">&lt;userPrincipalName&gt;</span></span>
<span data-ttu-id="6eeae-103">Indique le nom d'utilisateur principal (UPN) d'un service à authentifier par le client.</span><span class="sxs-lookup"><span data-stu-id="6eeae-103">Specifies the User Principal Name (UPN) of a service to be authenticated by the client.</span></span>  
  
 <span data-ttu-id="6eeae-104">Pour plus d’informations sur la définition de l’UPN, consultez [l’identité du Service et l’authentification](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="6eeae-104">For more information about setting the UPN, see [Service Identity and Authentication](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
<span data-ttu-id="6eeae-105">\<identité ></span><span class="sxs-lookup"><span data-stu-id="6eeae-105">\<identity></span></span>  
<span data-ttu-id="6eeae-106">\<userPrincipalName></span><span class="sxs-lookup"><span data-stu-id="6eeae-106">\<userPrincipalName></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6eeae-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6eeae-107">Syntax</span></span>  
  
```xml  
<userPrincipalName value="String" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6eeae-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6eeae-108">Attributes and Elements</span></span>  
 <span data-ttu-id="6eeae-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6eeae-109">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6eeae-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="6eeae-110">Attributes</span></span>  
  
|<span data-ttu-id="6eeae-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="6eeae-111">Attribute</span></span>|<span data-ttu-id="6eeae-112">Description</span><span class="sxs-lookup"><span data-stu-id="6eeae-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6eeae-113">par défaut</span><span class="sxs-lookup"><span data-stu-id="6eeae-113">value</span></span>|<span data-ttu-id="6eeae-114">Nom de compte d'utilisateur (parfois connu sous le nom de connexion d'utilisateur) et nom de domaine identifiant le domaine dans lequel se trouve le compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6eeae-114">A user account name (sometimes referred to as the user logon name) and a domain name identifying the domain in which the user account is located.</span></span> <span data-ttu-id="6eeae-115">Il s'agit de la méthode de connexion standard à un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="6eeae-115">This is the standard usage for logging on to a Windows domain.</span></span> <span data-ttu-id="6eeae-116">Le format est : someone@example.com (comme pour une adresse de messagerie).</span><span class="sxs-lookup"><span data-stu-id="6eeae-116">The format is: someone@example.com (as for an email address).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6eeae-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6eeae-117">Child Elements</span></span>  
 <span data-ttu-id="6eeae-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6eeae-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6eeae-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6eeae-119">Parent Elements</span></span>  
  
|<span data-ttu-id="6eeae-120">Élément</span><span class="sxs-lookup"><span data-stu-id="6eeae-120">Element</span></span>|<span data-ttu-id="6eeae-121">Description</span><span class="sxs-lookup"><span data-stu-id="6eeae-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6eeae-122">\<identité ></span><span class="sxs-lookup"><span data-stu-id="6eeae-122">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="6eeae-123">Spécifie l'identité du service à authentifier par le client.</span><span class="sxs-lookup"><span data-stu-id="6eeae-123">Specifies the identity of the service to be authenticated by the client.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6eeae-124">Notes</span><span class="sxs-lookup"><span data-stu-id="6eeae-124">Remarks</span></span>  
 <span data-ttu-id="6eeae-125">Un client Windows Communication Foundation (WCF) sécurisé qui se connecte à un point de terminaison avec cette identité utilise l’UPN lors de l’authentification SSPI avec le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="6eeae-125">A secure Windows Communication Foundation (WCF) client that connects to an endpoint with this identity uses the UPN when performing SSPI authentication with the endpoint.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6eeae-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="6eeae-126">Example</span></span>  
 <span data-ttu-id="6eeae-127">Le code de configuration suivant indique le nom UPN du service devant être authentifié par le client.</span><span class="sxs-lookup"><span data-stu-id="6eeae-127">The following configuration code specifies the UPN of the service to be authenticated by the client.</span></span>  
  
```xml  
<identity>  
  <userPrincipalName value="someone@cohowinery.com" />  
</identity>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6eeae-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6eeae-128">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.IdentityElement>  
 <xref:System.ServiceModel.EndpointAddress>  
 <xref:System.ServiceModel.EndpointAddress.Identity%2A>  
 <xref:System.ServiceModel.UpnEndpointIdentity>  
 [<span data-ttu-id="6eeae-129">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="6eeae-129">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="6eeae-130">\<identité ></span><span class="sxs-lookup"><span data-stu-id="6eeae-130">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)
