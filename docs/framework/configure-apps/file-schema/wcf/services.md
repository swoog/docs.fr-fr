---
title: '&lt;Services&gt;'
ms.date: 03/30/2017
ms.assetid: 80d76ba9-2058-48ad-9b91-5e4be7e5c113
ms.openlocfilehash: 789fc52f628174ef61a9c7169cb0cae0f1ba8e31
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32749229"
---
# <a name="ltservicesgt"></a><span data-ttu-id="c6c82-102">&lt;Services&gt;</span><span class="sxs-lookup"><span data-stu-id="c6c82-102">&lt;services&gt;</span></span>
<span data-ttu-id="c6c82-103">Les services sont définis dans la section `services` du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="c6c82-103">Services are defined in the `services` section of the configuration file.</span></span> <span data-ttu-id="c6c82-104">Chacun dispose de sa propre section de configuration de `service`.</span><span class="sxs-lookup"><span data-stu-id="c6c82-104">Each service has its own `service` configuration section.</span></span>  
  
 <span data-ttu-id="c6c82-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="c6c82-105">\<system.ServiceModel></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c6c82-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6c82-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>  
        <services>  
        <service>  
        </service>  
        </services>  
</system.serviceModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c6c82-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c6c82-107">Attributes and Elements</span></span>  
 <span data-ttu-id="c6c82-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c6c82-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c6c82-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="c6c82-109">Attributes</span></span>  
 <span data-ttu-id="c6c82-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="c6c82-110">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="c6c82-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c6c82-111">Child Elements</span></span>  
  
|<span data-ttu-id="c6c82-112">Élément</span><span class="sxs-lookup"><span data-stu-id="c6c82-112">Element</span></span>|<span data-ttu-id="c6c82-113">Description</span><span class="sxs-lookup"><span data-stu-id="c6c82-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c6c82-114">\<service></span><span class="sxs-lookup"><span data-stu-id="c6c82-114">\<service></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/service.md)|<span data-ttu-id="c6c82-115">Définissez le contrat de service, le comportement et les points de terminaison du service particulier.</span><span class="sxs-lookup"><span data-stu-id="c6c82-115">Define the service contract, behavior, and endpoints of the particular service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c6c82-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c6c82-116">Parent Elements</span></span>  
  
|<span data-ttu-id="c6c82-117">Élément</span><span class="sxs-lookup"><span data-stu-id="c6c82-117">Element</span></span>|<span data-ttu-id="c6c82-118">Description</span><span class="sxs-lookup"><span data-stu-id="c6c82-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c6c82-119">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="c6c82-119">\<system.serviceModel></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)|<span data-ttu-id="c6c82-120">Élément racine de tous les éléments de configuration Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="c6c82-120">The root element of all Windows Communication Foundation (WCF) configuration elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c6c82-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6c82-121">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServicesSection>
