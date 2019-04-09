---
title: <system.runtime.serialization>
ms.date: 03/30/2017
ms.assetid: a8cebf4c-06d2-4667-8f5b-c3e1fc90df6f
ms.openlocfilehash: c34eba2614a354f1753d8da077f8653f2c260a97
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59165891"
---
# <a name="systemruntimeserialization"></a><span data-ttu-id="80e10-102">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="80e10-102">\<system.runtime.serialization></span></span>
<span data-ttu-id="80e10-103">Représente l'élément racine correspondant à la section d'espace de noms <xref:System.Runtime.Serialization> et contient des éléments permettant de définir les options du <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="80e10-103">Represents the root element for the <xref:System.Runtime.Serialization> namespace section and contains elements for setting options of the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="80e10-104">system.runtime.serialization</span><span class="sxs-lookup"><span data-stu-id="80e10-104">system.runtime.serialization</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="80e10-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80e10-105">Syntax</span></span>  
  
```xml  
<configuration>
  <system.runtime.serialization>
    <dataContractSerializer ignoreExtensionDataObject="Boolean"
                            maxItemsInObjectGraph="Integer">
      <declaredTypes>
        <add type="String">
          <knownType type="String">
            <parameter index="Integer" />
          </knownType>
        </add>
      </declaredTypes>
    <dataContractSerializer>
  </system.runtime.serialization>
</configuration>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="80e10-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="80e10-106">Attributes and Elements</span></span>  
 <span data-ttu-id="80e10-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="80e10-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="80e10-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="80e10-108">Attributes</span></span>  
 <span data-ttu-id="80e10-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="80e10-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="80e10-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="80e10-110">Child Elements</span></span>  
  
|<span data-ttu-id="80e10-111">Élément</span><span class="sxs-lookup"><span data-stu-id="80e10-111">Element</span></span>|<span data-ttu-id="80e10-112">Description</span><span class="sxs-lookup"><span data-stu-id="80e10-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="80e10-113">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="80e10-113">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-of-system-runtime-serialization.md)|<span data-ttu-id="80e10-114">Active l'ajout de types connus à utiliser lors de la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="80e10-114">Enables addition of known types to be used when deserialization.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="80e10-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="80e10-115">Parent Elements</span></span>  
  
|<span data-ttu-id="80e10-116">Élément</span><span class="sxs-lookup"><span data-stu-id="80e10-116">Element</span></span>|<span data-ttu-id="80e10-117">Description</span><span class="sxs-lookup"><span data-stu-id="80e10-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="80e10-118">\<configuration > élément</span><span class="sxs-lookup"><span data-stu-id="80e10-118">\<configuration> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|<span data-ttu-id="80e10-119">Élément de niveau supérieur de la configuration.</span><span class="sxs-lookup"><span data-stu-id="80e10-119">The top level element for configuration.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="80e10-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80e10-120">See also</span></span>

- <xref:System.Runtime.Serialization>
- [<span data-ttu-id="80e10-121">Utilisation de contrats de données</span><span class="sxs-lookup"><span data-stu-id="80e10-121">Using Data Contracts</span></span>](../../../../../docs/framework/wcf/feature-details/using-data-contracts.md)
- [<span data-ttu-id="80e10-122">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="80e10-122">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
