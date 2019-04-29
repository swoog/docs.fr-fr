---
title: <parameter>
ms.date: 03/30/2017
ms.assetid: 0fb41e2d-64f7-44ab-993e-05892eac6d82
ms.openlocfilehash: 22ef3c3c6d23d6c68c27d6b5d1ed35b7c9910d48
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61783433"
---
# <a name="parameter"></a><span data-ttu-id="c1a56-101">\<parameter></span><span class="sxs-lookup"><span data-stu-id="c1a56-101">\<parameter></span></span>
<span data-ttu-id="c1a56-102">Indique le paramètre générique lorsqu'un type déclaré est générique.</span><span class="sxs-lookup"><span data-stu-id="c1a56-102">Specifies the generic parameter when a declared type is a generic type.</span></span>  
  
 <span data-ttu-id="c1a56-103">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="c1a56-103">\<system.runtime.serialization></span></span>  
<span data-ttu-id="c1a56-104">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="c1a56-104">\<dataContractSerializer></span></span>  
<span data-ttu-id="c1a56-105">\<declaredTypes > élément</span><span class="sxs-lookup"><span data-stu-id="c1a56-105">\<declaredTypes> Element</span></span>  
<span data-ttu-id="c1a56-106">\<Ajouter > élément pour \<declaredTypes ></span><span class="sxs-lookup"><span data-stu-id="c1a56-106">\<add> element for \<declaredTypes></span></span>  
<span data-ttu-id="c1a56-107">\<knownType > élément</span><span class="sxs-lookup"><span data-stu-id="c1a56-107">\<knownType> Element</span></span>  
<span data-ttu-id="c1a56-108">\<paramètre > élément</span><span class="sxs-lookup"><span data-stu-id="c1a56-108">\<parameter> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c1a56-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1a56-109">Syntax</span></span>  
  
```xml  
<parameter index="Integer"
           type="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c1a56-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c1a56-110">Attributes and Elements</span></span>  
 <span data-ttu-id="c1a56-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c1a56-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c1a56-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="c1a56-112">Attributes</span></span>  
  
|<span data-ttu-id="c1a56-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="c1a56-113">Attribute</span></span>|<span data-ttu-id="c1a56-114">Description</span><span class="sxs-lookup"><span data-stu-id="c1a56-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c1a56-115">index</span><span class="sxs-lookup"><span data-stu-id="c1a56-115">index</span></span>|<span data-ttu-id="c1a56-116">Lorsque le type déclaré est générique, spécifie le paramètre générique qui renverra le type connu.</span><span class="sxs-lookup"><span data-stu-id="c1a56-116">When the declared type is a generic type, specifies the generic parameter that will return the known type.</span></span>|  
|<span data-ttu-id="c1a56-117">type</span><span class="sxs-lookup"><span data-stu-id="c1a56-117">type</span></span>|<span data-ttu-id="c1a56-118">Chaîne décrivant le type connu utilisé pour la sérialisation et la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="c1a56-118">A string that describes the known type used for serialization and deserialization.</span></span>|  
  
## <a name="index-attribute"></a><span data-ttu-id="c1a56-119">Indexer l'Attribut</span><span class="sxs-lookup"><span data-stu-id="c1a56-119">index Attribute</span></span>  
  
|<span data-ttu-id="c1a56-120">Value</span><span class="sxs-lookup"><span data-stu-id="c1a56-120">Value</span></span>|<span data-ttu-id="c1a56-121">Description</span><span class="sxs-lookup"><span data-stu-id="c1a56-121">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="c1a56-122">"0"</span><span class="sxs-lookup"><span data-stu-id="c1a56-122">"0"</span></span>|<span data-ttu-id="c1a56-123">Premier paramètre du type générique.</span><span class="sxs-lookup"><span data-stu-id="c1a56-123">The first parameter in the generic type.</span></span> <span data-ttu-id="c1a56-124">Par exemple, <xref:System.Collections.Generic.List%601> dispose d'un seul paramètre.</span><span class="sxs-lookup"><span data-stu-id="c1a56-124">For example, a <xref:System.Collections.Generic.List%601> has only one parameter.</span></span> <span data-ttu-id="c1a56-125">S'il est utilisé comme type déclaré, l'index a la valeur « 0 ».</span><span class="sxs-lookup"><span data-stu-id="c1a56-125">If it is used as the declared type, the index would be set to "0".</span></span>|  
|<span data-ttu-id="c1a56-126">"1"</span><span class="sxs-lookup"><span data-stu-id="c1a56-126">"1"</span></span>|<span data-ttu-id="c1a56-127">Second paramètre d'un type générique.</span><span class="sxs-lookup"><span data-stu-id="c1a56-127">The second parameter in a generic type.</span></span> <span data-ttu-id="c1a56-128">Par exemple, <xref:System.Collections.Generic.Dictionary%602> dispose de deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="c1a56-128">For example, a <xref:System.Collections.Generic.Dictionary%602> has two parameters.</span></span> <span data-ttu-id="c1a56-129">Si le type connu est renvoyé par le second paramètre, affectez à l'attribut d'index la valeur « 1 ».</span><span class="sxs-lookup"><span data-stu-id="c1a56-129">If the known type is returned by the second parameter, set the index attribute to "1".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c1a56-130">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c1a56-130">Child Elements</span></span>  
 <span data-ttu-id="c1a56-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c1a56-131">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c1a56-132">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c1a56-132">Parent Elements</span></span>  
  
|<span data-ttu-id="c1a56-133">Élément</span><span class="sxs-lookup"><span data-stu-id="c1a56-133">Element</span></span>|<span data-ttu-id="c1a56-134">Description</span><span class="sxs-lookup"><span data-stu-id="c1a56-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c1a56-135">\<knownType></span><span class="sxs-lookup"><span data-stu-id="c1a56-135">\<knownType></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/knowntype.md)|<span data-ttu-id="c1a56-136">Spécifie un type connu pouvant être renvoyé par un champ ou une propriété du type déclaré.</span><span class="sxs-lookup"><span data-stu-id="c1a56-136">Specifies a known type that can be returned by a field or property of the declared type.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c1a56-137">Notes</span><span class="sxs-lookup"><span data-stu-id="c1a56-137">Remarks</span></span>  
 <span data-ttu-id="c1a56-138">Pour plus d’informations sur les types connus, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) et <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="c1a56-138">For more information about known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="c1a56-139">Consultez le [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) pour obtenir un exemple d’utilisation de cet élément.</span><span class="sxs-lookup"><span data-stu-id="c1a56-139">See the [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) for an example of using this element.</span></span>  
  
 <span data-ttu-id="c1a56-140">Cet élément de configuration ne peut pas contenir les deux attributs simultanément.</span><span class="sxs-lookup"><span data-stu-id="c1a56-140">This configuration element cannot have both attributes at the same time.</span></span> <span data-ttu-id="c1a56-141">Si c'est le cas, un <xref:System.Configuration.ConfigurationErrorsException> survient.</span><span class="sxs-lookup"><span data-stu-id="c1a56-141">If both attributes are set, a <xref:System.Configuration.ConfigurationErrorsException> occurs.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c1a56-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1a56-142">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractSerializer>
- [<span data-ttu-id="c1a56-143">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="c1a56-143">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [<span data-ttu-id="c1a56-144">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="c1a56-144">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)
- [<span data-ttu-id="c1a56-145">\<add></span><span class="sxs-lookup"><span data-stu-id="c1a56-145">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
