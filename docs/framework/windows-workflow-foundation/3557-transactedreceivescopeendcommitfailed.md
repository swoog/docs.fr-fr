---
title: 3557 - TransactedReceiveScopeEndCommitFailed
ms.date: 03/30/2017
ms.assetid: 079f0188-8146-49ee-b6ae-a08f4e4d2b9b
ms.openlocfilehash: 444fa2e51322edd793f709fd3f92c5f9fe826522
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774450"
---
# <a name="3557---transactedreceivescopeendcommitfailed"></a><span data-ttu-id="bb3d4-102">3557 - TransactedReceiveScopeEndCommitFailed</span><span class="sxs-lookup"><span data-stu-id="bb3d4-102">3557 - TransactedReceiveScopeEndCommitFailed</span></span>
## <a name="properties"></a><span data-ttu-id="bb3d4-103">Properties</span><span class="sxs-lookup"><span data-stu-id="bb3d4-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="bb3d4-104">Id</span><span class="sxs-lookup"><span data-stu-id="bb3d4-104">ID</span></span>|<span data-ttu-id="bb3d4-105">3557</span><span class="sxs-lookup"><span data-stu-id="bb3d4-105">3557</span></span>|  
|<span data-ttu-id="bb3d4-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="bb3d4-106">Keywords</span></span>|<span data-ttu-id="bb3d4-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="bb3d4-107">WFServices</span></span>|  
|<span data-ttu-id="bb3d4-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="bb3d4-108">Level</span></span>|<span data-ttu-id="bb3d4-109">Information</span><span class="sxs-lookup"><span data-stu-id="bb3d4-109">Information</span></span>|  
|<span data-ttu-id="bb3d4-110">Canal</span><span class="sxs-lookup"><span data-stu-id="bb3d4-110">Channel</span></span>|<span data-ttu-id="bb3d4-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="bb3d4-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="bb3d4-112">Description</span><span class="sxs-lookup"><span data-stu-id="bb3d4-112">Description</span></span>  
 <span data-ttu-id="bb3d4-113">Indique que l'appel à EndCommit sur un CommittableTransaction a levé une exception TransactionException.</span><span class="sxs-lookup"><span data-stu-id="bb3d4-113">Indicates the call to EndCommit on a CommittableTransaction threw a TransactionException.</span></span>  
  
## <a name="message"></a><span data-ttu-id="bb3d4-114">Message</span><span class="sxs-lookup"><span data-stu-id="bb3d4-114">Message</span></span>  
 <span data-ttu-id="bb3d4-115">L'appel à EndCommit sur le CommittableTransaction avec l'ID = « %1 » a levé un TransactionException avec le message suivant : « %2 ».</span><span class="sxs-lookup"><span data-stu-id="bb3d4-115">The call to EndCommit on the CommittableTransaction with id = '%1' threw a TransactionException with the following message: '%2'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="bb3d4-116">Détails</span><span class="sxs-lookup"><span data-stu-id="bb3d4-116">Details</span></span>  
  
|<span data-ttu-id="bb3d4-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="bb3d4-117">Data Item Name</span></span>|<span data-ttu-id="bb3d4-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="bb3d4-118">Data Item Type</span></span>|<span data-ttu-id="bb3d4-119">Description</span><span class="sxs-lookup"><span data-stu-id="bb3d4-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="bb3d4-120">TransactionId</span><span class="sxs-lookup"><span data-stu-id="bb3d4-120">TransactionId</span></span>|<span data-ttu-id="bb3d4-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="bb3d4-121">xs:string</span></span>|<span data-ttu-id="bb3d4-122">ID de CommittableTransaction.</span><span class="sxs-lookup"><span data-stu-id="bb3d4-122">The id of the CommittableTransaction.</span></span>|  
|<span data-ttu-id="bb3d4-123">Exception</span><span class="sxs-lookup"><span data-stu-id="bb3d4-123">Exception</span></span>|<span data-ttu-id="bb3d4-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="bb3d4-124">xs:string</span></span>|<span data-ttu-id="bb3d4-125">Détails de l'exception</span><span class="sxs-lookup"><span data-stu-id="bb3d4-125">The exception details for the exception</span></span>|  
|<span data-ttu-id="bb3d4-126">AppDomain</span><span class="sxs-lookup"><span data-stu-id="bb3d4-126">AppDomain</span></span>|<span data-ttu-id="bb3d4-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="bb3d4-127">xs:string</span></span>|<span data-ttu-id="bb3d4-128">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="bb3d4-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
