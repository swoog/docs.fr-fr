---
title: <findCriteria>
ms.date: 03/30/2017
ms.assetid: 5454cd19-6bf5-4ba8-94d1-f58d10dc1917
ms.openlocfilehash: e82312cb17fbd3f76f781ea37f761e946319a0a0
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57351852"
---
# <a name="findcriteria"></a><span data-ttu-id="3d6c4-101">\<findCriteria></span><span class="sxs-lookup"><span data-stu-id="3d6c4-101">\<findCriteria></span></span>
<span data-ttu-id="3d6c4-102">Élément de configuration qui fournit un jeu de critères utilisé par une application cliente pour rechercher un service de découverte.</span><span class="sxs-lookup"><span data-stu-id="3d6c4-102">A configuration element that supplies a set of criteria used by a client application to search for a discovery service.</span></span> <span data-ttu-id="3d6c4-103">Critères peuvent être regroupées en critères de recherche (spécifiant les services que vous recherchez) et recherchez les critères d’arrêt (la durée pendant laquelle la recherche doit durer).</span><span class="sxs-lookup"><span data-stu-id="3d6c4-103">Criteria can be grouped into search criteria (specifying what services you’re looking for) and find termination criteria (how long the search should last).</span></span>  
  
 <span data-ttu-id="3d6c4-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="3d6c4-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="3d6c4-105">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="3d6c4-105">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3d6c4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d6c4-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <dynamicEndpoint>
      <standardEndpoint>
        <discoveryClientSettings discoveryEndpoint="String">
          <findCriteria duration="TimeSpan"
                        maxResults="Integer"
                        scopeMatchBy="Uri">
            <contractTypeNames>
              <add name="String"
                   namespace="String" />
            </contractTypeNames>
            <extensions />
            <scopes>
              <add scope="URI" />
            </scopes>
          </findCriteria>
        </discoveryClientSettings>
      </standardEndpoint>
    </dynamicEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3d6c4-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3d6c4-107">Attributes and Elements</span></span>  
 <span data-ttu-id="3d6c4-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3d6c4-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3d6c4-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="3d6c4-109">Attributes</span></span>  
  
|<span data-ttu-id="3d6c4-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="3d6c4-110">Attribute</span></span>|<span data-ttu-id="3d6c4-111">Description</span><span class="sxs-lookup"><span data-stu-id="3d6c4-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="3d6c4-112">duration</span><span class="sxs-lookup"><span data-stu-id="3d6c4-112">duration</span></span>|<span data-ttu-id="3d6c4-113">Valeur Timespan qui spécifie le temps d'attente maximal des réponses envoyées par les services sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="3d6c4-113">A Timespan value that specifies the maximum time to wait for replies from services on the network.</span></span> <span data-ttu-id="3d6c4-114">La durée par défaut est de 20 secondes.</span><span class="sxs-lookup"><span data-stu-id="3d6c4-114">The default duration is 20 seconds.</span></span>|  
|<span data-ttu-id="3d6c4-115">maxResults</span><span class="sxs-lookup"><span data-stu-id="3d6c4-115">maxResults</span></span>|<span data-ttu-id="3d6c4-116">Entier qui spécifie le nombre maximal de réponses à attendre en provenance des services sur un réseau ou sur Internet.</span><span class="sxs-lookup"><span data-stu-id="3d6c4-116">An integer that specifies the maximum number of replies to wait for, from services on a network or the Internet.</span></span> <span data-ttu-id="3d6c4-117">Si le nombre maximal de réponses est reçu avant l'écoulement du délai d'attente spécifié dans l'attribut `duration`, l'opération de recherche prend fin.</span><span class="sxs-lookup"><span data-stu-id="3d6c4-117">If maximum replies are received before the value specified in the `duration` attribute has elapsed, the find operation ends.</span></span>|  
|<span data-ttu-id="3d6c4-118">scopeMatchBy</span><span class="sxs-lookup"><span data-stu-id="3d6c4-118">scopeMatchBy</span></span>|<span data-ttu-id="3d6c4-119">URI qui spécifie l'algorithme de correspondance à utiliser, lors de la comparaison des portées dans le message Probe avec celles du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="3d6c4-119">A URI that specify the matching algorithm to use while matching the scopes in the Probe message with that of the endpoint.</span></span><br /><br /> <span data-ttu-id="3d6c4-120">Il existe cinq règles de correspondance de portée prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3d6c4-120">There are five supported scope-matching rules.</span></span> <span data-ttu-id="3d6c4-121">Si vous ne spécifiez pas de règle de correspondance de portée, `ScopeMatchByPrefix` est utilisé.</span><span class="sxs-lookup"><span data-stu-id="3d6c4-121">If you do not specify a scope-matching rule, `ScopeMatchByPrefix` is used.</span></span> <span data-ttu-id="3d6c4-122">Pour plus d'informations, consultez <xref:System.ServiceModel.Discovery.FindCriteria>.</span><span class="sxs-lookup"><span data-stu-id="3d6c4-122">For more information on this, see <xref:System.ServiceModel.Discovery.FindCriteria>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3d6c4-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3d6c4-123">Child Elements</span></span>  
  
