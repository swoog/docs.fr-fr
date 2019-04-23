---
title: <backupLists>
ms.date: 03/30/2017
ms.assetid: 593b3390-f65b-4684-ad40-0596b62f0954
ms.openlocfilehash: 6e44dbe3c0966c6d243db343b9f9b0dec2480cb1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59134444"
---
# <a name="backuplists"></a><span data-ttu-id="b02e1-101">\<backupLists></span><span class="sxs-lookup"><span data-stu-id="b02e1-101">\<backupLists></span></span>
<span data-ttu-id="b02e1-102">Représente une section de configuration pour la définition d'un ensemble de services de sauvegarde utilisés dans la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="b02e1-102">Represents a configuration section for defining a set of backup services used in error handling.</span></span> <span data-ttu-id="b02e1-103">Chaque élément enfant est une liste de sauvegarde qui énumère un ensemble de points de terminaison que vous souhaitez que le Service de routage à utiliser au cas où le point de terminaison principal n’est pas accessible.</span><span class="sxs-lookup"><span data-stu-id="b02e1-103">Each child element is a backup list that enumerates a set of endpoints that you would like the Routing Service to use in case the primary endpoint can't be reached.</span></span> <span data-ttu-id="b02e1-104">Si le premier point de terminaison de la liste est inactif, le service de routage bascule automatiquement sur le suivant dans la liste.</span><span class="sxs-lookup"><span data-stu-id="b02e1-104">If the first endpoint in the list is down, the Routing Service will automatically fail-over to the next one in the list.</span></span>  <span data-ttu-id="b02e1-105">Vous disposez ainsi d’une méthode rapide pour renforcer la fiabilité de votre application sans avoir à apprendre à votre application cliente à gérer des modèles complexes ou à rechercher l’emplacement de tous vos services déployés.</span><span class="sxs-lookup"><span data-stu-id="b02e1-105">This gives you a quick way to add reliability to your application without having to teach your client application how to handle complex patterns or where all of your services are deployed.</span></span>  
  
 <span data-ttu-id="b02e1-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="b02e1-106">\<system.serviceModel></span></span>  
<span data-ttu-id="b02e1-107">\<routing></span><span class="sxs-lookup"><span data-stu-id="b02e1-107">\<routing></span></span>  
<span data-ttu-id="b02e1-108">\<backupLists></span><span class="sxs-lookup"><span data-stu-id="b02e1-108">\<backupLists></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b02e1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b02e1-109">Syntax</span></span>  
  
```xml  
<routing>
  <backupLists>
    <backupList name="String">
      <add endpointName="String" />
    </backupList>
  </backupLists>
</routing>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b02e1-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b02e1-110">Attributes and Elements</span></span>  
 <span data-ttu-id="b02e1-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b02e1-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b02e1-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="b02e1-112">Attributes</span></span>  
 <span data-ttu-id="b02e1-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b02e1-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="b02e1-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b02e1-114">Child Elements</span></span>  
  
|<span data-ttu-id="b02e1-115">Élément</span><span class="sxs-lookup"><span data-stu-id="b02e1-115">Element</span></span>|<span data-ttu-id="b02e1-116">Description</span><span class="sxs-lookup"><span data-stu-id="b02e1-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b02e1-117">\<filter></span><span class="sxs-lookup"><span data-stu-id="b02e1-117">\<filter></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filter.md)|<span data-ttu-id="b02e1-118">Contient une liste de points de terminaison que vous souhaitez que le Service de routage à utiliser au cas où le point de terminaison principal n’est pas accessible.</span><span class="sxs-lookup"><span data-stu-id="b02e1-118">Contains a list of endpoints that you would like the Routing Service to use in case the primary endpoint can't be reached.</span></span> <span data-ttu-id="b02e1-119">.</span><span class="sxs-lookup"><span data-stu-id="b02e1-119">.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b02e1-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b02e1-120">Parent Elements</span></span>  
  
|<span data-ttu-id="b02e1-121">Élément</span><span class="sxs-lookup"><span data-stu-id="b02e1-121">Element</span></span>|<span data-ttu-id="b02e1-122">Description</span><span class="sxs-lookup"><span data-stu-id="b02e1-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b02e1-123">\<routing></span><span class="sxs-lookup"><span data-stu-id="b02e1-123">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="b02e1-124">Représente une section de configuration pour définir un ensemble de filtres de routage, déterminant le type de Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> à utiliser lors de l’évaluation des messages entrants, ainsi que le routage des tables qui définissent les points de terminaison cible à envoyer des messages lorsqu’un filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="b02e1-124">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b02e1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b02e1-125">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.BackupEndpointCollection?displayProperty=nameWithType>
