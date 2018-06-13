---
title: Sécurité de transport avec l'authentification Windows
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 96dd26e2-46e7-4de0-9a29-4fcb05bf187b
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: d291cd3d00f8d0d40e0b8543d5347e1509cb8b90
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33498600"
---
# <a name="transport-security-with-windows-authentication"></a><span data-ttu-id="c9e3c-102">Sécurité de transport avec l'authentification Windows</span><span class="sxs-lookup"><span data-stu-id="c9e3c-102">Transport Security with Windows Authentication</span></span>
<span data-ttu-id="c9e3c-103">Le scénario suivant montre un client de Windows Communication Foundation (WCF) et d’un service sécurisé par la sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-103">The following scenario shows a Windows Communication Foundation (WCF) client and service secured by Windows security.</span></span> <span data-ttu-id="c9e3c-104">Pour plus d’informations sur la programmation, consultez [Comment : sécuriser un Service avec les informations d’identification Windows](../../../../docs/framework/wcf/how-to-secure-a-service-with-windows-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="c9e3c-104">For more information about programming, see [How to: Secure a Service with Windows Credentials](../../../../docs/framework/wcf/how-to-secure-a-service-with-windows-credentials.md).</span></span>  
  
 <span data-ttu-id="c9e3c-105">Un service Web d'intranet affiche des informations de ressources humaines.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-105">An intranet Web service displays human resources information.</span></span> <span data-ttu-id="c9e3c-106">Le client est une application Windows Form.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-106">The client is a Windows Form application.</span></span> <span data-ttu-id="c9e3c-107">L'application est déployée dans un domaine sécurisé par un contrôleur Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-107">The application is deployed in a domain with a Kerberos controller securing the domain.</span></span>  
  
 <span data-ttu-id="c9e3c-108">![Sécurité de transport avec l’authentification Windows](../../../../docs/framework/wcf/feature-details/media/securedbywindows.gif "SecuredByWindows")</span><span class="sxs-lookup"><span data-stu-id="c9e3c-108">![Transport security with Windows authentication](../../../../docs/framework/wcf/feature-details/media/securedbywindows.gif "SecuredByWindows")</span></span>  
  
|<span data-ttu-id="c9e3c-109">Caractéristique</span><span class="sxs-lookup"><span data-stu-id="c9e3c-109">Characteristic</span></span>|<span data-ttu-id="c9e3c-110">Description</span><span class="sxs-lookup"><span data-stu-id="c9e3c-110">Description</span></span>|  
|--------------------|-----------------|  
|<span data-ttu-id="c9e3c-111">Mode de sécurité</span><span class="sxs-lookup"><span data-stu-id="c9e3c-111">Security Mode</span></span>|<span data-ttu-id="c9e3c-112">Transport</span><span class="sxs-lookup"><span data-stu-id="c9e3c-112">Transport</span></span>|  
|<span data-ttu-id="c9e3c-113">Interopérabilité</span><span class="sxs-lookup"><span data-stu-id="c9e3c-113">Interoperability</span></span>|<span data-ttu-id="c9e3c-114">WCF uniquement</span><span class="sxs-lookup"><span data-stu-id="c9e3c-114">WCF only</span></span>|  
|<span data-ttu-id="c9e3c-115">Authentification (serveur)</span><span class="sxs-lookup"><span data-stu-id="c9e3c-115">Authentication (Server)</span></span><br /><br /> <span data-ttu-id="c9e3c-116">Authentification (client)</span><span class="sxs-lookup"><span data-stu-id="c9e3c-116">Authentication (Client)</span></span>|<span data-ttu-id="c9e3c-117">Oui (à l'aide de l'authentification intégrée Windows)</span><span class="sxs-lookup"><span data-stu-id="c9e3c-117">Yes (using Windows integrated authentication)</span></span><br /><br /> <span data-ttu-id="c9e3c-118">Oui (à l'aide de l'authentification intégrée Windows)</span><span class="sxs-lookup"><span data-stu-id="c9e3c-118">Yes (using Windows integrated authentication)</span></span>|  
|<span data-ttu-id="c9e3c-119">Intégrité</span><span class="sxs-lookup"><span data-stu-id="c9e3c-119">Integrity</span></span>|<span data-ttu-id="c9e3c-120">Oui</span><span class="sxs-lookup"><span data-stu-id="c9e3c-120">Yes</span></span>|  
|<span data-ttu-id="c9e3c-121">Confidentialité</span><span class="sxs-lookup"><span data-stu-id="c9e3c-121">Confidentiality</span></span>|<span data-ttu-id="c9e3c-122">Oui</span><span class="sxs-lookup"><span data-stu-id="c9e3c-122">Yes</span></span>|  
|<span data-ttu-id="c9e3c-123">Transport</span><span class="sxs-lookup"><span data-stu-id="c9e3c-123">Transport</span></span>|<span data-ttu-id="c9e3c-124">NET.TCP</span><span class="sxs-lookup"><span data-stu-id="c9e3c-124">NET.TCP</span></span>|  
|<span data-ttu-id="c9e3c-125">Liaison</span><span class="sxs-lookup"><span data-stu-id="c9e3c-125">Binding</span></span>|<xref:System.ServiceModel.NetTcpBinding>|  
  
## <a name="service"></a><span data-ttu-id="c9e3c-126">Service</span><span class="sxs-lookup"><span data-stu-id="c9e3c-126">Service</span></span>  
 <span data-ttu-id="c9e3c-127">La configuration et le code ci-dessous sont conçus pour s'exécuter indépendamment.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-127">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="c9e3c-128">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c9e3c-128">Do one of the following:</span></span>  
  
