---
title: 1020 - CreateBookmark
ms.date: 03/30/2017
ms.assetid: 4bee948d-816f-4803-85cc-3883b5e23d10
ms.openlocfilehash: 2a382a2f12f4800cd70286a553af253e2af64c9b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33510457"
---
# <a name="1020---createbookmark"></a><span data-ttu-id="7b0d2-102">1020 - CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="7b0d2-102">1020 - CreateBookmark</span></span>
## <a name="properties"></a><span data-ttu-id="7b0d2-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b0d2-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="7b0d2-104">ID</span><span class="sxs-lookup"><span data-stu-id="7b0d2-104">ID</span></span>|<span data-ttu-id="7b0d2-105">1020</span><span class="sxs-lookup"><span data-stu-id="7b0d2-105">1020</span></span>|  
|<span data-ttu-id="7b0d2-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="7b0d2-106">Keywords</span></span>|<span data-ttu-id="7b0d2-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="7b0d2-107">WFRuntime</span></span>|  
|<span data-ttu-id="7b0d2-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="7b0d2-108">Level</span></span>|<span data-ttu-id="7b0d2-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="7b0d2-109">Verbose</span></span>|  
|<span data-ttu-id="7b0d2-110">Canal</span><span class="sxs-lookup"><span data-stu-id="7b0d2-110">Channel</span></span>|<span data-ttu-id="7b0d2-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="7b0d2-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="7b0d2-112">Description</span><span class="sxs-lookup"><span data-stu-id="7b0d2-112">Description</span></span>  
 <span data-ttu-id="7b0d2-113">Indique qu'un signet a été créé pour une activité.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-113">Indicates a bookmark has been created for an activity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="7b0d2-114">Message</span><span class="sxs-lookup"><span data-stu-id="7b0d2-114">Message</span></span>  
 <span data-ttu-id="7b0d2-115">Un signet a été créé pour l’activité '%1', DisplayName : '%2', InstanceId : '%3'.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-115">A Bookmark has been created for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="7b0d2-116">BookmarkName : %4, BookmarkScope : %5.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-116">BookmarkName: %4, BookmarkScope: %5.</span></span>  
  
## <a name="details"></a><span data-ttu-id="7b0d2-117">Détails</span><span class="sxs-lookup"><span data-stu-id="7b0d2-117">Details</span></span>  
  
|<span data-ttu-id="7b0d2-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="7b0d2-118">Data Item Name</span></span>|<span data-ttu-id="7b0d2-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="7b0d2-119">Data Item Type</span></span>|<span data-ttu-id="7b0d2-120">Description</span><span class="sxs-lookup"><span data-stu-id="7b0d2-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="7b0d2-121">Activité</span><span class="sxs-lookup"><span data-stu-id="7b0d2-121">Activity</span></span>|<span data-ttu-id="7b0d2-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b0d2-122">xs:string</span></span>|<span data-ttu-id="7b0d2-123">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="7b0d2-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="7b0d2-124">DisplayName</span></span>|<span data-ttu-id="7b0d2-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b0d2-125">xs:string</span></span>|<span data-ttu-id="7b0d2-126">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="7b0d2-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="7b0d2-127">InstanceId</span></span>|<span data-ttu-id="7b0d2-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b0d2-128">xs:string</span></span>|<span data-ttu-id="7b0d2-129">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="7b0d2-130">BookmarkName</span><span class="sxs-lookup"><span data-stu-id="7b0d2-130">BookmarkName</span></span>|<span data-ttu-id="7b0d2-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b0d2-131">xs:string</span></span>|<span data-ttu-id="7b0d2-132">Nom du signet.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-132">The name of the bookmark.</span></span>|  
|<span data-ttu-id="7b0d2-133">BookmarkScope</span><span class="sxs-lookup"><span data-stu-id="7b0d2-133">BookmarkScope</span></span>|<span data-ttu-id="7b0d2-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b0d2-134">xs:string</span></span>|<span data-ttu-id="7b0d2-135">Portée du signet.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-135">The scope of the bookmark.</span></span>|  
|<span data-ttu-id="7b0d2-136">AppDomain</span><span class="sxs-lookup"><span data-stu-id="7b0d2-136">AppDomain</span></span>|<span data-ttu-id="7b0d2-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b0d2-137">xs:string</span></span>|<span data-ttu-id="7b0d2-138">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="7b0d2-138">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
