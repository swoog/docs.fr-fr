---
title: 1029 - ScheduleFaultWorkItem
ms.date: 03/30/2017
ms.assetid: 3a56b29e-f740-459d-8576-d81e58bf5a03
ms.openlocfilehash: f5beab91f7dd39a3f8ed3b76d6c0a1ddd9bd77c3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924356"
---
# <a name="1029---schedulefaultworkitem"></a><span data-ttu-id="fd9c4-102">1029 - ScheduleFaultWorkItem</span><span class="sxs-lookup"><span data-stu-id="fd9c4-102">1029 - ScheduleFaultWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="fd9c4-103">Properties</span><span class="sxs-lookup"><span data-stu-id="fd9c4-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="fd9c4-104">Id</span><span class="sxs-lookup"><span data-stu-id="fd9c4-104">ID</span></span>|<span data-ttu-id="fd9c4-105">1029</span><span class="sxs-lookup"><span data-stu-id="fd9c4-105">1029</span></span>|  
|<span data-ttu-id="fd9c4-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd9c4-106">Keywords</span></span>|<span data-ttu-id="fd9c4-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="fd9c4-107">WFRuntime</span></span>|  
|<span data-ttu-id="fd9c4-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="fd9c4-108">Level</span></span>|<span data-ttu-id="fd9c4-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="fd9c4-109">Verbose</span></span>|  
|<span data-ttu-id="fd9c4-110">Canal</span><span class="sxs-lookup"><span data-stu-id="fd9c4-110">Channel</span></span>|<span data-ttu-id="fd9c4-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="fd9c4-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="fd9c4-112">Description</span><span class="sxs-lookup"><span data-stu-id="fd9c4-112">Description</span></span>  
 <span data-ttu-id="fd9c4-113">Indique qu'un FaultWorkItem a été planifié.</span><span class="sxs-lookup"><span data-stu-id="fd9c4-113">Indicates a FaultWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="fd9c4-114">Message</span><span class="sxs-lookup"><span data-stu-id="fd9c4-114">Message</span></span>  
 <span data-ttu-id="fd9c4-115">Qu’un FaultWorkItem a été planifié pour l’activité « %1 », DisplayName : « %2 », InstanceId : '%3'.</span><span class="sxs-lookup"><span data-stu-id="fd9c4-115">A FaultWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="fd9c4-116">L'exception a été propagée à partir de l'activité « %4 », DisplayName : « %5 », InstanceId : « %6 ».</span><span class="sxs-lookup"><span data-stu-id="fd9c4-116">The exception was propagated from Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="fd9c4-117">Détails</span><span class="sxs-lookup"><span data-stu-id="fd9c4-117">Details</span></span>  
  
|<span data-ttu-id="fd9c4-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="fd9c4-118">Data Item Name</span></span>|<span data-ttu-id="fd9c4-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="fd9c4-119">Data Item Type</span></span>|<span data-ttu-id="fd9c4-120">Description</span><span class="sxs-lookup"><span data-stu-id="fd9c4-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="fd9c4-121">FaultActivity</span><span class="sxs-lookup"><span data-stu-id="fd9c4-121">FaultActivity</span></span>|<span data-ttu-id="fd9c4-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="fd9c4-122">xs:string</span></span>|<span data-ttu-id="fd9c4-123">Nom de type de l'activité d'erreur.</span><span class="sxs-lookup"><span data-stu-id="fd9c4-123">The type name of the fault activity.</span></span>|  
|<span data-ttu-id="fd9c4-124">FaultActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="fd9c4-124">FaultActivityDisplayName</span></span>|<span data-ttu-id="fd9c4-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="fd9c4-125">xs:string</span></span>|<span data-ttu-id="fd9c4-126">Nom complet de l'activité d'erreur.</span><span class="sxs-lookup"><span data-stu-id="fd9c4-126">The display name of the fault activity.</span></span>|  
|<span data-ttu-id="fd9c4-127">FaultActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="fd9c4-127">FaultActivityInstanceId</span></span>|<span data-ttu-id="fd9c4-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="fd9c4-128">xs:string</span></span>|<span data-ttu-id="fd9c4-129">ID d'instance de l'activité d'erreur.</span><span class="sxs-lookup"><span data-stu-id="fd9c4-129">The instance id of the fault activity.</span></span>|  
|<span data-ttu-id="fd9c4-130">ExceptionActivity</span><span class="sxs-lookup"><span data-stu-id="fd9c4-130">ExceptionActivity</span></span>|<span data-ttu-id="fd9c4-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="fd9c4-131">xs:string</span></span>|<span data-ttu-id="fd9c4-132">Nom de type de l'activité qui a levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="fd9c4-132">The type name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="fd9c4-133">ExceptionActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="fd9c4-133">ExceptionActivityDisplayName</span></span>|<span data-ttu-id="fd9c4-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="fd9c4-134">xs:string</span></span>|<span data-ttu-id="fd9c4-135">Nom complet de l'activité qui a levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="fd9c4-135">The display name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="fd9c4-136">ExceptionActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="fd9c4-136">ExceptionActivityInstanceId</span></span>|<span data-ttu-id="fd9c4-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="fd9c4-137">xs:string</span></span>|<span data-ttu-id="fd9c4-138">ID d'instance de l'activité ayant levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="fd9c4-138">The instance id of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="fd9c4-139">Exception</span><span class="sxs-lookup"><span data-stu-id="fd9c4-139">Exception</span></span>|<span data-ttu-id="fd9c4-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="fd9c4-140">xs:string</span></span>|<span data-ttu-id="fd9c4-141">Détails de l'exception</span><span class="sxs-lookup"><span data-stu-id="fd9c4-141">The exception details for the exception</span></span>|  
|<span data-ttu-id="fd9c4-142">AppDomain</span><span class="sxs-lookup"><span data-stu-id="fd9c4-142">AppDomain</span></span>|<span data-ttu-id="fd9c4-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="fd9c4-143">xs:string</span></span>|<span data-ttu-id="fd9c4-144">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="fd9c4-144">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