-   <span data-ttu-id="c9e3c-129">Créez un service autonome à l'aide du code sans configuration.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-129">Create a stand-alone service using the code with no configuration.</span></span>  
  
-   <span data-ttu-id="c9e3c-130">Créez un service à l'aide de la configuration fournie, mais ne définissez pas de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-130">Create a service using the supplied configuration, but do not define any endpoints.</span></span>  
  
### <a name="code"></a><span data-ttu-id="c9e3c-131">Code</span><span class="sxs-lookup"><span data-stu-id="c9e3c-131">Code</span></span>  
 <span data-ttu-id="c9e3c-132">Le code ci-dessous montre comment créer un point de terminaison de service qui utilise une sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-132">The following code shows how to create a service endpoint that uses a Windows security.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#3)]
 [!code-vb[C_SecurityScenarios#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#3)]  
  
### <a name="configuration"></a><span data-ttu-id="c9e3c-133">Configuration</span><span class="sxs-lookup"><span data-stu-id="c9e3c-133">Configuration</span></span>  
 <span data-ttu-id="c9e3c-134">La configuration ci-dessous peut être utilisée à la place du code pour paramétrer le point de terminaison de service :</span><span class="sxs-lookup"><span data-stu-id="c9e3c-134">The following configuration can be used instead of the code to set up the service endpoint:</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <behaviors />  
    <services>  
      <service behaviorConfiguration="" name="ServiceModel.Calculator">  
        <endpoint address="net.tcp://localhost:8008/Calculator"   
                  binding="netTcpBinding"  
          bindingConfiguration="WindowsClientOverTcp"   
                  name="WindowsClientOverTcp"  
                  contract="ServiceModel.ICalculator" />  
      </service>  
    </services>  
    <bindings>  
      <netTcpBinding>  
        <binding name="WindowsClientOverTcp">  
          <security mode="Transport">  
            <transport clientCredentialType="Windows" />  
          </security>  
        </binding>  
      </netTcpBinding>  
    </bindings>  
    <client />  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="client"></a><span data-ttu-id="c9e3c-135">Client</span><span class="sxs-lookup"><span data-stu-id="c9e3c-135">Client</span></span>  
 <span data-ttu-id="c9e3c-136">La configuration et le code ci-dessous sont conçus pour s'exécuter indépendamment.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-136">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="c9e3c-137">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c9e3c-137">Do one of the following:</span></span>  
  
-   <span data-ttu-id="c9e3c-138">Créez un client autonome à l'aide du code (et du code client).</span><span class="sxs-lookup"><span data-stu-id="c9e3c-138">Create a stand-alone client using the code (and client code).</span></span>  
  
-   <span data-ttu-id="c9e3c-139">Créez un client qui ne définit pas d'adresse de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-139">Create a client that does not define any endpoint addresses.</span></span> <span data-ttu-id="c9e3c-140">Au lieu de cela, utilisez le constructeur client qui accepte le nom de configuration comme argument.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-140">Instead, use the client constructor that takes the configuration name as an argument.</span></span> <span data-ttu-id="c9e3c-141">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c9e3c-141">For example:</span></span>  
  
     [!code-csharp[C_SecurityScenarios#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#0)]
     [!code-vb[C_SecurityScenarios#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#0)]  
  
### <a name="code"></a><span data-ttu-id="c9e3c-142">Code</span><span class="sxs-lookup"><span data-stu-id="c9e3c-142">Code</span></span>  
 <span data-ttu-id="c9e3c-143">Le code ci-dessous crée le client.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-143">The following code creates the client.</span></span> <span data-ttu-id="c9e3c-144">La liaison est configurée de manière à utiliser la sécurité du mode de transport, avec le transport TCP et avec le type Windows d’informations d’identification du client.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-144">The binding is configured to use the Transport mode security, with the TCP transport, with the client credential type set to Windows.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#4)]
 [!code-vb[C_SecurityScenarios#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#4)]  
  
### <a name="configuration"></a><span data-ttu-id="c9e3c-145">Configuration</span><span class="sxs-lookup"><span data-stu-id="c9e3c-145">Configuration</span></span>  
 <span data-ttu-id="c9e3c-146">La configuration ci-dessous peut être utilisée à la place du code pour créer le client.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-146">The following configuration can be used instead of the code to create the client.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <bindings>  
      <netTcpBinding>  
        <binding name="NetTcpBinding_ICalculator" >  
          <security mode="Transport">  
            <transport clientCredentialType="Windows" />  
          </security>  
        </binding>  
      </netTcpBinding>  
    </bindings>  
    <client>  
      <endpoint address="net.tcp://localhost:8008/Calculator"   
                binding="netTcpBinding"            
                bindingConfiguration="NetTcpBinding_ICalculator"   
                contract="ICalculator"  
                name="NetTcpBinding_ICalculator">  
      </endpoint>  
    </client>  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="c9e3c-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9e3c-147">See Also</span></span>  
 [<span data-ttu-id="c9e3c-148">Vue d’ensemble de la sécurité</span><span class="sxs-lookup"><span data-stu-id="c9e3c-148">Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/security-overview.md)  
 [<span data-ttu-id="c9e3c-149">Guide pratique pour sécuriser un service avec les informations d’identification Windows</span><span class="sxs-lookup"><span data-stu-id="c9e3c-149">How to: Secure a Service with Windows Credentials</span></span>](../../../../docs/framework/wcf/how-to-secure-a-service-with-windows-credentials.md)  
 [<span data-ttu-id="c9e3c-150">Modèle de sécurité pour Windows Server AppFabric</span><span class="sxs-lookup"><span data-stu-id="c9e3c-150">Security Model for Windows Server App Fabric</span></span>](http://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
