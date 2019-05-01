---
title: 'Service : Nombre d’échecs de la validation de la sécurité et de l’authentification'
ms.date: 03/30/2017
ms.assetid: 55c98268-b1ad-459d-851b-25ef52248187
ms.openlocfilehash: ba8da3ae6be6bd089690359f19e153da1e0b54fc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61998307"
---
# <a name="service-security-validation-and-authentication-failures"></a>Service : Nombre d’échecs de la validation de la sécurité et de l’authentification
Nom du compteur : Nombre d’échecs de la validation de la sécurité et de l’authentification  
  
## <a name="description"></a>Description  
 Ce compteur est incrémenté chaque fois qu'un message est rejeté en raison d'un problème de sécurité non couvert par le compteur « Appels de sécurité non autorisés ». Ces problèmes sont les suivants :  
  
- Impossibilité de lire le jeton client depuis le message.  
  
- Échec de l'authentification du jeton client (par exemple, mot de passe incorrect).  
  
- Échec de la vérification de signature (par exemple, falsification du message).  
  
- Le message est un doublon d'un message précédent, ce qui peut se produire lors d'une attaque par relecture.  
  
- Impossibilité de déchiffrer le message.  
  
- Absence de certains éléments requis dans le message (par exemple, horodateur ou bloc de données chiffrées manquant).  
  
- Erreurs lors de la négociation TLSNEGO/SPNEGO.
