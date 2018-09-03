---
title: '&lt;DNS&gt;'
ms.date: 03/30/2017
ms.assetid: 81819dae-4825-43b7-bccd-f16d2d3d2f06
ms.openlocfilehash: 2f5b9d5e1bc57230adbb32664e9ae15d3c71d46f
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43472031"
---
# <a name="ltdnsgt"></a><span data-ttu-id="09499-102">&lt;DNS&gt;</span><span class="sxs-lookup"><span data-stu-id="09499-102">&lt;dns&gt;</span></span>
<span data-ttu-id="09499-103">Spécifie l'identité attendue du serveur.</span><span class="sxs-lookup"><span data-stu-id="09499-103">Specifies the expected identity of the server.</span></span> <span data-ttu-id="09499-104">Cette identité est valide pour le mode d'authentification du certificat X509 si le certificat du serveur contient un DNS avec la même valeur.</span><span class="sxs-lookup"><span data-stu-id="09499-104">This identity is valid for X509 Certificate authentication mode if the server’s certificate contains a DNS with the same value.</span></span> <span data-ttu-id="09499-105">Elle est également valide pour le mode d'authentification Windows si le SPN a la même valeur.</span><span class="sxs-lookup"><span data-stu-id="09499-105">It is also valid for Windows authentication mode if the SPN has the same value.</span></span>  
  
 <span data-ttu-id="09499-106">Pour plus d’informations sur la définition de la valeur de l’élément, consultez [identité de Service et d’authentification](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="09499-106">For more information about setting the element value, see [Service Identity and Authentication](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
 <span data-ttu-id="09499-107">\<identité ></span><span class="sxs-lookup"><span data-stu-id="09499-107">\<identity></span></span>  
<span data-ttu-id="09499-108">\<DNS ></span><span class="sxs-lookup"><span data-stu-id="09499-108">\<dns></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="09499-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09499-109">Syntax</span></span>  
  
```xml  
<dns value = "String" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="09499-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="09499-110">Attributes and Elements</span></span>  
 <span data-ttu-id="09499-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="09499-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="09499-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="09499-112">Attributes</span></span>  
  
|<span data-ttu-id="09499-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="09499-113">Attribute</span></span>|<span data-ttu-id="09499-114">Description</span><span class="sxs-lookup"><span data-stu-id="09499-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="09499-115">par défaut</span><span class="sxs-lookup"><span data-stu-id="09499-115">value</span></span>|<span data-ttu-id="09499-116">Système DNS du certificat.</span><span class="sxs-lookup"><span data-stu-id="09499-116">The DNS of the certificate.</span></span> <span data-ttu-id="09499-117">Le système DNS est un protocole standard utilisé pour localiser des ordinateurs sur un réseau IP.</span><span class="sxs-lookup"><span data-stu-id="09499-117">DNS is an industry-standard protocol used to locate computers on an IP-based network.</span></span> <span data-ttu-id="09499-118">Les utilisateurs peuvent se souvenir de noms complets, tels que [ https://go.microsoft.com/fwlink/?prd=10929 ](https://go.microsoft.com/fwlink/?prd=10929) ou [ https://go.microsoft.com/fwlink/?LinkID=96165 ](https://go.microsoft.com/fwlink/?LinkID=96165), il est plus facile que le nombre que des adresses, 207.46.131.137.</span><span class="sxs-lookup"><span data-stu-id="09499-118">Users can remember display names, such as [https://go.microsoft.com/fwlink/?prd=10929](https://go.microsoft.com/fwlink/?prd=10929) or [https://go.microsoft.com/fwlink/?LinkID=96165](https://go.microsoft.com/fwlink/?LinkID=96165), easier than number-based addresses, such as 207.46.131.137.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="09499-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="09499-119">Child Elements</span></span>  
 <span data-ttu-id="09499-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="09499-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="09499-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="09499-121">Parent Elements</span></span>  
  
|<span data-ttu-id="09499-122">Élément</span><span class="sxs-lookup"><span data-stu-id="09499-122">Element</span></span>|<span data-ttu-id="09499-123">Description</span><span class="sxs-lookup"><span data-stu-id="09499-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="09499-124">\<identité ></span><span class="sxs-lookup"><span data-stu-id="09499-124">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="09499-125">Spécifie l'identité du service à authentifier par le client.</span><span class="sxs-lookup"><span data-stu-id="09499-125">Specifies the identity of the service to be authenticated by the client.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="09499-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="09499-126">Example</span></span>  
 <span data-ttu-id="09499-127">Le code de configuration suivant spécifie le système DNS d'un certificat X.509 utilisé pour authentifier un serveur.</span><span class="sxs-lookup"><span data-stu-id="09499-127">The following configuration code specifies the DNS of an X.509 certificate that is used to authenticate a server.</span></span>  
  
```xml  
<identity>  
  <dns value = "www.cohowinery.com" />  
</identity>  
```  
  
## <a name="see-also"></a><span data-ttu-id="09499-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09499-128">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.IdentityElement>  
 <xref:System.ServiceModel.EndpointAddress>  
 <xref:System.ServiceModel.EndpointAddress.Identity%2A>  
 <xref:System.ServiceModel.DnsEndpointIdentity>  
 [<span data-ttu-id="09499-129">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="09499-129">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="09499-130">\<identité ></span><span class="sxs-lookup"><span data-stu-id="09499-130">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)
