---
title: 'Point de terminaison : Nombre d’échecs de la validation de la sécurité et de l’authentification'
ms.date: 03/30/2017
ms.assetid: 5bad60aa-6084-4c7b-aefd-9b581f04382e
ms.openlocfilehash: e69549a276e2f9cece966dd44f6a1b3a3d3cb59f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61916328"
---
# <a name="endpoint-security-validation-and-authentication-failures"></a><span data-ttu-id="03ee3-102">Point de terminaison : Nombre d’échecs de la validation de la sécurité et de l’authentification</span><span class="sxs-lookup"><span data-stu-id="03ee3-102">Endpoint: Security Validation and Authentication Failures</span></span>
<span data-ttu-id="03ee3-103">Nom du compteur : Nombre d’échecs de la validation de la sécurité et de l’authentification</span><span class="sxs-lookup"><span data-stu-id="03ee3-103">Counter name: Security Validation and Authentication Failures</span></span>  
  
## <a name="description"></a><span data-ttu-id="03ee3-104">Description</span><span class="sxs-lookup"><span data-stu-id="03ee3-104">Description</span></span>  
 <span data-ttu-id="03ee3-105">Ce compteur est incrémenté chaque fois qu'un message est rejeté en raison d'un problème de sécurité non couvert par le compteur « Appels de sécurité non autorisés ».</span><span class="sxs-lookup"><span data-stu-id="03ee3-105">This counter is incremented whenever a message is rejected due to a security problem not covered by the "Security Calls Not Authorized" counter.</span></span> <span data-ttu-id="03ee3-106">Ces problèmes sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="03ee3-106">Such problems include:</span></span>  
  
- <span data-ttu-id="03ee3-107">Impossibilité de lire le jeton client depuis le message.</span><span class="sxs-lookup"><span data-stu-id="03ee3-107">Client token cannot be read from the message.</span></span>  
  
- <span data-ttu-id="03ee3-108">L'échec de l'authentification du jeton client (en raison d'un mot de passe erroné).</span><span class="sxs-lookup"><span data-stu-id="03ee3-108">Client token has failed authentication (bad password).</span></span>  
  
- <span data-ttu-id="03ee3-109">Impossibilité de vérifier la signature (parce que le message a été falsifié).</span><span class="sxs-lookup"><span data-stu-id="03ee3-109">Signature verification has failed (the message has been tampered).</span></span>  
  
- <span data-ttu-id="03ee3-110">Le message est un doublon d'un message précédent, ce qui peut se produire lors d'une attaque par relecture.</span><span class="sxs-lookup"><span data-stu-id="03ee3-110">The message is a duplicate from a previous one, which can happen during a replay attack.</span></span>  
  
- <span data-ttu-id="03ee3-111">Impossibilité de déchiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="03ee3-111">A decryption failure has occurred.</span></span>  
  
- <span data-ttu-id="03ee3-112">L'absence de certains éléments requis dans le message (horodatage ou bloc des données chiffrées manquant).</span><span class="sxs-lookup"><span data-stu-id="03ee3-112">Some required elements (missing timestamp or encrypted data block) are missing from the message.</span></span>  
  
- <span data-ttu-id="03ee3-113">Erreurs lors de la négociation TLSNEGO/SPNEGO.</span><span class="sxs-lookup"><span data-stu-id="03ee3-113">Errors have occurred during TLSNEGO/SPNEGO handshake.</span></span>
