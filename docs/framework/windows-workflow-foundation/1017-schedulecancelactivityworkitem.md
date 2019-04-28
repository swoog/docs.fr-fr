---
title: 1017 - ScheduleCancelActivityWorkItem
ms.date: 03/30/2017
ms.assetid: 864546ab-d65c-4989-8fcb-537ba03a3cdd
ms.openlocfilehash: 186b012cdd554ec7dd0d195b460619cca04eddcb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924486"
---
# <a name="1017---schedulecancelactivityworkitem"></a><span data-ttu-id="b09ba-102">1017 - ScheduleCancelActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="b09ba-102">1017 - ScheduleCancelActivityWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="b09ba-103">Properties</span><span class="sxs-lookup"><span data-stu-id="b09ba-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="b09ba-104">Id</span><span class="sxs-lookup"><span data-stu-id="b09ba-104">ID</span></span>|<span data-ttu-id="b09ba-105">1017</span><span class="sxs-lookup"><span data-stu-id="b09ba-105">1017</span></span>|  
|<span data-ttu-id="b09ba-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b09ba-106">Keywords</span></span>|<span data-ttu-id="b09ba-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="b09ba-107">WFRuntime</span></span>|  
|<span data-ttu-id="b09ba-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="b09ba-108">Level</span></span>|<span data-ttu-id="b09ba-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="b09ba-109">Verbose</span></span>|  
|<span data-ttu-id="b09ba-110">Canal</span><span class="sxs-lookup"><span data-stu-id="b09ba-110">Channel</span></span>|<span data-ttu-id="b09ba-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="b09ba-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="b09ba-112">Description</span><span class="sxs-lookup"><span data-stu-id="b09ba-112">Description</span></span>  
 <span data-ttu-id="b09ba-113">Indique qu'un CancelActivityWorkItem a été planifié.</span><span class="sxs-lookup"><span data-stu-id="b09ba-113">Indicates a CancelActivityWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="b09ba-114">Message</span><span class="sxs-lookup"><span data-stu-id="b09ba-114">Message</span></span>  
 <span data-ttu-id="b09ba-115">CancelActivityWorkItem a été planifié pour l'activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="b09ba-115">A CancelActivityWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="b09ba-116">Détails</span><span class="sxs-lookup"><span data-stu-id="b09ba-116">Details</span></span>  
  
|<span data-ttu-id="b09ba-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="b09ba-117">Data Item Name</span></span>|<span data-ttu-id="b09ba-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="b09ba-118">Data Item Type</span></span>|<span data-ttu-id="b09ba-119">Description</span><span class="sxs-lookup"><span data-stu-id="b09ba-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="b09ba-120">Activité</span><span class="sxs-lookup"><span data-stu-id="b09ba-120">Activity</span></span>|<span data-ttu-id="b09ba-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="b09ba-121">xs:string</span></span>|<span data-ttu-id="b09ba-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="b09ba-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="b09ba-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="b09ba-123">DisplayName</span></span>|<span data-ttu-id="b09ba-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="b09ba-124">xs:string</span></span>|<span data-ttu-id="b09ba-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="b09ba-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="b09ba-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="b09ba-126">InstanceId</span></span>|<span data-ttu-id="b09ba-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="b09ba-127">xs:string</span></span>|<span data-ttu-id="b09ba-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="b09ba-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="b09ba-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="b09ba-129">AppDomain</span></span>|<span data-ttu-id="b09ba-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="b09ba-130">xs:string</span></span>|<span data-ttu-id="b09ba-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="b09ba-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
