---
title: 'Point de terminaison : transactions passées par seconde'
ms.date: 03/30/2017
ms.assetid: 0f370ff1-a913-450b-bccb-c279ad165b3d
ms.openlocfilehash: 79f50b6706facd040ec2d325c676f210d5327bf8
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44227140"
---
# <a name="endpoint-transactions-flowed-per-second"></a>Point de terminaison : transactions passées par seconde
Nom du compteur : transactions passées par seconde.  
  
## <a name="description"></a>Description  
 Nombre de transactions transférées vers les opérations au niveau de ce point de terminaison en une seconde. Ce compteur est incrémenté à chaque ID de transaction présent dans un message envoyé vers le point de terminaison.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
