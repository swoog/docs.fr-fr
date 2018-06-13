---
title: 57398 - MaxInstancesExceeded
ms.date: 03/30/2017
ms.assetid: f943d209-dfeb-43e5-b572-c9a06217936e
ms.openlocfilehash: d644c25ec2dee06eea4a5fb66c30792bb650f252
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33512549"
---
# <a name="57398---maxinstancesexceeded"></a><span data-ttu-id="5a835-102">57398 - MaxInstancesExceeded</span><span class="sxs-lookup"><span data-stu-id="5a835-102">57398 - MaxInstancesExceeded</span></span>
## <a name="properties"></a><span data-ttu-id="5a835-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5a835-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="5a835-104">ID</span><span class="sxs-lookup"><span data-stu-id="5a835-104">ID</span></span>|<span data-ttu-id="5a835-105">57398</span><span class="sxs-lookup"><span data-stu-id="5a835-105">57398</span></span>|  
|<span data-ttu-id="5a835-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="5a835-106">Keywords</span></span>|<span data-ttu-id="5a835-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="5a835-107">WFServices</span></span>|  
|<span data-ttu-id="5a835-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="5a835-108">Level</span></span>|<span data-ttu-id="5a835-109">Avertissement</span><span class="sxs-lookup"><span data-stu-id="5a835-109">Warning</span></span>|  
|<span data-ttu-id="5a835-110">Canal</span><span class="sxs-lookup"><span data-stu-id="5a835-110">Channel</span></span>|<span data-ttu-id="5a835-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="5a835-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="5a835-112">Description</span><span class="sxs-lookup"><span data-stu-id="5a835-112">Description</span></span>  
 <span data-ttu-id="5a835-113">Indique que le système a atteint la limite définie pour la limitation des « MaxConcurrentInstances ».</span><span class="sxs-lookup"><span data-stu-id="5a835-113">Indicates the system hit the limit set for throttle 'MaxConcurrentInstances'.</span></span>  
  
## <a name="message"></a><span data-ttu-id="5a835-114">Message</span><span class="sxs-lookup"><span data-stu-id="5a835-114">Message</span></span>  
 <span data-ttu-id="5a835-115">Le système a atteint la limite définie pour la limitation des 'MaxConcurrentInstances'.</span><span class="sxs-lookup"><span data-stu-id="5a835-115">The system hit the limit set for throttle 'MaxConcurrentInstances'.</span></span> <span data-ttu-id="5a835-116">La limite a été définie sur %1.</span><span class="sxs-lookup"><span data-stu-id="5a835-116">Limit for this throttle was set to %1.</span></span> <span data-ttu-id="5a835-117">La valeur de limitation peut être modifiée en modifiant l'attribut « maxConcurrentInstances » de l'élément serviceThrottle ou en modifiant la propriété « MaxConcurrentInstances » à l'aide du comportement ServiceThrottlingBehavior.</span><span class="sxs-lookup"><span data-stu-id="5a835-117">Throttle value can be changed by modifying attribute 'maxConcurrentInstances' in serviceThrottle element or by modifying 'MaxConcurrentInstances' property on behavior ServiceThrottlingBehavior.</span></span>  
  
## <a name="details"></a><span data-ttu-id="5a835-118">Détails</span><span class="sxs-lookup"><span data-stu-id="5a835-118">Details</span></span>  
  
|<span data-ttu-id="5a835-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="5a835-119">Data Item Name</span></span>|<span data-ttu-id="5a835-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="5a835-120">Data Item Type</span></span>|<span data-ttu-id="5a835-121">Description</span><span class="sxs-lookup"><span data-stu-id="5a835-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="5a835-122">Nom</span><span class="sxs-lookup"><span data-stu-id="5a835-122">Name</span></span>|<span data-ttu-id="5a835-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="5a835-123">xs:string</span></span>|<span data-ttu-id="5a835-124">Nom de l'élément.</span><span class="sxs-lookup"><span data-stu-id="5a835-124">The name of the item.</span></span>|  
|<span data-ttu-id="5a835-125">AppDomain</span><span class="sxs-lookup"><span data-stu-id="5a835-125">AppDomain</span></span>|<span data-ttu-id="5a835-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="5a835-126">xs:string</span></span>|<span data-ttu-id="5a835-127">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="5a835-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
