---
title: <dynamicEndpoint>
ms.date: 03/30/2017
ms.assetid: 929f223d-176d-4205-9505-234ddb6dbff4
ms.openlocfilehash: 786a70e8c686497e91492938a4d0796db4f6dd91
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55269794"
---
# <a name="dynamicendpoint"></a><span data-ttu-id="02cfd-101">\<dynamicEndpoint></span><span class="sxs-lookup"><span data-stu-id="02cfd-101">\<dynamicEndpoint></span></span>
<span data-ttu-id="02cfd-102">Cet élément de configuration définit un point de terminaison standard qui contient des informations pour permettre à une application de fonctionner en tant que programme client qui peut rechercher l'adresse du point de terminaison de manière dynamique au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="02cfd-102">This configuration element defines a standard endpoint that contains information to enable an application to function as a client program that can find the endpoint address dynamically at runtime.</span></span>  
  
<span data-ttu-id="02cfd-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="02cfd-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="02cfd-104">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="02cfd-104">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="02cfd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02cfd-105">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="02cfd-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="02cfd-106">Attributes and Elements</span></span>  
 <span data-ttu-id="02cfd-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="02cfd-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="02cfd-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="02cfd-108">Attributes</span></span>  
 <span data-ttu-id="02cfd-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="02cfd-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="02cfd-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="02cfd-110">Child Elements</span></span>  
  
|<span data-ttu-id="02cfd-111">Élément</span><span class="sxs-lookup"><span data-stu-id="02cfd-111">Element</span></span>|<span data-ttu-id="02cfd-112">Description</span><span class="sxs-lookup"><span data-stu-id="02cfd-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="02cfd-113">\<discoveryClientSettings></span><span class="sxs-lookup"><span data-stu-id="02cfd-113">\<discoveryClientSettings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryclientsettings.md)|<span data-ttu-id="02cfd-114">Contient les paramètres requis par une application pour participer au processus de découverte de service en tant que client.</span><span class="sxs-lookup"><span data-stu-id="02cfd-114">Contains the settings needed by an application to participate in the service discovery process as a client.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="02cfd-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="02cfd-115">Parent Elements</span></span>  
  
|<span data-ttu-id="02cfd-116">Élément</span><span class="sxs-lookup"><span data-stu-id="02cfd-116">Element</span></span>|<span data-ttu-id="02cfd-117">Description</span><span class="sxs-lookup"><span data-stu-id="02cfd-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="02cfd-118">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="02cfd-118">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="02cfd-119">Collection de points de terminaison standard qui sont des points de terminaison prédéfinis dont une ou plusieurs propriétés (adresse, liaison, contrat) sont fixes.</span><span class="sxs-lookup"><span data-stu-id="02cfd-119">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="02cfd-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02cfd-120">See also</span></span>
- <xref:System.ServiceModel.Discovery.DynamicEndpoint>
- <xref:System.ServiceModel.Discovery.Configuration.DynamicEndpointElement>
