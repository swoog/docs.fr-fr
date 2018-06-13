---
title: 'Point de terminaison : appels ayant échoué par seconde'
ms.date: 03/30/2017
ms.assetid: bcbe9da4-c8dd-4e27-b630-11611adc7580
ms.openlocfilehash: c0273fc90ad5702663862612f52f03c42f410b8e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33473492"
---
# <a name="endpoint-calls-failed-per-second"></a><span data-ttu-id="ff906-102">Point de terminaison : appels ayant échoué par seconde</span><span class="sxs-lookup"><span data-stu-id="ff906-102">Endpoint: Calls Failed Per Second</span></span>
<span data-ttu-id="ff906-103">Nom du compteur : appels ayant échoué par seconde.</span><span class="sxs-lookup"><span data-stu-id="ff906-103">Counter Name: Calls Failed Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="ff906-104">Description</span><span class="sxs-lookup"><span data-stu-id="ff906-104">Description</span></span>  
 <span data-ttu-id="ff906-105">Nombre d'appels ayant des exceptions non traitées et reçus par ce point de terminaison en une seconde.</span><span class="sxs-lookup"><span data-stu-id="ff906-105">Number of calls that have unhandled exceptions and are received by this endpoint in a second.</span></span>  
  
 <span data-ttu-id="ff906-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="ff906-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="ff906-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="ff906-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="ff906-108">Ce compteur est incrémenté à chaque exception non traitée à ce point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ff906-108">This counter is incremented every time there is an unhandled exception at this endpoint.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff906-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff906-109">See Also</span></span>  
 [<span data-ttu-id="ff906-110">Spécification et gestion des erreurs dans les contrats et les services</span><span class="sxs-lookup"><span data-stu-id="ff906-110">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
