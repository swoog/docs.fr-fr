---
title: '&lt;add&gt; de &lt;defaultPorts&gt;'
ms.date: 03/30/2017
ms.assetid: f162ce42-963b-4779-96a7-d6d8b4ea0d2f
ms.openlocfilehash: 0932ef9afacb6278c4857dcfd6ba545595ff8f9d
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147718"
---
# <a name="ltaddgt-of-ltdefaultportsgt"></a><span data-ttu-id="bdfc9-102">&lt;add&gt; de &lt;defaultPorts&gt;</span><span class="sxs-lookup"><span data-stu-id="bdfc9-102">&lt;add&gt; of &lt;defaultPorts&gt;</span></span>
<span data-ttu-id="bdfc9-103">Point de terminaison de communication par défaut écouté par l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="bdfc9-103">A default communications endpoint that the client application listens to.</span></span>  
  
 <span data-ttu-id="bdfc9-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="bdfc9-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="bdfc9-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="bdfc9-105">\<behaviors></span></span>  
<span data-ttu-id="bdfc9-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="bdfc9-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="bdfc9-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="bdfc9-107">\<behavior></span></span>  
<span data-ttu-id="bdfc9-108">\<useRequestHeadersForMetadataAddress ></span><span class="sxs-lookup"><span data-stu-id="bdfc9-108">\<useRequestHeadersForMetadataAddress></span></span>  
<span data-ttu-id="bdfc9-109">\<defaultPorts ></span><span class="sxs-lookup"><span data-stu-id="bdfc9-109">\<defaultPorts></span></span>  
<span data-ttu-id="bdfc9-110">\<add></span><span class="sxs-lookup"><span data-stu-id="bdfc9-110">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bdfc9-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdfc9-111">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add port="Integer"
         scheme="String" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bdfc9-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="bdfc9-112">Attributes and Elements</span></span>  
 <span data-ttu-id="bdfc9-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="bdfc9-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bdfc9-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="bdfc9-114">Attributes</span></span>  
  
|<span data-ttu-id="bdfc9-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="bdfc9-115">Attribute</span></span>|<span data-ttu-id="bdfc9-116">Description</span><span class="sxs-lookup"><span data-stu-id="bdfc9-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="bdfc9-117">port</span><span class="sxs-lookup"><span data-stu-id="bdfc9-117">port</span></span>|<span data-ttu-id="bdfc9-118">Entier qui spécifie le numéro de port de communication par défaut.</span><span class="sxs-lookup"><span data-stu-id="bdfc9-118">An integer that specifies the default communications port number</span></span>|  
|<span data-ttu-id="bdfc9-119">scheme</span><span class="sxs-lookup"><span data-stu-id="bdfc9-119">scheme</span></span>|<span data-ttu-id="bdfc9-120">Chaîne qui spécifie le groupe de paramètres de protocole associé à un port de communication.</span><span class="sxs-lookup"><span data-stu-id="bdfc9-120">A string that specifies the group of protocol settings associated with a communications port.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bdfc9-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bdfc9-121">Child Elements</span></span>  
 <span data-ttu-id="bdfc9-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bdfc9-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="bdfc9-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bdfc9-123">Parent Elements</span></span>  
  
|<span data-ttu-id="bdfc9-124">Élément</span><span class="sxs-lookup"><span data-stu-id="bdfc9-124">Element</span></span>|<span data-ttu-id="bdfc9-125">Description</span><span class="sxs-lookup"><span data-stu-id="bdfc9-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bdfc9-126">\<defaultPorts ></span><span class="sxs-lookup"><span data-stu-id="bdfc9-126">\<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/defaultports.md)|<span data-ttu-id="bdfc9-127">Collection des ports par défaut répertoriant les points de terminaison de communication par défaut écoutés par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="bdfc9-127">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="bdfc9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdfc9-128">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.DefaultPortElement>
