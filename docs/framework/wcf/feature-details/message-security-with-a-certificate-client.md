---
title: Sécurité de message avec un client de certificat
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 99770573-c815-4428-a38c-e4335c8bd7ce
ms.openlocfilehash: f435136bb08876b759087b9cdd258f6ae7881be5
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50191114"
---
# <a name="message-security-with-a-certificate-client"></a><span data-ttu-id="a3e2b-102">Sécurité de message avec un client de certificat</span><span class="sxs-lookup"><span data-stu-id="a3e2b-102">Message Security with a Certificate Client</span></span>
<span data-ttu-id="a3e2b-103">Le scénario suivant montre un client Windows Communication Foundation (WCF) et un service sécurisé à l’aide du mode de sécurité de message.</span><span class="sxs-lookup"><span data-stu-id="a3e2b-103">The following scenario shows a Windows Communication Foundation (WCF) client and service secured using message security mode.</span></span> <span data-ttu-id="a3e2b-104">Le client et le service sont tous les deux authentifiés à l'aide de certificats.</span><span class="sxs-lookup"><span data-stu-id="a3e2b-104">Both the client and the service are authenticated with certificates.</span></span> <span data-ttu-id="a3e2b-105">Pour plus d’informations, consultez [sécurité des applications distribuées](../../../../docs/framework/wcf/feature-details/distributed-application-security.md).</span><span class="sxs-lookup"><span data-stu-id="a3e2b-105">For more information, see [Distributed Application Security](../../../../docs/framework/wcf/feature-details/distributed-application-security.md).</span></span>  
  
 <span data-ttu-id="a3e2b-106">Pour un exemple d’application, consultez [certificat de sécurité de Message](../../../../docs/framework/wcf/samples/message-security-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="a3e2b-106">For a sample application, see [Message Security Certificate](../../../../docs/framework/wcf/samples/message-security-certificate.md).</span></span>  
  
 <span data-ttu-id="a3e2b-107">![Client avec certificat](../../../../docs/framework/wcf/feature-details/media/clientwithcertificate.gif "ClientWithCertificate")</span><span class="sxs-lookup"><span data-stu-id="a3e2b-107">![Client with certificate](../../../../docs/framework/wcf/feature-details/media/clientwithcertificate.gif "ClientWithCertificate")</span></span>  
  
|<span data-ttu-id="a3e2b-108">Caractéristique</span><span class="sxs-lookup"><span data-stu-id="a3e2b-108">Characteristic</span></span>|<span data-ttu-id="a3e2b-109">Description</span><span class="sxs-lookup"><span data-stu-id="a3e2b-109">Description</span></span>|  
|--------------------|-----------------|  
|<span data-ttu-id="a3e2b-110">Mode de sécurité</span><span class="sxs-lookup"><span data-stu-id="a3e2b-110">Security Mode</span></span>|<span data-ttu-id="a3e2b-111">Message</span><span class="sxs-lookup"><span data-stu-id="a3e2b-111">Message</span></span>|  
|<span data-ttu-id="a3e2b-112">Interopérabilité</span><span class="sxs-lookup"><span data-stu-id="a3e2b-112">Interoperability</span></span>|<span data-ttu-id="a3e2b-113">WCF uniquement</span><span class="sxs-lookup"><span data-stu-id="a3e2b-113">WCF only</span></span>|  
|<span data-ttu-id="a3e2b-114">Authentification (serveur)</span><span class="sxs-lookup"><span data-stu-id="a3e2b-114">Authentication (Server)</span></span>|<span data-ttu-id="a3e2b-115">Utilisation de certificat de service</span><span class="sxs-lookup"><span data-stu-id="a3e2b-115">Using service certificate</span></span>|  
|<span data-ttu-id="a3e2b-116">Authentification (client)</span><span class="sxs-lookup"><span data-stu-id="a3e2b-116">Authentication (Client)</span></span>|<span data-ttu-id="a3e2b-117">Utilisation de certificat client</span><span class="sxs-lookup"><span data-stu-id="a3e2b-117">Using client certificate</span></span>|  
|<span data-ttu-id="a3e2b-118">Intégrité</span><span class="sxs-lookup"><span data-stu-id="a3e2b-118">Integrity</span></span>|<span data-ttu-id="a3e2b-119">Oui</span><span class="sxs-lookup"><span data-stu-id="a3e2b-119">Yes</span></span>|  
|<span data-ttu-id="a3e2b-120">Confidentialité</span><span class="sxs-lookup"><span data-stu-id="a3e2b-120">Confidentiality</span></span>|<span data-ttu-id="a3e2b-121">Oui</span><span class="sxs-lookup"><span data-stu-id="a3e2b-121">Yes</span></span>|  
|<span data-ttu-id="a3e2b-122">Transport</span><span class="sxs-lookup"><span data-stu-id="a3e2b-122">Transport</span></span>|<span data-ttu-id="a3e2b-123">HTTP</span><span class="sxs-lookup"><span data-stu-id="a3e2b-123">HTTP</span></span>|  
|<span data-ttu-id="a3e2b-124">Binding</span><span class="sxs-lookup"><span data-stu-id="a3e2b-124">Binding</span></span>|<xref:System.ServiceModel.WSHttpBinding>|  
  
## <a name="service"></a><span data-ttu-id="a3e2b-125">Service</span><span class="sxs-lookup"><span data-stu-id="a3e2b-125">Service</span></span>  
 <span data-ttu-id="a3e2b-126">La configuration et le code ci-dessous sont conçus pour s'exécuter indépendamment.</span><span class="sxs-lookup"><span data-stu-id="a3e2b-126">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="a3e2b-127">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3e2b-127">Do one of the following:</span></span>  
  
-   <span data-ttu-id="a3e2b-128">Créez un service autonome à l'aide du code sans configuration.</span><span class="sxs-lookup"><span data-stu-id="a3e2b-128">Create a stand-alone service using the code with no configuration.</span></span>  
  
-   <span data-ttu-id="a3e2b-129">Créez un service à l'aide de la configuration fournie, mais ne définissez pas de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a3e2b-129">Create a service using the supplied configuration, but do not define any endpoints.</span></span>  
  
### <a name="code"></a><span data-ttu-id="a3e2b-130">Code</span><span class="sxs-lookup"><span data-stu-id="a3e2b-130">Code</span></span>  
 <span data-ttu-id="a3e2b-131">Le code ci-dessous montre comment créer un point de terminaison de service qui utilise la sécurité de message pour établir un contexte sécurisé.</span><span class="sxs-lookup"><span data-stu-id="a3e2b-131">The following code shows how to create a service endpoint that uses message security to establish a secure context.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#10](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#10)]
 [!code-vb[C_SecurityScenarios#10](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#10)]  
  
### <a name="configuration"></a><span data-ttu-id="a3e2b-132">Configuration</span><span class="sxs-lookup"><span data-stu-id="a3e2b-132">Configuration</span></span>  
 <span data-ttu-id="a3e2b-133">La configuration ci-dessous peut être utilisée à la place du code.</span><span class="sxs-lookup"><span data-stu-id="a3e2b-133">The following configuration can be used instead of the code.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <behaviors>  
      <serviceBehaviors>  
        <behavior name="ServiceCredentialsBehavior">  
          <serviceCredentials>  
            <serviceCertificate findValue="Contoso.com"  
                                x509FindType="FindBySubjectName" />  
          </serviceCredentials>  
        </behavior>  
      </serviceBehaviors>  
    </behaviors>  
    <services>  
      <service behaviorConfiguration="ServiceCredentialsBehavior"   
               name="ServiceModel.Calculator">  
        <endpoint address="http://localhost/Calculator"   
                  binding="wsHttpBinding"  
                  bindingConfiguration="MessageAndCerficiateClient"   
                  name="SecuredByClientCertificate"  
                  contract="ServiceModel.ICalculator" />  
      </service>  
    </services>  
    <bindings>  
      <wsHttpBinding>  
        <binding name="WSHttpBinding_ICalculator">  
          <security mode="Message">  
            <message clientCredentialType="Certificate" />  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
    <client />  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="client"></a><span data-ttu-id="a3e2b-134">Client</span><span class="sxs-lookup"><span data-stu-id="a3e2b-134">Client</span></span>  
 <span data-ttu-id="a3e2b-135">La configuration et le code ci-dessous sont conçus pour s'exécuter indépendamment.</span><span class="sxs-lookup"><span data-stu-id="a3e2b-135">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="a3e2b-136">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3e2b-136">Do one of the following:</span></span>  
  
-   <span data-ttu-id="a3e2b-137">Créez un client autonome à l'aide du code (et du code client).</span><span class="sxs-lookup"><span data-stu-id="a3e2b-137">Create a stand-alone client using the code (and client code).</span></span>  
  
-   <span data-ttu-id="a3e2b-138">Créez un client qui ne définit pas d'adresse de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a3e2b-138">Create a client that does not define any endpoint addresses.</span></span> <span data-ttu-id="a3e2b-139">Au lieu de cela, utilisez le constructeur client qui accepte le nom de configuration comme argument.</span><span class="sxs-lookup"><span data-stu-id="a3e2b-139">Instead, use the client constructor that takes the configuration name as an argument.</span></span> <span data-ttu-id="a3e2b-140">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3e2b-140">For example:</span></span>  
  
     [!code-csharp[C_SecurityScenarios#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#0)]
     [!code-vb[C_SecurityScenarios#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#0)]  
  
### <a name="code"></a><span data-ttu-id="a3e2b-141">Code</span><span class="sxs-lookup"><span data-stu-id="a3e2b-141">Code</span></span>  
 <span data-ttu-id="a3e2b-142">Le code ci-dessous crée le client.</span><span class="sxs-lookup"><span data-stu-id="a3e2b-142">The following code creates the client.</span></span> <span data-ttu-id="a3e2b-143">La liaison s’effectue avec la sécurité en mode de message et le type d’informations d’identification client a la valeur `Certificate`.</span><span class="sxs-lookup"><span data-stu-id="a3e2b-143">The binding is to message mode security, and the client credential type is set to `Certificate`.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#17](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#17)]
 [!code-vb[C_SecurityScenarios#17](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#17)]  
  
### <a name="configuration"></a><span data-ttu-id="a3e2b-144">Configuration</span><span class="sxs-lookup"><span data-stu-id="a3e2b-144">Configuration</span></span>  
 <span data-ttu-id="a3e2b-145">La configuration ci-dessous spécifie le certificat client à l'aide d'un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a3e2b-145">The following configuration specifies the client certificate using an endpoint behavior.</span></span> <span data-ttu-id="a3e2b-146">Pour plus d’informations sur les certificats, consultez [Utilisation de certificats](../../../../docs/framework/wcf/feature-details/working-with-certificates.md).</span><span class="sxs-lookup"><span data-stu-id="a3e2b-146">For more information about certificates, see [Working with Certificates](../../../../docs/framework/wcf/feature-details/working-with-certificates.md).</span></span> <span data-ttu-id="a3e2b-147">Le code utilise également un <`identity`> élément pour spécifier un système DNS (Domain Name) de l’identité de serveur attendue.</span><span class="sxs-lookup"><span data-stu-id="a3e2b-147">The code also uses an <`identity`> element to specify a Domain Name System (DNS) of the expected server identity.</span></span> <span data-ttu-id="a3e2b-148">Pour plus d’informations sur l’identité, consultez [identité de Service et d’authentification](../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="a3e2b-148">For more information about identity, see [Service Identity and Authentication](../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <behaviors>  
      <endpointBehaviors>  
        <behavior name="endpointCredentialsBehavior">  
          <clientCredentials>  
            <clientCertificate findValue="Cohowinery.com"   
               storeLocation="LocalMachine"  
              x509FindType="FindBySubjectName" />  
          </clientCredentials>  
        </behavior>  
      </endpointBehaviors>  
    </behaviors>  
    <bindings>  
      <wsHttpBinding>  
        <binding name="WSHttpBinding_ICalculator" >  
          <security mode="Message">  
            <message clientCredentialType="Certificate" />  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
    <client>  
      <endpoint address="http://machineName/Calculator"   
                behaviorConfiguration="endpointCredentialsBehavior"  
                binding="wsHttpBinding"  
                bindingConfiguration="WSHttpBinding_ICalculator"  
                contract="ICalculator"  
                name="WSHttpBinding_ICalculator">  
        <identity>  
          <dns value="Contoso.com" />  
        </identity>  
      </endpoint>  
    </client>  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="a3e2b-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3e2b-149">See Also</span></span>  
 [<span data-ttu-id="a3e2b-150">Vue d’ensemble de la sécurité</span><span class="sxs-lookup"><span data-stu-id="a3e2b-150">Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/security-overview.md)  
 [<span data-ttu-id="a3e2b-151">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="a3e2b-151">Service Identity and Authentication</span></span>](../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="a3e2b-152">Utilisation des certificats</span><span class="sxs-lookup"><span data-stu-id="a3e2b-152">Working with Certificates</span></span>](../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 [<span data-ttu-id="a3e2b-153">Modèle de sécurité pour Windows Server AppFabric</span><span class="sxs-lookup"><span data-stu-id="a3e2b-153">Security Model for Windows Server App Fabric</span></span>](https://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
