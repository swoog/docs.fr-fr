---
title: dataContractSerializer
ms.date: 03/30/2017
ms.assetid: a47513a4-a96c-4350-8586-daacb05dee71
ms.openlocfilehash: 8ba16d9cc30b07d3e6b0924e6013ec01443867d4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59139046"
---
# <a name="datacontractserializer"></a><span data-ttu-id="a715e-102">dataContractSerializer</span><span class="sxs-lookup"><span data-stu-id="a715e-102">dataContractSerializer</span></span>
<span data-ttu-id="a715e-103">Contient les données de configuration correspondant au <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="a715e-103">Contains configuration data for the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="a715e-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="a715e-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="a715e-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="a715e-105">\<behaviors></span></span>  
<span data-ttu-id="a715e-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="a715e-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="a715e-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="a715e-107">\<behavior></span></span>  
<span data-ttu-id="a715e-108">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="a715e-108">\<dataContractSerializer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a715e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a715e-109">Syntax</span></span>  
  
```xml  
<dataContractSerializer ignoreExtensionDataObject="Boolean"
                        maxItemsInObjectGraph="Integer" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a715e-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a715e-110">Attributes and Elements</span></span>  
 <span data-ttu-id="a715e-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a715e-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a715e-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="a715e-112">Attributes</span></span>  
  
|<span data-ttu-id="a715e-113">Élément</span><span class="sxs-lookup"><span data-stu-id="a715e-113">Element</span></span>|<span data-ttu-id="a715e-114">Description</span><span class="sxs-lookup"><span data-stu-id="a715e-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a715e-115">ignoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="a715e-115">ignoreExtensionDataObject</span></span>|<span data-ttu-id="a715e-116">Valeur booléenne qui spécifie si les données fournies par le point de terminaison doivent être ignorées lorsqu'il est sérialisé ou désérialisé.</span><span class="sxs-lookup"><span data-stu-id="a715e-116">A Boolean value that specifies whether to ignore data supplied by the endpoint, when it is being serialized or deserialized.</span></span>|  
|<span data-ttu-id="a715e-117">maxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="a715e-117">maxItemsInObjectGraph</span></span>|<span data-ttu-id="a715e-118">Entier indiquant le nombre maximal d'éléments à sérialiser ou à désérialiser.</span><span class="sxs-lookup"><span data-stu-id="a715e-118">An integer that specifies the maximum number of items to serialize or deserialize.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a715e-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a715e-119">Child Elements</span></span>  
 <span data-ttu-id="a715e-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a715e-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a715e-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a715e-121">Parent Elements</span></span>  
  
|<span data-ttu-id="a715e-122">Élément</span><span class="sxs-lookup"><span data-stu-id="a715e-122">Element</span></span>|<span data-ttu-id="a715e-123">Description</span><span class="sxs-lookup"><span data-stu-id="a715e-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a715e-124">\<behavior></span><span class="sxs-lookup"><span data-stu-id="a715e-124">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="a715e-125">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a715e-125">Specifies an endpoint behavior.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a715e-126">Notes</span><span class="sxs-lookup"><span data-stu-id="a715e-126">Remarks</span></span>  
 <span data-ttu-id="a715e-127">Pour plus d'informations les types connus, consultez la documentation <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="a715e-127">See the <xref:System.Runtime.Serialization.DataContractSerializer> documentation for more information about known types.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="a715e-128">L'élément de comportement (si présent) `<dataContractSerializer>` doit toujours apparaître avant l'élément de comportement `<enableWebScript>` dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="a715e-128">The `<dataContractSerializer>` behavior element (if present) should always appear before the `<enableWebScript>` behavior element in the configuration file.</span></span> <span data-ttu-id="a715e-129">Sinon, le comportement résultant n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="a715e-129">Otherwise, the resulting behavior is undefined.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a715e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a715e-130">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractSerializer>
- <xref:System.ServiceModel.Description.DataContractSerializerOperationBehavior>
- <xref:System.ServiceModel.Configuration.DataContractSerializerElement>
- [<span data-ttu-id="a715e-131">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="a715e-131">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [<span data-ttu-id="a715e-132">Transfert de données et sérialisation</span><span class="sxs-lookup"><span data-stu-id="a715e-132">Data Transfer and Serialization</span></span>](../../../../../docs/framework/wcf/feature-details/data-transfer-and-serialization.md)
