---
title: 'Service : Appels par seconde'
ms.date: 03/30/2017
ms.assetid: 6261d28d-d449-425a-b9fc-a4ee14079134
ms.openlocfilehash: 5189a78e2655707d165f187e06ac9a60d055eac0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61773320"
---
# <a name="service-calls-per-second"></a><span data-ttu-id="ba7a8-102">Service : Appels par seconde</span><span class="sxs-lookup"><span data-stu-id="ba7a8-102">Service: Calls Per Second</span></span>
<span data-ttu-id="ba7a8-103">Nom du compteur : Appels par seconde.</span><span class="sxs-lookup"><span data-stu-id="ba7a8-103">Counter Name: Calls Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="ba7a8-104">Description</span><span class="sxs-lookup"><span data-stu-id="ba7a8-104">Description</span></span>  
 <span data-ttu-id="ba7a8-105">Nombre d'appels à ce service en une seconde.</span><span class="sxs-lookup"><span data-stu-id="ba7a8-105">Number of calls to this service in a second.</span></span>  
  
 <span data-ttu-id="ba7a8-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="ba7a8-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="ba7a8-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F) où le numérateur (N) représente le nombre d'opérations exécutées au cours du dernier intervalle échantillon, le dénominateur (D) représente le nombre de graduations écoulées au cours du dernier intervalle échantillon, et F représente la fréquence des graduations.</span><span class="sxs-lookup"><span data-stu-id="ba7a8-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F) where the numerator (N) represents the number of operations performed during the last sample interval, the denominator (D) represents the number of ticks elapsed during the last sample interval, and F is the frequency of the ticks.</span></span>
