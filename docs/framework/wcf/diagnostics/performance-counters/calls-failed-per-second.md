---
title: Nombre d'appels ayant échoué par seconde
ms.date: 03/30/2017
ms.assetid: e4ef3773-f650-4876-99cf-4d0c02aa03d4
ms.openlocfilehash: ff9320b0990a0543bbb1da553d040ff5a4b4fed9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59178618"
---
# <a name="calls-failed-per-second"></a><span data-ttu-id="60fe5-102">Nombre d'appels ayant échoué par seconde</span><span class="sxs-lookup"><span data-stu-id="60fe5-102">Calls Failed Per Second</span></span>
<span data-ttu-id="60fe5-103">Nom du compteur : Nombre d'appels ayant échoué par seconde</span><span class="sxs-lookup"><span data-stu-id="60fe5-103">Counter Name: Calls Failed Per Second</span></span>  
  
## <a name="description"></a><span data-ttu-id="60fe5-104">Description</span><span class="sxs-lookup"><span data-stu-id="60fe5-104">Description</span></span>  
 <span data-ttu-id="60fe5-105">Nombre d'appels à cette opération avec des exceptions non prises en charge par seconde.</span><span class="sxs-lookup"><span data-stu-id="60fe5-105">Number of calls with unhandled exceptions in this operation in a second.</span></span>  
  
 <span data-ttu-id="60fe5-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="60fe5-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="60fe5-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="60fe5-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="60fe5-108">Ce compteur est incrémenté à chaque exception non prise en charge dans cette opération.</span><span class="sxs-lookup"><span data-stu-id="60fe5-108">This counter is incremented everytime there is an unhandled exception in this operation.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="60fe5-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60fe5-109">See also</span></span>

- [<span data-ttu-id="60fe5-110">Spécification et gestion des erreurs dans les contrats et les services</span><span class="sxs-lookup"><span data-stu-id="60fe5-110">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
