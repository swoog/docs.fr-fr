---
title: 1034 - CompleteRuntimeWorkItem
ms.date: 03/30/2017
ms.assetid: 45620011-8b04-4f87-ab5a-65b24145e17d
ms.openlocfilehash: bd49c608a8f6a6caab6975850507a00a2c0edb03
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33509689"
---
# <a name="1034---completeruntimeworkitem"></a><span data-ttu-id="ebfd5-102">1034 - CompleteRuntimeWorkItem</span><span class="sxs-lookup"><span data-stu-id="ebfd5-102">1034 - CompleteRuntimeWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="ebfd5-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ebfd5-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="ebfd5-104">ID</span><span class="sxs-lookup"><span data-stu-id="ebfd5-104">ID</span></span>|<span data-ttu-id="ebfd5-105">1034</span><span class="sxs-lookup"><span data-stu-id="ebfd5-105">1034</span></span>|  
|<span data-ttu-id="ebfd5-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="ebfd5-106">Keywords</span></span>|<span data-ttu-id="ebfd5-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="ebfd5-107">WFRuntime</span></span>|  
|<span data-ttu-id="ebfd5-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="ebfd5-108">Level</span></span>|<span data-ttu-id="ebfd5-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="ebfd5-109">Verbose</span></span>|  
|<span data-ttu-id="ebfd5-110">Canal</span><span class="sxs-lookup"><span data-stu-id="ebfd5-110">Channel</span></span>|<span data-ttu-id="ebfd5-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="ebfd5-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="ebfd5-112">Description</span><span class="sxs-lookup"><span data-stu-id="ebfd5-112">Description</span></span>  
 <span data-ttu-id="ebfd5-113">Indique qu'un RuntimeWorkItem est terminé.</span><span class="sxs-lookup"><span data-stu-id="ebfd5-113">Indicates a RuntimeWorkItem has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="ebfd5-114">Message</span><span class="sxs-lookup"><span data-stu-id="ebfd5-114">Message</span></span>  
 <span data-ttu-id="ebfd5-115">Un élément de travail runtime est terminé pour l'activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="ebfd5-115">A runtime work item has completed for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="ebfd5-116">Détails</span><span class="sxs-lookup"><span data-stu-id="ebfd5-116">Details</span></span>  
  
|<span data-ttu-id="ebfd5-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="ebfd5-117">Data Item Name</span></span>|<span data-ttu-id="ebfd5-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="ebfd5-118">Data Item Type</span></span>|<span data-ttu-id="ebfd5-119">Description</span><span class="sxs-lookup"><span data-stu-id="ebfd5-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="ebfd5-120">Activité</span><span class="sxs-lookup"><span data-stu-id="ebfd5-120">Activity</span></span>|<span data-ttu-id="ebfd5-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="ebfd5-121">xs:string</span></span>|<span data-ttu-id="ebfd5-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="ebfd5-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="ebfd5-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="ebfd5-123">DisplayName</span></span>|<span data-ttu-id="ebfd5-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="ebfd5-124">xs:string</span></span>|<span data-ttu-id="ebfd5-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="ebfd5-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="ebfd5-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="ebfd5-126">InstanceId</span></span>|<span data-ttu-id="ebfd5-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="ebfd5-127">xs:string</span></span>|<span data-ttu-id="ebfd5-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="ebfd5-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="ebfd5-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="ebfd5-129">AppDomain</span></span>|<span data-ttu-id="ebfd5-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="ebfd5-130">xs:string</span></span>|<span data-ttu-id="ebfd5-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="ebfd5-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
