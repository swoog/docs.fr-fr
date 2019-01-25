---
title: Sécurité de message avec un client de type Nom d'utilisateur
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 36335cb9-76b8-4443-92c7-44f081eabb21
ms.openlocfilehash: 872283f55ae6f085b2cdf5c64c229b9d459b71f8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54701272"
---
# <a name="message-security-with-a-user-name-client"></a><span data-ttu-id="db3ac-102">Sécurité de message avec un client de type Nom d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="db3ac-102">Message Security with a User Name Client</span></span>
<span data-ttu-id="db3ac-103">L’illustration suivante montre un service Windows Communication Foundation (WCF) et le client sécurisé à l’aide de la sécurité au niveau du message.</span><span class="sxs-lookup"><span data-stu-id="db3ac-103">The following illustration shows an Windows Communication Foundation (WCF) service and client secured using message-level security.</span></span> <span data-ttu-id="db3ac-104">Le service est authentifié à l'aide d'un certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="db3ac-104">The service is authenticated with an X.509 certificate.</span></span> <span data-ttu-id="db3ac-105">Le client s'authentifie à l'aide d'un nom d'utilisateur et d'un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="db3ac-105">The client authenticates using a user name and password.</span></span>  
  
 <span data-ttu-id="db3ac-106">Pour un exemple d’application, consultez [nom d’utilisateur de sécurité de Message](../../../../docs/framework/wcf/samples/message-security-user-name.md).</span><span class="sxs-lookup"><span data-stu-id="db3ac-106">For a sample application, see [Message Security User Name](../../../../docs/framework/wcf/samples/message-security-user-name.md).</span></span>  
  
 <span data-ttu-id="db3ac-107">![Sécurité des messages à l’aide de l’authentification du nom d’utilisateur](../../../../docs/framework/wcf/feature-details/media/1fb10a61-7e1d-42f5-b1af-195bfee5b3c6.gif "1fb10a61-7e1d-42f5-b1af-195bfee5b3c6")</span><span class="sxs-lookup"><span data-stu-id="db3ac-107">![Message security using username authentication](../../../../docs/framework/wcf/feature-details/media/1fb10a61-7e1d-42f5-b1af-195bfee5b3c6.gif "1fb10a61-7e1d-42f5-b1af-195bfee5b3c6")</span></span>  
  
|<span data-ttu-id="db3ac-108">Caractéristique</span><span class="sxs-lookup"><span data-stu-id="db3ac-108">Characteristic</span></span>|<span data-ttu-id="db3ac-109">Description</span><span class="sxs-lookup"><span data-stu-id="db3ac-109">Description</span></span>|  
|--------------------|-----------------|  
|<span data-ttu-id="db3ac-110">Mode de sécurité</span><span class="sxs-lookup"><span data-stu-id="db3ac-110">Security Mode</span></span>|<span data-ttu-id="db3ac-111">Message</span><span class="sxs-lookup"><span data-stu-id="db3ac-111">Message</span></span>|  
|<span data-ttu-id="db3ac-112">Interopérabilité</span><span class="sxs-lookup"><span data-stu-id="db3ac-112">Interoperability</span></span>|<span data-ttu-id="db3ac-113">Windows Communication Foundation (WCF) uniquement</span><span class="sxs-lookup"><span data-stu-id="db3ac-113">Windows Communication Foundation (WCF) only</span></span>|  
|<span data-ttu-id="db3ac-114">Authentification (serveur)</span><span class="sxs-lookup"><span data-stu-id="db3ac-114">Authentication (Server)</span></span>|<span data-ttu-id="db3ac-115">La négociation initiale requiert l'authentification du serveur</span><span class="sxs-lookup"><span data-stu-id="db3ac-115">Initial negotiation requires server authentication</span></span>|  
|<span data-ttu-id="db3ac-116">Authentification (client)</span><span class="sxs-lookup"><span data-stu-id="db3ac-116">Authentication (Client)</span></span>|<span data-ttu-id="db3ac-117">Nom d'utilisateur/mot de passe</span><span class="sxs-lookup"><span data-stu-id="db3ac-117">User name/password</span></span>|  
|<span data-ttu-id="db3ac-118">Intégrité</span><span class="sxs-lookup"><span data-stu-id="db3ac-118">Integrity</span></span>|<span data-ttu-id="db3ac-119">Oui, à l'aide du contexte de sécurité partagé</span><span class="sxs-lookup"><span data-stu-id="db3ac-119">Yes, using shared security context</span></span>|  
|<span data-ttu-id="db3ac-120">Confidentialité</span><span class="sxs-lookup"><span data-stu-id="db3ac-120">Confidentiality</span></span>|<span data-ttu-id="db3ac-121">Oui, à l'aide du contexte de sécurité partagé</span><span class="sxs-lookup"><span data-stu-id="db3ac-121">Yes, using shared security context</span></span>|  
|<span data-ttu-id="db3ac-122">Transport</span><span class="sxs-lookup"><span data-stu-id="db3ac-122">Transport</span></span>|<span data-ttu-id="db3ac-123">HTTP</span><span class="sxs-lookup"><span data-stu-id="db3ac-123">HTTP</span></span>|  
|<span data-ttu-id="db3ac-124">Binding</span><span class="sxs-lookup"><span data-stu-id="db3ac-124">Binding</span></span>|<xref:System.ServiceModel.WSHttpBinding>|  
  
