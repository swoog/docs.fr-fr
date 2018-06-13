---
title: 1150 - CompensationState
ms.date: 03/30/2017
ms.assetid: eb015842-cc5a-47be-bce5-6af39e567723
ms.openlocfilehash: 61613a27c4d4d8fb0b206246fef25ae87def47a5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33510678"
---
# <a name="1150---compensationstate"></a><span data-ttu-id="f0765-102">1150 - CompensationState</span><span class="sxs-lookup"><span data-stu-id="f0765-102">1150 - CompensationState</span></span>
## <a name="properties"></a><span data-ttu-id="f0765-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f0765-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="f0765-104">ID</span><span class="sxs-lookup"><span data-stu-id="f0765-104">ID</span></span>|<span data-ttu-id="f0765-105">1150</span><span class="sxs-lookup"><span data-stu-id="f0765-105">1150</span></span>|  
|<span data-ttu-id="f0765-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f0765-106">Keywords</span></span>|<span data-ttu-id="f0765-107">WFActivities</span><span class="sxs-lookup"><span data-stu-id="f0765-107">WFActivities</span></span>|  
|<span data-ttu-id="f0765-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="f0765-108">Level</span></span>|<span data-ttu-id="f0765-109">Information</span><span class="sxs-lookup"><span data-stu-id="f0765-109">Information</span></span>|  
|<span data-ttu-id="f0765-110">Canal</span><span class="sxs-lookup"><span data-stu-id="f0765-110">Channel</span></span>|<span data-ttu-id="f0765-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="f0765-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="f0765-112">Description</span><span class="sxs-lookup"><span data-stu-id="f0765-112">Description</span></span>  
 <span data-ttu-id="f0765-113">Indique un changement d'état d'un CompensableActivity.</span><span class="sxs-lookup"><span data-stu-id="f0765-113">Indicates a change of state in a CompensableActivity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="f0765-114">Message</span><span class="sxs-lookup"><span data-stu-id="f0765-114">Message</span></span>  
 <span data-ttu-id="f0765-115">CompensableActivity « %1 » est dans l'état « %2 ».</span><span class="sxs-lookup"><span data-stu-id="f0765-115">CompensableActivity '%1' is in the '%2' state.</span></span>  
  
## <a name="details"></a><span data-ttu-id="f0765-116">Détails</span><span class="sxs-lookup"><span data-stu-id="f0765-116">Details</span></span>  
  
|<span data-ttu-id="f0765-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="f0765-117">Data Item Name</span></span>|<span data-ttu-id="f0765-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="f0765-118">Data Item Type</span></span>|<span data-ttu-id="f0765-119">Description</span><span class="sxs-lookup"><span data-stu-id="f0765-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="f0765-120">DisplayName</span><span class="sxs-lookup"><span data-stu-id="f0765-120">DisplayName</span></span>|<span data-ttu-id="f0765-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="f0765-121">xs:string</span></span>|<span data-ttu-id="f0765-122">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="f0765-122">The display name of the activity.</span></span>|  
|<span data-ttu-id="f0765-123">État</span><span class="sxs-lookup"><span data-stu-id="f0765-123">State</span></span>|<span data-ttu-id="f0765-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="f0765-124">xs:string</span></span>|<span data-ttu-id="f0765-125">État de compensation.</span><span class="sxs-lookup"><span data-stu-id="f0765-125">The compensation state.</span></span>|  
|<span data-ttu-id="f0765-126">AppDomain</span><span class="sxs-lookup"><span data-stu-id="f0765-126">AppDomain</span></span>|<span data-ttu-id="f0765-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="f0765-127">xs:string</span></span>|<span data-ttu-id="f0765-128">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="f0765-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
