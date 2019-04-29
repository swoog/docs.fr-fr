---
title: 39458 - TrackingRecordTruncated
ms.date: 03/30/2017
ms.assetid: 5352f0eb-d571-454a-bab5-e2162888b218
ms.openlocfilehash: 416feb4073b31178b016ae72c9cd85e15c4a68c3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774411"
---
# <a name="39458---trackingrecordtruncated"></a><span data-ttu-id="3c09c-102">39458 - TrackingRecordTruncated</span><span class="sxs-lookup"><span data-stu-id="3c09c-102">39458 - TrackingRecordTruncated</span></span>
## <a name="properties"></a><span data-ttu-id="3c09c-103">Properties</span><span class="sxs-lookup"><span data-stu-id="3c09c-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="3c09c-104">Id</span><span class="sxs-lookup"><span data-stu-id="3c09c-104">ID</span></span>|<span data-ttu-id="3c09c-105">39458</span><span class="sxs-lookup"><span data-stu-id="3c09c-105">39458</span></span>|  
|<span data-ttu-id="3c09c-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="3c09c-106">Keywords</span></span>|<span data-ttu-id="3c09c-107">WFTracking</span><span class="sxs-lookup"><span data-stu-id="3c09c-107">WFTracking</span></span>|  
|<span data-ttu-id="3c09c-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="3c09c-108">Level</span></span>|<span data-ttu-id="3c09c-109">Warning</span><span class="sxs-lookup"><span data-stu-id="3c09c-109">Warning</span></span>|  
|<span data-ttu-id="3c09c-110">Canal</span><span class="sxs-lookup"><span data-stu-id="3c09c-110">Channel</span></span>|<span data-ttu-id="3c09c-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="3c09c-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="3c09c-112">Description</span><span class="sxs-lookup"><span data-stu-id="3c09c-112">Description</span></span>  
 <span data-ttu-id="3c09c-113">Indique qu'un enregistrement de suivi a été tronqué.</span><span class="sxs-lookup"><span data-stu-id="3c09c-113">Indicates a tracking record has been truncated.</span></span> <span data-ttu-id="3c09c-114">Les données de variables/annotations/utilisateur ont été supprimées.</span><span class="sxs-lookup"><span data-stu-id="3c09c-114">Variables/annotations/user data have been removed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="3c09c-115">Message</span><span class="sxs-lookup"><span data-stu-id="3c09c-115">Message</span></span>  
 <span data-ttu-id="3c09c-116">Enregistrement de suivi %1 tronqué écrit dans la session ETW avec le fournisseur %2.</span><span class="sxs-lookup"><span data-stu-id="3c09c-116">Truncated tracking record %1 written to ETW session with provider %2.</span></span> <span data-ttu-id="3c09c-117">Les données de variables/annotations/utilisateur ont été supprimées</span><span class="sxs-lookup"><span data-stu-id="3c09c-117">Variables/annotations/user data have been removed</span></span>  
  
## <a name="details"></a><span data-ttu-id="3c09c-118">Détails</span><span class="sxs-lookup"><span data-stu-id="3c09c-118">Details</span></span>  
  
|<span data-ttu-id="3c09c-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="3c09c-119">Data Item Name</span></span>|<span data-ttu-id="3c09c-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="3c09c-120">Data Item Type</span></span>|<span data-ttu-id="3c09c-121">Description</span><span class="sxs-lookup"><span data-stu-id="3c09c-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="3c09c-122">RecordNumber</span><span class="sxs-lookup"><span data-stu-id="3c09c-122">RecordNumber</span></span>|<span data-ttu-id="3c09c-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="3c09c-123">xs:string</span></span>|<span data-ttu-id="3c09c-124">Numéro d'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="3c09c-124">The tracking record number.</span></span>|  
|<span data-ttu-id="3c09c-125">ProviderId</span><span class="sxs-lookup"><span data-stu-id="3c09c-125">ProviderId</span></span>|<span data-ttu-id="3c09c-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="3c09c-126">xs:string</span></span>|<span data-ttu-id="3c09c-127">ID du fournisseur ETW.</span><span class="sxs-lookup"><span data-stu-id="3c09c-127">The ETW provider id.</span></span>|  
|<span data-ttu-id="3c09c-128">AppDomain</span><span class="sxs-lookup"><span data-stu-id="3c09c-128">AppDomain</span></span>|<span data-ttu-id="3c09c-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="3c09c-129">xs:string</span></span>|<span data-ttu-id="3c09c-130">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="3c09c-130">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
