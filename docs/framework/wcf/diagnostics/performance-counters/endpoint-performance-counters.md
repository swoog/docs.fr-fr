---
title: Compteurs de performance de point de terminaison
ms.date: 03/30/2017
ms.assetid: 7d44d576-bd4e-453b-8b76-a818ce90b806
ms.openlocfilehash: f07e318e39a68e689ec484b09fa743623cfb51d9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59158383"
---
# <a name="endpoint-performance-counters"></a><span data-ttu-id="517de-102">Compteurs de performance de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="517de-102">Endpoint Performance Counters</span></span>
<span data-ttu-id="517de-103">Les compteurs de performance de point de terminaison capturent des données qui révèlent comment un point de terminaison accepte des messages.</span><span class="sxs-lookup"><span data-stu-id="517de-103">Endpoint performance counters capture data that reveals how an endpoint is accepting messages.</span></span> <span data-ttu-id="517de-104">Ils se trouvent sous l'objet de performance `ServiceModelEndpoint 4.0.0.0` dans l'affichage de l'analyseur de performances.</span><span class="sxs-lookup"><span data-stu-id="517de-104">They can be found under the `ServiceModelEndpoint 4.0.0.0` performance object when viewing with the Performance Monitor.</span></span> <span data-ttu-id="517de-105">Les instances sont nommées à l’aide du modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="517de-105">The instances are named using this pattern:</span></span>  
  
```  
(ServiceName).(ContractName)@(endpoint listener address)  
```  
  
 <span data-ttu-id="517de-106">Les données sont semblables à celles recueillies pour des opérations individuelles, mais sont regroupées uniquement sur l'ensemble du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="517de-106">The data is similar to that collected for individual operations, but is only aggregated across the endpoint.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="517de-107">La longueur du nom d'une instance de compteur de performance est limitée.</span><span class="sxs-lookup"><span data-stu-id="517de-107">There is a limit on the length of a performance counter instance's name.</span></span> <span data-ttu-id="517de-108">Lorsqu’un nom d’instance de compteur Windows Communication Foundation (WCF) dépasse la longueur maximale, WCF remplace une partie du nom de l’instance avec une valeur de hachage.</span><span class="sxs-lookup"><span data-stu-id="517de-108">When a Windows Communication Foundation (WCF) counter instance name exceeds the maximum length, WCF replaces a portion of the instance name with a hash value.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="517de-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="517de-109">See also</span></span>

- [<span data-ttu-id="517de-110">Compteurs de performance</span><span class="sxs-lookup"><span data-stu-id="517de-110">Performance Counters</span></span>](../../../../../docs/framework/wcf/diagnostics/performance-counters/index.md)
