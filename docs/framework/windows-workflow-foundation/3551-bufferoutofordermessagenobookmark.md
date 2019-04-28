---
title: 3551 - BufferOutOfOrderMessageNoBookmark
ms.date: 03/30/2017
ms.assetid: 7930d6c4-c843-4a83-933a-cecd71b80d1e
ms.openlocfilehash: 89643edde5856688c762b0cf0d188bd4e7ba8a24
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61755530"
---
# <a name="3551---bufferoutofordermessagenobookmark"></a><span data-ttu-id="e0c6b-102">3551 - BufferOutOfOrderMessageNoBookmark</span><span class="sxs-lookup"><span data-stu-id="e0c6b-102">3551 - BufferOutOfOrderMessageNoBookmark</span></span>
## <a name="properties"></a><span data-ttu-id="e0c6b-103">Properties</span><span class="sxs-lookup"><span data-stu-id="e0c6b-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="e0c6b-104">Id</span><span class="sxs-lookup"><span data-stu-id="e0c6b-104">ID</span></span>|<span data-ttu-id="e0c6b-105">3551</span><span class="sxs-lookup"><span data-stu-id="e0c6b-105">3551</span></span>|  
|<span data-ttu-id="e0c6b-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e0c6b-106">Keywords</span></span>|<span data-ttu-id="e0c6b-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="e0c6b-107">WFServices</span></span>|  
|<span data-ttu-id="e0c6b-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="e0c6b-108">Level</span></span>|<span data-ttu-id="e0c6b-109">Information</span><span class="sxs-lookup"><span data-stu-id="e0c6b-109">Information</span></span>|  
|<span data-ttu-id="e0c6b-110">Canal</span><span class="sxs-lookup"><span data-stu-id="e0c6b-110">Channel</span></span>|<span data-ttu-id="e0c6b-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="e0c6b-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="e0c6b-112">Description</span><span class="sxs-lookup"><span data-stu-id="e0c6b-112">Description</span></span>  
 <span data-ttu-id="e0c6b-113">Indique qu'une reprise de signet a échoué.</span><span class="sxs-lookup"><span data-stu-id="e0c6b-113">Indicates a bookmark resumption has failed.</span></span> <span data-ttu-id="e0c6b-114">Une autre tentative d'opération de réception en mémoire tampon sera faite lorsque l'instance de service sera prête à traiter cette opération.</span><span class="sxs-lookup"><span data-stu-id="e0c6b-114">The buffered receive operation will be attempted again when the service instance is ready to process this particular operation.</span></span>  
  
## <a name="message"></a><span data-ttu-id="e0c6b-115">Message</span><span class="sxs-lookup"><span data-stu-id="e0c6b-115">Message</span></span>  
 <span data-ttu-id="e0c6b-116">Impossible d'effectuer actuellement l'opération « %2 » sur l'instance de service « %1 ».</span><span class="sxs-lookup"><span data-stu-id="e0c6b-116">Operation '%2' on service instance '%1' cannot be performed at this time.</span></span> <span data-ttu-id="e0c6b-117">Une autre tentative sera faite lorsque l'instance de service sera prête à traiter cette opération.</span><span class="sxs-lookup"><span data-stu-id="e0c6b-117">Another attempt will be made when the service instance is ready to process this particular operation.</span></span>  
  
## <a name="details"></a><span data-ttu-id="e0c6b-118">Détails</span><span class="sxs-lookup"><span data-stu-id="e0c6b-118">Details</span></span>  
  
|<span data-ttu-id="e0c6b-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="e0c6b-119">Data Item Name</span></span>|<span data-ttu-id="e0c6b-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="e0c6b-120">Data Item Type</span></span>|<span data-ttu-id="e0c6b-121">Description</span><span class="sxs-lookup"><span data-stu-id="e0c6b-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="e0c6b-122">OperationName</span><span class="sxs-lookup"><span data-stu-id="e0c6b-122">OperationName</span></span>|<span data-ttu-id="e0c6b-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="e0c6b-123">xs:string</span></span>|<span data-ttu-id="e0c6b-124">Nom de l'opération.</span><span class="sxs-lookup"><span data-stu-id="e0c6b-124">The name of the operation.</span></span>|  
|<span data-ttu-id="e0c6b-125">ServiceInstanceId</span><span class="sxs-lookup"><span data-stu-id="e0c6b-125">ServiceInstanceId</span></span>|<span data-ttu-id="e0c6b-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="e0c6b-126">xs:string</span></span>|<span data-ttu-id="e0c6b-127">ID de l'instance du service.</span><span class="sxs-lookup"><span data-stu-id="e0c6b-127">The id of the service instance.</span></span>|  
|<span data-ttu-id="e0c6b-128">AppDomain</span><span class="sxs-lookup"><span data-stu-id="e0c6b-128">AppDomain</span></span>|<span data-ttu-id="e0c6b-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="e0c6b-129">xs:string</span></span>|<span data-ttu-id="e0c6b-130">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="e0c6b-130">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
