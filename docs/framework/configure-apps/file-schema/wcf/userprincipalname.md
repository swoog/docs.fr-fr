---
title: <userPrincipalName>
ms.date: 03/30/2017
ms.assetid: 68032f69-149e-4613-bae4-18314d4fd294
ms.openlocfilehash: 19ea7e940fc7013fc526629a8aac4361ff3fb8bc
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55275014"
---
# <a name="userprincipalname"></a><span data-ttu-id="f323b-101">\<userPrincipalName></span><span class="sxs-lookup"><span data-stu-id="f323b-101">\<userPrincipalName></span></span>
<span data-ttu-id="f323b-102">Indique le nom d'utilisateur principal (UPN) d'un service à authentifier par le client.</span><span class="sxs-lookup"><span data-stu-id="f323b-102">Specifies the User Principal Name (UPN) of a service to be authenticated by the client.</span></span>  
  
 <span data-ttu-id="f323b-103">Pour plus d’informations sur la définition de l’UPN, consultez [identité de Service et d’authentification](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="f323b-103">For more information about setting the UPN, see [Service Identity and Authentication](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
<span data-ttu-id="f323b-104">\<identity></span><span class="sxs-lookup"><span data-stu-id="f323b-104">\<identity></span></span>  
<span data-ttu-id="f323b-105">\<userPrincipalName></span><span class="sxs-lookup"><span data-stu-id="f323b-105">\<userPrincipalName></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f323b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f323b-106">Syntax</span></span>  
  
```xml  
<userPrincipalName value="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f323b-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f323b-107">Attributes and Elements</span></span>  
 <span data-ttu-id="f323b-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f323b-108">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f323b-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="f323b-109">Attributes</span></span>  
  
|<span data-ttu-id="f323b-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="f323b-110">Attribute</span></span>|<span data-ttu-id="f323b-111">Description</span><span class="sxs-lookup"><span data-stu-id="f323b-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f323b-112">par défaut</span><span class="sxs-lookup"><span data-stu-id="f323b-112">value</span></span>|<span data-ttu-id="f323b-113">Nom de compte d'utilisateur (parfois connu sous le nom de connexion d'utilisateur) et nom de domaine identifiant le domaine dans lequel se trouve le compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f323b-113">A user account name (sometimes referred to as the user logon name) and a domain name identifying the domain in which the user account is located.</span></span> <span data-ttu-id="f323b-114">Il s'agit de la méthode de connexion standard à un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="f323b-114">This is the standard usage for logging on to a Windows domain.</span></span> <span data-ttu-id="f323b-115">Le format est : someone@example.com (comme pour une adresse de messagerie).</span><span class="sxs-lookup"><span data-stu-id="f323b-115">The format is: someone@example.com (as for an email address).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f323b-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f323b-116">Child Elements</span></span>  
 <span data-ttu-id="f323b-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f323b-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f323b-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f323b-118">Parent Elements</span></span>  
  
|<span data-ttu-id="f323b-119">Élément</span><span class="sxs-lookup"><span data-stu-id="f323b-119">Element</span></span>|<span data-ttu-id="f323b-120">Description</span><span class="sxs-lookup"><span data-stu-id="f323b-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f323b-121">\<identity></span><span class="sxs-lookup"><span data-stu-id="f323b-121">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="f323b-122">Spécifie l'identité du service à authentifier par le client.</span><span class="sxs-lookup"><span data-stu-id="f323b-122">Specifies the identity of the service to be authenticated by the client.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f323b-123">Notes</span><span class="sxs-lookup"><span data-stu-id="f323b-123">Remarks</span></span>  
 <span data-ttu-id="f323b-124">Un client Windows Communication Foundation (WCF) sécurisé qui se connecte à un point de terminaison avec cette identité utilise le nom UPN lors de l’authentification SSPI avec le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f323b-124">A secure Windows Communication Foundation (WCF) client that connects to an endpoint with this identity uses the UPN when performing SSPI authentication with the endpoint.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f323b-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="f323b-125">Example</span></span>  
 <span data-ttu-id="f323b-126">Le code de configuration suivant indique le nom UPN du service devant être authentifié par le client.</span><span class="sxs-lookup"><span data-stu-id="f323b-126">The following configuration code specifies the UPN of the service to be authenticated by the client.</span></span>  
  
```xml  
<identity>
  <userPrincipalName value="someone@cohowinery.com" />
</identity>
```  
  
## <a name="see-also"></a><span data-ttu-id="f323b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f323b-127">See also</span></span>
- <xref:System.ServiceModel.Configuration.IdentityElement>
- <xref:System.ServiceModel.EndpointAddress>
- <xref:System.ServiceModel.EndpointAddress.Identity%2A>
- <xref:System.ServiceModel.UpnEndpointIdentity>
- [<span data-ttu-id="f323b-128">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="f323b-128">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="f323b-129">\<identity></span><span class="sxs-lookup"><span data-stu-id="f323b-129">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)
