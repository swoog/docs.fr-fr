---
title: '&lt;security&gt; de &lt;msmqIntegrationBinding&gt;'
ms.date: 03/30/2017
ms.assetid: ae5c68a8-14a2-4c6e-b9e0-3e94e3e9135e
ms.openlocfilehash: a0c6e016980b5a40d74b9bd94dab96a0aa9fb243
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145274"
---
# <a name="ltsecuritygt-of-ltmsmqintegrationbindinggt"></a><span data-ttu-id="5dd99-102">&lt;security&gt; de &lt;msmqIntegrationBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="5dd99-102">&lt;security&gt; of &lt;msmqIntegrationBinding&gt;</span></span>
<span data-ttu-id="5dd99-103">Définit les paramètres de sécurité de transport pour le canal d'intégration MSMQ (Message Queuing).</span><span class="sxs-lookup"><span data-stu-id="5dd99-103">Defines the transport security settings for the Message Queuing (MSMQ) integration channel.</span></span>  
  
 <span data-ttu-id="5dd99-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="5dd99-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="5dd99-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="5dd99-105">\<bindings></span></span>  
<span data-ttu-id="5dd99-106">msmqIntegrationBinding</span><span class="sxs-lookup"><span data-stu-id="5dd99-106">msmqIntegrationBinding</span></span>  
<span data-ttu-id="5dd99-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="5dd99-107">\<binding></span></span>  
<span data-ttu-id="5dd99-108">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="5dd99-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5dd99-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5dd99-109">Syntax</span></span>  
  
```xml  
<msmqIntegrationBinding>
  <binding>
    <security mode="None/Transport">
      <transport msmqAuthenticationMode="None/Windows/Certificate"
                 msmqEncryptionAlgorithm="RC4Stream/AES"
                 msmqProtectionLevel="None/Sign/EncryptAndSign"
                 msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />
      <message algorithmSuite="Aes128/Aes192/Aes256/Rsa15Aes128/ Rsa15Aes256/TripleDes"
               clientCredentialType="None/Windows/UserName/Certificate/CardSpace"
               defaultProtectionLevel="None/Sign/EncryptAndSign" />
    </security>
  </binding>
</msmqIntegrationBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5dd99-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5dd99-110">Attributes and Elements</span></span>  
 <span data-ttu-id="5dd99-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5dd99-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5dd99-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="5dd99-112">Attributes</span></span>  
  
|<span data-ttu-id="5dd99-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="5dd99-113">Attribute</span></span>|<span data-ttu-id="5dd99-114">Description</span><span class="sxs-lookup"><span data-stu-id="5dd99-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5dd99-115">mode</span><span class="sxs-lookup"><span data-stu-id="5dd99-115">mode</span></span>|<span data-ttu-id="5dd99-116">Spécifie le type de sécurité qui contrôle l'intégrité, la confidentialité et l'authentification avec le canal d'intégration Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="5dd99-116">Specifies the type of security that controls integrity, confidentiality and authentication with the Message Queuing integration channel.</span></span> <span data-ttu-id="5dd99-117">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5dd99-117">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="5dd99-118">-None : Cela désactive la sécurité.</span><span class="sxs-lookup"><span data-stu-id="5dd99-118">-   None: This disables security.</span></span><br /><span data-ttu-id="5dd99-119">-Transport : Protection et l’authentification sont offertes par le transport.</span><span class="sxs-lookup"><span data-stu-id="5dd99-119">-   Transport: Protection and authentication are offered by the transport.</span></span> <span data-ttu-id="5dd99-120">Cela s'applique à la sécurité des message entre les deux gestionnaires de files d'attente.</span><span class="sxs-lookup"><span data-stu-id="5dd99-120">This applies to the message security between the two queue managers.</span></span> <span data-ttu-id="5dd99-121">Il n'y a aucune sécurité offerte entre l'application et gestionnaire de files d'attente.</span><span class="sxs-lookup"><span data-stu-id="5dd99-121">There is no security offered between the application and queue manager.</span></span> <span data-ttu-id="5dd99-122">Les applications Msmq existantes sont équivalentes au niveau des fonctionnalités avec ce type de mode de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5dd99-122">Existing Msmq applications are functionally equivalent with this type of security mode.</span></span><br /><br /> <span data-ttu-id="5dd99-123">La valeur par défaut est `Transport`.</span><span class="sxs-lookup"><span data-stu-id="5dd99-123">The default value is `Transport`.</span></span> <span data-ttu-id="5dd99-124">Cet attribut est de type <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurityMode>.</span><span class="sxs-lookup"><span data-stu-id="5dd99-124">This attribute is of type <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurityMode>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5dd99-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5dd99-125">Child Elements</span></span>  
  
|<span data-ttu-id="5dd99-126">Élément</span><span class="sxs-lookup"><span data-stu-id="5dd99-126">Element</span></span>|<span data-ttu-id="5dd99-127">Description</span><span class="sxs-lookup"><span data-stu-id="5dd99-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5dd99-128">\<transport></span><span class="sxs-lookup"><span data-stu-id="5dd99-128">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-msmqintegrationbinding.md)|<span data-ttu-id="5dd99-129">Définit les paramètres de sécurité pour le transport d'intégration Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="5dd99-129">Defines the security settings for the Message Queuing integration transport.</span></span> <span data-ttu-id="5dd99-130">Cet élément est de type <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>.</span><span class="sxs-lookup"><span data-stu-id="5dd99-130">This element is of type <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5dd99-131">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5dd99-131">Parent Elements</span></span>  
  
|<span data-ttu-id="5dd99-132">Élément</span><span class="sxs-lookup"><span data-stu-id="5dd99-132">Element</span></span>|<span data-ttu-id="5dd99-133">Description</span><span class="sxs-lookup"><span data-stu-id="5dd99-133">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5dd99-134">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="5dd99-134">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="5dd99-135">L’élément de liaison de la [ \<msmqIntegrationBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/msmqintegrationbinding.md).</span><span class="sxs-lookup"><span data-stu-id="5dd99-135">The binding element of the [\<msmqIntegrationBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/msmqintegrationbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5dd99-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dd99-136">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.MsmqIntegrationSecurityElement>  
 <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.MsmqIntegrationBindingElement.Security%2A>  
 <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurity>  
 [<span data-ttu-id="5dd99-137">Files d’attente dans WCF</span><span class="sxs-lookup"><span data-stu-id="5dd99-137">Queues in WCF</span></span>](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)  
 [<span data-ttu-id="5dd99-138">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="5dd99-138">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="5dd99-139">Liaisons</span><span class="sxs-lookup"><span data-stu-id="5dd99-139">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="5dd99-140">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="5dd99-140">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="5dd99-141">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="5dd99-141">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="5dd99-142">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="5dd99-142">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)  
 [<span data-ttu-id="5dd99-143">\<msmqIntegrationBinding></span><span class="sxs-lookup"><span data-stu-id="5dd99-143">\<msmqIntegrationBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/msmqintegrationbinding.md)
