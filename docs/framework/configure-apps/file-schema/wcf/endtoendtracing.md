---
title: <endToEndTracing>
ms.date: 03/30/2017
ms.assetid: 5034f5de-bb60-4157-9ad4-58aaade094e0
ms.openlocfilehash: 266b33e9b0386d0346a86ba8bd82cc65def4f0c2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61673054"
---
# <a name="endtoendtracing"></a><span data-ttu-id="6ef3e-101">\<endToEndTracing></span><span class="sxs-lookup"><span data-stu-id="6ef3e-101">\<endToEndTracing></span></span>
<span data-ttu-id="6ef3e-102">Élément de configuration qui vous permet d'activer et désactiver différents aspects du suivi de bout en bout pendant l'exécution d'une application de service.</span><span class="sxs-lookup"><span data-stu-id="6ef3e-102">A configuration element that allows you to enable and disable different aspects of end-to-end tracing during the running of a service application.</span></span>  
  
 <span data-ttu-id="6ef3e-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="6ef3e-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="6ef3e-104">\<diagnostic></span><span class="sxs-lookup"><span data-stu-id="6ef3e-104">\<diagnostic></span></span>  
<span data-ttu-id="6ef3e-105">\<endToEndTracing></span><span class="sxs-lookup"><span data-stu-id="6ef3e-105">\<endToEndTracing></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6ef3e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ef3e-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <diagnostics>
    <endToEndTracing activityTracing="Boolean"
                     messageFlowTracing="Boolean"
                     propagateActivity="Boolean" />
  </diagnostics>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6ef3e-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6ef3e-107">Attributes and Elements</span></span>  
 <span data-ttu-id="6ef3e-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6ef3e-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6ef3e-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="6ef3e-109">Attributes</span></span>  
  
|<span data-ttu-id="6ef3e-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="6ef3e-110">Attribute</span></span>|<span data-ttu-id="6ef3e-111">Description</span><span class="sxs-lookup"><span data-stu-id="6ef3e-111">Description</span></span>|  
|---------------|-----------------|  
|`activityTracing`|<span data-ttu-id="6ef3e-112">Valeur booléenne qui spécifie si le suivi d'activité est activé.</span><span class="sxs-lookup"><span data-stu-id="6ef3e-112">A Boolean value that specifies whether activity tracing is enabled.</span></span>|  
|`messageFlowTracing`|<span data-ttu-id="6ef3e-113">Valeur booléenne qui spécifie si le suivi de flux de messages est activé.</span><span class="sxs-lookup"><span data-stu-id="6ef3e-113">A Boolean value that specifies whether message flow tracing in enabled.</span></span>|  
|`propagateActivity`|<span data-ttu-id="6ef3e-114">Valeur booléenne qui spécifie si l'attribut de propagation a la valeur True.</span><span class="sxs-lookup"><span data-stu-id="6ef3e-114">A Boolean value that specifies whether the propagate attribute is set to true.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6ef3e-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6ef3e-115">Child Elements</span></span>  
 <span data-ttu-id="6ef3e-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6ef3e-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6ef3e-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6ef3e-117">Parent Elements</span></span>  
  
|<span data-ttu-id="6ef3e-118">Élément</span><span class="sxs-lookup"><span data-stu-id="6ef3e-118">Element</span></span>|<span data-ttu-id="6ef3e-119">Description</span><span class="sxs-lookup"><span data-stu-id="6ef3e-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6ef3e-120">\<diagnostics></span><span class="sxs-lookup"><span data-stu-id="6ef3e-120">\<diagnostics></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/diagnostics.md)|<span data-ttu-id="6ef3e-121">Définit des paramètres WCF pour l'inspection et le contrôle au moment de l'exécution pour l'administrateur.</span><span class="sxs-lookup"><span data-stu-id="6ef3e-121">Defines WCF settings for runtime inspection and control for the administrator.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6ef3e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ef3e-122">See also</span></span>

- <xref:System.ServiceModel.Configuration.DiagnosticSection>
- <xref:System.ServiceModel.Diagnostics>
- <xref:System.ServiceModel.Configuration.DiagnosticSection.EndToEndTracing%2A>
- <xref:System.ServiceModel.Configuration.EndToEndTracingElement>
- [<span data-ttu-id="6ef3e-123">Suivi de bout en bout</span><span class="sxs-lookup"><span data-stu-id="6ef3e-123">End-to-End Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/end-to-end-tracing.md)
