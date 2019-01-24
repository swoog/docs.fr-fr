---
title: '&lt;dataContractSerializer&gt; de &lt;system.runtime.serialization&gt;'
ms.date: 03/30/2017
ms.assetid: d9b3d625-be3f-4768-8e0d-1b7e6929f6a8
ms.openlocfilehash: 3a959c9a4e2b1cbbbb6a52a1438261037704d244
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54557966"
---
# <a name="ltdatacontractserializergt-of-ltsystemruntimeserializationgt"></a><span data-ttu-id="b50ca-102">&lt;dataContractSerializer&gt; de &lt;system.runtime.serialization&gt;</span><span class="sxs-lookup"><span data-stu-id="b50ca-102">&lt;dataContractSerializer&gt; of &lt;system.runtime.serialization&gt;</span></span>
<span data-ttu-id="b50ca-103">Contient les données de configuration correspondant au <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="b50ca-103">Contains configuration data for the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="b50ca-104">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="b50ca-104">\<system.runtime.serialization></span></span>  
<span data-ttu-id="b50ca-105">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="b50ca-105">\<dataContractSerializer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b50ca-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b50ca-106">Syntax</span></span>  
  
```xml  
<configuration>
  <system.runtime.serialization>
    <dataContractSerializer ignoreExtensionDataObject="Boolean"
                            maxItemsInObjectGraph="Integer">
      <declaredTypes>
        <add type="String">
          <knownType type="String">
            <parameter index="Integer"
                       type="String" />
          </knownType>
        </add>
      </declaredTypes>
    <dataContractSerializer>
  </system.runtime.serialization>
</configuration>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b50ca-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b50ca-107">Attributes and Elements</span></span>  
 <span data-ttu-id="b50ca-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b50ca-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b50ca-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="b50ca-109">Attributes</span></span>  
  
|<span data-ttu-id="b50ca-110">Élément</span><span class="sxs-lookup"><span data-stu-id="b50ca-110">Element</span></span>|<span data-ttu-id="b50ca-111">Description</span><span class="sxs-lookup"><span data-stu-id="b50ca-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b50ca-112">ignoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="b50ca-112">ignoreExtensionDataObject</span></span>|<span data-ttu-id="b50ca-113">Valeur booléenne indiquant si les données fournies par le point de terminaison doivent être ignorées ou non lors d'une sérialisation ou d'une désérialisation.</span><span class="sxs-lookup"><span data-stu-id="b50ca-113">A Boolean value that specifies whether to ignore data supplied by the endpoint when it is being serialized or deserialized.</span></span> <span data-ttu-id="b50ca-114">Cet attribut peut uniquement être défini sur le `<dataContractSerializer>` situé sous l'élément `<behavior>`.</span><span class="sxs-lookup"><span data-stu-id="b50ca-114">This attribute is settable only on the `<dataContractSerializer>` under the `<behavior>` element.</span></span>|  
|<span data-ttu-id="b50ca-115">maxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="b50ca-115">maxItemsInObjectGraph</span></span>|<span data-ttu-id="b50ca-116">Entier indiquant le nombre maximal d'éléments à sérialiser ou à désérialiser.</span><span class="sxs-lookup"><span data-stu-id="b50ca-116">An integer that specifies the maximum number of items to serialize or deserialize.</span></span> <span data-ttu-id="b50ca-117">Cet attribut a la valeur 65 536.</span><span class="sxs-lookup"><span data-stu-id="b50ca-117">This attribute is 65536.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b50ca-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b50ca-118">Child Elements</span></span>  
  
|<span data-ttu-id="b50ca-119">Élément</span><span class="sxs-lookup"><span data-stu-id="b50ca-119">Element</span></span>|<span data-ttu-id="b50ca-120">Description</span><span class="sxs-lookup"><span data-stu-id="b50ca-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b50ca-121">\<declaredTypes></span><span class="sxs-lookup"><span data-stu-id="b50ca-121">\<declaredTypes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/declaredtypes.md)|<span data-ttu-id="b50ca-122">Contient les types connus utilisés par le <xref:System.Runtime.Serialization.DataContractSerializer> lors de la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="b50ca-122">Contains the known types that the <xref:System.Runtime.Serialization.DataContractSerializer> uses when deserializing.</span></span><br /><br /> <span data-ttu-id="b50ca-123">Pour plus d’informations sur les contrats de données et les types connus, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span><span class="sxs-lookup"><span data-stu-id="b50ca-123">For more information about data contracts and known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b50ca-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b50ca-124">Parent Elements</span></span>  
  
|<span data-ttu-id="b50ca-125">Élément</span><span class="sxs-lookup"><span data-stu-id="b50ca-125">Element</span></span>|<span data-ttu-id="b50ca-126">Description</span><span class="sxs-lookup"><span data-stu-id="b50ca-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b50ca-127">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="b50ca-127">\<system.runtime.serialization></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-runtime-serialization.md)|<span data-ttu-id="b50ca-128">Représente l'élément racine correspondant à la section d'espace de noms <xref:System.Runtime.Serialization> et contient des éléments permettant de définir les options du <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="b50ca-128">Represents the root element for the <xref:System.Runtime.Serialization> namespace section and contains elements for setting options of the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b50ca-129">Notes</span><span class="sxs-lookup"><span data-stu-id="b50ca-129">Remarks</span></span>  
 <span data-ttu-id="b50ca-130">Pour plus d’informations sur les types connus, consultez <xref:System.Runtime.Serialization.DataContractSerializer> et [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span><span class="sxs-lookup"><span data-stu-id="b50ca-130">For more information about known types, see <xref:System.Runtime.Serialization.DataContractSerializer> and [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b50ca-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b50ca-131">See also</span></span>
- <xref:System.Runtime.Serialization.DataContractSerializer>
- <xref:System.ServiceModel.Description.DataContractSerializerOperationBehavior>
- [<span data-ttu-id="b50ca-132">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="b50ca-132">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
