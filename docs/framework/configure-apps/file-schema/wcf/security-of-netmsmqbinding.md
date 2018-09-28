---
title: '&lt;security&gt; de &lt;netMsmqBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 001d11a9-7439-498c-b09d-fca20eaf8cd3
author: BrucePerlerMS
ms.openlocfilehash: 40f0e72069e96d3c0f28e708d67e8777e18e2b1f
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47402537"
---
# <a name="ltsecuritygt-of-ltnetmsmqbindinggt"></a><span data-ttu-id="cc4cd-102">&lt;security&gt; de &lt;netMsmqBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="cc4cd-102">&lt;security&gt; of &lt;netMsmqBinding&gt;</span></span>
<span data-ttu-id="cc4cd-103">Définit les paramètres de sécurité pour une liaison MSMQ.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-103">Defines the security settings for a MSMQ binding.</span></span> <span data-ttu-id="cc4cd-104">Elle spécifie si le transport ou la sécurité SOAP sont activés et, si c'est le cas, le mode d'authentification et les niveaux de protection utilisés.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-104">It specifies whether transport or SOAP security is enabled and, if so, what authentication mode and protection levels are in use.</span></span>  
  
 <span data-ttu-id="cc4cd-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="cc4cd-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="cc4cd-106">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="cc4cd-106">\<bindings></span></span>  
<span data-ttu-id="cc4cd-107">\<netMsmqBinding></span><span class="sxs-lookup"><span data-stu-id="cc4cd-107">\<netMsmqBinding></span></span>  
<span data-ttu-id="cc4cd-108">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="cc4cd-108">\<binding></span></span>  
<span data-ttu-id="cc4cd-109">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="cc4cd-109">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc4cd-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc4cd-110">Syntax</span></span>  
  
