---
title: <declaredTypes>
ms.date: 03/30/2017
helpviewer_keywords:
- dataContractSerializer element
- declaredTypes element
- DataContractSerializer
- KnownTypes
- <declaredTypes> element
ms.assetid: f35184e4-9d9e-4d37-8fb4-d5b58220eb3e
ms.openlocfilehash: 8919ee717012f8badcf7015bf8d850ed431c5943
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59090275"
---
# <a name="declaredtypes"></a><span data-ttu-id="5474a-101">\<declaredTypes></span><span class="sxs-lookup"><span data-stu-id="5474a-101">\<declaredTypes></span></span>
<span data-ttu-id="5474a-102">Contient les types connus utilisés par le <xref:System.Runtime.Serialization.DataContractSerializer> lors de la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="5474a-102">Contains the known types that the <xref:System.Runtime.Serialization.DataContractSerializer> uses when deserializing.</span></span>  
  
 <span data-ttu-id="5474a-103">Pour plus d’informations sur les contrats de données et les types connus, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span><span class="sxs-lookup"><span data-stu-id="5474a-103">For more information about data contracts and known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>  
  
 <span data-ttu-id="5474a-104">system.runtime.serialization</span><span class="sxs-lookup"><span data-stu-id="5474a-104">system.runtime.serialization</span></span>  
<span data-ttu-id="5474a-105">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="5474a-105">\<dataContractSerializer></span></span>  
<span data-ttu-id="5474a-106">\<declaredTypes></span><span class="sxs-lookup"><span data-stu-id="5474a-106">\<declaredTypes></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5474a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5474a-107">Syntax</span></span>  
  
