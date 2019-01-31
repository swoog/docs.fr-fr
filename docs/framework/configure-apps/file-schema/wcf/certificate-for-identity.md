---
title: <certificate> pour <identity>
ms.date: 03/30/2017
ms.assetid: 4aeccaf7-8f23-495c-aa5f-5bd8b5d4a10c
ms.openlocfilehash: 804600e4eb1612cd8654fc58ec3df28596c1e84d
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55265036"
---
# <a name="certificate-for-identity"></a><span data-ttu-id="5e38c-102">\<certificat > pour \<identité ></span><span class="sxs-lookup"><span data-stu-id="5e38c-102">\<certificate> for \<identity></span></span>
<span data-ttu-id="5e38c-103">Spécifie un certificat X.509 utilisé pour valider un serveur auprès d'un client.</span><span class="sxs-lookup"><span data-stu-id="5e38c-103">Specifies an X.509 certificate used to validate a server to a client.</span></span>  
  
 <span data-ttu-id="5e38c-104">Pour plus d’informations sur la définition de la valeur de l’élément, consultez [identité de Service et d’authentification](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="5e38c-104">For more information about setting the element value, see [Service Identity and Authentication](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
 <span data-ttu-id="5e38c-105">\<identity></span><span class="sxs-lookup"><span data-stu-id="5e38c-105">\<identity></span></span>  
<span data-ttu-id="5e38c-106">\<certificate></span><span class="sxs-lookup"><span data-stu-id="5e38c-106">\<certificate></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e38c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e38c-107">Syntax</span></span>  
  
```xml  
<certificate encodedValue = "String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5e38c-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5e38c-108">Attributes and Elements</span></span>  
 <span data-ttu-id="5e38c-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5e38c-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5e38c-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="5e38c-110">Attributes</span></span>  
  
|<span data-ttu-id="5e38c-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="5e38c-111">Attribute</span></span>|<span data-ttu-id="5e38c-112">Description</span><span class="sxs-lookup"><span data-stu-id="5e38c-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5e38c-113">encodedValue</span><span class="sxs-lookup"><span data-stu-id="5e38c-113">encodedValue</span></span>|<span data-ttu-id="5e38c-114">Encodage Base64 du certificat.</span><span class="sxs-lookup"><span data-stu-id="5e38c-114">A Base64 encoding of the certificate.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5e38c-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5e38c-115">Child Elements</span></span>  
 <span data-ttu-id="5e38c-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5e38c-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5e38c-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5e38c-117">Parent Elements</span></span>  
  
|<span data-ttu-id="5e38c-118">Élément</span><span class="sxs-lookup"><span data-stu-id="5e38c-118">Element</span></span>|<span data-ttu-id="5e38c-119">Description</span><span class="sxs-lookup"><span data-stu-id="5e38c-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5e38c-120">\<identity></span><span class="sxs-lookup"><span data-stu-id="5e38c-120">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="5e38c-121">Spécifie l'identité du service à authentifier par le client.</span><span class="sxs-lookup"><span data-stu-id="5e38c-121">Specifies the identity of the service to be authenticated by the client.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="5e38c-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="5e38c-122">Example</span></span>  
 <span data-ttu-id="5e38c-123">Le code suivant spécifie la représentation encodée d'un certificat qui est utilisée pour valider un serveur auprès d'un client.</span><span class="sxs-lookup"><span data-stu-id="5e38c-123">The following code specifies the encoded representation of a certificate used to validate a server to a client.</span></span>  
  
```xml  
<identity>
  <certificate encodedValue="MIIBxjCCAXSgAwIBAgIQmXJgyu9tro1M98GifjtuoDAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC1Jvb3QgQWdlbmN5MB4XDTA2MDUxNzIxNDQyNVoXDTM5MTIzMTIzNTk1OVowKTEQMA4GA1UEChMHQ29udG9zbzEVMBMGA1UEAxMMaWRlbnRpdHkuY29tMIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDBmivcb8hYbh11hqVoDuB7zmJ2y230f" />
</identity>
```  
  
## <a name="see-also"></a><span data-ttu-id="5e38c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e38c-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.IdentityElement>
- <xref:System.ServiceModel.EndpointAddress>
- <xref:System.ServiceModel.EndpointAddress.Identity%2A>
- <xref:System.ServiceModel.EndpointIdentity>
- [<span data-ttu-id="5e38c-125">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="5e38c-125">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="5e38c-126">\<identity></span><span class="sxs-lookup"><span data-stu-id="5e38c-126">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)
