---
title: <policyImporter>
ms.date: 03/30/2017
ms.assetid: b0d03456-546f-44bb-ab12-1b2ce7f98fca
ms.openlocfilehash: ab9193d5974ccffcbfa3e741ac4d32ff357ed372
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55269235"
---
# <a name="policyimporter"></a><span data-ttu-id="ce9bf-101">\<policyImporter></span><span class="sxs-lookup"><span data-stu-id="ce9bf-101">\<policyImporter></span></span>
<span data-ttu-id="ce9bf-102">Indique un importateur de stratégie qui contrôle l’importation d’assertions de stratégie personnalisées concernant les liaisons.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-102">Specifies a policy importer that controls the import of custom policy assertions about bindings.</span></span>  
  
 <span data-ttu-id="ce9bf-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="ce9bf-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="ce9bf-104">\<client></span><span class="sxs-lookup"><span data-stu-id="ce9bf-104">\<client></span></span>  
<span data-ttu-id="ce9bf-105">\<metadata></span><span class="sxs-lookup"><span data-stu-id="ce9bf-105">\<metadata></span></span>  
<span data-ttu-id="ce9bf-106">\<policyImporters></span><span class="sxs-lookup"><span data-stu-id="ce9bf-106">\<policyImporters></span></span>  
<span data-ttu-id="ce9bf-107">\<policyImporter></span><span class="sxs-lookup"><span data-stu-id="ce9bf-107">\<policyImporter></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ce9bf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce9bf-108">Syntax</span></span>  
  
```xml  
<metadata>
  <policyImporters>
    <policyImporter type="String" />
  </policyImporters>
</metadata>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ce9bf-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ce9bf-109">Attributes and Elements</span></span>  
 <span data-ttu-id="ce9bf-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ce9bf-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="ce9bf-111">Attributes</span></span>  
  
|<span data-ttu-id="ce9bf-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="ce9bf-112">Attribute</span></span>|<span data-ttu-id="ce9bf-113">Description</span><span class="sxs-lookup"><span data-stu-id="ce9bf-113">Description</span></span>|  
|---------------|-----------------|  
|`type`|<span data-ttu-id="ce9bf-114">Type de cet élément.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-114">The type of this element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ce9bf-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ce9bf-115">Child Elements</span></span>  
 <span data-ttu-id="ce9bf-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-116">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ce9bf-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ce9bf-117">Parent Elements</span></span>  
  
|<span data-ttu-id="ce9bf-118">Élément</span><span class="sxs-lookup"><span data-stu-id="ce9bf-118">Element</span></span>|<span data-ttu-id="ce9bf-119">Description</span><span class="sxs-lookup"><span data-stu-id="ce9bf-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ce9bf-120">\<policyImporters></span><span class="sxs-lookup"><span data-stu-id="ce9bf-120">\<policyImporters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/policyimporters.md)|<span data-ttu-id="ce9bf-121">Indique tous les importateurs de stratégie contrôlant l’importation d’assertions de stratégie personnalisées concernant les liaisons.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-121">Specifies all the policy importers that control the import of custom policy assertions about bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ce9bf-122">Notes</span><span class="sxs-lookup"><span data-stu-id="ce9bf-122">Remarks</span></span>  
 <span data-ttu-id="ce9bf-123">Un importateur de stratégie permet de rechercher des assertions de stratégie personnalisées concernant les fonctionnalités de liaison et de joindre un élément de liaison personnalisé qui implémente les fonctionnalités requises par l’assertion.</span><span class="sxs-lookup"><span data-stu-id="ce9bf-123">A policy importer is used to search custom policy assertions about binding features, as well as attach a custom binding element that implements the features the assertion requires.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ce9bf-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce9bf-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.PolicyImporterElementCollection>
- <xref:System.ServiceModel.Configuration.PolicyImporterElement>
- <xref:System.ServiceModel.Configuration.MetadataElement>
- <xref:System.ServiceModel.Description.MetadataImporter>
- [<span data-ttu-id="ce9bf-125">Configuration du client WCF</span><span class="sxs-lookup"><span data-stu-id="ce9bf-125">WCF Client Configuration</span></span>](../../../../../docs/framework/wcf/feature-details/client-configuration.md)
- [<span data-ttu-id="ce9bf-126">Clients</span><span class="sxs-lookup"><span data-stu-id="ce9bf-126">Clients</span></span>](../../../../../docs/framework/wcf/feature-details/clients.md)
