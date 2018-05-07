---
title: Compteurs de performance de service
ms.date: 03/30/2017
ms.assetid: 4210f549-31f2-4ea7-99bd-69eaffb98ddf
ms.openlocfilehash: 71eff5c656a4782056ac518f105f73bc549da336
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="service-performance-counters"></a>Compteurs de performance de service
Les compteurs de performance de service mesurent le comportement du service dans son ensemble et peuvent être utilisés pour diagnostiquer les performances de la totalité du service. Ils se trouvent sous l'objet de performance `ServiceModelService 4.0.0.0` dans l'affichage de l'analyseur de performances (Perfmon.exe). Les instances sont nommées à l’aide du modèle suivant :  
  
```  
ServiceName@ServiceBaseAddress  
```  
  
> [!CAUTION]
>  La longueur du nom d'une instance de compteur de performance est limitée. Lorsqu’un nom d’instance de compteur Windows Communication Foundation (WCF) dépasse la longueur maximale, [!INCLUDE[indigo2](../../../../../includes/indigo2-md.md)] remplace une partie de l’instance par une valeur de hachage.  
  
## <a name="see-also"></a>Voir aussi  
 [Compteurs de performance](../../../../../docs/framework/wcf/diagnostics/performance-counters/index.md)
