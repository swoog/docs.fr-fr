---
title: <knownType>
ms.date: 03/30/2017
ms.assetid: ee2b7be3-7148-4a3a-b861-48e7330615e5
ms.openlocfilehash: 4d3dd9042951ffb46b8e0a3f7bb7bcdee23fd58b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61760686"
---
# <a name="knowntype"></a><span data-ttu-id="66123-101">\<knownType></span><span class="sxs-lookup"><span data-stu-id="66123-101">\<knownType></span></span>
<span data-ttu-id="66123-102">Indique un type devant être utilisé par le <xref:System.Runtime.Serialization.DataContractSerializer> pendant la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="66123-102">Specifies a type to be used by <xref:System.Runtime.Serialization.DataContractSerializer> during deserialization.</span></span> <span data-ttu-id="66123-103">L'élément indique un « type connu » renvoyé par un champ ou une propriété d'un « type déclaré ».</span><span class="sxs-lookup"><span data-stu-id="66123-103">The element specifies a "known type" that is returned by a field or property of a "declared type."</span></span> <span data-ttu-id="66123-104">Pour plus d’informations, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span><span class="sxs-lookup"><span data-stu-id="66123-104">For more information, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>  
  
 <span data-ttu-id="66123-105">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="66123-105">\<system.runtime.serialization></span></span>  
<span data-ttu-id="66123-106">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="66123-106">\<dataContractSerializer></span></span>  
<span data-ttu-id="66123-107">\<declaredTypes > élément</span><span class="sxs-lookup"><span data-stu-id="66123-107">\<declaredTypes> Element</span></span>  
<span data-ttu-id="66123-108">\<add> of \<declaredTypes></span><span class="sxs-lookup"><span data-stu-id="66123-108">\<add> of \<declaredTypes></span></span>  
<span data-ttu-id="66123-109">\<knownType > élément</span><span class="sxs-lookup"><span data-stu-id="66123-109">\<knownType> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="66123-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66123-110">Syntax</span></span>  
  
```xml  
<knownType type="String">
  <parameter index="Integer"
             type="String" />
</knownType>
```  
  
## <a name="type"></a><span data-ttu-id="66123-111">Type</span><span class="sxs-lookup"><span data-stu-id="66123-111">Type</span></span>  
 `string`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="66123-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="66123-112">Attributes and Elements</span></span>  
 <span data-ttu-id="66123-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="66123-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="66123-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="66123-114">Attributes</span></span>  
  
|<span data-ttu-id="66123-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="66123-115">Attribute</span></span>|<span data-ttu-id="66123-116">Description</span><span class="sxs-lookup"><span data-stu-id="66123-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="66123-117">type</span><span class="sxs-lookup"><span data-stu-id="66123-117">type</span></span>|<span data-ttu-id="66123-118">Indique le type (espace de noms compris), le nom de l'assembly, la version, la culture et le jeton de clé publique.</span><span class="sxs-lookup"><span data-stu-id="66123-118">Specifies the type (including namespace), assembly name, version, culture, and public key token.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="66123-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="66123-119">Child Elements</span></span>  
  
|<span data-ttu-id="66123-120">Élément</span><span class="sxs-lookup"><span data-stu-id="66123-120">Element</span></span>|<span data-ttu-id="66123-121">Description</span><span class="sxs-lookup"><span data-stu-id="66123-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="66123-122">\<parameter></span><span class="sxs-lookup"><span data-stu-id="66123-122">\<parameter></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/parameter.md)|<span data-ttu-id="66123-123">Indique un index de paramètre lorsque le type déclaré est générique.</span><span class="sxs-lookup"><span data-stu-id="66123-123">Specifies a parameter index when the declared type is a generic type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="66123-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="66123-124">Parent Elements</span></span>  
  
|<span data-ttu-id="66123-125">Élément</span><span class="sxs-lookup"><span data-stu-id="66123-125">Element</span></span>|<span data-ttu-id="66123-126">Description</span><span class="sxs-lookup"><span data-stu-id="66123-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="66123-127">\<add></span><span class="sxs-lookup"><span data-stu-id="66123-127">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)|<span data-ttu-id="66123-128">Ajoute un type déclaré à la collection de types déclarés.</span><span class="sxs-lookup"><span data-stu-id="66123-128">Adds a declared type to the collection of declared types.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="66123-129">Notes</span><span class="sxs-lookup"><span data-stu-id="66123-129">Remarks</span></span>  
 <span data-ttu-id="66123-130">Pour plus d’informations sur les types connus, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) et <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="66123-130">For more information about known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="66123-131">Consultez le [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) pour obtenir un exemple d’utilisation de cet élément.</span><span class="sxs-lookup"><span data-stu-id="66123-131">See the [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) for an example of using this element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="66123-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="66123-132">Example</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="66123-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66123-133">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractSerializer>
- [<span data-ttu-id="66123-134">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="66123-134">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [<span data-ttu-id="66123-135">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="66123-135">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)
- [<span data-ttu-id="66123-136">\<add></span><span class="sxs-lookup"><span data-stu-id="66123-136">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
