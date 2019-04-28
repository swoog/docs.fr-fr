---
title: 1026 - ScheduleTransactionContextWorkItem
ms.date: 03/30/2017
ms.assetid: 0d5f86ba-ec21-4129-a726-5432e425384c
ms.openlocfilehash: 6d0b43208f86c52e8863d4415a64466b0531832c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924629"
---
# <a name="1026---scheduletransactioncontextworkitem"></a><span data-ttu-id="9ebdc-102">1026 - ScheduleTransactionContextWorkItem</span><span class="sxs-lookup"><span data-stu-id="9ebdc-102">1026 - ScheduleTransactionContextWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="9ebdc-103">Properties</span><span class="sxs-lookup"><span data-stu-id="9ebdc-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="9ebdc-104">Id</span><span class="sxs-lookup"><span data-stu-id="9ebdc-104">ID</span></span>|<span data-ttu-id="9ebdc-105">1026</span><span class="sxs-lookup"><span data-stu-id="9ebdc-105">1026</span></span>|  
|<span data-ttu-id="9ebdc-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="9ebdc-106">Keywords</span></span>|<span data-ttu-id="9ebdc-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="9ebdc-107">WFRuntime</span></span>|  
|<span data-ttu-id="9ebdc-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="9ebdc-108">Level</span></span>|<span data-ttu-id="9ebdc-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="9ebdc-109">Verbose</span></span>|  
|<span data-ttu-id="9ebdc-110">Canal</span><span class="sxs-lookup"><span data-stu-id="9ebdc-110">Channel</span></span>|<span data-ttu-id="9ebdc-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="9ebdc-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="9ebdc-112">Description</span><span class="sxs-lookup"><span data-stu-id="9ebdc-112">Description</span></span>  
 <span data-ttu-id="9ebdc-113">Indique qu’un TransactionContextWorkItem a été planifié.</span><span class="sxs-lookup"><span data-stu-id="9ebdc-113">Indicates a TransactionContextWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="9ebdc-114">Message</span><span class="sxs-lookup"><span data-stu-id="9ebdc-114">Message</span></span>  
 <span data-ttu-id="9ebdc-115">TransactionContextWorkItem a été planifié pour l'activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="9ebdc-115">A TransactionContextWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="9ebdc-116">Détails</span><span class="sxs-lookup"><span data-stu-id="9ebdc-116">Details</span></span>  
  
|<span data-ttu-id="9ebdc-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="9ebdc-117">Data Item Name</span></span>|<span data-ttu-id="9ebdc-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="9ebdc-118">Data Item Type</span></span>|<span data-ttu-id="9ebdc-119">Description</span><span class="sxs-lookup"><span data-stu-id="9ebdc-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="9ebdc-120">Activité</span><span class="sxs-lookup"><span data-stu-id="9ebdc-120">Activity</span></span>|<span data-ttu-id="9ebdc-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ebdc-121">xs:string</span></span>|<span data-ttu-id="9ebdc-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="9ebdc-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="9ebdc-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="9ebdc-123">DisplayName</span></span>|<span data-ttu-id="9ebdc-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ebdc-124">xs:string</span></span>|<span data-ttu-id="9ebdc-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="9ebdc-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="9ebdc-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="9ebdc-126">InstanceId</span></span>|<span data-ttu-id="9ebdc-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ebdc-127">xs:string</span></span>|<span data-ttu-id="9ebdc-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="9ebdc-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="9ebdc-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="9ebdc-129">AppDomain</span></span>|<span data-ttu-id="9ebdc-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ebdc-130">xs:string</span></span>|<span data-ttu-id="9ebdc-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="9ebdc-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
