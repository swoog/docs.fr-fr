---
title: Service et client Internet non sécurisés
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 97a10d79-3e7d-4bd1-9a99-fd9807fd70bc
ms.openlocfilehash: ca6b028ef20095d6faeb125151772eedf1500fa0
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59133755"
---
# <a name="internet-unsecured-client-and-service"></a><span data-ttu-id="37f76-102">Service et client Internet non sécurisés</span><span class="sxs-lookup"><span data-stu-id="37f76-102">Internet Unsecured Client and Service</span></span>
<span data-ttu-id="37f76-103">L’illustration suivante montre un exemple de client Windows Communication Foundation (WCF) publics, non sécurisés et service :</span><span class="sxs-lookup"><span data-stu-id="37f76-103">The following illustration shows an example of a public, unsecured Windows Communication Foundation (WCF) client and service:</span></span>  
  
 ![Capture d’écran montrant un scénario Internet non sécurisé](./media/internet-unsecured-client-and-service/public-unsecured-internet.gif)  
  
|<span data-ttu-id="37f76-105">Caractéristique</span><span class="sxs-lookup"><span data-stu-id="37f76-105">Characteristic</span></span>|<span data-ttu-id="37f76-106">Description</span><span class="sxs-lookup"><span data-stu-id="37f76-106">Description</span></span>|  
|--------------------|-----------------|  
|<span data-ttu-id="37f76-107">Mode de sécurité</span><span class="sxs-lookup"><span data-stu-id="37f76-107">Security Mode</span></span>|<span data-ttu-id="37f76-108">Aucun.</span><span class="sxs-lookup"><span data-stu-id="37f76-108">None</span></span>|  
|<span data-ttu-id="37f76-109">Transport</span><span class="sxs-lookup"><span data-stu-id="37f76-109">Transport</span></span>|<span data-ttu-id="37f76-110">HTTP</span><span class="sxs-lookup"><span data-stu-id="37f76-110">HTTP</span></span>|  
|<span data-ttu-id="37f76-111">Liaison</span><span class="sxs-lookup"><span data-stu-id="37f76-111">Binding</span></span>|<xref:System.ServiceModel.BasicHttpBinding> <span data-ttu-id="37f76-112">dans le code, ou le [ \<basicHttpBinding >](../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md) élément de configuration.</span><span class="sxs-lookup"><span data-stu-id="37f76-112">in code, or the [\<basicHttpBinding>](../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md) element in configuration.</span></span>|  
|<span data-ttu-id="37f76-113">Interopérabilité</span><span class="sxs-lookup"><span data-stu-id="37f76-113">Interoperability</span></span>|<span data-ttu-id="37f76-114">Avec les clients de service Web et les services existants</span><span class="sxs-lookup"><span data-stu-id="37f76-114">With existing Web service clients and services</span></span>|  
|<span data-ttu-id="37f76-115">Authentification</span><span class="sxs-lookup"><span data-stu-id="37f76-115">Authentication</span></span>|<span data-ttu-id="37f76-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="37f76-116">None</span></span>|  
|<span data-ttu-id="37f76-117">Intégrité</span><span class="sxs-lookup"><span data-stu-id="37f76-117">Integrity</span></span>|<span data-ttu-id="37f76-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="37f76-118">None</span></span>|  
|<span data-ttu-id="37f76-119">Confidentialité</span><span class="sxs-lookup"><span data-stu-id="37f76-119">Confidentiality</span></span>|<span data-ttu-id="37f76-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="37f76-120">None</span></span>|  
  
## <a name="service"></a><span data-ttu-id="37f76-121">Service</span><span class="sxs-lookup"><span data-stu-id="37f76-121">Service</span></span>  
 <span data-ttu-id="37f76-122">La configuration et le code ci-dessous sont conçus pour s'exécuter indépendamment.</span><span class="sxs-lookup"><span data-stu-id="37f76-122">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="37f76-123">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="37f76-123">Do one of the following:</span></span>  
  
-   <span data-ttu-id="37f76-124">Créez un service autonome à l'aide du code sans configuration.</span><span class="sxs-lookup"><span data-stu-id="37f76-124">Create a stand-alone service using the code with no configuration.</span></span>  
  
-   <span data-ttu-id="37f76-125">Créez un service à l'aide de la configuration fournie, mais ne définissez pas de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="37f76-125">Create a service using the supplied configuration, but do not define any endpoints.</span></span>  
  
