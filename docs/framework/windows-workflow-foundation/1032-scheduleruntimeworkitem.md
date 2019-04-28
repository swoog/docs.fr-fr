---
title: 1032 - ScheduleRuntimeWorkItem
ms.date: 03/30/2017
ms.assetid: 54688101-becf-42f3-80ca-f53a7b527620
ms.openlocfilehash: 505b852d54e256b2c2bfff8d90944dd4e993e0c0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924863"
---
# <a name="1032---scheduleruntimeworkitem"></a><span data-ttu-id="b29f7-102">1032 - ScheduleRuntimeWorkItem</span><span class="sxs-lookup"><span data-stu-id="b29f7-102">1032 - ScheduleRuntimeWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="b29f7-103">Properties</span><span class="sxs-lookup"><span data-stu-id="b29f7-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="b29f7-104">Id</span><span class="sxs-lookup"><span data-stu-id="b29f7-104">ID</span></span>|<span data-ttu-id="b29f7-105">1032</span><span class="sxs-lookup"><span data-stu-id="b29f7-105">1032</span></span>|  
|<span data-ttu-id="b29f7-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b29f7-106">Keywords</span></span>|<span data-ttu-id="b29f7-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="b29f7-107">WFRuntime</span></span>|  
|<span data-ttu-id="b29f7-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="b29f7-108">Level</span></span>|<span data-ttu-id="b29f7-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="b29f7-109">Verbose</span></span>|  
|<span data-ttu-id="b29f7-110">Canal</span><span class="sxs-lookup"><span data-stu-id="b29f7-110">Channel</span></span>|<span data-ttu-id="b29f7-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="b29f7-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="b29f7-112">Description</span><span class="sxs-lookup"><span data-stu-id="b29f7-112">Description</span></span>  
 <span data-ttu-id="b29f7-113">Indique qu'un RuntimeWorkItem a été planifié.</span><span class="sxs-lookup"><span data-stu-id="b29f7-113">Indicates a RuntimeWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="b29f7-114">Message</span><span class="sxs-lookup"><span data-stu-id="b29f7-114">Message</span></span>  
 <span data-ttu-id="b29f7-115">Un élément de travail runtime a été planifié pour l’activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="b29f7-115">A runtime work item has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="b29f7-116">Détails</span><span class="sxs-lookup"><span data-stu-id="b29f7-116">Details</span></span>  
  
|<span data-ttu-id="b29f7-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="b29f7-117">Data Item Name</span></span>|<span data-ttu-id="b29f7-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="b29f7-118">Data Item Type</span></span>|<span data-ttu-id="b29f7-119">Description</span><span class="sxs-lookup"><span data-stu-id="b29f7-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="b29f7-120">Activité</span><span class="sxs-lookup"><span data-stu-id="b29f7-120">Activity</span></span>|<span data-ttu-id="b29f7-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="b29f7-121">xs:string</span></span>|<span data-ttu-id="b29f7-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="b29f7-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="b29f7-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="b29f7-123">DisplayName</span></span>|<span data-ttu-id="b29f7-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="b29f7-124">xs:string</span></span>|<span data-ttu-id="b29f7-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="b29f7-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="b29f7-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="b29f7-126">InstanceId</span></span>|<span data-ttu-id="b29f7-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="b29f7-127">xs:string</span></span>|<span data-ttu-id="b29f7-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="b29f7-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="b29f7-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="b29f7-129">AppDomain</span></span>|<span data-ttu-id="b29f7-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="b29f7-130">xs:string</span></span>|<span data-ttu-id="b29f7-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="b29f7-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
