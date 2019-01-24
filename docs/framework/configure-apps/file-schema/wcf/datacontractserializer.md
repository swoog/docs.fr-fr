---
title: dataContractSerializer
ms.date: 03/30/2017
ms.assetid: a47513a4-a96c-4350-8586-daacb05dee71
ms.openlocfilehash: 933d49092c392fa293468d546e521bf7ed858376
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54539842"
---
# <a name="datacontractserializer"></a><span data-ttu-id="76e77-102">dataContractSerializer</span><span class="sxs-lookup"><span data-stu-id="76e77-102">dataContractSerializer</span></span>
<span data-ttu-id="76e77-103">Contient les données de configuration correspondant au <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="76e77-103">Contains configuration data for the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="76e77-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="76e77-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="76e77-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="76e77-105">\<behaviors></span></span>  
<span data-ttu-id="76e77-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="76e77-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="76e77-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="76e77-107">\<behavior></span></span>  
<span data-ttu-id="76e77-108">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="76e77-108">\<dataContractSerializer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="76e77-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76e77-109">Syntax</span></span>  
  
```xml  
<dataContractSerializer ignoreExtensionDataObject="Boolean"
                        maxItemsInObjectGraph="Integer" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="76e77-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="76e77-110">Attributes and Elements</span></span>  
 <span data-ttu-id="76e77-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="76e77-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="76e77-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="76e77-112">Attributes</span></span>  
  
|<span data-ttu-id="76e77-113">Élément</span><span class="sxs-lookup"><span data-stu-id="76e77-113">Element</span></span>|<span data-ttu-id="76e77-114">Description</span><span class="sxs-lookup"><span data-stu-id="76e77-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="76e77-115">ignoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="76e77-115">ignoreExtensionDataObject</span></span>|<span data-ttu-id="76e77-116">Valeur booléenne qui spécifie si les données fournies par le point de terminaison doivent être ignorées lorsqu'il est sérialisé ou désérialisé.</span><span class="sxs-lookup"><span data-stu-id="76e77-116">A Boolean value that specifies whether to ignore data supplied by the endpoint, when it is being serialized or deserialized.</span></span>|  
|<span data-ttu-id="76e77-117">maxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="76e77-117">maxItemsInObjectGraph</span></span>|<span data-ttu-id="76e77-118">Entier indiquant le nombre maximal d'éléments à sérialiser ou à désérialiser.</span><span class="sxs-lookup"><span data-stu-id="76e77-118">An integer that specifies the maximum number of items to serialize or deserialize.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="76e77-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="76e77-119">Child Elements</span></span>  
 <span data-ttu-id="76e77-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="76e77-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="76e77-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="76e77-121">Parent Elements</span></span>  
  
|<span data-ttu-id="76e77-122">Élément</span><span class="sxs-lookup"><span data-stu-id="76e77-122">Element</span></span>|<span data-ttu-id="76e77-123">Description</span><span class="sxs-lookup"><span data-stu-id="76e77-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="76e77-124">\<behavior></span><span class="sxs-lookup"><span data-stu-id="76e77-124">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="76e77-125">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="76e77-125">Specifies an endpoint behavior.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="76e77-126">Notes</span><span class="sxs-lookup"><span data-stu-id="76e77-126">Remarks</span></span>  
 <span data-ttu-id="76e77-127">Pour plus d'informations les types connus, consultez la documentation <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="76e77-127">See the <xref:System.Runtime.Serialization.DataContractSerializer> documentation for more information about known types.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="76e77-128">L'élément de comportement (si présent) `<dataContractSerializer>` doit toujours apparaître avant l'élément de comportement `<enableWebScript>` dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="76e77-128">The `<dataContractSerializer>` behavior element (if present) should always appear before the `<enableWebScript>` behavior element in the configuration file.</span></span> <span data-ttu-id="76e77-129">Sinon, le comportement résultant n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="76e77-129">Otherwise, the resulting behavior is undefined.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76e77-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76e77-130">See also</span></span>
- <xref:System.Runtime.Serialization.DataContractSerializer>
- <xref:System.ServiceModel.Description.DataContractSerializerOperationBehavior>
- <xref:System.ServiceModel.Configuration.DataContractSerializerElement>
- [<span data-ttu-id="76e77-131">Types connus de contrats de données</span><span class="sxs-lookup"><span data-stu-id="76e77-131">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [<span data-ttu-id="76e77-132">Transfert de données et sérialisation</span><span class="sxs-lookup"><span data-stu-id="76e77-132">Data Transfer and Serialization</span></span>](../../../../../docs/framework/wcf/feature-details/data-transfer-and-serialization.md)
