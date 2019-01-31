---
title: <services>
ms.date: 03/30/2017
ms.assetid: 80d76ba9-2058-48ad-9b91-5e4be7e5c113
ms.openlocfilehash: 4dc425fa97eaf99664f0d9bbbbc851c462cbf373
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55274961"
---
# <a name="services"></a><span data-ttu-id="09388-101">\<services></span><span class="sxs-lookup"><span data-stu-id="09388-101">\<services></span></span>
<span data-ttu-id="09388-102">Les services sont définis dans la section `services` du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="09388-102">Services are defined in the `services` section of the configuration file.</span></span> <span data-ttu-id="09388-103">Chacun dispose de sa propre section de configuration de `service`.</span><span class="sxs-lookup"><span data-stu-id="09388-103">Each service has its own `service` configuration section.</span></span>  
  
 <span data-ttu-id="09388-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="09388-104">\<system.ServiceModel></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="09388-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09388-105">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <services>
    <service>
    </service>
  </services>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="09388-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="09388-106">Attributes and Elements</span></span>  
 <span data-ttu-id="09388-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="09388-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="09388-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="09388-108">Attributes</span></span>  
 <span data-ttu-id="09388-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="09388-109">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="09388-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="09388-110">Child Elements</span></span>  
  
|<span data-ttu-id="09388-111">Élément</span><span class="sxs-lookup"><span data-stu-id="09388-111">Element</span></span>|<span data-ttu-id="09388-112">Description</span><span class="sxs-lookup"><span data-stu-id="09388-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="09388-113">\<service></span><span class="sxs-lookup"><span data-stu-id="09388-113">\<service></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/service.md)|<span data-ttu-id="09388-114">Définissez le contrat de service, le comportement et les points de terminaison du service particulier.</span><span class="sxs-lookup"><span data-stu-id="09388-114">Define the service contract, behavior, and endpoints of the particular service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="09388-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="09388-115">Parent Elements</span></span>  
  
|<span data-ttu-id="09388-116">Élément</span><span class="sxs-lookup"><span data-stu-id="09388-116">Element</span></span>|<span data-ttu-id="09388-117">Description</span><span class="sxs-lookup"><span data-stu-id="09388-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="09388-118">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="09388-118">\<system.serviceModel></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)|<span data-ttu-id="09388-119">Élément racine de tous les éléments de configuration Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="09388-119">The root element of all Windows Communication Foundation (WCF) configuration elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="09388-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09388-120">See also</span></span>
- <xref:System.ServiceModel.Configuration.ServicesSection>
