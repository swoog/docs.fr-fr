---
title: Événements ETW de conflit - .NET
ms.date: 03/30/2017
helpviewer_keywords:
- contention events [.NET Framework]
- ETW, contention events (CLR)
ms.assetid: 6933e753-2f2a-425b-ae84-42138c957d76
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 95f56a6c8b51c58ed36d5d0de428bf57b728009c
ms.sourcegitcommit: 5dcfeb59179e81071f54840d4902cbe00b184294
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54857643"
---
# <a name="contention-etw-events"></a><span data-ttu-id="f2a1f-102">Événements ETW de conflit</span><span class="sxs-lookup"><span data-stu-id="f2a1f-102">Contention ETW events</span></span>

<span data-ttu-id="f2a1f-103">Les événements de conflit sont déclenchés chaque fois qu’il existe un conflit sur les verrous <xref:System.Threading.Monitor?displayProperty=nameWithType> ou les verrous natifs utilisés par le runtime.</span><span class="sxs-lookup"><span data-stu-id="f2a1f-103">Contention events are raised whenever there is contention for <xref:System.Threading.Monitor?displayProperty=nameWithType> locks or native locks used by the runtime.</span></span> <span data-ttu-id="f2a1f-104">Le conflit se produit quand un thread attend un verrou alors qu’un autre thread possède ce verrou.</span><span class="sxs-lookup"><span data-stu-id="f2a1f-104">Contention occurs when a thread is waiting for a lock while another thread possesses the lock.</span></span>

<span data-ttu-id="f2a1f-105">Le tableau suivant montre le mot clé sous lequel les événements de conflit sont déclenchés, ainsi que le niveau des événements.</span><span class="sxs-lookup"><span data-stu-id="f2a1f-105">The following table shows the keyword under which contention events are raised, and the level of the events.</span></span> <span data-ttu-id="f2a1f-106">Pour plus d’informations, consultez [CLR ETW Keywords and Levels](clr-etw-keywords-and-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f2a1f-106">For more information, see [CLR ETW Keywords and Levels](clr-etw-keywords-and-levels.md).</span></span>

|<span data-ttu-id="f2a1f-107">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="f2a1f-107">Keyword for raising the event</span></span>|<span data-ttu-id="f2a1f-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="f2a1f-108">Level</span></span>|
|-----------------------------------|-----------|
|<span data-ttu-id="f2a1f-109">`ContentionKeyword` (0x4000)</span><span class="sxs-lookup"><span data-stu-id="f2a1f-109">`ContentionKeyword` (0x4000)</span></span>|<span data-ttu-id="f2a1f-110">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="f2a1f-110">Informational (4)</span></span>|

<span data-ttu-id="f2a1f-111">Le tableau suivant présente des informations sur les événements :</span><span class="sxs-lookup"><span data-stu-id="f2a1f-111">The following table shows event information:</span></span>

|<span data-ttu-id="f2a1f-112">Événement</span><span class="sxs-lookup"><span data-stu-id="f2a1f-112">Event</span></span>|<span data-ttu-id="f2a1f-113">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="f2a1f-113">Event ID</span></span>|<span data-ttu-id="f2a1f-114">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="f2a1f-114">Raised when</span></span>|
|-----------|--------------|-----------------|
|`ContentionStart_V1`|<span data-ttu-id="f2a1f-115">81</span><span class="sxs-lookup"><span data-stu-id="f2a1f-115">81</span></span>|<span data-ttu-id="f2a1f-116">Le conflit démarre.</span><span class="sxs-lookup"><span data-stu-id="f2a1f-116">Contention starts.</span></span> <span data-ttu-id="f2a1f-117">Cet événement n’inclut pas le temps qui s’écoule avant qu’un thread ne commence à attendre l’acquisition d’un verrou. Il est déclenché uniquement quand l’attente commence.</span><span class="sxs-lookup"><span data-stu-id="f2a1f-117">This event does not include the amount of spinning time before a thread waits to acquire a lock; it is raised only when the thread waits to acquire a lock.</span></span>|
|`ContentionStop`|<span data-ttu-id="f2a1f-118">91</span><span class="sxs-lookup"><span data-stu-id="f2a1f-118">91</span></span>|<span data-ttu-id="f2a1f-119">Le conflit se termine.</span><span class="sxs-lookup"><span data-stu-id="f2a1f-119">Contention ends.</span></span>|

<span data-ttu-id="f2a1f-120">Le tableau suivant présente les données d’événement :</span><span class="sxs-lookup"><span data-stu-id="f2a1f-120">The following table shows event data:</span></span>

|<span data-ttu-id="f2a1f-121">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="f2a1f-121">Field name</span></span>|<span data-ttu-id="f2a1f-122">Type de données</span><span class="sxs-lookup"><span data-stu-id="f2a1f-122">Data type</span></span>|<span data-ttu-id="f2a1f-123">Description</span><span class="sxs-lookup"><span data-stu-id="f2a1f-123">Description</span></span>|
|----------------|---------------|-----------------|
|<span data-ttu-id="f2a1f-124">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="f2a1f-124">Flags</span></span>|<span data-ttu-id="f2a1f-125">win:UInt8</span><span class="sxs-lookup"><span data-stu-id="f2a1f-125">win:UInt8</span></span>|<span data-ttu-id="f2a1f-126">0 pour managé ; 1 pour natif.</span><span class="sxs-lookup"><span data-stu-id="f2a1f-126">0 for managed; 1 for native.</span></span>|
|<span data-ttu-id="f2a1f-127">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="f2a1f-127">ClrInstanceID</span></span>|<span data-ttu-id="f2a1f-128">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="f2a1f-128">win:UInt16</span></span>|<span data-ttu-id="f2a1f-129">ID unique de l’instance de CLR.</span><span class="sxs-lookup"><span data-stu-id="f2a1f-129">Unique ID for the instance of CLR.</span></span>|

## <a name="see-also"></a><span data-ttu-id="f2a1f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2a1f-130">See also</span></span>

- [<span data-ttu-id="f2a1f-131">Événements ETW du CLR</span><span class="sxs-lookup"><span data-stu-id="f2a1f-131">CLR ETW Events</span></span>](clr-etw-events.md)
