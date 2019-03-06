---
title: <discoveryClient>
ms.date: 03/30/2017
ms.assetid: a78f74c3-1152-4149-ab29-3f12d316caeb
ms.openlocfilehash: 512a91bf25180606213eb9eb3b4f7c6a0cb4cbbf
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57366229"
---
# <a name="discoveryclient"></a><span data-ttu-id="65c5a-101">\<discoveryClient></span><span class="sxs-lookup"><span data-stu-id="65c5a-101">\<discoveryClient></span></span>
<span data-ttu-id="65c5a-102">Élément de configuration qui crée une liaison personnalisée permettant à une application cliente de rechercher automatiquement un service détectable et de trouver son adresse au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="65c5a-102">A configuration element for creating a custom binding that enables a client application to automatically search for a discoverable service and find its address at runtime.</span></span>  
  
<span data-ttu-id="65c5a-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="65c5a-103">\<system.serviceModel></span></span>  
<span data-ttu-id="65c5a-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="65c5a-104">\<bindings></span></span>  
<span data-ttu-id="65c5a-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="65c5a-105">\<customBinding></span></span>  
<span data-ttu-id="65c5a-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="65c5a-106">\<binding></span></span>  
<span data-ttu-id="65c5a-107">\<discoveryClient></span><span class="sxs-lookup"><span data-stu-id="65c5a-107">\<discoveryClient></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="65c5a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65c5a-108">Syntax</span></span>  
  
```xml  
<discoveryClient discoveryEndpoint="String">
  <findCriteria duration="TimeSpan"
                maxResults="Integer"
                scopeMatchBy="Uri">
    <contractTypeNames>
      <add name="String"
           namespace="String" />
    </contractTypeNames>
    <extensions />
    <scopes>
      <add scope="URI"/>
    </scopes>
  </findCriteria>
</discoveryClient>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="65c5a-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="65c5a-109">Attributes and Elements</span></span>  
 <span data-ttu-id="65c5a-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="65c5a-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="65c5a-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="65c5a-111">Attributes</span></span>  
  
|<span data-ttu-id="65c5a-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="65c5a-112">Attribute</span></span>|<span data-ttu-id="65c5a-113">Description</span><span class="sxs-lookup"><span data-stu-id="65c5a-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="65c5a-114">discoveryEndpoint</span><span class="sxs-lookup"><span data-stu-id="65c5a-114">discoveryEndpoint</span></span>|<span data-ttu-id="65c5a-115">Chaîne qui contient le nom du point de terminaison de découverte permettant à une application cliente de rechercher automatiquement un service détectable et de trouver son adresse au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="65c5a-115">A string that contains the name of the Discovery Endpoint that enables a client application to automatically search for a discoverable service and find its address at runtime.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="65c5a-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="65c5a-116">Child Elements</span></span>  
  
|<span data-ttu-id="65c5a-117">Élément</span><span class="sxs-lookup"><span data-stu-id="65c5a-117">Element</span></span>|<span data-ttu-id="65c5a-118">Description</span><span class="sxs-lookup"><span data-stu-id="65c5a-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="65c5a-119">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="65c5a-119">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="65c5a-120">Élément de configuration qui fournit un jeu de critères utilisé par une application cliente pour rechercher un service de découverte.</span><span class="sxs-lookup"><span data-stu-id="65c5a-120">A configuration element that supplies a set of criteria used by a client application to search for a discovery service.</span></span> <span data-ttu-id="65c5a-121">Critères peuvent être regroupées en critères de recherche (spécifiant les services que vous recherchez) et recherchez les critères d’arrêt (la durée pendant laquelle la recherche doit durer).</span><span class="sxs-lookup"><span data-stu-id="65c5a-121">Criteria can be grouped into search criteria (specifying what services you’re looking for) and find termination criteria (how long the search should last).</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="65c5a-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="65c5a-122">Parent Elements</span></span>  
  
|<span data-ttu-id="65c5a-123">Élément</span><span class="sxs-lookup"><span data-stu-id="65c5a-123">Element</span></span>|<span data-ttu-id="65c5a-124">Description</span><span class="sxs-lookup"><span data-stu-id="65c5a-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="65c5a-125">\<binding></span><span class="sxs-lookup"><span data-stu-id="65c5a-125">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="65c5a-126">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="65c5a-126">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="65c5a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65c5a-127">See also</span></span>
- <xref:System.ServiceModel.Discovery.DiscoveryClientBindingElement>
- <xref:System.ServiceModel.Discovery.Configuration.DiscoveryClientElement>
