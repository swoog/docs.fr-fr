---
title: Messages incohérents en file d'attente par seconde
ms.date: 03/30/2017
ms.assetid: d193fdd1-02f1-44a0-906e-f632a8f574c3
ms.openlocfilehash: d4c921b105dfd1c1a364d2c86f54ab920078dd4a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61916147"
---
# <a name="queued-poison-messages-per-second"></a>Messages incohérents en file d'attente par seconde
Nom du compteur : Messages incohérents en file d’attente par seconde.  
  
## <a name="description"></a>Description  
 Nombre de messages vers ce service marqués comme incohérents par le transport de mise en file d'attente par seconde.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
