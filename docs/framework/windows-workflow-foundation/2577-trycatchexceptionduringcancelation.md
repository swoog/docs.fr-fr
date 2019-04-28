---
title: 2577 - TryCatchExceptionDuringCancelation
ms.date: 03/30/2017
ms.assetid: 35ee9f55-227f-4566-bcb4-4c7c75dea85b
ms.openlocfilehash: c272dd91249dfc90e6f4c38a7339919a5a6446e5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61755621"
---
# <a name="2577---trycatchexceptionduringcancelation"></a><span data-ttu-id="44423-102">2577 - TryCatchExceptionDuringCancelation</span><span class="sxs-lookup"><span data-stu-id="44423-102">2577 - TryCatchExceptionDuringCancelation</span></span>
## <a name="properties"></a><span data-ttu-id="44423-103">Properties</span><span class="sxs-lookup"><span data-stu-id="44423-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="44423-104">Id</span><span class="sxs-lookup"><span data-stu-id="44423-104">ID</span></span>|<span data-ttu-id="44423-105">2577</span><span class="sxs-lookup"><span data-stu-id="44423-105">2577</span></span>|  
|<span data-ttu-id="44423-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="44423-106">Keywords</span></span>|<span data-ttu-id="44423-107">WFActivities</span><span class="sxs-lookup"><span data-stu-id="44423-107">WFActivities</span></span>|  
|<span data-ttu-id="44423-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="44423-108">Level</span></span>|<span data-ttu-id="44423-109">Warning</span><span class="sxs-lookup"><span data-stu-id="44423-109">Warning</span></span>|  
|<span data-ttu-id="44423-110">Canal</span><span class="sxs-lookup"><span data-stu-id="44423-110">Channel</span></span>|<span data-ttu-id="44423-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="44423-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="44423-112">Description</span><span class="sxs-lookup"><span data-stu-id="44423-112">Description</span></span>  
 <span data-ttu-id="44423-113">Indique qu'une activité enfant de l'activité TryCatch a levé une exception durant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="44423-113">Indicates a child activity of the TryCatch activity has thrown an exception during cancelation.</span></span>  
  
## <a name="message"></a><span data-ttu-id="44423-114">Message</span><span class="sxs-lookup"><span data-stu-id="44423-114">Message</span></span>  
 <span data-ttu-id="44423-115">Une activité enfant de l'activité TryCatch « %1 » a levé une exception durant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="44423-115">A child activity of the TryCatch activity '%1' has thrown an exception during cancelation.</span></span>  
  
## <a name="details"></a><span data-ttu-id="44423-116">Détails</span><span class="sxs-lookup"><span data-stu-id="44423-116">Details</span></span>  
  
|<span data-ttu-id="44423-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="44423-117">Data Item Name</span></span>|<span data-ttu-id="44423-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="44423-118">Data Item Type</span></span>|<span data-ttu-id="44423-119">Description</span><span class="sxs-lookup"><span data-stu-id="44423-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="44423-120">DisplayName</span><span class="sxs-lookup"><span data-stu-id="44423-120">DisplayName</span></span>|<span data-ttu-id="44423-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="44423-121">xs:string</span></span>|<span data-ttu-id="44423-122">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="44423-122">The display name of the activity.</span></span>|  
|<span data-ttu-id="44423-123">AppDomain</span><span class="sxs-lookup"><span data-stu-id="44423-123">AppDomain</span></span>|<span data-ttu-id="44423-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="44423-124">xs:string</span></span>|<span data-ttu-id="44423-125">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="44423-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
