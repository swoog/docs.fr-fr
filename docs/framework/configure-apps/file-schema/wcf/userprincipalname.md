---
title: <userPrincipalName>
ms.date: 03/30/2017
ms.assetid: 68032f69-149e-4613-bae4-18314d4fd294
ms.openlocfilehash: 9e7b845d39495dba1d1a19af95faf308b8b8c0fa
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59188244"
---
# <a name="userprincipalname"></a><span data-ttu-id="0fdea-101">\<userPrincipalName></span><span class="sxs-lookup"><span data-stu-id="0fdea-101">\<userPrincipalName></span></span>
<span data-ttu-id="0fdea-102">Indique le nom d'utilisateur principal (UPN) d'un service à authentifier par le client.</span><span class="sxs-lookup"><span data-stu-id="0fdea-102">Specifies the User Principal Name (UPN) of a service to be authenticated by the client.</span></span>  
  
 <span data-ttu-id="0fdea-103">Pour plus d’informations sur la définition de l’UPN, consultez [identité de Service et d’authentification](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="0fdea-103">For more information about setting the UPN, see [Service Identity and Authentication](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
<span data-ttu-id="0fdea-104">\<identity></span><span class="sxs-lookup"><span data-stu-id="0fdea-104">\<identity></span></span>  
<span data-ttu-id="0fdea-105">\<userPrincipalName></span><span class="sxs-lookup"><span data-stu-id="0fdea-105">\<userPrincipalName></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0fdea-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fdea-106">Syntax</span></span>  
  
```xml  
<userPrincipalName value="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0fdea-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0fdea-107">Attributes and Elements</span></span>  
 <span data-ttu-id="0fdea-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0fdea-108">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0fdea-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="0fdea-109">Attributes</span></span>  
  
|<span data-ttu-id="0fdea-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="0fdea-110">Attribute</span></span>|<span data-ttu-id="0fdea-111">Description</span><span class="sxs-lookup"><span data-stu-id="0fdea-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0fdea-112">par défaut</span><span class="sxs-lookup"><span data-stu-id="0fdea-112">value</span></span>|<span data-ttu-id="0fdea-113">Nom de compte d'utilisateur (parfois connu sous le nom de connexion d'utilisateur) et nom de domaine identifiant le domaine dans lequel se trouve le compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0fdea-113">A user account name (sometimes referred to as the user logon name) and a domain name identifying the domain in which the user account is located.</span></span> <span data-ttu-id="0fdea-114">Il s'agit de la méthode de connexion standard à un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="0fdea-114">This is the standard usage for logging on to a Windows domain.</span></span> <span data-ttu-id="0fdea-115">Le format est : someone@example.com (comme pour une adresse de messagerie).</span><span class="sxs-lookup"><span data-stu-id="0fdea-115">The format is: someone@example.com (as for an email address).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0fdea-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0fdea-116">Child Elements</span></span>  
 <span data-ttu-id="0fdea-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0fdea-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0fdea-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0fdea-118">Parent Elements</span></span>  
  
|<span data-ttu-id="0fdea-119">Élément</span><span class="sxs-lookup"><span data-stu-id="0fdea-119">Element</span></span>|<span data-ttu-id="0fdea-120">Description</span><span class="sxs-lookup"><span data-stu-id="0fdea-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0fdea-121">\<identity></span><span class="sxs-lookup"><span data-stu-id="0fdea-121">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="0fdea-122">Spécifie l'identité du service à authentifier par le client.</span><span class="sxs-lookup"><span data-stu-id="0fdea-122">Specifies the identity of the service to be authenticated by the client.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0fdea-123">Notes</span><span class="sxs-lookup"><span data-stu-id="0fdea-123">Remarks</span></span>  
 <span data-ttu-id="0fdea-124">Un client Windows Communication Foundation (WCF) sécurisé qui se connecte à un point de terminaison avec cette identité utilise le nom UPN lors de l’authentification SSPI avec le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0fdea-124">A secure Windows Communication Foundation (WCF) client that connects to an endpoint with this identity uses the UPN when performing SSPI authentication with the endpoint.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0fdea-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="0fdea-125">Example</span></span>  
 <span data-ttu-id="0fdea-126">Le code de configuration suivant indique le nom UPN du service devant être authentifié par le client.</span><span class="sxs-lookup"><span data-stu-id="0fdea-126">The following configuration code specifies the UPN of the service to be authenticated by the client.</span></span>  
  
```xml  
<identity>
  <userPrincipalName value="someone@cohowinery.com" />
</identity>
```  
  
## <a name="see-also"></a><span data-ttu-id="0fdea-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fdea-127">See also</span></span>

- <xref:System.ServiceModel.Configuration.IdentityElement>
- <xref:System.ServiceModel.EndpointAddress>
- <xref:System.ServiceModel.EndpointAddress.Identity%2A>
- <xref:System.ServiceModel.UpnEndpointIdentity>
- [<span data-ttu-id="0fdea-128">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="0fdea-128">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="0fdea-129">\<identity></span><span class="sxs-lookup"><span data-stu-id="0fdea-129">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)
