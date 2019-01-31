---
title: <add> de <defaultPorts>
ms.date: 03/30/2017
ms.assetid: f162ce42-963b-4779-96a7-d6d8b4ea0d2f
ms.openlocfilehash: 799715ef008274ead6b745e8ab97e769cb59e6b5
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55261594"
---
# <a name="add-of-defaultports"></a><span data-ttu-id="6d506-102">\<Ajouter > de \<defaultPorts ></span><span class="sxs-lookup"><span data-stu-id="6d506-102">\<add> of \<defaultPorts></span></span>
<span data-ttu-id="6d506-103">Point de terminaison de communication par défaut écouté par l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="6d506-103">A default communications endpoint that the client application listens to.</span></span>  
  
 <span data-ttu-id="6d506-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="6d506-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="6d506-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="6d506-105">\<behaviors></span></span>  
<span data-ttu-id="6d506-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="6d506-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="6d506-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="6d506-107">\<behavior></span></span>  
<span data-ttu-id="6d506-108">\<useRequestHeadersForMetadataAddress></span><span class="sxs-lookup"><span data-stu-id="6d506-108">\<useRequestHeadersForMetadataAddress></span></span>  
<span data-ttu-id="6d506-109">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="6d506-109">\<defaultPorts></span></span>  
<span data-ttu-id="6d506-110">\<add></span><span class="sxs-lookup"><span data-stu-id="6d506-110">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6d506-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d506-111">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add port="Integer"
         scheme="String" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6d506-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6d506-112">Attributes and Elements</span></span>  
 <span data-ttu-id="6d506-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6d506-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6d506-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="6d506-114">Attributes</span></span>  
  
|<span data-ttu-id="6d506-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="6d506-115">Attribute</span></span>|<span data-ttu-id="6d506-116">Description</span><span class="sxs-lookup"><span data-stu-id="6d506-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6d506-117">port</span><span class="sxs-lookup"><span data-stu-id="6d506-117">port</span></span>|<span data-ttu-id="6d506-118">Entier qui spécifie le numéro de port de communication par défaut.</span><span class="sxs-lookup"><span data-stu-id="6d506-118">An integer that specifies the default communications port number</span></span>|  
|<span data-ttu-id="6d506-119">scheme</span><span class="sxs-lookup"><span data-stu-id="6d506-119">scheme</span></span>|<span data-ttu-id="6d506-120">Chaîne qui spécifie le groupe de paramètres de protocole associé à un port de communication.</span><span class="sxs-lookup"><span data-stu-id="6d506-120">A string that specifies the group of protocol settings associated with a communications port.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6d506-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6d506-121">Child Elements</span></span>  
 <span data-ttu-id="6d506-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6d506-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6d506-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6d506-123">Parent Elements</span></span>  
  
|<span data-ttu-id="6d506-124">Élément</span><span class="sxs-lookup"><span data-stu-id="6d506-124">Element</span></span>|<span data-ttu-id="6d506-125">Description</span><span class="sxs-lookup"><span data-stu-id="6d506-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6d506-126">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="6d506-126">\<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/defaultports.md)|<span data-ttu-id="6d506-127">Collection des ports par défaut répertoriant les points de terminaison de communication par défaut écoutés par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="6d506-127">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6d506-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d506-128">See also</span></span>
- <xref:System.ServiceModel.Configuration.DefaultPortElement>
