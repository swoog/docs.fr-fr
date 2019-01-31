---
title: <webScriptEndpoint>
ms.date: 03/30/2017
ms.assetid: 85cb5ecf-351b-45f3-aa29-aa2e4b64bcdd
ms.openlocfilehash: 3d95624c82388ed6219fc567dd2d3c17bedad7a1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255287"
---
# <a name="webscriptendpoint"></a><span data-ttu-id="c6874-101">\<webScriptEndpoint></span><span class="sxs-lookup"><span data-stu-id="c6874-101">\<webScriptEndpoint></span></span>
<span data-ttu-id="c6874-102">Cet élément de configuration définit un point de terminaison standard avec fixe [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) automatiquement une liaison qui ajoute le [ \<enableWebScript >](../../../../../docs/framework/configure-apps/file-schema/wcf/enablewebscript.md) comportement.</span><span class="sxs-lookup"><span data-stu-id="c6874-102">This configuration element defines a standard endpoint with a fixed [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) binding that automatically adds the [\<enableWebScript>](../../../../../docs/framework/configure-apps/file-schema/wcf/enablewebscript.md) behavior.</span></span> <span data-ttu-id="c6874-103">Utilisez ce point de terminaison lorsque vous écrivez un service appelé à partir d'une application ASP.NET AJAX.</span><span class="sxs-lookup"><span data-stu-id="c6874-103">Use this endpoint when you are writing a service that is called from an ASP.NET AJAX application.</span></span>  
  
<span data-ttu-id="c6874-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="c6874-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="c6874-105">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="c6874-105">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c6874-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6874-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <webScriptEndpoint>
      <standardEndpoint webEndpointType="String" />
    </webScriptEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c6874-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c6874-107">Attributes and Elements</span></span>  
 <span data-ttu-id="c6874-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c6874-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c6874-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="c6874-109">Attributes</span></span>  
  
|<span data-ttu-id="c6874-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="c6874-110">Attribute</span></span>|<span data-ttu-id="c6874-111">Description</span><span class="sxs-lookup"><span data-stu-id="c6874-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c6874-112">webEndpointType</span><span class="sxs-lookup"><span data-stu-id="c6874-112">webEndpointType</span></span>|<span data-ttu-id="c6874-113">Chaîne qui spécifie le type du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="c6874-113">A string that specifies the type of the endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c6874-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c6874-114">Child Elements</span></span>  
 <span data-ttu-id="c6874-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c6874-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c6874-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c6874-116">Parent Elements</span></span>  
  
|<span data-ttu-id="c6874-117">Élément</span><span class="sxs-lookup"><span data-stu-id="c6874-117">Element</span></span>|<span data-ttu-id="c6874-118">Description</span><span class="sxs-lookup"><span data-stu-id="c6874-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c6874-119">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="c6874-119">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="c6874-120">Collection de points de terminaison standard qui sont des points de terminaison prédéfinis dont une ou plusieurs propriétés (adresse, liaison, contrat) sont fixes.</span><span class="sxs-lookup"><span data-stu-id="c6874-120">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c6874-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6874-121">See also</span></span>
- <xref:System.ServiceModel.Description.WebScriptEndpoint>
- <xref:System.ServiceModel.Configuration.WebScriptEndpointElement>
