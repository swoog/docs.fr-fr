---
title: 1016 - CompleteCompletionWorkItem
ms.date: 03/30/2017
ms.assetid: 246929fb-6f14-440a-814b-cd8349350644
ms.openlocfilehash: 3f0904a561a242cd3be528c9707a409b6f98e0fe
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61925084"
---
# <a name="1016---completecompletionworkitem"></a><span data-ttu-id="ae048-102">1016 - CompleteCompletionWorkItem</span><span class="sxs-lookup"><span data-stu-id="ae048-102">1016 - CompleteCompletionWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="ae048-103">Properties</span><span class="sxs-lookup"><span data-stu-id="ae048-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="ae048-104">Id</span><span class="sxs-lookup"><span data-stu-id="ae048-104">ID</span></span>|<span data-ttu-id="ae048-105">1016</span><span class="sxs-lookup"><span data-stu-id="ae048-105">1016</span></span>|  
|<span data-ttu-id="ae048-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="ae048-106">Keywords</span></span>|<span data-ttu-id="ae048-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="ae048-107">WFRuntime</span></span>|  
|<span data-ttu-id="ae048-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="ae048-108">Level</span></span>|<span data-ttu-id="ae048-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="ae048-109">Verbose</span></span>|  
|<span data-ttu-id="ae048-110">Canal</span><span class="sxs-lookup"><span data-stu-id="ae048-110">Channel</span></span>|<span data-ttu-id="ae048-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="ae048-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="ae048-112">Description</span><span class="sxs-lookup"><span data-stu-id="ae048-112">Description</span></span>  
 <span data-ttu-id="ae048-113">Indique qu'un CompletionWorkItem est terminé.</span><span class="sxs-lookup"><span data-stu-id="ae048-113">Indicates a CompletionWorkItem has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="ae048-114">Message</span><span class="sxs-lookup"><span data-stu-id="ae048-114">Message</span></span>  
 <span data-ttu-id="ae048-115">Un CompletionWorkItem est achevé pour l'activité parente « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="ae048-115">A CompletionWorkItem has completed for parent Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span> <span data-ttu-id="ae048-116">Activité terminée « %4 », DisplayName : « %5 », InstanceId : « %6 ».</span><span class="sxs-lookup"><span data-stu-id="ae048-116">Completed Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="ae048-117">Détails</span><span class="sxs-lookup"><span data-stu-id="ae048-117">Details</span></span>  
  
|<span data-ttu-id="ae048-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="ae048-118">Data Item Name</span></span>|<span data-ttu-id="ae048-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="ae048-119">Data Item Type</span></span>|<span data-ttu-id="ae048-120">Description</span><span class="sxs-lookup"><span data-stu-id="ae048-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="ae048-121">ParentActivity</span><span class="sxs-lookup"><span data-stu-id="ae048-121">ParentActivity</span></span>|<span data-ttu-id="ae048-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="ae048-122">xs:string</span></span>|<span data-ttu-id="ae048-123">Nom de type de l'activité parente.</span><span class="sxs-lookup"><span data-stu-id="ae048-123">The type name of the parent activity.</span></span>|  
|<span data-ttu-id="ae048-124">ParentDisplayName</span><span class="sxs-lookup"><span data-stu-id="ae048-124">ParentDisplayName</span></span>|<span data-ttu-id="ae048-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="ae048-125">xs:string</span></span>|<span data-ttu-id="ae048-126">Nom complet de l'activité parente.</span><span class="sxs-lookup"><span data-stu-id="ae048-126">The display name of the parent activity.</span></span>|  
|<span data-ttu-id="ae048-127">ParentInstanceId</span><span class="sxs-lookup"><span data-stu-id="ae048-127">ParentInstanceId</span></span>|<span data-ttu-id="ae048-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="ae048-128">xs:string</span></span>|<span data-ttu-id="ae048-129">ID d'instance de l'activité parente.</span><span class="sxs-lookup"><span data-stu-id="ae048-129">The instance id of the parent activity.</span></span>|  
|<span data-ttu-id="ae048-130">CompletedActivity</span><span class="sxs-lookup"><span data-stu-id="ae048-130">CompletedActivity</span></span>|<span data-ttu-id="ae048-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="ae048-131">xs:string</span></span>|<span data-ttu-id="ae048-132">Nom de type de l'activité achevée.</span><span class="sxs-lookup"><span data-stu-id="ae048-132">The type name of the completed activity.</span></span>|  
|<span data-ttu-id="ae048-133">CompletedActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="ae048-133">CompletedActivityDisplayName</span></span>|<span data-ttu-id="ae048-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="ae048-134">xs:string</span></span>|<span data-ttu-id="ae048-135">Nom complet de l'activité achevée.</span><span class="sxs-lookup"><span data-stu-id="ae048-135">The display name of the completed activity.</span></span>|  
|<span data-ttu-id="ae048-136">CompletedActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="ae048-136">CompletedActivityInstanceId</span></span>|<span data-ttu-id="ae048-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="ae048-137">xs:string</span></span>|<span data-ttu-id="ae048-138">ID d'instance de l'activité achevée.</span><span class="sxs-lookup"><span data-stu-id="ae048-138">The instance id of the completed activity.</span></span>|  
|<span data-ttu-id="ae048-139">AppDomain</span><span class="sxs-lookup"><span data-stu-id="ae048-139">AppDomain</span></span>|<span data-ttu-id="ae048-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="ae048-140">xs:string</span></span>|<span data-ttu-id="ae048-141">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="ae048-141">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
