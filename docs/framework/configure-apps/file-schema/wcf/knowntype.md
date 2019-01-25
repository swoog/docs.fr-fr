---
title: '&lt;knownType&gt;'
ms.date: 03/30/2017
ms.assetid: ee2b7be3-7148-4a3a-b861-48e7330615e5
ms.openlocfilehash: cb36a0d1d1ceb13a6db902904783ee15b14e673b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54541064"
---
# <a name="ltknowntypegt"></a><span data-ttu-id="2ac97-102">&lt;knownType&gt;</span><span class="sxs-lookup"><span data-stu-id="2ac97-102">&lt;knownType&gt;</span></span>
<span data-ttu-id="2ac97-103">Indique un type devant être utilisé par le <xref:System.Runtime.Serialization.DataContractSerializer> pendant la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="2ac97-103">Specifies a type to be used by <xref:System.Runtime.Serialization.DataContractSerializer> during deserialization.</span></span> <span data-ttu-id="2ac97-104">L'élément indique un « type connu » renvoyé par un champ ou une propriété d'un « type déclaré ».</span><span class="sxs-lookup"><span data-stu-id="2ac97-104">The element specifies a "known type" that is returned by a field or property of a "declared type."</span></span> <span data-ttu-id="2ac97-105">Pour plus d’informations, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span><span class="sxs-lookup"><span data-stu-id="2ac97-105">For more information, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>  
  
 <span data-ttu-id="2ac97-106">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="2ac97-106">\<system.runtime.serialization></span></span>  
<span data-ttu-id="2ac97-107">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="2ac97-107">\<dataContractSerializer></span></span>  
<span data-ttu-id="2ac97-108">\<declaredTypes > élément</span><span class="sxs-lookup"><span data-stu-id="2ac97-108">\<declaredTypes> Element</span></span>  
<span data-ttu-id="2ac97-109">\<add> of \<declaredTypes></span><span class="sxs-lookup"><span data-stu-id="2ac97-109">\<add> of \<declaredTypes></span></span>  
<span data-ttu-id="2ac97-110">\<knownType > élément</span><span class="sxs-lookup"><span data-stu-id="2ac97-110">\<knownType> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2ac97-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ac97-111">Syntax</span></span>  
  
```xml  
<knownType type="String">
  <parameter index="Integer"
             type="String" />
</knownType>
```  
  
## <a name="type"></a><span data-ttu-id="2ac97-112">Type</span><span class="sxs-lookup"><span data-stu-id="2ac97-112">Type</span></span>  
 `string`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2ac97-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="2ac97-113">Attributes and Elements</span></span>  
 <span data-ttu-id="2ac97-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="2ac97-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2ac97-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="2ac97-115">Attributes</span></span>  
  
|<span data-ttu-id="2ac97-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="2ac97-116">Attribute</span></span>|<span data-ttu-id="2ac97-117">Description</span><span class="sxs-lookup"><span data-stu-id="2ac97-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="2ac97-118">type</span><span class="sxs-lookup"><span data-stu-id="2ac97-118">type</span></span>|<span data-ttu-id="2ac97-119">Indique le type (espace de noms compris), le nom de l'assembly, la version, la culture et le jeton de clé publique.</span><span class="sxs-lookup"><span data-stu-id="2ac97-119">Specifies the type (including namespace), assembly name, version, culture, and public key token.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2ac97-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2ac97-120">Child Elements</span></span>  
  
|<span data-ttu-id="2ac97-121">Élément</span><span class="sxs-lookup"><span data-stu-id="2ac97-121">Element</span></span>|<span data-ttu-id="2ac97-122">Description</span><span class="sxs-lookup"><span data-stu-id="2ac97-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2ac97-123">\<parameter></span><span class="sxs-lookup"><span data-stu-id="2ac97-123">\<parameter></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/parameter.md)|<span data-ttu-id="2ac97-124">Indique un index de paramètre lorsque le type déclaré est générique.</span><span class="sxs-lookup"><span data-stu-id="2ac97-124">Specifies a parameter index when the declared type is a generic type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="2ac97-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2ac97-125">Parent Elements</span></span>  
  
|<span data-ttu-id="2ac97-126">Élément</span><span class="sxs-lookup"><span data-stu-id="2ac97-126">Element</span></span>|<span data-ttu-id="2ac97-127">Description</span><span class="sxs-lookup"><span data-stu-id="2ac97-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2ac97-128">\<add></span><span class="sxs-lookup"><span data-stu-id="2ac97-128">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)|<span data-ttu-id="2ac97-129">Ajoute un type déclaré à la collection de types déclarés.</span><span class="sxs-lookup"><span data-stu-id="2ac97-129">Adds a declared type to the collection of declared types.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2ac97-130">Notes</span><span class="sxs-lookup"><span data-stu-id="2ac97-130">Remarks</span></span>  
 <span data-ttu-id="2ac97-131">Pour plus d’informations sur les types connus, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) et <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="2ac97-131">For more information about known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="2ac97-132">Consultez le [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) pour obtenir un exemple d’utilisation de cet élément.</span><span class="sxs-lookup"><span data-stu-id="2ac97-132">See the [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) for an example of using this element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2ac97-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="2ac97-133">Example</span></span>  
  
```xml  
<add type="MyCompany.Library.Shape,
           MyAssembly, Version=2.0.0.0, Culture=neutral,
           PublicKeyToken=XXXXXX, processorArchitecture=MSIL">
  <knownType type="MyCompany.Library.Circle,
                   MyAssembly, Version=2.0.0.0, Culture=neutral,
                   PublicKeyToken=XXXXXX,
                   processorArchitecture=MSIL"/>
</add>
```  
  
## <a name="see-also"></a><span data-ttu-id="2ac97-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ac97-134">See also</span></span>
- <xref:System.Runtime.Serialization.DataContractSerializer>
- [<span data-ttu-id="2ac97-135">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="2ac97-135">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [<span data-ttu-id="2ac97-136">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="2ac97-136">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)
- [<span data-ttu-id="2ac97-137">\<add></span><span class="sxs-lookup"><span data-stu-id="2ac97-137">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
