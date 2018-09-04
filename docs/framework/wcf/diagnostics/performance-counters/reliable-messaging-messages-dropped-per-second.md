---
title: Messages de messagerie fiable déposés par seconde
ms.date: 03/30/2017
ms.assetid: a11b0b80-b242-48e1-b0bb-7f756db5486b
ms.openlocfilehash: 7722b32f99b302c5c272e095033879c9e04c7ee1
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43542839"
---
# <a name="reliable-messaging-messages-dropped-per-second"></a>Messages de messagerie fiable déposés par seconde
Nom du compteur : messages de messagerie fiable déposés par seconde.  
  
## <a name="description"></a>Description  
 Nombre total de messages de messagerie fiable déposés dans ce service en une seconde.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
