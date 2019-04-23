---
title: <callbackTimeouts>
ms.date: 03/30/2017
ms.assetid: d7fcfc5f-6d35-491e-8fa6-2f964c1e792f
ms.openlocfilehash: e666bac0be772e417f140e1482649f82ea70e2f6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59173639"
---
# <a name="callbacktimeouts"></a><span data-ttu-id="3df6e-101">\<callbackTimeouts></span><span class="sxs-lookup"><span data-stu-id="3df6e-101">\<callbackTimeouts></span></span>
<span data-ttu-id="3df6e-102">Spécifie la valeur du délai d'attente lors du transfert de transactions du serveur vers un client dans un scénario de contrat de rappel duplex.</span><span class="sxs-lookup"><span data-stu-id="3df6e-102">Specifies the timeout value when flowing transactions from server to client.in a duplex callback contract scenario.</span></span>  
  
 <span data-ttu-id="3df6e-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="3df6e-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="3df6e-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="3df6e-104">\<behaviors></span></span>  
<span data-ttu-id="3df6e-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="3df6e-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="3df6e-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="3df6e-106">\<behavior></span></span>  
<span data-ttu-id="3df6e-107">\<callbackTimeOuts></span><span class="sxs-lookup"><span data-stu-id="3df6e-107">\<callbackTimeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3df6e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3df6e-108">Syntax</span></span>  
  
```xml  
<callbackTimeOuts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="3df6e-109">Type</span><span class="sxs-lookup"><span data-stu-id="3df6e-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3df6e-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3df6e-110">Attributes and Elements</span></span>  
 <span data-ttu-id="3df6e-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3df6e-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3df6e-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="3df6e-112">Attributes</span></span>  
  
|<span data-ttu-id="3df6e-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="3df6e-113">Attribute</span></span>|<span data-ttu-id="3df6e-114">Description</span><span class="sxs-lookup"><span data-stu-id="3df6e-114">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="3df6e-115">Valeur <xref:System.TimeSpan> qui spécifie l’intervalle au cours duquel les transactions doivent être automatiquement effectuées ou arrêtées.</span><span class="sxs-lookup"><span data-stu-id="3df6e-115">A <xref:System.TimeSpan> value that specifies the interval of time within which transactions must complete or be automatically terminated.</span></span> <span data-ttu-id="3df6e-116">La valeur par défaut est « 00 : 00:00 ».</span><span class="sxs-lookup"><span data-stu-id="3df6e-116">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3df6e-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3df6e-117">Child Elements</span></span>  
 <span data-ttu-id="3df6e-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3df6e-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3df6e-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3df6e-119">Parent Elements</span></span>  
  
|<span data-ttu-id="3df6e-120">Élément</span><span class="sxs-lookup"><span data-stu-id="3df6e-120">Element</span></span>|<span data-ttu-id="3df6e-121">Description</span><span class="sxs-lookup"><span data-stu-id="3df6e-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3df6e-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="3df6e-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="3df6e-123">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="3df6e-123">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3df6e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3df6e-124">See also</span></span>

- <xref:System.ServiceModel.Configuration.CallbackTimeoutsElement>
