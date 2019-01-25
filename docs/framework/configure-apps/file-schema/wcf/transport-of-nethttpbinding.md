---
title: '&lt;transport&gt; of &lt;netHttpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 3b180006-1661-43bf-a699-96fd3da469af
ms.openlocfilehash: 0195708d24e61dfee4c396518c94d5e21b7783bb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54578885"
---
# <a name="lttransportgt-of-ltnethttpbindinggt"></a><span data-ttu-id="161b3-102">&lt;transport&gt; of &lt;netHttpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="161b3-102">&lt;transport&gt; of &lt;netHttpBinding&gt;</span></span>
<span data-ttu-id="161b3-103">Définit les propriétés qui déterminent les paramètres d'authentification pour le transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="161b3-103">Defines properties that control authentication parameters for the HTTP transport.</span></span>  
  
<span data-ttu-id="161b3-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="161b3-104">\<system.serviceModel></span></span>  
<span data-ttu-id="161b3-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="161b3-105">\<bindings></span></span>  
<span data-ttu-id="161b3-106">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="161b3-106">\<netHttpBinding></span></span>  
<span data-ttu-id="161b3-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="161b3-107">\<binding></span></span>  
<span data-ttu-id="161b3-108">\<security></span><span class="sxs-lookup"><span data-stu-id="161b3-108">\<security></span></span>  
<span data-ttu-id="161b3-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="161b3-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="161b3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="161b3-110">Syntax</span></span>  
  
