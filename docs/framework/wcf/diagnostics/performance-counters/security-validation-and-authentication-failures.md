---
title: Nombre d’échecs de la validation de la sécurité et de l’authentification
ms.date: 03/30/2017
ms.assetid: 0d4e3666-dfc6-421c-baf8-9479c22f7050
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 5d7964c59f28f33d6ec7bc3ba605b84e6a201b14
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33474257"
---
# <a name="security-validation-and-authentication-failures"></a>Nombre d’échecs de la validation de la sécurité et de l’authentification
Nom de compteur : nombre d’échecs de la validation de la sécurité et de l’authentification  
  
## <a name="description"></a>Description  
 Ce compteur est incrémenté chaque fois qu'un message est rejeté en raison d'un problème de sécurité non couvert par le compteur « Appels de sécurité non autorisés ». Ces problèmes sont les suivants :  
  
-   Impossibilité de lire le jeton client depuis le message.  
  
-   Échec de l'authentification du jeton client (par exemple, mot de passe incorrect).  
  
-   Échec de la vérification de signature (par exemple, falsification du message).  
  
-   Le message est un doublon d'un message précédent, ce qui peut se produire lors d'une attaque par relecture.  
  
-   Impossibilité de déchiffrer le message.  
  
-   Absence de certains éléments requis dans le message (par exemple, horodatage ou bloc des données chiffrées manquant).  
  
-   Erreurs lors de la négociation TLSNEGO/SPNEGO.
