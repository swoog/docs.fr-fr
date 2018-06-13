---
title: "&lt;diagnostics&gt; pour l'activation"
ms.date: 03/30/2017
ms.assetid: 1486e0eb-fe2a-46c3-b584-c924889477dd
ms.openlocfilehash: 4e5332eed87ded51cebcd614f45cbc8e80e570fb
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32747929"
---
# <a name="ltdiagnosticsgt-for-activation"></a><span data-ttu-id="90c1d-102">&lt;diagnostics&gt; pour l'activation</span><span class="sxs-lookup"><span data-stu-id="90c1d-102">&lt;diagnostics&gt; for Activation</span></span>
<span data-ttu-id="90c1d-103">Configure les fonctionnalités de diagnostic de l’écouteur Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="90c1d-103">Configures Windows Communication Foundation (WCF) listener's diagnostics functionalities.</span></span>  
  
 <span data-ttu-id="90c1d-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="90c1d-104">\<system.serviceModel.activation></span></span>  
<span data-ttu-id="90c1d-105">\<Diagnostics ></span><span class="sxs-lookup"><span data-stu-id="90c1d-105">\<diagnostics></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="90c1d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90c1d-106">Syntax</span></span>  
  
```xml  
<configuration>  
   <system.serviceModel.activation>  
       <diagnostics performanceCountersEnabled="Boolean" />  
   </system.serviceModel.activation>  
</configuration>  
```  
  
## <a name="type"></a><span data-ttu-id="90c1d-107">Type</span><span class="sxs-lookup"><span data-stu-id="90c1d-107">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="90c1d-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="90c1d-108">Attributes and Elements</span></span>  
 <span data-ttu-id="90c1d-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="90c1d-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="90c1d-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="90c1d-110">Attributes</span></span>  
  
|<span data-ttu-id="90c1d-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="90c1d-111">Attribute</span></span>|<span data-ttu-id="90c1d-112">Description</span><span class="sxs-lookup"><span data-stu-id="90c1d-112">Description</span></span>|  
|---------------|-----------------|  
|`performanceCountersEnabled`|<span data-ttu-id="90c1d-113">Valeur booléenne qui indique si les compteurs de performance sont activés à des fins de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="90c1d-113">A Boolean value that indicates whether performance counters are enabled for diagnostic purposes.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="90c1d-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="90c1d-114">Child Elements</span></span>  
 <span data-ttu-id="90c1d-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="90c1d-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="90c1d-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="90c1d-116">Parent Elements</span></span>  
  
|<span data-ttu-id="90c1d-117">Élément</span><span class="sxs-lookup"><span data-stu-id="90c1d-117">Element</span></span>|<span data-ttu-id="90c1d-118">Description</span><span class="sxs-lookup"><span data-stu-id="90c1d-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="90c1d-119">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="90c1d-119">\<system.serviceModel.activation></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel-activation.md)|<span data-ttu-id="90c1d-120">Contient les paramètres de configuration du processus de l'écouteur SMSvcHost.exe.</span><span class="sxs-lookup"><span data-stu-id="90c1d-120">Contains configuration settings for the listener process SMSvcHost.exe.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="90c1d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90c1d-121">See Also</span></span>  
 <xref:System.ServiceModel.Activation.Configuration.DiagnosticSection>
