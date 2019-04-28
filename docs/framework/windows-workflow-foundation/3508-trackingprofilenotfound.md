---
title: 3508 - TrackingProfileNotFound
ms.date: 03/30/2017
ms.assetid: 4cee3c4a-0490-4c94-aa19-ef7ce7287c02
ms.openlocfilehash: 94c7ce231df241778f7c6ec5fe5998eae364750d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61755569"
---
# <a name="3508---trackingprofilenotfound"></a><span data-ttu-id="2841f-102">3508 - TrackingProfileNotFound</span><span class="sxs-lookup"><span data-stu-id="2841f-102">3508 - TrackingProfileNotFound</span></span>
## <a name="properties"></a><span data-ttu-id="2841f-103">Properties</span><span class="sxs-lookup"><span data-stu-id="2841f-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="2841f-104">Id</span><span class="sxs-lookup"><span data-stu-id="2841f-104">ID</span></span>|<span data-ttu-id="2841f-105">3508</span><span class="sxs-lookup"><span data-stu-id="2841f-105">3508</span></span>|  
|<span data-ttu-id="2841f-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="2841f-106">Keywords</span></span>|<span data-ttu-id="2841f-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="2841f-107">WFServices</span></span>|  
|<span data-ttu-id="2841f-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="2841f-108">Level</span></span>|<span data-ttu-id="2841f-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="2841f-109">Verbose</span></span>|  
|<span data-ttu-id="2841f-110">Canal</span><span class="sxs-lookup"><span data-stu-id="2841f-110">Channel</span></span>|<span data-ttu-id="2841f-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="2841f-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="2841f-112">Description</span><span class="sxs-lookup"><span data-stu-id="2841f-112">Description</span></span>  
 <span data-ttu-id="2841f-113">Indique si un TrackingProfile est introuvable dans le fichier de configuration ou un ActivityDefinitionId ne correspond pas au modèle.</span><span class="sxs-lookup"><span data-stu-id="2841f-113">Indicates either a TrackingProfile is not found in the config file or the ActivityDefinitionId does not match the profile.</span></span>  
  
## <a name="message"></a><span data-ttu-id="2841f-114">Message</span><span class="sxs-lookup"><span data-stu-id="2841f-114">Message</span></span>  
 <span data-ttu-id="2841f-115">TrackingProfile « %1 » pour le ActivityDefinitionId « %2 » introuvable.</span><span class="sxs-lookup"><span data-stu-id="2841f-115">TrackingProfile '%1' for the ActivityDefinitionId '%2' not found.</span></span> <span data-ttu-id="2841f-116">TrackingProfile est introuvable dans le fichier de configuration ou ActivityDefinitionId ne correspond pas.</span><span class="sxs-lookup"><span data-stu-id="2841f-116">Either the TrackingProfile is not found in the config file or the ActivityDefinitionId does not match.</span></span>  
  
## <a name="details"></a><span data-ttu-id="2841f-117">Détails</span><span class="sxs-lookup"><span data-stu-id="2841f-117">Details</span></span>  
  
|<span data-ttu-id="2841f-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="2841f-118">Data Item Name</span></span>|<span data-ttu-id="2841f-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="2841f-119">Data Item Type</span></span>|<span data-ttu-id="2841f-120">Description</span><span class="sxs-lookup"><span data-stu-id="2841f-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="2841f-121">TrackingProfile</span><span class="sxs-lookup"><span data-stu-id="2841f-121">TrackingProfile</span></span>|<span data-ttu-id="2841f-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="2841f-122">xs:string</span></span>|<span data-ttu-id="2841f-123">Nom du modèle de suivi.</span><span class="sxs-lookup"><span data-stu-id="2841f-123">The name of the tracking profile.</span></span>|  
|<span data-ttu-id="2841f-124">ActivityDefinitionId</span><span class="sxs-lookup"><span data-stu-id="2841f-124">ActivityDefinitionId</span></span>|<span data-ttu-id="2841f-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="2841f-125">xs:string</span></span>|<span data-ttu-id="2841f-126">ID de définition d'activité.</span><span class="sxs-lookup"><span data-stu-id="2841f-126">The activity definition id.</span></span>|  
|<span data-ttu-id="2841f-127">AppDomain</span><span class="sxs-lookup"><span data-stu-id="2841f-127">AppDomain</span></span>|<span data-ttu-id="2841f-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="2841f-128">xs:string</span></span>|<span data-ttu-id="2841f-129">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="2841f-129">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
