---
title: Nombre d’échecs de la validation de la sécurité et de l’authentification
ms.date: 03/30/2017
ms.assetid: 0d4e3666-dfc6-421c-baf8-9479c22f7050
ms.openlocfilehash: 32a7d41f93dd99f1950a073e1cac1b62177ff6c3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61916043"
---
# <a name="security-validation-and-authentication-failures"></a><span data-ttu-id="443a2-102">Nombre d’échecs de la validation de la sécurité et de l’authentification</span><span class="sxs-lookup"><span data-stu-id="443a2-102">Security Validation and Authentication Failures</span></span>
<span data-ttu-id="443a2-103">Nom du compteur : Nombre d’échecs de la validation de la sécurité et de l’authentification</span><span class="sxs-lookup"><span data-stu-id="443a2-103">Counter name: Security Validation and Authentication Failures</span></span>  
  
## <a name="description"></a><span data-ttu-id="443a2-104">Description</span><span class="sxs-lookup"><span data-stu-id="443a2-104">Description</span></span>  
 <span data-ttu-id="443a2-105">Ce compteur est incrémenté chaque fois qu'un message est rejeté en raison d'un problème de sécurité non couvert par le compteur « Appels de sécurité non autorisés ».</span><span class="sxs-lookup"><span data-stu-id="443a2-105">This counter is incremented whenever a message is rejected due to a security problem not covered by the "Security Calls Not Authorized" counter.</span></span> <span data-ttu-id="443a2-106">Ces problèmes sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="443a2-106">Such problems include:</span></span>  
  
- <span data-ttu-id="443a2-107">Impossibilité de lire le jeton client depuis le message.</span><span class="sxs-lookup"><span data-stu-id="443a2-107">Client token cannot be read from the message.</span></span>  
  
- <span data-ttu-id="443a2-108">Échec de l'authentification du jeton client (par exemple, mot de passe incorrect).</span><span class="sxs-lookup"><span data-stu-id="443a2-108">Client token has failed authentication (for example, bad password).</span></span>  
  
- <span data-ttu-id="443a2-109">Échec de la vérification de signature (par exemple, falsification du message).</span><span class="sxs-lookup"><span data-stu-id="443a2-109">Signature verification has failed (for example, the message has been tampered).</span></span>  
  
- <span data-ttu-id="443a2-110">Le message est un doublon d'un message précédent, ce qui peut se produire lors d'une attaque par relecture.</span><span class="sxs-lookup"><span data-stu-id="443a2-110">The message is a duplicate from a previous one, which can happen during a replay attack.</span></span>  
  
- <span data-ttu-id="443a2-111">Impossibilité de déchiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="443a2-111">A decryption failure has occurred.</span></span>  
  
- <span data-ttu-id="443a2-112">Absence de certains éléments requis dans le message (par exemple, horodatage ou bloc des données chiffrées manquant).</span><span class="sxs-lookup"><span data-stu-id="443a2-112">Some required elements (for example, missing timestamp or encrypted data block) are missing from the message.</span></span>  
  
- <span data-ttu-id="443a2-113">Erreurs lors de la négociation TLSNEGO/SPNEGO.</span><span class="sxs-lookup"><span data-stu-id="443a2-113">Errors have occurred during TLSNEGO/SPNEGO handshake.</span></span>
