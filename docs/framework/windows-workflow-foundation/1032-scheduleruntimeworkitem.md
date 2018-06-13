---
title: 1032 - ScheduleRuntimeWorkItem
ms.date: 03/30/2017
ms.assetid: 54688101-becf-42f3-80ca-f53a7b527620
ms.openlocfilehash: 505b852d54e256b2c2bfff8d90944dd4e993e0c0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33510245"
---
# <a name="1032---scheduleruntimeworkitem"></a><span data-ttu-id="7b68a-102">1032 - ScheduleRuntimeWorkItem</span><span class="sxs-lookup"><span data-stu-id="7b68a-102">1032 - ScheduleRuntimeWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="7b68a-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b68a-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="7b68a-104">ID</span><span class="sxs-lookup"><span data-stu-id="7b68a-104">ID</span></span>|<span data-ttu-id="7b68a-105">1032</span><span class="sxs-lookup"><span data-stu-id="7b68a-105">1032</span></span>|  
|<span data-ttu-id="7b68a-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="7b68a-106">Keywords</span></span>|<span data-ttu-id="7b68a-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="7b68a-107">WFRuntime</span></span>|  
|<span data-ttu-id="7b68a-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="7b68a-108">Level</span></span>|<span data-ttu-id="7b68a-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="7b68a-109">Verbose</span></span>|  
|<span data-ttu-id="7b68a-110">Canal</span><span class="sxs-lookup"><span data-stu-id="7b68a-110">Channel</span></span>|<span data-ttu-id="7b68a-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="7b68a-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="7b68a-112">Description</span><span class="sxs-lookup"><span data-stu-id="7b68a-112">Description</span></span>  
 <span data-ttu-id="7b68a-113">Indique qu'un RuntimeWorkItem a été planifié.</span><span class="sxs-lookup"><span data-stu-id="7b68a-113">Indicates a RuntimeWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="7b68a-114">Message</span><span class="sxs-lookup"><span data-stu-id="7b68a-114">Message</span></span>  
 <span data-ttu-id="7b68a-115">Un élément de travail runtime a été planifié pour l'activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="7b68a-115">A runtime work item has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="7b68a-116">Détails</span><span class="sxs-lookup"><span data-stu-id="7b68a-116">Details</span></span>  
  
|<span data-ttu-id="7b68a-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="7b68a-117">Data Item Name</span></span>|<span data-ttu-id="7b68a-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="7b68a-118">Data Item Type</span></span>|<span data-ttu-id="7b68a-119">Description</span><span class="sxs-lookup"><span data-stu-id="7b68a-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="7b68a-120">Activité</span><span class="sxs-lookup"><span data-stu-id="7b68a-120">Activity</span></span>|<span data-ttu-id="7b68a-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b68a-121">xs:string</span></span>|<span data-ttu-id="7b68a-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="7b68a-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="7b68a-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="7b68a-123">DisplayName</span></span>|<span data-ttu-id="7b68a-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b68a-124">xs:string</span></span>|<span data-ttu-id="7b68a-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="7b68a-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="7b68a-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="7b68a-126">InstanceId</span></span>|<span data-ttu-id="7b68a-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b68a-127">xs:string</span></span>|<span data-ttu-id="7b68a-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="7b68a-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="7b68a-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="7b68a-129">AppDomain</span></span>|<span data-ttu-id="7b68a-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b68a-130">xs:string</span></span>|<span data-ttu-id="7b68a-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="7b68a-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
