---
title: 1035 - RuntimeTransactionSet
ms.date: 03/30/2017
ms.assetid: 03b37de9-778c-4beb-b0e3-de73ece6088e
ms.openlocfilehash: 198e11dd94b0ad5cdc1e01c3611280754ca081d3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924850"
---
# <a name="1035---runtimetransactionset"></a><span data-ttu-id="88f4e-102">1035 - RuntimeTransactionSet</span><span class="sxs-lookup"><span data-stu-id="88f4e-102">1035 - RuntimeTransactionSet</span></span>
## <a name="properties"></a><span data-ttu-id="88f4e-103">Properties</span><span class="sxs-lookup"><span data-stu-id="88f4e-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="88f4e-104">Id</span><span class="sxs-lookup"><span data-stu-id="88f4e-104">ID</span></span>|<span data-ttu-id="88f4e-105">1035</span><span class="sxs-lookup"><span data-stu-id="88f4e-105">1035</span></span>|  
|<span data-ttu-id="88f4e-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="88f4e-106">Keywords</span></span>|<span data-ttu-id="88f4e-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="88f4e-107">WFRuntime</span></span>|  
|<span data-ttu-id="88f4e-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="88f4e-108">Level</span></span>|<span data-ttu-id="88f4e-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="88f4e-109">Verbose</span></span>|  
|<span data-ttu-id="88f4e-110">Canal</span><span class="sxs-lookup"><span data-stu-id="88f4e-110">Channel</span></span>|<span data-ttu-id="88f4e-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="88f4e-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="88f4e-112">Description</span><span class="sxs-lookup"><span data-stu-id="88f4e-112">Description</span></span>  
 <span data-ttu-id="88f4e-113">Indique qu'une activité a défini la transaction d'exécution.</span><span class="sxs-lookup"><span data-stu-id="88f4e-113">Indicates an activity has set the runtime transaction.</span></span>  
  
## <a name="message"></a><span data-ttu-id="88f4e-114">Message</span><span class="sxs-lookup"><span data-stu-id="88f4e-114">Message</span></span>  
 <span data-ttu-id="88f4e-115">La transaction runtime a été définie par l’activité « %1 », DisplayName : « %2 », InstanceId : '%3'.</span><span class="sxs-lookup"><span data-stu-id="88f4e-115">The runtime transaction has been set by Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="88f4e-116">Exécution isolée à l’activité « %4 », DisplayName : « %5 », InstanceId : '%6'.</span><span class="sxs-lookup"><span data-stu-id="88f4e-116">Execution isolated to Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="88f4e-117">Détails</span><span class="sxs-lookup"><span data-stu-id="88f4e-117">Details</span></span>  
  
|<span data-ttu-id="88f4e-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="88f4e-118">Data Item Name</span></span>|<span data-ttu-id="88f4e-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="88f4e-119">Data Item Type</span></span>|<span data-ttu-id="88f4e-120">Description</span><span class="sxs-lookup"><span data-stu-id="88f4e-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="88f4e-121">Activité</span><span class="sxs-lookup"><span data-stu-id="88f4e-121">Activity</span></span>|<span data-ttu-id="88f4e-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="88f4e-122">xs:string</span></span>|<span data-ttu-id="88f4e-123">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="88f4e-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="88f4e-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="88f4e-124">DisplayName</span></span>|<span data-ttu-id="88f4e-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="88f4e-125">xs:string</span></span>|<span data-ttu-id="88f4e-126">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="88f4e-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="88f4e-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="88f4e-127">InstanceId</span></span>|<span data-ttu-id="88f4e-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="88f4e-128">xs:string</span></span>|<span data-ttu-id="88f4e-129">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="88f4e-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="88f4e-130">IsolatedActivity</span><span class="sxs-lookup"><span data-stu-id="88f4e-130">IsolatedActivity</span></span>|<span data-ttu-id="88f4e-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="88f4e-131">xs:string</span></span>|<span data-ttu-id="88f4e-132">Nom de type de l’activité dans laquelle la transaction est isolée.</span><span class="sxs-lookup"><span data-stu-id="88f4e-132">The type name of the activity that the transaction is isolated to.</span></span>|  
|<span data-ttu-id="88f4e-133">IsolatedActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="88f4e-133">IsolatedActivityDisplayName</span></span>|<span data-ttu-id="88f4e-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="88f4e-134">xs:string</span></span>|<span data-ttu-id="88f4e-135">Nom complet de l’activité dans laquelle la transaction est isolée.</span><span class="sxs-lookup"><span data-stu-id="88f4e-135">The display name of the activity that the transaction is isolated to.</span></span>|  
|<span data-ttu-id="88f4e-136">IsolatedActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="88f4e-136">IsolatedActivityInstanceId</span></span>|<span data-ttu-id="88f4e-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="88f4e-137">xs:string</span></span>|<span data-ttu-id="88f4e-138">ID d’instance de l’activité dans laquelle la transaction est isolée.</span><span class="sxs-lookup"><span data-stu-id="88f4e-138">The instance id of the activity that the transaction is isolated to.</span></span>|  
|<span data-ttu-id="88f4e-139">AppDomain</span><span class="sxs-lookup"><span data-stu-id="88f4e-139">AppDomain</span></span>|<span data-ttu-id="88f4e-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="88f4e-140">xs:string</span></span>|<span data-ttu-id="88f4e-141">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="88f4e-141">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