```xml  
<configuration>
  <system.runtime.serialization>
    <dataContractSerializer>
      <declaredTypes>
        <add type="String ">
          <knownType type="String">
            <parameter index="Integer"/>
          </knownType>
        </add>
      </declaredTypes>
    <dataContractSerializer>
  </system.runtime.serialization>
</configuration>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5474a-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5474a-108">Attributes and Elements</span></span>  
 <span data-ttu-id="5474a-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5474a-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5474a-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="5474a-110">Attributes</span></span>  
 <span data-ttu-id="5474a-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5474a-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="5474a-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5474a-112">Child Elements</span></span>  
  
|<span data-ttu-id="5474a-113">Élément</span><span class="sxs-lookup"><span data-stu-id="5474a-113">Element</span></span>|<span data-ttu-id="5474a-114">Description</span><span class="sxs-lookup"><span data-stu-id="5474a-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5474a-115">\<add></span><span class="sxs-lookup"><span data-stu-id="5474a-115">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)|<span data-ttu-id="5474a-116">Ajoute des types qui requièrent des types connus.</span><span class="sxs-lookup"><span data-stu-id="5474a-116">Adds types that require known types.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5474a-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5474a-117">Parent Elements</span></span>  
  
|<span data-ttu-id="5474a-118">Élément</span><span class="sxs-lookup"><span data-stu-id="5474a-118">Element</span></span>|<span data-ttu-id="5474a-119">Description</span><span class="sxs-lookup"><span data-stu-id="5474a-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5474a-120">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="5474a-120">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-of-system-runtime-serialization.md)|<span data-ttu-id="5474a-121">Contient les données de configuration correspondant au <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="5474a-121">Contains configuration data for the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5474a-122">Notes</span><span class="sxs-lookup"><span data-stu-id="5474a-122">Remarks</span></span>  
 <span data-ttu-id="5474a-123">Pour plus d’informations sur les types connus, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) et <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="5474a-123">For more information about known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5474a-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="5474a-124">Example</span></span>  
 <span data-ttu-id="5474a-125">Le code XML suivant montre les types déclarés et les types connus ajoutés à un `DataContractSerializer` élément.</span><span class="sxs-lookup"><span data-stu-id="5474a-125">The following XML code shows declared types and known types added to a `DataContractSerializer` element.</span></span> <span data-ttu-id="5474a-126">L'exemple montre l'ajout de trois types.</span><span class="sxs-lookup"><span data-stu-id="5474a-126">The example shows three types being added.</span></span> <span data-ttu-id="5474a-127">Le premier est un type personnalisé nommé « Orders » qui utilise un type connu nommé « Item ».</span><span class="sxs-lookup"><span data-stu-id="5474a-127">The first is a custom type named "Orders" that uses a known type named "Item".</span></span> <span data-ttu-id="5474a-128">Le deuxième est un <xref:System.Collections.Generic.List%601> qui utilise `Item` comme un type connu.</span><span class="sxs-lookup"><span data-stu-id="5474a-128">The second declared type is a <xref:System.Collections.Generic.List%601> that uses `Item` as a known type.</span></span> <span data-ttu-id="5474a-129">Le troisième et dernier est un <xref:System.Collections.Generic.Dictionary%602>.</span><span class="sxs-lookup"><span data-stu-id="5474a-129">Finally the third declared type is a <xref:System.Collections.Generic.Dictionary%602>.</span></span> <span data-ttu-id="5474a-130">Le type de classe <xref:System.Collections.Generic.Dictionary%602> est un type générique contenant deux paramètres de type.</span><span class="sxs-lookup"><span data-stu-id="5474a-130">The <xref:System.Collections.Generic.Dictionary%602> class type is a generic type, with two type parameters.</span></span> <span data-ttu-id="5474a-131">Le premier représente la clé et le second représente la valeur.</span><span class="sxs-lookup"><span data-stu-id="5474a-131">The first represents the key and the second represents the value.</span></span> <span data-ttu-id="5474a-132">L'exemple suivant ajoute un <xref:System.Collections.Generic.List%601> du deuxième type (la valeur) à la liste de types connus.</span><span class="sxs-lookup"><span data-stu-id="5474a-132">The following example adds a <xref:System.Collections.Generic.List%601> of the second type (the value) to the list of known types.</span></span> <span data-ttu-id="5474a-133">Vous devez utiliser l'attribut `index` pour spécifier le paramètre de type à utiliser dans le type connu.</span><span class="sxs-lookup"><span data-stu-id="5474a-133">You must use the `index` attribute to specify which type parameter to use in the known type.</span></span> <span data-ttu-id="5474a-134">Dans ce cas, le type de valeur est indiqué par l'ensemble d'attributs d'index ayant la valeur "1" (la collection est de base zéro).</span><span class="sxs-lookup"><span data-stu-id="5474a-134">In this case, the value type is indicated by the index attribute set to "1" (the collection is zero-based).</span></span>  
  
```xml  
<configuration>
  <system.runtime.serialization>
    <dataContractSerializer>
      <declaredTypes>
        <add type="Examples.Types.Orders, SerializationTypes, Version = 2.0.0.0, Culture = neutral, PublicKeyToken=null">
          <knownType type="Examples.Types.Item, SerializationTypes, Version=2.0.0.0, Culture=neutral, PublicKey=null" />
        </add>
        <add type="System.Collections.Generic.List`1, SerializationTypes, Version = 2.0.0.0, Culture = neutral, PublicKeyToken=null">
          <knownType type="Examples.Types.Item, SerializationTypes, Version=2.0.0.0, Culture=neutral, PublicKey=null" />
        </add>
        <add type="System.Collections.Generic.Dictionary`2, SerializationTypes, Version = 2.0.0.0, Culture = neutral, PublicKeyToken=null">
          <knownType type="System.Collections.Generic.List`1, SerializationTypes, Version = 2.0.0.0, Culture = neutral, PublicKeyToken=null">
            <parameter index="1"/>
          </knownType>
        </add>
      </declaredTypes>
    <dataContractSerializer>
  </system.runtime.serialization>
</configuration>
```  
  
## <a name="see-also"></a><span data-ttu-id="5474a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5474a-135">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractSerializer>
- [<span data-ttu-id="5474a-136">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="5474a-136">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)
- [<span data-ttu-id="5474a-137">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="5474a-137">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [<span data-ttu-id="5474a-138">\<add></span><span class="sxs-lookup"><span data-stu-id="5474a-138">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
