---
title: <add> de <transportConfigurationType>
ms.date: 03/30/2017
ms.assetid: 03d79db9-571d-4534-acef-d05e5467b257
ms.openlocfilehash: c71a58b13e89bedb5eed24d784c82fb1525f7625
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61701435"
---
# <a name="add-of-transportconfigurationtype"></a><span data-ttu-id="6392a-102">\<add> of \<transportConfigurationType></span><span class="sxs-lookup"><span data-stu-id="6392a-102">\<add> of \<transportConfigurationType></span></span>
<span data-ttu-id="6392a-103">Cet élément est une paire clé/valeur, qui identifie le type d'un transport particulier.</span><span class="sxs-lookup"><span data-stu-id="6392a-103">This element is a key/value pair, which identifies the type of a particular transport.</span></span>  
  
 <span data-ttu-id="6392a-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="6392a-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="6392a-105">\<ServiceHostingEnvironment></span><span class="sxs-lookup"><span data-stu-id="6392a-105">\<ServiceHostingEnvironment></span></span>  
<span data-ttu-id="6392a-106">\<transportConfigurationTypes></span><span class="sxs-lookup"><span data-stu-id="6392a-106">\<transportConfigurationTypes></span></span>  
<span data-ttu-id="6392a-107">\<add></span><span class="sxs-lookup"><span data-stu-id="6392a-107">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6392a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6392a-108">Syntax</span></span>  
  
```xml  
<serviceHostingEnvironment>
  <transportConfigurationTypes>
    <add name="String"
         transportConfigurationType="String" />
  </transportConfigurationTypes>
</serviceHostingEnvironment>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6392a-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6392a-109">Attributes and Elements</span></span>  
 <span data-ttu-id="6392a-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6392a-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6392a-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="6392a-111">Attributes</span></span>  
  
|<span data-ttu-id="6392a-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="6392a-112">Attribute</span></span>|<span data-ttu-id="6392a-113">Description</span><span class="sxs-lookup"><span data-stu-id="6392a-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6392a-114">name</span><span class="sxs-lookup"><span data-stu-id="6392a-114">name</span></span>|<span data-ttu-id="6392a-115">Attribut de chaîne requis.</span><span class="sxs-lookup"><span data-stu-id="6392a-115">Required String attribute.</span></span><br /><br /> <span data-ttu-id="6392a-116">Contient une clé définie par l'utilisateur qui identifie uniquement le type de transport.</span><span class="sxs-lookup"><span data-stu-id="6392a-116">Contains a user-defined key that uniquely identifies the transport type.</span></span>|  
|<span data-ttu-id="6392a-117">transportConfigurationType</span><span class="sxs-lookup"><span data-stu-id="6392a-117">transportConfigurationType</span></span>|<span data-ttu-id="6392a-118">Chaîne contenant le type qui implémente le transport spécifique.</span><span class="sxs-lookup"><span data-stu-id="6392a-118">A string that contains the type that implements the specific transport.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6392a-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6392a-119">Child Elements</span></span>  
 <span data-ttu-id="6392a-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6392a-120">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6392a-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6392a-121">Parent Elements</span></span>  
  
|<span data-ttu-id="6392a-122">Élément</span><span class="sxs-lookup"><span data-stu-id="6392a-122">Element</span></span>|<span data-ttu-id="6392a-123">Description</span><span class="sxs-lookup"><span data-stu-id="6392a-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6392a-124">\<transportConfigurationTypes></span><span class="sxs-lookup"><span data-stu-id="6392a-124">\<transportConfigurationTypes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transportconfigurationtypes.md)|<span data-ttu-id="6392a-125">Collection de types implémentant le transport spécifique.</span><span class="sxs-lookup"><span data-stu-id="6392a-125">A collection of types that implement the specific transport.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="6392a-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="6392a-126">Example</span></span>  
  
```xml  
<serviceHostingEnvironment>
  <transportConfigurationTypes>
    <add name="net.udp"
         transportConfigurationType="Microsoft.ServiceModel.Samples.Hosting.HostedUdpTransportConfiguration, UdpActivation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=6fa904d2da1848d6" />
  </transportConfigurationTypes>
</serviceHostingEnvironment>
```  
  
## <a name="see-also"></a><span data-ttu-id="6392a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6392a-127">See also</span></span>

- <xref:System.ServiceModel.Configuration.TransportConfigurationTypeElement>
- <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>
- <xref:System.ServiceModel.ServiceHostingEnvironment>
- [<span data-ttu-id="6392a-128">Hébergement</span><span class="sxs-lookup"><span data-stu-id="6392a-128">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
