---
title: '&lt;endToEndTracing&gt;'
ms.date: 03/30/2017
ms.assetid: 5034f5de-bb60-4157-9ad4-58aaade094e0
ms.openlocfilehash: 78a69256a391e97ff1962eea923f09115c4ebadd
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150108"
---
# <a name="ltendtoendtracinggt"></a><span data-ttu-id="46658-102">&lt;endToEndTracing&gt;</span><span class="sxs-lookup"><span data-stu-id="46658-102">&lt;endToEndTracing&gt;</span></span>
<span data-ttu-id="46658-103">Élément de configuration qui vous permet d'activer et désactiver différents aspects du suivi de bout en bout pendant l'exécution d'une application de service.</span><span class="sxs-lookup"><span data-stu-id="46658-103">A configuration element that allows you to enable and disable different aspects of end-to-end tracing during the running of a service application.</span></span>  
  
 <span data-ttu-id="46658-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="46658-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="46658-105">\<diagnostic ></span><span class="sxs-lookup"><span data-stu-id="46658-105">\<diagnostic></span></span>  
<span data-ttu-id="46658-106">\<endToEndTracing ></span><span class="sxs-lookup"><span data-stu-id="46658-106">\<endToEndTracing></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46658-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46658-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <diagnostics>
    <endToEndTracing activityTracing="Boolean"
                     messageFlowTracing="Boolean"
                     propagateActivity="Boolean" />
  </diagnostics>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="46658-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="46658-108">Attributes and Elements</span></span>  
 <span data-ttu-id="46658-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="46658-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="46658-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="46658-110">Attributes</span></span>  
  
|<span data-ttu-id="46658-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="46658-111">Attribute</span></span>|<span data-ttu-id="46658-112">Description</span><span class="sxs-lookup"><span data-stu-id="46658-112">Description</span></span>|  
|---------------|-----------------|  
|`activityTracing`|<span data-ttu-id="46658-113">Valeur booléenne qui spécifie si le suivi d'activité est activé.</span><span class="sxs-lookup"><span data-stu-id="46658-113">A Boolean value that specifies whether activity tracing is enabled.</span></span>|  
|`messageFlowTracing`|<span data-ttu-id="46658-114">Valeur booléenne qui spécifie si le suivi de flux de messages est activé.</span><span class="sxs-lookup"><span data-stu-id="46658-114">A Boolean value that specifies whether message flow tracing in enabled.</span></span>|  
|`propagateActivity`|<span data-ttu-id="46658-115">Valeur booléenne qui spécifie si l'attribut de propagation a la valeur True.</span><span class="sxs-lookup"><span data-stu-id="46658-115">A Boolean value that specifies whether the propagate attribute is set to true.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="46658-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="46658-116">Child Elements</span></span>  
 <span data-ttu-id="46658-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="46658-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="46658-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="46658-118">Parent Elements</span></span>  
  
|<span data-ttu-id="46658-119">Élément</span><span class="sxs-lookup"><span data-stu-id="46658-119">Element</span></span>|<span data-ttu-id="46658-120">Description</span><span class="sxs-lookup"><span data-stu-id="46658-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="46658-121">\<Diagnostics ></span><span class="sxs-lookup"><span data-stu-id="46658-121">\<diagnostics></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/diagnostics.md)|<span data-ttu-id="46658-122">Définit des paramètres WCF pour l'inspection et le contrôle au moment de l'exécution pour l'administrateur.</span><span class="sxs-lookup"><span data-stu-id="46658-122">Defines WCF settings for runtime inspection and control for the administrator.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="46658-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46658-123">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.DiagnosticSection>  
 <xref:System.ServiceModel.Diagnostics>  
 <xref:System.ServiceModel.Configuration.DiagnosticSection.EndToEndTracing%2A>  
 <xref:System.ServiceModel.Configuration.EndToEndTracingElement>  
 [<span data-ttu-id="46658-124">Suivi de bout en bout</span><span class="sxs-lookup"><span data-stu-id="46658-124">End-to-End Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/end-to-end-tracing.md)
