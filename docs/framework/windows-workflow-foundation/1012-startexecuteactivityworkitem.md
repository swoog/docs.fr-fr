---
title: 1012 - StartExecuteActivityWorkItem
ms.date: 03/30/2017
ms.assetid: 29e9b1c6-c5d7-4b58-b59d-a06a923d3c80
ms.openlocfilehash: d6b330bc454c39584e5027f757fd9d9d3434d941
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924577"
---
# <a name="1012---startexecuteactivityworkitem"></a><span data-ttu-id="ca815-102">1012 - StartExecuteActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="ca815-102">1012 - StartExecuteActivityWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="ca815-103">Properties</span><span class="sxs-lookup"><span data-stu-id="ca815-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="ca815-104">Id</span><span class="sxs-lookup"><span data-stu-id="ca815-104">ID</span></span>|<span data-ttu-id="ca815-105">1012</span><span class="sxs-lookup"><span data-stu-id="ca815-105">1012</span></span>|  
|<span data-ttu-id="ca815-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="ca815-106">Keywords</span></span>|<span data-ttu-id="ca815-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="ca815-107">WFRuntime</span></span>|  
|<span data-ttu-id="ca815-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="ca815-108">Level</span></span>|<span data-ttu-id="ca815-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="ca815-109">Verbose</span></span>|  
|<span data-ttu-id="ca815-110">Canal</span><span class="sxs-lookup"><span data-stu-id="ca815-110">Channel</span></span>|<span data-ttu-id="ca815-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="ca815-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="ca815-112">Description</span><span class="sxs-lookup"><span data-stu-id="ca815-112">Description</span></span>  
 <span data-ttu-id="ca815-113">Indique qu'un ExecuteActivityWorkItem démarre l'exécution.</span><span class="sxs-lookup"><span data-stu-id="ca815-113">Indicates an ExecuteActivityWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="ca815-114">Message</span><span class="sxs-lookup"><span data-stu-id="ca815-114">Message</span></span>  
 <span data-ttu-id="ca815-115">Début de l'exécution d'un ExecuteActivityWorkItem pour l'activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="ca815-115">Starting execution of an ExecuteActivityWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="ca815-116">Détails</span><span class="sxs-lookup"><span data-stu-id="ca815-116">Details</span></span>  
  
|<span data-ttu-id="ca815-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="ca815-117">Data Item Name</span></span>|<span data-ttu-id="ca815-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="ca815-118">Data Item Type</span></span>|<span data-ttu-id="ca815-119">Description</span><span class="sxs-lookup"><span data-stu-id="ca815-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="ca815-120">Activité</span><span class="sxs-lookup"><span data-stu-id="ca815-120">Activity</span></span>|<span data-ttu-id="ca815-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="ca815-121">xs:string</span></span>|<span data-ttu-id="ca815-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="ca815-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="ca815-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="ca815-123">DisplayName</span></span>|<span data-ttu-id="ca815-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="ca815-124">xs:string</span></span>|<span data-ttu-id="ca815-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="ca815-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="ca815-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="ca815-126">InstanceId</span></span>|<span data-ttu-id="ca815-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="ca815-127">xs:string</span></span>|<span data-ttu-id="ca815-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="ca815-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="ca815-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="ca815-129">AppDomain</span></span>|<span data-ttu-id="ca815-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="ca815-130">xs:string</span></span>|<span data-ttu-id="ca815-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="ca815-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
