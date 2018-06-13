---
title: 3508 - TrackingProfileNotFound
ms.date: 03/30/2017
ms.assetid: 4cee3c4a-0490-4c94-aa19-ef7ce7287c02
ms.openlocfilehash: 94c7ce231df241778f7c6ec5fe5998eae364750d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33512182"
---
# <a name="3508---trackingprofilenotfound"></a><span data-ttu-id="4150c-102">3508 - TrackingProfileNotFound</span><span class="sxs-lookup"><span data-stu-id="4150c-102">3508 - TrackingProfileNotFound</span></span>
## <a name="properties"></a><span data-ttu-id="4150c-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4150c-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="4150c-104">ID</span><span class="sxs-lookup"><span data-stu-id="4150c-104">ID</span></span>|<span data-ttu-id="4150c-105">3508</span><span class="sxs-lookup"><span data-stu-id="4150c-105">3508</span></span>|  
|<span data-ttu-id="4150c-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4150c-106">Keywords</span></span>|<span data-ttu-id="4150c-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="4150c-107">WFServices</span></span>|  
|<span data-ttu-id="4150c-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="4150c-108">Level</span></span>|<span data-ttu-id="4150c-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="4150c-109">Verbose</span></span>|  
|<span data-ttu-id="4150c-110">Canal</span><span class="sxs-lookup"><span data-stu-id="4150c-110">Channel</span></span>|<span data-ttu-id="4150c-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="4150c-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="4150c-112">Description</span><span class="sxs-lookup"><span data-stu-id="4150c-112">Description</span></span>  
 <span data-ttu-id="4150c-113">Indique si un TrackingProfile est introuvable dans le fichier de configuration ou un ActivityDefinitionId ne correspond pas au modèle.</span><span class="sxs-lookup"><span data-stu-id="4150c-113">Indicates either a TrackingProfile is not found in the config file or the ActivityDefinitionId does not match the profile.</span></span>  
  
## <a name="message"></a><span data-ttu-id="4150c-114">Message</span><span class="sxs-lookup"><span data-stu-id="4150c-114">Message</span></span>  
 <span data-ttu-id="4150c-115">TrackingProfile « %1 » pour le ActivityDefinitionId « %2 » introuvable.</span><span class="sxs-lookup"><span data-stu-id="4150c-115">TrackingProfile '%1' for the ActivityDefinitionId '%2' not found.</span></span> <span data-ttu-id="4150c-116">TrackingProfile est introuvable dans le fichier de configuration ou ActivityDefinitionId ne correspond pas.</span><span class="sxs-lookup"><span data-stu-id="4150c-116">Either the TrackingProfile is not found in the config file or the ActivityDefinitionId does not match.</span></span>  
  
## <a name="details"></a><span data-ttu-id="4150c-117">Détails</span><span class="sxs-lookup"><span data-stu-id="4150c-117">Details</span></span>  
  
|<span data-ttu-id="4150c-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="4150c-118">Data Item Name</span></span>|<span data-ttu-id="4150c-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="4150c-119">Data Item Type</span></span>|<span data-ttu-id="4150c-120">Description</span><span class="sxs-lookup"><span data-stu-id="4150c-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="4150c-121">TrackingProfile</span><span class="sxs-lookup"><span data-stu-id="4150c-121">TrackingProfile</span></span>|<span data-ttu-id="4150c-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="4150c-122">xs:string</span></span>|<span data-ttu-id="4150c-123">Nom du modèle de suivi.</span><span class="sxs-lookup"><span data-stu-id="4150c-123">The name of the tracking profile.</span></span>|  
|<span data-ttu-id="4150c-124">ActivityDefinitionId</span><span class="sxs-lookup"><span data-stu-id="4150c-124">ActivityDefinitionId</span></span>|<span data-ttu-id="4150c-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="4150c-125">xs:string</span></span>|<span data-ttu-id="4150c-126">ID de définition d'activité.</span><span class="sxs-lookup"><span data-stu-id="4150c-126">The activity definition id.</span></span>|  
|<span data-ttu-id="4150c-127">AppDomain</span><span class="sxs-lookup"><span data-stu-id="4150c-127">AppDomain</span></span>|<span data-ttu-id="4150c-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="4150c-128">xs:string</span></span>|<span data-ttu-id="4150c-129">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="4150c-129">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
