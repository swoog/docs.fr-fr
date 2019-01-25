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
# <a name="endpoint-performance-counters"></a>Compteurs de performance de point de terminaison
Les compteurs de performance de point de terminaison capturent des données qui révèlent comment un point de terminaison accepte des messages. Ils se trouvent sous l'objet de performance `ServiceModelEndpoint 4.0.0.0` dans l'affichage de l'analyseur de performances. Les instances sont nommées à l’aide du modèle suivant :  
  
```  
(ServiceName).(ContractName)@(endpoint listener address)  
```  
  
 Les données sont semblables à celles recueillies pour des opérations individuelles, mais sont regroupées uniquement sur l'ensemble du point de terminaison.  
  
> [!CAUTION]
>  La longueur du nom d'une instance de compteur de performance est limitée. Lorsqu’un nom d’instance de compteur Windows Communication Foundation (WCF) dépasse la longueur maximale, WCF remplace une partie du nom de l’instance avec une valeur de hachage.  
  
## <a name="see-also"></a>Voir aussi
- [Compteurs de performance](../../../../../docs/framework/wcf/diagnostics/performance-counters/index.md)
