---
title: <transport> de <basicHttpBinding>
ms.date: 03/30/2017
ms.assetid: 4c5ba293-3d7e-47a6-b84e-e9022857b7e5
ms.openlocfilehash: 3d305c90233e4af7dde2a0b80e79e2adbe85c356
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57360005"
---
# <a name="transport-of-basichttpbinding"></a><span data-ttu-id="39ce1-102">\<transport > de \<basicHttpBinding ></span><span class="sxs-lookup"><span data-stu-id="39ce1-102">\<transport> of \<basicHttpBinding></span></span>
<span data-ttu-id="39ce1-103">Définit les propriétés qui déterminent les paramètres d'authentification pour le transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="39ce1-103">Defines properties that control authentication parameters for the HTTP transport.</span></span>  
  
 <span data-ttu-id="39ce1-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="39ce1-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="39ce1-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="39ce1-105">\<bindings></span></span>  
<span data-ttu-id="39ce1-106">\<basicHttpBinding></span><span class="sxs-lookup"><span data-stu-id="39ce1-106">\<basicHttpBinding></span></span>  
<span data-ttu-id="39ce1-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="39ce1-107">\<binding></span></span>  
<span data-ttu-id="39ce1-108">\<security></span><span class="sxs-lookup"><span data-stu-id="39ce1-108">\<security></span></span>  
<span data-ttu-id="39ce1-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="39ce1-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="39ce1-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39ce1-110">Syntax</span></span>  
  
