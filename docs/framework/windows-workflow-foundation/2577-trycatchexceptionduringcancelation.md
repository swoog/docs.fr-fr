---
title: 2577 - TryCatchExceptionDuringCancelation
ms.date: 03/30/2017
ms.assetid: 35ee9f55-227f-4566-bcb4-4c7c75dea85b
ms.openlocfilehash: c272dd91249dfc90e6f4c38a7339919a5a6446e5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33510722"
---
# <a name="2577---trycatchexceptionduringcancelation"></a><span data-ttu-id="e51bb-102">2577 - TryCatchExceptionDuringCancelation</span><span class="sxs-lookup"><span data-stu-id="e51bb-102">2577 - TryCatchExceptionDuringCancelation</span></span>
## <a name="properties"></a><span data-ttu-id="e51bb-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e51bb-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="e51bb-104">ID</span><span class="sxs-lookup"><span data-stu-id="e51bb-104">ID</span></span>|<span data-ttu-id="e51bb-105">2577</span><span class="sxs-lookup"><span data-stu-id="e51bb-105">2577</span></span>|  
|<span data-ttu-id="e51bb-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e51bb-106">Keywords</span></span>|<span data-ttu-id="e51bb-107">WFActivities</span><span class="sxs-lookup"><span data-stu-id="e51bb-107">WFActivities</span></span>|  
|<span data-ttu-id="e51bb-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="e51bb-108">Level</span></span>|<span data-ttu-id="e51bb-109">Avertissement</span><span class="sxs-lookup"><span data-stu-id="e51bb-109">Warning</span></span>|  
|<span data-ttu-id="e51bb-110">Canal</span><span class="sxs-lookup"><span data-stu-id="e51bb-110">Channel</span></span>|<span data-ttu-id="e51bb-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="e51bb-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="e51bb-112">Description</span><span class="sxs-lookup"><span data-stu-id="e51bb-112">Description</span></span>  
 <span data-ttu-id="e51bb-113">Indique qu'une activité enfant de l'activité TryCatch a levé une exception durant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="e51bb-113">Indicates a child activity of the TryCatch activity has thrown an exception during cancelation.</span></span>  
  
## <a name="message"></a><span data-ttu-id="e51bb-114">Message</span><span class="sxs-lookup"><span data-stu-id="e51bb-114">Message</span></span>  
 <span data-ttu-id="e51bb-115">Une activité enfant de l'activité TryCatch « %1 » a levé une exception durant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="e51bb-115">A child activity of the TryCatch activity '%1' has thrown an exception during cancelation.</span></span>  
  
## <a name="details"></a><span data-ttu-id="e51bb-116">Détails</span><span class="sxs-lookup"><span data-stu-id="e51bb-116">Details</span></span>  
  
|<span data-ttu-id="e51bb-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="e51bb-117">Data Item Name</span></span>|<span data-ttu-id="e51bb-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="e51bb-118">Data Item Type</span></span>|<span data-ttu-id="e51bb-119">Description</span><span class="sxs-lookup"><span data-stu-id="e51bb-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="e51bb-120">DisplayName</span><span class="sxs-lookup"><span data-stu-id="e51bb-120">DisplayName</span></span>|<span data-ttu-id="e51bb-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="e51bb-121">xs:string</span></span>|<span data-ttu-id="e51bb-122">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="e51bb-122">The display name of the activity.</span></span>|  
|<span data-ttu-id="e51bb-123">AppDomain</span><span class="sxs-lookup"><span data-stu-id="e51bb-123">AppDomain</span></span>|<span data-ttu-id="e51bb-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="e51bb-124">xs:string</span></span>|<span data-ttu-id="e51bb-125">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="e51bb-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
