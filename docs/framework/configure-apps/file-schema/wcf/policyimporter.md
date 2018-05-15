---
title: '&lt;policyImporter&gt;'
ms.date: 03/30/2017
ms.assetid: b0d03456-546f-44bb-ab12-1b2ce7f98fca
ms.openlocfilehash: 7483a95accef0a4bc956d919087379363b4762ca
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltpolicyimportergt"></a><span data-ttu-id="59c3e-102">&lt;policyImporter&gt;</span><span class="sxs-lookup"><span data-stu-id="59c3e-102">&lt;policyImporter&gt;</span></span>
<span data-ttu-id="59c3e-103">Indique un importateur de stratégie qui contrôle l’importation d’assertions de stratégie personnalisées concernant les liaisons.</span><span class="sxs-lookup"><span data-stu-id="59c3e-103">Specifies a policy importer that controls the import of custom policy assertions about bindings.</span></span>  
  
 <span data-ttu-id="59c3e-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="59c3e-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="59c3e-105">\<client></span><span class="sxs-lookup"><span data-stu-id="59c3e-105">\<client></span></span>  
<span data-ttu-id="59c3e-106">\<métadonnées ></span><span class="sxs-lookup"><span data-stu-id="59c3e-106">\<metadata></span></span>  
<span data-ttu-id="59c3e-107">\<policyImporters ></span><span class="sxs-lookup"><span data-stu-id="59c3e-107">\<policyImporters></span></span>  
<span data-ttu-id="59c3e-108">\<policyImporter ></span><span class="sxs-lookup"><span data-stu-id="59c3e-108">\<policyImporter></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="59c3e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59c3e-109">Syntax</span></span>  
  
```xml  
<metadata>  
   <policyImporters>  
      <policyImporter type="string" />  
   </policyImporters>  
</metadata>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="59c3e-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="59c3e-110">Attributes and Elements</span></span>  
 <span data-ttu-id="59c3e-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="59c3e-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="59c3e-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="59c3e-112">Attributes</span></span>  
  
|<span data-ttu-id="59c3e-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="59c3e-113">Attribute</span></span>|<span data-ttu-id="59c3e-114">Description</span><span class="sxs-lookup"><span data-stu-id="59c3e-114">Description</span></span>|  
|---------------|-----------------|  
|`type`|<span data-ttu-id="59c3e-115">Type de cet élément.</span><span class="sxs-lookup"><span data-stu-id="59c3e-115">The type of this element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="59c3e-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="59c3e-116">Child Elements</span></span>  
 <span data-ttu-id="59c3e-117">Aucun</span><span class="sxs-lookup"><span data-stu-id="59c3e-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="59c3e-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="59c3e-118">Parent Elements</span></span>  
  
|<span data-ttu-id="59c3e-119">Élément</span><span class="sxs-lookup"><span data-stu-id="59c3e-119">Element</span></span>|<span data-ttu-id="59c3e-120">Description</span><span class="sxs-lookup"><span data-stu-id="59c3e-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="59c3e-121">\<policyImporters ></span><span class="sxs-lookup"><span data-stu-id="59c3e-121">\<policyImporters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/policyimporters.md)|<span data-ttu-id="59c3e-122">Indique tous les importateurs de stratégie contrôlant l’importation d’assertions de stratégie personnalisées concernant les liaisons.</span><span class="sxs-lookup"><span data-stu-id="59c3e-122">Specifies all the policy importers that control the import of custom policy assertions about bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="59c3e-123">Notes</span><span class="sxs-lookup"><span data-stu-id="59c3e-123">Remarks</span></span>  
 <span data-ttu-id="59c3e-124">Un importateur de stratégie permet de rechercher des assertions de stratégie personnalisées concernant les fonctionnalités de liaison et de joindre un élément de liaison personnalisé qui implémente les fonctionnalités requises par l’assertion.</span><span class="sxs-lookup"><span data-stu-id="59c3e-124">A policy importer is used to search custom policy assertions about binding features, as well as attach a custom binding element that implements the features the assertion requires.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59c3e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59c3e-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PolicyImporterElementCollection>  
 <xref:System.ServiceModel.Configuration.PolicyImporterElement>  
 <xref:System.ServiceModel.Configuration.MetadataElement>  
 <xref:System.ServiceModel.Description.MetadataImporter>  
 [<span data-ttu-id="59c3e-126">Configuration du client WCF</span><span class="sxs-lookup"><span data-stu-id="59c3e-126">WCF Client Configuration</span></span>](../../../../../docs/framework/wcf/feature-details/client-configuration.md)  
 [<span data-ttu-id="59c3e-127">Clients</span><span class="sxs-lookup"><span data-stu-id="59c3e-127">Clients</span></span>](../../../../../docs/framework/wcf/feature-details/clients.md)
