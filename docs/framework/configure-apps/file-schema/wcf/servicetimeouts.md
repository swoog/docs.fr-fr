---
title: '&lt;serviceTimeouts&gt;'
ms.date: 03/30/2017
ms.assetid: ada536cf-97dc-4cd7-89ec-ed1466c1c557
ms.openlocfilehash: 4cb4b4ae6fe01430989d9ee5f3d94b16778595aa
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148472"
---
# <a name="ltservicetimeoutsgt"></a><span data-ttu-id="0742b-102">&lt;serviceTimeouts&gt;</span><span class="sxs-lookup"><span data-stu-id="0742b-102">&lt;serviceTimeouts&gt;</span></span>
<span data-ttu-id="0742b-103">Spécifie le délai d'attente pour un service.</span><span class="sxs-lookup"><span data-stu-id="0742b-103">Specifies the timeout for a service.</span></span>  
  
 <span data-ttu-id="0742b-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="0742b-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="0742b-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="0742b-105">\<behaviors></span></span>  
<span data-ttu-id="0742b-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="0742b-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="0742b-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="0742b-107">\<behavior></span></span>  
<span data-ttu-id="0742b-108">\<serviceTimeouts ></span><span class="sxs-lookup"><span data-stu-id="0742b-108">\<serviceTimeouts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0742b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0742b-109">Syntax</span></span>  
  
```xml  
<serviceTimeouts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="0742b-110">Type</span><span class="sxs-lookup"><span data-stu-id="0742b-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0742b-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0742b-111">Attributes and Elements</span></span>  
 <span data-ttu-id="0742b-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0742b-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0742b-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="0742b-113">Attributes</span></span>  
  
|<span data-ttu-id="0742b-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="0742b-114">Attribute</span></span>|<span data-ttu-id="0742b-115">Description</span><span class="sxs-lookup"><span data-stu-id="0742b-115">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="0742b-116">Valeur <xref:System.TimeSpan> qui spécifie l’intervalle de temps pour le transfert d’une transaction du client au serveur.</span><span class="sxs-lookup"><span data-stu-id="0742b-116">A <xref:System.TimeSpan> value that specifies the interval of time a transaction must flow from client to server.</span></span> <span data-ttu-id="0742b-117">La valeur par défaut est « 00 : 00:00 ».</span><span class="sxs-lookup"><span data-stu-id="0742b-117">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0742b-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0742b-118">Child Elements</span></span>  
 <span data-ttu-id="0742b-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0742b-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0742b-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0742b-120">Parent Elements</span></span>  
  
|<span data-ttu-id="0742b-121">Élément</span><span class="sxs-lookup"><span data-stu-id="0742b-121">Element</span></span>|<span data-ttu-id="0742b-122">Description</span><span class="sxs-lookup"><span data-stu-id="0742b-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0742b-123">\<behavior></span><span class="sxs-lookup"><span data-stu-id="0742b-123">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="0742b-124">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="0742b-124">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0742b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0742b-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceTimeoutsElement>
