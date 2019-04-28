---
title: 1021 - ScheduleBookmarkWorkItem
ms.date: 03/30/2017
ms.assetid: 2e0da311-b219-4637-9460-90cdafcc4ecd
ms.openlocfilehash: abc026165568d05faef619da28c94f27f37eea27
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924421"
---
# <a name="1021---schedulebookmarkworkitem"></a><span data-ttu-id="78507-102">1021 - ScheduleBookmarkWorkItem</span><span class="sxs-lookup"><span data-stu-id="78507-102">1021 - ScheduleBookmarkWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="78507-103">Properties</span><span class="sxs-lookup"><span data-stu-id="78507-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="78507-104">Id</span><span class="sxs-lookup"><span data-stu-id="78507-104">ID</span></span>|<span data-ttu-id="78507-105">1021</span><span class="sxs-lookup"><span data-stu-id="78507-105">1021</span></span>|  
|<span data-ttu-id="78507-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="78507-106">Keywords</span></span>|<span data-ttu-id="78507-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="78507-107">WFRuntime</span></span>|  
|<span data-ttu-id="78507-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="78507-108">Level</span></span>|<span data-ttu-id="78507-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="78507-109">Verbose</span></span>|  
|<span data-ttu-id="78507-110">Canal</span><span class="sxs-lookup"><span data-stu-id="78507-110">Channel</span></span>|<span data-ttu-id="78507-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="78507-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="78507-112">Description</span><span class="sxs-lookup"><span data-stu-id="78507-112">Description</span></span>  
 <span data-ttu-id="78507-113">Indique qu'un BookmarkWorkItem a été planifié.</span><span class="sxs-lookup"><span data-stu-id="78507-113">Indicates a BookmarkWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="78507-114">Message</span><span class="sxs-lookup"><span data-stu-id="78507-114">Message</span></span>  
 <span data-ttu-id="78507-115">Qu’un BookmarkWorkItem a été planifié pour l’activité « %1 », DisplayName : « %2 », InstanceId : '%3'.</span><span class="sxs-lookup"><span data-stu-id="78507-115">A BookmarkWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="78507-116">BookmarkName : %4, BookmarkScope : %5.</span><span class="sxs-lookup"><span data-stu-id="78507-116">BookmarkName: %4, BookmarkScope: %5.</span></span>  
  
## <a name="details"></a><span data-ttu-id="78507-117">Détails</span><span class="sxs-lookup"><span data-stu-id="78507-117">Details</span></span>  
  
|<span data-ttu-id="78507-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="78507-118">Data Item Name</span></span>|<span data-ttu-id="78507-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="78507-119">Data Item Type</span></span>|<span data-ttu-id="78507-120">Description</span><span class="sxs-lookup"><span data-stu-id="78507-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="78507-121">Activité</span><span class="sxs-lookup"><span data-stu-id="78507-121">Activity</span></span>|<span data-ttu-id="78507-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="78507-122">xs:string</span></span>|<span data-ttu-id="78507-123">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="78507-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="78507-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="78507-124">DisplayName</span></span>|<span data-ttu-id="78507-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="78507-125">xs:string</span></span>|<span data-ttu-id="78507-126">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="78507-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="78507-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="78507-127">InstanceId</span></span>|<span data-ttu-id="78507-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="78507-128">xs:string</span></span>|<span data-ttu-id="78507-129">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="78507-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="78507-130">BookmarkName</span><span class="sxs-lookup"><span data-stu-id="78507-130">BookmarkName</span></span>|<span data-ttu-id="78507-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="78507-131">xs:string</span></span>|<span data-ttu-id="78507-132">Nom du signet.</span><span class="sxs-lookup"><span data-stu-id="78507-132">The name of the bookmark.</span></span>|  
|<span data-ttu-id="78507-133">BookmarkScope</span><span class="sxs-lookup"><span data-stu-id="78507-133">BookmarkScope</span></span>|<span data-ttu-id="78507-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="78507-134">xs:string</span></span>|<span data-ttu-id="78507-135">Portée du signet.</span><span class="sxs-lookup"><span data-stu-id="78507-135">The scope of the bookmark.</span></span>|  
|<span data-ttu-id="78507-136">AppDomain</span><span class="sxs-lookup"><span data-stu-id="78507-136">AppDomain</span></span>|<span data-ttu-id="78507-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="78507-137">xs:string</span></span>|<span data-ttu-id="78507-138">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="78507-138">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
