---
title: '&lt;discoveryClientSettings&gt;'
ms.date: 03/30/2017
ms.assetid: 02e1b823-a8bb-4074-90d5-8599f71e8f9d
ms.openlocfilehash: bb443334e0713464e64ec9297bbab4ad11eda723
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145053"
---
# <a name="ltdiscoveryclientsettingsgt"></a><span data-ttu-id="e1342-102">&lt;discoveryClientSettings&gt;</span><span class="sxs-lookup"><span data-stu-id="e1342-102">&lt;discoveryClientSettings&gt;</span></span>
<span data-ttu-id="e1342-103">Contient les paramètres requis par une application pour participer au processus de découverte de service en tant que client.</span><span class="sxs-lookup"><span data-stu-id="e1342-103">Contains the settings needed by an application to participate in the service discovery process as a client.</span></span>  
  
<span data-ttu-id="e1342-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="e1342-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="e1342-105">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="e1342-105">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e1342-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1342-106">Syntax</span></span>  
  
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
            <contractTypeNames>
            <extensions />
            <scopes>
              <add scope="URI"/>
            </scopes>
          </findCriteria>
        </discoveryClientSettings>
      <standardEndpoint>
    </dynamicEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e1342-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e1342-107">Attributes and Elements</span></span>  
 <span data-ttu-id="e1342-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e1342-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e1342-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="e1342-109">Attributes</span></span>  
  
|<span data-ttu-id="e1342-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="e1342-110">Attribute</span></span>|<span data-ttu-id="e1342-111">Description</span><span class="sxs-lookup"><span data-stu-id="e1342-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e1342-112">discoveryEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1342-112">discoveryEndpoint</span></span>|<span data-ttu-id="e1342-113">Chaîne qui contient le nom du point de terminaison de découverte permettant à une application cliente de rechercher automatiquement un service détectable et de trouver son adresse au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="e1342-113">A string that contains the name of the Discovery Endpoint that enables a client application to automatically search for a discoverable service and find its address at runtime.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e1342-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e1342-114">Child Elements</span></span>  
  
|<span data-ttu-id="e1342-115">Élément</span><span class="sxs-lookup"><span data-stu-id="e1342-115">Element</span></span>|<span data-ttu-id="e1342-116">Description</span><span class="sxs-lookup"><span data-stu-id="e1342-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e1342-117">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="e1342-117">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="e1342-118">Élément de configuration qui fournit un jeu de critères utilisé par une application cliente pour rechercher un service de découverte.</span><span class="sxs-lookup"><span data-stu-id="e1342-118">A configuration element that supplies a set of criteria used by a client application to search for a discovery service.</span></span> <span data-ttu-id="e1342-119">Critères peuvent être regroupées en critères de recherche (spécifiant les services que vous recherchez) et recherchez les critères d’arrêt (la durée pendant laquelle la recherche doit durer).</span><span class="sxs-lookup"><span data-stu-id="e1342-119">Criteria can be grouped into search criteria (specifying what services you’re looking for) and find termination criteria (how long the search should last).</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e1342-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e1342-120">Parent Elements</span></span>  
  
|<span data-ttu-id="e1342-121">Élément</span><span class="sxs-lookup"><span data-stu-id="e1342-121">Element</span></span>|<span data-ttu-id="e1342-122">Description</span><span class="sxs-lookup"><span data-stu-id="e1342-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e1342-123">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="e1342-123">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="e1342-124">Définit un point de terminaison standard qui contient des informations pour permettre à une application de fonctionner en tant que programme client qui peut rechercher l'adresse du point de terminaison de manière dynamique au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="e1342-124">Defines a standard endpoint that contains information to enable an application to function as a client program that can find the endpoint address dynamically at runtime.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e1342-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1342-125">See Also</span></span>  
 <xref:System.ServiceModel.Discovery.DiscoveryClientBindingElement>  
 <xref:System.ServiceModel.Discovery.Configuration.DiscoveryClientSettingsElement>