```xml  
<basicHttpBinding>
  <binding>
    <security mode="None|Transport|Message|TransportWithMessageCredential|TransportCredentialOnly">
      <transport clientCredentialType="None|Basic|Digest|Ntlm|Windows"
                 proxyCredentialType="None|Basic|Digest|Ntlm|Windows"
                 realm="String">
        <extendedProtectionPolicy policyEnforcement="Never|WhenSupported|Always"
                                  protectionScenario="TransportSelected|TrustedProxy">
          <customServiceNames>
          </customServiceNames>
        </extendedProtectionPolicy>
      </transport>
    </security>
  </binding>
</basicHttpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="39ce1-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="39ce1-111">Attributes and Elements</span></span>  
 <span data-ttu-id="39ce1-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="39ce1-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="39ce1-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="39ce1-113">Attributes</span></span>  
  
|<span data-ttu-id="39ce1-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="39ce1-114">Attribute</span></span>|<span data-ttu-id="39ce1-115">Description</span><span class="sxs-lookup"><span data-stu-id="39ce1-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="39ce1-116">clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="39ce1-116">clientCredentialType</span></span>|<span data-ttu-id="39ce1-117">-Spécifie le type d’informations d’identification à utiliser lors de l’authentification du client à l’aide de l’authentification HTTP.</span><span class="sxs-lookup"><span data-stu-id="39ce1-117">-   Specifies the type of credential to be used when performing client authentication using HTTP authentication.</span></span>  <span data-ttu-id="39ce1-118">La valeur par défaut est `None`.</span><span class="sxs-lookup"><span data-stu-id="39ce1-118">The default is `None`.</span></span> <span data-ttu-id="39ce1-119">Cet attribut est de type <xref:System.ServiceModel.HttpClientCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="39ce1-119">This attribute is of type <xref:System.ServiceModel.HttpClientCredentialType>.</span></span>|  
|<span data-ttu-id="39ce1-120">proxyCredentialType</span><span class="sxs-lookup"><span data-stu-id="39ce1-120">proxyCredentialType</span></span>|<span data-ttu-id="39ce1-121">-Spécifie le type d’informations d’identification à utiliser lors de l’authentification du client à partir d’un domaine à l’aide d’un proxy sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="39ce1-121">-   Specifies the type of credential to be used when performing client authentication from within a domain using a proxy over HTTP.</span></span> <span data-ttu-id="39ce1-122">Cet attribut est applicable uniquement lorsque l'attribut `mode` de l'élément `security` parent est `Transport` ou `TransportCredentialsOnly`.</span><span class="sxs-lookup"><span data-stu-id="39ce1-122">This attribute is applicable only when the `mode` attribute of the parent `security` element is `Transport` or `TransportCredentialsOnly`.</span></span> <span data-ttu-id="39ce1-123">Cet attribut est de type <xref:System.ServiceModel.HttpProxyCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="39ce1-123">This attribute is of type <xref:System.ServiceModel.HttpProxyCredentialType>.</span></span>|  
|<span data-ttu-id="39ce1-124">realm</span><span class="sxs-lookup"><span data-stu-id="39ce1-124">realm</span></span>|<span data-ttu-id="39ce1-125">Chaîne qui spécifie le domaine utilisé par la méthode d'authentification HTTP pour l'authentification Digest ou de base.</span><span class="sxs-lookup"><span data-stu-id="39ce1-125">A string that specifies the realm that is used by the HTTP authentication scheme for digest or basic authentication.</span></span> <span data-ttu-id="39ce1-126">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="39ce1-126">The default is an empty string.</span></span>|  
|<span data-ttu-id="39ce1-127">policyEnforcement</span><span class="sxs-lookup"><span data-stu-id="39ce1-127">policyEnforcement</span></span>|<span data-ttu-id="39ce1-128">Cette énumération spécifie à quel moment <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> doit être appliqué.</span><span class="sxs-lookup"><span data-stu-id="39ce1-128">This enumeration specifies when the <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> should be enforced.</span></span><br /><br /> <span data-ttu-id="39ce1-129">1.  Never : la stratégie n'est jamais appliquée (la protection étendue est désactivée).</span><span class="sxs-lookup"><span data-stu-id="39ce1-129">1.  Never – The policy is never enforced (Extended Protection is disabled).</span></span><br /><span data-ttu-id="39ce1-130">2.  WhenSupported : la stratégie est appliquée uniquement si le client prend en charge la protection étendue.</span><span class="sxs-lookup"><span data-stu-id="39ce1-130">2.  WhenSupported – The policy is enforced only if the client supports Extended Protection.</span></span><br /><span data-ttu-id="39ce1-131">3.  Always : la stratégie est toujours appliquée.</span><span class="sxs-lookup"><span data-stu-id="39ce1-131">3.  Always – The policy is always enforced.</span></span> <span data-ttu-id="39ce1-132">Les clients qui ne prennent pas en charge la protection étendue ne pourront pas être authentifiés.</span><span class="sxs-lookup"><span data-stu-id="39ce1-132">Clients which don’t support Extended Protection will fail to authenticate.</span></span>|  
|<span data-ttu-id="39ce1-133">protectionScenario</span><span class="sxs-lookup"><span data-stu-id="39ce1-133">protectionScenario</span></span>|<span data-ttu-id="39ce1-134">Cette énumération spécifie le scénario de protection appliqué par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="39ce1-134">This enumeration specifies the protection scenario enforced by the policy.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="39ce1-135">Attribut clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="39ce1-135">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="39ce1-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="39ce1-136">Value</span></span>|<span data-ttu-id="39ce1-137">Description</span><span class="sxs-lookup"><span data-stu-id="39ce1-137">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="39ce1-138">None</span><span class="sxs-lookup"><span data-stu-id="39ce1-138">None</span></span>|<span data-ttu-id="39ce1-139">Les messages ne sont pas sécurisés pendant le transfert.</span><span class="sxs-lookup"><span data-stu-id="39ce1-139">Messages are not secured during transfer.</span></span>|  
|<span data-ttu-id="39ce1-140">Basic</span><span class="sxs-lookup"><span data-stu-id="39ce1-140">Basic</span></span>|<span data-ttu-id="39ce1-141">Spécifie l'authentification de base.</span><span class="sxs-lookup"><span data-stu-id="39ce1-141">Specifies basic authentication.</span></span>|  
|<span data-ttu-id="39ce1-142">Digest</span><span class="sxs-lookup"><span data-stu-id="39ce1-142">Digest</span></span>|<span data-ttu-id="39ce1-143">Spécifie l'authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="39ce1-143">Specifies digest authentication.</span></span>|  
|<span data-ttu-id="39ce1-144">Ntlm</span><span class="sxs-lookup"><span data-stu-id="39ce1-144">Ntlm</span></span>|<span data-ttu-id="39ce1-145">Spécifie l'authentification NTLM le cas échéant et en cas d'échec d'authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="39ce1-145">Specifies NTLM authentication when possible, and if Windows authentication fails.</span></span>|  
|<span data-ttu-id="39ce1-146">Windows</span><span class="sxs-lookup"><span data-stu-id="39ce1-146">Windows</span></span>|<span data-ttu-id="39ce1-147">Spécifie l'authentification intégrée Windows.</span><span class="sxs-lookup"><span data-stu-id="39ce1-147">Specifies Windows integrated authentication.</span></span>|  
  
## <a name="proxycredentialtype-attribute"></a><span data-ttu-id="39ce1-148">Attribut proxyCredentialType</span><span class="sxs-lookup"><span data-stu-id="39ce1-148">proxyCredentialType Attribute</span></span>  
  
|<span data-ttu-id="39ce1-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="39ce1-149">Value</span></span>|<span data-ttu-id="39ce1-150">Description</span><span class="sxs-lookup"><span data-stu-id="39ce1-150">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="39ce1-151">Aucun.</span><span class="sxs-lookup"><span data-stu-id="39ce1-151">None</span></span>|<span data-ttu-id="39ce1-152">-Les messages ne sont pas sécurisés pendant le transfert.</span><span class="sxs-lookup"><span data-stu-id="39ce1-152">-   Messages are not secured during transfer.</span></span>|  
|<span data-ttu-id="39ce1-153">Basic</span><span class="sxs-lookup"><span data-stu-id="39ce1-153">Basic</span></span>|<span data-ttu-id="39ce1-154">Spécifie l’authentification de base tel que défini par RFC 2617 – HTTP Authentication : Base et authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="39ce1-154">Specifies basic authentication as defined by RFC 2617 – HTTP Authentication: Basic and Digest Authentication.</span></span>|  
|<span data-ttu-id="39ce1-155">Digest</span><span class="sxs-lookup"><span data-stu-id="39ce1-155">Digest</span></span>|<span data-ttu-id="39ce1-156">Spécifie l’authentification digest, comme défini par RFC 2617 – HTTP Authentication : Base et authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="39ce1-156">Specifies digest authentication as defined by RFC 2617 – HTTP Authentication: Basic and Digest Authentication.</span></span>|  
|<span data-ttu-id="39ce1-157">Ntlm</span><span class="sxs-lookup"><span data-stu-id="39ce1-157">Ntlm</span></span>|<span data-ttu-id="39ce1-158">Spécifie l'authentification NTLM le cas échéant et en cas d'échec d'authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="39ce1-158">Specifies NTLM authentication when possible, and if Windows authentication fails.</span></span>|  
|<span data-ttu-id="39ce1-159">Windows</span><span class="sxs-lookup"><span data-stu-id="39ce1-159">Windows</span></span>|<span data-ttu-id="39ce1-160">Spécifie l'authentification intégrée Windows.</span><span class="sxs-lookup"><span data-stu-id="39ce1-160">Specifies Windows integrated authentication.</span></span>|  
|<span data-ttu-id="39ce1-161">Certificat</span><span class="sxs-lookup"><span data-stu-id="39ce1-161">Certificate</span></span>|<span data-ttu-id="39ce1-162">Effectue l'authentification du client à l'aide d'un certificat.</span><span class="sxs-lookup"><span data-stu-id="39ce1-162">Performs client authentication using a certificate.</span></span> <span data-ttu-id="39ce1-163">Cette option fonctionne uniquement si l'attribut `Mode` de l'élément `security` parent est configuré pour le transport et ne fonctionnera pas s'il a la valeur TransportCredentialOnly.</span><span class="sxs-lookup"><span data-stu-id="39ce1-163">This option works only if the `Mode` attribute of the parent `security` element is set to Transport, and will not work if it is set to TransportCredentialOnly.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="39ce1-164">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="39ce1-164">Child Elements</span></span>  
 <span data-ttu-id="39ce1-165">Aucun.</span><span class="sxs-lookup"><span data-stu-id="39ce1-165">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="39ce1-166">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="39ce1-166">Parent Elements</span></span>  
  
|<span data-ttu-id="39ce1-167">Élément</span><span class="sxs-lookup"><span data-stu-id="39ce1-167">Element</span></span>|<span data-ttu-id="39ce1-168">Description</span><span class="sxs-lookup"><span data-stu-id="39ce1-168">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="39ce1-169">\<security></span><span class="sxs-lookup"><span data-stu-id="39ce1-169">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-basichttpbinding.md)|<span data-ttu-id="39ce1-170">Définit les fonctionnalités de sécurité pour le [ \<basicHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="39ce1-170">Defines the security capabilities for the [\<basicHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span></span>|  
  
## <a name="example"></a><span data-ttu-id="39ce1-171">Exemple</span><span class="sxs-lookup"><span data-stu-id="39ce1-171">Example</span></span>  
 <span data-ttu-id="39ce1-172">L'exemple suivant montre l'utilisation de la sécurité de transport SSL avec la liaison de base.</span><span class="sxs-lookup"><span data-stu-id="39ce1-172">The following example demonstrates the use of SSL transport security with the basic binding.</span></span> <span data-ttu-id="39ce1-173">Par défaut, la liaison de base prend en charge la communication HTTP.</span><span class="sxs-lookup"><span data-stu-id="39ce1-173">By default, the basic binding supports HTTP communication.</span></span>  
  
```xml  
<system.serviceModel>
  <services>
    <service type="Microsoft.ServiceModel.Samples.CalculatorService"
             behaviorConfiguration="CalculatorServiceBehavior">
      <endpoint address=""
                binding="basicHttpBinding"
                bindingConfiguration="Binding1"
                contract="Microsoft.ServiceModel.Samples.ICalculator" />
    </service>
  </services>
  <bindings>
    <basicHttpBinding>
      <!-- Configure basicHttpBinding with Transport security -->
      <!-- mode and clientCredentialType set to None. -->
      <binding name="Binding1">
        <security mode="Transport">
          <transport clientCredentialType="None"
                     proxyCredentialType="None">
            <extendedProtectionPolicy policyEnforcement="WhenSupported"
                                      protectionScenario="TransportSelected">
              <customServiceNames>
              </customServiceNames>
            </extendedProtectionPolicy>
          </transport>
        </security>
      </binding>
    </basicHttpBinding>
  </bindings>
</system.serviceModel>
```  
  
## <a name="see-also"></a><span data-ttu-id="39ce1-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39ce1-174">See also</span></span>
- <xref:System.ServiceModel.Configuration.BasicHttpSecurityElement.Transport%2A>
- <xref:System.ServiceModel.BasicHttpSecurity.Transport%2A>
- <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement>
- <xref:System.ServiceModel.HttpTransportSecurity>
- [<span data-ttu-id="39ce1-175">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="39ce1-175">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="39ce1-176">Liaisons</span><span class="sxs-lookup"><span data-stu-id="39ce1-176">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="39ce1-177">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="39ce1-177">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="39ce1-178">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="39ce1-178">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="39ce1-179">\<binding></span><span class="sxs-lookup"><span data-stu-id="39ce1-179">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
