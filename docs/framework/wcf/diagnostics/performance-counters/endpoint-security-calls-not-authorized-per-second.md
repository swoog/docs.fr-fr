---
title: 'Point de terminaison : appels de sécurité non autorisés par seconde'
ms.date: 03/30/2017
ms.assetid: c8a1547b-986b-45c1-b302-dea0cd4b516d
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 4cefdd7480c7d0e9475b1883e603d9db1f287d4a
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44186329"
---
# <a name="endpoint-security-calls-not-authorized-per-second"></a>Point de terminaison : appels de sécurité non autorisés par seconde
Nom du compteur : Appels de sécurité non autorisés par seconde.  
  
## <a name="description"></a>Description  
 Nombre de messages entrants en une seconde qui proviennent d'un utilisateur valide et sont protégés correctement, mais pour lesquels l'utilisateur n'est pas autorisé à effectuer des tâches spécifiques.  
  
 Ce compteur est incrémenté lorsque la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> retourne la valeur `false`.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
