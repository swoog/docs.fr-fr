---
title: <add> de <transportConfigurationType>
ms.date: 03/30/2017
ms.assetid: 03d79db9-571d-4534-acef-d05e5467b257
ms.openlocfilehash: c71a58b13e89bedb5eed24d784c82fb1525f7625
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59126722"
---
# <a name="add-of-transportconfigurationtype"></a><span data-ttu-id="c7876-102">\<add> of \<transportConfigurationType></span><span class="sxs-lookup"><span data-stu-id="c7876-102">\<add> of \<transportConfigurationType></span></span>
<span data-ttu-id="c7876-103">Cet élément est une paire clé/valeur, qui identifie le type d'un transport particulier.</span><span class="sxs-lookup"><span data-stu-id="c7876-103">This element is a key/value pair, which identifies the type of a particular transport.</span></span>  
  
 <span data-ttu-id="c7876-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="c7876-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="c7876-105">\<ServiceHostingEnvironment></span><span class="sxs-lookup"><span data-stu-id="c7876-105">\<ServiceHostingEnvironment></span></span>  
<span data-ttu-id="c7876-106">\<transportConfigurationTypes></span><span class="sxs-lookup"><span data-stu-id="c7876-106">\<transportConfigurationTypes></span></span>  
<span data-ttu-id="c7876-107">\<add></span><span class="sxs-lookup"><span data-stu-id="c7876-107">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7876-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7876-108">Syntax</span></span>  
  
```xml  
<serviceHostingEnvironment>
  <transportConfigurationTypes>
    <add name="String"
         transportConfigurationType="String" />
  </transportConfigurationTypes>
</serviceHostingEnvironment>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c7876-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c7876-109">Attributes and Elements</span></span>  
 <span data-ttu-id="c7876-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c7876-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c7876-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="c7876-111">Attributes</span></span>  
  
|<span data-ttu-id="c7876-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="c7876-112">Attribute</span></span>|<span data-ttu-id="c7876-113">Description</span><span class="sxs-lookup"><span data-stu-id="c7876-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c7876-114">name</span><span class="sxs-lookup"><span data-stu-id="c7876-114">name</span></span>|<span data-ttu-id="c7876-115">Attribut de chaîne requis.</span><span class="sxs-lookup"><span data-stu-id="c7876-115">Required String attribute.</span></span><br /><br /> <span data-ttu-id="c7876-116">Contient une clé définie par l'utilisateur qui identifie uniquement le type de transport.</span><span class="sxs-lookup"><span data-stu-id="c7876-116">Contains a user-defined key that uniquely identifies the transport type.</span></span>|  
|<span data-ttu-id="c7876-117">transportConfigurationType</span><span class="sxs-lookup"><span data-stu-id="c7876-117">transportConfigurationType</span></span>|<span data-ttu-id="c7876-118">Chaîne contenant le type qui implémente le transport spécifique.</span><span class="sxs-lookup"><span data-stu-id="c7876-118">A string that contains the type that implements the specific transport.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c7876-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c7876-119">Child Elements</span></span>  
 <span data-ttu-id="c7876-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c7876-120">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c7876-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c7876-121">Parent Elements</span></span>  
  
|<span data-ttu-id="c7876-122">Élément</span><span class="sxs-lookup"><span data-stu-id="c7876-122">Element</span></span>|<span data-ttu-id="c7876-123">Description</span><span class="sxs-lookup"><span data-stu-id="c7876-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c7876-124">\<transportConfigurationTypes></span><span class="sxs-lookup"><span data-stu-id="c7876-124">\<transportConfigurationTypes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transportconfigurationtypes.md)|<span data-ttu-id="c7876-125">Collection de types implémentant le transport spécifique.</span><span class="sxs-lookup"><span data-stu-id="c7876-125">A collection of types that implement the specific transport.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="c7876-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="c7876-126">Example</span></span>  
  
```xml  
<serviceHostingEnvironment>
  <transportConfigurationTypes>
    <add name="net.udp"
         transportConfigurationType="Microsoft.ServiceModel.Samples.Hosting.HostedUdpTransportConfiguration, UdpActivation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=6fa904d2da1848d6" />
  </transportConfigurationTypes>
</serviceHostingEnvironment>
```  
  
## <a name="see-also"></a><span data-ttu-id="c7876-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7876-127">See also</span></span>

- <xref:System.ServiceModel.Configuration.TransportConfigurationTypeElement>
- <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>
- <xref:System.ServiceModel.ServiceHostingEnvironment>
- [<span data-ttu-id="c7876-128">Hébergement</span><span class="sxs-lookup"><span data-stu-id="c7876-128">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
