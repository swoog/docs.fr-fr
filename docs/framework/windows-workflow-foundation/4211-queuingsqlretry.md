---
title: 4211 - QueuingSqlRetry
ms.date: 03/30/2017
ms.assetid: df569f88-c86b-4503-840d-1399b67f4df7
ms.openlocfilehash: ede74eb642c5c2c79b90cf1458db424d9f83b087
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774242"
---
# <a name="4211---queuingsqlretry"></a><span data-ttu-id="958ad-102">4211 - QueuingSqlRetry</span><span class="sxs-lookup"><span data-stu-id="958ad-102">4211 - QueuingSqlRetry</span></span>
## <a name="properties"></a><span data-ttu-id="958ad-103">Properties</span><span class="sxs-lookup"><span data-stu-id="958ad-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="958ad-104">Id</span><span class="sxs-lookup"><span data-stu-id="958ad-104">ID</span></span>|<span data-ttu-id="958ad-105">4211</span><span class="sxs-lookup"><span data-stu-id="958ad-105">4211</span></span>|  
|<span data-ttu-id="958ad-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="958ad-106">Keywords</span></span>|<span data-ttu-id="958ad-107">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="958ad-107">WFInstanceStore</span></span>|  
|<span data-ttu-id="958ad-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="958ad-108">Level</span></span>|<span data-ttu-id="958ad-109">Warning</span><span class="sxs-lookup"><span data-stu-id="958ad-109">Warning</span></span>|  
|<span data-ttu-id="958ad-110">Canal</span><span class="sxs-lookup"><span data-stu-id="958ad-110">Channel</span></span>|<span data-ttu-id="958ad-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="958ad-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="958ad-112">Description</span><span class="sxs-lookup"><span data-stu-id="958ad-112">Description</span></span>  
 <span data-ttu-id="958ad-113">Indique une nouvelle tentative de mise en file d'attente SQL.</span><span class="sxs-lookup"><span data-stu-id="958ad-113">Indicates queuing SQL retry.</span></span>  
  
## <a name="message"></a><span data-ttu-id="958ad-114">Message</span><span class="sxs-lookup"><span data-stu-id="958ad-114">Message</span></span>  
 <span data-ttu-id="958ad-115">Mise en file d'attente d'une tentative SQL avec un retard de %1 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="958ad-115">Queuing SQL retry with delay %1 milliseconds.</span></span>  
  
## <a name="details"></a><span data-ttu-id="958ad-116">Détails</span><span class="sxs-lookup"><span data-stu-id="958ad-116">Details</span></span>  
  
|<span data-ttu-id="958ad-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="958ad-117">Data Item Name</span></span>|<span data-ttu-id="958ad-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="958ad-118">Data Item Type</span></span>|<span data-ttu-id="958ad-119">Description</span><span class="sxs-lookup"><span data-stu-id="958ad-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="958ad-120">Délai</span><span class="sxs-lookup"><span data-stu-id="958ad-120">Delay</span></span>|<span data-ttu-id="958ad-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="958ad-121">xs:string</span></span>|<span data-ttu-id="958ad-122">Délai entre les tentatives.</span><span class="sxs-lookup"><span data-stu-id="958ad-122">The delay between retries.</span></span>|  
|<span data-ttu-id="958ad-123">AppDomain</span><span class="sxs-lookup"><span data-stu-id="958ad-123">AppDomain</span></span>|<span data-ttu-id="958ad-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="958ad-124">xs:string</span></span>|<span data-ttu-id="958ad-125">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="958ad-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