```xml  
<netHttpBinding>
  <binding>
    <security mode="None|Transport|Message|TransportWithMessageCredential|TransportCredentialOnly">
      <transport clientCredentialType="None|Basic|Digest|Ntlm|Windows"
                 proxyCredentialType="None|Basic|Digest|Ntlm|Windows"
                 realm="string">
        <extendedProtectionPolicy policyEnforcement="Never|WhenSupported|Always"
                                  protectionScenario="TransportSelected|TrustedProxy">
          <customServiceNames>
          </customServiceNames>
        </extendedProtectionPolicy>
      </transport>
    </security>
  </binding>
</netHttpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="161b3-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="161b3-111">Attributes and Elements</span></span>  
 <span data-ttu-id="161b3-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="161b3-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="161b3-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="161b3-113">Attributes</span></span>  
  
|<span data-ttu-id="161b3-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="161b3-114">Attribute</span></span>|<span data-ttu-id="161b3-115">Description</span><span class="sxs-lookup"><span data-stu-id="161b3-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="161b3-116">clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="161b3-116">clientCredentialType</span></span>|<span data-ttu-id="161b3-117">-Spécifie le type d’informations d’identification à utiliser lors de l’authentification du client à l’aide de l’authentification HTTP.</span><span class="sxs-lookup"><span data-stu-id="161b3-117">-   Specifies the type of credential to be used when performing client authentication using HTTP authentication.</span></span>  <span data-ttu-id="161b3-118">La valeur par défaut est `None`.</span><span class="sxs-lookup"><span data-stu-id="161b3-118">The default is `None`.</span></span> <span data-ttu-id="161b3-119">Cet attribut est de type <xref:System.ServiceModel.HttpClientCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="161b3-119">This attribute is of type <xref:System.ServiceModel.HttpClientCredentialType>.</span></span>|  
|<span data-ttu-id="161b3-120">proxyCredentialType</span><span class="sxs-lookup"><span data-stu-id="161b3-120">proxyCredentialType</span></span>|<span data-ttu-id="161b3-121">-Spécifie le type d’informations d’identification à utiliser lors de l’authentification du client à partir d’un domaine à l’aide d’un proxy sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="161b3-121">-   Specifies the type of credential to be used when performing client authentication from within a domain using a proxy over HTTP.</span></span> <span data-ttu-id="161b3-122">Cet attribut est applicable uniquement lorsque l'attribut `mode` de l'élément `security` parent est `Transport` ou `TransportCredentialsOnly`.</span><span class="sxs-lookup"><span data-stu-id="161b3-122">This attribute is applicable only when the `mode` attribute of the parent `security` element is `Transport` or `TransportCredentialsOnly`.</span></span> <span data-ttu-id="161b3-123">Cet attribut est de type <xref:System.ServiceModel.HttpProxyCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="161b3-123">This attribute is of type <xref:System.ServiceModel.HttpProxyCredentialType>.</span></span>|  
|<span data-ttu-id="161b3-124">realm</span><span class="sxs-lookup"><span data-stu-id="161b3-124">realm</span></span>|<span data-ttu-id="161b3-125">Chaîne qui spécifie le domaine utilisé par la méthode d'authentification HTTP pour l'authentification Digest ou de base.</span><span class="sxs-lookup"><span data-stu-id="161b3-125">A string that specifies the realm that is used by the HTTP authentication scheme for digest or basic authentication.</span></span> <span data-ttu-id="161b3-126">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="161b3-126">The default is an empty string.</span></span>|  
|<span data-ttu-id="161b3-127">policyEnforcement</span><span class="sxs-lookup"><span data-stu-id="161b3-127">policyEnforcement</span></span>|<span data-ttu-id="161b3-128">Cette énumération spécifie à quel moment <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> doit être appliqué.</span><span class="sxs-lookup"><span data-stu-id="161b3-128">This enumeration specifies when the <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> should be enforced.</span></span><br /><br /> <span data-ttu-id="161b3-129">1.  Never : la stratégie n'est jamais appliquée (la protection étendue est désactivée).</span><span class="sxs-lookup"><span data-stu-id="161b3-129">1.  Never – The policy is never enforced (Extended Protection is disabled).</span></span><br /><span data-ttu-id="161b3-130">2.  WhenSupported : la stratégie est appliquée uniquement si le client prend en charge la protection étendue.</span><span class="sxs-lookup"><span data-stu-id="161b3-130">2.  WhenSupported – The policy is enforced only if the client supports Extended Protection.</span></span><br /><span data-ttu-id="161b3-131">3.  Always : la stratégie est toujours appliquée.</span><span class="sxs-lookup"><span data-stu-id="161b3-131">3.  Always – The policy is always enforced.</span></span> <span data-ttu-id="161b3-132">Les clients qui ne prennent pas en charge la protection étendue ne pourront pas être authentifiés.</span><span class="sxs-lookup"><span data-stu-id="161b3-132">Clients which don’t support Extended Protection will fail to authenticate.</span></span>|  
|<span data-ttu-id="161b3-133">protectionScenario</span><span class="sxs-lookup"><span data-stu-id="161b3-133">protectionScenario</span></span>|<span data-ttu-id="161b3-134">Cette énumération spécifie le scénario de protection appliqué par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="161b3-134">This enumeration specifies the protection scenario enforced by the policy.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="161b3-135">Attribut clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="161b3-135">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="161b3-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="161b3-136">Value</span></span>|<span data-ttu-id="161b3-137">Description</span><span class="sxs-lookup"><span data-stu-id="161b3-137">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="161b3-138">None</span><span class="sxs-lookup"><span data-stu-id="161b3-138">None</span></span>|<span data-ttu-id="161b3-139">Les messages ne sont pas sécurisés pendant le transfert.</span><span class="sxs-lookup"><span data-stu-id="161b3-139">Messages are not secured during transfer.</span></span>|  
|<span data-ttu-id="161b3-140">Basic</span><span class="sxs-lookup"><span data-stu-id="161b3-140">Basic</span></span>|<span data-ttu-id="161b3-141">Spécifie l'authentification de base.</span><span class="sxs-lookup"><span data-stu-id="161b3-141">Specifies basic authentication.</span></span>|  
|<span data-ttu-id="161b3-142">Digest</span><span class="sxs-lookup"><span data-stu-id="161b3-142">Digest</span></span>|<span data-ttu-id="161b3-143">Spécifie l'authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="161b3-143">Specifies digest authentication.</span></span>|  
|<span data-ttu-id="161b3-144">Ntlm</span><span class="sxs-lookup"><span data-stu-id="161b3-144">Ntlm</span></span>|<span data-ttu-id="161b3-145">Spécifie l'authentification NTLM le cas échéant et en cas d'échec d'authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="161b3-145">Specifies NTLM authentication when possible, and if Windows authentication fails.</span></span>|  
|<span data-ttu-id="161b3-146">Windows</span><span class="sxs-lookup"><span data-stu-id="161b3-146">Windows</span></span>|<span data-ttu-id="161b3-147">Spécifie l'authentification intégrée Windows.</span><span class="sxs-lookup"><span data-stu-id="161b3-147">Specifies Windows integrated authentication.</span></span>|  
  
## <a name="proxycredentialtype-attribute"></a><span data-ttu-id="161b3-148">Attribut proxyCredentialType</span><span class="sxs-lookup"><span data-stu-id="161b3-148">proxyCredentialType Attribute</span></span>  
  
|<span data-ttu-id="161b3-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="161b3-149">Value</span></span>|<span data-ttu-id="161b3-150">Description</span><span class="sxs-lookup"><span data-stu-id="161b3-150">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="161b3-151">Aucun.</span><span class="sxs-lookup"><span data-stu-id="161b3-151">None</span></span>|<span data-ttu-id="161b3-152">-Les messages ne sont pas sécurisés pendant le transfert.</span><span class="sxs-lookup"><span data-stu-id="161b3-152">-   Messages are not secured during transfer.</span></span>|  
|<span data-ttu-id="161b3-153">Basic</span><span class="sxs-lookup"><span data-stu-id="161b3-153">Basic</span></span>|<span data-ttu-id="161b3-154">Spécifie l’authentification de base tel que défini par RFC 2617 – HTTP Authentication : Base et authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="161b3-154">Specifies basic authentication as defined by RFC 2617 – HTTP Authentication: Basic and Digest Authentication.</span></span>|  
|<span data-ttu-id="161b3-155">Digest</span><span class="sxs-lookup"><span data-stu-id="161b3-155">Digest</span></span>|<span data-ttu-id="161b3-156">Spécifie l’authentification digest, comme défini par RFC 2617 – HTTP Authentication : Base et authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="161b3-156">Specifies digest authentication as defined by RFC 2617 – HTTP Authentication: Basic and Digest Authentication.</span></span>|  
|<span data-ttu-id="161b3-157">Ntlm</span><span class="sxs-lookup"><span data-stu-id="161b3-157">Ntlm</span></span>|<span data-ttu-id="161b3-158">Spécifie l'authentification NTLM le cas échéant et en cas d'échec d'authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="161b3-158">Specifies NTLM authentication when possible, and if Windows authentication fails.</span></span>|  
|<span data-ttu-id="161b3-159">Windows</span><span class="sxs-lookup"><span data-stu-id="161b3-159">Windows</span></span>|<span data-ttu-id="161b3-160">Spécifie l'authentification intégrée Windows.</span><span class="sxs-lookup"><span data-stu-id="161b3-160">Specifies Windows integrated authentication.</span></span>|  
|<span data-ttu-id="161b3-161">Certificat</span><span class="sxs-lookup"><span data-stu-id="161b3-161">Certificate</span></span>|<span data-ttu-id="161b3-162">Effectue l'authentification du client à l'aide d'un certificat.</span><span class="sxs-lookup"><span data-stu-id="161b3-162">Performs client authentication using a certificate.</span></span> <span data-ttu-id="161b3-163">Cette option fonctionne uniquement si l'attribut `Mode` de l'élément `security` parent est configuré pour le transport et ne fonctionnera pas s'il a la valeur TransportCredentialOnly.</span><span class="sxs-lookup"><span data-stu-id="161b3-163">This option works only if the `Mode` attribute of the parent `security` element is set to Transport, and will not work if it is set to TransportCredentialOnly.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="161b3-164">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="161b3-164">Child Elements</span></span>  
 <span data-ttu-id="161b3-165">Aucun.</span><span class="sxs-lookup"><span data-stu-id="161b3-165">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="161b3-166">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="161b3-166">Parent Elements</span></span>  
  
|<span data-ttu-id="161b3-167">Élément</span><span class="sxs-lookup"><span data-stu-id="161b3-167">Element</span></span>|<span data-ttu-id="161b3-168">Description</span><span class="sxs-lookup"><span data-stu-id="161b3-168">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="161b3-169">\<security></span><span class="sxs-lookup"><span data-stu-id="161b3-169">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-nethttpbinding.md)|<span data-ttu-id="161b3-170">Définit les fonctionnalités de sécurité pour le [ \<netHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/nethttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="161b3-170">Defines the security capabilities for the [\<netHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/nethttpbinding.md).</span></span>|  
  
## <a name="example"></a><span data-ttu-id="161b3-171">Exemple</span><span class="sxs-lookup"><span data-stu-id="161b3-171">Example</span></span>  
 <span data-ttu-id="161b3-172">L’exemple suivant montre l’utilisation de la sécurité de transport SSL avec la liaison de base.</span><span class="sxs-lookup"><span data-stu-id="161b3-172">The following example demonstrates the use of SSL transport security with the basic binding.</span></span> <span data-ttu-id="161b3-173">Par défaut, la liaison de base prend en charge la communication HTTP.</span><span class="sxs-lookup"><span data-stu-id="161b3-173">By default, the basic binding supports HTTP communication.</span></span>  
  
```xml  
<system.serviceModel>
  <services>
    <service type="Microsoft.ServiceModel.Samples.CalculatorService"
             behaviorConfiguration="CalculatorServiceBehavior">
      <endpoint address=""
                binding="netHttpBinding"
                bindingConfiguration="Binding1"
                contract="Microsoft.ServiceModel.Samples.ICalculator" />
    </service>
  </services>
  <bindings>
    <netHttpBinding>
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
    </netHttpBinding>
  </bindings>
</system.serviceModel>
```  
  
## <a name="see-also"></a><span data-ttu-id="161b3-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="161b3-174">See also</span></span>
- <xref:System.ServiceModel.BasicHttpSecurityMode.Transport>
- <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement>
- <xref:System.ServiceModel.HttpTransportSecurity>
- [<span data-ttu-id="161b3-175">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="161b3-175">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="161b3-176">Liaisons</span><span class="sxs-lookup"><span data-stu-id="161b3-176">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="161b3-177">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="161b3-177">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="161b3-178">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="161b3-178">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="161b3-179">\<binding></span><span class="sxs-lookup"><span data-stu-id="161b3-179">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
