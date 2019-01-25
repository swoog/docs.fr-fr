---
title: '&lt;services&gt;'
ms.date: 03/30/2017
ms.assetid: 80d76ba9-2058-48ad-9b91-5e4be7e5c113
ms.openlocfilehash: 7b26224f1217e7f73a529c082c2c9272ec189a5a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54573255"
---
# <a name="ltservicesgt"></a><span data-ttu-id="74439-102">&lt;services&gt;</span><span class="sxs-lookup"><span data-stu-id="74439-102">&lt;services&gt;</span></span>
<span data-ttu-id="74439-103">Les services sont définis dans la section `services` du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="74439-103">Services are defined in the `services` section of the configuration file.</span></span> <span data-ttu-id="74439-104">Chacun dispose de sa propre section de configuration de `service`.</span><span class="sxs-lookup"><span data-stu-id="74439-104">Each service has its own `service` configuration section.</span></span>  
  
 <span data-ttu-id="74439-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="74439-105">\<system.ServiceModel></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="74439-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74439-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <services>
    <service>
    </service>
  </services>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="74439-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="74439-107">Attributes and Elements</span></span>  
 <span data-ttu-id="74439-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="74439-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="74439-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="74439-109">Attributes</span></span>  
 <span data-ttu-id="74439-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="74439-110">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="74439-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="74439-111">Child Elements</span></span>  
  
|<span data-ttu-id="74439-112">Élément</span><span class="sxs-lookup"><span data-stu-id="74439-112">Element</span></span>|<span data-ttu-id="74439-113">Description</span><span class="sxs-lookup"><span data-stu-id="74439-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="74439-114">\<service></span><span class="sxs-lookup"><span data-stu-id="74439-114">\<service></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/service.md)|<span data-ttu-id="74439-115">Définissez le contrat de service, le comportement et les points de terminaison du service particulier.</span><span class="sxs-lookup"><span data-stu-id="74439-115">Define the service contract, behavior, and endpoints of the particular service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="74439-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="74439-116">Parent Elements</span></span>  
  
|<span data-ttu-id="74439-117">Élément</span><span class="sxs-lookup"><span data-stu-id="74439-117">Element</span></span>|<span data-ttu-id="74439-118">Description</span><span class="sxs-lookup"><span data-stu-id="74439-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="74439-119">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="74439-119">\<system.serviceModel></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)|<span data-ttu-id="74439-120">Élément racine de tous les éléments de configuration Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="74439-120">The root element of all Windows Communication Foundation (WCF) configuration elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="74439-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74439-121">See also</span></span>
- <xref:System.ServiceModel.Configuration.ServicesSection>
