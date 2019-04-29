---
title: Opérations traitées avec des résultats incertains par seconde
ms.date: 03/30/2017
ms.assetid: 7e6b0716-c107-42e5-a21d-31d988e7a691
ms.openlocfilehash: f7365c4e5f03711129916c8c6964f7e25e9b553e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61766335"
---
# <a name="transacted-operations-in-doubt-per-second"></a><span data-ttu-id="6f893-102">Opérations traitées avec des résultats incertains par seconde</span><span class="sxs-lookup"><span data-stu-id="6f893-102">Transacted Operations In Doubt Per Second</span></span>
<span data-ttu-id="6f893-103">Nom du compteur : Opérations traitées avec des résultats incertains par seconde.</span><span class="sxs-lookup"><span data-stu-id="6f893-103">Counter Name: Transacted Operations In Doubt Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="6f893-104">Description</span><span class="sxs-lookup"><span data-stu-id="6f893-104">Description</span></span>  
 <span data-ttu-id="6f893-105">Nombre d'opérations transactionnelles avec un résultat incertain dans ce service en une seconde.</span><span class="sxs-lookup"><span data-stu-id="6f893-105">Number of transactional operations with an in-doubt outcome in this service in a second.</span></span>  
  
 <span data-ttu-id="6f893-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="6f893-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="6f893-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="6f893-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
