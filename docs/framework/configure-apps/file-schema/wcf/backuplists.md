---
title: '&lt;backupLists&gt;'
ms.date: 03/30/2017
ms.assetid: 593b3390-f65b-4684-ad40-0596b62f0954
ms.openlocfilehash: 5fb89ce5a942db40b07a65f59ddd05ab4cd624aa
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32749593"
---
# <a name="ltbackuplistsgt"></a><span data-ttu-id="aded2-102">&lt;backupLists&gt;</span><span class="sxs-lookup"><span data-stu-id="aded2-102">&lt;backupLists&gt;</span></span>
<span data-ttu-id="aded2-103">Représente une section de configuration pour la définition d'un ensemble de services de sauvegarde utilisés dans la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="aded2-103">Represents a configuration section for defining a set of backup services used in error handling.</span></span> <span data-ttu-id="aded2-104">Chaque élément enfant est une liste de sauvegarde qui énumère un ensemble de points de terminaison que vous souhaitez que le Service de routage à utiliser au cas où le point de terminaison principal ne peut pas être atteint.</span><span class="sxs-lookup"><span data-stu-id="aded2-104">Each child element is a backup list that enumerates a set of endpoints that you would like the Routing Service to use in case the primary endpoint can't be reached.</span></span> <span data-ttu-id="aded2-105">Si le premier point de terminaison de la liste est inactif, le service de routage bascule automatiquement sur le suivant dans la liste.</span><span class="sxs-lookup"><span data-stu-id="aded2-105">If the first endpoint in the list is down, the Routing Service will automatically fail-over to the next one in the list.</span></span>  <span data-ttu-id="aded2-106">Vous disposez ainsi d’une méthode rapide pour renforcer la fiabilité de votre application sans avoir à apprendre à votre application cliente à gérer des modèles complexes ou à rechercher l’emplacement de tous vos services déployés.</span><span class="sxs-lookup"><span data-stu-id="aded2-106">This gives you a quick way to add reliability to your application without having to teach your client application how to handle complex patterns or where all of your services are deployed.</span></span>  
  
 <span data-ttu-id="aded2-107">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="aded2-107">\<system.serviceModel></span></span>  
<span data-ttu-id="aded2-108">\<routage ></span><span class="sxs-lookup"><span data-stu-id="aded2-108">\<routing></span></span>  
<span data-ttu-id="aded2-109">\<backupLists ></span><span class="sxs-lookup"><span data-stu-id="aded2-109">\<backupLists></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aded2-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aded2-110">Syntax</span></span>  
  
```xml
   <routing>  <backupLists>    <backupList name="String">      <add endpointName="String" />    </backupList>    </backupLists></routing>  
```

## <a name="attributes-and-elements"></a><span data-ttu-id="aded2-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="aded2-111">Attributes and Elements</span></span>  
 <span data-ttu-id="aded2-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="aded2-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="aded2-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="aded2-113">Attributes</span></span>  
 <span data-ttu-id="aded2-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="aded2-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="aded2-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="aded2-115">Child Elements</span></span>  
  
|<span data-ttu-id="aded2-116">Élément</span><span class="sxs-lookup"><span data-stu-id="aded2-116">Element</span></span>|<span data-ttu-id="aded2-117">Description</span><span class="sxs-lookup"><span data-stu-id="aded2-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="aded2-118">\<filter></span><span class="sxs-lookup"><span data-stu-id="aded2-118">\<filter></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filter.md)|<span data-ttu-id="aded2-119">Contient une liste de points de terminaison que vous souhaitez que le Service de routage à utiliser au cas où le point de terminaison principal ne peut pas être atteint.</span><span class="sxs-lookup"><span data-stu-id="aded2-119">Contains a list of endpoints that you would like the Routing Service to use in case the primary endpoint can't be reached.</span></span> <span data-ttu-id="aded2-120">.</span><span class="sxs-lookup"><span data-stu-id="aded2-120">.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="aded2-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="aded2-121">Parent Elements</span></span>  
  
|<span data-ttu-id="aded2-122">Élément</span><span class="sxs-lookup"><span data-stu-id="aded2-122">Element</span></span>|<span data-ttu-id="aded2-123">Description</span><span class="sxs-lookup"><span data-stu-id="aded2-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="aded2-124">\<routage ></span><span class="sxs-lookup"><span data-stu-id="aded2-124">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="aded2-125">Représente une section de configuration pour définir un ensemble de filtres de routage, qui détermine le type de Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> à utiliser lors de l’évaluation des messages entrants, ainsi que le routage des tables qui définissent les points de terminaison cible à envoyer des messages lorsqu’un filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="aded2-125">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="aded2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aded2-126">See Also</span></span>  
 <xref:System.ServiceModel.Routing.Configuration.BackupEndpointCollection?displayProperty=nameWithType>    
