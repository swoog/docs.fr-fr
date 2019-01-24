---
title: "Service : Nombre d'appels ayant échoué par seconde"
ms.date: 03/30/2017
ms.assetid: 5a2c7939-107d-4f0c-b43c-e02e079e8a9d
ms.openlocfilehash: a043cf30fa67707aca3edf50cf23372ade5e5a42
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54559890"
---
# <a name="service-calls-failed-per-second"></a>Service : Nombre d'appels ayant échoué par seconde
Nom du compteur : Appels ayant échoué par seconde.  
  
## <a name="description"></a>Description  
 Nombre d'appels qui ont des exceptions non prises en charge et qui sont reçus par ce service par seconde.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)  
  
 Dans le code managé, des exceptions sont levées en cas de conditions d'erreur.  
  
 Dans le code managé, des exceptions sont levées en cas de conditions d'erreur.  
  
 Ce compteur est incrémenté à chaque exception non prise en charge dans ce service.  
  
## <a name="see-also"></a>Voir aussi
- [Spécification et gestion des erreurs dans les contrats et les services](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
