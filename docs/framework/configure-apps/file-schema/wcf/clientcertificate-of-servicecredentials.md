---
title: <clientCertificate> de <serviceCredentials>
ms.date: 03/30/2017
ms.assetid: 90ad03aa-2317-43dd-8a72-6d24cdcad15c
ms.openlocfilehash: 26ebac6439a90959e3a926e6a36c9044251a4aae
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59107982"
---
# <a name="clientcertificate-of-servicecredentials"></a><span data-ttu-id="e603a-102">\<clientCertificate> of \<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="e603a-102">\<clientCertificate> of \<serviceCredentials></span></span>
<span data-ttu-id="e603a-103">Définit un certificat X.509 permettant de signer et de chiffrer des messages destinés à un client et envoyés à partir d'un service selon un modèle de communication duplex.</span><span class="sxs-lookup"><span data-stu-id="e603a-103">Defines an X.509 certificate used to sign and encrypt messages to a client form a service in a duplex communication pattern.</span></span>  
  
 <span data-ttu-id="e603a-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="e603a-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="e603a-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="e603a-105">\<behaviors></span></span>  
<span data-ttu-id="e603a-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="e603a-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="e603a-107">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="e603a-107">\<serviceBehaviors></span></span>  
<span data-ttu-id="e603a-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="e603a-108">\<behavior></span></span>  
<span data-ttu-id="e603a-109">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="e603a-109">\<serviceCredentials></span></span>  
<span data-ttu-id="e603a-110">\<clientCertificate></span><span class="sxs-lookup"><span data-stu-id="e603a-110">\<clientCertificate></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e603a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e603a-111">Syntax</span></span>  
  
```xml  
<clientCertificate>
  <certificate />
  <authentication />
</clientCertificate>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e603a-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e603a-112">Attributes and Elements</span></span>  
 <span data-ttu-id="e603a-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e603a-113">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e603a-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="e603a-114">Attributes</span></span>  
 <span data-ttu-id="e603a-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e603a-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="e603a-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e603a-116">Child Elements</span></span>  
  
|<span data-ttu-id="e603a-117">Élément</span><span class="sxs-lookup"><span data-stu-id="e603a-117">Element</span></span>|<span data-ttu-id="e603a-118">Description</span><span class="sxs-lookup"><span data-stu-id="e603a-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e603a-119">\<authentication></span><span class="sxs-lookup"><span data-stu-id="e603a-119">\<authentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/authentication-of-clientcertificate-element.md)|<span data-ttu-id="e603a-120">Spécifie des options d'authentification pour le certificat client.</span><span class="sxs-lookup"><span data-stu-id="e603a-120">Specifies authentication options for the client certificate.</span></span>|  
|[<span data-ttu-id="e603a-121">\<certificate></span><span class="sxs-lookup"><span data-stu-id="e603a-121">\<certificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-of-clientcertificate-element.md)|<span data-ttu-id="e603a-122">Spécifie le certificat à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e603a-122">Specifies the certificate to use.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e603a-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e603a-123">Parent Elements</span></span>  
  
|<span data-ttu-id="e603a-124">Élément</span><span class="sxs-lookup"><span data-stu-id="e603a-124">Element</span></span>|<span data-ttu-id="e603a-125">Description</span><span class="sxs-lookup"><span data-stu-id="e603a-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e603a-126">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="e603a-126">\<serviceCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md)|<span data-ttu-id="e603a-127">Spécifie les informations d’identification à utiliser pour authentifier le service, ainsi que les paramètres liés à la validation des informations d’identification du client.</span><span class="sxs-lookup"><span data-stu-id="e603a-127">Specifies the credentials to be used in authenticating the service, and the client credential validation related settings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e603a-128">Notes</span><span class="sxs-lookup"><span data-stu-id="e603a-128">Remarks</span></span>  
 <span data-ttu-id="e603a-129">Cet élément est utilisé lorsque le service doit disposer du certificat du client à l'avance afin de communiquer de manière sécurisée avec le client.</span><span class="sxs-lookup"><span data-stu-id="e603a-129">This element is used when the service must have the client's certificate in advance to communicate securely with the client.</span></span> <span data-ttu-id="e603a-130">Cela se produit lors de l'utilisation du modèle de communication duplex.</span><span class="sxs-lookup"><span data-stu-id="e603a-130">This occurs when using the duplex communication pattern.</span></span> <span data-ttu-id="e603a-131">Dans le modèle demande-réponse classique, le client inclut son certificat dans la demande que le service utilise pour sécuriser à nouveau sa réponse au client.</span><span class="sxs-lookup"><span data-stu-id="e603a-131">In the more typical request/response pattern, the client includes its certificate in the request, which the service uses to encrypt and sign its response back to the client.</span></span> <span data-ttu-id="e603a-132">Dans le modèle de communication duplex, toutefois, le service ne dispose pas de demande du client et, par conséquent, requiert le certificat du client à l'avance pour sécuriser l'envoi du message au client.</span><span class="sxs-lookup"><span data-stu-id="e603a-132">In the duplex communication pattern, however, the service does not have a request from the client and therefore it needs the client's certificate in advance to secure the message to the client.</span></span> <span data-ttu-id="e603a-133">C'est pourquoi vous devez obtenir le certificat du client dans une négociation hors bande et l'indiquer à l'aide de cet élément.</span><span class="sxs-lookup"><span data-stu-id="e603a-133">Therefore you must obtain the client's certificate in an out-of-band negotiation, and specify the certificate using this element.</span></span> <span data-ttu-id="e603a-134">Pour plus d’informations sur les services duplex, consultez [Comment : Créer un contrat Duplex](../../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md).</span><span class="sxs-lookup"><span data-stu-id="e603a-134">For more information about duplex services, see [How to: Create a Duplex Contract](../../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md).</span></span>  
  
 <span data-ttu-id="e603a-135">Le certificat défini dans cet élément est utilisé pour chiffrer les messages au client uniquement pour les liaisons configurées avec le mode d’authentification de sécurité des messages `MutualCertificateDuplex`.</span><span class="sxs-lookup"><span data-stu-id="e603a-135">The certificate set in this element is used to encrypt messages to the client only for bindings that are configured with `MutualCertificateDuplex` message security authentication mode.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e603a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e603a-136">See also</span></span>

- <xref:System.ServiceModel.Configuration.X509InitiatorCertificateServiceElement>
- <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.ClientCertificate%2A>
- <xref:System.ServiceModel.Configuration.X509InitiatorCertificateServiceElement>
- <xref:System.ServiceModel.Description.ServiceCredentials.ClientCertificate%2A>
- <xref:System.ServiceModel.Security.X509CertificateInitiatorServiceCredential>
- [<span data-ttu-id="e603a-137">Guide pratique pour Créer un contrat Duplex</span><span class="sxs-lookup"><span data-stu-id="e603a-137">How to: Create a Duplex Contract</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md)
- [<span data-ttu-id="e603a-138">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="e603a-138">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="e603a-139">Utilisation des certificats</span><span class="sxs-lookup"><span data-stu-id="e603a-139">Working with Certificates</span></span>](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)
