---
title: 1022 - StartBookmarkWorkItem
ms.date: 03/30/2017
ms.assetid: 4415fbdb-0329-4019-803f-aea66e75f3da
ms.openlocfilehash: 93d906b32b51effaa709da6763f535708cd6f821
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924720"
---
# <a name="1022---startbookmarkworkitem"></a><span data-ttu-id="3bf84-102">1022 - StartBookmarkWorkItem</span><span class="sxs-lookup"><span data-stu-id="3bf84-102">1022 - StartBookmarkWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="3bf84-103">Properties</span><span class="sxs-lookup"><span data-stu-id="3bf84-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="3bf84-104">Id</span><span class="sxs-lookup"><span data-stu-id="3bf84-104">ID</span></span>|<span data-ttu-id="3bf84-105">1022</span><span class="sxs-lookup"><span data-stu-id="3bf84-105">1022</span></span>|  
|<span data-ttu-id="3bf84-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="3bf84-106">Keywords</span></span>|<span data-ttu-id="3bf84-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="3bf84-107">WFRuntime</span></span>|  
|<span data-ttu-id="3bf84-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="3bf84-108">Level</span></span>|<span data-ttu-id="3bf84-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="3bf84-109">Verbose</span></span>|  
|<span data-ttu-id="3bf84-110">Canal</span><span class="sxs-lookup"><span data-stu-id="3bf84-110">Channel</span></span>|<span data-ttu-id="3bf84-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="3bf84-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="3bf84-112">Description</span><span class="sxs-lookup"><span data-stu-id="3bf84-112">Description</span></span>  
 <span data-ttu-id="3bf84-113">Indique qu'un BookmarkWorkItem démarre l'exécution.</span><span class="sxs-lookup"><span data-stu-id="3bf84-113">Indicates a BookmarkWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="3bf84-114">Message</span><span class="sxs-lookup"><span data-stu-id="3bf84-114">Message</span></span>  
 <span data-ttu-id="3bf84-115">Démarrage de l’exécution d’un BookmarkWorkItem pour l’activité « %1 », DisplayName : « %2 », InstanceId : '%3'.</span><span class="sxs-lookup"><span data-stu-id="3bf84-115">Starting execution of a BookmarkWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="3bf84-116">BookmarkName : %4, BookmarkScope : %5.</span><span class="sxs-lookup"><span data-stu-id="3bf84-116">BookmarkName: %4, BookmarkScope: %5.</span></span>  
  
## <a name="details"></a><span data-ttu-id="3bf84-117">Détails</span><span class="sxs-lookup"><span data-stu-id="3bf84-117">Details</span></span>  
  
|<span data-ttu-id="3bf84-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="3bf84-118">Data Item Name</span></span>|<span data-ttu-id="3bf84-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="3bf84-119">Data Item Type</span></span>|<span data-ttu-id="3bf84-120">Description</span><span class="sxs-lookup"><span data-stu-id="3bf84-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="3bf84-121">Activité</span><span class="sxs-lookup"><span data-stu-id="3bf84-121">Activity</span></span>|<span data-ttu-id="3bf84-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="3bf84-122">xs:string</span></span>|<span data-ttu-id="3bf84-123">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="3bf84-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="3bf84-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="3bf84-124">DisplayName</span></span>|<span data-ttu-id="3bf84-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="3bf84-125">xs:string</span></span>|<span data-ttu-id="3bf84-126">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="3bf84-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="3bf84-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="3bf84-127">InstanceId</span></span>|<span data-ttu-id="3bf84-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="3bf84-128">xs:string</span></span>|<span data-ttu-id="3bf84-129">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="3bf84-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="3bf84-130">BookmarkName</span><span class="sxs-lookup"><span data-stu-id="3bf84-130">BookmarkName</span></span>|<span data-ttu-id="3bf84-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="3bf84-131">xs:string</span></span>|<span data-ttu-id="3bf84-132">Nom du signet.</span><span class="sxs-lookup"><span data-stu-id="3bf84-132">The name of the bookmark.</span></span>|  
|<span data-ttu-id="3bf84-133">BookmarkScope</span><span class="sxs-lookup"><span data-stu-id="3bf84-133">BookmarkScope</span></span>|<span data-ttu-id="3bf84-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="3bf84-134">xs:string</span></span>|<span data-ttu-id="3bf84-135">Portée du signet.</span><span class="sxs-lookup"><span data-stu-id="3bf84-135">The scope of the bookmark.</span></span>|  
|<span data-ttu-id="3bf84-136">AppDomain</span><span class="sxs-lookup"><span data-stu-id="3bf84-136">AppDomain</span></span>|<span data-ttu-id="3bf84-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="3bf84-137">xs:string</span></span>|<span data-ttu-id="3bf84-138">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="3bf84-138">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
