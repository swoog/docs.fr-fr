---
title: Messages de messagerie fiable déposés par seconde
ms.date: 03/30/2017
ms.assetid: a11b0b80-b242-48e1-b0bb-7f756db5486b
ms.openlocfilehash: 9a87ec509b19f0c566b50ae3672a6c3d2940ee12
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33474192"
---
# <a name="reliable-messaging-messages-dropped-per-second"></a>Messages de messagerie fiable déposés par seconde
Nom du compteur : messages de messagerie fiable déposés par seconde.  
  
## <a name="description"></a>Description  
 Nombre total de messages de messagerie fiable déposés dans ce service en une seconde.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
