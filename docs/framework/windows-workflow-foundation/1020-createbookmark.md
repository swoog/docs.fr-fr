---
title: 1020 - CreateBookmark
ms.date: 03/30/2017
ms.assetid: 4bee948d-816f-4803-85cc-3883b5e23d10
ms.openlocfilehash: 2a382a2f12f4800cd70286a553af253e2af64c9b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924746"
---
# <a name="1020---createbookmark"></a><span data-ttu-id="98da0-102">1020 - CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="98da0-102">1020 - CreateBookmark</span></span>
## <a name="properties"></a><span data-ttu-id="98da0-103">Properties</span><span class="sxs-lookup"><span data-stu-id="98da0-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="98da0-104">Id</span><span class="sxs-lookup"><span data-stu-id="98da0-104">ID</span></span>|<span data-ttu-id="98da0-105">1020</span><span class="sxs-lookup"><span data-stu-id="98da0-105">1020</span></span>|  
|<span data-ttu-id="98da0-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="98da0-106">Keywords</span></span>|<span data-ttu-id="98da0-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="98da0-107">WFRuntime</span></span>|  
|<span data-ttu-id="98da0-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="98da0-108">Level</span></span>|<span data-ttu-id="98da0-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="98da0-109">Verbose</span></span>|  
|<span data-ttu-id="98da0-110">Canal</span><span class="sxs-lookup"><span data-stu-id="98da0-110">Channel</span></span>|<span data-ttu-id="98da0-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="98da0-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="98da0-112">Description</span><span class="sxs-lookup"><span data-stu-id="98da0-112">Description</span></span>  
 <span data-ttu-id="98da0-113">Indique qu'un signet a été créé pour une activité.</span><span class="sxs-lookup"><span data-stu-id="98da0-113">Indicates a bookmark has been created for an activity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="98da0-114">Message</span><span class="sxs-lookup"><span data-stu-id="98da0-114">Message</span></span>  
 <span data-ttu-id="98da0-115">Un signet a été créé pour l’activité « %1 », DisplayName : « %2 », InstanceId : '%3'.</span><span class="sxs-lookup"><span data-stu-id="98da0-115">A Bookmark has been created for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="98da0-116">BookmarkName : %4, BookmarkScope : %5.</span><span class="sxs-lookup"><span data-stu-id="98da0-116">BookmarkName: %4, BookmarkScope: %5.</span></span>  
  
## <a name="details"></a><span data-ttu-id="98da0-117">Détails</span><span class="sxs-lookup"><span data-stu-id="98da0-117">Details</span></span>  
  
|<span data-ttu-id="98da0-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="98da0-118">Data Item Name</span></span>|<span data-ttu-id="98da0-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="98da0-119">Data Item Type</span></span>|<span data-ttu-id="98da0-120">Description</span><span class="sxs-lookup"><span data-stu-id="98da0-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="98da0-121">Activité</span><span class="sxs-lookup"><span data-stu-id="98da0-121">Activity</span></span>|<span data-ttu-id="98da0-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="98da0-122">xs:string</span></span>|<span data-ttu-id="98da0-123">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="98da0-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="98da0-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="98da0-124">DisplayName</span></span>|<span data-ttu-id="98da0-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="98da0-125">xs:string</span></span>|<span data-ttu-id="98da0-126">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="98da0-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="98da0-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="98da0-127">InstanceId</span></span>|<span data-ttu-id="98da0-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="98da0-128">xs:string</span></span>|<span data-ttu-id="98da0-129">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="98da0-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="98da0-130">BookmarkName</span><span class="sxs-lookup"><span data-stu-id="98da0-130">BookmarkName</span></span>|<span data-ttu-id="98da0-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="98da0-131">xs:string</span></span>|<span data-ttu-id="98da0-132">Nom du signet.</span><span class="sxs-lookup"><span data-stu-id="98da0-132">The name of the bookmark.</span></span>|  
|<span data-ttu-id="98da0-133">BookmarkScope</span><span class="sxs-lookup"><span data-stu-id="98da0-133">BookmarkScope</span></span>|<span data-ttu-id="98da0-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="98da0-134">xs:string</span></span>|<span data-ttu-id="98da0-135">Portée du signet.</span><span class="sxs-lookup"><span data-stu-id="98da0-135">The scope of the bookmark.</span></span>|  
|<span data-ttu-id="98da0-136">AppDomain</span><span class="sxs-lookup"><span data-stu-id="98da0-136">AppDomain</span></span>|<span data-ttu-id="98da0-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="98da0-137">xs:string</span></span>|<span data-ttu-id="98da0-138">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="98da0-138">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
