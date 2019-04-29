---
title: "Point de terminaison : Nombre d'appels ayant échoué par seconde"
ms.date: 03/30/2017
ms.assetid: bcbe9da4-c8dd-4e27-b630-11611adc7580
ms.openlocfilehash: 52419f45adde768d19d6b46642d52ad0a1844197
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61797343"
---
# <a name="endpoint-calls-failed-per-second"></a><span data-ttu-id="52967-102">Point de terminaison : Nombre d'appels ayant échoué par seconde</span><span class="sxs-lookup"><span data-stu-id="52967-102">Endpoint: Calls Failed Per Second</span></span>
<span data-ttu-id="52967-103">Nom du compteur : Appels ayant échoué par seconde.</span><span class="sxs-lookup"><span data-stu-id="52967-103">Counter Name: Calls Failed Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="52967-104">Description</span><span class="sxs-lookup"><span data-stu-id="52967-104">Description</span></span>  
 <span data-ttu-id="52967-105">Nombre d'appels ayant des exceptions non traitées et reçus par ce point de terminaison en une seconde.</span><span class="sxs-lookup"><span data-stu-id="52967-105">Number of calls that have unhandled exceptions and are received by this endpoint in a second.</span></span>  
  
 <span data-ttu-id="52967-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="52967-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="52967-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="52967-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="52967-108">Ce compteur est incrémenté à chaque exception non traitée à ce point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="52967-108">This counter is incremented every time there is an unhandled exception at this endpoint.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="52967-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52967-109">See also</span></span>

- [<span data-ttu-id="52967-110">Spécification et gestion des erreurs dans les contrats et les services</span><span class="sxs-lookup"><span data-stu-id="52967-110">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
