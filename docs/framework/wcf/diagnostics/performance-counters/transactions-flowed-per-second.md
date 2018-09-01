---
title: Transactions passées par seconde
ms.date: 03/30/2017
ms.assetid: b9f661e1-576c-48fc-9fdf-91853e0749e8
ms.openlocfilehash: e77aef4cfff1e64f112e720183675dfb7aa25d27
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43392934"
---
# <a name="transactions-flowed-per-second"></a>Transactions passées par seconde
Nom du compteur : transactions passées par seconde  
  
## <a name="description"></a>Description  
 Nombre de transactions transmises à cette opération en une seconde. Ce compteur est incrémenté à chaque fois qu’un ID de transaction est présent dans un message envoyé à l’opération.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
