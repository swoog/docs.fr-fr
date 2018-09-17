---
title: Sessions de messagerie fiable ayant renvoyé une erreur par seconde
ms.date: 03/30/2017
ms.assetid: 8f8ca2eb-1be4-4b6a-aa78-fcd3ee145fe8
ms.openlocfilehash: c77d6a5f12dcce15dba94e2f63025a219ebcc6fd
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45964603"
---
# <a name="reliable-messaging-sessions-faulted-per-second"></a>Sessions de messagerie fiable ayant renvoyé une erreur par seconde
Nom du compteur : Sessions de messagerie fiable ayant renvoyé une erreur par seconde.  
  
## <a name="description"></a>Description  
 Nombre de sessions de messagerie fiable ayant renvoyé une erreur dans ce service en une seconde.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
