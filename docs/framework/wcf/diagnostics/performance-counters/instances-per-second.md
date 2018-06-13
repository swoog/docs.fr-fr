---
title: Instances par seconde
ms.date: 03/30/2017
ms.assetid: 74579397-1058-4278-80cf-2d00854a480f
ms.openlocfilehash: c955d2cd0d87c89f412892e7088285f2db27ff42
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33471866"
---
# <a name="instances-per-second"></a>Instances par seconde
Nom du compteur : instances créées par seconde.  
  
## <a name="description"></a>Description  
 Nombre total d'instances de service créées en une seconde.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
