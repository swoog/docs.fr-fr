---
title: 'Point de terminaison : nombre d’échecs de la validation de la sécurité et de l’authentification'
ms.date: 03/30/2017
ms.assetid: 5bad60aa-6084-4c7b-aefd-9b581f04382e
ms.openlocfilehash: e69549a276e2f9cece966dd44f6a1b3a3d3cb59f
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50181093"
---
# <a name="endpoint-security-validation-and-authentication-failures"></a>Point de terminaison : nombre d’échecs de la validation de la sécurité et de l’authentification
Nom de compteur : nombre d’échecs de la validation de la sécurité et de l’authentification  
  
## <a name="description"></a>Description  
 Ce compteur est incrémenté chaque fois qu'un message est rejeté en raison d'un problème de sécurité non couvert par le compteur « Appels de sécurité non autorisés ». Ces problèmes sont les suivants :  
  
-   Impossibilité de lire le jeton client depuis le message.  
  
-   L'échec de l'authentification du jeton client (en raison d'un mot de passe erroné).  
  
-   Impossibilité de vérifier la signature (parce que le message a été falsifié).  
  
-   Le message est un doublon d'un message précédent, ce qui peut se produire lors d'une attaque par relecture.  
  
-   Impossibilité de déchiffrer le message.  
  
-   L'absence de certains éléments requis dans le message (horodatage ou bloc des données chiffrées manquant).  
  
-   Erreurs lors de la négociation TLSNEGO/SPNEGO.
