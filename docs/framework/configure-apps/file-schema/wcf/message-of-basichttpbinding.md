---
title: '&lt;message&gt; de &lt;basicHttpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 51cdd329-6461-471a-8747-56c2299b61e5
ms.openlocfilehash: 08307d1120904fc703e7b76616aacce7e153929a
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48782075"
---
# <a name="ltmessagegt-of-ltbasichttpbindinggt"></a><span data-ttu-id="93480-102">&lt;message&gt; de &lt;basicHttpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="93480-102">&lt;message&gt; of &lt;basicHttpBinding&gt;</span></span>
<span data-ttu-id="93480-103">Définit les paramètres de sécurité au niveau du message de la [ \<basicHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="93480-103">Defines the settings for message-level security of the [\<basicHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span></span>  
  
 <span data-ttu-id="93480-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="93480-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="93480-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="93480-105">\<bindings></span></span>  
<span data-ttu-id="93480-106">\<basicHttpBinding></span><span class="sxs-lookup"><span data-stu-id="93480-106">\<basicHttpBinding></span></span>  
<span data-ttu-id="93480-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="93480-107">\<binding></span></span>  
<span data-ttu-id="93480-108">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="93480-108">\<security></span></span>  
<span data-ttu-id="93480-109">\<message></span><span class="sxs-lookup"><span data-stu-id="93480-109">\<message></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="93480-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93480-110">Syntax</span></span>  
  
```xml  
<message   
   algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
      clientCredentialType="UserName/Certificate"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="93480-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="93480-111">Attributes and Elements</span></span>  
 <span data-ttu-id="93480-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="93480-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="93480-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="93480-113">Attributes</span></span>  
  
|<span data-ttu-id="93480-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="93480-114">Attribute</span></span>|<span data-ttu-id="93480-115">Description</span><span class="sxs-lookup"><span data-stu-id="93480-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="93480-116">algorithmSuite</span><span class="sxs-lookup"><span data-stu-id="93480-116">algorithmSuite</span></span>|<span data-ttu-id="93480-117">Définit les algorithmes de chiffrement de message et de clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="93480-117">Sets the message encryption and key-wrap algorithms.</span></span> <span data-ttu-id="93480-118">Cet attribut est de type <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>, qui spécifie les algorithmes et les tailles de clé.</span><span class="sxs-lookup"><span data-stu-id="93480-118">This attribute is of type <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>, which specifies the algorithms and the key sizes.</span></span> <span data-ttu-id="93480-119">Ces algorithmes se mappent à ceux définis dans la spécification Security Policy Language (WS-SecurityPolicy).</span><span class="sxs-lookup"><span data-stu-id="93480-119">These algorithms map to those specified in the Security Policy Language (WS-SecurityPolicy) specification.</span></span><br /><br /> <span data-ttu-id="93480-120">La valeur par défaut est `Basic256`.</span><span class="sxs-lookup"><span data-stu-id="93480-120">The default value is `Basic256`.</span></span>|  
|<span data-ttu-id="93480-121">clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="93480-121">clientCredentialType</span></span>|<span data-ttu-id="93480-122">Spécifie le type d'informations d'identification à utiliser lors de l'authentification du client à l'aide de la sécurité basée sur les messages.</span><span class="sxs-lookup"><span data-stu-id="93480-122">Specifies the type of credential to be used when performing client authentication using message-based security.</span></span> <span data-ttu-id="93480-123">La valeur par défaut est `UserName`.</span><span class="sxs-lookup"><span data-stu-id="93480-123">The default is `UserName`.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="93480-124">Attribut clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="93480-124">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="93480-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="93480-125">Value</span></span>|<span data-ttu-id="93480-126">Description</span><span class="sxs-lookup"><span data-stu-id="93480-126">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="93480-127">UserName</span><span class="sxs-lookup"><span data-stu-id="93480-127">UserName</span></span>|<span data-ttu-id="93480-128">-Nécessite le client soit authentifié au serveur avec une information d’identification de nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="93480-128">-   Requires the client be authenticated to the server with a UserName credential.</span></span> <span data-ttu-id="93480-129">Ces informations d’identification doivent être spécifiées à l’aide de la [ \<clientCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md).</span><span class="sxs-lookup"><span data-stu-id="93480-129">This credential needs to be specified using the [\<clientCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md).</span></span><br /><span data-ttu-id="93480-130">-WCF ne prend pas en charge l’envoi d’un mot de passe digest ou de dérivation de clés à l’aide de mots de passe et à l’aide de ces clés pour la sécurité de message.</span><span class="sxs-lookup"><span data-stu-id="93480-130">-   WCF does not support sending a password digest or deriving keys using passwords and using such keys for message security.</span></span> <span data-ttu-id="93480-131">WCF applique donc que le transport est sécurisé lors de l’utilisation des informations d’identification UserName.</span><span class="sxs-lookup"><span data-stu-id="93480-131">Therefore, WCF enforces that the transport be secured when using UserName credentials.</span></span> <span data-ttu-id="93480-132">Pour le `basicHttpBinding`, cela requiert la configuration d'un canal SSL.</span><span class="sxs-lookup"><span data-stu-id="93480-132">For the `basicHttpBinding`, this requires setting up an SSL channel.</span></span>|  
|<span data-ttu-id="93480-133">Certificat</span><span class="sxs-lookup"><span data-stu-id="93480-133">Certificate</span></span>|<span data-ttu-id="93480-134">Requiert que le client soit authentifié auprès du serveur à l'aide d'un certificat.</span><span class="sxs-lookup"><span data-stu-id="93480-134">Requires that the client be authenticated to the server using a certificate.</span></span> <span data-ttu-id="93480-135">Les informations d’identification du client dans ce cas doivent être spécifiées à l’aide [ \<clientCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) et [ \<clientCertificate >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcertificate-of-servicecredentials.md).</span><span class="sxs-lookup"><span data-stu-id="93480-135">The client credential in this case needs to be specified using [\<clientCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) and the [\<clientCertificate>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcertificate-of-servicecredentials.md).</span></span> <span data-ttu-id="93480-136">De plus, lors de l'utilisation du mode de sécurité du message, le client doit être configuré avec le certificat du service.</span><span class="sxs-lookup"><span data-stu-id="93480-136">In addition, when using message security mode, the client needs to be provisioned with the service certificate.</span></span> <span data-ttu-id="93480-137">Les informations d’identification de service dans ce cas doivent être spécifiées à l’aide <xref:System.ServiceModel.Description.ClientCredentials> classe ou `ClientCredentials` élément de comportement et spécifiez le service de certificats à l’aide de la [ \<serviceCertificate >](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecertificate-of-servicecredentials.md).</span><span class="sxs-lookup"><span data-stu-id="93480-137">The service credential in this case needs to be specified using <xref:System.ServiceModel.Description.ClientCredentials> class or `ClientCredentials` behavior element and specifying the service certificate using the [\<serviceCertificate>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecertificate-of-servicecredentials.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="93480-138">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="93480-138">Child Elements</span></span>  
 <span data-ttu-id="93480-139">Aucun.</span><span class="sxs-lookup"><span data-stu-id="93480-139">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="93480-140">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="93480-140">Parent Elements</span></span>  
  
|<span data-ttu-id="93480-141">Élément</span><span class="sxs-lookup"><span data-stu-id="93480-141">Element</span></span>|<span data-ttu-id="93480-142">Description</span><span class="sxs-lookup"><span data-stu-id="93480-142">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="93480-143">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="93480-143">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-basichttpbinding.md)|<span data-ttu-id="93480-144">Définit les fonctionnalités de sécurité pour le [ \<basicHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="93480-144">Defines the security capabilities for the [\<basicHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span></span>|  
  
## <a name="example"></a><span data-ttu-id="93480-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="93480-145">Example</span></span>  
 <span data-ttu-id="93480-146">Cet exemple montre comment implémenter une application qui utilise le basicHttpBinding et la sécurité de message.</span><span class="sxs-lookup"><span data-stu-id="93480-146">This sample demonstrates how to implement an application that uses the basicHttpBinding and message security.</span></span> <span data-ttu-id="93480-147">Dans l'exemple de configuration suivant pour un service, la définition du point de terminaison spécifie le basicHttpBinding et référence une configuration de liaison nommée `Binding1`.</span><span class="sxs-lookup"><span data-stu-id="93480-147">In the following configuration example for a service, the endpoint definition specifies the basicHttpBinding and references a binding configuration named `Binding1`.</span></span> <span data-ttu-id="93480-148">Le certificat que le service utilise pour s'authentifier auprès du client est défini dans la section `behaviors` du fichier de configuration sous l'élément `serviceCredentials`.</span><span class="sxs-lookup"><span data-stu-id="93480-148">The certificate that the service uses to authenticate itself to the client is set in the `behaviors` section of the configuration file under the `serviceCredentials` element.</span></span> <span data-ttu-id="93480-149">Le mode de validation qui s'applique au certificat que le client utilise pour s'authentifier auprès du service est également défini dans la section `behaviors` sous l'élément `clientCertificate`.</span><span class="sxs-lookup"><span data-stu-id="93480-149">The validation mode that applies to the certificate that the client uses to authenticate itself to the service is also set in the `behaviors` section under the `clientCertificate` element.</span></span>  
  
 <span data-ttu-id="93480-150">Les mêmes détails sur la liaison et la sécurité sont spécifiés dans le fichier de configuration client.</span><span class="sxs-lookup"><span data-stu-id="93480-150">The same binding and security details are specified in the client configuration file.</span></span>  
  
```xml  
<system.serviceModel>  
    <services>  
      <service name="Microsoft.ServiceModel.Samples.CalculatorService"  
               behaviorConfiguration="CalculatorServiceBehavior">  
        <host>  
          <baseAddresses>  
            <add baseAddress="http://localhost:8000/ServiceModelSamples/service"/>  
          </baseAddresses>  
        </host>  
        <!-- this endpoint is exposed at the base address provided by host: http://localhost:8000/ServiceModelSamples/service  -->  
        <endpoint address=""  
                  binding="basicHttpBinding"  
                  bindingConfiguration="Binding1"   
                  contract="Microsoft.ServiceModel.Samples.ICalculator" />  
        <!-- the mex endpoint is exposed at http://localhost:8000/ServiceModelSamples/service/mex -->  
        <endpoint address="mex"  
                  binding="mexHttpBinding"  
                  contract="IMetadataExchange" />  
      </service>  
    </services>  
  
    <bindings>  
      <basicHttpBinding>  
        <!--   
        This configuration defines the SecurityMode as Message and   
        the clientCredentialType as Certificate.  
        -->  
        <binding name="Binding1" >  
          <security mode = "Message">  
            <message clientCredentialType="Certificate"/>  
          </security>  
        </binding>  
      </basicHttpBinding>  
    </bindings>  
  
    <!--For debugging purposes set the includeExceptionDetailInFaults attribute to true-->  
    <behaviors>  
      <serviceBehaviors>  
        <behavior name="CalculatorServiceBehavior">  
          <serviceMetadata httpGetEnabled="True"/>  
          <serviceDebug includeExceptionDetailInFaults="False" />  
          <!--  
        The serviceCredentials behavior allows one to define a service certificate.  
        A service certificate is used by a client to authenticate the service and provide message protection.  
        This configuration references the "localhost" certificate installed during the setup instructions.  
        -->  
          <serviceCredentials>  
            <serviceCertificate findValue="localhost" storeLocation="LocalMachine" storeName="My" x509FindType="FindBySubjectName" />  
            <clientCertificate>  
              <!--   
            Setting the certificateValidationMode to PeerOrChainTrust means that if the certificate   
            is in the user's Trusted People store, then it will be trusted without performing a  
            validation of the certificate's issuer chain. This setting is used here for convenience so that the   
            sample can be run without having to have certificates issued by a certification authority (CA).  
            This setting is less secure than the default, ChainTrust. The security implications of this   
            setting should be carefully considered before using PeerOrChainTrust in production code.   
            -->  
              <authentication certificateValidationMode="PeerOrChainTrust" />  
            </clientCertificate>  
          </serviceCredentials>  
        </behavior>  
      </serviceBehaviors>  
    </behaviors>  
</system.serviceModel>  
```  
  
## <a name="see-also"></a><span data-ttu-id="93480-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93480-151">See Also</span></span>  
 <xref:System.ServiceModel.BasicHttpMessageSecurity>  
 <xref:System.ServiceModel.Configuration.BasicHttpSecurityElement.Message%2A>  
 <xref:System.ServiceModel.BasicHttpSecurity.Message%2A>  
 <xref:System.ServiceModel.Configuration.BasicHttpMessageSecurityElement>  
 [<span data-ttu-id="93480-152">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="93480-152">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="93480-153">Liaisons</span><span class="sxs-lookup"><span data-stu-id="93480-153">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="93480-154">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="93480-154">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="93480-155">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="93480-155">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="93480-156">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="93480-156">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
