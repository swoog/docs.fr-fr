---
title: <services>
ms.date: 03/30/2017
ms.assetid: 80d76ba9-2058-48ad-9b91-5e4be7e5c113
ms.openlocfilehash: 2db168d48e3959a7d80a10ca27134f58e3fcb2de
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59168075"
---
# <a name="services"></a><span data-ttu-id="9c866-101">\<services></span><span class="sxs-lookup"><span data-stu-id="9c866-101">\<services></span></span>
<span data-ttu-id="9c866-102">Les services sont définis dans la section `services` du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="9c866-102">Services are defined in the `services` section of the configuration file.</span></span> <span data-ttu-id="9c866-103">Chacun dispose de sa propre section de configuration de `service`.</span><span class="sxs-lookup"><span data-stu-id="9c866-103">Each service has its own `service` configuration section.</span></span>  
  
 <span data-ttu-id="9c866-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="9c866-104">\<system.ServiceModel></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9c866-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c866-105">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <services>
    <service>
    </service>
  </services>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9c866-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9c866-106">Attributes and Elements</span></span>  
 <span data-ttu-id="9c866-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9c866-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9c866-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="9c866-108">Attributes</span></span>  
 <span data-ttu-id="9c866-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9c866-109">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="9c866-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9c866-110">Child Elements</span></span>  
  
|<span data-ttu-id="9c866-111">Élément</span><span class="sxs-lookup"><span data-stu-id="9c866-111">Element</span></span>|<span data-ttu-id="9c866-112">Description</span><span class="sxs-lookup"><span data-stu-id="9c866-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9c866-113">\<service></span><span class="sxs-lookup"><span data-stu-id="9c866-113">\<service></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/service.md)|<span data-ttu-id="9c866-114">Définissez le contrat de service, le comportement et les points de terminaison du service particulier.</span><span class="sxs-lookup"><span data-stu-id="9c866-114">Define the service contract, behavior, and endpoints of the particular service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9c866-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9c866-115">Parent Elements</span></span>  
  
|<span data-ttu-id="9c866-116">Élément</span><span class="sxs-lookup"><span data-stu-id="9c866-116">Element</span></span>|<span data-ttu-id="9c866-117">Description</span><span class="sxs-lookup"><span data-stu-id="9c866-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9c866-118">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="9c866-118">\<system.serviceModel></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)|<span data-ttu-id="9c866-119">Élément racine de tous les éléments de configuration Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="9c866-119">The root element of all Windows Communication Foundation (WCF) configuration elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9c866-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c866-120">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServicesSection>
