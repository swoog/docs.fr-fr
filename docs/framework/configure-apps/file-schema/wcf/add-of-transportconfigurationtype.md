---
title: <add> de <transportConfigurationType>
ms.date: 03/30/2017
ms.assetid: 03d79db9-571d-4534-acef-d05e5467b257
ms.openlocfilehash: 84ad745e7789fc2de8dcc23f3607b63702af05a1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55263448"
---
# <a name="add-of-transportconfigurationtype"></a><span data-ttu-id="67387-102">\<add> of \<transportConfigurationType></span><span class="sxs-lookup"><span data-stu-id="67387-102">\<add> of \<transportConfigurationType></span></span>
<span data-ttu-id="67387-103">Cet élément est une paire clé/valeur, qui identifie le type d'un transport particulier.</span><span class="sxs-lookup"><span data-stu-id="67387-103">This element is a key/value pair, which identifies the type of a particular transport.</span></span>  
  
 <span data-ttu-id="67387-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="67387-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="67387-105">\<ServiceHostingEnvironment></span><span class="sxs-lookup"><span data-stu-id="67387-105">\<ServiceHostingEnvironment></span></span>  
<span data-ttu-id="67387-106">\<transportConfigurationTypes></span><span class="sxs-lookup"><span data-stu-id="67387-106">\<transportConfigurationTypes></span></span>  
<span data-ttu-id="67387-107">\<add></span><span class="sxs-lookup"><span data-stu-id="67387-107">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="67387-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67387-108">Syntax</span></span>  
  
```xml  
<serviceHostingEnvironment>
  <transportConfigurationTypes>
    <add name="String"
         transportConfigurationType="String" />
  </transportConfigurationTypes>
</serviceHostingEnvironment>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="67387-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="67387-109">Attributes and Elements</span></span>  
 <span data-ttu-id="67387-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="67387-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="67387-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="67387-111">Attributes</span></span>  
  
|<span data-ttu-id="67387-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="67387-112">Attribute</span></span>|<span data-ttu-id="67387-113">Description</span><span class="sxs-lookup"><span data-stu-id="67387-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="67387-114">name</span><span class="sxs-lookup"><span data-stu-id="67387-114">name</span></span>|<span data-ttu-id="67387-115">Attribut de chaîne requis.</span><span class="sxs-lookup"><span data-stu-id="67387-115">Required String attribute.</span></span><br /><br /> <span data-ttu-id="67387-116">Contient une clé définie par l'utilisateur qui identifie uniquement le type de transport.</span><span class="sxs-lookup"><span data-stu-id="67387-116">Contains a user-defined key that uniquely identifies the transport type.</span></span>|  
|<span data-ttu-id="67387-117">transportConfigurationType</span><span class="sxs-lookup"><span data-stu-id="67387-117">transportConfigurationType</span></span>|<span data-ttu-id="67387-118">Chaîne contenant le type qui implémente le transport spécifique.</span><span class="sxs-lookup"><span data-stu-id="67387-118">A string that contains the type that implements the specific transport.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="67387-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="67387-119">Child Elements</span></span>  
 <span data-ttu-id="67387-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="67387-120">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="67387-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="67387-121">Parent Elements</span></span>  
  
|<span data-ttu-id="67387-122">Élément</span><span class="sxs-lookup"><span data-stu-id="67387-122">Element</span></span>|<span data-ttu-id="67387-123">Description</span><span class="sxs-lookup"><span data-stu-id="67387-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="67387-124">\<transportConfigurationTypes></span><span class="sxs-lookup"><span data-stu-id="67387-124">\<transportConfigurationTypes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transportconfigurationtypes.md)|<span data-ttu-id="67387-125">Collection de types implémentant le transport spécifique.</span><span class="sxs-lookup"><span data-stu-id="67387-125">A collection of types that implement the specific transport.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="67387-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="67387-126">Example</span></span>  
  
```xml  
<serviceHostingEnvironment>
  <transportConfigurationTypes>
    <add name="net.udp"
         transportConfigurationType="Microsoft.ServiceModel.Samples.Hosting.HostedUdpTransportConfiguration, UdpActivation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=6fa904d2da1848d6" />
  </transportConfigurationTypes>
</serviceHostingEnvironment>
```  
  
## <a name="see-also"></a><span data-ttu-id="67387-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67387-127">See also</span></span>
- <xref:System.ServiceModel.Configuration.TransportConfigurationTypeElement>
- <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>
- <xref:System.ServiceModel.ServiceHostingEnvironment>
- [<span data-ttu-id="67387-128">Hébergement</span><span class="sxs-lookup"><span data-stu-id="67387-128">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
