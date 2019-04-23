---
title: <dataContractSerializer>
ms.date: 03/30/2017
helpviewer_keywords:
- dataContractSerializer element
- <dataContractSerializer> element
- DataContractSerializer
- KnownTypes
ms.assetid: f41fb4d5-24e7-4059-8010-286a30bfea93
ms.openlocfilehash: b635f03d1e4a6628a76d678f7366482717276376
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59116387"
---
# <a name="datacontractserializer"></a><span data-ttu-id="c25bf-101">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="c25bf-101">\<dataContractSerializer></span></span>
<span data-ttu-id="c25bf-102">Contient les données de configuration correspondant au <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="c25bf-102">Contains configuration data for the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span> <span data-ttu-id="c25bf-103">Cet élément se produit dans deux hiérarchies différentes :</span><span class="sxs-lookup"><span data-stu-id="c25bf-103">This element occurs in two different hierarchies.</span></span> <span data-ttu-id="c25bf-104">l'une est répertoriée dans la section Hiérarchie de schéma suivante et l'autre dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c25bf-104">One is listed the following Schema Hierarchy section and the other is listed in the Remarks section.</span></span>  
  
 <span data-ttu-id="c25bf-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="c25bf-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="c25bf-106">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="c25bf-106">\<behaviors></span></span>  
<span data-ttu-id="c25bf-107">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="c25bf-107">\<serviceBehaviors></span></span>  
<span data-ttu-id="c25bf-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="c25bf-108">\<behavior></span></span>  
<span data-ttu-id="c25bf-109">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="c25bf-109">\<dataContractSerializer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c25bf-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c25bf-110">Syntax</span></span>  
  
```xml  
<dataContractSerializer ignoreExtensionDataObject="Boolean"
                        maxItemsInObjectGraph="Integer" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c25bf-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c25bf-111">Attributes and Elements</span></span>  
 <span data-ttu-id="c25bf-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c25bf-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c25bf-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="c25bf-113">Attributes</span></span>  
  
|<span data-ttu-id="c25bf-114">Élément</span><span class="sxs-lookup"><span data-stu-id="c25bf-114">Element</span></span>|<span data-ttu-id="c25bf-115">Description</span><span class="sxs-lookup"><span data-stu-id="c25bf-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c25bf-116">ignoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="c25bf-116">ignoreExtensionDataObject</span></span>|<span data-ttu-id="c25bf-117">Valeur booléenne indiquant si les données fournies par le point de terminaison doivent être ignorées ou non lors d'une sérialisation ou d'une désérialisation.</span><span class="sxs-lookup"><span data-stu-id="c25bf-117">A Boolean value that specifies whether to ignore data supplied by the endpoint when it is being serialized or deserialized.</span></span> <span data-ttu-id="c25bf-118">Cet attribut peut uniquement être défini sur le `<dataContractSerializer>` situé sous l'élément `<behavior>`.</span><span class="sxs-lookup"><span data-stu-id="c25bf-118">This attribute is settable only on the `<dataContractSerializer>` under the `<behavior>` element.</span></span>|  
|<span data-ttu-id="c25bf-119">maxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="c25bf-119">maxItemsInObjectGraph</span></span>|<span data-ttu-id="c25bf-120">Entier indiquant le nombre maximal d'éléments à sérialiser ou à désérialiser.</span><span class="sxs-lookup"><span data-stu-id="c25bf-120">An integer that specifies the maximum number of items to serialize or deserialize.</span></span> <span data-ttu-id="c25bf-121">Cet attribut a la valeur 65 536.</span><span class="sxs-lookup"><span data-stu-id="c25bf-121">This attribute is 65536.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c25bf-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c25bf-122">Child Elements</span></span>  
 <span data-ttu-id="c25bf-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c25bf-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c25bf-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c25bf-124">Parent Elements</span></span>  
  
|<span data-ttu-id="c25bf-125">Élément</span><span class="sxs-lookup"><span data-stu-id="c25bf-125">Element</span></span>|<span data-ttu-id="c25bf-126">Description</span><span class="sxs-lookup"><span data-stu-id="c25bf-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c25bf-127">\<behavior></span><span class="sxs-lookup"><span data-stu-id="c25bf-127">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-servicebehaviors.md)|<span data-ttu-id="c25bf-128">Collection de paramètres correspondant au comportement d’un service.</span><span class="sxs-lookup"><span data-stu-id="c25bf-128">A collection of settings for the behavior of a service.</span></span>|  
|[<span data-ttu-id="c25bf-129">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="c25bf-129">\<system.runtime.serialization></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-runtime-serialization.md)|<span data-ttu-id="c25bf-130">Représente l'élément racine correspondant à la section d'espace de noms <xref:System.Runtime.Serialization> et contient des éléments permettant de définir les options du <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="c25bf-130">Represents the root element for the <xref:System.Runtime.Serialization> namespace section and contains elements for setting options of the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c25bf-131">Notes</span><span class="sxs-lookup"><span data-stu-id="c25bf-131">Remarks</span></span>  
 <span data-ttu-id="c25bf-132">Comme indiqué dans l’Introduction de cette rubrique, il s’agit de la deuxième hiérarchie dans laquelle le \<X509Extension > élément se produit.</span><span class="sxs-lookup"><span data-stu-id="c25bf-132">As stated in the Introduction of this topic, this is the second hierarchy in which the \<X509Extension> element occurs.</span></span>  
  
 [<span data-ttu-id="c25bf-133">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="c25bf-133">\<system.runtime.serialization></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-runtime-serialization.md)  
  
 [<span data-ttu-id="c25bf-134">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="c25bf-134">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)  
  
 <span data-ttu-id="c25bf-135">Pour plus d'informations sur les types connus, consultez <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="c25bf-135">For more information about known types, see <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c25bf-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c25bf-136">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractSerializer>
- <xref:System.ServiceModel.Description.DataContractSerializerOperationBehavior>
- <xref:System.ServiceModel.Configuration.DataContractSerializerElement>
- [<span data-ttu-id="c25bf-137">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="c25bf-137">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [<span data-ttu-id="c25bf-138">Transfert de données et sérialisation</span><span class="sxs-lookup"><span data-stu-id="c25bf-138">Data Transfer and Serialization</span></span>](../../../../../docs/framework/wcf/feature-details/data-transfer-and-serialization.md)
