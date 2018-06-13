---
title: 1030 - StartFaultWorkItem
ms.date: 03/30/2017
ms.assetid: e1601fb9-0bc6-4dbe-816f-f24914063d34
ms.openlocfilehash: 3848d644e77041a62a52eb2eae5eeef286dfe334
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33509678"
---
# <a name="1030---startfaultworkitem"></a><span data-ttu-id="578e0-102">1030 - StartFaultWorkItem</span><span class="sxs-lookup"><span data-stu-id="578e0-102">1030 - StartFaultWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="578e0-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="578e0-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="578e0-104">ID</span><span class="sxs-lookup"><span data-stu-id="578e0-104">ID</span></span>|<span data-ttu-id="578e0-105">1030</span><span class="sxs-lookup"><span data-stu-id="578e0-105">1030</span></span>|  
|<span data-ttu-id="578e0-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="578e0-106">Keywords</span></span>|<span data-ttu-id="578e0-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="578e0-107">WFRuntime</span></span>|  
|<span data-ttu-id="578e0-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="578e0-108">Level</span></span>|<span data-ttu-id="578e0-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="578e0-109">Verbose</span></span>|  
|<span data-ttu-id="578e0-110">Canal</span><span class="sxs-lookup"><span data-stu-id="578e0-110">Channel</span></span>|<span data-ttu-id="578e0-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="578e0-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="578e0-112">Description</span><span class="sxs-lookup"><span data-stu-id="578e0-112">Description</span></span>  
 <span data-ttu-id="578e0-113">Indique qu'un FaultWorkItem démarre l'exécution.</span><span class="sxs-lookup"><span data-stu-id="578e0-113">Indicates a FaultWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="578e0-114">Message</span><span class="sxs-lookup"><span data-stu-id="578e0-114">Message</span></span>  
 <span data-ttu-id="578e0-115">Début de l’exécution d’un FaultWorkItem pour l’activité '%1', DisplayName : '%2', InstanceId : '%3'.</span><span class="sxs-lookup"><span data-stu-id="578e0-115">Starting execution of a FaultWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="578e0-116">L'exception a été propagée à partir de l'activité « %4 », DisplayName : « %5 », InstanceId : « %6 ».</span><span class="sxs-lookup"><span data-stu-id="578e0-116">The exception was propagated from Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="578e0-117">Détails</span><span class="sxs-lookup"><span data-stu-id="578e0-117">Details</span></span>  
  
|<span data-ttu-id="578e0-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="578e0-118">Data Item Name</span></span>|<span data-ttu-id="578e0-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="578e0-119">Data Item Type</span></span>|<span data-ttu-id="578e0-120">Description</span><span class="sxs-lookup"><span data-stu-id="578e0-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="578e0-121">FaultActivity</span><span class="sxs-lookup"><span data-stu-id="578e0-121">FaultActivity</span></span>|<span data-ttu-id="578e0-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="578e0-122">xs:string</span></span>|<span data-ttu-id="578e0-123">Nom de type de l'activité d'erreur.</span><span class="sxs-lookup"><span data-stu-id="578e0-123">The type name of the fault activity.</span></span>|  
|<span data-ttu-id="578e0-124">FaultActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="578e0-124">FaultActivityDisplayName</span></span>|<span data-ttu-id="578e0-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="578e0-125">xs:string</span></span>|<span data-ttu-id="578e0-126">Nom complet de l'activité d'erreur.</span><span class="sxs-lookup"><span data-stu-id="578e0-126">The display name of the fault activity.</span></span>|  
|<span data-ttu-id="578e0-127">FaultActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="578e0-127">FaultActivityInstanceId</span></span>|<span data-ttu-id="578e0-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="578e0-128">xs:string</span></span>|<span data-ttu-id="578e0-129">ID d'instance de l'activité d'erreur.</span><span class="sxs-lookup"><span data-stu-id="578e0-129">The instance id of the fault activity.</span></span>|  
|<span data-ttu-id="578e0-130">ExceptionActivity</span><span class="sxs-lookup"><span data-stu-id="578e0-130">ExceptionActivity</span></span>|<span data-ttu-id="578e0-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="578e0-131">xs:string</span></span>|<span data-ttu-id="578e0-132">Nom de type de l'activité qui a levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="578e0-132">The type name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="578e0-133">ExceptionActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="578e0-133">ExceptionActivityDisplayName</span></span>|<span data-ttu-id="578e0-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="578e0-134">xs:string</span></span>|<span data-ttu-id="578e0-135">Nom complet de l'activité qui a levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="578e0-135">The display name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="578e0-136">ExceptionActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="578e0-136">ExceptionActivityInstanceId</span></span>|<span data-ttu-id="578e0-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="578e0-137">xs:string</span></span>|<span data-ttu-id="578e0-138">ID d'instance de l'activité ayant levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="578e0-138">The instance id of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="578e0-139">Exception</span><span class="sxs-lookup"><span data-stu-id="578e0-139">Exception</span></span>|<span data-ttu-id="578e0-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="578e0-140">xs:string</span></span>|<span data-ttu-id="578e0-141">Détails de l'exception</span><span class="sxs-lookup"><span data-stu-id="578e0-141">The exception details for the exception</span></span>|  
|<span data-ttu-id="578e0-142">AppDomain</span><span class="sxs-lookup"><span data-stu-id="578e0-142">AppDomain</span></span>|<span data-ttu-id="578e0-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="578e0-143">xs:string</span></span>|<span data-ttu-id="578e0-144">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="578e0-144">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
