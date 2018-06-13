---
title: '&lt;add&gt; de &lt;backupList&gt;'
ms.date: 03/30/2017
ms.assetid: bc5939fc-314a-4ea4-a533-c96958da7173
ms.openlocfilehash: 7e7361b24c0444b5f3d51a6f5bf079d5eb2dee18
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32745550"
---
# <a name="ltaddgt-of-ltbackuplistgt"></a><span data-ttu-id="a4de0-102">&lt;add&gt; de &lt;backupList&gt;</span><span class="sxs-lookup"><span data-stu-id="a4de0-102">&lt;add&gt; of &lt;backupList&gt;</span></span>
<span data-ttu-id="a4de0-103">Représente un élément de configuration qui définit un élément de point de terminaison de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="a4de0-103">Represents a configuration element that defines a backup endpoint element.</span></span>  
  
 <span data-ttu-id="a4de0-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="a4de0-104">\<system.serviceModel></span></span>  
<span data-ttu-id="a4de0-105">\<routage ></span><span class="sxs-lookup"><span data-stu-id="a4de0-105">\<routing></span></span>  
<span data-ttu-id="a4de0-106">\<backupLists ></span><span class="sxs-lookup"><span data-stu-id="a4de0-106">\<backupLists></span></span>  
<span data-ttu-id="a4de0-107">\<backupList ></span><span class="sxs-lookup"><span data-stu-id="a4de0-107">\<backupList></span></span>  
<span data-ttu-id="a4de0-108">\<add></span><span class="sxs-lookup"><span data-stu-id="a4de0-108">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a4de0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4de0-109">Syntax</span></span>  
  
```xml  
   <routing>  <backupLists>    <backupList name="String">      <add endpointName="String" />    </backupList>    </backupLists></routing>  
```  
  
```csharp  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a4de0-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a4de0-110">Attributes and Elements</span></span>  
 <span data-ttu-id="a4de0-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a4de0-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a4de0-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="a4de0-112">Attributes</span></span>  
  
|<span data-ttu-id="a4de0-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="a4de0-113">Attribute</span></span>|<span data-ttu-id="a4de0-114">Description</span><span class="sxs-lookup"><span data-stu-id="a4de0-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a4de0-115">name</span><span class="sxs-lookup"><span data-stu-id="a4de0-115">name</span></span>|<span data-ttu-id="a4de0-116">Chaîne qui spécifie le nom du point de terminaison de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="a4de0-116">A string that specifies the name of the backup endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a4de0-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a4de0-117">Child Elements</span></span>  
 <span data-ttu-id="a4de0-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a4de0-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a4de0-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a4de0-119">Parent Elements</span></span>  
  
|<span data-ttu-id="a4de0-120">Élément</span><span class="sxs-lookup"><span data-stu-id="a4de0-120">Element</span></span>|<span data-ttu-id="a4de0-121">Description</span><span class="sxs-lookup"><span data-stu-id="a4de0-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a4de0-122">\<routage ></span><span class="sxs-lookup"><span data-stu-id="a4de0-122">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="a4de0-123">Contient une liste de points de terminaison que vous souhaitez que le Service de routage à utiliser au cas où le point de terminaison principal ne peut pas être atteint.</span><span class="sxs-lookup"><span data-stu-id="a4de0-123">Contains a list of endpoints that you would like the Routing Service to use in case the primary endpoint can't be reached.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a4de0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4de0-124">See Also</span></span>  
 <xref:System.ServiceModel.Routing.Configuration.BackupEndpointElement?displayProperty=nameWithType> 
