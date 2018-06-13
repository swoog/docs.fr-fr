---
title: 1035 - RuntimeTransactionSet
ms.date: 03/30/2017
ms.assetid: 03b37de9-778c-4beb-b0e3-de73ece6088e
ms.openlocfilehash: 198e11dd94b0ad5cdc1e01c3611280754ca081d3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33510032"
---
# <a name="1035---runtimetransactionset"></a><span data-ttu-id="956b5-102">1035 - RuntimeTransactionSet</span><span class="sxs-lookup"><span data-stu-id="956b5-102">1035 - RuntimeTransactionSet</span></span>
## <a name="properties"></a><span data-ttu-id="956b5-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="956b5-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="956b5-104">ID</span><span class="sxs-lookup"><span data-stu-id="956b5-104">ID</span></span>|<span data-ttu-id="956b5-105">1035</span><span class="sxs-lookup"><span data-stu-id="956b5-105">1035</span></span>|  
|<span data-ttu-id="956b5-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="956b5-106">Keywords</span></span>|<span data-ttu-id="956b5-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="956b5-107">WFRuntime</span></span>|  
|<span data-ttu-id="956b5-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="956b5-108">Level</span></span>|<span data-ttu-id="956b5-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="956b5-109">Verbose</span></span>|  
|<span data-ttu-id="956b5-110">Canal</span><span class="sxs-lookup"><span data-stu-id="956b5-110">Channel</span></span>|<span data-ttu-id="956b5-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="956b5-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="956b5-112">Description</span><span class="sxs-lookup"><span data-stu-id="956b5-112">Description</span></span>  
 <span data-ttu-id="956b5-113">Indique qu'une activité a défini la transaction d'exécution.</span><span class="sxs-lookup"><span data-stu-id="956b5-113">Indicates an activity has set the runtime transaction.</span></span>  
  
## <a name="message"></a><span data-ttu-id="956b5-114">Message</span><span class="sxs-lookup"><span data-stu-id="956b5-114">Message</span></span>  
 <span data-ttu-id="956b5-115">La transaction runtime a été définie par l’activité '%1', DisplayName : '%2', InstanceId : '%3'.</span><span class="sxs-lookup"><span data-stu-id="956b5-115">The runtime transaction has been set by Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="956b5-116">L’exécution isolée à l’activité '%4', DisplayName : '%5', InstanceId : '%6'.</span><span class="sxs-lookup"><span data-stu-id="956b5-116">Execution isolated to Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="956b5-117">Détails</span><span class="sxs-lookup"><span data-stu-id="956b5-117">Details</span></span>  
  
|<span data-ttu-id="956b5-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="956b5-118">Data Item Name</span></span>|<span data-ttu-id="956b5-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="956b5-119">Data Item Type</span></span>|<span data-ttu-id="956b5-120">Description</span><span class="sxs-lookup"><span data-stu-id="956b5-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="956b5-121">Activité</span><span class="sxs-lookup"><span data-stu-id="956b5-121">Activity</span></span>|<span data-ttu-id="956b5-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="956b5-122">xs:string</span></span>|<span data-ttu-id="956b5-123">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="956b5-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="956b5-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="956b5-124">DisplayName</span></span>|<span data-ttu-id="956b5-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="956b5-125">xs:string</span></span>|<span data-ttu-id="956b5-126">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="956b5-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="956b5-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="956b5-127">InstanceId</span></span>|<span data-ttu-id="956b5-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="956b5-128">xs:string</span></span>|<span data-ttu-id="956b5-129">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="956b5-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="956b5-130">IsolatedActivity</span><span class="sxs-lookup"><span data-stu-id="956b5-130">IsolatedActivity</span></span>|<span data-ttu-id="956b5-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="956b5-131">xs:string</span></span>|<span data-ttu-id="956b5-132">Nom de type de l'activité dans laquelle la transaction est isolée.</span><span class="sxs-lookup"><span data-stu-id="956b5-132">The type name of the activity that the transaction is isolated to.</span></span>|  
|<span data-ttu-id="956b5-133">IsolatedActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="956b5-133">IsolatedActivityDisplayName</span></span>|<span data-ttu-id="956b5-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="956b5-134">xs:string</span></span>|<span data-ttu-id="956b5-135">Nom complet de l'activité dans laquelle la transaction est isolée.</span><span class="sxs-lookup"><span data-stu-id="956b5-135">The display name of the activity that the transaction is isolated to.</span></span>|  
|<span data-ttu-id="956b5-136">IsolatedActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="956b5-136">IsolatedActivityInstanceId</span></span>|<span data-ttu-id="956b5-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="956b5-137">xs:string</span></span>|<span data-ttu-id="956b5-138">ID d'instance de l'activité dans laquelle la transaction est isolée.</span><span class="sxs-lookup"><span data-stu-id="956b5-138">The instance id of the activity that the transaction is isolated to.</span></span>|  
|<span data-ttu-id="956b5-139">AppDomain</span><span class="sxs-lookup"><span data-stu-id="956b5-139">AppDomain</span></span>|<span data-ttu-id="956b5-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="956b5-140">xs:string</span></span>|<span data-ttu-id="956b5-141">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="956b5-141">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
