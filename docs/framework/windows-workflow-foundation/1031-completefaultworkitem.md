---
title: 1031 - CompleteFaultWorkItem
ms.date: 03/30/2017
ms.assetid: 95f4ccb0-6be4-41f3-9330-fae43165828f
ms.openlocfilehash: cdcbe516fc8ba7440b3d109a5e5cadc105ecee9f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62008796"
---
# <a name="1031---completefaultworkitem"></a><span data-ttu-id="fcf89-102">1031 - CompleteFaultWorkItem</span><span class="sxs-lookup"><span data-stu-id="fcf89-102">1031 - CompleteFaultWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="fcf89-103">Properties</span><span class="sxs-lookup"><span data-stu-id="fcf89-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="fcf89-104">Id</span><span class="sxs-lookup"><span data-stu-id="fcf89-104">ID</span></span>|<span data-ttu-id="fcf89-105">1031</span><span class="sxs-lookup"><span data-stu-id="fcf89-105">1031</span></span>|  
|<span data-ttu-id="fcf89-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fcf89-106">Keywords</span></span>|<span data-ttu-id="fcf89-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="fcf89-107">WFRuntime</span></span>|  
|<span data-ttu-id="fcf89-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="fcf89-108">Level</span></span>|<span data-ttu-id="fcf89-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="fcf89-109">Verbose</span></span>|  
|<span data-ttu-id="fcf89-110">Canal</span><span class="sxs-lookup"><span data-stu-id="fcf89-110">Channel</span></span>|<span data-ttu-id="fcf89-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="fcf89-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="fcf89-112">Description</span><span class="sxs-lookup"><span data-stu-id="fcf89-112">Description</span></span>  
 <span data-ttu-id="fcf89-113">Indique qu'un FaultWorkItem est terminé.</span><span class="sxs-lookup"><span data-stu-id="fcf89-113">Indicates a FaultWorkItem has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="fcf89-114">Message</span><span class="sxs-lookup"><span data-stu-id="fcf89-114">Message</span></span>  
 <span data-ttu-id="fcf89-115">Un FaultWorkItem est achevé pour l'activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="fcf89-115">A FaultWorkItem has completed for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span> <span data-ttu-id="fcf89-116">L'exception a été propagée à partir de l'activité « %4 », DisplayName : « %5 », InstanceId : « %6 ».</span><span class="sxs-lookup"><span data-stu-id="fcf89-116">The exception was propagated from Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="fcf89-117">Détails</span><span class="sxs-lookup"><span data-stu-id="fcf89-117">Details</span></span>  
  
|<span data-ttu-id="fcf89-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="fcf89-118">Data Item Name</span></span>|<span data-ttu-id="fcf89-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="fcf89-119">Data Item Type</span></span>|<span data-ttu-id="fcf89-120">Description</span><span class="sxs-lookup"><span data-stu-id="fcf89-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="fcf89-121">FaultActivity</span><span class="sxs-lookup"><span data-stu-id="fcf89-121">FaultActivity</span></span>|<span data-ttu-id="fcf89-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="fcf89-122">xs:string</span></span>|<span data-ttu-id="fcf89-123">Nom de type de l'activité d'erreur.</span><span class="sxs-lookup"><span data-stu-id="fcf89-123">The type name of the fault activity.</span></span>|  
|<span data-ttu-id="fcf89-124">FaultActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="fcf89-124">FaultActivityDisplayName</span></span>|<span data-ttu-id="fcf89-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="fcf89-125">xs:string</span></span>|<span data-ttu-id="fcf89-126">Nom complet de l'activité d'erreur.</span><span class="sxs-lookup"><span data-stu-id="fcf89-126">The display name of the fault activity.</span></span>|  
|<span data-ttu-id="fcf89-127">FaultActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="fcf89-127">FaultActivityInstanceId</span></span>|<span data-ttu-id="fcf89-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="fcf89-128">xs:string</span></span>|<span data-ttu-id="fcf89-129">ID d'instance de l'activité d'erreur.</span><span class="sxs-lookup"><span data-stu-id="fcf89-129">The instance id of the fault activity.</span></span>|  
|<span data-ttu-id="fcf89-130">ExceptionActivity</span><span class="sxs-lookup"><span data-stu-id="fcf89-130">ExceptionActivity</span></span>|<span data-ttu-id="fcf89-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="fcf89-131">xs:string</span></span>|<span data-ttu-id="fcf89-132">Nom de type de l'activité qui a levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="fcf89-132">The type name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="fcf89-133">ExceptionActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="fcf89-133">ExceptionActivityDisplayName</span></span>|<span data-ttu-id="fcf89-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="fcf89-134">xs:string</span></span>|<span data-ttu-id="fcf89-135">Nom complet de l'activité qui a levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="fcf89-135">The display name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="fcf89-136">ExceptionActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="fcf89-136">ExceptionActivityInstanceId</span></span>|<span data-ttu-id="fcf89-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="fcf89-137">xs:string</span></span>|<span data-ttu-id="fcf89-138">ID d'instance de l'activité ayant levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="fcf89-138">The instance id of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="fcf89-139">Exception</span><span class="sxs-lookup"><span data-stu-id="fcf89-139">Exception</span></span>|<span data-ttu-id="fcf89-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="fcf89-140">xs:string</span></span>|<span data-ttu-id="fcf89-141">Détails de l'exception</span><span class="sxs-lookup"><span data-stu-id="fcf89-141">The exception details for the exception</span></span>|  
|<span data-ttu-id="fcf89-142">AppDomain</span><span class="sxs-lookup"><span data-stu-id="fcf89-142">AppDomain</span></span>|<span data-ttu-id="fcf89-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="fcf89-143">xs:string</span></span>|<span data-ttu-id="fcf89-144">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="fcf89-144">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
