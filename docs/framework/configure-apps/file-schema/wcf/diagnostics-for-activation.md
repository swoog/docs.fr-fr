---
title: <diagnostics> pour l’Activation
ms.date: 03/30/2017
ms.assetid: 1486e0eb-fe2a-46c3-b584-c924889477dd
ms.openlocfilehash: 30456963a7d74a93e39bb1fddc0910daae97f039
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704256"
---
# <a name="diagnostics-for-activation"></a><span data-ttu-id="1cccd-102">\<Diagnostics > pour l’Activation</span><span class="sxs-lookup"><span data-stu-id="1cccd-102">\<diagnostics> for Activation</span></span>
<span data-ttu-id="1cccd-103">Configure les fonctionnalités de diagnostic de l’écouteur Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="1cccd-103">Configures Windows Communication Foundation (WCF) listener's diagnostics functionalities.</span></span>  
  
 <span data-ttu-id="1cccd-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="1cccd-104">\<system.serviceModel.activation></span></span>  
<span data-ttu-id="1cccd-105">\<diagnostics></span><span class="sxs-lookup"><span data-stu-id="1cccd-105">\<diagnostics></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1cccd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cccd-106">Syntax</span></span>  
  
```xml  
<configuration>
  <system.serviceModel.activation>
    <diagnostics performanceCountersEnabled="Boolean" />
  </system.serviceModel.activation>
</configuration>
```  
  
## <a name="type"></a><span data-ttu-id="1cccd-107">Type</span><span class="sxs-lookup"><span data-stu-id="1cccd-107">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1cccd-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1cccd-108">Attributes and Elements</span></span>  
 <span data-ttu-id="1cccd-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1cccd-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1cccd-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="1cccd-110">Attributes</span></span>  
  
|<span data-ttu-id="1cccd-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="1cccd-111">Attribute</span></span>|<span data-ttu-id="1cccd-112">Description</span><span class="sxs-lookup"><span data-stu-id="1cccd-112">Description</span></span>|  
|---------------|-----------------|  
|`performanceCountersEnabled`|<span data-ttu-id="1cccd-113">Valeur booléenne qui indique si les compteurs de performance sont activés à des fins de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="1cccd-113">A Boolean value that indicates whether performance counters are enabled for diagnostic purposes.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1cccd-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1cccd-114">Child Elements</span></span>  
 <span data-ttu-id="1cccd-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1cccd-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1cccd-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1cccd-116">Parent Elements</span></span>  
  
|<span data-ttu-id="1cccd-117">Élément</span><span class="sxs-lookup"><span data-stu-id="1cccd-117">Element</span></span>|<span data-ttu-id="1cccd-118">Description</span><span class="sxs-lookup"><span data-stu-id="1cccd-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1cccd-119">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="1cccd-119">\<system.serviceModel.activation></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel-activation.md)|<span data-ttu-id="1cccd-120">Contient les paramètres de configuration du processus de l'écouteur SMSvcHost.exe.</span><span class="sxs-lookup"><span data-stu-id="1cccd-120">Contains configuration settings for the listener process SMSvcHost.exe.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1cccd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cccd-121">See also</span></span>

- <xref:System.ServiceModel.Activation.Configuration.DiagnosticSection>