|<span data-ttu-id="3d6c4-124">Élément</span><span class="sxs-lookup"><span data-stu-id="3d6c4-124">Element</span></span>|<span data-ttu-id="3d6c4-125">Description</span><span class="sxs-lookup"><span data-stu-id="3d6c4-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3d6c4-126">\<contractTypeNames></span><span class="sxs-lookup"><span data-stu-id="3d6c4-126">\<contractTypeNames></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/contracttypenames.md)|<span data-ttu-id="3d6c4-127">Une collection d’éléments de configuration qui contiennent les noms de types de contrat de service de workflow.</span><span class="sxs-lookup"><span data-stu-id="3d6c4-127">A collection of configuration elements that contain the names of workflow service contract types.</span></span>|  
|<span data-ttu-id="3d6c4-128">\<extensions > de \<findCriteria ></span><span class="sxs-lookup"><span data-stu-id="3d6c4-128">\<extensions> of \<findCriteria></span></span>|<span data-ttu-id="3d6c4-129">Collection d'objets d'élément XML qui fournissent des extensions.</span><span class="sxs-lookup"><span data-stu-id="3d6c4-129">A collection of XML element objects that provide extensions.</span></span>|  
|[<span data-ttu-id="3d6c4-130">\<scopes></span><span class="sxs-lookup"><span data-stu-id="3d6c4-130">\<scopes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)|<span data-ttu-id="3d6c4-131">Collection d’objets qui contiennent des URI absolus utilisés pendant une opération de recherche afin de localiser des services ou un service particulier.</span><span class="sxs-lookup"><span data-stu-id="3d6c4-131">A collection of objects that contain absolute URIs that are used during a find operation to locate a specific service or services.</span></span><br /><br /> <span data-ttu-id="3d6c4-132">Si le service particulier est trouvé, une correspondance réussie est établie entre l'URI de service et l'URI de portée, parfois à l'aide de règles de portée qui gèrent les problèmes de correspondance.</span><span class="sxs-lookup"><span data-stu-id="3d6c4-132">If the specific service is found, a successful match has been made between the service URI and the Scope URI, sometimes with the help of scope rules that handle complications of matching.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="3d6c4-133">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3d6c4-133">Parent Elements</span></span>  
  
|<span data-ttu-id="3d6c4-134">Élément</span><span class="sxs-lookup"><span data-stu-id="3d6c4-134">Element</span></span>|<span data-ttu-id="3d6c4-135">Description</span><span class="sxs-lookup"><span data-stu-id="3d6c4-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3d6c4-136">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="3d6c4-136">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="3d6c4-137">Contient les paramètres requis par une application pour participer au processus de découverte de service en tant que client.</span><span class="sxs-lookup"><span data-stu-id="3d6c4-137">Contains the settings needed by an application to participate in the service discovery process as a client.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3d6c4-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d6c4-138">See also</span></span>
- <xref:System.ServiceModel.Discovery.FindCriteria>
- <xref:System.ServiceModel.Discovery.Configuration.FindCriteriaElement>
