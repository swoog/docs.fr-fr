---
title: '&lt;DataContractSerializer&gt;'
ms.date: 03/30/2017
helpviewer_keywords:
- dataContractSerializer element
- <dataContractSerializer> element
- DataContractSerializer
- KnownTypes
ms.assetid: f41fb4d5-24e7-4059-8010-286a30bfea93
ms.openlocfilehash: 5f2a05fdf2e38923205092b232995a70a87f7e87
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltdatacontractserializergt"></a><span data-ttu-id="506e1-102">&lt;DataContractSerializer&gt;</span><span class="sxs-lookup"><span data-stu-id="506e1-102">&lt;dataContractSerializer&gt;</span></span>
<span data-ttu-id="506e1-103">Contient les données de configuration correspondant au <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="506e1-103">Contains configuration data for the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span> <span data-ttu-id="506e1-104">Cet élément se produit dans deux hiérarchies différentes :</span><span class="sxs-lookup"><span data-stu-id="506e1-104">This element occurs in two different hierarchies.</span></span> <span data-ttu-id="506e1-105">l'une est répertoriée dans la section Hiérarchie de schéma suivante et l'autre dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="506e1-105">One is listed the following Schema Hierarchy section and the other is listed in the Remarks section.</span></span>  
  
 <span data-ttu-id="506e1-106">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="506e1-106">\<system.ServiceModel></span></span>  
<span data-ttu-id="506e1-107">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="506e1-107">\<behaviors></span></span>  
<span data-ttu-id="506e1-108">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="506e1-108">\<serviceBehaviors></span></span>  
<span data-ttu-id="506e1-109">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="506e1-109">\<behavior></span></span>  
<span data-ttu-id="506e1-110">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="506e1-110">\<dataContractSerializer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="506e1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="506e1-111">Syntax</span></span>  
  
```xml  
<dataContractSerializer ignoreExtensionDataObject="Boolean"  
   maxItemsInObjectGraph="Integer" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="506e1-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="506e1-112">Attributes and Elements</span></span>  
 <span data-ttu-id="506e1-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="506e1-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="506e1-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="506e1-114">Attributes</span></span>  
  
|<span data-ttu-id="506e1-115">Élément</span><span class="sxs-lookup"><span data-stu-id="506e1-115">Element</span></span>|<span data-ttu-id="506e1-116">Description</span><span class="sxs-lookup"><span data-stu-id="506e1-116">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="506e1-117">ignoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="506e1-117">ignoreExtensionDataObject</span></span>|<span data-ttu-id="506e1-118">Valeur booléenne indiquant si les données fournies par le point de terminaison doivent être ignorées ou non lors d'une sérialisation ou d'une désérialisation.</span><span class="sxs-lookup"><span data-stu-id="506e1-118">A Boolean value that specifies whether to ignore data supplied by the endpoint when it is being serialized or deserialized.</span></span> <span data-ttu-id="506e1-119">Cet attribut peut uniquement être défini sur le `<dataContractSerializer>` situé sous l'élément `<behavior>`.</span><span class="sxs-lookup"><span data-stu-id="506e1-119">This attribute is settable only on the `<dataContractSerializer>` under the `<behavior>` element.</span></span>|  
|<span data-ttu-id="506e1-120">maxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="506e1-120">maxItemsInObjectGraph</span></span>|<span data-ttu-id="506e1-121">Entier indiquant le nombre maximal d'éléments à sérialiser ou à désérialiser.</span><span class="sxs-lookup"><span data-stu-id="506e1-121">An integer that specifies the maximum number of items to serialize or deserialize.</span></span> <span data-ttu-id="506e1-122">Cet attribut a la valeur 65 536.</span><span class="sxs-lookup"><span data-stu-id="506e1-122">This attribute is 65536.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="506e1-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="506e1-123">Child Elements</span></span>  
 <span data-ttu-id="506e1-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="506e1-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="506e1-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="506e1-125">Parent Elements</span></span>  
  
|<span data-ttu-id="506e1-126">Élément</span><span class="sxs-lookup"><span data-stu-id="506e1-126">Element</span></span>|<span data-ttu-id="506e1-127">Description</span><span class="sxs-lookup"><span data-stu-id="506e1-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="506e1-128">\<behavior></span><span class="sxs-lookup"><span data-stu-id="506e1-128">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-servicebehaviors.md)|<span data-ttu-id="506e1-129">Collection de paramètres correspondant au comportement d’un service.</span><span class="sxs-lookup"><span data-stu-id="506e1-129">A collection of settings for the behavior of a service.</span></span>|  
|[<span data-ttu-id="506e1-130">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="506e1-130">\<system.runtime.serialization></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-runtime-serialization.md)|<span data-ttu-id="506e1-131">Représente l'élément racine correspondant à la section d'espace de noms <xref:System.Runtime.Serialization> et contient des éléments permettant de définir les options du <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="506e1-131">Represents the root element for the <xref:System.Runtime.Serialization> namespace section and contains elements for setting options of the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="506e1-132">Notes</span><span class="sxs-lookup"><span data-stu-id="506e1-132">Remarks</span></span>  
 <span data-ttu-id="506e1-133">Comme indiqué dans l’Introduction de cette rubrique, il s’agit de la deuxième hiérarchie dans laquelle le \<X509Extension > élément se produit.</span><span class="sxs-lookup"><span data-stu-id="506e1-133">As stated in the Introduction of this topic, this is the second hierarchy in which the \<X509Extension> element occurs.</span></span>  
  
 [<span data-ttu-id="506e1-134">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="506e1-134">\<system.runtime.serialization></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-runtime-serialization.md)  
  
 [<span data-ttu-id="506e1-135">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="506e1-135">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)  
  
 <span data-ttu-id="506e1-136">Pour plus d'informations sur les types connus, consultez <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="506e1-136">For more information about known types, see <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="506e1-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="506e1-137">See Also</span></span>  
 <xref:System.Runtime.Serialization.DataContractSerializer>  
 <xref:System.ServiceModel.Description.DataContractSerializerOperationBehavior>  
 <xref:System.ServiceModel.Configuration.DataContractSerializerElement>  
 [<span data-ttu-id="506e1-138">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="506e1-138">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)  
 [<span data-ttu-id="506e1-139">Transfert de données et sérialisation</span><span class="sxs-lookup"><span data-stu-id="506e1-139">Data Transfer and Serialization</span></span>](../../../../../docs/framework/wcf/feature-details/data-transfer-and-serialization.md)
