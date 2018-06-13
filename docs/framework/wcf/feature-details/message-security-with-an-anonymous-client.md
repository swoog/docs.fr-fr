---
title: Sécurité de message avec un client anonyme
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: cad53e1a-b7c9-4064-bc87-508c3d1dce49
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: b8cab1762a8c8c672d557c7bcccc2f339cbaefe9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33495052"
---
# <a name="message-security-with-an-anonymous-client"></a><span data-ttu-id="656df-102">Sécurité de message avec un client anonyme</span><span class="sxs-lookup"><span data-stu-id="656df-102">Message Security with an Anonymous Client</span></span>
<span data-ttu-id="656df-103">Le scénario suivant montre un client et un service sécurisé par la sécurité de message Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="656df-103">The following scenario shows a client and service secured by Windows Communication Foundation (WCF) message security.</span></span> <span data-ttu-id="656df-104">L'un des objectifs de conception consiste à utiliser la sécurité de message plutôt que la sécurité de transport, afin qu'à l'avenir il puisse prendre en charge un modèle plus riche basé sur les revendications.</span><span class="sxs-lookup"><span data-stu-id="656df-104">A design goal is to use message security rather than transport security, so that in the future it can support a richer claims-based model.</span></span> <span data-ttu-id="656df-105">Pour plus d’informations sur l’utilisation des revendications riche pour l’autorisation, consultez [la gestion des revendications et autorisation avec le modèle d’identité](../../../../docs/framework/wcf/feature-details/managing-claims-and-authorization-with-the-identity-model.md).</span><span class="sxs-lookup"><span data-stu-id="656df-105">For more information about using rich claims for authorization, see [Managing Claims and Authorization with the Identity Model](../../../../docs/framework/wcf/feature-details/managing-claims-and-authorization-with-the-identity-model.md).</span></span>  
  
 <span data-ttu-id="656df-106">Pour un exemple d’application, consultez [Message Security Anonymous](../../../../docs/framework/wcf/samples/message-security-anonymous.md).</span><span class="sxs-lookup"><span data-stu-id="656df-106">For a sample application, see [Message Security Anonymous](../../../../docs/framework/wcf/samples/message-security-anonymous.md).</span></span>  
  
 <span data-ttu-id="656df-107">![Message de sécurité avec un client anonyme](../../../../docs/framework/wcf/feature-details/media/b361a565-831c-4c10-90d7-66d8eeece0a1.gif "b361a565-831c-4c10-90d7-66d8eeece0a1")</span><span class="sxs-lookup"><span data-stu-id="656df-107">![Message security with an anynymous client](../../../../docs/framework/wcf/feature-details/media/b361a565-831c-4c10-90d7-66d8eeece0a1.gif "b361a565-831c-4c10-90d7-66d8eeece0a1")</span></span>  
  
|<span data-ttu-id="656df-108">Caractéristique</span><span class="sxs-lookup"><span data-stu-id="656df-108">Characteristic</span></span>|<span data-ttu-id="656df-109">Description</span><span class="sxs-lookup"><span data-stu-id="656df-109">Description</span></span>|  
|--------------------|-----------------|  
|<span data-ttu-id="656df-110">Mode de sécurité</span><span class="sxs-lookup"><span data-stu-id="656df-110">Security Mode</span></span>|<span data-ttu-id="656df-111">Message</span><span class="sxs-lookup"><span data-stu-id="656df-111">Message</span></span>|  
|<span data-ttu-id="656df-112">Interopérabilité</span><span class="sxs-lookup"><span data-stu-id="656df-112">Interoperability</span></span>|<span data-ttu-id="656df-113">WCF uniquement</span><span class="sxs-lookup"><span data-stu-id="656df-113">WCF only</span></span>|  
|<span data-ttu-id="656df-114">Authentification (serveur)</span><span class="sxs-lookup"><span data-stu-id="656df-114">Authentication (Server)</span></span>|<span data-ttu-id="656df-115">La négociation initiale requiert l'authentification du serveur, mais pas l'authentification du client</span><span class="sxs-lookup"><span data-stu-id="656df-115">Initial negotiation requires server authentication, but not client authentication</span></span>|  
|<span data-ttu-id="656df-116">Authentification (client)</span><span class="sxs-lookup"><span data-stu-id="656df-116">Authentication (Client)</span></span>|<span data-ttu-id="656df-117">None</span><span class="sxs-lookup"><span data-stu-id="656df-117">None</span></span>|  
|<span data-ttu-id="656df-118">Intégrité</span><span class="sxs-lookup"><span data-stu-id="656df-118">Integrity</span></span>|<span data-ttu-id="656df-119">Oui, à l'aide du contexte de sécurité partagé</span><span class="sxs-lookup"><span data-stu-id="656df-119">Yes, using shared security context</span></span>|  
|<span data-ttu-id="656df-120">Confidentialité</span><span class="sxs-lookup"><span data-stu-id="656df-120">Confidentiality</span></span>|<span data-ttu-id="656df-121">Oui, à l'aide du contexte de sécurité partagé</span><span class="sxs-lookup"><span data-stu-id="656df-121">Yes, using shared security context</span></span>|  
|<span data-ttu-id="656df-122">Transport</span><span class="sxs-lookup"><span data-stu-id="656df-122">Transport</span></span>|<span data-ttu-id="656df-123">HTTP</span><span class="sxs-lookup"><span data-stu-id="656df-123">HTTP</span></span>|  
  
