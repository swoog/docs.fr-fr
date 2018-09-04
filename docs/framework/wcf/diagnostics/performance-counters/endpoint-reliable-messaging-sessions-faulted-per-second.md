---
title: 'Point de terminaison : sessions de messagerie fiable ayant renvoyé une erreur par seconde'
ms.date: 03/30/2017
ms.assetid: e9ae808a-7e1f-46b0-9560-d5a866be6d6e
ms.openlocfilehash: f6b48ec4c37c28588dd874a5bfa94a01a2f43b0c
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43564185"
---
# <a name="endpoint-reliable-messaging-sessions-faulted-per-second"></a>Point de terminaison : sessions de messagerie fiable ayant renvoyé une erreur par seconde
Nom du compteur : Sessions de messagerie fiable ayant renvoyé une erreur par seconde.  
  
## <a name="description"></a>Description  
 Nombre de sessions de messagerie fiable ayant renvoyé une erreur au niveau de ce point de terminaison par seconde.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
