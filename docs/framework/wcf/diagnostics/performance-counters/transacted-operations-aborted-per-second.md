---
title: Nombre d'opérations traitées abandonnées par seconde
ms.date: 03/30/2017
ms.assetid: 19fc993f-2b3d-4898-852e-3b98ec2153a5
ms.openlocfilehash: 6369fea6def5ebb6b62274caed31d5fb63b3b0e1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61998190"
---
# <a name="transacted-operations-aborted-per-second"></a>Nombre d'opérations traitées abandonnées par seconde
Nom du compteur : Opérations traitées abandonnées par seconde.  
  
## <a name="description"></a>Description  
 Nombre d’opérations transactionnelles abandonnées dans ce service par seconde.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