## <a name="service"></a><span data-ttu-id="656df-124">Service</span><span class="sxs-lookup"><span data-stu-id="656df-124">Service</span></span>  
 <span data-ttu-id="656df-125">La configuration et le code ci-dessous sont conçus pour s'exécuter indépendamment.</span><span class="sxs-lookup"><span data-stu-id="656df-125">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="656df-126">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="656df-126">Do one of the following:</span></span>  
  
-   <span data-ttu-id="656df-127">Créez un service autonome à l'aide du code sans configuration.</span><span class="sxs-lookup"><span data-stu-id="656df-127">Create a stand-alone service using the code with no configuration.</span></span>  
  
-   <span data-ttu-id="656df-128">Créez un service à l'aide de la configuration fournie, mais ne définissez pas de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="656df-128">Create a service using the supplied configuration, but do not define any endpoints.</span></span>  
  
### <a name="code"></a><span data-ttu-id="656df-129">Code</span><span class="sxs-lookup"><span data-stu-id="656df-129">Code</span></span>  
 <span data-ttu-id="656df-130">Le code suivant montre comment créer un point de terminaison de service qui utilise la sécurité de message.</span><span class="sxs-lookup"><span data-stu-id="656df-130">The following code shows how to create a service endpoint that uses message security.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#8](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#8)]
 [!code-vb[C_SecurityScenarios#8](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#8)]  
  
### <a name="configuration"></a><span data-ttu-id="656df-131">Configuration</span><span class="sxs-lookup"><span data-stu-id="656df-131">Configuration</span></span>  
 <span data-ttu-id="656df-132">La configuration ci-dessous peut être utilisée à la place du code.</span><span class="sxs-lookup"><span data-stu-id="656df-132">The following configuration can be used instead of the code.</span></span> <span data-ttu-id="656df-133">L'élément de comportement du service est utilisé pour spécifier un certificat servant à authentifier le service auprès du client.</span><span class="sxs-lookup"><span data-stu-id="656df-133">The service behavior element is used to specify a certificate that is used to authenticate the service to the client.</span></span> <span data-ttu-id="656df-134">L'élément de service doit spécifier le comportement à l'aide de l'attribut `behaviorConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="656df-134">The service element must specify the behavior using the `behaviorConfiguration` attribute.</span></span> <span data-ttu-id="656df-135">L'élément de liaison spécifie que le type d'informations d'identification du client est `None`, ce qui permet aux clients anonymes d'utiliser le service.</span><span class="sxs-lookup"><span data-stu-id="656df-135">The binding element specifies that the client credential type is `None`, allowing anonymous clients to use the service.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <behaviors>  
      <serviceBehaviors>  
        <behavior name="ServiceCredentialsBehavior">  
          <serviceCredentials>  
            <serviceCertificate findValue="contoso.com"   
                                storeLocation="LocalMachine"  
                                storeName="My" />  
          </serviceCredentials>  
        </behavior>  
      </serviceBehaviors>  
    </behaviors>  
    <services>  
      <service behaviorConfiguration="ServiceCredentialsBehavior"   
               name="ServiceModel.Calculator">  
        <endpoint address="http://localhost/Calculator"   
                  binding="wsHttpBinding"  
                  bindingConfiguration="WSHttpBinding_ICalculator"   
                  name="CalculatorService"  
                  contract="ServiceModel.ICalculator" />  
      </service>  
    </services>  
    <bindings>  
      <wsHttpBinding>  
        <binding name="WSHttpBinding_ICalculator" >  
          <security mode="Message">  
            <message clientCredentialType="None" />  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
    <client />  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="client"></a><span data-ttu-id="656df-136">Client</span><span class="sxs-lookup"><span data-stu-id="656df-136">Client</span></span>  
 <span data-ttu-id="656df-137">La configuration et le code ci-dessous sont conçus pour s'exécuter indépendamment.</span><span class="sxs-lookup"><span data-stu-id="656df-137">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="656df-138">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="656df-138">Do one of the following:</span></span>  
  
-   <span data-ttu-id="656df-139">Créez un client autonome à l'aide du code (et du code client).</span><span class="sxs-lookup"><span data-stu-id="656df-139">Create a stand-alone client using the code (and client code).</span></span>  
  
-   <span data-ttu-id="656df-140">Créez un client qui ne définit pas d'adresse de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="656df-140">Create a client that does not define any endpoint addresses.</span></span> <span data-ttu-id="656df-141">Au lieu de cela, utilisez le constructeur client qui accepte le nom de configuration comme argument.</span><span class="sxs-lookup"><span data-stu-id="656df-141">Instead, use the client constructor that takes the configuration name as an argument.</span></span> <span data-ttu-id="656df-142">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="656df-142">For example:</span></span>  
  
     [!code-csharp[C_SecurityScenarios#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#0)]
     [!code-vb[C_SecurityScenarios#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#0)]  
  
### <a name="code"></a><span data-ttu-id="656df-143">Code</span><span class="sxs-lookup"><span data-stu-id="656df-143">Code</span></span>  
 <span data-ttu-id="656df-144">Le code suivant crée une instance du client.</span><span class="sxs-lookup"><span data-stu-id="656df-144">The following code creates an instance of the client.</span></span> <span data-ttu-id="656df-145">La liaison utilise le mode de sécurité au niveau du message, et le type d'informations d'identification du client a la valeur Aucun.</span><span class="sxs-lookup"><span data-stu-id="656df-145">The binding uses message mode security, and the client credential type is set to none.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#15](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#15)]
 [!code-vb[C_SecurityScenarios#15](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#15)]  
  
### <a name="configuration"></a><span data-ttu-id="656df-146">Configuration</span><span class="sxs-lookup"><span data-stu-id="656df-146">Configuration</span></span>  
 <span data-ttu-id="656df-147">Le code ci-dessous configure le client.</span><span class="sxs-lookup"><span data-stu-id="656df-147">The following code configures the client.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <bindings>  
      <wsHttpBinding>  
        <binding name="WSHttpBinding_ICalculator" >  
          <security mode="Message">  
            <message clientCredentialType="None" />  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
    <client>  
      <endpoint address="http://machineName/Calculator"  
        binding="wsHttpBinding"  
        bindingConfiguration="WSHttpBinding_ICalculator"   
        contract="ICalculator"  
        name="WSHttpBinding_ICalculator">  
        <identity>  
          <dns value="contoso.com" />  
        </identity>  
      </endpoint>  
    </client>  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="656df-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="656df-148">See Also</span></span>  
 [<span data-ttu-id="656df-149">Vue d’ensemble de la sécurité</span><span class="sxs-lookup"><span data-stu-id="656df-149">Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/security-overview.md)  
 [<span data-ttu-id="656df-150">Sécurité des applications distribuées</span><span class="sxs-lookup"><span data-stu-id="656df-150">Distributed Application Security</span></span>](../../../../docs/framework/wcf/feature-details/distributed-application-security.md)  
 [<span data-ttu-id="656df-151">Sécurité de message anonyme</span><span class="sxs-lookup"><span data-stu-id="656df-151">Message Security Anonymous</span></span>](../../../../docs/framework/wcf/samples/message-security-anonymous.md)  
 [<span data-ttu-id="656df-152">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="656df-152">Service Identity and Authentication</span></span>](../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="656df-153">Modèle de sécurité pour Windows Server AppFabric</span><span class="sxs-lookup"><span data-stu-id="656df-153">Security Model for Windows Server App Fabric</span></span>](http://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