## <a name="service"></a><span data-ttu-id="db3ac-125">Service</span><span class="sxs-lookup"><span data-stu-id="db3ac-125">Service</span></span>  
 <span data-ttu-id="db3ac-126">La configuration et le code ci-dessous sont conçus pour s'exécuter indépendamment.</span><span class="sxs-lookup"><span data-stu-id="db3ac-126">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="db3ac-127">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="db3ac-127">Do one of the following:</span></span>  
  
-   <span data-ttu-id="db3ac-128">Créez un service autonome à l'aide du code sans configuration.</span><span class="sxs-lookup"><span data-stu-id="db3ac-128">Create a stand-alone service using the code with no configuration.</span></span>  
  
-   <span data-ttu-id="db3ac-129">Créez un service à l'aide de la configuration fournie, mais ne définissez pas de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="db3ac-129">Create a service using the supplied configuration, but do not define any endpoints.</span></span>  
  
### <a name="code"></a><span data-ttu-id="db3ac-130">Code</span><span class="sxs-lookup"><span data-stu-id="db3ac-130">Code</span></span>  
 <span data-ttu-id="db3ac-131">Le code suivant montre comment créer un point de terminaison de service qui utilise la sécurité de message.</span><span class="sxs-lookup"><span data-stu-id="db3ac-131">The following code shows how to create a service endpoint that uses message security.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#9](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#9)]
 [!code-vb[C_SecurityScenarios#9](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#9)]  
  
### <a name="configuration"></a><span data-ttu-id="db3ac-132">Configuration</span><span class="sxs-lookup"><span data-stu-id="db3ac-132">Configuration</span></span>  
 <span data-ttu-id="db3ac-133">La configuration suivante peut être utilisée à la place du code :</span><span class="sxs-lookup"><span data-stu-id="db3ac-133">The following configuration can be used instead of the code:</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <behaviors>  
      <serviceBehaviors>  
        <behavior name="ServiceCredentialsBehavior">  
          <serviceCredentials>  
            <serviceCertificate findValue="Contoso.com"   
                                storeLocation="LocalMachine"  
                                storeName="My"     
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
                  bindingConfiguration="MessageAndUserName"  
                  name="SecuredByTransportEndpoint"  
                  contract="ServiceModel.ICalculator" />  
      </service>  
    </services>  
    <bindings>  
      <wsHttpBinding>  
        <binding name="MessageAndUserName">  
          <security mode="Message">              
            <message clientCredentialType="UserName" />  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
    <client />  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="client"></a><span data-ttu-id="db3ac-134">Client</span><span class="sxs-lookup"><span data-stu-id="db3ac-134">Client</span></span>  
  
### <a name="code"></a><span data-ttu-id="db3ac-135">Code</span><span class="sxs-lookup"><span data-stu-id="db3ac-135">Code</span></span>  
 <span data-ttu-id="db3ac-136">Le code ci-dessous crée le client.</span><span class="sxs-lookup"><span data-stu-id="db3ac-136">The following code creates the client.</span></span> <span data-ttu-id="db3ac-137">La liaison s’effectue avec la sécurité en mode de message et le type d’informations d’identification client a la valeur `UserName`.</span><span class="sxs-lookup"><span data-stu-id="db3ac-137">The binding is to message mode security, and the client credential type is set to `UserName`.</span></span> <span data-ttu-id="db3ac-138">Le nom d'utilisateur et le mot de passe peuvent uniquement être spécifiés à l'aide du code (cela n'est pas configurable).</span><span class="sxs-lookup"><span data-stu-id="db3ac-138">The user name and password can only be specified using code (it is not configurable).</span></span> <span data-ttu-id="db3ac-139">Le code permettant de retourner le nom d'utilisateur et le mot de passe n'est pas indiqué dans ce cas car il doit être exécuté au niveau de l'application.</span><span class="sxs-lookup"><span data-stu-id="db3ac-139">The code to return the user name and password is not shown here because it must be done at the application level.</span></span> <span data-ttu-id="db3ac-140">Par exemple, utilisez une boîte de dialogue Windows Forms pour demander les données à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db3ac-140">For example, use a Windows Forms dialog box to query the user for the data.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#16](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#16)]
 [!code-vb[C_SecurityScenarios#16](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#16)]  
  
### <a name="configuration"></a><span data-ttu-id="db3ac-141">Configuration</span><span class="sxs-lookup"><span data-stu-id="db3ac-141">Configuration</span></span>  
 <span data-ttu-id="db3ac-142">Le code ci-dessous configure le client.</span><span class="sxs-lookup"><span data-stu-id="db3ac-142">The following code configures the client.</span></span> <span data-ttu-id="db3ac-143">La liaison s’effectue avec la sécurité en mode de message et le type d’informations d’identification client a la valeur `UserName`.</span><span class="sxs-lookup"><span data-stu-id="db3ac-143">The binding is to message mode security, and the client credential type is set to `UserName`.</span></span> <span data-ttu-id="db3ac-144">Le nom d'utilisateur et le mot de passe peuvent uniquement être spécifiés à l'aide du code (cela n'est pas configurable).</span><span class="sxs-lookup"><span data-stu-id="db3ac-144">The user name and password can only be specified using code (it is not configurable).</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <bindings>  
      <wsHttpBinding>  
        <binding name="WSHttpBinding_ICalculator" >  
          <security mode="Message">  
            <message clientCredentialType="UserName" />  
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
          <dns value ="Contoso.com" />  
        </identity>  
      </endpoint>  
    </client>  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="db3ac-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db3ac-145">See also</span></span>
- [<span data-ttu-id="db3ac-146">Vue d’ensemble de la sécurité</span><span class="sxs-lookup"><span data-stu-id="db3ac-146">Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/security-overview.md)
- [<span data-ttu-id="db3ac-147">Nom d’utilisateur de sécurité de message</span><span class="sxs-lookup"><span data-stu-id="db3ac-147">Message Security User Name</span></span>](../../../../docs/framework/wcf/samples/message-security-user-name.md)
- [<span data-ttu-id="db3ac-148">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="db3ac-148">Service Identity and Authentication</span></span>](../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="db3ac-149">\<identity></span><span class="sxs-lookup"><span data-stu-id="db3ac-149">\<identity></span></span>](../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)
- [<span data-ttu-id="db3ac-150">Modèle de sécurité pour Windows Server AppFabric</span><span class="sxs-lookup"><span data-stu-id="db3ac-150">Security Model for Windows Server App Fabric</span></span>](https://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
