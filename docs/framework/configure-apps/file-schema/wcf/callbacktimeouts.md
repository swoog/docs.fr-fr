---
title: <callbackTimeouts>
ms.date: 03/30/2017
ms.assetid: d7fcfc5f-6d35-491e-8fa6-2f964c1e792f
ms.openlocfilehash: 269500324ad1beaa0b519fa17d251ee942276faa
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55269066"
---
# <a name="callbacktimeouts"></a><span data-ttu-id="2e6aa-101">\<callbackTimeouts></span><span class="sxs-lookup"><span data-stu-id="2e6aa-101">\<callbackTimeouts></span></span>
<span data-ttu-id="2e6aa-102">Spécifie la valeur du délai d’attente lors du transfert de transactions du serveur vers un client dans un scénario de contrat de rappel duplex.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-102">Specifies the timeout value when flowing transactions from server to client.in a duplex callback contract scenario.</span></span>  
  
 <span data-ttu-id="2e6aa-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="2e6aa-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="2e6aa-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="2e6aa-104">\<behaviors></span></span>  
<span data-ttu-id="2e6aa-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="2e6aa-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="2e6aa-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="2e6aa-106">\<behavior></span></span>  
<span data-ttu-id="2e6aa-107">\<callbackTimeOuts></span><span class="sxs-lookup"><span data-stu-id="2e6aa-107">\<callbackTimeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2e6aa-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e6aa-108">Syntax</span></span>  
  
```xml  
<callbackTimeOuts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="2e6aa-109">Type</span><span class="sxs-lookup"><span data-stu-id="2e6aa-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2e6aa-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="2e6aa-110">Attributes and Elements</span></span>  
 <span data-ttu-id="2e6aa-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2e6aa-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="2e6aa-112">Attributes</span></span>  
  
|<span data-ttu-id="2e6aa-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="2e6aa-113">Attribute</span></span>|<span data-ttu-id="2e6aa-114">Description</span><span class="sxs-lookup"><span data-stu-id="2e6aa-114">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="2e6aa-115">Valeur <xref:System.TimeSpan> qui spécifie l’intervalle au cours duquel les transactions doivent être automatiquement effectuées ou arrêtées.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-115">A <xref:System.TimeSpan> value that specifies the interval of time within which transactions must complete or be automatically terminated.</span></span> <span data-ttu-id="2e6aa-116">La valeur par défaut est « 00 : 00:00 ».</span><span class="sxs-lookup"><span data-stu-id="2e6aa-116">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2e6aa-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2e6aa-117">Child Elements</span></span>  
 <span data-ttu-id="2e6aa-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2e6aa-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2e6aa-119">Parent Elements</span></span>  
  
|<span data-ttu-id="2e6aa-120">Élément</span><span class="sxs-lookup"><span data-stu-id="2e6aa-120">Element</span></span>|<span data-ttu-id="2e6aa-121">Description</span><span class="sxs-lookup"><span data-stu-id="2e6aa-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2e6aa-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="2e6aa-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="2e6aa-123">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-123">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="2e6aa-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e6aa-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.CallbackTimeoutsElement>
