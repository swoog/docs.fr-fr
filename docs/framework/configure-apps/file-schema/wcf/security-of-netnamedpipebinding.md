---
title: <security> de <netNamedPipeBinding>
ms.date: 03/30/2017
ms.assetid: bb3cb022-637e-49fd-92e8-6766038affa7
ms.openlocfilehash: fa31dda3274c9768694bdf5232f31554899e1d82
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59203390"
---
# <a name="security-of-netnamedpipebinding"></a><span data-ttu-id="eb551-102">\<security> of \<netNamedPipeBinding></span><span class="sxs-lookup"><span data-stu-id="eb551-102">\<security> of \<netNamedPipeBinding></span></span>
<span data-ttu-id="eb551-103">Définit les paramètres de sécurité d’une liaison.</span><span class="sxs-lookup"><span data-stu-id="eb551-103">Defines the security settings for a binding.</span></span>  
  
 <span data-ttu-id="eb551-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="eb551-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="eb551-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="eb551-105">\<bindings></span></span>  
<span data-ttu-id="eb551-106">\<netNamedPipeBinding></span><span class="sxs-lookup"><span data-stu-id="eb551-106">\<netNamedPipeBinding></span></span>  
<span data-ttu-id="eb551-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="eb551-107">\<binding></span></span>  
<span data-ttu-id="eb551-108">\<security></span><span class="sxs-lookup"><span data-stu-id="eb551-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eb551-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb551-109">Syntax</span></span>  
  
```xml  
<netNamedPipeBinding>
  <binding>
    <security mode="None/Transport">
      <transport protectionLevel="None/Sign/EncryptAndSign" />
    </security>
  </binding>
</netNamedPipeBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="eb551-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="eb551-110">Attributes and Elements</span></span>  
 <span data-ttu-id="eb551-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="eb551-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="eb551-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="eb551-112">Attributes</span></span>  
  
|<span data-ttu-id="eb551-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="eb551-113">Attribute</span></span>|<span data-ttu-id="eb551-114">Description</span><span class="sxs-lookup"><span data-stu-id="eb551-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="eb551-115">mode</span><span class="sxs-lookup"><span data-stu-id="eb551-115">mode</span></span>|<span data-ttu-id="eb551-116">Spécifie le type de sécurité appliqué à cette liaison.</span><span class="sxs-lookup"><span data-stu-id="eb551-116">Specifies the type of security that is applied to this binding.</span></span> <span data-ttu-id="eb551-117">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="eb551-117">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="eb551-118">-None : Cela désactive la sécurité.</span><span class="sxs-lookup"><span data-stu-id="eb551-118">-   None: This disables security.</span></span><br /><span data-ttu-id="eb551-119">-Transport : Sécurité est assurée à l’aide de la sécurité en fonction de transport sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="eb551-119">-   Transport: Security is provided using underlying transport based security.</span></span> <span data-ttu-id="eb551-120">Il est possible de contrôler le niveau de protection avec ce mode.</span><span class="sxs-lookup"><span data-stu-id="eb551-120">It is possible to control the protection level with this mode.</span></span><br /><span data-ttu-id="eb551-121">-La valeur par défaut est Transport.</span><span class="sxs-lookup"><span data-stu-id="eb551-121">-   The default value is Transport.</span></span> <span data-ttu-id="eb551-122">Cet attribut est de type <xref:System.ServiceModel.NetNamedPipeSecurityMode>.</span><span class="sxs-lookup"><span data-stu-id="eb551-122">This attribute is of type <xref:System.ServiceModel.NetNamedPipeSecurityMode>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="eb551-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eb551-123">Child Elements</span></span>  
  
|<span data-ttu-id="eb551-124">Élément</span><span class="sxs-lookup"><span data-stu-id="eb551-124">Element</span></span>|<span data-ttu-id="eb551-125">Description</span><span class="sxs-lookup"><span data-stu-id="eb551-125">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="eb551-126">transport</span><span class="sxs-lookup"><span data-stu-id="eb551-126">transport</span></span>|<span data-ttu-id="eb551-127">Définit les paramètres de sécurité pour le transport.</span><span class="sxs-lookup"><span data-stu-id="eb551-127">Defines the security settings for the transport.</span></span> <span data-ttu-id="eb551-128">Cet élément est de type <xref:System.ServiceModel.Configuration.NamedPipeTransportSecurityElement>.</span><span class="sxs-lookup"><span data-stu-id="eb551-128">This element is of type <xref:System.ServiceModel.Configuration.NamedPipeTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="eb551-129">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="eb551-129">Parent Elements</span></span>  
  
|<span data-ttu-id="eb551-130">Élément</span><span class="sxs-lookup"><span data-stu-id="eb551-130">Element</span></span>|<span data-ttu-id="eb551-131">Description</span><span class="sxs-lookup"><span data-stu-id="eb551-131">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="eb551-132">liaison</span><span class="sxs-lookup"><span data-stu-id="eb551-132">binding</span></span>|<span data-ttu-id="eb551-133">L’élément de liaison de la [ \<netNamedPipeBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netnamedpipebinding.md).</span><span class="sxs-lookup"><span data-stu-id="eb551-133">The binding element of the [\<netNamedPipeBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netnamedpipebinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="eb551-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb551-134">See also</span></span>

- <xref:System.ServiceModel.NetNamedPipeSecurity>
- <xref:System.ServiceModel.NetNamedPipeBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.NetNamedPipeBindingElement.Security%2A>
- <xref:System.ServiceModel.Configuration.NetNamedPipeSecurityElement>
- [<span data-ttu-id="eb551-135">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="eb551-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="eb551-136">Sélection d’un type d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="eb551-136">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)
- [<span data-ttu-id="eb551-137">Liaisons</span><span class="sxs-lookup"><span data-stu-id="eb551-137">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="eb551-138">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="eb551-138">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="eb551-139">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="eb551-139">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="eb551-140">\<binding></span><span class="sxs-lookup"><span data-stu-id="eb551-140">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
