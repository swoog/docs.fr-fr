---
title: '&lt;knownType&gt;'
ms.date: 03/30/2017
ms.assetid: ee2b7be3-7148-4a3a-b861-48e7330615e5
ms.openlocfilehash: b2445f12f1eaac03b3f3ab66f3d13a5f465a1133
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltknowntypegt"></a><span data-ttu-id="c4fc1-102">&lt;knownType&gt;</span><span class="sxs-lookup"><span data-stu-id="c4fc1-102">&lt;knownType&gt;</span></span>
<span data-ttu-id="c4fc1-103">Indique un type devant être utilisé par le <xref:System.Runtime.Serialization.DataContractSerializer> pendant la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="c4fc1-103">Specifies a type to be used by <xref:System.Runtime.Serialization.DataContractSerializer> during deserialization.</span></span> <span data-ttu-id="c4fc1-104">L'élément indique un « type connu » renvoyé par un champ ou une propriété d'un « type déclaré ».</span><span class="sxs-lookup"><span data-stu-id="c4fc1-104">The element specifies a "known type" that is returned by a field or property of a "declared type."</span></span> <span data-ttu-id="c4fc1-105">Pour plus d’informations, consultez [Types connus de contrat de données](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span><span class="sxs-lookup"><span data-stu-id="c4fc1-105">For more information, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>  
  
 <span data-ttu-id="c4fc1-106">\<System.Runtime.Serialization ></span><span class="sxs-lookup"><span data-stu-id="c4fc1-106">\<system.runtime.serialization></span></span>  
<span data-ttu-id="c4fc1-107">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="c4fc1-107">\<dataContractSerializer></span></span>  
<span data-ttu-id="c4fc1-108">\<declaredTypes > élément</span><span class="sxs-lookup"><span data-stu-id="c4fc1-108">\<declaredTypes> Element</span></span>  
<span data-ttu-id="c4fc1-109">\<Ajouter > de \<declaredTypes ></span><span class="sxs-lookup"><span data-stu-id="c4fc1-109">\<add> of \<declaredTypes></span></span>  
<span data-ttu-id="c4fc1-110">\<knownType > élément</span><span class="sxs-lookup"><span data-stu-id="c4fc1-110">\<knownType> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4fc1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4fc1-111">Syntax</span></span>  
  
```xml  
<knownType type="String">  
     <parameter index="Integer"  
                type="String" />  
</knownType>  
```  
  
## <a name="type"></a><span data-ttu-id="c4fc1-112">Type</span><span class="sxs-lookup"><span data-stu-id="c4fc1-112">Type</span></span>  
 `string`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c4fc1-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c4fc1-113">Attributes and Elements</span></span>  
 <span data-ttu-id="c4fc1-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c4fc1-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c4fc1-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="c4fc1-115">Attributes</span></span>  
  
|<span data-ttu-id="c4fc1-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="c4fc1-116">Attribute</span></span>|<span data-ttu-id="c4fc1-117">Description</span><span class="sxs-lookup"><span data-stu-id="c4fc1-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c4fc1-118">type</span><span class="sxs-lookup"><span data-stu-id="c4fc1-118">type</span></span>|<span data-ttu-id="c4fc1-119">Indique le type (espace de noms compris), le nom de l'assembly, la version, la culture et le jeton de clé publique.</span><span class="sxs-lookup"><span data-stu-id="c4fc1-119">Specifies the type (including namespace), assembly name, version, culture, and public key token.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c4fc1-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c4fc1-120">Child Elements</span></span>  
  
|<span data-ttu-id="c4fc1-121">Élément</span><span class="sxs-lookup"><span data-stu-id="c4fc1-121">Element</span></span>|<span data-ttu-id="c4fc1-122">Description</span><span class="sxs-lookup"><span data-stu-id="c4fc1-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c4fc1-123">\<paramètre ></span><span class="sxs-lookup"><span data-stu-id="c4fc1-123">\<parameter></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/parameter.md)|<span data-ttu-id="c4fc1-124">Indique un index de paramètre lorsque le type déclaré est générique.</span><span class="sxs-lookup"><span data-stu-id="c4fc1-124">Specifies a parameter index when the declared type is a generic type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c4fc1-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c4fc1-125">Parent Elements</span></span>  
  
|<span data-ttu-id="c4fc1-126">Élément</span><span class="sxs-lookup"><span data-stu-id="c4fc1-126">Element</span></span>|<span data-ttu-id="c4fc1-127">Description</span><span class="sxs-lookup"><span data-stu-id="c4fc1-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c4fc1-128">\<add></span><span class="sxs-lookup"><span data-stu-id="c4fc1-128">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)|<span data-ttu-id="c4fc1-129">Ajoute un type déclaré à la collection de types déclarés.</span><span class="sxs-lookup"><span data-stu-id="c4fc1-129">Adds a declared type to the collection of declared types.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c4fc1-130">Notes</span><span class="sxs-lookup"><span data-stu-id="c4fc1-130">Remarks</span></span>  
 <span data-ttu-id="c4fc1-131">Pour plus d’informations sur les types connus, consultez [Types connus de contrat de données](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) et <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="c4fc1-131">For more information about known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="c4fc1-132">Consultez le [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) pour obtenir un exemple d’utilisation de cet élément.</span><span class="sxs-lookup"><span data-stu-id="c4fc1-132">See the [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) for an example of using this element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c4fc1-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="c4fc1-133">Example</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="c4fc1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4fc1-134">See Also</span></span>  
 <xref:System.Runtime.Serialization.DataContractSerializer>  
 [<span data-ttu-id="c4fc1-135">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="c4fc1-135">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)  
 [<span data-ttu-id="c4fc1-136">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="c4fc1-136">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)  
 [<span data-ttu-id="c4fc1-137">\<add></span><span class="sxs-lookup"><span data-stu-id="c4fc1-137">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
