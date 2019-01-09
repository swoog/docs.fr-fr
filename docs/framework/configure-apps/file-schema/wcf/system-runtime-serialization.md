---
title: '&lt;System.Runtime.Serialization&gt;'
ms.date: 03/30/2017
ms.assetid: a8cebf4c-06d2-4667-8f5b-c3e1fc90df6f
ms.openlocfilehash: 7cda0918ec14f9065ab1aea2479a14c8d224fcf8
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150550"
---
# <a name="ltsystemruntimeserializationgt"></a><span data-ttu-id="9d0be-102">&lt;System.Runtime.Serialization&gt;</span><span class="sxs-lookup"><span data-stu-id="9d0be-102">&lt;system.runtime.serialization&gt;</span></span>
<span data-ttu-id="9d0be-103">Représente l'élément racine correspondant à la section d'espace de noms <xref:System.Runtime.Serialization> et contient des éléments permettant de définir les options du <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="9d0be-103">Represents the root element for the <xref:System.Runtime.Serialization> namespace section and contains elements for setting options of the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="9d0be-104">system.runtime.serialization</span><span class="sxs-lookup"><span data-stu-id="9d0be-104">system.runtime.serialization</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9d0be-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d0be-105">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9d0be-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9d0be-106">Attributes and Elements</span></span>  
 <span data-ttu-id="9d0be-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9d0be-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9d0be-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="9d0be-108">Attributes</span></span>  
 <span data-ttu-id="9d0be-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9d0be-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="9d0be-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9d0be-110">Child Elements</span></span>  
  
|<span data-ttu-id="9d0be-111">Élément</span><span class="sxs-lookup"><span data-stu-id="9d0be-111">Element</span></span>|<span data-ttu-id="9d0be-112">Description</span><span class="sxs-lookup"><span data-stu-id="9d0be-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9d0be-113">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="9d0be-113">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-of-system-runtime-serialization.md)|<span data-ttu-id="9d0be-114">Active l’ajout de types connus à utiliser lors de la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="9d0be-114">Enables addition of known types to be used when deserialization.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9d0be-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9d0be-115">Parent Elements</span></span>  
  
|<span data-ttu-id="9d0be-116">Élément</span><span class="sxs-lookup"><span data-stu-id="9d0be-116">Element</span></span>|<span data-ttu-id="9d0be-117">Description</span><span class="sxs-lookup"><span data-stu-id="9d0be-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9d0be-118">\<configuration>, élément</span><span class="sxs-lookup"><span data-stu-id="9d0be-118">\<configuration> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|<span data-ttu-id="9d0be-119">Élément de niveau supérieur de la configuration.</span><span class="sxs-lookup"><span data-stu-id="9d0be-119">The top level element for configuration.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9d0be-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d0be-120">See Also</span></span>  
 <xref:System.Runtime.Serialization>  
 [<span data-ttu-id="9d0be-121">Utilisation de contrats de données</span><span class="sxs-lookup"><span data-stu-id="9d0be-121">Using Data Contracts</span></span>](../../../../../docs/framework/wcf/feature-details/using-data-contracts.md)  
 [<span data-ttu-id="9d0be-122">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="9d0be-122">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
