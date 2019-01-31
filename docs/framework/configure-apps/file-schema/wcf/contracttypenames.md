---
title: <contractTypeNames>
ms.date: 03/30/2017
ms.assetid: 5ec5efc6-87f8-4160-9be0-dcd2e01df3df
ms.openlocfilehash: d8f2b600b700a19cf587a6c8c4cc3f0e851edbd9
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55261277"
---
# <a name="contracttypenames"></a><span data-ttu-id="51504-101">\<contractTypeNames></span><span class="sxs-lookup"><span data-stu-id="51504-101">\<contractTypeNames></span></span>
<span data-ttu-id="51504-102">Section de configuration qui spécifie une liste de noms de type de contrat, qui sont les noms de contrat des services recherchés, et les critères généralement utilisés lors de la recherche d'un service.</span><span class="sxs-lookup"><span data-stu-id="51504-102">A configuration section that specifies a list of contract type names, which are the contract names of the services being searched for, and the criteria typically used when searching for a service.</span></span> <span data-ttu-id="51504-103">Si plusieurs noms de contrat sont spécifiés, seuls les points de terminaison de service correspondant à TOUS les contrats répondent.</span><span class="sxs-lookup"><span data-stu-id="51504-103">If more than one contract name is specified, only service endpoints matching ALL contracts will reply.</span></span> <span data-ttu-id="51504-104">Notez que dans Windows Communication Foundation (WCF), un point de terminaison peut uniquement prendre en charge un seul contrat.</span><span class="sxs-lookup"><span data-stu-id="51504-104">Note that in Windows Communication Foundation (WCF), an endpoint can only support one contract.</span></span>  
  
 <span data-ttu-id="51504-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="51504-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="51504-106">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="51504-106">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="51504-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51504-107">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="51504-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="51504-108">Attributes and Elements</span></span>  
 <span data-ttu-id="51504-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="51504-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="51504-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="51504-110">Attributes</span></span>  
 <span data-ttu-id="51504-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="51504-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="51504-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="51504-112">Child Elements</span></span>  
  
|<span data-ttu-id="51504-113">Élément</span><span class="sxs-lookup"><span data-stu-id="51504-113">Element</span></span>|<span data-ttu-id="51504-114">Description</span><span class="sxs-lookup"><span data-stu-id="51504-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="51504-115">\<add></span><span class="sxs-lookup"><span data-stu-id="51504-115">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/contracttypenames.md)|<span data-ttu-id="51504-116">Un nom de type de contrat est une propriété qui fait référence au jeu de critères utilisé en général au cours de la recherche d'un service.</span><span class="sxs-lookup"><span data-stu-id="51504-116">A contract type name is a property that refers to the set of criteria typically used when searching for a service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="51504-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="51504-117">Parent Elements</span></span>  
  
|<span data-ttu-id="51504-118">Élément</span><span class="sxs-lookup"><span data-stu-id="51504-118">Element</span></span>|<span data-ttu-id="51504-119">Description</span><span class="sxs-lookup"><span data-stu-id="51504-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="51504-120">\<findCriteria></span><span class="sxs-lookup"><span data-stu-id="51504-120">\<findCriteria></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/findcriteria.md)|<span data-ttu-id="51504-121">Élément de configuration qui fournit un jeu de critères utilisé par une application cliente pour rechercher un service de découverte.</span><span class="sxs-lookup"><span data-stu-id="51504-121">A configuration element that supplies a set of criteria used by a client application to search for a discovery service.</span></span> <span data-ttu-id="51504-122">Critères peuvent être regroupées en critères de recherche (spécifiant les services que vous recherchez) et recherchez les critères d’arrêt (la durée pendant laquelle la recherche doit durer).</span><span class="sxs-lookup"><span data-stu-id="51504-122">Criteria can be grouped into search criteria (specifying what services you’re looking for) and find termination criteria (how long the search should last).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="51504-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51504-123">See also</span></span>
- <xref:System.ServiceModel.Discovery.FindCriteria>
- <xref:System.ServiceModel.Discovery.Configuration.FindCriteriaElement>
- <xref:System.ServiceModel.Discovery.Configuration.ContractTypeNameElementCollection>
