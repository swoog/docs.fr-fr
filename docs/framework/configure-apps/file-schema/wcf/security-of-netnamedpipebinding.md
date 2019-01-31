---
title: <security> de <netNamedPipeBinding>
ms.date: 03/30/2017
ms.assetid: bb3cb022-637e-49fd-92e8-6766038affa7
ms.openlocfilehash: ee2c4161f70c01dc09ac36bbcf6a234f822682d0
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55265300"
---
# <a name="security-of-netnamedpipebinding"></a><span data-ttu-id="ecb81-102">\<security> of \<netNamedPipeBinding></span><span class="sxs-lookup"><span data-stu-id="ecb81-102">\<security> of \<netNamedPipeBinding></span></span>
<span data-ttu-id="ecb81-103">Définit les paramètres de sécurité d’une liaison.</span><span class="sxs-lookup"><span data-stu-id="ecb81-103">Defines the security settings for a binding.</span></span>  
  
 <span data-ttu-id="ecb81-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="ecb81-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="ecb81-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="ecb81-105">\<bindings></span></span>  
<span data-ttu-id="ecb81-106">\<netNamedPipeBinding></span><span class="sxs-lookup"><span data-stu-id="ecb81-106">\<netNamedPipeBinding></span></span>  
<span data-ttu-id="ecb81-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="ecb81-107">\<binding></span></span>  
<span data-ttu-id="ecb81-108">\<security></span><span class="sxs-lookup"><span data-stu-id="ecb81-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ecb81-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ecb81-109">Syntax</span></span>  
  
```xml  
<netNamedPipeBinding>
  <binding>
    <security mode="None/Transport">
      <transport protectionLevel="None/Sign/EncryptAndSign" />
    </security>
  </binding>
</netNamedPipeBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ecb81-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ecb81-110">Attributes and Elements</span></span>  
 <span data-ttu-id="ecb81-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ecb81-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ecb81-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="ecb81-112">Attributes</span></span>  
  
|<span data-ttu-id="ecb81-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="ecb81-113">Attribute</span></span>|<span data-ttu-id="ecb81-114">Description</span><span class="sxs-lookup"><span data-stu-id="ecb81-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ecb81-115">mode</span><span class="sxs-lookup"><span data-stu-id="ecb81-115">mode</span></span>|<span data-ttu-id="ecb81-116">Spécifie le type de sécurité appliqué à cette liaison.</span><span class="sxs-lookup"><span data-stu-id="ecb81-116">Specifies the type of security that is applied to this binding.</span></span> <span data-ttu-id="ecb81-117">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ecb81-117">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="ecb81-118">-None : Cela désactive la sécurité.</span><span class="sxs-lookup"><span data-stu-id="ecb81-118">-   None: This disables security.</span></span><br /><span data-ttu-id="ecb81-119">-Transport : Sécurité est assurée à l’aide de la sécurité en fonction de transport sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="ecb81-119">-   Transport: Security is provided using underlying transport based security.</span></span> <span data-ttu-id="ecb81-120">Il est possible de contrôler le niveau de protection avec ce mode.</span><span class="sxs-lookup"><span data-stu-id="ecb81-120">It is possible to control the protection level with this mode.</span></span><br /><span data-ttu-id="ecb81-121">-La valeur par défaut est Transport.</span><span class="sxs-lookup"><span data-stu-id="ecb81-121">-   The default value is Transport.</span></span> <span data-ttu-id="ecb81-122">Cet attribut est de type <xref:System.ServiceModel.NetNamedPipeSecurityMode>.</span><span class="sxs-lookup"><span data-stu-id="ecb81-122">This attribute is of type <xref:System.ServiceModel.NetNamedPipeSecurityMode>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ecb81-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ecb81-123">Child Elements</span></span>  
  
|<span data-ttu-id="ecb81-124">Élément</span><span class="sxs-lookup"><span data-stu-id="ecb81-124">Element</span></span>|<span data-ttu-id="ecb81-125">Description</span><span class="sxs-lookup"><span data-stu-id="ecb81-125">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ecb81-126">transport</span><span class="sxs-lookup"><span data-stu-id="ecb81-126">transport</span></span>|<span data-ttu-id="ecb81-127">Définit les paramètres de sécurité pour le transport.</span><span class="sxs-lookup"><span data-stu-id="ecb81-127">Defines the security settings for the transport.</span></span> <span data-ttu-id="ecb81-128">Cet élément est de type <xref:System.ServiceModel.Configuration.NamedPipeTransportSecurityElement>.</span><span class="sxs-lookup"><span data-stu-id="ecb81-128">This element is of type <xref:System.ServiceModel.Configuration.NamedPipeTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ecb81-129">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ecb81-129">Parent Elements</span></span>  
  
|<span data-ttu-id="ecb81-130">Élément</span><span class="sxs-lookup"><span data-stu-id="ecb81-130">Element</span></span>|<span data-ttu-id="ecb81-131">Description</span><span class="sxs-lookup"><span data-stu-id="ecb81-131">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ecb81-132">liaison</span><span class="sxs-lookup"><span data-stu-id="ecb81-132">binding</span></span>|<span data-ttu-id="ecb81-133">L’élément de liaison de la [ \<netNamedPipeBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netnamedpipebinding.md).</span><span class="sxs-lookup"><span data-stu-id="ecb81-133">The binding element of the [\<netNamedPipeBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netnamedpipebinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ecb81-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecb81-134">See also</span></span>
- <xref:System.ServiceModel.NetNamedPipeSecurity>
- <xref:System.ServiceModel.NetNamedPipeBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.NetNamedPipeBindingElement.Security%2A>
- <xref:System.ServiceModel.Configuration.NetNamedPipeSecurityElement>
- [<span data-ttu-id="ecb81-135">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="ecb81-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="ecb81-136">Sélection d’un type d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="ecb81-136">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)
- [<span data-ttu-id="ecb81-137">Liaisons</span><span class="sxs-lookup"><span data-stu-id="ecb81-137">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="ecb81-138">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="ecb81-138">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="ecb81-139">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="ecb81-139">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="ecb81-140">\<binding></span><span class="sxs-lookup"><span data-stu-id="ecb81-140">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
