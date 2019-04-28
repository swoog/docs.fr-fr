---
title: 1018 - StartCancelActivityWorkItem
ms.date: 03/30/2017
ms.assetid: 68b4fa1d-eee6-4a2a-8c16-7e9d89f08ab9
ms.openlocfilehash: 8d7045b0a7f31ecfd5dd90f319192bd202804353
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62008861"
---
# <a name="1018---startcancelactivityworkitem"></a><span data-ttu-id="5d96f-102">1018 - StartCancelActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="5d96f-102">1018 - StartCancelActivityWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="5d96f-103">Properties</span><span class="sxs-lookup"><span data-stu-id="5d96f-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="5d96f-104">Id</span><span class="sxs-lookup"><span data-stu-id="5d96f-104">ID</span></span>|<span data-ttu-id="5d96f-105">1018</span><span class="sxs-lookup"><span data-stu-id="5d96f-105">1018</span></span>|  
|<span data-ttu-id="5d96f-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="5d96f-106">Keywords</span></span>|<span data-ttu-id="5d96f-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="5d96f-107">WFRuntime</span></span>|  
|<span data-ttu-id="5d96f-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="5d96f-108">Level</span></span>|<span data-ttu-id="5d96f-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="5d96f-109">Verbose</span></span>|  
|<span data-ttu-id="5d96f-110">Canal</span><span class="sxs-lookup"><span data-stu-id="5d96f-110">Channel</span></span>|<span data-ttu-id="5d96f-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="5d96f-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="5d96f-112">Description</span><span class="sxs-lookup"><span data-stu-id="5d96f-112">Description</span></span>  
 <span data-ttu-id="5d96f-113">Indique qu'un CancelActivityWorkItem démarre l'exécution.</span><span class="sxs-lookup"><span data-stu-id="5d96f-113">Indicates a CancelActivityWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="5d96f-114">Message</span><span class="sxs-lookup"><span data-stu-id="5d96f-114">Message</span></span>  
 <span data-ttu-id="5d96f-115">Début de l'exécution d'un CancelActivityWorkItem pour l'activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="5d96f-115">Starting execution of a CancelActivityWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="5d96f-116">Détails</span><span class="sxs-lookup"><span data-stu-id="5d96f-116">Details</span></span>  
  
|<span data-ttu-id="5d96f-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="5d96f-117">Data Item Name</span></span>|<span data-ttu-id="5d96f-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="5d96f-118">Data Item Type</span></span>|<span data-ttu-id="5d96f-119">Description</span><span class="sxs-lookup"><span data-stu-id="5d96f-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="5d96f-120">Activité</span><span class="sxs-lookup"><span data-stu-id="5d96f-120">Activity</span></span>|<span data-ttu-id="5d96f-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="5d96f-121">xs:string</span></span>|<span data-ttu-id="5d96f-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="5d96f-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="5d96f-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="5d96f-123">DisplayName</span></span>|<span data-ttu-id="5d96f-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="5d96f-124">xs:string</span></span>|<span data-ttu-id="5d96f-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="5d96f-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="5d96f-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="5d96f-126">InstanceId</span></span>|<span data-ttu-id="5d96f-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="5d96f-127">xs:string</span></span>|<span data-ttu-id="5d96f-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="5d96f-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="5d96f-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="5d96f-129">AppDomain</span></span>|<span data-ttu-id="5d96f-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="5d96f-130">xs:string</span></span>|<span data-ttu-id="5d96f-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="5d96f-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
