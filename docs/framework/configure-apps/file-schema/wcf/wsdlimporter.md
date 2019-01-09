---
title: '&lt;wsdlImporter&gt;'
ms.date: 03/30/2017
ms.assetid: 986b2165-8430-4dba-b1b8-00396841bb96
ms.openlocfilehash: 43c1a50c740cd9c75ee641e4ac4d0fa8ea3ca36b
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54144988"
---
# <a name="ltwsdlimportergt"></a><span data-ttu-id="2e85a-102">&lt;wsdlImporter&gt;</span><span class="sxs-lookup"><span data-stu-id="2e85a-102">&lt;wsdlImporter&gt;</span></span>
<span data-ttu-id="2e85a-103">Indique tous les importateurs WSDL qui importent des métadonnées WSDL (Web Services Description Language) 1.1 avec des pièces jointes WS-Policy.</span><span class="sxs-lookup"><span data-stu-id="2e85a-103">Specifies all the WSDL importers that imports Web Services Description Language (WSDL) 1.1 metadata with WS-Policy attachments.</span></span>  
  
<span data-ttu-id="2e85a-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="2e85a-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="2e85a-105">\<client></span><span class="sxs-lookup"><span data-stu-id="2e85a-105">\<client></span></span>  
<span data-ttu-id="2e85a-106">\<métadonnées ></span><span class="sxs-lookup"><span data-stu-id="2e85a-106">\<metadata></span></span>  
<span data-ttu-id="2e85a-107">\<wsdlImporters ></span><span class="sxs-lookup"><span data-stu-id="2e85a-107">\<wsdlImporters></span></span>  
<span data-ttu-id="2e85a-108">\<wsdlImporter ></span><span class="sxs-lookup"><span data-stu-id="2e85a-108">\<wsdlImporter></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2e85a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e85a-109">Syntax</span></span>  
  
```xml  
<metadata>
  <wsdlImporters>
    <wsdlImporter type="string" />
  </wsdlImporters>
</metadata>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2e85a-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="2e85a-110">Attributes and Elements</span></span>  
 <span data-ttu-id="2e85a-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="2e85a-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2e85a-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="2e85a-112">Attributes</span></span>  
  
|<span data-ttu-id="2e85a-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="2e85a-113">Attribute</span></span>|<span data-ttu-id="2e85a-114">Description</span><span class="sxs-lookup"><span data-stu-id="2e85a-114">Description</span></span>|  
|---------------|-----------------|  
|`type`|<span data-ttu-id="2e85a-115">Type de cet élément.</span><span class="sxs-lookup"><span data-stu-id="2e85a-115">The type of this element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2e85a-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2e85a-116">Child Elements</span></span>  
 <span data-ttu-id="2e85a-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2e85a-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2e85a-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2e85a-118">Parent Elements</span></span>  
  
|<span data-ttu-id="2e85a-119">Élément</span><span class="sxs-lookup"><span data-stu-id="2e85a-119">Element</span></span>|<span data-ttu-id="2e85a-120">Description</span><span class="sxs-lookup"><span data-stu-id="2e85a-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2e85a-121">\<wsdlImporters ></span><span class="sxs-lookup"><span data-stu-id="2e85a-121">\<wsdlImporters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdlimporters.md)|<span data-ttu-id="2e85a-122">Indique tous les importateurs WSDL qui importent des métadonnées WSDL (Web Services Description Language) 1.1 avec des pièces jointes WS-Policy.</span><span class="sxs-lookup"><span data-stu-id="2e85a-122">Specifies all the WSDL importers that imports Web Services Description Language (WSDL) 1.1 metadata with WS-Policy attachments.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2e85a-123">Notes</span><span class="sxs-lookup"><span data-stu-id="2e85a-123">Remarks</span></span>  
 <span data-ttu-id="2e85a-124">Un importateur WSDL permet d'importer des métadonnées et de convertir ces informations en différentes classes représentant les informations de contrat et de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="2e85a-124">A WSDL importer is used to import metadata as well as convert that information into various classes that represent contract and endpoint information.</span></span> <span data-ttu-id="2e85a-125">Il peut importer sélectivement des informations de contrat et de point de terminaison ainsi que des propriétés qui exposent toute erreur d'importation et accepte des informations de types liées au processus d'importation et de conversion.</span><span class="sxs-lookup"><span data-stu-id="2e85a-125">It can selectively import contract and endpoint information and properties that expose any import errors and accept type information relevant to the import and conversion process.</span></span> <span data-ttu-id="2e85a-126">Il prend également en charge les informations et les propriétés de liaison qui donnent accès aux documents de stratégie, documents WSDL, extensions WSDL et documents de schéma XML.</span><span class="sxs-lookup"><span data-stu-id="2e85a-126">It also supports importing binding information and properties that provide access to any policy documents, WSDL documents, WSDL extensions, and XML schema documents.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2e85a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e85a-127">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.WsdlImporterElement>  
 <xref:System.ServiceModel.Configuration.MetadataElement>  
 <xref:System.ServiceModel.Configuration.WsdlImporterElementCollection>  
 <xref:System.ServiceModel.Description.MetadataImporter>  
 <xref:System.ServiceModel.Description.WsdlImporter>  
 [<span data-ttu-id="2e85a-128">Configuration du client WCF</span><span class="sxs-lookup"><span data-stu-id="2e85a-128">WCF Client Configuration</span></span>](../../../../../docs/framework/wcf/feature-details/client-configuration.md)  
 [<span data-ttu-id="2e85a-129">Clients</span><span class="sxs-lookup"><span data-stu-id="2e85a-129">Clients</span></span>](../../../../../docs/framework/wcf/feature-details/clients.md)
