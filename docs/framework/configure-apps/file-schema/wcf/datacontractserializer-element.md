---
title: <dataContractSerializer>
ms.date: 03/30/2017
helpviewer_keywords:
- dataContractSerializer element
- <dataContractSerializer> element
- DataContractSerializer
- KnownTypes
ms.assetid: f41fb4d5-24e7-4059-8010-286a30bfea93
ms.openlocfilehash: 1b4fd959d5e522150751d2e9b8be8c5b2252bf27
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55254949"
---
# <a name="datacontractserializer"></a><span data-ttu-id="5e3b7-101">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="5e3b7-101">\<dataContractSerializer></span></span>
<span data-ttu-id="5e3b7-102">Contient les données de configuration correspondant au <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-102">Contains configuration data for the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span> <span data-ttu-id="5e3b7-103">Cet élément se produit dans deux hiérarchies différentes :</span><span class="sxs-lookup"><span data-stu-id="5e3b7-103">This element occurs in two different hierarchies.</span></span> <span data-ttu-id="5e3b7-104">l'une est répertoriée dans la section Hiérarchie de schéma suivante et l'autre dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-104">One is listed the following Schema Hierarchy section and the other is listed in the Remarks section.</span></span>  
  
 <span data-ttu-id="5e3b7-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="5e3b7-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="5e3b7-106">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="5e3b7-106">\<behaviors></span></span>  
<span data-ttu-id="5e3b7-107">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="5e3b7-107">\<serviceBehaviors></span></span>  
<span data-ttu-id="5e3b7-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="5e3b7-108">\<behavior></span></span>  
<span data-ttu-id="5e3b7-109">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="5e3b7-109">\<dataContractSerializer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e3b7-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e3b7-110">Syntax</span></span>  
  
```xml  
<dataContractSerializer ignoreExtensionDataObject="Boolean"
                        maxItemsInObjectGraph="Integer" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5e3b7-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5e3b7-111">Attributes and Elements</span></span>  
 <span data-ttu-id="5e3b7-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5e3b7-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="5e3b7-113">Attributes</span></span>  
  
|<span data-ttu-id="5e3b7-114">Élément</span><span class="sxs-lookup"><span data-stu-id="5e3b7-114">Element</span></span>|<span data-ttu-id="5e3b7-115">Description</span><span class="sxs-lookup"><span data-stu-id="5e3b7-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="5e3b7-116">ignoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="5e3b7-116">ignoreExtensionDataObject</span></span>|<span data-ttu-id="5e3b7-117">Valeur booléenne indiquant si les données fournies par le point de terminaison doivent être ignorées ou non lors d'une sérialisation ou d'une désérialisation.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-117">A Boolean value that specifies whether to ignore data supplied by the endpoint when it is being serialized or deserialized.</span></span> <span data-ttu-id="5e3b7-118">Cet attribut peut uniquement être défini sur le `<dataContractSerializer>` situé sous l'élément `<behavior>`.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-118">This attribute is settable only on the `<dataContractSerializer>` under the `<behavior>` element.</span></span>|  
|<span data-ttu-id="5e3b7-119">maxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="5e3b7-119">maxItemsInObjectGraph</span></span>|<span data-ttu-id="5e3b7-120">Entier indiquant le nombre maximal d'éléments à sérialiser ou à désérialiser.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-120">An integer that specifies the maximum number of items to serialize or deserialize.</span></span> <span data-ttu-id="5e3b7-121">Cet attribut a la valeur 65 536.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-121">This attribute is 65536.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5e3b7-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5e3b7-122">Child Elements</span></span>  
 <span data-ttu-id="5e3b7-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5e3b7-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5e3b7-124">Parent Elements</span></span>  
  
|<span data-ttu-id="5e3b7-125">Élément</span><span class="sxs-lookup"><span data-stu-id="5e3b7-125">Element</span></span>|<span data-ttu-id="5e3b7-126">Description</span><span class="sxs-lookup"><span data-stu-id="5e3b7-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5e3b7-127">\<behavior></span><span class="sxs-lookup"><span data-stu-id="5e3b7-127">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-servicebehaviors.md)|<span data-ttu-id="5e3b7-128">Collection de paramètres correspondant au comportement d’un service.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-128">A collection of settings for the behavior of a service.</span></span>|  
|[<span data-ttu-id="5e3b7-129">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="5e3b7-129">\<system.runtime.serialization></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-runtime-serialization.md)|<span data-ttu-id="5e3b7-130">Représente l'élément racine correspondant à la section d'espace de noms <xref:System.Runtime.Serialization> et contient des éléments permettant de définir les options du <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-130">Represents the root element for the <xref:System.Runtime.Serialization> namespace section and contains elements for setting options of the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5e3b7-131">Notes</span><span class="sxs-lookup"><span data-stu-id="5e3b7-131">Remarks</span></span>  
 <span data-ttu-id="5e3b7-132">Comme indiqué dans l’Introduction de cette rubrique, il s’agit de la deuxième hiérarchie dans laquelle le \<X509Extension > élément se produit.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-132">As stated in the Introduction of this topic, this is the second hierarchy in which the \<X509Extension> element occurs.</span></span>  
  
 [<span data-ttu-id="5e3b7-133">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="5e3b7-133">\<system.runtime.serialization></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-runtime-serialization.md)  
  
 [<span data-ttu-id="5e3b7-134">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="5e3b7-134">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)  
  
 <span data-ttu-id="5e3b7-135">Pour plus d'informations sur les types connus, consultez <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-135">For more information about known types, see <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e3b7-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e3b7-136">See also</span></span>
- <xref:System.Runtime.Serialization.DataContractSerializer>
- <xref:System.ServiceModel.Description.DataContractSerializerOperationBehavior>
- <xref:System.ServiceModel.Configuration.DataContractSerializerElement>
- [<span data-ttu-id="5e3b7-137">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="5e3b7-137">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [<span data-ttu-id="5e3b7-138">Transfert de données et sérialisation</span><span class="sxs-lookup"><span data-stu-id="5e3b7-138">Data Transfer and Serialization</span></span>](../../../../../docs/framework/wcf/feature-details/data-transfer-and-serialization.md)
