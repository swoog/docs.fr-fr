---
title: <parameter>
ms.date: 03/30/2017
ms.assetid: 0fb41e2d-64f7-44ab-993e-05892eac6d82
ms.openlocfilehash: 22ef3c3c6d23d6c68c27d6b5d1ed35b7c9910d48
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59230796"
---
# <a name="parameter"></a><span data-ttu-id="733fd-101">\<parameter></span><span class="sxs-lookup"><span data-stu-id="733fd-101">\<parameter></span></span>
<span data-ttu-id="733fd-102">Indique le paramètre générique lorsqu'un type déclaré est générique.</span><span class="sxs-lookup"><span data-stu-id="733fd-102">Specifies the generic parameter when a declared type is a generic type.</span></span>  
  
 <span data-ttu-id="733fd-103">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="733fd-103">\<system.runtime.serialization></span></span>  
<span data-ttu-id="733fd-104">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="733fd-104">\<dataContractSerializer></span></span>  
<span data-ttu-id="733fd-105">\<declaredTypes > élément</span><span class="sxs-lookup"><span data-stu-id="733fd-105">\<declaredTypes> Element</span></span>  
<span data-ttu-id="733fd-106">\<Ajouter > élément pour \<declaredTypes ></span><span class="sxs-lookup"><span data-stu-id="733fd-106">\<add> element for \<declaredTypes></span></span>  
<span data-ttu-id="733fd-107">\<knownType > élément</span><span class="sxs-lookup"><span data-stu-id="733fd-107">\<knownType> Element</span></span>  
<span data-ttu-id="733fd-108">\<paramètre > élément</span><span class="sxs-lookup"><span data-stu-id="733fd-108">\<parameter> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="733fd-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="733fd-109">Syntax</span></span>  
  
```xml  
<parameter index="Integer"
           type="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="733fd-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="733fd-110">Attributes and Elements</span></span>  
 <span data-ttu-id="733fd-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="733fd-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="733fd-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="733fd-112">Attributes</span></span>  
  
|<span data-ttu-id="733fd-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="733fd-113">Attribute</span></span>|<span data-ttu-id="733fd-114">Description</span><span class="sxs-lookup"><span data-stu-id="733fd-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="733fd-115">index</span><span class="sxs-lookup"><span data-stu-id="733fd-115">index</span></span>|<span data-ttu-id="733fd-116">Lorsque le type déclaré est générique, spécifie le paramètre générique qui renverra le type connu.</span><span class="sxs-lookup"><span data-stu-id="733fd-116">When the declared type is a generic type, specifies the generic parameter that will return the known type.</span></span>|  
|<span data-ttu-id="733fd-117">type</span><span class="sxs-lookup"><span data-stu-id="733fd-117">type</span></span>|<span data-ttu-id="733fd-118">Chaîne décrivant le type connu utilisé pour la sérialisation et la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="733fd-118">A string that describes the known type used for serialization and deserialization.</span></span>|  
  
## <a name="index-attribute"></a><span data-ttu-id="733fd-119">Indexer l'Attribut</span><span class="sxs-lookup"><span data-stu-id="733fd-119">index Attribute</span></span>  
  
|<span data-ttu-id="733fd-120">Value</span><span class="sxs-lookup"><span data-stu-id="733fd-120">Value</span></span>|<span data-ttu-id="733fd-121">Description</span><span class="sxs-lookup"><span data-stu-id="733fd-121">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="733fd-122">"0"</span><span class="sxs-lookup"><span data-stu-id="733fd-122">"0"</span></span>|<span data-ttu-id="733fd-123">Premier paramètre du type générique.</span><span class="sxs-lookup"><span data-stu-id="733fd-123">The first parameter in the generic type.</span></span> <span data-ttu-id="733fd-124">Par exemple, <xref:System.Collections.Generic.List%601> dispose d'un seul paramètre.</span><span class="sxs-lookup"><span data-stu-id="733fd-124">For example, a <xref:System.Collections.Generic.List%601> has only one parameter.</span></span> <span data-ttu-id="733fd-125">S'il est utilisé comme type déclaré, l'index a la valeur « 0 ».</span><span class="sxs-lookup"><span data-stu-id="733fd-125">If it is used as the declared type, the index would be set to "0".</span></span>|  
|<span data-ttu-id="733fd-126">"1"</span><span class="sxs-lookup"><span data-stu-id="733fd-126">"1"</span></span>|<span data-ttu-id="733fd-127">Second paramètre d'un type générique.</span><span class="sxs-lookup"><span data-stu-id="733fd-127">The second parameter in a generic type.</span></span> <span data-ttu-id="733fd-128">Par exemple, <xref:System.Collections.Generic.Dictionary%602> dispose de deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="733fd-128">For example, a <xref:System.Collections.Generic.Dictionary%602> has two parameters.</span></span> <span data-ttu-id="733fd-129">Si le type connu est renvoyé par le second paramètre, affectez à l'attribut d'index la valeur « 1 ».</span><span class="sxs-lookup"><span data-stu-id="733fd-129">If the known type is returned by the second parameter, set the index attribute to "1".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="733fd-130">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="733fd-130">Child Elements</span></span>  
 <span data-ttu-id="733fd-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="733fd-131">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="733fd-132">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="733fd-132">Parent Elements</span></span>  
  
|<span data-ttu-id="733fd-133">Élément</span><span class="sxs-lookup"><span data-stu-id="733fd-133">Element</span></span>|<span data-ttu-id="733fd-134">Description</span><span class="sxs-lookup"><span data-stu-id="733fd-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="733fd-135">\<knownType></span><span class="sxs-lookup"><span data-stu-id="733fd-135">\<knownType></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/knowntype.md)|<span data-ttu-id="733fd-136">Spécifie un type connu pouvant être renvoyé par un champ ou une propriété du type déclaré.</span><span class="sxs-lookup"><span data-stu-id="733fd-136">Specifies a known type that can be returned by a field or property of the declared type.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="733fd-137">Notes</span><span class="sxs-lookup"><span data-stu-id="733fd-137">Remarks</span></span>  
 <span data-ttu-id="733fd-138">Pour plus d’informations sur les types connus, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) et <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="733fd-138">For more information about known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="733fd-139">Consultez le [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) pour obtenir un exemple d’utilisation de cet élément.</span><span class="sxs-lookup"><span data-stu-id="733fd-139">See the [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) for an example of using this element.</span></span>  
  
 <span data-ttu-id="733fd-140">Cet élément de configuration ne peut pas contenir les deux attributs simultanément.</span><span class="sxs-lookup"><span data-stu-id="733fd-140">This configuration element cannot have both attributes at the same time.</span></span> <span data-ttu-id="733fd-141">Si c'est le cas, un <xref:System.Configuration.ConfigurationErrorsException> survient.</span><span class="sxs-lookup"><span data-stu-id="733fd-141">If both attributes are set, a <xref:System.Configuration.ConfigurationErrorsException> occurs.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="733fd-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="733fd-142">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractSerializer>
- [<span data-ttu-id="733fd-143">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="733fd-143">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [<span data-ttu-id="733fd-144">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="733fd-144">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)
- [<span data-ttu-id="733fd-145">\<add></span><span class="sxs-lookup"><span data-stu-id="733fd-145">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
