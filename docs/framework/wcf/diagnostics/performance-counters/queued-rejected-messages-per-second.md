---
title: Messages rejetés par le transport de mise en file d'attente par seconde
ms.date: 03/30/2017
ms.assetid: 77ea9aa3-b9e2-4a1d-a65e-5ca115ba0567
ms.openlocfilehash: 096e2188b13d0fd5a9be35e5e6473107a58c5566
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61916185"
---
# <a name="queued-rejected-messages-per-second"></a>Messages rejetés par le transport de mise en file d'attente par seconde
Nom du compteur : En file d’attente de Messages rejetés par seconde.  
  
## <a name="description"></a>Description  
 Nombre de messages vers ce service qui ont été rejetés par le transport de mise en file d'attente en une seconde.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
