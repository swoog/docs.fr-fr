---
title: '&lt;security&gt; de &lt;msmqIntegrationBinding&gt;'
ms.date: 03/30/2017
ms.assetid: ae5c68a8-14a2-4c6e-b9e0-3e94e3e9135e
author: BrucePerlerMS
ms.openlocfilehash: 3f0810a705b5f46ee68a891f9b4ced42efdcb757
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47077589"
---
# <a name="ltsecuritygt-of-ltmsmqintegrationbindinggt"></a><span data-ttu-id="8c6b6-102">&lt;security&gt; de &lt;msmqIntegrationBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="8c6b6-102">&lt;security&gt; of &lt;msmqIntegrationBinding&gt;</span></span>
<span data-ttu-id="8c6b6-103">Définit les paramètres de sécurité de transport pour le canal d'intégration MSMQ (Message Queuing).</span><span class="sxs-lookup"><span data-stu-id="8c6b6-103">Defines the transport security settings for the Message Queuing (MSMQ) integration channel.</span></span>  
  
 <span data-ttu-id="8c6b6-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="8c6b6-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="8c6b6-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="8c6b6-105">\<bindings></span></span>  
<span data-ttu-id="8c6b6-106">msmqIntegrationBinding</span><span class="sxs-lookup"><span data-stu-id="8c6b6-106">msmqIntegrationBinding</span></span>  
<span data-ttu-id="8c6b6-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="8c6b6-107">\<binding></span></span>  
<span data-ttu-id="8c6b6-108">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="8c6b6-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8c6b6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c6b6-109">Syntax</span></span>  
  
```xml  
<msmqIntegrationBinding>  
   <binding>   
       <security mode="None/Transport">  
         <transport msmqAuthenticationMode="None/Windows/Certificate"  
            msmqEncryptionAlgorithm="RC4Stream/AES"  
            msmqProtectionLevel="None/Sign/EncryptAndSign"  
            msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />  
          <message  algorithmSuite="Aes128/Aes192/Aes256/Rsa15Aes128/ Rsa15Aes256/TripleDes"  
                        clientCredentialType="None/Windows/UserName/Certificate/CardSpace"  
            defaultProtectionLevel="None/Sign/EncryptAndSign" />  
       </security>  
   </binding>  
</msmqIntegrationBinding>   
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8c6b6-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="8c6b6-110">Attributes and Elements</span></span>  
 <span data-ttu-id="8c6b6-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8c6b6-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="8c6b6-112">Attributes</span></span>  
  
|<span data-ttu-id="8c6b6-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="8c6b6-113">Attribute</span></span>|<span data-ttu-id="8c6b6-114">Description</span><span class="sxs-lookup"><span data-stu-id="8c6b6-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="8c6b6-115">mode</span><span class="sxs-lookup"><span data-stu-id="8c6b6-115">mode</span></span>|<span data-ttu-id="8c6b6-116">Spécifie le type de sécurité qui contrôle l'intégrité, la confidentialité et l'authentification avec le canal d'intégration Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-116">Specifies the type of security that controls integrity, confidentiality and authentication with the Message Queuing integration channel.</span></span> <span data-ttu-id="8c6b6-117">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c6b6-117">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="8c6b6-118">-None : Sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-118">-   None: This disables security.</span></span><br /><span data-ttu-id="8c6b6-119">-Transport : Protection et l’authentification sont offertes par le transport.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-119">-   Transport: Protection and authentication are offered by the transport.</span></span> <span data-ttu-id="8c6b6-120">Cela s'applique à la sécurité des message entre les deux gestionnaires de files d'attente.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-120">This applies to the message security between the two queue managers.</span></span> <span data-ttu-id="8c6b6-121">Il n'y a aucune sécurité offerte entre l'application et gestionnaire de files d'attente.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-121">There is no security offered between the application and queue manager.</span></span> <span data-ttu-id="8c6b6-122">Les applications Msmq existantes sont équivalentes au niveau des fonctionnalités avec ce type de mode de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-122">Existing Msmq applications are functionally equivalent with this type of security mode.</span></span><br /><br /> <span data-ttu-id="8c6b6-123">La valeur par défaut est `Transport`.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-123">The default value is `Transport`.</span></span> <span data-ttu-id="8c6b6-124">Cet attribut est de type <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurityMode>.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-124">This attribute is of type <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurityMode>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8c6b6-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8c6b6-125">Child Elements</span></span>  
  
|<span data-ttu-id="8c6b6-126">Élément</span><span class="sxs-lookup"><span data-stu-id="8c6b6-126">Element</span></span>|<span data-ttu-id="8c6b6-127">Description</span><span class="sxs-lookup"><span data-stu-id="8c6b6-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8c6b6-128">\<transport></span><span class="sxs-lookup"><span data-stu-id="8c6b6-128">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-msmqintegrationbinding.md)|<span data-ttu-id="8c6b6-129">Définit les paramètres de sécurité pour le transport d'intégration Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-129">Defines the security settings for the Message Queuing integration transport.</span></span> <span data-ttu-id="8c6b6-130">Cet élément est de type <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-130">This element is of type <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="8c6b6-131">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8c6b6-131">Parent Elements</span></span>  
  
|<span data-ttu-id="8c6b6-132">Élément</span><span class="sxs-lookup"><span data-stu-id="8c6b6-132">Element</span></span>|<span data-ttu-id="8c6b6-133">Description</span><span class="sxs-lookup"><span data-stu-id="8c6b6-133">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8c6b6-134">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="8c6b6-134">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="8c6b6-135">L’élément de liaison de la [ \<msmqIntegrationBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/msmqintegrationbinding.md).</span><span class="sxs-lookup"><span data-stu-id="8c6b6-135">The binding element of the [\<msmqIntegrationBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/msmqintegrationbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8c6b6-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c6b6-136">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.MsmqIntegrationSecurityElement>  
 <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.MsmqIntegrationBindingElement.Security%2A>  
 <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurity>  
 [<span data-ttu-id="8c6b6-137">Files d’attente dans WCF</span><span class="sxs-lookup"><span data-stu-id="8c6b6-137">Queues in WCF</span></span>](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)  
 [<span data-ttu-id="8c6b6-138">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="8c6b6-138">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="8c6b6-139">Liaisons</span><span class="sxs-lookup"><span data-stu-id="8c6b6-139">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="8c6b6-140">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="8c6b6-140">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="8c6b6-141">Utilisation de liaisons pour configurer les Clients et les Services Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="8c6b6-141">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="8c6b6-142">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="8c6b6-142">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)  
 [<span data-ttu-id="8c6b6-143">\<msmqIntegrationBinding></span><span class="sxs-lookup"><span data-stu-id="8c6b6-143">\<msmqIntegrationBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/msmqintegrationbinding.md)
