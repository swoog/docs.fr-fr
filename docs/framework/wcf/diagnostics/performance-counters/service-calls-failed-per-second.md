---
title: "Service : Nombre d'appels ayant échoué par seconde"
ms.date: 03/30/2017
ms.assetid: 5a2c7939-107d-4f0c-b43c-e02e079e8a9d
ms.openlocfilehash: d87d5f06d0c9a3849ec80a3d1c7badefde7cf372
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61915679"
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
