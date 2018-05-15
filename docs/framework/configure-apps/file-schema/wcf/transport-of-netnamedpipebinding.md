---
title: '&lt;transport&gt; de &lt;netNamedPipeBinding&gt;'
ms.date: 03/30/2017
ms.assetid: d9eff52d-4bde-4586-b56a-b0ec24611f8d
ms.openlocfilehash: 9116532c8b4aae2f7539706b97d564444195c79d
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="lttransportgt-of-ltnetnamedpipebindinggt"></a><span data-ttu-id="64447-102">&lt;transport&gt; de &lt;netNamedPipeBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="64447-102">&lt;transport&gt; of &lt;netNamedPipeBinding&gt;</span></span>
<span data-ttu-id="64447-103">Définit les paramètres de sécurité de transport pour un canal nommé.</span><span class="sxs-lookup"><span data-stu-id="64447-103">Defines the transport security settings for a named pipe.</span></span>  
  
 <span data-ttu-id="64447-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="64447-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="64447-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="64447-105">\<bindings></span></span>  
<span data-ttu-id="64447-106">\<netNamedPipeBinding></span><span class="sxs-lookup"><span data-stu-id="64447-106">\<netNamedPipeBinding></span></span>  
<span data-ttu-id="64447-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="64447-107">\<binding></span></span>  
<span data-ttu-id="64447-108">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="64447-108">\<security></span></span>  
<span data-ttu-id="64447-109">\<transport ></span><span class="sxs-lookup"><span data-stu-id="64447-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64447-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64447-110">Syntax</span></span>  
  
```xml  
<netNamedPipeBinding>  
   <binding>  
      <security mode="None/Transport">  
            <transport protectionLevel="None/Sign/EncryptAndSign" />  
      </security>  
   </binding>  
</netNamedPipeBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="64447-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="64447-111">Attributes and Elements</span></span>  
 <span data-ttu-id="64447-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="64447-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="64447-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="64447-113">Attributes</span></span>  
  
|<span data-ttu-id="64447-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="64447-114">Attribute</span></span>|<span data-ttu-id="64447-115">Description</span><span class="sxs-lookup"><span data-stu-id="64447-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="64447-116">protectionLevel</span><span class="sxs-lookup"><span data-stu-id="64447-116">protectionLevel</span></span>|<span data-ttu-id="64447-117">Définit le niveau de protection du canal nommé.</span><span class="sxs-lookup"><span data-stu-id="64447-117">Defines protection level of the named pipe.</span></span> <span data-ttu-id="64447-118">La signature des messages atténue le risque de modification par un tiers pendant le transfert.</span><span class="sxs-lookup"><span data-stu-id="64447-118">Signing messages mitigates the risk of a third party tampering with the message while it is being transferred.</span></span> <span data-ttu-id="64447-119">Le chiffrement garantit la confidentialité des données pendant le transport.</span><span class="sxs-lookup"><span data-stu-id="64447-119">Encryption provides data-level privacy during transport.</span></span> <span data-ttu-id="64447-120">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="64447-120">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="64447-121">-None : Aucune protection.</span><span class="sxs-lookup"><span data-stu-id="64447-121">-   None: No protection.</span></span><br /><span data-ttu-id="64447-122">-Sign : Les Messages sont signés.</span><span class="sxs-lookup"><span data-stu-id="64447-122">-   Sign: Messages are signed.</span></span><br /><span data-ttu-id="64447-123">-EncryptAndSign : Les Messages sont chiffrés et signés.</span><span class="sxs-lookup"><span data-stu-id="64447-123">-   EncryptAndSign: Messages are encrypted and signed.</span></span><br /><br /> <span data-ttu-id="64447-124">La valeur par défaut est EncryptAndSign.</span><span class="sxs-lookup"><span data-stu-id="64447-124">The default value is EncryptAndSign.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="64447-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="64447-125">Child Elements</span></span>  
 <span data-ttu-id="64447-126">Aucun</span><span class="sxs-lookup"><span data-stu-id="64447-126">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="64447-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="64447-127">Parent Elements</span></span>  
  
|<span data-ttu-id="64447-128">Élément</span><span class="sxs-lookup"><span data-stu-id="64447-128">Element</span></span>|<span data-ttu-id="64447-129">Description</span><span class="sxs-lookup"><span data-stu-id="64447-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="64447-130">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="64447-130">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netnamedpipebinding.md)|<span data-ttu-id="64447-131">Définit les paramètres de sécurité d’une liaison.</span><span class="sxs-lookup"><span data-stu-id="64447-131">Defines the security settings for a binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="64447-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64447-132">See Also</span></span>  
 <xref:System.ServiceModel.NamedPipeTransportSecurity>  
 <xref:System.ServiceModel.Configuration.NetNamedPipeSecurityElement.Transport%2A>  
 <xref:System.ServiceModel.NetNamedPipeSecurity.Transport%2A>  
 <xref:System.ServiceModel.Configuration.NamedPipeTransportSecurityElement>  
 [<span data-ttu-id="64447-133">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="64447-133">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="64447-134">Liaisons</span><span class="sxs-lookup"><span data-stu-id="64447-134">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="64447-135">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="64447-135">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="64447-136">Utilisation de liaisons pour configurer les Clients et les Services Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="64447-136">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](http://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="64447-137">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="64447-137">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
