---
title: '&lt;callbackTimeouts&gt;'
ms.date: 03/30/2017
ms.assetid: d7fcfc5f-6d35-491e-8fa6-2f964c1e792f
ms.openlocfilehash: 01932fe2b7b7e699311e2c65ec8adaf0aef82dc5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54557901"
---
# <a name="ltcallbacktimeoutsgt"></a><span data-ttu-id="3f267-102">&lt;callbackTimeouts&gt;</span><span class="sxs-lookup"><span data-stu-id="3f267-102">&lt;callbackTimeouts&gt;</span></span>
<span data-ttu-id="3f267-103">Spécifie la valeur du délai d’attente lors du transfert de transactions du serveur vers un client dans un scénario de contrat de rappel duplex.</span><span class="sxs-lookup"><span data-stu-id="3f267-103">Specifies the timeout value when flowing transactions from server to client.in a duplex callback contract scenario.</span></span>  
  
 <span data-ttu-id="3f267-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="3f267-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="3f267-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="3f267-105">\<behaviors></span></span>  
<span data-ttu-id="3f267-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="3f267-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="3f267-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="3f267-107">\<behavior></span></span>  
<span data-ttu-id="3f267-108">\<callbackTimeOuts></span><span class="sxs-lookup"><span data-stu-id="3f267-108">\<callbackTimeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f267-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f267-109">Syntax</span></span>  
  
```xml  
<callbackTimeOuts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="3f267-110">Type</span><span class="sxs-lookup"><span data-stu-id="3f267-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3f267-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3f267-111">Attributes and Elements</span></span>  
 <span data-ttu-id="3f267-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3f267-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3f267-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="3f267-113">Attributes</span></span>  
  
|<span data-ttu-id="3f267-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="3f267-114">Attribute</span></span>|<span data-ttu-id="3f267-115">Description</span><span class="sxs-lookup"><span data-stu-id="3f267-115">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="3f267-116">Valeur <xref:System.TimeSpan> qui spécifie l’intervalle au cours duquel les transactions doivent être automatiquement effectuées ou arrêtées.</span><span class="sxs-lookup"><span data-stu-id="3f267-116">A <xref:System.TimeSpan> value that specifies the interval of time within which transactions must complete or be automatically terminated.</span></span> <span data-ttu-id="3f267-117">La valeur par défaut est « 00 : 00:00 ».</span><span class="sxs-lookup"><span data-stu-id="3f267-117">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3f267-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3f267-118">Child Elements</span></span>  
 <span data-ttu-id="3f267-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3f267-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3f267-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3f267-120">Parent Elements</span></span>  
  
|<span data-ttu-id="3f267-121">Élément</span><span class="sxs-lookup"><span data-stu-id="3f267-121">Element</span></span>|<span data-ttu-id="3f267-122">Description</span><span class="sxs-lookup"><span data-stu-id="3f267-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3f267-123">\<behavior></span><span class="sxs-lookup"><span data-stu-id="3f267-123">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="3f267-124">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="3f267-124">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3f267-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f267-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.CallbackTimeoutsElement>
