---
title: 1009 - ActivityScheduled
ms.date: 03/30/2017
ms.assetid: 307e38b6-d47e-47a4-9708-e74d8314b1a1
ms.openlocfilehash: 0e3ea53a7b0509fcb8b73b61193742d615ac7e91
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33509970"
---
# <a name="1009---activityscheduled"></a><span data-ttu-id="78750-102">1009 - ActivityScheduled</span><span class="sxs-lookup"><span data-stu-id="78750-102">1009 - ActivityScheduled</span></span>
## <a name="properties"></a><span data-ttu-id="78750-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="78750-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="78750-104">ID</span><span class="sxs-lookup"><span data-stu-id="78750-104">ID</span></span>|<span data-ttu-id="78750-105">1009</span><span class="sxs-lookup"><span data-stu-id="78750-105">1009</span></span>|  
|<span data-ttu-id="78750-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="78750-106">Keywords</span></span>|<span data-ttu-id="78750-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="78750-107">WFRuntime</span></span>|  
|<span data-ttu-id="78750-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="78750-108">Level</span></span>|<span data-ttu-id="78750-109">Information</span><span class="sxs-lookup"><span data-stu-id="78750-109">Information</span></span>|  
|<span data-ttu-id="78750-110">Canal</span><span class="sxs-lookup"><span data-stu-id="78750-110">Channel</span></span>|<span data-ttu-id="78750-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="78750-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="78750-112">Description</span><span class="sxs-lookup"><span data-stu-id="78750-112">Description</span></span>  
 <span data-ttu-id="78750-113">Indique qu'une activité est planifiée en vue de son exécution.</span><span class="sxs-lookup"><span data-stu-id="78750-113">Indicates an activity is being scheduled for execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="78750-114">Message</span><span class="sxs-lookup"><span data-stu-id="78750-114">Message</span></span>  
 <span data-ttu-id="78750-115">L'activité parent « %1 », DisplayName : « %2 », InstanceId : « %3 » a planifié l'activité enfant « %4 », DisplayName : « %5 », InstanceId : « %6 ».</span><span class="sxs-lookup"><span data-stu-id="78750-115">Parent Activity '%1', DisplayName: '%2', InstanceId: '%3' scheduled child Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="78750-116">Détails</span><span class="sxs-lookup"><span data-stu-id="78750-116">Details</span></span>  
  
|<span data-ttu-id="78750-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="78750-117">Data Item Name</span></span>|<span data-ttu-id="78750-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="78750-118">Data Item Type</span></span>|<span data-ttu-id="78750-119">Description</span><span class="sxs-lookup"><span data-stu-id="78750-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="78750-120">ParentActivity</span><span class="sxs-lookup"><span data-stu-id="78750-120">ParentActivity</span></span>|<span data-ttu-id="78750-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="78750-121">xs:string</span></span>|<span data-ttu-id="78750-122">Nom de type de l'activité parente.</span><span class="sxs-lookup"><span data-stu-id="78750-122">The type name of the parent activity.</span></span>|  
|<span data-ttu-id="78750-123">ParentDisplayName</span><span class="sxs-lookup"><span data-stu-id="78750-123">ParentDisplayName</span></span>|<span data-ttu-id="78750-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="78750-124">xs:string</span></span>|<span data-ttu-id="78750-125">Nom complet de l'activité parente.</span><span class="sxs-lookup"><span data-stu-id="78750-125">The display name of the parent activity.</span></span>|  
|<span data-ttu-id="78750-126">ParentInstanceId</span><span class="sxs-lookup"><span data-stu-id="78750-126">ParentInstanceId</span></span>|<span data-ttu-id="78750-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="78750-127">xs:string</span></span>|<span data-ttu-id="78750-128">ID d'instance de l'activité parente.</span><span class="sxs-lookup"><span data-stu-id="78750-128">The instance id of the parent activity.</span></span>|  
|<span data-ttu-id="78750-129">ChildActivity</span><span class="sxs-lookup"><span data-stu-id="78750-129">ChildActivity</span></span>|<span data-ttu-id="78750-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="78750-130">xs:string</span></span>|<span data-ttu-id="78750-131">Nom de type de l'activité enfant planifiée.</span><span class="sxs-lookup"><span data-stu-id="78750-131">The type name of the scheduled child activity.</span></span>|  
|<span data-ttu-id="78750-132">ChildDisplayName</span><span class="sxs-lookup"><span data-stu-id="78750-132">ChildDisplayName</span></span>|<span data-ttu-id="78750-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="78750-133">xs:string</span></span>|<span data-ttu-id="78750-134">Nom complet de l'activité enfant planifiée.</span><span class="sxs-lookup"><span data-stu-id="78750-134">The display name of the scheduled child activity.</span></span>|  
|<span data-ttu-id="78750-135">ChildInstanceId</span><span class="sxs-lookup"><span data-stu-id="78750-135">ChildInstanceId</span></span>|<span data-ttu-id="78750-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="78750-136">xs:string</span></span>|<span data-ttu-id="78750-137">ID d'instance de l'activité enfant planifiée.</span><span class="sxs-lookup"><span data-stu-id="78750-137">The instance id of the scheduled child activity.</span></span>|  
|<span data-ttu-id="78750-138">AppDomain</span><span class="sxs-lookup"><span data-stu-id="78750-138">AppDomain</span></span>|<span data-ttu-id="78750-139">xs:string</span><span class="sxs-lookup"><span data-stu-id="78750-139">xs:string</span></span>|<span data-ttu-id="78750-140">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="78750-140">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
