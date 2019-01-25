---
title: Compteurs de performance de point de terminaison
ms.date: 03/30/2017
ms.assetid: 7d44d576-bd4e-453b-8b76-a818ce90b806
ms.openlocfilehash: de750b3e5ee61b6bfc5b387fb7de84b74171d8d9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54501959"
---
# <a name="endpoint-performance-counters"></a><span data-ttu-id="e15b4-102">Compteurs de performance de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e15b4-102">Endpoint Performance Counters</span></span>
<span data-ttu-id="e15b4-103">Les compteurs de performance de point de terminaison capturent des données qui révèlent comment un point de terminaison accepte des messages.</span><span class="sxs-lookup"><span data-stu-id="e15b4-103">Endpoint performance counters capture data that reveals how an endpoint is accepting messages.</span></span> <span data-ttu-id="e15b4-104">Ils se trouvent sous l'objet de performance `ServiceModelEndpoint 4.0.0.0` dans l'affichage de l'analyseur de performances.</span><span class="sxs-lookup"><span data-stu-id="e15b4-104">They can be found under the `ServiceModelEndpoint 4.0.0.0` performance object when viewing with the Performance Monitor.</span></span> <span data-ttu-id="e15b4-105">Les instances sont nommées à l’aide du modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="e15b4-105">The instances are named using this pattern:</span></span>  
  
```  
(ServiceName).(ContractName)@(endpoint listener address)  
```  
  
 <span data-ttu-id="e15b4-106">Les données sont semblables à celles recueillies pour des opérations individuelles, mais sont regroupées uniquement sur l'ensemble du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="e15b4-106">The data is similar to that collected for individual operations, but is only aggregated across the endpoint.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="e15b4-107">La longueur du nom d'une instance de compteur de performance est limitée.</span><span class="sxs-lookup"><span data-stu-id="e15b4-107">There is a limit on the length of a performance counter instance's name.</span></span> <span data-ttu-id="e15b4-108">Lorsqu’un nom d’instance de compteur Windows Communication Foundation (WCF) dépasse la longueur maximale, WCF remplace une partie du nom de l’instance avec une valeur de hachage.</span><span class="sxs-lookup"><span data-stu-id="e15b4-108">When a Windows Communication Foundation (WCF) counter instance name exceeds the maximum length, WCF replaces a portion of the instance name with a hash value.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e15b4-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e15b4-109">See also</span></span>
- [<span data-ttu-id="e15b4-110">Compteurs de performance</span><span class="sxs-lookup"><span data-stu-id="e15b4-110">Performance Counters</span></span>](../../../../../docs/framework/wcf/diagnostics/performance-counters/index.md)
