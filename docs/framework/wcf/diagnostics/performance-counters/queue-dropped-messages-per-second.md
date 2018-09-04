---
title: Messages déposés par le transport de mise en file d’attente par seconde
ms.date: 03/30/2017
ms.assetid: 74540f52-8762-4147-b5ba-e171180515a3
ms.openlocfilehash: f15b2db08ac4486377189a1533b653260d79024a
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43528121"
---
# <a name="queue-dropped-messages-per-second"></a><span data-ttu-id="89d09-102">Messages déposés par le transport de mise en file d’attente par seconde</span><span class="sxs-lookup"><span data-stu-id="89d09-102">Queue Dropped Messages Per Second</span></span>
<span data-ttu-id="89d09-103">Nom du compteur : messages de la file d’attente déposés par seconde.</span><span class="sxs-lookup"><span data-stu-id="89d09-103">Counter Name: Queued Messages Dropped Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="89d09-104">Description</span><span class="sxs-lookup"><span data-stu-id="89d09-104">Description</span></span>  
 <span data-ttu-id="89d09-105">Nombre de messages supprimés du transport de mise en file d’attente au niveau de ce service en une seconde.</span><span class="sxs-lookup"><span data-stu-id="89d09-105">Number of messages that are dropped by the queued transport at this service in a second.</span></span>  
  
 <span data-ttu-id="89d09-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="89d09-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="89d09-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="89d09-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
