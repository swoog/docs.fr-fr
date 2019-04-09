---
title: <policyImporter>
ms.date: 03/30/2017
ms.assetid: b0d03456-546f-44bb-ab12-1b2ce7f98fca
ms.openlocfilehash: 81f38d2a163163ca7255ca546bbddbbb58fa3a1b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59094175"
---
# <a name="policyimporter"></a><span data-ttu-id="3e3ef-101">\<policyImporter></span><span class="sxs-lookup"><span data-stu-id="3e3ef-101">\<policyImporter></span></span>
<span data-ttu-id="3e3ef-102">Indique un importateur de stratégie qui contrôle l’importation d’assertions de stratégie personnalisées concernant les liaisons.</span><span class="sxs-lookup"><span data-stu-id="3e3ef-102">Specifies a policy importer that controls the import of custom policy assertions about bindings.</span></span>  
  
 <span data-ttu-id="3e3ef-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="3e3ef-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="3e3ef-104">\<client></span><span class="sxs-lookup"><span data-stu-id="3e3ef-104">\<client></span></span>  
<span data-ttu-id="3e3ef-105">\<metadata></span><span class="sxs-lookup"><span data-stu-id="3e3ef-105">\<metadata></span></span>  
<span data-ttu-id="3e3ef-106">\<policyImporters></span><span class="sxs-lookup"><span data-stu-id="3e3ef-106">\<policyImporters></span></span>  
<span data-ttu-id="3e3ef-107">\<policyImporter></span><span class="sxs-lookup"><span data-stu-id="3e3ef-107">\<policyImporter></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e3ef-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e3ef-108">Syntax</span></span>  
  
```xml  
<metadata>
  <policyImporters>
    <policyImporter type="String" />
  </policyImporters>
</metadata>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3e3ef-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3e3ef-109">Attributes and Elements</span></span>  
 <span data-ttu-id="3e3ef-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3e3ef-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3e3ef-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="3e3ef-111">Attributes</span></span>  
  
|<span data-ttu-id="3e3ef-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="3e3ef-112">Attribute</span></span>|<span data-ttu-id="3e3ef-113">Description</span><span class="sxs-lookup"><span data-stu-id="3e3ef-113">Description</span></span>|  
|---------------|-----------------|  
|`type`|<span data-ttu-id="3e3ef-114">Type de cet élément.</span><span class="sxs-lookup"><span data-stu-id="3e3ef-114">The type of this element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3e3ef-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3e3ef-115">Child Elements</span></span>  
 <span data-ttu-id="3e3ef-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3e3ef-116">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3e3ef-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3e3ef-117">Parent Elements</span></span>  
  
|<span data-ttu-id="3e3ef-118">Élément</span><span class="sxs-lookup"><span data-stu-id="3e3ef-118">Element</span></span>|<span data-ttu-id="3e3ef-119">Description</span><span class="sxs-lookup"><span data-stu-id="3e3ef-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3e3ef-120">\<policyImporters></span><span class="sxs-lookup"><span data-stu-id="3e3ef-120">\<policyImporters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/policyimporters.md)|<span data-ttu-id="3e3ef-121">Indique tous les importateurs de stratégie contrôlant l'importation d'assertions de stratégie personnalisées concernant les liaisons.</span><span class="sxs-lookup"><span data-stu-id="3e3ef-121">Specifies all the policy importers that control the import of custom policy assertions about bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3e3ef-122">Notes</span><span class="sxs-lookup"><span data-stu-id="3e3ef-122">Remarks</span></span>  
 <span data-ttu-id="3e3ef-123">Un importateur de stratégie permet de rechercher des assertions de stratégie personnalisées concernant les fonctionnalités de liaison et de joindre un élément de liaison personnalisé qui implémente les fonctionnalités requises par l’assertion.</span><span class="sxs-lookup"><span data-stu-id="3e3ef-123">A policy importer is used to search custom policy assertions about binding features, as well as attach a custom binding element that implements the features the assertion requires.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e3ef-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e3ef-124">See also</span></span>

- <xref:System.ServiceModel.Configuration.PolicyImporterElementCollection>
- <xref:System.ServiceModel.Configuration.PolicyImporterElement>
- <xref:System.ServiceModel.Configuration.MetadataElement>
- <xref:System.ServiceModel.Description.MetadataImporter>
- [<span data-ttu-id="3e3ef-125">Configuration du client WCF</span><span class="sxs-lookup"><span data-stu-id="3e3ef-125">WCF Client Configuration</span></span>](../../../../../docs/framework/wcf/feature-details/client-configuration.md)
- [<span data-ttu-id="3e3ef-126">Clients</span><span class="sxs-lookup"><span data-stu-id="3e3ef-126">Clients</span></span>](../../../../../docs/framework/wcf/feature-details/clients.md)
