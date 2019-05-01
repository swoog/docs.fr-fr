---
title: 1015 - StartCompletionWorkItem
ms.date: 03/30/2017
ms.assetid: 96fd1d4e-c5d0-46ad-8a71-4b4b49ac7262
ms.openlocfilehash: 6a2d4c866ec7d43e8ae40b5616a97c3b7adf1843
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62032264"
---
# <a name="1015---startcompletionworkitem"></a><span data-ttu-id="69f9d-102">1015 - StartCompletionWorkItem</span><span class="sxs-lookup"><span data-stu-id="69f9d-102">1015 - StartCompletionWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="69f9d-103">Properties</span><span class="sxs-lookup"><span data-stu-id="69f9d-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="69f9d-104">Id</span><span class="sxs-lookup"><span data-stu-id="69f9d-104">ID</span></span>|<span data-ttu-id="69f9d-105">1015</span><span class="sxs-lookup"><span data-stu-id="69f9d-105">1015</span></span>|  
|<span data-ttu-id="69f9d-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="69f9d-106">Keywords</span></span>|<span data-ttu-id="69f9d-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="69f9d-107">WFRuntime</span></span>|  
|<span data-ttu-id="69f9d-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="69f9d-108">Level</span></span>|<span data-ttu-id="69f9d-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="69f9d-109">Verbose</span></span>|  
|<span data-ttu-id="69f9d-110">Canal</span><span class="sxs-lookup"><span data-stu-id="69f9d-110">Channel</span></span>|<span data-ttu-id="69f9d-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="69f9d-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="69f9d-112">Description</span><span class="sxs-lookup"><span data-stu-id="69f9d-112">Description</span></span>  
 <span data-ttu-id="69f9d-113">Indique qu'un CompletionWorkItem démarre l'exécution.</span><span class="sxs-lookup"><span data-stu-id="69f9d-113">Indicates a CompletionWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="69f9d-114">Message</span><span class="sxs-lookup"><span data-stu-id="69f9d-114">Message</span></span>  
 <span data-ttu-id="69f9d-115">Début de l'exécution d'un CompletionWorkItem pour l'activité parente « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="69f9d-115">Starting execution of a CompletionWorkItem for parent Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span> <span data-ttu-id="69f9d-116">Activité terminée « %4 », DisplayName : « %5 », InstanceId : « %6 ».</span><span class="sxs-lookup"><span data-stu-id="69f9d-116">Completed Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="69f9d-117">Détails</span><span class="sxs-lookup"><span data-stu-id="69f9d-117">Details</span></span>  
  
|<span data-ttu-id="69f9d-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="69f9d-118">Data Item Name</span></span>|<span data-ttu-id="69f9d-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="69f9d-119">Data Item Type</span></span>|<span data-ttu-id="69f9d-120">Description</span><span class="sxs-lookup"><span data-stu-id="69f9d-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="69f9d-121">ParentActivity</span><span class="sxs-lookup"><span data-stu-id="69f9d-121">ParentActivity</span></span>|<span data-ttu-id="69f9d-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="69f9d-122">xs:string</span></span>|<span data-ttu-id="69f9d-123">Nom de type de l'activité parente.</span><span class="sxs-lookup"><span data-stu-id="69f9d-123">The type name of the parent activity.</span></span>|  
|<span data-ttu-id="69f9d-124">ParentDisplayName</span><span class="sxs-lookup"><span data-stu-id="69f9d-124">ParentDisplayName</span></span>|<span data-ttu-id="69f9d-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="69f9d-125">xs:string</span></span>|<span data-ttu-id="69f9d-126">Nom complet de l'activité parente.</span><span class="sxs-lookup"><span data-stu-id="69f9d-126">The display name of the parent activity.</span></span>|  
|<span data-ttu-id="69f9d-127">ParentInstanceId</span><span class="sxs-lookup"><span data-stu-id="69f9d-127">ParentInstanceId</span></span>|<span data-ttu-id="69f9d-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="69f9d-128">xs:string</span></span>|<span data-ttu-id="69f9d-129">ID d'instance de l'activité parente.</span><span class="sxs-lookup"><span data-stu-id="69f9d-129">The instance id of the parent activity.</span></span>|  
|<span data-ttu-id="69f9d-130">CompletedActivity</span><span class="sxs-lookup"><span data-stu-id="69f9d-130">CompletedActivity</span></span>|<span data-ttu-id="69f9d-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="69f9d-131">xs:string</span></span>|<span data-ttu-id="69f9d-132">Nom de type de l'activité achevée.</span><span class="sxs-lookup"><span data-stu-id="69f9d-132">The type name of the completed activity.</span></span>|  
|<span data-ttu-id="69f9d-133">CompletedActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="69f9d-133">CompletedActivityDisplayName</span></span>|<span data-ttu-id="69f9d-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="69f9d-134">xs:string</span></span>|<span data-ttu-id="69f9d-135">Nom complet de l'activité achevée.</span><span class="sxs-lookup"><span data-stu-id="69f9d-135">The display name of the completed activity.</span></span>|  
|<span data-ttu-id="69f9d-136">CompletedActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="69f9d-136">CompletedActivityInstanceId</span></span>|<span data-ttu-id="69f9d-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="69f9d-137">xs:string</span></span>|<span data-ttu-id="69f9d-138">ID d'instance de l'activité achevée.</span><span class="sxs-lookup"><span data-stu-id="69f9d-138">The instance id of the completed activity.</span></span>|  
|<span data-ttu-id="69f9d-139">AppDomain</span><span class="sxs-lookup"><span data-stu-id="69f9d-139">AppDomain</span></span>|<span data-ttu-id="69f9d-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="69f9d-140">xs:string</span></span>|<span data-ttu-id="69f9d-141">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="69f9d-141">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
