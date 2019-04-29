---
title: Compteurs de performance de service
ms.date: 03/30/2017
ms.assetid: 4210f549-31f2-4ea7-99bd-69eaffb98ddf
ms.openlocfilehash: dc31e05f82f232095f6560c8fdd9bf75c040e2ca
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61773437"
---
# <a name="service-performance-counters"></a><span data-ttu-id="d59ca-102">Compteurs de performance de service</span><span class="sxs-lookup"><span data-stu-id="d59ca-102">Service Performance Counters</span></span>
<span data-ttu-id="d59ca-103">Les compteurs de performance de service mesurent le comportement du service dans son ensemble et peuvent être utilisés pour diagnostiquer les performances de la totalité du service.</span><span class="sxs-lookup"><span data-stu-id="d59ca-103">Service performance counters measure the service behavior as a whole and can be used to diagnose the performance of the whole service.</span></span> <span data-ttu-id="d59ca-104">Ils se trouvent sous l'objet de performance `ServiceModelService 4.0.0.0` dans l'affichage de l'analyseur de performances (Perfmon.exe).</span><span class="sxs-lookup"><span data-stu-id="d59ca-104">They can be found under the `ServiceModelService 4.0.0.0` performance object when viewing with Performance Monitor (Perfmon.exe).</span></span> <span data-ttu-id="d59ca-105">Les instances sont nommées à l'aide du modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="d59ca-105">The instances are named using the following pattern:</span></span>  
  
```  
ServiceName@ServiceBaseAddress  
```  
  
> [!CAUTION]
>  <span data-ttu-id="d59ca-106">La longueur du nom d'une instance de compteur de performance est limitée.</span><span class="sxs-lookup"><span data-stu-id="d59ca-106">There is a limit on the length of a performance counter instance's name.</span></span> <span data-ttu-id="d59ca-107">Lorsqu’un nom d’instance de compteur Windows Communication Foundation (WCF) dépasse la longueur maximale, WCF remplace une partie du nom de l’instance avec une valeur de hachage.</span><span class="sxs-lookup"><span data-stu-id="d59ca-107">When a Windows Communication Foundation (WCF) counter instance name exceeds the maximum length, WCF replaces a portion of the instance name with a hash value.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d59ca-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d59ca-108">See also</span></span>

- [<span data-ttu-id="d59ca-109">Compteurs de performance</span><span class="sxs-lookup"><span data-stu-id="d59ca-109">Performance Counters</span></span>](../../../../../docs/framework/wcf/diagnostics/performance-counters/index.md)