```xml  
<security mode="None/Transport/Message/Both">  
   <transport msmqAuthenticationMode="None/WindowsDomain/Certificate"  
      msmqEncryptionAlgorithm="RC4Stream/AES"  
      msmqProtectionLevel="None/Sign/EncryptAndSign"  
      msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />  
      <message  
      algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
      clientCredentialType="None/Windows/UserName/Certificate/CardSpace"/>  
</security>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cc4cd-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="cc4cd-111">Attributes and Elements</span></span>  
 <span data-ttu-id="cc4cd-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cc4cd-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="cc4cd-113">Attributes</span></span>  
  
|<span data-ttu-id="cc4cd-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="cc4cd-114">Attribute</span></span>|<span data-ttu-id="cc4cd-115">Description</span><span class="sxs-lookup"><span data-stu-id="cc4cd-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="cc4cd-116">mode</span><span class="sxs-lookup"><span data-stu-id="cc4cd-116">mode</span></span>|<span data-ttu-id="cc4cd-117">Spécifie le type de sécurité qui contrôle l'intégrité, la confidentialité et l'authentification.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-117">Specifies the type of security that controls integrity, confidentiality and authentication.</span></span> <span data-ttu-id="cc4cd-118">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="cc4cd-118">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="cc4cd-119">-None : Sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-119">-   None: This disables security.</span></span><br /><span data-ttu-id="cc4cd-120">-Transport : Protection et l’authentification sont offertes par le transport.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-120">-   Transport: Protection and authentication are offered by the transport.</span></span> <span data-ttu-id="cc4cd-121">Cela s'applique à la sécurité des message entre les deux gestionnaires de files d'attente.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-121">This applies to the message security between the two queue managers.</span></span> <span data-ttu-id="cc4cd-122">Il n'y a aucune sécurité offerte entre l'application et gestionnaire de files d'attente.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-122">There is no security offered between the application and queue manager.</span></span> <span data-ttu-id="cc4cd-123">Les applications Msmq existantes sont équivalentes au niveau des fonctionnalités avec ce type de mode de sécurité.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-123">Existing Msmq applications are functionally equivalent with this type of security mode.</span></span><br /><span data-ttu-id="cc4cd-124">-Message : Spécifie la sécurité de l’application de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-124">-   Message: Specifies end-end application security.</span></span> <span data-ttu-id="cc4cd-125">Il n'y a aucune sécurité offerte à la couche de transport.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-125">There is no security offered at the transport layer.</span></span> <span data-ttu-id="cc4cd-126">Cette valeur est semblable à la sécurité offerte par d'autres liaisons standard.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-126">This is similar to the security offered by other standard bindings.</span></span><br /><span data-ttu-id="cc4cd-127">-Both : Offre la sécurité au niveau du transport et la couche de messagerie SOAP.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-127">-   Both: Offers security at both the transport and SOAP messaging layer.</span></span> <span data-ttu-id="cc4cd-128">La même information d'identification est requise pour les deux niveaux.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-128">The same credential is required at both the levels.</span></span><br /><br /> <span data-ttu-id="cc4cd-129">La valeur par défaut est Transport.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-129">The default value is Transport.</span></span> <span data-ttu-id="cc4cd-130">Cet attribut est de type <xref:System.ServiceModel.NetMsmqSecurityMode>.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-130">This attribute is of type <xref:System.ServiceModel.NetMsmqSecurityMode>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cc4cd-131">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cc4cd-131">Child Elements</span></span>  
  
|<span data-ttu-id="cc4cd-132">Élément</span><span class="sxs-lookup"><span data-stu-id="cc4cd-132">Element</span></span>|<span data-ttu-id="cc4cd-133">Description</span><span class="sxs-lookup"><span data-stu-id="cc4cd-133">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cc4cd-134">\<message></span><span class="sxs-lookup"><span data-stu-id="cc4cd-134">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-of-netmsmqbinding.md)|<span data-ttu-id="cc4cd-135">Définit le les paramètres de sécurité des messages SOAP.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-135">Defines the SOAP message security settings.</span></span> <span data-ttu-id="cc4cd-136">Cet élément est de type <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement>.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-136">This element is of type <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement>.</span></span>|  
|[<span data-ttu-id="cc4cd-137">\<transport></span><span class="sxs-lookup"><span data-stu-id="cc4cd-137">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-netmsmqbinding.md)|<span data-ttu-id="cc4cd-138">Définit les paramètres de sécurité pour le transport MSMQ.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-138">Defines the security settings for the MSMQ transport.</span></span> <span data-ttu-id="cc4cd-139">Cet élément est de type <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-139">This element is of type <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="cc4cd-140">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="cc4cd-140">Parent Elements</span></span>  
  
|<span data-ttu-id="cc4cd-141">Élément</span><span class="sxs-lookup"><span data-stu-id="cc4cd-141">Element</span></span>|<span data-ttu-id="cc4cd-142">Description</span><span class="sxs-lookup"><span data-stu-id="cc4cd-142">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="cc4cd-143">liaison</span><span class="sxs-lookup"><span data-stu-id="cc4cd-143">binding</span></span>|<span data-ttu-id="cc4cd-144">L’élément de liaison de la [ \<netMsmqBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netmsmqbinding.md)</span><span class="sxs-lookup"><span data-stu-id="cc4cd-144">The binding element of the [\<netMsmqBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netmsmqbinding.md)</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="cc4cd-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc4cd-145">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement>  
 <xref:System.ServiceModel.NetMsmqBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.NetMsmqBindingElement.Security%2A>  
 <xref:System.ServiceModel.NetMsmqSecurity>  
 [<span data-ttu-id="cc4cd-146">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="cc4cd-146">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="cc4cd-147">Liaisons</span><span class="sxs-lookup"><span data-stu-id="cc4cd-147">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="cc4cd-148">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="cc4cd-148">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="cc4cd-149">Utilisation de liaisons pour configurer les Clients et les Services Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="cc4cd-149">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="cc4cd-150">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="cc4cd-150">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)  
 [<span data-ttu-id="cc4cd-151">Files d’attente dans WCF</span><span class="sxs-lookup"><span data-stu-id="cc4cd-151">Queues in WCF</span></span>](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)
