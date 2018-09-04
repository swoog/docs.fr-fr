---
title: 'Service : appels par seconde'
ms.date: 03/30/2017
ms.assetid: 6261d28d-d449-425a-b9fc-a4ee14079134
ms.openlocfilehash: 5189a78e2655707d165f187e06ac9a60d055eac0
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43499885"
---
# <a name="service-calls-per-second"></a><span data-ttu-id="8cdba-102">Service : appels par seconde</span><span class="sxs-lookup"><span data-stu-id="8cdba-102">Service: Calls Per Second</span></span>
<span data-ttu-id="8cdba-103">Nom du compteur : Appels par seconde.</span><span class="sxs-lookup"><span data-stu-id="8cdba-103">Counter Name: Calls Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="8cdba-104">Description</span><span class="sxs-lookup"><span data-stu-id="8cdba-104">Description</span></span>  
 <span data-ttu-id="8cdba-105">Nombre d'appels à ce service en une seconde.</span><span class="sxs-lookup"><span data-stu-id="8cdba-105">Number of calls to this service in a second.</span></span>  
  
 <span data-ttu-id="8cdba-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="8cdba-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="8cdba-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F) où le numérateur (N) représente le nombre d'opérations exécutées au cours du dernier intervalle échantillon, le dénominateur (D) représente le nombre de graduations écoulées au cours du dernier intervalle échantillon, et F représente la fréquence des graduations.</span><span class="sxs-lookup"><span data-stu-id="8cdba-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F) where the numerator (N) represents the number of operations performed during the last sample interval, the denominator (D) represents the number of ticks elapsed during the last sample interval, and F is the frequency of the ticks.</span></span>
