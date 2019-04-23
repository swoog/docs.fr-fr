---
title: 'Service : Appels ayant renvoyé une erreur par seconde'
ms.date: 03/30/2017
ms.assetid: 94247356-2b29-4b50-b639-91ca8c1cf3a9
ms.openlocfilehash: 595b623d70bad82ea39ab3ef93fb5fd499268ff2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59088474"
---
# <a name="service-calls-faulted-per-second"></a>Service : Appels ayant renvoyé une erreur par seconde
Nom du compteur : Appels erronés par seconde.  
  
## <a name="description"></a>Description  
 Nombre d'appels qui ont retourné des erreurs à ce service en une seconde.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)  
  
 Dans les applications Windows Communication Foundation (WCF), les méthodes de service communiquent des informations d’erreur de traitement à l’aide de messages d’erreur SOAP. Les erreurs SOAP sont des types de message inclus dans les métadonnées d'une opération de service et créent, par conséquent, un contrat d'erreur permettant aux clients d'améliorer la fiabilité ou l'interactivité de leur exécution. Les erreurs SOAP étant exprimées aux clients dans un format XML, elles sont très interopérables.  
  
## <a name="see-also"></a>Voir aussi

- [Spécification et gestion des erreurs dans les contrats et les services](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
