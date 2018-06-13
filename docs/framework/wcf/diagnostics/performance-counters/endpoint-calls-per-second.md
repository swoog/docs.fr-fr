---
title: 'Point de terminaison : appels par seconde'
ms.date: 03/30/2017
ms.assetid: ca0fc06d-d68f-4236-bd5f-c7ff6214acdd
ms.openlocfilehash: 186d59d2f0255f0f964130659a2053fc8f440dd8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33474504"
---
# <a name="endpoint-calls-per-second"></a>Point de terminaison : appels par seconde
Nom du compteur : Appels par seconde.  
  
## <a name="description"></a>Description  
 Nombre d'appels à ce point de terminaison en une seconde.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
