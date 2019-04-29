---
title: 57398 - MaxInstancesExceeded
ms.date: 03/30/2017
ms.assetid: f943d209-dfeb-43e5-b572-c9a06217936e
ms.openlocfilehash: d644c25ec2dee06eea4a5fb66c30792bb650f252
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61945962"
---
# <a name="57398---maxinstancesexceeded"></a><span data-ttu-id="81752-102">57398 - MaxInstancesExceeded</span><span class="sxs-lookup"><span data-stu-id="81752-102">57398 - MaxInstancesExceeded</span></span>
## <a name="properties"></a><span data-ttu-id="81752-103">Properties</span><span class="sxs-lookup"><span data-stu-id="81752-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="81752-104">Id</span><span class="sxs-lookup"><span data-stu-id="81752-104">ID</span></span>|<span data-ttu-id="81752-105">57398</span><span class="sxs-lookup"><span data-stu-id="81752-105">57398</span></span>|  
|<span data-ttu-id="81752-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="81752-106">Keywords</span></span>|<span data-ttu-id="81752-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="81752-107">WFServices</span></span>|  
|<span data-ttu-id="81752-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="81752-108">Level</span></span>|<span data-ttu-id="81752-109">Warning</span><span class="sxs-lookup"><span data-stu-id="81752-109">Warning</span></span>|  
|<span data-ttu-id="81752-110">Canal</span><span class="sxs-lookup"><span data-stu-id="81752-110">Channel</span></span>|<span data-ttu-id="81752-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="81752-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="81752-112">Description</span><span class="sxs-lookup"><span data-stu-id="81752-112">Description</span></span>  
 <span data-ttu-id="81752-113">Indique que le système a atteint la limite définie pour la limitation des « MaxConcurrentInstances ».</span><span class="sxs-lookup"><span data-stu-id="81752-113">Indicates the system hit the limit set for throttle 'MaxConcurrentInstances'.</span></span>  
  
## <a name="message"></a><span data-ttu-id="81752-114">Message</span><span class="sxs-lookup"><span data-stu-id="81752-114">Message</span></span>  
 <span data-ttu-id="81752-115">Le système a atteint la limite définie pour la limitation des 'MaxConcurrentInstances'.</span><span class="sxs-lookup"><span data-stu-id="81752-115">The system hit the limit set for throttle 'MaxConcurrentInstances'.</span></span> <span data-ttu-id="81752-116">La limite a été définie sur %1.</span><span class="sxs-lookup"><span data-stu-id="81752-116">Limit for this throttle was set to %1.</span></span> <span data-ttu-id="81752-117">La valeur de limitation peut être modifiée en modifiant l'attribut « maxConcurrentInstances » de l'élément serviceThrottle ou en modifiant la propriété « MaxConcurrentInstances » à l'aide du comportement ServiceThrottlingBehavior.</span><span class="sxs-lookup"><span data-stu-id="81752-117">Throttle value can be changed by modifying attribute 'maxConcurrentInstances' in serviceThrottle element or by modifying 'MaxConcurrentInstances' property on behavior ServiceThrottlingBehavior.</span></span>  
  
## <a name="details"></a><span data-ttu-id="81752-118">Détails</span><span class="sxs-lookup"><span data-stu-id="81752-118">Details</span></span>  
  
|<span data-ttu-id="81752-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="81752-119">Data Item Name</span></span>|<span data-ttu-id="81752-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="81752-120">Data Item Type</span></span>|<span data-ttu-id="81752-121">Description</span><span class="sxs-lookup"><span data-stu-id="81752-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="81752-122">Nom</span><span class="sxs-lookup"><span data-stu-id="81752-122">Name</span></span>|<span data-ttu-id="81752-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="81752-123">xs:string</span></span>|<span data-ttu-id="81752-124">Nom de l'élément.</span><span class="sxs-lookup"><span data-stu-id="81752-124">The name of the item.</span></span>|  
|<span data-ttu-id="81752-125">AppDomain</span><span class="sxs-lookup"><span data-stu-id="81752-125">AppDomain</span></span>|<span data-ttu-id="81752-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="81752-126">xs:string</span></span>|<span data-ttu-id="81752-127">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="81752-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
