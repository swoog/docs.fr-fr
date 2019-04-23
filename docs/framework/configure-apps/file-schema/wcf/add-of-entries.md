---
title: <add> de <entries>
ms.date: 03/30/2017
ms.assetid: 3af4805b-dc72-4f68-b168-da4fba8c6170
ms.openlocfilehash: 1324803d7c0f127cfee9eadebff2672955780eda
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59165410"
---
# <a name="add-of-entries"></a><span data-ttu-id="96d8d-102">\<Ajouter > de \<entrées ></span><span class="sxs-lookup"><span data-stu-id="96d8d-102">\<add> of \<entries></span></span>
<span data-ttu-id="96d8d-103">Représente une entrée de routage qui mappe un filtre à un point de terminaison client défini précédemment.</span><span class="sxs-lookup"><span data-stu-id="96d8d-103">Represents a routing entry that maps a filter to a client endpoint that was previously defined.</span></span> <span data-ttu-id="96d8d-104">Les messages correspondant à ce filtre sont envoyés à cette destination.</span><span class="sxs-lookup"><span data-stu-id="96d8d-104">Messages matching this filter will be sent to this destination.</span></span>  
  
 <span data-ttu-id="96d8d-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="96d8d-105">\<system.serviceModel></span></span>  
<span data-ttu-id="96d8d-106">\<routing></span><span class="sxs-lookup"><span data-stu-id="96d8d-106">\<routing></span></span>  
<span data-ttu-id="96d8d-107">\<filterTables></span><span class="sxs-lookup"><span data-stu-id="96d8d-107">\<filterTables></span></span>  
<span data-ttu-id="96d8d-108">\<filterTable></span><span class="sxs-lookup"><span data-stu-id="96d8d-108">\<filterTable></span></span>  
<span data-ttu-id="96d8d-109">\<entries></span><span class="sxs-lookup"><span data-stu-id="96d8d-109">\<entries></span></span>  
<span data-ttu-id="96d8d-110">\<add></span><span class="sxs-lookup"><span data-stu-id="96d8d-110">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="96d8d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96d8d-111">Syntax</span></span>  
  
```xml  
<routing>
  <filterTables>
    <filterTable name="String">
      <entries>
        <add backupList="String"
             endpointName="String"
             filterName="String"
             priority="Integer" />
      </entries>
    </filterTable>
  </filterTables>
</routing>
```  
  
```csharp  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="96d8d-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="96d8d-112">Attributes and Elements</span></span>  
 <span data-ttu-id="96d8d-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="96d8d-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="96d8d-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="96d8d-114">Attributes</span></span>  
  
|<span data-ttu-id="96d8d-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="96d8d-115">Attribute</span></span>|<span data-ttu-id="96d8d-116">Description</span><span class="sxs-lookup"><span data-stu-id="96d8d-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="96d8d-117">backupList</span><span class="sxs-lookup"><span data-stu-id="96d8d-117">backupList</span></span>|<span data-ttu-id="96d8d-118">Chaîne qui spécifie une référence à une liste de sauvegarde de points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="96d8d-118">A string that specifies a reference to a backup list of endpoints.</span></span>|  
|<span data-ttu-id="96d8d-119">Point de terminaison (endpoint)</span><span class="sxs-lookup"><span data-stu-id="96d8d-119">endpoint</span></span>|<span data-ttu-id="96d8d-120">Chaîne qui spécifie une référence à un point de terminaison client qui reçoit les messages correspondant au filtre indiqué par l'attribut `filterName`.</span><span class="sxs-lookup"><span data-stu-id="96d8d-120">A string that specifies a reference to a client endpoint that will receive messages that match the filter specified by the `filterName` attribute.</span></span>|  
|<span data-ttu-id="96d8d-121">filterName</span><span class="sxs-lookup"><span data-stu-id="96d8d-121">filterName</span></span>|<span data-ttu-id="96d8d-122">Chaîne qui spécifie une référence à un élément de filtre.</span><span class="sxs-lookup"><span data-stu-id="96d8d-122">A string that specifies a reference to a filter element.</span></span>|  
|<span data-ttu-id="96d8d-123">priority</span><span class="sxs-lookup"><span data-stu-id="96d8d-123">priority</span></span>|<span data-ttu-id="96d8d-124">Entier qui spécifie la priorité de cette entrée.</span><span class="sxs-lookup"><span data-stu-id="96d8d-124">An integer that specifies the priority of this entry.</span></span><br /><br /> <span data-ttu-id="96d8d-125">Les entrées dans la table de routage sont évaluées selon leur priorité, 0 correspondant à la priorité la plus basse.</span><span class="sxs-lookup"><span data-stu-id="96d8d-125">Entries in the routing table will be evaluated based on priority, with 0 being the lowest priority.</span></span> <span data-ttu-id="96d8d-126">Toutes les entrées d'une priorité donnée sont évaluées simultanément, si aucune entrée correspondante n'est trouvée pour la priorité actuelle, le niveau de priorité suivant est évalué.</span><span class="sxs-lookup"><span data-stu-id="96d8d-126">All entries for a specific priority are evaluated simultaneously, if no matching entry is found for the current priority, the next priority level will be evaluated.</span></span><br /><br /> <span data-ttu-id="96d8d-127">Cette valeur est facultative.</span><span class="sxs-lookup"><span data-stu-id="96d8d-127">This value is optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="96d8d-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="96d8d-128">Child Elements</span></span>  
 <span data-ttu-id="96d8d-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="96d8d-129">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="96d8d-130">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="96d8d-130">Parent Elements</span></span>  
  
|<span data-ttu-id="96d8d-131">Élément</span><span class="sxs-lookup"><span data-stu-id="96d8d-131">Element</span></span>|<span data-ttu-id="96d8d-132">Description</span><span class="sxs-lookup"><span data-stu-id="96d8d-132">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="96d8d-133">\<routing></span><span class="sxs-lookup"><span data-stu-id="96d8d-133">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="96d8d-134">Section de configuration qui contient les entrées de mappage de routage.</span><span class="sxs-lookup"><span data-stu-id="96d8d-134">A configuration section that contains routing mapping entries.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="96d8d-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96d8d-135">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType>
