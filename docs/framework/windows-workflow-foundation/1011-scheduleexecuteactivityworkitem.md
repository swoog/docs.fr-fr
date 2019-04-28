---
title: 1011 - ScheduleExecuteActivityWorkItem
ms.date: 03/30/2017
ms.assetid: e503ae46-ad6b-4fcb-8c0e-146d59a8eff1
ms.openlocfilehash: 299d09b7c4db94a2e27378ba0cc3dfeb03734ab4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61982252"
---
# <a name="1011---scheduleexecuteactivityworkitem"></a><span data-ttu-id="aa930-102">1011 - ScheduleExecuteActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="aa930-102">1011 - ScheduleExecuteActivityWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="aa930-103">Properties</span><span class="sxs-lookup"><span data-stu-id="aa930-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="aa930-104">Id</span><span class="sxs-lookup"><span data-stu-id="aa930-104">ID</span></span>|<span data-ttu-id="aa930-105">1011</span><span class="sxs-lookup"><span data-stu-id="aa930-105">1011</span></span>|  
|<span data-ttu-id="aa930-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="aa930-106">Keywords</span></span>|<span data-ttu-id="aa930-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="aa930-107">WFRuntime</span></span>|  
|<span data-ttu-id="aa930-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="aa930-108">Level</span></span>|<span data-ttu-id="aa930-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="aa930-109">Verbose</span></span>|  
|<span data-ttu-id="aa930-110">Canal</span><span class="sxs-lookup"><span data-stu-id="aa930-110">Channel</span></span>|<span data-ttu-id="aa930-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="aa930-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="aa930-112">Description</span><span class="sxs-lookup"><span data-stu-id="aa930-112">Description</span></span>  
 <span data-ttu-id="aa930-113">Indique qu'un ExecuteActivityWorkItem a été planifié.</span><span class="sxs-lookup"><span data-stu-id="aa930-113">Indicates an ExecuteActivityWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="aa930-114">Message</span><span class="sxs-lookup"><span data-stu-id="aa930-114">Message</span></span>  
 <span data-ttu-id="aa930-115">ExecuteActivityWorkItem a été planifié pour l'activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="aa930-115">An ExecuteActivityWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="aa930-116">Détails</span><span class="sxs-lookup"><span data-stu-id="aa930-116">Details</span></span>  
  
|<span data-ttu-id="aa930-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="aa930-117">Data Item Name</span></span>|<span data-ttu-id="aa930-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="aa930-118">Data Item Type</span></span>|<span data-ttu-id="aa930-119">Description</span><span class="sxs-lookup"><span data-stu-id="aa930-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="aa930-120">Activité</span><span class="sxs-lookup"><span data-stu-id="aa930-120">Activity</span></span>|<span data-ttu-id="aa930-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="aa930-121">xs:string</span></span>|<span data-ttu-id="aa930-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="aa930-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="aa930-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="aa930-123">DisplayName</span></span>|<span data-ttu-id="aa930-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="aa930-124">xs:string</span></span>|<span data-ttu-id="aa930-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="aa930-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="aa930-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="aa930-126">InstanceId</span></span>|<span data-ttu-id="aa930-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="aa930-127">xs:string</span></span>|<span data-ttu-id="aa930-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="aa930-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="aa930-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="aa930-129">AppDomain</span></span>|<span data-ttu-id="aa930-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="aa930-130">xs:string</span></span>|<span data-ttu-id="aa930-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="aa930-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
