---
title: <add> de <backupList>
ms.date: 03/30/2017
ms.assetid: bc5939fc-314a-4ea4-a533-c96958da7173
ms.openlocfilehash: 03bf1bbb8156e4722d987e171d9034747ac6bb61
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59089534"
---
# <a name="add-of-backuplist"></a><span data-ttu-id="32f40-102">\<Ajouter > de \<backupList ></span><span class="sxs-lookup"><span data-stu-id="32f40-102">\<add> of \<backupList></span></span>
<span data-ttu-id="32f40-103">Représente un élément de configuration qui définit un élément de point de terminaison de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="32f40-103">Represents a configuration element that defines a backup endpoint element.</span></span>  
  
 <span data-ttu-id="32f40-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="32f40-104">\<system.serviceModel></span></span>  
<span data-ttu-id="32f40-105">\<routing></span><span class="sxs-lookup"><span data-stu-id="32f40-105">\<routing></span></span>  
<span data-ttu-id="32f40-106">\<backupLists></span><span class="sxs-lookup"><span data-stu-id="32f40-106">\<backupLists></span></span>  
<span data-ttu-id="32f40-107">\<backupList></span><span class="sxs-lookup"><span data-stu-id="32f40-107">\<backupList></span></span>  
<span data-ttu-id="32f40-108">\<add></span><span class="sxs-lookup"><span data-stu-id="32f40-108">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="32f40-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32f40-109">Syntax</span></span>  
  
```xml  
<routing>
  <backupLists>
    <backupList name="String">
      <add endpointName="String" />
    </backupList>
  </backupLists>
</routing>
```  
  
```csharp  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="32f40-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="32f40-110">Attributes and Elements</span></span>  
 <span data-ttu-id="32f40-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="32f40-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="32f40-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="32f40-112">Attributes</span></span>  
  
|<span data-ttu-id="32f40-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="32f40-113">Attribute</span></span>|<span data-ttu-id="32f40-114">Description</span><span class="sxs-lookup"><span data-stu-id="32f40-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="32f40-115">name</span><span class="sxs-lookup"><span data-stu-id="32f40-115">name</span></span>|<span data-ttu-id="32f40-116">Chaîne qui spécifie le nom du point de terminaison de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="32f40-116">A string that specifies the name of the backup endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="32f40-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="32f40-117">Child Elements</span></span>  
 <span data-ttu-id="32f40-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="32f40-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="32f40-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="32f40-119">Parent Elements</span></span>  
  
|<span data-ttu-id="32f40-120">Élément</span><span class="sxs-lookup"><span data-stu-id="32f40-120">Element</span></span>|<span data-ttu-id="32f40-121">Description</span><span class="sxs-lookup"><span data-stu-id="32f40-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="32f40-122">\<routing></span><span class="sxs-lookup"><span data-stu-id="32f40-122">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="32f40-123">Contient une liste de points de terminaison que vous souhaitez que le Service de routage à utiliser au cas où le point de terminaison principal n’est pas accessible.</span><span class="sxs-lookup"><span data-stu-id="32f40-123">Contains a list of endpoints that you would like the Routing Service to use in case the primary endpoint can't be reached.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="32f40-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32f40-124">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.BackupEndpointElement?displayProperty=nameWithType>
