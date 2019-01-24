---
title: Nombre d'appels ayant échoué par seconde
ms.date: 03/30/2017
ms.assetid: e4ef3773-f650-4876-99cf-4d0c02aa03d4
ms.openlocfilehash: bad37e0124698209955603c1b7d8a1aec4b87418
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54521047"
---
# <a name="calls-failed-per-second"></a><span data-ttu-id="ad1e5-102">Nombre d'appels ayant échoué par seconde</span><span class="sxs-lookup"><span data-stu-id="ad1e5-102">Calls Failed Per Second</span></span>
<span data-ttu-id="ad1e5-103">Nom du compteur : Nombre d'appels ayant échoué par seconde</span><span class="sxs-lookup"><span data-stu-id="ad1e5-103">Counter Name: Calls Failed Per Second</span></span>  
  
## <a name="description"></a><span data-ttu-id="ad1e5-104">Description</span><span class="sxs-lookup"><span data-stu-id="ad1e5-104">Description</span></span>  
 <span data-ttu-id="ad1e5-105">Nombre d'appels à cette opération avec des exceptions non prises en charge par seconde.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-105">Number of calls with unhandled exceptions in this operation in a second.</span></span>  
  
 <span data-ttu-id="ad1e5-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="ad1e5-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="ad1e5-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="ad1e5-108">Ce compteur est incrémenté à chaque exception non prise en charge dans cette opération.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-108">This counter is incremented everytime there is an unhandled exception in this operation.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad1e5-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad1e5-109">See also</span></span>
- [<span data-ttu-id="ad1e5-110">Spécification et gestion des erreurs dans les contrats et les services</span><span class="sxs-lookup"><span data-stu-id="ad1e5-110">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
