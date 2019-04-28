---
title: 1023 - CompleteBookmarkWorkItem
ms.date: 03/30/2017
ms.assetid: fc5dac57-b3eb-4826-b505-c6d269e4774d
ms.openlocfilehash: 8677f25057486247e64879298755fe972bd373d3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62008848"
---
# <a name="1023---completebookmarkworkitem"></a><span data-ttu-id="219d4-102">1023 - CompleteBookmarkWorkItem</span><span class="sxs-lookup"><span data-stu-id="219d4-102">1023 - CompleteBookmarkWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="219d4-103">Properties</span><span class="sxs-lookup"><span data-stu-id="219d4-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="219d4-104">Id</span><span class="sxs-lookup"><span data-stu-id="219d4-104">ID</span></span>|<span data-ttu-id="219d4-105">1023</span><span class="sxs-lookup"><span data-stu-id="219d4-105">1023</span></span>|  
|<span data-ttu-id="219d4-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="219d4-106">Keywords</span></span>|<span data-ttu-id="219d4-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="219d4-107">WFRuntime</span></span>|  
|<span data-ttu-id="219d4-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="219d4-108">Level</span></span>|<span data-ttu-id="219d4-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="219d4-109">Verbose</span></span>|  
|<span data-ttu-id="219d4-110">Canal</span><span class="sxs-lookup"><span data-stu-id="219d4-110">Channel</span></span>|<span data-ttu-id="219d4-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="219d4-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="219d4-112">Description</span><span class="sxs-lookup"><span data-stu-id="219d4-112">Description</span></span>  
 <span data-ttu-id="219d4-113">Indique qu'un BookmarkWorkItem est terminé.</span><span class="sxs-lookup"><span data-stu-id="219d4-113">Indicates a BookmarkWorkItem has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="219d4-114">Message</span><span class="sxs-lookup"><span data-stu-id="219d4-114">Message</span></span>  
 <span data-ttu-id="219d4-115">Un BookmarkWorkItem est achevé pour l'activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="219d4-115">A BookmarkWorkItem has completed for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span> <span data-ttu-id="219d4-116">BookmarkName : %4, BookmarkScope : %5.</span><span class="sxs-lookup"><span data-stu-id="219d4-116">BookmarkName: %4, BookmarkScope: %5.</span></span>  
  
## <a name="details"></a><span data-ttu-id="219d4-117">Détails</span><span class="sxs-lookup"><span data-stu-id="219d4-117">Details</span></span>  
  
|<span data-ttu-id="219d4-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="219d4-118">Data Item Name</span></span>|<span data-ttu-id="219d4-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="219d4-119">Data Item Type</span></span>|<span data-ttu-id="219d4-120">Description</span><span class="sxs-lookup"><span data-stu-id="219d4-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="219d4-121">Activité</span><span class="sxs-lookup"><span data-stu-id="219d4-121">Activity</span></span>|<span data-ttu-id="219d4-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="219d4-122">xs:string</span></span>|<span data-ttu-id="219d4-123">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="219d4-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="219d4-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="219d4-124">DisplayName</span></span>|<span data-ttu-id="219d4-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="219d4-125">xs:string</span></span>|<span data-ttu-id="219d4-126">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="219d4-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="219d4-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="219d4-127">InstanceId</span></span>|<span data-ttu-id="219d4-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="219d4-128">xs:string</span></span>|<span data-ttu-id="219d4-129">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="219d4-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="219d4-130">BookmarkName</span><span class="sxs-lookup"><span data-stu-id="219d4-130">BookmarkName</span></span>|<span data-ttu-id="219d4-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="219d4-131">xs:string</span></span>|<span data-ttu-id="219d4-132">Nom du signet.</span><span class="sxs-lookup"><span data-stu-id="219d4-132">The name of the bookmark.</span></span>|  
|<span data-ttu-id="219d4-133">BookmarkScope</span><span class="sxs-lookup"><span data-stu-id="219d4-133">BookmarkScope</span></span>|<span data-ttu-id="219d4-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="219d4-134">xs:string</span></span>|<span data-ttu-id="219d4-135">Portée du signet.</span><span class="sxs-lookup"><span data-stu-id="219d4-135">The scope of the bookmark.</span></span>|  
|<span data-ttu-id="219d4-136">AppDomain</span><span class="sxs-lookup"><span data-stu-id="219d4-136">AppDomain</span></span>|<span data-ttu-id="219d4-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="219d4-137">xs:string</span></span>|<span data-ttu-id="219d4-138">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="219d4-138">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
