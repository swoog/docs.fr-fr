---
title: 1011 - ScheduleExecuteActivityWorkItem
ms.date: 03/30/2017
ms.assetid: e503ae46-ad6b-4fcb-8c0e-146d59a8eff1
ms.openlocfilehash: 299d09b7c4db94a2e27378ba0cc3dfeb03734ab4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33509613"
---
# <a name="1011---scheduleexecuteactivityworkitem"></a><span data-ttu-id="49b45-102">1011 - ScheduleExecuteActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="49b45-102">1011 - ScheduleExecuteActivityWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="49b45-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="49b45-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="49b45-104">ID</span><span class="sxs-lookup"><span data-stu-id="49b45-104">ID</span></span>|<span data-ttu-id="49b45-105">1011</span><span class="sxs-lookup"><span data-stu-id="49b45-105">1011</span></span>|  
|<span data-ttu-id="49b45-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="49b45-106">Keywords</span></span>|<span data-ttu-id="49b45-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="49b45-107">WFRuntime</span></span>|  
|<span data-ttu-id="49b45-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="49b45-108">Level</span></span>|<span data-ttu-id="49b45-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="49b45-109">Verbose</span></span>|  
|<span data-ttu-id="49b45-110">Canal</span><span class="sxs-lookup"><span data-stu-id="49b45-110">Channel</span></span>|<span data-ttu-id="49b45-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="49b45-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="49b45-112">Description</span><span class="sxs-lookup"><span data-stu-id="49b45-112">Description</span></span>  
 <span data-ttu-id="49b45-113">Indique qu'un ExecuteActivityWorkItem a été planifié.</span><span class="sxs-lookup"><span data-stu-id="49b45-113">Indicates an ExecuteActivityWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="49b45-114">Message</span><span class="sxs-lookup"><span data-stu-id="49b45-114">Message</span></span>  
 <span data-ttu-id="49b45-115">ExecuteActivityWorkItem a été planifié pour l'activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="49b45-115">An ExecuteActivityWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="49b45-116">Détails</span><span class="sxs-lookup"><span data-stu-id="49b45-116">Details</span></span>  
  
|<span data-ttu-id="49b45-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="49b45-117">Data Item Name</span></span>|<span data-ttu-id="49b45-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="49b45-118">Data Item Type</span></span>|<span data-ttu-id="49b45-119">Description</span><span class="sxs-lookup"><span data-stu-id="49b45-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="49b45-120">Activité</span><span class="sxs-lookup"><span data-stu-id="49b45-120">Activity</span></span>|<span data-ttu-id="49b45-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="49b45-121">xs:string</span></span>|<span data-ttu-id="49b45-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="49b45-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="49b45-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="49b45-123">DisplayName</span></span>|<span data-ttu-id="49b45-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="49b45-124">xs:string</span></span>|<span data-ttu-id="49b45-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="49b45-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="49b45-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="49b45-126">InstanceId</span></span>|<span data-ttu-id="49b45-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="49b45-127">xs:string</span></span>|<span data-ttu-id="49b45-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="49b45-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="49b45-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="49b45-129">AppDomain</span></span>|<span data-ttu-id="49b45-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="49b45-130">xs:string</span></span>|<span data-ttu-id="49b45-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="49b45-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
