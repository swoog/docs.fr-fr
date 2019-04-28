---
title: <callbackTimeouts>
ms.date: 03/30/2017
ms.assetid: d7fcfc5f-6d35-491e-8fa6-2f964c1e792f
ms.openlocfilehash: e666bac0be772e417f140e1482649f82ea70e2f6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61673418"
---
# <a name="callbacktimeouts"></a><span data-ttu-id="06b9a-101">\<callbackTimeouts></span><span class="sxs-lookup"><span data-stu-id="06b9a-101">\<callbackTimeouts></span></span>
<span data-ttu-id="06b9a-102">Spécifie la valeur du délai d'attente lors du transfert de transactions du serveur vers un client dans un scénario de contrat de rappel duplex.</span><span class="sxs-lookup"><span data-stu-id="06b9a-102">Specifies the timeout value when flowing transactions from server to client.in a duplex callback contract scenario.</span></span>  
  
 <span data-ttu-id="06b9a-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="06b9a-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="06b9a-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="06b9a-104">\<behaviors></span></span>  
<span data-ttu-id="06b9a-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="06b9a-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="06b9a-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="06b9a-106">\<behavior></span></span>  
<span data-ttu-id="06b9a-107">\<callbackTimeOuts></span><span class="sxs-lookup"><span data-stu-id="06b9a-107">\<callbackTimeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="06b9a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06b9a-108">Syntax</span></span>  
  
```xml  
<callbackTimeOuts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="06b9a-109">Type</span><span class="sxs-lookup"><span data-stu-id="06b9a-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="06b9a-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="06b9a-110">Attributes and Elements</span></span>  
 <span data-ttu-id="06b9a-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="06b9a-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="06b9a-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="06b9a-112">Attributes</span></span>  
  
|<span data-ttu-id="06b9a-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="06b9a-113">Attribute</span></span>|<span data-ttu-id="06b9a-114">Description</span><span class="sxs-lookup"><span data-stu-id="06b9a-114">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="06b9a-115">Valeur <xref:System.TimeSpan> qui spécifie l’intervalle au cours duquel les transactions doivent être automatiquement effectuées ou arrêtées.</span><span class="sxs-lookup"><span data-stu-id="06b9a-115">A <xref:System.TimeSpan> value that specifies the interval of time within which transactions must complete or be automatically terminated.</span></span> <span data-ttu-id="06b9a-116">La valeur par défaut est « 00 : 00:00 ».</span><span class="sxs-lookup"><span data-stu-id="06b9a-116">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="06b9a-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="06b9a-117">Child Elements</span></span>  
 <span data-ttu-id="06b9a-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="06b9a-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="06b9a-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="06b9a-119">Parent Elements</span></span>  
  
|<span data-ttu-id="06b9a-120">Élément</span><span class="sxs-lookup"><span data-stu-id="06b9a-120">Element</span></span>|<span data-ttu-id="06b9a-121">Description</span><span class="sxs-lookup"><span data-stu-id="06b9a-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="06b9a-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="06b9a-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="06b9a-123">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="06b9a-123">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="06b9a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06b9a-124">See also</span></span>

- <xref:System.ServiceModel.Configuration.CallbackTimeoutsElement>
