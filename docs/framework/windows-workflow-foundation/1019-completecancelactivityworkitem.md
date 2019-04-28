---
title: 1019 - CompleteCancelActivityWorkItem
ms.date: 03/30/2017
ms.assetid: 75a4a1ab-e5a3-4f4e-88e4-d19806e671d7
ms.openlocfilehash: 28d19742055c51ca94c36ffddf15dced7dfc14cf
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924434"
---
# <a name="1019---completecancelactivityworkitem"></a><span data-ttu-id="31a72-102">1019 - CompleteCancelActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="31a72-102">1019 - CompleteCancelActivityWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="31a72-103">Properties</span><span class="sxs-lookup"><span data-stu-id="31a72-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="31a72-104">Id</span><span class="sxs-lookup"><span data-stu-id="31a72-104">ID</span></span>|<span data-ttu-id="31a72-105">1019</span><span class="sxs-lookup"><span data-stu-id="31a72-105">1019</span></span>|  
|<span data-ttu-id="31a72-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="31a72-106">Keywords</span></span>|<span data-ttu-id="31a72-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="31a72-107">WFRuntime</span></span>|  
|<span data-ttu-id="31a72-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="31a72-108">Level</span></span>|<span data-ttu-id="31a72-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="31a72-109">Verbose</span></span>|  
|<span data-ttu-id="31a72-110">Canal</span><span class="sxs-lookup"><span data-stu-id="31a72-110">Channel</span></span>|<span data-ttu-id="31a72-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="31a72-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="31a72-112">Description</span><span class="sxs-lookup"><span data-stu-id="31a72-112">Description</span></span>  
 <span data-ttu-id="31a72-113">Indique qu'un CancelActivityWorkItem est terminé.</span><span class="sxs-lookup"><span data-stu-id="31a72-113">Indicates a CancelActivityWorkItem has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="31a72-114">Message</span><span class="sxs-lookup"><span data-stu-id="31a72-114">Message</span></span>  
 <span data-ttu-id="31a72-115">CancelActivityWorkItem est terminé pour l'activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="31a72-115">A CancelActivityWorkItem has completed for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="31a72-116">Détails</span><span class="sxs-lookup"><span data-stu-id="31a72-116">Details</span></span>  
  
|<span data-ttu-id="31a72-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="31a72-117">Data Item Name</span></span>|<span data-ttu-id="31a72-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="31a72-118">Data Item Type</span></span>|<span data-ttu-id="31a72-119">Description</span><span class="sxs-lookup"><span data-stu-id="31a72-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="31a72-120">Activité</span><span class="sxs-lookup"><span data-stu-id="31a72-120">Activity</span></span>|<span data-ttu-id="31a72-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="31a72-121">xs:string</span></span>|<span data-ttu-id="31a72-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="31a72-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="31a72-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="31a72-123">DisplayName</span></span>|<span data-ttu-id="31a72-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="31a72-124">xs:string</span></span>|<span data-ttu-id="31a72-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="31a72-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="31a72-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="31a72-126">InstanceId</span></span>|<span data-ttu-id="31a72-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="31a72-127">xs:string</span></span>|<span data-ttu-id="31a72-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="31a72-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="31a72-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="31a72-129">AppDomain</span></span>|<span data-ttu-id="31a72-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="31a72-130">xs:string</span></span>|<span data-ttu-id="31a72-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="31a72-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
