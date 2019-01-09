---
title: '&lt;workflowControlEndpoint&gt;'
ms.date: 03/30/2017
ms.assetid: 6c89e76c-643b-4b6a-9b25-628f753d7027
ms.openlocfilehash: 178ccc8ac35b0ac76d74c818dce43dcffc5c0835
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54144949"
---
# <a name="ltworkflowcontrolendpointgt"></a><span data-ttu-id="c7402-102">&lt;workflowControlEndpoint&gt;</span><span class="sxs-lookup"><span data-stu-id="c7402-102">&lt;workflowControlEndpoint&gt;</span></span>
<span data-ttu-id="c7402-103">Cet élément de configuration définit un point de terminaison standard permettant de contrôler l'exécution d'instances de flux de travail (créer, exécuter, interrompre, arrêter, etc.).</span><span class="sxs-lookup"><span data-stu-id="c7402-103">This configuration element defines a standard endpoint for controlling the execution of workflow instances (create, run, suspend, terminate, etc).</span></span>  
  
<span data-ttu-id="c7402-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="c7402-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="c7402-105">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="c7402-105">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7402-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7402-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <workflowControlEndpoint>
      <standardEndpoint name="String" />
    </workflowControlEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c7402-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c7402-107">Attributes and Elements</span></span>  
 <span data-ttu-id="c7402-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c7402-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c7402-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="c7402-109">Attributes</span></span>  
  
|<span data-ttu-id="c7402-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="c7402-110">Attribute</span></span>|<span data-ttu-id="c7402-111">Description</span><span class="sxs-lookup"><span data-stu-id="c7402-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c7402-112">name</span><span class="sxs-lookup"><span data-stu-id="c7402-112">name</span></span>|<span data-ttu-id="c7402-113">Chaîne qui spécifie le nom de la configuration du point de terminaison standard.</span><span class="sxs-lookup"><span data-stu-id="c7402-113">A String that specifies the name of the configuration of the standard endpoint.</span></span> <span data-ttu-id="c7402-114">Le nom est utilisé dans l'attribut `endpointConfiguration` du point de terminaison de service pour lier un point de terminaison standard à sa configuration.</span><span class="sxs-lookup"><span data-stu-id="c7402-114">The name is used in the `endpointConfiguration` attribute of the service endpoint to link a standard endpoint to its configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c7402-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c7402-115">Child Elements</span></span>  
 <span data-ttu-id="c7402-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c7402-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c7402-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c7402-117">Parent Elements</span></span>  
  
|<span data-ttu-id="c7402-118">Élément</span><span class="sxs-lookup"><span data-stu-id="c7402-118">Element</span></span>|<span data-ttu-id="c7402-119">Description</span><span class="sxs-lookup"><span data-stu-id="c7402-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c7402-120">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="c7402-120">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="c7402-121">Collection de points de terminaison standard qui sont des points de terminaison prédéfinis dont une ou plusieurs propriétés (adresse, liaison, contrat) sont fixes.</span><span class="sxs-lookup"><span data-stu-id="c7402-121">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c7402-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7402-122">See Also</span></span>  
 <xref:System.ServiceModel.Activities.WorkflowControlEndpoint>
