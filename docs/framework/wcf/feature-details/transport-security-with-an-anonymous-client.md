---
title: Sécurité des transports avec un client anonyme
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: 056653a5-384e-4a02-ae3c-1b0157d2ccb4
caps.latest.revision: 14
author: BrucePerlerMS
ms.author: bruceper
manager: mbaldwin
ms.workload:
- dotnet
ms.openlocfilehash: 2b52a32db1f1ac02f9204198a4cda5d4cb157486
ms.sourcegitcommit: 94d33cadc5ff81d2ac389bf5f26422c227832052
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2018
---
# <a name="transport-security-with-an-anonymous-client"></a><span data-ttu-id="0670e-102">Sécurité des transports avec un client anonyme</span><span class="sxs-lookup"><span data-stu-id="0670e-102">Transport Security with an Anonymous Client</span></span>
<span data-ttu-id="0670e-103">Dans cette situation, [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] utilise la sécurité de transport (HTTPS) pour garantir l'intégrité et la confidentialité des données.</span><span class="sxs-lookup"><span data-stu-id="0670e-103">This [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] scenario uses transport security (HTTPS) to ensure confidentiality and integrity.</span></span> <span data-ttu-id="0670e-104">Le serveur doit être authentifié à l'aide d'un certificat SSL (Secure Sockets Layer). Les clients doivent ensuite faire confiance à ce certificat.</span><span class="sxs-lookup"><span data-stu-id="0670e-104">The server must be authenticated with a Secure Sockets Layer (SSL) certificate, and the clients must trust the server's certificate.</span></span> <span data-ttu-id="0670e-105">Aucun mécanisme n'authentifie les clients, ceux-ci restent donc anonymes.</span><span class="sxs-lookup"><span data-stu-id="0670e-105">The client is not authenticated by any mechanism and is, therefore, anonymous.</span></span>  
  
 <span data-ttu-id="0670e-106">Pour un exemple d’application, consultez [sécurité du Transport WS](../../../../docs/framework/wcf/samples/ws-transport-security.md).</span><span class="sxs-lookup"><span data-stu-id="0670e-106">For a sample application, see [WS Transport Security](../../../../docs/framework/wcf/samples/ws-transport-security.md).</span></span> <span data-ttu-id="0670e-107">Pour plus d’informations sur la sécurité de transport, consultez [vue d’ensemble de sécurité de Transport](../../../../docs/framework/wcf/feature-details/transport-security-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0670e-107">For more information about transport security, see [Transport Security Overview](../../../../docs/framework/wcf/feature-details/transport-security-overview.md).</span></span>  
  
 <span data-ttu-id="0670e-108">Pour plus d’informations sur l’utilisation d’un certificat avec un service, consultez [utilisation des certificats](../../../../docs/framework/wcf/feature-details/working-with-certificates.md) et [Comment : configurer un Port avec un certificat SSL](../../../../docs/framework/wcf/feature-details/how-to-configure-a-port-with-an-ssl-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="0670e-108">For more information about using a certificate with a service, see [Working with Certificates](../../../../docs/framework/wcf/feature-details/working-with-certificates.md) and [How to: Configure a Port with an SSL Certificate](../../../../docs/framework/wcf/feature-details/how-to-configure-a-port-with-an-ssl-certificate.md).</span></span>  
  
 <span data-ttu-id="0670e-109">![À l’aide de la sécurité de transport avec un client anonyme](../../../../docs/framework/wcf/feature-details/media/8fa2e931-0cfb-4aaa-9272-91d652b85d8d.gif "8fa2e931-0cfb-4aaa-9272-91d652b85d8d")</span><span class="sxs-lookup"><span data-stu-id="0670e-109">![Using transport security with an anonymous client](../../../../docs/framework/wcf/feature-details/media/8fa2e931-0cfb-4aaa-9272-91d652b85d8d.gif "8fa2e931-0cfb-4aaa-9272-91d652b85d8d")</span></span>  
  
|<span data-ttu-id="0670e-110">Caractéristique</span><span class="sxs-lookup"><span data-stu-id="0670e-110">Characteristic</span></span>|<span data-ttu-id="0670e-111">Description</span><span class="sxs-lookup"><span data-stu-id="0670e-111">Description</span></span>|  
|--------------------|-----------------|  
|<span data-ttu-id="0670e-112">Mode de sécurité</span><span class="sxs-lookup"><span data-stu-id="0670e-112">Security Mode</span></span>|<span data-ttu-id="0670e-113">Transport</span><span class="sxs-lookup"><span data-stu-id="0670e-113">Transport</span></span>|  
|<span data-ttu-id="0670e-114">Interopérabilité</span><span class="sxs-lookup"><span data-stu-id="0670e-114">Interoperability</span></span>|<span data-ttu-id="0670e-115">Avec les services Web et les clients existants</span><span class="sxs-lookup"><span data-stu-id="0670e-115">With existing Web services and clients</span></span>|  
|<span data-ttu-id="0670e-116">Authentification (serveur)</span><span class="sxs-lookup"><span data-stu-id="0670e-116">Authentication (Server)</span></span><br /><br /> <span data-ttu-id="0670e-117">Authentification (client)</span><span class="sxs-lookup"><span data-stu-id="0670e-117">Authentication (Client)</span></span>|<span data-ttu-id="0670e-118">Oui</span><span class="sxs-lookup"><span data-stu-id="0670e-118">Yes</span></span><br /><br /> <span data-ttu-id="0670e-119">Niveau application (pas de prise en charge [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)])</span><span class="sxs-lookup"><span data-stu-id="0670e-119">Application level (no [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] support)</span></span>|  
|<span data-ttu-id="0670e-120">Intégrité</span><span class="sxs-lookup"><span data-stu-id="0670e-120">Integrity</span></span>|<span data-ttu-id="0670e-121">Oui</span><span class="sxs-lookup"><span data-stu-id="0670e-121">Yes</span></span>|  
|<span data-ttu-id="0670e-122">Confidentialité</span><span class="sxs-lookup"><span data-stu-id="0670e-122">Confidentiality</span></span>|<span data-ttu-id="0670e-123">Oui</span><span class="sxs-lookup"><span data-stu-id="0670e-123">Yes</span></span>|  
|<span data-ttu-id="0670e-124">Transport</span><span class="sxs-lookup"><span data-stu-id="0670e-124">Transport</span></span>|<span data-ttu-id="0670e-125">HTTPS</span><span class="sxs-lookup"><span data-stu-id="0670e-125">HTTPS</span></span>|  
|<span data-ttu-id="0670e-126">Liaison</span><span class="sxs-lookup"><span data-stu-id="0670e-126">Binding</span></span>|<span data-ttu-id="0670e-127"><<!--zz xref:System.ServiceModel.WsHttpBinding --> `xref:System.ServiceModel.WsHttpBinding`></span><span class="sxs-lookup"><span data-stu-id="0670e-127"><<!--zz xref:System.ServiceModel.WsHttpBinding --> `xref:System.ServiceModel.WsHttpBinding`></span></span>|  
  
## <a name="service"></a><span data-ttu-id="0670e-128">Service</span><span class="sxs-lookup"><span data-stu-id="0670e-128">Service</span></span>  
 <span data-ttu-id="0670e-129">La configuration et le code ci-dessous sont conçus pour s'exécuter indépendamment.</span><span class="sxs-lookup"><span data-stu-id="0670e-129">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="0670e-130">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0670e-130">Do one of the following:</span></span>  
  
-   <span data-ttu-id="0670e-131">Créez un service autonome à l'aide du code sans configuration.</span><span class="sxs-lookup"><span data-stu-id="0670e-131">Create a stand-alone service using the code with no configuration.</span></span>  
  
-   <span data-ttu-id="0670e-132">Créez un service à l'aide de la configuration fournie, mais ne définissez pas de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0670e-132">Create a service using the supplied configuration, but do not define any endpoints.</span></span>  
  
### <a name="code"></a><span data-ttu-id="0670e-133">Code</span><span class="sxs-lookup"><span data-stu-id="0670e-133">Code</span></span>  
 <span data-ttu-id="0670e-134">Le code suivant illustre comment créer un point de terminaison à l'aide de la sécurité de transport :</span><span class="sxs-lookup"><span data-stu-id="0670e-134">The following code shows how to create an endpoint using transport security:</span></span>  
  
 [!code-csharp[c_SecurityScenarios#5](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#5)]
 [!code-vb[c_SecurityScenarios#5](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#5)]  
  
### <a name="configuration"></a><span data-ttu-id="0670e-135">Configuration</span><span class="sxs-lookup"><span data-stu-id="0670e-135">Configuration</span></span>  
 <span data-ttu-id="0670e-136">Le code ci-dessous configure le même point de terminaison en utilisant la configuration.</span><span class="sxs-lookup"><span data-stu-id="0670e-136">The following code sets up the same endpoint using configuration.</span></span> <span data-ttu-id="0670e-137">Aucun mécanisme n'authentifie les clients, ceux-ci restent donc anonymes.</span><span class="sxs-lookup"><span data-stu-id="0670e-137">The client is not authenticated by any mechanism, and is therefore anonymous.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <services>  
      <service name="ServiceModel.Calculator">  
        <endpoint address="http://localhost/Calculator"   
                  binding="wsHttpBinding"  
                  bindingConfiguration="WSHttpBinding_ICalculator"   
                  name="SecuredByTransportEndpoint"  
                  contract="ServiceModel.ICalculator" />  
      </service>  
    </services>  
    <bindings>  
      <wsHttpBinding>  
        <binding name="WSHttpBinding_ICalculator">  
          <security mode="Transport">  
            <transport clientCredentialType="None" />  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
    <client />  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="client"></a><span data-ttu-id="0670e-138">Client</span><span class="sxs-lookup"><span data-stu-id="0670e-138">Client</span></span>  
 <span data-ttu-id="0670e-139">La configuration et le code ci-dessous sont conçus pour s'exécuter indépendamment.</span><span class="sxs-lookup"><span data-stu-id="0670e-139">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="0670e-140">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0670e-140">Do one of the following:</span></span>  
  
-   <span data-ttu-id="0670e-141">Créez un client autonome à l'aide du code (et du code client).</span><span class="sxs-lookup"><span data-stu-id="0670e-141">Create a stand-alone client using the code (and client code).</span></span>  
  
-   <span data-ttu-id="0670e-142">Créez un client qui ne définit pas d'adresse de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0670e-142">Create a client that does not define any endpoint addresses.</span></span> <span data-ttu-id="0670e-143">Au lieu de cela, utilisez le constructeur client qui accepte le nom de configuration comme argument.</span><span class="sxs-lookup"><span data-stu-id="0670e-143">Instead, use the client constructor that takes the configuration name as an argument.</span></span> <span data-ttu-id="0670e-144">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="0670e-144">For example:</span></span>  
  
     [!code-csharp[C_SecurityScenarios#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#0)]
     [!code-vb[C_SecurityScenarios#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#0)]  
  
### <a name="code"></a><span data-ttu-id="0670e-145">Code</span><span class="sxs-lookup"><span data-stu-id="0670e-145">Code</span></span>  
 [!code-csharp[c_SecurityScenarios#6](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#6)]
 [!code-vb[c_SecurityScenarios#6](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#6)]  
  
### <a name="configuration"></a><span data-ttu-id="0670e-146">Configuration</span><span class="sxs-lookup"><span data-stu-id="0670e-146">Configuration</span></span>  
 <span data-ttu-id="0670e-147">La configuration suivante peut être utilisée à la place du code pour paramétrer le service :</span><span class="sxs-lookup"><span data-stu-id="0670e-147">The following configuration can be used instead of the code to set up the service.</span></span>  
  
```xml  
<configuration>  
  <system.serviceModel>  
    <bindings>  
      <wsHttpBinding>  
        <binding name="WSHttpBinding_ICalculator" >  
          <security mode="Transport">  
            <transport clientCredentialType="None" />  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
    <client>  
      <endpoint address="https://machineName/Calculator"   
                binding="wsHttpBinding"  
                bindingConfiguration="WSHttpBinding_ICalculator"   
                contract="ICalculator"  
                name="WSHttpBinding_ICalculator" />  
    </client>  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="0670e-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0670e-148">See Also</span></span>  
 [<span data-ttu-id="0670e-149">Vue d’ensemble de la sécurité</span><span class="sxs-lookup"><span data-stu-id="0670e-149">Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/security-overview.md)  
 [<span data-ttu-id="0670e-150">Sécurité de transport WS</span><span class="sxs-lookup"><span data-stu-id="0670e-150">WS Transport Security</span></span>](../../../../docs/framework/wcf/samples/ws-transport-security.md)  
 [<span data-ttu-id="0670e-151">Vue d’ensemble de la sécurité de transport</span><span class="sxs-lookup"><span data-stu-id="0670e-151">Transport Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/transport-security-overview.md)  
 [<span data-ttu-id="0670e-152">Modèle de sécurité pour Windows Server AppFabric</span><span class="sxs-lookup"><span data-stu-id="0670e-152">Security Model for Windows Server App Fabric</span></span>](http://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
