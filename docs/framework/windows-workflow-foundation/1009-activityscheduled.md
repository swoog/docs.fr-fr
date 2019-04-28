---
title: 1009 - ActivityScheduled
ms.date: 03/30/2017
ms.assetid: 307e38b6-d47e-47a4-9708-e74d8314b1a1
ms.openlocfilehash: 0e3ea53a7b0509fcb8b73b61193742d615ac7e91
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924655"
---
# <a name="1009---activityscheduled"></a><span data-ttu-id="d40ed-102">1009 - ActivityScheduled</span><span class="sxs-lookup"><span data-stu-id="d40ed-102">1009 - ActivityScheduled</span></span>
## <a name="properties"></a><span data-ttu-id="d40ed-103">Properties</span><span class="sxs-lookup"><span data-stu-id="d40ed-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="d40ed-104">Id</span><span class="sxs-lookup"><span data-stu-id="d40ed-104">ID</span></span>|<span data-ttu-id="d40ed-105">1009</span><span class="sxs-lookup"><span data-stu-id="d40ed-105">1009</span></span>|  
|<span data-ttu-id="d40ed-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d40ed-106">Keywords</span></span>|<span data-ttu-id="d40ed-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="d40ed-107">WFRuntime</span></span>|  
|<span data-ttu-id="d40ed-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="d40ed-108">Level</span></span>|<span data-ttu-id="d40ed-109">Information</span><span class="sxs-lookup"><span data-stu-id="d40ed-109">Information</span></span>|  
|<span data-ttu-id="d40ed-110">Canal</span><span class="sxs-lookup"><span data-stu-id="d40ed-110">Channel</span></span>|<span data-ttu-id="d40ed-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="d40ed-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="d40ed-112">Description</span><span class="sxs-lookup"><span data-stu-id="d40ed-112">Description</span></span>  
 <span data-ttu-id="d40ed-113">Indique qu'une activité est planifiée en vue de son exécution.</span><span class="sxs-lookup"><span data-stu-id="d40ed-113">Indicates an activity is being scheduled for execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="d40ed-114">Message</span><span class="sxs-lookup"><span data-stu-id="d40ed-114">Message</span></span>  
 <span data-ttu-id="d40ed-115">L'activité parent « %1 », DisplayName : « %2 », InstanceId : « %3 » a planifié l'activité enfant « %4 », DisplayName : « %5 », InstanceId : « %6 ».</span><span class="sxs-lookup"><span data-stu-id="d40ed-115">Parent Activity '%1', DisplayName: '%2', InstanceId: '%3' scheduled child Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="d40ed-116">Détails</span><span class="sxs-lookup"><span data-stu-id="d40ed-116">Details</span></span>  
  
|<span data-ttu-id="d40ed-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="d40ed-117">Data Item Name</span></span>|<span data-ttu-id="d40ed-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="d40ed-118">Data Item Type</span></span>|<span data-ttu-id="d40ed-119">Description</span><span class="sxs-lookup"><span data-stu-id="d40ed-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="d40ed-120">ParentActivity</span><span class="sxs-lookup"><span data-stu-id="d40ed-120">ParentActivity</span></span>|<span data-ttu-id="d40ed-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="d40ed-121">xs:string</span></span>|<span data-ttu-id="d40ed-122">Nom de type de l'activité parente.</span><span class="sxs-lookup"><span data-stu-id="d40ed-122">The type name of the parent activity.</span></span>|  
|<span data-ttu-id="d40ed-123">ParentDisplayName</span><span class="sxs-lookup"><span data-stu-id="d40ed-123">ParentDisplayName</span></span>|<span data-ttu-id="d40ed-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="d40ed-124">xs:string</span></span>|<span data-ttu-id="d40ed-125">Nom complet de l'activité parente.</span><span class="sxs-lookup"><span data-stu-id="d40ed-125">The display name of the parent activity.</span></span>|  
|<span data-ttu-id="d40ed-126">ParentInstanceId</span><span class="sxs-lookup"><span data-stu-id="d40ed-126">ParentInstanceId</span></span>|<span data-ttu-id="d40ed-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="d40ed-127">xs:string</span></span>|<span data-ttu-id="d40ed-128">ID d'instance de l'activité parente.</span><span class="sxs-lookup"><span data-stu-id="d40ed-128">The instance id of the parent activity.</span></span>|  
|<span data-ttu-id="d40ed-129">ChildActivity</span><span class="sxs-lookup"><span data-stu-id="d40ed-129">ChildActivity</span></span>|<span data-ttu-id="d40ed-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="d40ed-130">xs:string</span></span>|<span data-ttu-id="d40ed-131">Nom de type de l'activité enfant planifiée.</span><span class="sxs-lookup"><span data-stu-id="d40ed-131">The type name of the scheduled child activity.</span></span>|  
|<span data-ttu-id="d40ed-132">ChildDisplayName</span><span class="sxs-lookup"><span data-stu-id="d40ed-132">ChildDisplayName</span></span>|<span data-ttu-id="d40ed-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="d40ed-133">xs:string</span></span>|<span data-ttu-id="d40ed-134">Nom complet de l'activité enfant planifiée.</span><span class="sxs-lookup"><span data-stu-id="d40ed-134">The display name of the scheduled child activity.</span></span>|  
|<span data-ttu-id="d40ed-135">ChildInstanceId</span><span class="sxs-lookup"><span data-stu-id="d40ed-135">ChildInstanceId</span></span>|<span data-ttu-id="d40ed-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="d40ed-136">xs:string</span></span>|<span data-ttu-id="d40ed-137">ID d'instance de l'activité enfant planifiée.</span><span class="sxs-lookup"><span data-stu-id="d40ed-137">The instance id of the scheduled child activity.</span></span>|  
|<span data-ttu-id="d40ed-138">AppDomain</span><span class="sxs-lookup"><span data-stu-id="d40ed-138">AppDomain</span></span>|<span data-ttu-id="d40ed-139">xs:string</span><span class="sxs-lookup"><span data-stu-id="d40ed-139">xs:string</span></span>|<span data-ttu-id="d40ed-140">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="d40ed-140">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
