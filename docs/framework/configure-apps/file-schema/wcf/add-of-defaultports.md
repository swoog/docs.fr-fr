---
title: '&lt;add&gt; de &lt;defaultPorts&gt;'
ms.date: 03/30/2017
ms.assetid: f162ce42-963b-4779-96a7-d6d8b4ea0d2f
ms.openlocfilehash: 28ddc98bd66c1f74f857448aa710d3998ddbd3dc
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32748748"
---
# <a name="ltaddgt-of-ltdefaultportsgt"></a><span data-ttu-id="ea09d-102">&lt;add&gt; de &lt;defaultPorts&gt;</span><span class="sxs-lookup"><span data-stu-id="ea09d-102">&lt;add&gt; of &lt;defaultPorts&gt;</span></span>
<span data-ttu-id="ea09d-103">Point de terminaison de communication par défaut écouté par l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="ea09d-103">A default communications endpoint that the client application listens to.</span></span>  
  
 <span data-ttu-id="ea09d-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="ea09d-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="ea09d-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="ea09d-105">\<behaviors></span></span>  
<span data-ttu-id="ea09d-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="ea09d-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="ea09d-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="ea09d-107">\<behavior></span></span>  
<span data-ttu-id="ea09d-108">\<useRequestHeadersForMetadataAddress ></span><span class="sxs-lookup"><span data-stu-id="ea09d-108">\<useRequestHeadersForMetadataAddress></span></span>  
<span data-ttu-id="ea09d-109">\<defaultPorts ></span><span class="sxs-lookup"><span data-stu-id="ea09d-109">\<defaultPorts></span></span>  
<span data-ttu-id="ea09d-110">\<add></span><span class="sxs-lookup"><span data-stu-id="ea09d-110">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ea09d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea09d-111">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>   <defaultPorts>      <add port="Integer" scheme="String" />   </defaultPorts></useRequestHeadersForMetadataAddress>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ea09d-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ea09d-112">Attributes and Elements</span></span>  
 <span data-ttu-id="ea09d-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ea09d-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ea09d-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="ea09d-114">Attributes</span></span>  
  
|<span data-ttu-id="ea09d-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="ea09d-115">Attribute</span></span>|<span data-ttu-id="ea09d-116">Description</span><span class="sxs-lookup"><span data-stu-id="ea09d-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ea09d-117">port</span><span class="sxs-lookup"><span data-stu-id="ea09d-117">port</span></span>|<span data-ttu-id="ea09d-118">Entier qui spécifie le numéro de port de communication par défaut.</span><span class="sxs-lookup"><span data-stu-id="ea09d-118">An integer that specifies the default communications port number</span></span>|  
|<span data-ttu-id="ea09d-119">scheme</span><span class="sxs-lookup"><span data-stu-id="ea09d-119">scheme</span></span>|<span data-ttu-id="ea09d-120">Chaîne qui spécifie le groupe de paramètres de protocole associé à un port de communication.</span><span class="sxs-lookup"><span data-stu-id="ea09d-120">A string that specifies the group of protocol settings associated with a communications port.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ea09d-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ea09d-121">Child Elements</span></span>  
 <span data-ttu-id="ea09d-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ea09d-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ea09d-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ea09d-123">Parent Elements</span></span>  
  
|<span data-ttu-id="ea09d-124">Élément</span><span class="sxs-lookup"><span data-stu-id="ea09d-124">Element</span></span>|<span data-ttu-id="ea09d-125">Description</span><span class="sxs-lookup"><span data-stu-id="ea09d-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ea09d-126">\<defaultPorts ></span><span class="sxs-lookup"><span data-stu-id="ea09d-126">\<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/defaultports.md)|<span data-ttu-id="ea09d-127">Collection des ports par défaut répertoriant les points de terminaison de communication par défaut écoutés par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="ea09d-127">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ea09d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea09d-128">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.DefaultPortElement>
