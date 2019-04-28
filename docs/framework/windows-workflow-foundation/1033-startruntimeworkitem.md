---
title: 1033 - StartRuntimeWorkItem
ms.date: 03/30/2017
ms.assetid: 172b5346-9f3b-46ae-bc06-39872022376a
ms.openlocfilehash: c7192ed7c5fb43fe6f65b47b8cebde3cf4aed32c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924239"
---
# <a name="1033---startruntimeworkitem"></a><span data-ttu-id="5c61c-102">1033 - StartRuntimeWorkItem</span><span class="sxs-lookup"><span data-stu-id="5c61c-102">1033 - StartRuntimeWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="5c61c-103">Properties</span><span class="sxs-lookup"><span data-stu-id="5c61c-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="5c61c-104">Id</span><span class="sxs-lookup"><span data-stu-id="5c61c-104">ID</span></span>|<span data-ttu-id="5c61c-105">1033</span><span class="sxs-lookup"><span data-stu-id="5c61c-105">1033</span></span>|  
|<span data-ttu-id="5c61c-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="5c61c-106">Keywords</span></span>|<span data-ttu-id="5c61c-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="5c61c-107">WFRuntime</span></span>|  
|<span data-ttu-id="5c61c-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="5c61c-108">Level</span></span>|<span data-ttu-id="5c61c-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="5c61c-109">Verbose</span></span>|  
|<span data-ttu-id="5c61c-110">Canal</span><span class="sxs-lookup"><span data-stu-id="5c61c-110">Channel</span></span>|<span data-ttu-id="5c61c-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="5c61c-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="5c61c-112">Description</span><span class="sxs-lookup"><span data-stu-id="5c61c-112">Description</span></span>  
 <span data-ttu-id="5c61c-113">Indique qu'un RuntimeWorkItem démarre l'exécution.</span><span class="sxs-lookup"><span data-stu-id="5c61c-113">Indicates a RuntimeWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="5c61c-114">Message</span><span class="sxs-lookup"><span data-stu-id="5c61c-114">Message</span></span>  
 <span data-ttu-id="5c61c-115">Début de l’exécution d’un élément de travail runtime pour l’activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="5c61c-115">Starting execution of a runtime work item for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="5c61c-116">Détails</span><span class="sxs-lookup"><span data-stu-id="5c61c-116">Details</span></span>  
  
|<span data-ttu-id="5c61c-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="5c61c-117">Data Item Name</span></span>|<span data-ttu-id="5c61c-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="5c61c-118">Data Item Type</span></span>|<span data-ttu-id="5c61c-119">Description</span><span class="sxs-lookup"><span data-stu-id="5c61c-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="5c61c-120">Activité</span><span class="sxs-lookup"><span data-stu-id="5c61c-120">Activity</span></span>|<span data-ttu-id="5c61c-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="5c61c-121">xs:string</span></span>|<span data-ttu-id="5c61c-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="5c61c-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="5c61c-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="5c61c-123">DisplayName</span></span>|<span data-ttu-id="5c61c-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="5c61c-124">xs:string</span></span>|<span data-ttu-id="5c61c-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="5c61c-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="5c61c-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="5c61c-126">InstanceId</span></span>|<span data-ttu-id="5c61c-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="5c61c-127">xs:string</span></span>|<span data-ttu-id="5c61c-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="5c61c-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="5c61c-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="5c61c-129">AppDomain</span></span>|<span data-ttu-id="5c61c-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="5c61c-130">xs:string</span></span>|<span data-ttu-id="5c61c-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="5c61c-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
