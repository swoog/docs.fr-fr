---
title: 1030 - StartFaultWorkItem
ms.date: 03/30/2017
ms.assetid: e1601fb9-0bc6-4dbe-816f-f24914063d34
ms.openlocfilehash: 3848d644e77041a62a52eb2eae5eeef286dfe334
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924317"
---
# <a name="1030---startfaultworkitem"></a><span data-ttu-id="06426-102">1030 - StartFaultWorkItem</span><span class="sxs-lookup"><span data-stu-id="06426-102">1030 - StartFaultWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="06426-103">Properties</span><span class="sxs-lookup"><span data-stu-id="06426-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="06426-104">Id</span><span class="sxs-lookup"><span data-stu-id="06426-104">ID</span></span>|<span data-ttu-id="06426-105">1030</span><span class="sxs-lookup"><span data-stu-id="06426-105">1030</span></span>|  
|<span data-ttu-id="06426-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="06426-106">Keywords</span></span>|<span data-ttu-id="06426-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="06426-107">WFRuntime</span></span>|  
|<span data-ttu-id="06426-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="06426-108">Level</span></span>|<span data-ttu-id="06426-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="06426-109">Verbose</span></span>|  
|<span data-ttu-id="06426-110">Canal</span><span class="sxs-lookup"><span data-stu-id="06426-110">Channel</span></span>|<span data-ttu-id="06426-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="06426-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="06426-112">Description</span><span class="sxs-lookup"><span data-stu-id="06426-112">Description</span></span>  
 <span data-ttu-id="06426-113">Indique qu'un FaultWorkItem démarre l'exécution.</span><span class="sxs-lookup"><span data-stu-id="06426-113">Indicates a FaultWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="06426-114">Message</span><span class="sxs-lookup"><span data-stu-id="06426-114">Message</span></span>  
 <span data-ttu-id="06426-115">Démarrage de l’exécution d’un FaultWorkItem pour l’activité « %1 », DisplayName : « %2 », InstanceId : '%3'.</span><span class="sxs-lookup"><span data-stu-id="06426-115">Starting execution of a FaultWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="06426-116">L'exception a été propagée à partir de l'activité « %4 », DisplayName : « %5 », InstanceId : « %6 ».</span><span class="sxs-lookup"><span data-stu-id="06426-116">The exception was propagated from Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="06426-117">Détails</span><span class="sxs-lookup"><span data-stu-id="06426-117">Details</span></span>  
  
|<span data-ttu-id="06426-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="06426-118">Data Item Name</span></span>|<span data-ttu-id="06426-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="06426-119">Data Item Type</span></span>|<span data-ttu-id="06426-120">Description</span><span class="sxs-lookup"><span data-stu-id="06426-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="06426-121">FaultActivity</span><span class="sxs-lookup"><span data-stu-id="06426-121">FaultActivity</span></span>|<span data-ttu-id="06426-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="06426-122">xs:string</span></span>|<span data-ttu-id="06426-123">Nom de type de l'activité d'erreur.</span><span class="sxs-lookup"><span data-stu-id="06426-123">The type name of the fault activity.</span></span>|  
|<span data-ttu-id="06426-124">FaultActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="06426-124">FaultActivityDisplayName</span></span>|<span data-ttu-id="06426-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="06426-125">xs:string</span></span>|<span data-ttu-id="06426-126">Nom complet de l'activité d'erreur.</span><span class="sxs-lookup"><span data-stu-id="06426-126">The display name of the fault activity.</span></span>|  
|<span data-ttu-id="06426-127">FaultActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="06426-127">FaultActivityInstanceId</span></span>|<span data-ttu-id="06426-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="06426-128">xs:string</span></span>|<span data-ttu-id="06426-129">ID d'instance de l'activité d'erreur.</span><span class="sxs-lookup"><span data-stu-id="06426-129">The instance id of the fault activity.</span></span>|  
|<span data-ttu-id="06426-130">ExceptionActivity</span><span class="sxs-lookup"><span data-stu-id="06426-130">ExceptionActivity</span></span>|<span data-ttu-id="06426-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="06426-131">xs:string</span></span>|<span data-ttu-id="06426-132">Nom de type de l'activité qui a levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="06426-132">The type name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="06426-133">ExceptionActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="06426-133">ExceptionActivityDisplayName</span></span>|<span data-ttu-id="06426-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="06426-134">xs:string</span></span>|<span data-ttu-id="06426-135">Nom complet de l'activité qui a levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="06426-135">The display name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="06426-136">ExceptionActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="06426-136">ExceptionActivityInstanceId</span></span>|<span data-ttu-id="06426-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="06426-137">xs:string</span></span>|<span data-ttu-id="06426-138">ID d'instance de l'activité ayant levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="06426-138">The instance id of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="06426-139">Exception</span><span class="sxs-lookup"><span data-stu-id="06426-139">Exception</span></span>|<span data-ttu-id="06426-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="06426-140">xs:string</span></span>|<span data-ttu-id="06426-141">Détails de l'exception</span><span class="sxs-lookup"><span data-stu-id="06426-141">The exception details for the exception</span></span>|  
|<span data-ttu-id="06426-142">AppDomain</span><span class="sxs-lookup"><span data-stu-id="06426-142">AppDomain</span></span>|<span data-ttu-id="06426-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="06426-143">xs:string</span></span>|<span data-ttu-id="06426-144">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="06426-144">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
