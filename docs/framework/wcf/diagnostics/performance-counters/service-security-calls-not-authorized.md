---
title: 'Service : appels de sécurité non autorisés'
ms.date: 03/30/2017
ms.assetid: 3024b20a-5250-4bd1-a38c-c6d79f89610b
author: BrucePerlerMS
ms.openlocfilehash: f90ed5746c8b798e55b7e300ba7ff63bbafdcac4
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2018
ms.locfileid: "48035881"
---
# <a name="service-security-calls-not-authorized"></a>Service : appels de sécurité non autorisés
Nom du compteur : Appels de sécurité non autorisés.  
  
## <a name="description"></a>Description  
 Ce compteur est incrémenté lorsque la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> retourne la valeur `false`. Il indique que le message entrant provient d'un utilisateur valide et qu'il est correctement protégé, mais que l'utilisateur n'est pas autorisé à exécuter des tâches spécifiques.
