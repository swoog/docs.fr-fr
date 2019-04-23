---
title: <dynamicEndpoint>
ms.date: 03/30/2017
ms.assetid: 929f223d-176d-4205-9505-234ddb6dbff4
ms.openlocfilehash: e1a53869faa1997d2e79c3d2869a15001ee29626
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59187744"
---
# <a name="dynamicendpoint"></a><span data-ttu-id="4b136-101">\<dynamicEndpoint></span><span class="sxs-lookup"><span data-stu-id="4b136-101">\<dynamicEndpoint></span></span>
<span data-ttu-id="4b136-102">Cet élément de configuration définit un point de terminaison standard qui contient des informations pour permettre à une application de fonctionner en tant que programme client qui peut rechercher l'adresse du point de terminaison de manière dynamique au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="4b136-102">This configuration element defines a standard endpoint that contains information to enable an application to function as a client program that can find the endpoint address dynamically at runtime.</span></span>  
  
<span data-ttu-id="4b136-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="4b136-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="4b136-104">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="4b136-104">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b136-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b136-105">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4b136-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4b136-106">Attributes and Elements</span></span>  
 <span data-ttu-id="4b136-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4b136-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4b136-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="4b136-108">Attributes</span></span>  
 <span data-ttu-id="4b136-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4b136-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4b136-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4b136-110">Child Elements</span></span>  
  
|<span data-ttu-id="4b136-111">Élément</span><span class="sxs-lookup"><span data-stu-id="4b136-111">Element</span></span>|<span data-ttu-id="4b136-112">Description</span><span class="sxs-lookup"><span data-stu-id="4b136-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4b136-113">\<discoveryClientSettings></span><span class="sxs-lookup"><span data-stu-id="4b136-113">\<discoveryClientSettings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryclientsettings.md)|<span data-ttu-id="4b136-114">Contient les paramètres requis par une application pour participer au processus de découverte de service en tant que client.</span><span class="sxs-lookup"><span data-stu-id="4b136-114">Contains the settings needed by an application to participate in the service discovery process as a client.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4b136-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4b136-115">Parent Elements</span></span>  
  
|<span data-ttu-id="4b136-116">Élément</span><span class="sxs-lookup"><span data-stu-id="4b136-116">Element</span></span>|<span data-ttu-id="4b136-117">Description</span><span class="sxs-lookup"><span data-stu-id="4b136-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4b136-118">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="4b136-118">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="4b136-119">Collection de points de terminaison standard qui sont des points de terminaison prédéfinis dont une ou plusieurs propriétés (adresse, liaison, contrat) sont fixes.</span><span class="sxs-lookup"><span data-stu-id="4b136-119">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4b136-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b136-120">See also</span></span>

- <xref:System.ServiceModel.Discovery.DynamicEndpoint>
- <xref:System.ServiceModel.Discovery.Configuration.DynamicEndpointElement>
