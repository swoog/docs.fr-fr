---
title: <serviceTimeouts>
ms.date: 03/30/2017
ms.assetid: ada536cf-97dc-4cd7-89ec-ed1466c1c557
ms.openlocfilehash: 5c2f0ef7ad509eb5d6c686802c3fe5a75ea1a258
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59075520"
---
# <a name="servicetimeouts"></a><span data-ttu-id="b0343-101">\<serviceTimeouts></span><span class="sxs-lookup"><span data-stu-id="b0343-101">\<serviceTimeouts></span></span>
<span data-ttu-id="b0343-102">Spécifie le délai d'attente pour un service.</span><span class="sxs-lookup"><span data-stu-id="b0343-102">Specifies the timeout for a service.</span></span>  
  
 <span data-ttu-id="b0343-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="b0343-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="b0343-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="b0343-104">\<behaviors></span></span>  
<span data-ttu-id="b0343-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="b0343-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="b0343-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="b0343-106">\<behavior></span></span>  
<span data-ttu-id="b0343-107">\<serviceTimeouts></span><span class="sxs-lookup"><span data-stu-id="b0343-107">\<serviceTimeouts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b0343-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0343-108">Syntax</span></span>  
  
```xml  
<serviceTimeouts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="b0343-109">Type</span><span class="sxs-lookup"><span data-stu-id="b0343-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b0343-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b0343-110">Attributes and Elements</span></span>  
 <span data-ttu-id="b0343-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b0343-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b0343-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="b0343-112">Attributes</span></span>  
  
|<span data-ttu-id="b0343-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="b0343-113">Attribute</span></span>|<span data-ttu-id="b0343-114">Description</span><span class="sxs-lookup"><span data-stu-id="b0343-114">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="b0343-115">Valeur <xref:System.TimeSpan> qui spécifie l’intervalle de temps pour le transfert d’une transaction du client au serveur.</span><span class="sxs-lookup"><span data-stu-id="b0343-115">A <xref:System.TimeSpan> value that specifies the interval of time a transaction must flow from client to server.</span></span> <span data-ttu-id="b0343-116">La valeur par défaut est « 00 : 00:00 ».</span><span class="sxs-lookup"><span data-stu-id="b0343-116">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b0343-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b0343-117">Child Elements</span></span>  
 <span data-ttu-id="b0343-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b0343-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b0343-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b0343-119">Parent Elements</span></span>  
  
|<span data-ttu-id="b0343-120">Élément</span><span class="sxs-lookup"><span data-stu-id="b0343-120">Element</span></span>|<span data-ttu-id="b0343-121">Description</span><span class="sxs-lookup"><span data-stu-id="b0343-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b0343-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="b0343-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="b0343-123">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="b0343-123">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b0343-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0343-124">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceTimeoutsElement>
