---
title: <transport> de <netNamedPipeBinding>
ms.date: 03/30/2017
ms.assetid: d9eff52d-4bde-4586-b56a-b0ec24611f8d
ms.openlocfilehash: a6d3dd2c24e90bdcdc6520e62dcc1dbe7ce797f9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59199822"
---
# <a name="transport-of-netnamedpipebinding"></a><span data-ttu-id="ccf1e-102">\<transport > de \<netNamedPipeBinding ></span><span class="sxs-lookup"><span data-stu-id="ccf1e-102">\<transport> of \<netNamedPipeBinding></span></span>
<span data-ttu-id="ccf1e-103">Définit les paramètres de sécurité de transport pour un canal nommé.</span><span class="sxs-lookup"><span data-stu-id="ccf1e-103">Defines the transport security settings for a named pipe.</span></span>  
  
 <span data-ttu-id="ccf1e-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="ccf1e-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="ccf1e-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="ccf1e-105">\<bindings></span></span>  
<span data-ttu-id="ccf1e-106">\<netNamedPipeBinding></span><span class="sxs-lookup"><span data-stu-id="ccf1e-106">\<netNamedPipeBinding></span></span>  
<span data-ttu-id="ccf1e-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="ccf1e-107">\<binding></span></span>  
<span data-ttu-id="ccf1e-108">\<security></span><span class="sxs-lookup"><span data-stu-id="ccf1e-108">\<security></span></span>  
<span data-ttu-id="ccf1e-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="ccf1e-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ccf1e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ccf1e-110">Syntax</span></span>  
  
```xml  
<netNamedPipeBinding>
  <binding>
    <security mode="None/Transport">
      <transport protectionLevel="None/Sign/EncryptAndSign" />
    </security>
  </binding>
</netNamedPipeBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ccf1e-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ccf1e-111">Attributes and Elements</span></span>  
 <span data-ttu-id="ccf1e-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ccf1e-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ccf1e-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="ccf1e-113">Attributes</span></span>  
  
|<span data-ttu-id="ccf1e-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="ccf1e-114">Attribute</span></span>|<span data-ttu-id="ccf1e-115">Description</span><span class="sxs-lookup"><span data-stu-id="ccf1e-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ccf1e-116">protectionLevel</span><span class="sxs-lookup"><span data-stu-id="ccf1e-116">protectionLevel</span></span>|<span data-ttu-id="ccf1e-117">Définit le niveau de protection du canal nommé.</span><span class="sxs-lookup"><span data-stu-id="ccf1e-117">Defines protection level of the named pipe.</span></span> <span data-ttu-id="ccf1e-118">La signature des messages atténue le risque de modification par un tiers pendant le transfert.</span><span class="sxs-lookup"><span data-stu-id="ccf1e-118">Signing messages mitigates the risk of a third party tampering with the message while it is being transferred.</span></span> <span data-ttu-id="ccf1e-119">Le chiffrement garantit la confidentialité des données pendant le transport.</span><span class="sxs-lookup"><span data-stu-id="ccf1e-119">Encryption provides data-level privacy during transport.</span></span> <span data-ttu-id="ccf1e-120">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ccf1e-120">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="ccf1e-121">-None : Aucune protection.</span><span class="sxs-lookup"><span data-stu-id="ccf1e-121">-   None: No protection.</span></span><br /><span data-ttu-id="ccf1e-122">-Signe : Les messages sont signés.</span><span class="sxs-lookup"><span data-stu-id="ccf1e-122">-   Sign: Messages are signed.</span></span><br /><span data-ttu-id="ccf1e-123">-   EncryptAndSign: Les messages sont chiffrés et signés.</span><span class="sxs-lookup"><span data-stu-id="ccf1e-123">-   EncryptAndSign: Messages are encrypted and signed.</span></span><br /><br /> <span data-ttu-id="ccf1e-124">La valeur par défaut est EncryptAndSign.</span><span class="sxs-lookup"><span data-stu-id="ccf1e-124">The default value is EncryptAndSign.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ccf1e-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ccf1e-125">Child Elements</span></span>  
 <span data-ttu-id="ccf1e-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ccf1e-126">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ccf1e-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ccf1e-127">Parent Elements</span></span>  
  
|<span data-ttu-id="ccf1e-128">Élément</span><span class="sxs-lookup"><span data-stu-id="ccf1e-128">Element</span></span>|<span data-ttu-id="ccf1e-129">Description</span><span class="sxs-lookup"><span data-stu-id="ccf1e-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ccf1e-130">\<security></span><span class="sxs-lookup"><span data-stu-id="ccf1e-130">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netnamedpipebinding.md)|<span data-ttu-id="ccf1e-131">Définit les paramètres de sécurité d’une liaison.</span><span class="sxs-lookup"><span data-stu-id="ccf1e-131">Defines the security settings for a binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ccf1e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccf1e-132">See also</span></span>

- <xref:System.ServiceModel.NamedPipeTransportSecurity>
- <xref:System.ServiceModel.Configuration.NetNamedPipeSecurityElement.Transport%2A>
- <xref:System.ServiceModel.NetNamedPipeSecurity.Transport%2A>
- <xref:System.ServiceModel.Configuration.NamedPipeTransportSecurityElement>
- [<span data-ttu-id="ccf1e-133">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="ccf1e-133">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="ccf1e-134">Liaisons</span><span class="sxs-lookup"><span data-stu-id="ccf1e-134">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="ccf1e-135">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="ccf1e-135">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="ccf1e-136">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="ccf1e-136">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="ccf1e-137">\<binding></span><span class="sxs-lookup"><span data-stu-id="ccf1e-137">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
