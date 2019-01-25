---
title: Compteurs de performance d'opération
ms.date: 03/30/2017
ms.assetid: 333a51e0-f56e-4e1a-b359-5c91ff390568
ms.openlocfilehash: 16608132c6557f8612d42402a2cb2c49fcc29637
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54566086"
---
# <a name="operation-performance-counters"></a>Compteurs de performance d'opération
Les compteurs de performance d'opération se trouvent sous l'objet de performance `ServiceModelOperation 4.0.0.0` lors de l'affichage avec l'analyseur de performances (Perfmon.exe). Chaque opération a une instance individuelle. Autrement dit, si un contrat donné a 10 opérations, 10 instances de compteur d'opération sont associées à ce contrat. Les instances d'objet sont nommées à l'aide du modèle suivant :  
  
```  
(ServiceName).(ContractName).(OperationName)@(first endpoint listener address)  
```  
  
 Ce compteur vous permet de mesurer la manière dont l'appel est utilisé et comment l'opération s'exécute.  
  
> [!CAUTION]
>  La longueur du nom d'une instance de compteur de performance est limitée. Lorsqu’un nom d’instance de compteur Windows Communication Foundation (WCF) dépasse la longueur maximale, WCF remplace une partie du nom de l’instance avec une valeur de hachage.  
  
## <a name="see-also"></a>Voir aussi
- [Compteurs de performance](../../../../../docs/framework/wcf/diagnostics/performance-counters/index.md)
