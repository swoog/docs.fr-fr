---
title: '&lt;transport&gt; de &lt;netTcpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 49462e0a-66e1-463f-b3e1-c83a441673c6
ms.openlocfilehash: 8c2a0de73db2ec4a1c2150fc7e62b7a3a9f086bc
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43515050"
---
# <a name="lttransportgt-of-ltnettcpbindinggt"></a><span data-ttu-id="5ccd3-102">&lt;transport&gt; de &lt;netTcpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="5ccd3-102">&lt;transport&gt; of &lt;netTcpBinding&gt;</span></span>
<span data-ttu-id="5ccd3-103">Définit le type d’exigences de sécurité au niveau du message pour un point de terminaison configuré avec le [ \<netTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/nettcpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="5ccd3-103">Defines the type of message-level security requirements for an endpoint configured with the [\<netTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/nettcpbinding.md).</span></span>  
  
 <span data-ttu-id="5ccd3-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="5ccd3-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="5ccd3-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="5ccd3-105">\<bindings></span></span>  
<span data-ttu-id="5ccd3-106">\<netTcpBinding></span><span class="sxs-lookup"><span data-stu-id="5ccd3-106">\<netTcpBinding></span></span>  
<span data-ttu-id="5ccd3-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="5ccd3-107">\<binding></span></span>  
<span data-ttu-id="5ccd3-108">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="5ccd3-108">\<security></span></span>  
<span data-ttu-id="5ccd3-109">\<transport ></span><span class="sxs-lookup"><span data-stu-id="5ccd3-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5ccd3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ccd3-110">Syntax</span></span>  
  
```xml  
<netTcpBinding>  
    <binding>  
        <security  
         mode="None|Transport|Message|TransportWithMessageCredential">  
            <transport clientCredentialType="None|Windows|Certificate"  
             protectionLevel="None|Sign|EncryptAndSign"             sslProtocols="Tls|Tls11|Tls12">  
                <extendedProtectionPolicy  
                     policyEnforcement="Never|WhenSupported|Always"  
                     protectionScenario="TransportSelected|TrustedProxy">  
                    <customServiceNames></customServiceNames>  
                        </extendedProtectionPolicy>  
            </transport>  
        </security>  
    </binding>  
</netTcpBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5ccd3-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5ccd3-111">Attributes and Elements</span></span>  
 <span data-ttu-id="5ccd3-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5ccd3-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="5ccd3-113">Attributes</span></span>  
  
|<span data-ttu-id="5ccd3-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="5ccd3-114">Attribute</span></span>|<span data-ttu-id="5ccd3-115">Description</span><span class="sxs-lookup"><span data-stu-id="5ccd3-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5ccd3-116">clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="5ccd3-116">clientCredentialType</span></span>|<span data-ttu-id="5ccd3-117">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-117">Optional.</span></span> <span data-ttu-id="5ccd3-118">Spécifie le type d'informations d'identification à utiliser lors de l'authentification du client à l'aide de la sécurité de transport.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-118">Specifies the type of credential to be used when performing client authentication using Transport security.</span></span><br /><br /> <span data-ttu-id="5ccd3-119">-La valeur par défaut est `Windows`.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-119">-   The default value is `Windows`.</span></span><br /><span data-ttu-id="5ccd3-120">-Cet attribut est de type <xref:System.ServiceModel.TcpClientCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-120">-   This attribute is of type <xref:System.ServiceModel.TcpClientCredentialType>.</span></span>|  
|<span data-ttu-id="5ccd3-121">protectionLevel</span><span class="sxs-lookup"><span data-stu-id="5ccd3-121">protectionLevel</span></span>|<span data-ttu-id="5ccd3-122">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-122">Optional.</span></span> <span data-ttu-id="5ccd3-123">Définit la sécurité au niveau du transport TCP.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-123">Defines security at the level of the TCP transport.</span></span> <span data-ttu-id="5ccd3-124">La signature des messages atténue le risque de modification par un tiers pendant le transfert.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-124">Signing messages mitigates the risk of a third party tampering with the message while it is being transferred.</span></span> <span data-ttu-id="5ccd3-125">Le chiffrement garantit la confidentialité des données pendant le transport.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-125">Encryption provides data-level privacy during transport.</span></span><br /><br /> <span data-ttu-id="5ccd3-126">La valeur par défaut est `EncryptAndSign`.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-126">The default value is `EncryptAndSign`.</span></span>|  
|<span data-ttu-id="5ccd3-127">sslProtocols</span><span class="sxs-lookup"><span data-stu-id="5ccd3-127">sslProtocols</span></span>|<span data-ttu-id="5ccd3-128">Valeur d'indicateur d'énumération SslProtocols qui spécifie les protocoles SSL pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-128">A SslProtocols enum flag value that specifies which SslProtocols are supported.</span></span> <span data-ttu-id="5ccd3-129">La valeur par défaut est Tls&#124;Tls11&#124;Tls12.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-129">The default is Tls&#124;Tls11&#124;Tls12.</span></span>|  
|<span data-ttu-id="5ccd3-130">policyEnforcement</span><span class="sxs-lookup"><span data-stu-id="5ccd3-130">policyEnforcement</span></span>|<span data-ttu-id="5ccd3-131">Cette énumération spécifie à quel moment <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> doit être appliqué.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-131">This enumeration specifies when the <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> should be enforced.</span></span><br /><br /> <span data-ttu-id="5ccd3-132">1.  Never : la stratégie n'est jamais appliquée (la protection étendue est désactivée).</span><span class="sxs-lookup"><span data-stu-id="5ccd3-132">1.  Never – The policy is never enforced (Extended Protection is disabled).</span></span><br /><span data-ttu-id="5ccd3-133">2.  WhenSupported : la stratégie est appliquée uniquement si le client prend en charge la protection étendue.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-133">2.  WhenSupported – The policy is enforced only if the client supports Extended Protection.</span></span><br /><span data-ttu-id="5ccd3-134">3.  Always : la stratégie est toujours appliquée.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-134">3.  Always – The policy is always enforced.</span></span> <span data-ttu-id="5ccd3-135">Les clients qui ne prennent pas en charge la protection étendue ne pourront pas être authentifiés.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-135">Clients which don’t support Extended Protection will fail to authenticate.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="5ccd3-136">Attribut clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="5ccd3-136">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="5ccd3-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ccd3-137">Value</span></span>|<span data-ttu-id="5ccd3-138">Description</span><span class="sxs-lookup"><span data-stu-id="5ccd3-138">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="5ccd3-139">None</span><span class="sxs-lookup"><span data-stu-id="5ccd3-139">None</span></span>|<span data-ttu-id="5ccd3-140">Le client est anonyme.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-140">The client is anonymous.</span></span> <span data-ttu-id="5ccd3-141">Cela requiert un certificat pour le service.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-141">This requires a certificate for the service.</span></span>|  
|<span data-ttu-id="5ccd3-142">Windows</span><span class="sxs-lookup"><span data-stu-id="5ccd3-142">Windows</span></span>|<span data-ttu-id="5ccd3-143">Spécifie l'authentification Windows du client à l'aide de la négociation SP (négociation Kerberos).</span><span class="sxs-lookup"><span data-stu-id="5ccd3-143">Specifies Windows authentication of the client using SP Negotiation (Kerberos negotiation).</span></span>|  
|<span data-ttu-id="5ccd3-144">Certificat</span><span class="sxs-lookup"><span data-stu-id="5ccd3-144">Certificate</span></span>|<span data-ttu-id="5ccd3-145">Le client est authentifié à l'aide d'un certificat.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-145">The client is authenticated using a certificate.</span></span> <span data-ttu-id="5ccd3-146">Cette valeur utilise la négociation SSL et requiert un certificat pour le service.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-146">This uses SSL Negotiation and requires a certificate for the service.</span></span>|  
  
## <a name="protectionlevel-attribute"></a><span data-ttu-id="5ccd3-147">protectionLevel, attribut</span><span class="sxs-lookup"><span data-stu-id="5ccd3-147">protectionLevel Attribute</span></span>  
  
|<span data-ttu-id="5ccd3-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ccd3-148">Value</span></span>|<span data-ttu-id="5ccd3-149">Description</span><span class="sxs-lookup"><span data-stu-id="5ccd3-149">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="5ccd3-150">None</span><span class="sxs-lookup"><span data-stu-id="5ccd3-150">None</span></span>|<span data-ttu-id="5ccd3-151">Aucune protection.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-151">No protection.</span></span>|  
|<span data-ttu-id="5ccd3-152">Sign</span><span class="sxs-lookup"><span data-stu-id="5ccd3-152">Sign</span></span>|<span data-ttu-id="5ccd3-153">Les messages sont signés.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-153">Messages are signed.</span></span>|  
|<span data-ttu-id="5ccd3-154">EncryptAndSign</span><span class="sxs-lookup"><span data-stu-id="5ccd3-154">EncryptAndSign</span></span>|<span data-ttu-id="5ccd3-155">-Les messages sont chiffrés et signés.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-155">-   Messages are encrypted and signed.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5ccd3-156">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5ccd3-156">Child Elements</span></span>  
 <span data-ttu-id="5ccd3-157">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-157">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5ccd3-158">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5ccd3-158">Parent Elements</span></span>  
  
|<span data-ttu-id="5ccd3-159">Élément</span><span class="sxs-lookup"><span data-stu-id="5ccd3-159">Element</span></span>|<span data-ttu-id="5ccd3-160">Description</span><span class="sxs-lookup"><span data-stu-id="5ccd3-160">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5ccd3-161">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="5ccd3-161">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-nettcpbinding.md)|<span data-ttu-id="5ccd3-162">Spécifie les fonctionnalités de sécurité le [ \<netTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/nettcpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="5ccd3-162">Specifies the security capabilities of the [\<netTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/nettcpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5ccd3-163">Notes</span><span class="sxs-lookup"><span data-stu-id="5ccd3-163">Remarks</span></span>  
 <span data-ttu-id="5ccd3-164">Utilisez la sécurité de transport pour l'intégrité et la confidentialité du message SOAP et l'authentification mutuelle.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-164">Use Transport security for integrity and confidentiality of the SOAP message and for mutual authentication.</span></span> <span data-ttu-id="5ccd3-165">Si ce mode de sécurité est sélectionné sur une liaison, la pile de canaux est configurée à l’aide d’un transport sécurisé et les messages SOAP sont sécurisés à l’aide d’une sécurité de transport, telle que Windows (Negotiate) ou SSL sur TCP.</span><span class="sxs-lookup"><span data-stu-id="5ccd3-165">If this security mode is selected on a binding, the channel stack is configured using a secure transport and the SOAP messages are secured using transport security such as Windows (Negotiate) or SSL over TCP.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5ccd3-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ccd3-166">See Also</span></span>  
 <xref:System.ServiceModel.TcpTransportSecurity>  
 <xref:System.ServiceModel.Configuration.NetTcpSecurityElement.Transport%2A>  
 <xref:System.ServiceModel.NetTcpSecurity.Transport%2A>  
 <xref:System.ServiceModel.Configuration.NetTcpSecurityElement>  
 [<span data-ttu-id="5ccd3-167">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="5ccd3-167">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="5ccd3-168">Liaisons</span><span class="sxs-lookup"><span data-stu-id="5ccd3-168">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="5ccd3-169">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="5ccd3-169">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="5ccd3-170">Utilisation de liaisons pour configurer les Clients et les Services Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="5ccd3-170">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="5ccd3-171">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="5ccd3-171">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
