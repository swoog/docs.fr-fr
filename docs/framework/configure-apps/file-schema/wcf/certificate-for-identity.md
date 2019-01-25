---
title: '&lt;certificate&gt; de &lt;identity&gt;'
ms.date: 03/30/2017
ms.assetid: 4aeccaf7-8f23-495c-aa5f-5bd8b5d4a10c
ms.openlocfilehash: 28a1b992a70986652030ad42d4d4a5738350ae1f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54676157"
---
# <a name="ltcertificategt-for-ltidentitygt"></a><span data-ttu-id="e5472-102">&lt;certificate&gt; de &lt;identity&gt;</span><span class="sxs-lookup"><span data-stu-id="e5472-102">&lt;certificate&gt; for &lt;identity&gt;</span></span>
<span data-ttu-id="e5472-103">Spécifie un certificat X.509 utilisé pour valider un serveur auprès d'un client.</span><span class="sxs-lookup"><span data-stu-id="e5472-103">Specifies an X.509 certificate used to validate a server to a client.</span></span>  
  
 <span data-ttu-id="e5472-104">Pour plus d’informations sur la définition de la valeur de l’élément, consultez [identité de Service et d’authentification](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="e5472-104">For more information about setting the element value, see [Service Identity and Authentication](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
 <span data-ttu-id="e5472-105">\<identity></span><span class="sxs-lookup"><span data-stu-id="e5472-105">\<identity></span></span>  
<span data-ttu-id="e5472-106">\<certificate></span><span class="sxs-lookup"><span data-stu-id="e5472-106">\<certificate></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5472-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5472-107">Syntax</span></span>  
  
```xml  
<certificate encodedValue = "String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e5472-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e5472-108">Attributes and Elements</span></span>  
 <span data-ttu-id="e5472-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e5472-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e5472-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="e5472-110">Attributes</span></span>  
  
|<span data-ttu-id="e5472-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="e5472-111">Attribute</span></span>|<span data-ttu-id="e5472-112">Description</span><span class="sxs-lookup"><span data-stu-id="e5472-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e5472-113">encodedValue</span><span class="sxs-lookup"><span data-stu-id="e5472-113">encodedValue</span></span>|<span data-ttu-id="e5472-114">Encodage Base64 du certificat.</span><span class="sxs-lookup"><span data-stu-id="e5472-114">A Base64 encoding of the certificate.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e5472-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e5472-115">Child Elements</span></span>  
 <span data-ttu-id="e5472-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e5472-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e5472-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e5472-117">Parent Elements</span></span>  
  
|<span data-ttu-id="e5472-118">Élément</span><span class="sxs-lookup"><span data-stu-id="e5472-118">Element</span></span>|<span data-ttu-id="e5472-119">Description</span><span class="sxs-lookup"><span data-stu-id="e5472-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e5472-120">\<identity></span><span class="sxs-lookup"><span data-stu-id="e5472-120">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="e5472-121">Spécifie l'identité du service à authentifier par le client.</span><span class="sxs-lookup"><span data-stu-id="e5472-121">Specifies the identity of the service to be authenticated by the client.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="e5472-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="e5472-122">Example</span></span>  
 <span data-ttu-id="e5472-123">Le code suivant spécifie la représentation encodée d'un certificat qui est utilisée pour valider un serveur auprès d'un client.</span><span class="sxs-lookup"><span data-stu-id="e5472-123">The following code specifies the encoded representation of a certificate used to validate a server to a client.</span></span>  
  
```xml  
<identity>
  <certificate encodedValue="MIIBxjCCAXSgAwIBAgIQmXJgyu9tro1M98GifjtuoDAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC1Jvb3QgQWdlbmN5MB4XDTA2MDUxNzIxNDQyNVoXDTM5MTIzMTIzNTk1OVowKTEQMA4GA1UEChMHQ29udG9zbzEVMBMGA1UEAxMMaWRlbnRpdHkuY29tMIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDBmivcb8hYbh11hqVoDuB7zmJ2y230f" />
</identity>
```  
  
## <a name="see-also"></a><span data-ttu-id="e5472-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5472-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.IdentityElement>
- <xref:System.ServiceModel.EndpointAddress>
- <xref:System.ServiceModel.EndpointAddress.Identity%2A>
- <xref:System.ServiceModel.EndpointIdentity>
- [<span data-ttu-id="e5472-125">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="e5472-125">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="e5472-126">\<identity></span><span class="sxs-lookup"><span data-stu-id="e5472-126">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)
