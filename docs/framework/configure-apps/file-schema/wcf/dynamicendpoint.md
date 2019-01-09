---
title: '&lt;DynamicEndpoint&gt;'
ms.date: 03/30/2017
ms.assetid: 929f223d-176d-4205-9505-234ddb6dbff4
ms.openlocfilehash: 78ec2d4639161f8e10105f205576f052c8a5567c
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146834"
---
# <a name="ltdynamicendpointgt"></a><span data-ttu-id="0b5bd-102">&lt;DynamicEndpoint&gt;</span><span class="sxs-lookup"><span data-stu-id="0b5bd-102">&lt;dynamicEndpoint&gt;</span></span>
<span data-ttu-id="0b5bd-103">Cet élément de configuration définit un point de terminaison standard qui contient des informations pour permettre à une application de fonctionner en tant que programme client qui peut rechercher l'adresse du point de terminaison de manière dynamique au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="0b5bd-103">This configuration element defines a standard endpoint that contains information to enable an application to function as a client program that can find the endpoint address dynamically at runtime.</span></span>  
  
<span data-ttu-id="0b5bd-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="0b5bd-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="0b5bd-105">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="0b5bd-105">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0b5bd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b5bd-106">Syntax</span></span>  
  
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
              <add scope="URI" />
            </scopes>
          </findCriteria>
        </discoveryClientSettings>
      <standardEndpoint>
    </dynamicEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0b5bd-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0b5bd-107">Attributes and Elements</span></span>  
 <span data-ttu-id="0b5bd-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0b5bd-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0b5bd-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="0b5bd-109">Attributes</span></span>  
 <span data-ttu-id="0b5bd-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0b5bd-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="0b5bd-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0b5bd-111">Child Elements</span></span>  
  
|<span data-ttu-id="0b5bd-112">Élément</span><span class="sxs-lookup"><span data-stu-id="0b5bd-112">Element</span></span>|<span data-ttu-id="0b5bd-113">Description</span><span class="sxs-lookup"><span data-stu-id="0b5bd-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0b5bd-114">\<discoveryClientSettings ></span><span class="sxs-lookup"><span data-stu-id="0b5bd-114">\<discoveryClientSettings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryclientsettings.md)|<span data-ttu-id="0b5bd-115">Contient les paramètres requis par une application pour participer au processus de découverte de service en tant que client.</span><span class="sxs-lookup"><span data-stu-id="0b5bd-115">Contains the settings needed by an application to participate in the service discovery process as a client.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0b5bd-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0b5bd-116">Parent Elements</span></span>  
  
|<span data-ttu-id="0b5bd-117">Élément</span><span class="sxs-lookup"><span data-stu-id="0b5bd-117">Element</span></span>|<span data-ttu-id="0b5bd-118">Description</span><span class="sxs-lookup"><span data-stu-id="0b5bd-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0b5bd-119">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="0b5bd-119">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="0b5bd-120">Collection de points de terminaison standard qui sont des points de terminaison prédéfinis dont une ou plusieurs propriétés (adresse, liaison, contrat) sont fixes.</span><span class="sxs-lookup"><span data-stu-id="0b5bd-120">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0b5bd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b5bd-121">See Also</span></span>  
 <xref:System.ServiceModel.Discovery.DynamicEndpoint>  
 <xref:System.ServiceModel.Discovery.Configuration.DynamicEndpointElement>
