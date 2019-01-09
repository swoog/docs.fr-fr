---
title: '&lt;webScriptEndpoint&gt;'
ms.date: 03/30/2017
ms.assetid: 85cb5ecf-351b-45f3-aa29-aa2e4b64bcdd
ms.openlocfilehash: beb17d4ccc39bcca30e97d4f0df47c797cde6216
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148771"
---
# <a name="ltwebscriptendpointgt"></a><span data-ttu-id="1e200-102">&lt;webScriptEndpoint&gt;</span><span class="sxs-lookup"><span data-stu-id="1e200-102">&lt;webScriptEndpoint&gt;</span></span>
<span data-ttu-id="1e200-103">Cet élément de configuration définit un point de terminaison standard avec fixe [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) automatiquement une liaison qui ajoute le [ \<enableWebScript >](../../../../../docs/framework/configure-apps/file-schema/wcf/enablewebscript.md) comportement.</span><span class="sxs-lookup"><span data-stu-id="1e200-103">This configuration element defines a standard endpoint with a fixed [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) binding that automatically adds the [\<enableWebScript>](../../../../../docs/framework/configure-apps/file-schema/wcf/enablewebscript.md) behavior.</span></span> <span data-ttu-id="1e200-104">Utilisez ce point de terminaison lorsque vous écrivez un service appelé à partir d'une application ASP.NET AJAX.</span><span class="sxs-lookup"><span data-stu-id="1e200-104">Use this endpoint when you are writing a service that is called from an ASP.NET AJAX application.</span></span>  
  
<span data-ttu-id="1e200-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="1e200-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="1e200-106">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="1e200-106">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1e200-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e200-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <webScriptEndpoint>
      <standardEndpoint webEndpointType="String" />
    </webScriptEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1e200-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1e200-108">Attributes and Elements</span></span>  
 <span data-ttu-id="1e200-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1e200-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1e200-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="1e200-110">Attributes</span></span>  
  
|<span data-ttu-id="1e200-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="1e200-111">Attribute</span></span>|<span data-ttu-id="1e200-112">Description</span><span class="sxs-lookup"><span data-stu-id="1e200-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="1e200-113">webEndpointType</span><span class="sxs-lookup"><span data-stu-id="1e200-113">webEndpointType</span></span>|<span data-ttu-id="1e200-114">Chaîne qui spécifie le type du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1e200-114">A string that specifies the type of the endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1e200-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1e200-115">Child Elements</span></span>  
 <span data-ttu-id="1e200-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1e200-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1e200-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1e200-117">Parent Elements</span></span>  
  
|<span data-ttu-id="1e200-118">Élément</span><span class="sxs-lookup"><span data-stu-id="1e200-118">Element</span></span>|<span data-ttu-id="1e200-119">Description</span><span class="sxs-lookup"><span data-stu-id="1e200-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1e200-120">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="1e200-120">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="1e200-121">Collection de points de terminaison standard qui sont des points de terminaison prédéfinis dont une ou plusieurs propriétés (adresse, liaison, contrat) sont fixes.</span><span class="sxs-lookup"><span data-stu-id="1e200-121">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1e200-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e200-122">See Also</span></span>  
 <xref:System.ServiceModel.Description.WebScriptEndpoint>  
 <xref:System.ServiceModel.Configuration.WebScriptEndpointElement>
