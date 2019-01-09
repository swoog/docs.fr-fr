---
title: '&lt;certificate&gt; de &lt;identity&gt;'
ms.date: 03/30/2017
ms.assetid: 4aeccaf7-8f23-495c-aa5f-5bd8b5d4a10c
ms.openlocfilehash: 0b65157aea84760f3e52bc294f7559967fc308f1
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146912"
---
# <a name="ltcertificategt-for-ltidentitygt"></a><span data-ttu-id="54936-102">&lt;certificate&gt; de &lt;identity&gt;</span><span class="sxs-lookup"><span data-stu-id="54936-102">&lt;certificate&gt; for &lt;identity&gt;</span></span>
<span data-ttu-id="54936-103">Spécifie un certificat X.509 utilisé pour valider un serveur auprès d'un client.</span><span class="sxs-lookup"><span data-stu-id="54936-103">Specifies an X.509 certificate used to validate a server to a client.</span></span>  
  
 <span data-ttu-id="54936-104">Pour plus d’informations sur la définition de la valeur de l’élément, consultez [identité de Service et d’authentification](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="54936-104">For more information about setting the element value, see [Service Identity and Authentication](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
 <span data-ttu-id="54936-105">\<identité ></span><span class="sxs-lookup"><span data-stu-id="54936-105">\<identity></span></span>  
<span data-ttu-id="54936-106">\<certificate></span><span class="sxs-lookup"><span data-stu-id="54936-106">\<certificate></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="54936-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54936-107">Syntax</span></span>  
  
```xml  
<certificate encodedValue = "String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="54936-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="54936-108">Attributes and Elements</span></span>  
 <span data-ttu-id="54936-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="54936-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="54936-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="54936-110">Attributes</span></span>  
  
|<span data-ttu-id="54936-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="54936-111">Attribute</span></span>|<span data-ttu-id="54936-112">Description</span><span class="sxs-lookup"><span data-stu-id="54936-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="54936-113">encodedValue</span><span class="sxs-lookup"><span data-stu-id="54936-113">encodedValue</span></span>|<span data-ttu-id="54936-114">Encodage Base64 du certificat.</span><span class="sxs-lookup"><span data-stu-id="54936-114">A Base64 encoding of the certificate.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="54936-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="54936-115">Child Elements</span></span>  
 <span data-ttu-id="54936-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="54936-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="54936-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="54936-117">Parent Elements</span></span>  
  
|<span data-ttu-id="54936-118">Élément</span><span class="sxs-lookup"><span data-stu-id="54936-118">Element</span></span>|<span data-ttu-id="54936-119">Description</span><span class="sxs-lookup"><span data-stu-id="54936-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="54936-120">\<identité ></span><span class="sxs-lookup"><span data-stu-id="54936-120">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="54936-121">Spécifie l'identité du service à authentifier par le client.</span><span class="sxs-lookup"><span data-stu-id="54936-121">Specifies the identity of the service to be authenticated by the client.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="54936-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="54936-122">Example</span></span>  
 <span data-ttu-id="54936-123">Le code suivant spécifie la représentation encodée d'un certificat qui est utilisée pour valider un serveur auprès d'un client.</span><span class="sxs-lookup"><span data-stu-id="54936-123">The following code specifies the encoded representation of a certificate used to validate a server to a client.</span></span>  
  
```xml  
<identity>
  <certificate encodedValue="MIIBxjCCAXSgAwIBAgIQmXJgyu9tro1M98GifjtuoDAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC1Jvb3QgQWdlbmN5MB4XDTA2MDUxNzIxNDQyNVoXDTM5MTIzMTIzNTk1OVowKTEQMA4GA1UEChMHQ29udG9zbzEVMBMGA1UEAxMMaWRlbnRpdHkuY29tMIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDBmivcb8hYbh11hqVoDuB7zmJ2y230f" />
</identity>
```  
  
## <a name="see-also"></a><span data-ttu-id="54936-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54936-124">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.IdentityElement>  
 <xref:System.ServiceModel.EndpointAddress>  
 <xref:System.ServiceModel.EndpointAddress.Identity%2A>  
 <xref:System.ServiceModel.EndpointIdentity>  
 [<span data-ttu-id="54936-125">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="54936-125">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="54936-126">\<identité ></span><span class="sxs-lookup"><span data-stu-id="54936-126">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)
