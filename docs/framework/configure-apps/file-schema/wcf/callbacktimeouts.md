---
title: <callbackTimeouts>
ms.date: 03/30/2017
ms.assetid: d7fcfc5f-6d35-491e-8fa6-2f964c1e792f
ms.openlocfilehash: e666bac0be772e417f140e1482649f82ea70e2f6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59173639"
---
# <a name="callbacktimeouts"></a><span data-ttu-id="1d411-101">\<callbackTimeouts></span><span class="sxs-lookup"><span data-stu-id="1d411-101">\<callbackTimeouts></span></span>
<span data-ttu-id="1d411-102">Spécifie la valeur du délai d'attente lors du transfert de transactions du serveur vers un client dans un scénario de contrat de rappel duplex.</span><span class="sxs-lookup"><span data-stu-id="1d411-102">Specifies the timeout value when flowing transactions from server to client.in a duplex callback contract scenario.</span></span>  
  
 <span data-ttu-id="1d411-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="1d411-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="1d411-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="1d411-104">\<behaviors></span></span>  
<span data-ttu-id="1d411-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="1d411-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="1d411-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="1d411-106">\<behavior></span></span>  
<span data-ttu-id="1d411-107">\<callbackTimeOuts></span><span class="sxs-lookup"><span data-stu-id="1d411-107">\<callbackTimeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1d411-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d411-108">Syntax</span></span>  
  
```xml  
<callbackTimeOuts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="1d411-109">Type</span><span class="sxs-lookup"><span data-stu-id="1d411-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1d411-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1d411-110">Attributes and Elements</span></span>  
 <span data-ttu-id="1d411-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1d411-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1d411-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="1d411-112">Attributes</span></span>  
  
|<span data-ttu-id="1d411-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="1d411-113">Attribute</span></span>|<span data-ttu-id="1d411-114">Description</span><span class="sxs-lookup"><span data-stu-id="1d411-114">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="1d411-115">Valeur <xref:System.TimeSpan> qui spécifie l’intervalle au cours duquel les transactions doivent être automatiquement effectuées ou arrêtées.</span><span class="sxs-lookup"><span data-stu-id="1d411-115">A <xref:System.TimeSpan> value that specifies the interval of time within which transactions must complete or be automatically terminated.</span></span> <span data-ttu-id="1d411-116">La valeur par défaut est « 00 : 00:00 ».</span><span class="sxs-lookup"><span data-stu-id="1d411-116">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1d411-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1d411-117">Child Elements</span></span>  
 <span data-ttu-id="1d411-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1d411-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1d411-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1d411-119">Parent Elements</span></span>  
  
|<span data-ttu-id="1d411-120">Élément</span><span class="sxs-lookup"><span data-stu-id="1d411-120">Element</span></span>|<span data-ttu-id="1d411-121">Description</span><span class="sxs-lookup"><span data-stu-id="1d411-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1d411-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="1d411-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="1d411-123">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1d411-123">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1d411-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d411-124">See also</span></span>

- <xref:System.ServiceModel.Configuration.CallbackTimeoutsElement>
