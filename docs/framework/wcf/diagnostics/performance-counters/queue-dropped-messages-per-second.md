---
title: Messages déposés par le transport de mise en file d’attente par seconde
ms.date: 03/30/2017
ms.assetid: 74540f52-8762-4147-b5ba-e171180515a3
ms.openlocfilehash: f15b2db08ac4486377189a1533b653260d79024a
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43418246"
---
# <a name="queue-dropped-messages-per-second"></a>Messages déposés par le transport de mise en file d’attente par seconde
Nom du compteur : messages de la file d’attente déposés par seconde.  
  
## <a name="description"></a>Description  
 Nombre de messages supprimés du transport de mise en file d’attente au niveau de ce service en une seconde.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
