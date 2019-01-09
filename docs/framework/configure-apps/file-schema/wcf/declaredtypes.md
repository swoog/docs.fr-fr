---
title: '&lt;declaredTypes&gt;'
ms.date: 03/30/2017
helpviewer_keywords:
- dataContractSerializer element
- declaredTypes element
- DataContractSerializer
- KnownTypes
- <declaredTypes> element
ms.assetid: f35184e4-9d9e-4d37-8fb4-d5b58220eb3e
ms.openlocfilehash: 0fadb13d4fcfbe87eb2c08fc35323c726c0ac2a6
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146418"
---
# <a name="ltdeclaredtypesgt"></a><span data-ttu-id="4d920-102">&lt;declaredTypes&gt;</span><span class="sxs-lookup"><span data-stu-id="4d920-102">&lt;declaredTypes&gt;</span></span>
<span data-ttu-id="4d920-103">Contient les types connus utilisés par le <xref:System.Runtime.Serialization.DataContractSerializer> lors de la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="4d920-103">Contains the known types that the <xref:System.Runtime.Serialization.DataContractSerializer> uses when deserializing.</span></span>  
  
 <span data-ttu-id="4d920-104">Pour plus d’informations sur les contrats de données et les types connus, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span><span class="sxs-lookup"><span data-stu-id="4d920-104">For more information about data contracts and known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>  
  
 <span data-ttu-id="4d920-105">system.runtime.serialization</span><span class="sxs-lookup"><span data-stu-id="4d920-105">system.runtime.serialization</span></span>  
<span data-ttu-id="4d920-106">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="4d920-106">\<dataContractSerializer></span></span>  
<span data-ttu-id="4d920-107">\<declaredTypes ></span><span class="sxs-lookup"><span data-stu-id="4d920-107">\<declaredTypes></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4d920-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d920-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4d920-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4d920-109">Attributes and Elements</span></span>  
 <span data-ttu-id="4d920-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4d920-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4d920-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="4d920-111">Attributes</span></span>  
 <span data-ttu-id="4d920-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4d920-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4d920-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4d920-113">Child Elements</span></span>  
  
|<span data-ttu-id="4d920-114">Élément</span><span class="sxs-lookup"><span data-stu-id="4d920-114">Element</span></span>|<span data-ttu-id="4d920-115">Description</span><span class="sxs-lookup"><span data-stu-id="4d920-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4d920-116">\<add></span><span class="sxs-lookup"><span data-stu-id="4d920-116">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)|<span data-ttu-id="4d920-117">Ajoute des types qui requièrent des types connus.</span><span class="sxs-lookup"><span data-stu-id="4d920-117">Adds types that require known types.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4d920-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4d920-118">Parent Elements</span></span>  
  
|<span data-ttu-id="4d920-119">Élément</span><span class="sxs-lookup"><span data-stu-id="4d920-119">Element</span></span>|<span data-ttu-id="4d920-120">Description</span><span class="sxs-lookup"><span data-stu-id="4d920-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4d920-121">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="4d920-121">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-of-system-runtime-serialization.md)|<span data-ttu-id="4d920-122">Contient les données de configuration correspondant au <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="4d920-122">Contains configuration data for the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4d920-123">Notes</span><span class="sxs-lookup"><span data-stu-id="4d920-123">Remarks</span></span>  
 <span data-ttu-id="4d920-124">Pour plus d’informations sur les types connus, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) et <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="4d920-124">For more information about known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4d920-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="4d920-125">Example</span></span>  
 <span data-ttu-id="4d920-126">Le code XML suivant montre les types déclarés et les types connus ajoutés à un `DataContractSerializer` élément.</span><span class="sxs-lookup"><span data-stu-id="4d920-126">The following XML code shows declared types and known types added to a `DataContractSerializer` element.</span></span> <span data-ttu-id="4d920-127">L'exemple montre l'ajout de trois types.</span><span class="sxs-lookup"><span data-stu-id="4d920-127">The example shows three types being added.</span></span> <span data-ttu-id="4d920-128">Le premier est un type personnalisé nommé « Orders » qui utilise un type connu nommé « Item ».</span><span class="sxs-lookup"><span data-stu-id="4d920-128">The first is a custom type named "Orders" that uses a known type named "Item".</span></span> <span data-ttu-id="4d920-129">Le deuxième est un <xref:System.Collections.Generic.List%601> qui utilise `Item` comme un type connu.</span><span class="sxs-lookup"><span data-stu-id="4d920-129">The second declared type is a <xref:System.Collections.Generic.List%601> that uses `Item` as a known type.</span></span> <span data-ttu-id="4d920-130">Le troisième et dernier est un <xref:System.Collections.Generic.Dictionary%602>.</span><span class="sxs-lookup"><span data-stu-id="4d920-130">Finally the third declared type is a <xref:System.Collections.Generic.Dictionary%602>.</span></span> <span data-ttu-id="4d920-131">Le type de classe <xref:System.Collections.Generic.Dictionary%602> est un type générique contenant deux paramètres de type.</span><span class="sxs-lookup"><span data-stu-id="4d920-131">The <xref:System.Collections.Generic.Dictionary%602> class type is a generic type, with two type parameters.</span></span> <span data-ttu-id="4d920-132">Le premier représente la clé et le second représente la valeur.</span><span class="sxs-lookup"><span data-stu-id="4d920-132">The first represents the key and the second represents the value.</span></span> <span data-ttu-id="4d920-133">L'exemple suivant ajoute un <xref:System.Collections.Generic.List%601> du deuxième type (la valeur) à la liste de types connus.</span><span class="sxs-lookup"><span data-stu-id="4d920-133">The following example adds a <xref:System.Collections.Generic.List%601> of the second type (the value) to the list of known types.</span></span> <span data-ttu-id="4d920-134">Vous devez utiliser l'attribut `index` pour spécifier le paramètre de type à utiliser dans le type connu.</span><span class="sxs-lookup"><span data-stu-id="4d920-134">You must use the `index` attribute to specify which type parameter to use in the known type.</span></span> <span data-ttu-id="4d920-135">Dans ce cas, le type de valeur est indiqué par l’ensemble d’attributs d’index ayant la valeur "1" (la collection est de base zéro).</span><span class="sxs-lookup"><span data-stu-id="4d920-135">In this case, the value type is indicated by the index attribute set to "1" (the collection is zero-based).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="4d920-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d920-136">See Also</span></span>  
 <xref:System.Runtime.Serialization.DataContractSerializer>  
 [<span data-ttu-id="4d920-137">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="4d920-137">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)  
 [<span data-ttu-id="4d920-138">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="4d920-138">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)  
 [<span data-ttu-id="4d920-139">\<add></span><span class="sxs-lookup"><span data-stu-id="4d920-139">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
