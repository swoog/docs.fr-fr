---
title: 1014 - ScheduleCompletionWorkItem
ms.date: 03/30/2017
ms.assetid: 84203735-478d-42d8-a320-c175dbddcb38
ms.openlocfilehash: 50b00a49ea73dcbe09e8f4c4195cbce8c1cbf615
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61982265"
---
# <a name="1014---schedulecompletionworkitem"></a><span data-ttu-id="fa404-102">1014 - ScheduleCompletionWorkItem</span><span class="sxs-lookup"><span data-stu-id="fa404-102">1014 - ScheduleCompletionWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="fa404-103">Properties</span><span class="sxs-lookup"><span data-stu-id="fa404-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="fa404-104">Id</span><span class="sxs-lookup"><span data-stu-id="fa404-104">ID</span></span>|<span data-ttu-id="fa404-105">1014</span><span class="sxs-lookup"><span data-stu-id="fa404-105">1014</span></span>|  
|<span data-ttu-id="fa404-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fa404-106">Keywords</span></span>|<span data-ttu-id="fa404-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="fa404-107">WFRuntime</span></span>|  
|<span data-ttu-id="fa404-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="fa404-108">Level</span></span>|<span data-ttu-id="fa404-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="fa404-109">Verbose</span></span>|  
|<span data-ttu-id="fa404-110">Canal</span><span class="sxs-lookup"><span data-stu-id="fa404-110">Channel</span></span>|<span data-ttu-id="fa404-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="fa404-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="fa404-112">Description</span><span class="sxs-lookup"><span data-stu-id="fa404-112">Description</span></span>  
 <span data-ttu-id="fa404-113">Indique qu'un CompletionWorkItem a été planifié.</span><span class="sxs-lookup"><span data-stu-id="fa404-113">Indicates a CompletionWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="fa404-114">Message</span><span class="sxs-lookup"><span data-stu-id="fa404-114">Message</span></span>  
 <span data-ttu-id="fa404-115">Qu’un CompletionWorkItem a été planifié pour l’activité parente « %1 », DisplayName : « %2 », InstanceId : '%3'.</span><span class="sxs-lookup"><span data-stu-id="fa404-115">A CompletionWorkItem has been scheduled for parent Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="fa404-116">Activité terminée « %4 », DisplayName : « %5 », InstanceId : « %6 ».</span><span class="sxs-lookup"><span data-stu-id="fa404-116">Completed Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="fa404-117">Détails</span><span class="sxs-lookup"><span data-stu-id="fa404-117">Details</span></span>  
  
|<span data-ttu-id="fa404-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="fa404-118">Data Item Name</span></span>|<span data-ttu-id="fa404-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="fa404-119">Data Item Type</span></span>|<span data-ttu-id="fa404-120">Description</span><span class="sxs-lookup"><span data-stu-id="fa404-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="fa404-121">ParentActivity</span><span class="sxs-lookup"><span data-stu-id="fa404-121">ParentActivity</span></span>|<span data-ttu-id="fa404-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="fa404-122">xs:string</span></span>|<span data-ttu-id="fa404-123">Nom de type de l'activité parente.</span><span class="sxs-lookup"><span data-stu-id="fa404-123">The type name of the parent activity.</span></span>|  
|<span data-ttu-id="fa404-124">ParentDisplayName</span><span class="sxs-lookup"><span data-stu-id="fa404-124">ParentDisplayName</span></span>|<span data-ttu-id="fa404-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="fa404-125">xs:string</span></span>|<span data-ttu-id="fa404-126">Nom complet de l'activité parente.</span><span class="sxs-lookup"><span data-stu-id="fa404-126">The display name of the parent activity.</span></span>|  
|<span data-ttu-id="fa404-127">ParentInstanceId</span><span class="sxs-lookup"><span data-stu-id="fa404-127">ParentInstanceId</span></span>|<span data-ttu-id="fa404-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="fa404-128">xs:string</span></span>|<span data-ttu-id="fa404-129">ID d'instance de l'activité parente.</span><span class="sxs-lookup"><span data-stu-id="fa404-129">The instance id of the parent activity.</span></span>|  
|<span data-ttu-id="fa404-130">CompletedActivity</span><span class="sxs-lookup"><span data-stu-id="fa404-130">CompletedActivity</span></span>|<span data-ttu-id="fa404-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="fa404-131">xs:string</span></span>|<span data-ttu-id="fa404-132">Nom de type de l'activité achevée.</span><span class="sxs-lookup"><span data-stu-id="fa404-132">The type name of the completed activity.</span></span>|  
|<span data-ttu-id="fa404-133">CompletedActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="fa404-133">CompletedActivityDisplayName</span></span>|<span data-ttu-id="fa404-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="fa404-134">xs:string</span></span>|<span data-ttu-id="fa404-135">Nom complet de l'activité achevée.</span><span class="sxs-lookup"><span data-stu-id="fa404-135">The display name of the completed activity.</span></span>|  
|<span data-ttu-id="fa404-136">CompletedActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="fa404-136">CompletedActivityInstanceId</span></span>|<span data-ttu-id="fa404-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="fa404-137">xs:string</span></span>|<span data-ttu-id="fa404-138">ID d'instance de l'activité achevée.</span><span class="sxs-lookup"><span data-stu-id="fa404-138">The instance id of the completed activity.</span></span>|  
|<span data-ttu-id="fa404-139">AppDomain</span><span class="sxs-lookup"><span data-stu-id="fa404-139">AppDomain</span></span>|<span data-ttu-id="fa404-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="fa404-140">xs:string</span></span>|<span data-ttu-id="fa404-141">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="fa404-141">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