### <a name="code"></a><span data-ttu-id="37f76-126">Code</span><span class="sxs-lookup"><span data-stu-id="37f76-126">Code</span></span>  
 <span data-ttu-id="37f76-127">Le code ci-dessous montre comment créer un point de terminaison sans sécurité.</span><span class="sxs-lookup"><span data-stu-id="37f76-127">The following code shows how to create an endpoint with no security.</span></span> <span data-ttu-id="37f76-128">Par défaut, <xref:System.ServiceModel.BasicHttpBinding> a le mode de sécurité défini avec la valeur <xref:System.ServiceModel.BasicHttpSecurityMode.None>.</span><span class="sxs-lookup"><span data-stu-id="37f76-128">By default, the <xref:System.ServiceModel.BasicHttpBinding> has the security mode set to <xref:System.ServiceModel.BasicHttpSecurityMode.None>.</span></span>  
  
 [!code-csharp[C_UnsecuredService#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_unsecuredservice/cs/source.cs#1)]
 [!code-vb[C_UnsecuredService#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_unsecuredservice/vb/source.vb#1)]  
  
### <a name="service-configuration"></a><span data-ttu-id="37f76-129">Configuration du service</span><span class="sxs-lookup"><span data-stu-id="37f76-129">Service Configuration</span></span>  
 <span data-ttu-id="37f76-130">Le code ci-dessous configure le même point de terminaison en utilisant la configuration.</span><span class="sxs-lookup"><span data-stu-id="37f76-130">The following code sets up the same endpoint using configuration.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <behaviors />  
    <services>  
      <service behaviorConfiguration="" name="ServiceModel.Calculator">  
        <endpoint address="http://localhost/Calculator"   
                  binding="basicHttpBinding"  
                  bindingConfiguration="Basic_Unsecured"   
                  name="BasicHttp_ICalculator"  
                  contract="ServiceModel.ICalculator" />  
      </service>  
    </services>  
    <bindings>  
      <basicHttpBinding>  
        <binding name="Basic_Unsecured" />  
      </basicHttpBinding>  
    </bindings>  
    <client />  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="client"></a><span data-ttu-id="37f76-131">Client</span><span class="sxs-lookup"><span data-stu-id="37f76-131">Client</span></span>  
 <span data-ttu-id="37f76-132">La configuration et le code ci-dessous sont conçus pour s'exécuter indépendamment.</span><span class="sxs-lookup"><span data-stu-id="37f76-132">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="37f76-133">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="37f76-133">Do one of the following:</span></span>  
  
-   <span data-ttu-id="37f76-134">Créez un client autonome à l'aide du code (et du code client).</span><span class="sxs-lookup"><span data-stu-id="37f76-134">Create a stand-alone client using the code (and client code).</span></span>  
  
-   <span data-ttu-id="37f76-135">Créez un client qui ne définit pas d'adresse de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="37f76-135">Create a client that does not define any endpoint addresses.</span></span> <span data-ttu-id="37f76-136">Au lieu de cela, utilisez le constructeur client qui accepte le nom de configuration comme argument.</span><span class="sxs-lookup"><span data-stu-id="37f76-136">Instead, use the client constructor that takes the configuration name as an argument.</span></span> <span data-ttu-id="37f76-137">Exemple :</span><span class="sxs-lookup"><span data-stu-id="37f76-137">For example:</span></span>  
  
     [!code-csharp[C_SecurityScenarios#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#0)]
     [!code-vb[C_SecurityScenarios#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#0)]  
  
### <a name="code"></a><span data-ttu-id="37f76-138">Code</span><span class="sxs-lookup"><span data-stu-id="37f76-138">Code</span></span>  
 <span data-ttu-id="37f76-139">Le code suivant montre un client WCF de base qui accède à un point de terminaison non sécurisé.</span><span class="sxs-lookup"><span data-stu-id="37f76-139">The following code shows a basic WCF client that accesses an unsecured endpoint.</span></span>  
  
 [!code-csharp[C_UnsecuredClient#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_unsecuredclient/cs/source.cs#1)]
 [!code-vb[C_UnsecuredClient#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_unsecuredclient/vb/source.vb#1)]  
  
### <a name="client-configuration"></a><span data-ttu-id="37f76-140">Configuration client</span><span class="sxs-lookup"><span data-stu-id="37f76-140">Client Configuration</span></span>  
 <span data-ttu-id="37f76-141">Le code ci-dessous configure le client.</span><span class="sxs-lookup"><span data-stu-id="37f76-141">The following code configures the client.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <bindings>  
      <basicHttpBinding>  
        <binding name="BasicHttpBinding_ICalculator" >  
          <security mode="None">  
          </security>  
        </binding>  
      </basicHttpBinding>  
    </bindings>  
    <client>  
      <endpoint address="http://localhost/Calculator/Unsecured"  
          binding="basicHttpBinding"   
          bindingConfiguration="BasicHttpBinding_ICalculator"  
          contract="ICalculator"   
          name="BasicHttpBinding_ICalculator" />  
    </client>  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="37f76-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37f76-142">See also</span></span>

- [<span data-ttu-id="37f76-143">Scénarios de sécurité courants</span><span class="sxs-lookup"><span data-stu-id="37f76-143">Common Security Scenarios</span></span>](../../../../docs/framework/wcf/feature-details/common-security-scenarios.md)
- [<span data-ttu-id="37f76-144">Vue d'ensemble de la sécurité</span><span class="sxs-lookup"><span data-stu-id="37f76-144">Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/security-overview.md)
- [<span data-ttu-id="37f76-145">Modèle de sécurité pour Windows Server AppFabric</span><span class="sxs-lookup"><span data-stu-id="37f76-145">Security Model for Windows Server App Fabric</span></span>](https://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
