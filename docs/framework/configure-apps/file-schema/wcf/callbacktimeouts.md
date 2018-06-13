---
title: '&lt;callbackTimeouts&gt;'
ms.date: 03/30/2017
ms.assetid: d7fcfc5f-6d35-491e-8fa6-2f964c1e792f
ms.openlocfilehash: 48da0351d162a2143a26cc5b9eaa05b731358639
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32749564"
---
# <a name="ltcallbacktimeoutsgt"></a><span data-ttu-id="20942-102">&lt;callbackTimeouts&gt;</span><span class="sxs-lookup"><span data-stu-id="20942-102">&lt;callbackTimeouts&gt;</span></span>
<span data-ttu-id="20942-103">Spécifie la valeur du délai d’attente lors du transfert de transactions du serveur vers un client dans un scénario de contrat de rappel duplex.</span><span class="sxs-lookup"><span data-stu-id="20942-103">Specifies the timeout value when flowing transactions from server to client.in a duplex callback contract scenario.</span></span>  
  
 <span data-ttu-id="20942-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="20942-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="20942-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="20942-105">\<behaviors></span></span>  
<span data-ttu-id="20942-106">\<endpointBehaviors ></span><span class="sxs-lookup"><span data-stu-id="20942-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="20942-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="20942-107">\<behavior></span></span>  
<span data-ttu-id="20942-108">\<callbackTimeOuts ></span><span class="sxs-lookup"><span data-stu-id="20942-108">\<callbackTimeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20942-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20942-109">Syntax</span></span>  
  
```xml  
<callbackTimeOuts transactionTimeout="TimeSpan" />  
```  
  
## <a name="type"></a><span data-ttu-id="20942-110">Type</span><span class="sxs-lookup"><span data-stu-id="20942-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="20942-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="20942-111">Attributes and Elements</span></span>  
 <span data-ttu-id="20942-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="20942-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="20942-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="20942-113">Attributes</span></span>  
  
|<span data-ttu-id="20942-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="20942-114">Attribute</span></span>|<span data-ttu-id="20942-115">Description</span><span class="sxs-lookup"><span data-stu-id="20942-115">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="20942-116">Valeur <xref:System.TimeSpan> qui spécifie l'intervalle au cours duquel les transactions doivent être automatiquement effectuées ou arrêtées.</span><span class="sxs-lookup"><span data-stu-id="20942-116">A <xref:System.TimeSpan> value that specifies the interval of time within which transactions must complete or be automatically terminated.</span></span> <span data-ttu-id="20942-117">La valeur par défaut est « 00 : 00:00 ».</span><span class="sxs-lookup"><span data-stu-id="20942-117">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="20942-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="20942-118">Child Elements</span></span>  
 <span data-ttu-id="20942-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="20942-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="20942-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="20942-120">Parent Elements</span></span>  
  
|<span data-ttu-id="20942-121">Élément</span><span class="sxs-lookup"><span data-stu-id="20942-121">Element</span></span>|<span data-ttu-id="20942-122">Description</span><span class="sxs-lookup"><span data-stu-id="20942-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="20942-123">\<behavior></span><span class="sxs-lookup"><span data-stu-id="20942-123">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="20942-124">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="20942-124">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="20942-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20942-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.CallbackTimeoutsElement>
