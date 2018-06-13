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
# <a name="security-validation-and-authentication-failures"></a><span data-ttu-id="6b41e-102">Nombre d’échecs de la validation de la sécurité et de l’authentification</span><span class="sxs-lookup"><span data-stu-id="6b41e-102">Security Validation and Authentication Failures</span></span>
<span data-ttu-id="6b41e-103">Nom de compteur : nombre d’échecs de la validation de la sécurité et de l’authentification</span><span class="sxs-lookup"><span data-stu-id="6b41e-103">Counter name: Security Validation and Authentication Failures</span></span>  
  
## <a name="description"></a><span data-ttu-id="6b41e-104">Description</span><span class="sxs-lookup"><span data-stu-id="6b41e-104">Description</span></span>  
 <span data-ttu-id="6b41e-105">Ce compteur est incrémenté chaque fois qu'un message est rejeté en raison d'un problème de sécurité non couvert par le compteur « Appels de sécurité non autorisés ».</span><span class="sxs-lookup"><span data-stu-id="6b41e-105">This counter is incremented whenever a message is rejected due to a security problem not covered by the "Security Calls Not Authorized" counter.</span></span> <span data-ttu-id="6b41e-106">Ces problèmes sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="6b41e-106">Such problems include:</span></span>  
  
-   <span data-ttu-id="6b41e-107">Impossibilité de lire le jeton client depuis le message.</span><span class="sxs-lookup"><span data-stu-id="6b41e-107">Client token cannot be read from the message.</span></span>  
  
-   <span data-ttu-id="6b41e-108">Échec de l'authentification du jeton client (par exemple, mot de passe incorrect).</span><span class="sxs-lookup"><span data-stu-id="6b41e-108">Client token has failed authentication (for example, bad password).</span></span>  
  
-   <span data-ttu-id="6b41e-109">Échec de la vérification de signature (par exemple, falsification du message).</span><span class="sxs-lookup"><span data-stu-id="6b41e-109">Signature verification has failed (for example, the message has been tampered).</span></span>  
  
-   <span data-ttu-id="6b41e-110">Le message est un doublon d'un message précédent, ce qui peut se produire lors d'une attaque par relecture.</span><span class="sxs-lookup"><span data-stu-id="6b41e-110">The message is a duplicate from a previous one, which can happen during a replay attack.</span></span>  
  
-   <span data-ttu-id="6b41e-111">Impossibilité de déchiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="6b41e-111">A decryption failure has occurred.</span></span>  
  
-   <span data-ttu-id="6b41e-112">Absence de certains éléments requis dans le message (par exemple, horodatage ou bloc des données chiffrées manquant).</span><span class="sxs-lookup"><span data-stu-id="6b41e-112">Some required elements (for example, missing timestamp or encrypted data block) are missing from the message.</span></span>  
  
-   <span data-ttu-id="6b41e-113">Erreurs lors de la négociation TLSNEGO/SPNEGO.</span><span class="sxs-lookup"><span data-stu-id="6b41e-113">Errors have occurred during TLSNEGO/SPNEGO handshake.</span></span>
