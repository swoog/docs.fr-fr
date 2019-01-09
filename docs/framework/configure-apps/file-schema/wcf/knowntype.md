---
title: '&lt;knownType&gt;'
ms.date: 03/30/2017
ms.assetid: ee2b7be3-7148-4a3a-b861-48e7330615e5
ms.openlocfilehash: 6156f102573333ec0d5533b8f1a8506d91215f47
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151928"
---
# <a name="ltknowntypegt"></a><span data-ttu-id="012a0-102">&lt;knownType&gt;</span><span class="sxs-lookup"><span data-stu-id="012a0-102">&lt;knownType&gt;</span></span>
<span data-ttu-id="012a0-103">Indique un type devant être utilisé par le <xref:System.Runtime.Serialization.DataContractSerializer> pendant la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="012a0-103">Specifies a type to be used by <xref:System.Runtime.Serialization.DataContractSerializer> during deserialization.</span></span> <span data-ttu-id="012a0-104">L'élément indique un « type connu » renvoyé par un champ ou une propriété d'un « type déclaré ».</span><span class="sxs-lookup"><span data-stu-id="012a0-104">The element specifies a "known type" that is returned by a field or property of a "declared type."</span></span> <span data-ttu-id="012a0-105">Pour plus d’informations, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span><span class="sxs-lookup"><span data-stu-id="012a0-105">For more information, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>  
  
 <span data-ttu-id="012a0-106">\<System.Runtime.Serialization ></span><span class="sxs-lookup"><span data-stu-id="012a0-106">\<system.runtime.serialization></span></span>  
<span data-ttu-id="012a0-107">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="012a0-107">\<dataContractSerializer></span></span>  
<span data-ttu-id="012a0-108">\<declaredTypes > élément</span><span class="sxs-lookup"><span data-stu-id="012a0-108">\<declaredTypes> Element</span></span>  
<span data-ttu-id="012a0-109">\<Ajouter > de \<declaredTypes ></span><span class="sxs-lookup"><span data-stu-id="012a0-109">\<add> of \<declaredTypes></span></span>  
<span data-ttu-id="012a0-110">\<knownType > élément</span><span class="sxs-lookup"><span data-stu-id="012a0-110">\<knownType> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="012a0-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="012a0-111">Syntax</span></span>  
  
```xml  
<knownType type="String">
  <parameter index="Integer"
             type="String" />
</knownType>
```  
  
## <a name="type"></a><span data-ttu-id="012a0-112">Type</span><span class="sxs-lookup"><span data-stu-id="012a0-112">Type</span></span>  
 `string`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="012a0-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="012a0-113">Attributes and Elements</span></span>  
 <span data-ttu-id="012a0-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="012a0-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="012a0-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="012a0-115">Attributes</span></span>  
  
|<span data-ttu-id="012a0-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="012a0-116">Attribute</span></span>|<span data-ttu-id="012a0-117">Description</span><span class="sxs-lookup"><span data-stu-id="012a0-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="012a0-118">type</span><span class="sxs-lookup"><span data-stu-id="012a0-118">type</span></span>|<span data-ttu-id="012a0-119">Indique le type (espace de noms compris), le nom de l'assembly, la version, la culture et le jeton de clé publique.</span><span class="sxs-lookup"><span data-stu-id="012a0-119">Specifies the type (including namespace), assembly name, version, culture, and public key token.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="012a0-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="012a0-120">Child Elements</span></span>  
  
|<span data-ttu-id="012a0-121">Élément</span><span class="sxs-lookup"><span data-stu-id="012a0-121">Element</span></span>|<span data-ttu-id="012a0-122">Description</span><span class="sxs-lookup"><span data-stu-id="012a0-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="012a0-123">\<Paramètre ></span><span class="sxs-lookup"><span data-stu-id="012a0-123">\<parameter></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/parameter.md)|<span data-ttu-id="012a0-124">Indique un index de paramètre lorsque le type déclaré est générique.</span><span class="sxs-lookup"><span data-stu-id="012a0-124">Specifies a parameter index when the declared type is a generic type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="012a0-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="012a0-125">Parent Elements</span></span>  
  
|<span data-ttu-id="012a0-126">Élément</span><span class="sxs-lookup"><span data-stu-id="012a0-126">Element</span></span>|<span data-ttu-id="012a0-127">Description</span><span class="sxs-lookup"><span data-stu-id="012a0-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="012a0-128">\<add></span><span class="sxs-lookup"><span data-stu-id="012a0-128">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)|<span data-ttu-id="012a0-129">Ajoute un type déclaré à la collection de types déclarés.</span><span class="sxs-lookup"><span data-stu-id="012a0-129">Adds a declared type to the collection of declared types.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="012a0-130">Notes</span><span class="sxs-lookup"><span data-stu-id="012a0-130">Remarks</span></span>  
 <span data-ttu-id="012a0-131">Pour plus d’informations sur les types connus, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) et <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="012a0-131">For more information about known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="012a0-132">Consultez le [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) pour obtenir un exemple d’utilisation de cet élément.</span><span class="sxs-lookup"><span data-stu-id="012a0-132">See the [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) for an example of using this element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="012a0-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="012a0-133">Example</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="012a0-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="012a0-134">See Also</span></span>  
 <xref:System.Runtime.Serialization.DataContractSerializer>  
 [<span data-ttu-id="012a0-135">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="012a0-135">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)  
 [<span data-ttu-id="012a0-136">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="012a0-136">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)  
 [<span data-ttu-id="012a0-137">\<add></span><span class="sxs-lookup"><span data-stu-id="012a0-137">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
