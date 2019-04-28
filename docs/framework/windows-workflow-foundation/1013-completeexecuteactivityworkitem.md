---
title: 1013 - CompleteExecuteActivityWorkItem
ms.date: 03/30/2017
ms.assetid: 31fc57b3-ef2f-48f0-a5de-b4e2c5c9ded7
ms.openlocfilehash: c1ff62bb4143bb798ea7adb7c3fee539ef68bc37
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61925188"
---
# <a name="1013---completeexecuteactivityworkitem"></a><span data-ttu-id="544df-102">1013 - CompleteExecuteActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="544df-102">1013 - CompleteExecuteActivityWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="544df-103">Properties</span><span class="sxs-lookup"><span data-stu-id="544df-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="544df-104">Id</span><span class="sxs-lookup"><span data-stu-id="544df-104">ID</span></span>|<span data-ttu-id="544df-105">1013</span><span class="sxs-lookup"><span data-stu-id="544df-105">1013</span></span>|  
|<span data-ttu-id="544df-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="544df-106">Keywords</span></span>|<span data-ttu-id="544df-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="544df-107">WFRuntime</span></span>|  
|<span data-ttu-id="544df-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="544df-108">Level</span></span>|<span data-ttu-id="544df-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="544df-109">Verbose</span></span>|  
|<span data-ttu-id="544df-110">Canal</span><span class="sxs-lookup"><span data-stu-id="544df-110">Channel</span></span>|<span data-ttu-id="544df-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="544df-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="544df-112">Description</span><span class="sxs-lookup"><span data-stu-id="544df-112">Description</span></span>  
 <span data-ttu-id="544df-113">Indique qu'un ExecuteActivityWorkItem est terminé.</span><span class="sxs-lookup"><span data-stu-id="544df-113">Indicates an ExecuteActivityWorkItem has completed</span></span>  
  
## <a name="message"></a><span data-ttu-id="544df-114">Message</span><span class="sxs-lookup"><span data-stu-id="544df-114">Message</span></span>  
 <span data-ttu-id="544df-115">ExecuteActivityWorkItem est terminé pour l'activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="544df-115">An ExecuteActivityWorkItem has completed for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="544df-116">Détails</span><span class="sxs-lookup"><span data-stu-id="544df-116">Details</span></span>  
  
|<span data-ttu-id="544df-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="544df-117">Data Item Name</span></span>|<span data-ttu-id="544df-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="544df-118">Data Item Type</span></span>|<span data-ttu-id="544df-119">Description</span><span class="sxs-lookup"><span data-stu-id="544df-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="544df-120">Activité</span><span class="sxs-lookup"><span data-stu-id="544df-120">Activity</span></span>|<span data-ttu-id="544df-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="544df-121">xs:string</span></span>|<span data-ttu-id="544df-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="544df-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="544df-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="544df-123">DisplayName</span></span>|<span data-ttu-id="544df-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="544df-124">xs:string</span></span>|<span data-ttu-id="544df-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="544df-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="544df-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="544df-126">InstanceId</span></span>|<span data-ttu-id="544df-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="544df-127">xs:string</span></span>|<span data-ttu-id="544df-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="544df-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="544df-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="544df-129">AppDomain</span></span>|<span data-ttu-id="544df-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="544df-130">xs:string</span></span>|<span data-ttu-id="544df-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="544df-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
