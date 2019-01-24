---
title: '&lt;workflowControlEndpoint&gt;'
ms.date: 03/30/2017
ms.assetid: 6c89e76c-643b-4b6a-9b25-628f753d7027
ms.openlocfilehash: 9c641d4081d88b059e1d778f6383f85c064af7f0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54558668"
---
# <a name="ltworkflowcontrolendpointgt"></a><span data-ttu-id="f6838-102">&lt;workflowControlEndpoint&gt;</span><span class="sxs-lookup"><span data-stu-id="f6838-102">&lt;workflowControlEndpoint&gt;</span></span>
<span data-ttu-id="f6838-103">Cet élément de configuration définit un point de terminaison standard permettant de contrôler l'exécution d'instances de flux de travail (créer, exécuter, interrompre, arrêter, etc.).</span><span class="sxs-lookup"><span data-stu-id="f6838-103">This configuration element defines a standard endpoint for controlling the execution of workflow instances (create, run, suspend, terminate, etc).</span></span>  
  
<span data-ttu-id="f6838-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="f6838-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="f6838-105">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="f6838-105">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6838-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6838-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <workflowControlEndpoint>
      <standardEndpoint name="String" />
    </workflowControlEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f6838-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f6838-107">Attributes and Elements</span></span>  
 <span data-ttu-id="f6838-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f6838-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f6838-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="f6838-109">Attributes</span></span>  
  
|<span data-ttu-id="f6838-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="f6838-110">Attribute</span></span>|<span data-ttu-id="f6838-111">Description</span><span class="sxs-lookup"><span data-stu-id="f6838-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f6838-112">name</span><span class="sxs-lookup"><span data-stu-id="f6838-112">name</span></span>|<span data-ttu-id="f6838-113">Chaîne qui spécifie le nom de la configuration du point de terminaison standard.</span><span class="sxs-lookup"><span data-stu-id="f6838-113">A String that specifies the name of the configuration of the standard endpoint.</span></span> <span data-ttu-id="f6838-114">Le nom est utilisé dans l'attribut `endpointConfiguration` du point de terminaison de service pour lier un point de terminaison standard à sa configuration.</span><span class="sxs-lookup"><span data-stu-id="f6838-114">The name is used in the `endpointConfiguration` attribute of the service endpoint to link a standard endpoint to its configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f6838-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f6838-115">Child Elements</span></span>  
 <span data-ttu-id="f6838-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f6838-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f6838-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f6838-117">Parent Elements</span></span>  
  
|<span data-ttu-id="f6838-118">Élément</span><span class="sxs-lookup"><span data-stu-id="f6838-118">Element</span></span>|<span data-ttu-id="f6838-119">Description</span><span class="sxs-lookup"><span data-stu-id="f6838-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f6838-120">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="f6838-120">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="f6838-121">Collection de points de terminaison standard qui sont des points de terminaison prédéfinis dont une ou plusieurs propriétés (adresse, liaison, contrat) sont fixes.</span><span class="sxs-lookup"><span data-stu-id="f6838-121">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f6838-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6838-122">See also</span></span>
- <xref:System.ServiceModel.Activities.WorkflowControlEndpoint>
