---
title: 'Point de terminaison : Nombre d’échecs de la validation de la sécurité et de l’authentification'
ms.date: 03/30/2017
ms.assetid: 5bad60aa-6084-4c7b-aefd-9b581f04382e
ms.openlocfilehash: 9e0192ea600bb52abd555f2f83cfe8e96d3fe203
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64619340"
---
# <a name="endpoint-security-validation-and-authentication-failures"></a>Point de terminaison : Nombre d’échecs de la validation de la sécurité et de l’authentification
Nom du compteur : Nombre d’échecs de la validation de la sécurité et de l’authentification  
  
## <a name="description"></a>Description  
 Ce compteur est incrémenté chaque fois qu'un message est rejeté en raison d'un problème de sécurité non couvert par le compteur « Appels de sécurité non autorisés ». Ces problèmes sont les suivants :  
  
- Impossibilité de lire le jeton client depuis le message.  
  
- L'échec de l'authentification du jeton client (en raison d'un mot de passe erroné).  
  
- Impossibilité de vérifier la signature (parce que le message a été falsifié).  
  
- Le message est un doublon d'un message précédent, ce qui peut se produire lors d'une attaque par relecture.  
  
- Impossibilité de déchiffrer le message.  
  
- L'absence de certains éléments requis dans le message (horodatage ou bloc des données chiffrées manquant).  
  
- Erreurs lors de la négociation TLSNEGO/SPNEGO.
