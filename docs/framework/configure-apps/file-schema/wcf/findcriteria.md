---
title: '&lt;findCriteria&gt;'
ms.date: 03/30/2017
ms.assetid: 5454cd19-6bf5-4ba8-94d1-f58d10dc1917
ms.openlocfilehash: b90e6cab923075dbf750dc0d26a0eb1196cfde32
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54741238"
---
# <a name="ltfindcriteriagt"></a><span data-ttu-id="bebe7-102">&lt;findCriteria&gt;</span><span class="sxs-lookup"><span data-stu-id="bebe7-102">&lt;findCriteria&gt;</span></span>
<span data-ttu-id="bebe7-103">Élément de configuration qui fournit un jeu de critères utilisé par une application cliente pour rechercher un service de découverte.</span><span class="sxs-lookup"><span data-stu-id="bebe7-103">A configuration element that supplies a set of criteria used by a client application to search for a discovery service.</span></span> <span data-ttu-id="bebe7-104">Critères peuvent être regroupées en critères de recherche (spécifiant les services que vous recherchez) et recherchez les critères d’arrêt (la durée pendant laquelle la recherche doit durer).</span><span class="sxs-lookup"><span data-stu-id="bebe7-104">Criteria can be grouped into search criteria (specifying what services you’re looking for) and find termination criteria (how long the search should last).</span></span>  
  
 <span data-ttu-id="bebe7-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="bebe7-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="bebe7-106">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="bebe7-106">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bebe7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bebe7-107">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bebe7-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="bebe7-108">Attributes and Elements</span></span>  
 <span data-ttu-id="bebe7-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="bebe7-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bebe7-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="bebe7-110">Attributes</span></span>  
  
|<span data-ttu-id="bebe7-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="bebe7-111">Attribute</span></span>|<span data-ttu-id="bebe7-112">Description</span><span class="sxs-lookup"><span data-stu-id="bebe7-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="bebe7-113">duration</span><span class="sxs-lookup"><span data-stu-id="bebe7-113">duration</span></span>|<span data-ttu-id="bebe7-114">Valeur Timespan qui spécifie le temps d'attente maximal des réponses envoyées par les services sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="bebe7-114">A Timespan value that specifies the maximum time to wait for replies from services on the network.</span></span> <span data-ttu-id="bebe7-115">La durée par défaut est de 20 secondes.</span><span class="sxs-lookup"><span data-stu-id="bebe7-115">The default duration is 20 seconds.</span></span>|  
|<span data-ttu-id="bebe7-116">maxResults</span><span class="sxs-lookup"><span data-stu-id="bebe7-116">maxResults</span></span>|<span data-ttu-id="bebe7-117">Entier qui spécifie le nombre maximal de réponses à attendre en provenance des services sur un réseau ou sur Internet.</span><span class="sxs-lookup"><span data-stu-id="bebe7-117">An integer that specifies the maximum number of replies to wait for, from services on a network or the Internet.</span></span> <span data-ttu-id="bebe7-118">Si le nombre maximal de réponses est reçu avant l'écoulement du délai d'attente spécifié dans l'attribut `duration`, l'opération de recherche prend fin.</span><span class="sxs-lookup"><span data-stu-id="bebe7-118">If maximum replies are received before the value specified in the `duration` attribute has elapsed, the find operation ends.</span></span>|  
|<span data-ttu-id="bebe7-119">scopeMatchBy</span><span class="sxs-lookup"><span data-stu-id="bebe7-119">scopeMatchBy</span></span>|<span data-ttu-id="bebe7-120">URI qui spécifie l'algorithme de correspondance à utiliser, lors de la comparaison des portées dans le message Probe avec celles du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="bebe7-120">A URI that specify the matching algorithm to use while matching the scopes in the Probe message with that of the endpoint.</span></span><br /><br /> <span data-ttu-id="bebe7-121">Il existe cinq règles de correspondance de portée prises en charge.</span><span class="sxs-lookup"><span data-stu-id="bebe7-121">There are five supported scope-matching rules.</span></span> <span data-ttu-id="bebe7-122">Si vous ne spécifiez pas de règle de correspondance de portée, `ScopeMatchByPrefix` est utilisé.</span><span class="sxs-lookup"><span data-stu-id="bebe7-122">If you do not specify a scope-matching rule, `ScopeMatchByPrefix` is used.</span></span> <span data-ttu-id="bebe7-123">Pour plus d'informations, consultez <xref:System.ServiceModel.Discovery.FindCriteria>.</span><span class="sxs-lookup"><span data-stu-id="bebe7-123">For more information on this, see <xref:System.ServiceModel.Discovery.FindCriteria>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bebe7-124">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bebe7-124">Child Elements</span></span>  
  
|<span data-ttu-id="bebe7-125">Élément</span><span class="sxs-lookup"><span data-stu-id="bebe7-125">Element</span></span>|<span data-ttu-id="bebe7-126">Description</span><span class="sxs-lookup"><span data-stu-id="bebe7-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bebe7-127">\<contractTypeNames></span><span class="sxs-lookup"><span data-stu-id="bebe7-127">\<contractTypeNames></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/contracttypenames.md)|<span data-ttu-id="bebe7-128">Une collection d’éléments de configuration qui contiennent les noms de types de contrat de service de workflow.</span><span class="sxs-lookup"><span data-stu-id="bebe7-128">A collection of configuration elements that contain the names of workflow service contract types.</span></span>|  
|<span data-ttu-id="bebe7-129">\<extensions > de \<findCriteria ></span><span class="sxs-lookup"><span data-stu-id="bebe7-129">\<extensions> of \<findCriteria></span></span>|<span data-ttu-id="bebe7-130">Collection d’objets d’élément XML qui fournissent des extensions.</span><span class="sxs-lookup"><span data-stu-id="bebe7-130">A collection of XML element objects that provide extensions.</span></span>|  
|[<span data-ttu-id="bebe7-131">\<scopes></span><span class="sxs-lookup"><span data-stu-id="bebe7-131">\<scopes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)|<span data-ttu-id="bebe7-132">Collection d’objets qui contiennent des URI absolus utilisés pendant une opération de recherche afin de localiser des services ou un service particulier.</span><span class="sxs-lookup"><span data-stu-id="bebe7-132">A collection of objects that contain absolute URIs that are used during a find operation to locate a specific service or services.</span></span><br /><br /> <span data-ttu-id="bebe7-133">Si le service particulier est trouvé, une correspondance réussie est établie entre l'URI de service et l'URI de portée, parfois à l'aide de règles de portée qui gèrent les problèmes de correspondance.</span><span class="sxs-lookup"><span data-stu-id="bebe7-133">If the specific service is found, a successful match has been made between the service URI and the Scope URI, sometimes with the help of scope rules that handle complications of matching.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="bebe7-134">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bebe7-134">Parent Elements</span></span>  
  
|<span data-ttu-id="bebe7-135">Élément</span><span class="sxs-lookup"><span data-stu-id="bebe7-135">Element</span></span>|<span data-ttu-id="bebe7-136">Description</span><span class="sxs-lookup"><span data-stu-id="bebe7-136">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bebe7-137">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="bebe7-137">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="bebe7-138">Contient les paramètres requis par une application pour participer au processus de découverte de service en tant que client.</span><span class="sxs-lookup"><span data-stu-id="bebe7-138">Contains the settings needed by an application to participate in the service discovery process as a client.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="bebe7-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bebe7-139">See also</span></span>
- <xref:System.ServiceModel.Discovery.FindCriteria>
- <xref:System.ServiceModel.Discovery.Configuration.FindCriteriaElement>
