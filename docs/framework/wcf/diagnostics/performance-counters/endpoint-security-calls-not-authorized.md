---
title: 'Point de terminaison : appels de sécurité non autorisés'
ms.date: 03/30/2017
ms.assetid: d25095ff-9ff0-4c69-a674-4e6a9fe3f4dc
ms.openlocfilehash: b37d4cd33c41c6e978dd82ca7ce6332302a843de
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/26/2018
ms.locfileid: "50046679"
---
# <a name="endpoint-security-calls-not-authorized"></a>Point de terminaison : appels de sécurité non autorisés
Nom du compteur : Appels de sécurité non autorisés.  
  
## <a name="description"></a>Description  
 Ce compteur est incrémenté lorsque la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> retourne la valeur `false`. Il indique que le message entrant provient d'un utilisateur valide et qu'il est correctement protégé, mais que l'utilisateur n'est pas autorisé à exécuter des tâches spécifiques.
