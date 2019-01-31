---
title: <serviceTimeouts>
ms.date: 03/30/2017
ms.assetid: ada536cf-97dc-4cd7-89ec-ed1466c1c557
ms.openlocfilehash: b67ea137e6c116d00a8a098b9c0df99430114dc5
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55267285"
---
# <a name="servicetimeouts"></a><span data-ttu-id="26855-101">\<serviceTimeouts></span><span class="sxs-lookup"><span data-stu-id="26855-101">\<serviceTimeouts></span></span>
<span data-ttu-id="26855-102">Spécifie le délai d'attente pour un service.</span><span class="sxs-lookup"><span data-stu-id="26855-102">Specifies the timeout for a service.</span></span>  
  
 <span data-ttu-id="26855-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="26855-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="26855-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="26855-104">\<behaviors></span></span>  
<span data-ttu-id="26855-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="26855-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="26855-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="26855-106">\<behavior></span></span>  
<span data-ttu-id="26855-107">\<serviceTimeouts></span><span class="sxs-lookup"><span data-stu-id="26855-107">\<serviceTimeouts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26855-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26855-108">Syntax</span></span>  
  
```xml  
<serviceTimeouts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="26855-109">Type</span><span class="sxs-lookup"><span data-stu-id="26855-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="26855-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="26855-110">Attributes and Elements</span></span>  
 <span data-ttu-id="26855-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="26855-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="26855-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="26855-112">Attributes</span></span>  
  
|<span data-ttu-id="26855-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="26855-113">Attribute</span></span>|<span data-ttu-id="26855-114">Description</span><span class="sxs-lookup"><span data-stu-id="26855-114">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="26855-115">Valeur <xref:System.TimeSpan> qui spécifie l’intervalle de temps pour le transfert d’une transaction du client au serveur.</span><span class="sxs-lookup"><span data-stu-id="26855-115">A <xref:System.TimeSpan> value that specifies the interval of time a transaction must flow from client to server.</span></span> <span data-ttu-id="26855-116">La valeur par défaut est « 00 : 00:00 ».</span><span class="sxs-lookup"><span data-stu-id="26855-116">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="26855-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="26855-117">Child Elements</span></span>  
 <span data-ttu-id="26855-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="26855-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="26855-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="26855-119">Parent Elements</span></span>  
  
|<span data-ttu-id="26855-120">Élément</span><span class="sxs-lookup"><span data-stu-id="26855-120">Element</span></span>|<span data-ttu-id="26855-121">Description</span><span class="sxs-lookup"><span data-stu-id="26855-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="26855-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="26855-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="26855-123">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="26855-123">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="26855-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26855-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.ServiceTimeoutsElement>
