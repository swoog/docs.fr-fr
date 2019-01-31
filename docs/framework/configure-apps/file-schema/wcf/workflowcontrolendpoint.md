---
title: <workflowControlEndpoint>
ms.date: 03/30/2017
ms.assetid: 6c89e76c-643b-4b6a-9b25-628f753d7027
ms.openlocfilehash: de0a51ed6f2a878ab3a6ebe15863f1f2925034ce
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55272580"
---
# <a name="workflowcontrolendpoint"></a><span data-ttu-id="5b981-101">\<workflowControlEndpoint></span><span class="sxs-lookup"><span data-stu-id="5b981-101">\<workflowControlEndpoint></span></span>
<span data-ttu-id="5b981-102">Cet élément de configuration définit un point de terminaison standard permettant de contrôler l'exécution d'instances de flux de travail (créer, exécuter, interrompre, arrêter, etc.).</span><span class="sxs-lookup"><span data-stu-id="5b981-102">This configuration element defines a standard endpoint for controlling the execution of workflow instances (create, run, suspend, terminate, etc).</span></span>  
  
<span data-ttu-id="5b981-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="5b981-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="5b981-104">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="5b981-104">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5b981-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b981-105">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <workflowControlEndpoint>
      <standardEndpoint name="String" />
    </workflowControlEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5b981-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5b981-106">Attributes and Elements</span></span>  
 <span data-ttu-id="5b981-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5b981-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5b981-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="5b981-108">Attributes</span></span>  
  
|<span data-ttu-id="5b981-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="5b981-109">Attribute</span></span>|<span data-ttu-id="5b981-110">Description</span><span class="sxs-lookup"><span data-stu-id="5b981-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5b981-111">name</span><span class="sxs-lookup"><span data-stu-id="5b981-111">name</span></span>|<span data-ttu-id="5b981-112">Chaîne qui spécifie le nom de la configuration du point de terminaison standard.</span><span class="sxs-lookup"><span data-stu-id="5b981-112">A String that specifies the name of the configuration of the standard endpoint.</span></span> <span data-ttu-id="5b981-113">Le nom est utilisé dans l'attribut `endpointConfiguration` du point de terminaison de service pour lier un point de terminaison standard à sa configuration.</span><span class="sxs-lookup"><span data-stu-id="5b981-113">The name is used in the `endpointConfiguration` attribute of the service endpoint to link a standard endpoint to its configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5b981-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5b981-114">Child Elements</span></span>  
 <span data-ttu-id="5b981-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5b981-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5b981-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5b981-116">Parent Elements</span></span>  
  
|<span data-ttu-id="5b981-117">Élément</span><span class="sxs-lookup"><span data-stu-id="5b981-117">Element</span></span>|<span data-ttu-id="5b981-118">Description</span><span class="sxs-lookup"><span data-stu-id="5b981-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5b981-119">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="5b981-119">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="5b981-120">Collection de points de terminaison standard qui sont des points de terminaison prédéfinis dont une ou plusieurs propriétés (adresse, liaison, contrat) sont fixes.</span><span class="sxs-lookup"><span data-stu-id="5b981-120">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5b981-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b981-121">See also</span></span>
- <xref:System.ServiceModel.Activities.WorkflowControlEndpoint>
