---
title: 'Service : Nombre d’échecs de la validation de la sécurité et de l’authentification'
ms.date: 03/30/2017
ms.assetid: 55c98268-b1ad-459d-851b-25ef52248187
ms.openlocfilehash: 5843d25eb26bdd9facc324a2af50c6b02c5ad7c8
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64613580"
---
# <a name="service-security-validation-and-authentication-failures"></a><span data-ttu-id="7ed44-102">Service : Nombre d’échecs de la validation de la sécurité et de l’authentification</span><span class="sxs-lookup"><span data-stu-id="7ed44-102">Service: Security Validation and Authentication Failures</span></span>
<span data-ttu-id="7ed44-103">Nom du compteur : Nombre d’échecs de la validation de la sécurité et de l’authentification</span><span class="sxs-lookup"><span data-stu-id="7ed44-103">Counter name: Security Validation and Authentication Failures</span></span>  
  
## <a name="description"></a><span data-ttu-id="7ed44-104">Description</span><span class="sxs-lookup"><span data-stu-id="7ed44-104">Description</span></span>  
 <span data-ttu-id="7ed44-105">Ce compteur est incrémenté chaque fois qu'un message est rejeté en raison d'un problème de sécurité non couvert par le compteur « Appels de sécurité non autorisés ».</span><span class="sxs-lookup"><span data-stu-id="7ed44-105">This counter is incremented whenever a message is rejected due to a security problem not covered by the "Security Calls Not Authorized" counter.</span></span> <span data-ttu-id="7ed44-106">Ces problèmes sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="7ed44-106">Such problems include:</span></span>  
  
- <span data-ttu-id="7ed44-107">Impossibilité de lire le jeton client depuis le message.</span><span class="sxs-lookup"><span data-stu-id="7ed44-107">Client token cannot be read from the message.</span></span>  
  
- <span data-ttu-id="7ed44-108">Échec de l'authentification du jeton client (par exemple, mot de passe incorrect).</span><span class="sxs-lookup"><span data-stu-id="7ed44-108">Client token has failed authentication (for example,, bad password).</span></span>  
  
- <span data-ttu-id="7ed44-109">Échec de la vérification de signature (par exemple, falsification du message).</span><span class="sxs-lookup"><span data-stu-id="7ed44-109">Signature verification has failed (for example,, the message has been tampered).</span></span>  
  
- <span data-ttu-id="7ed44-110">Le message est un doublon d'un message précédent, ce qui peut se produire lors d'une attaque par relecture.</span><span class="sxs-lookup"><span data-stu-id="7ed44-110">The message is a duplicate from a previous one, which can happen during a replay attack.</span></span>  
  
- <span data-ttu-id="7ed44-111">Impossibilité de déchiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="7ed44-111">A decryption failure has occurred.</span></span>  
  
- <span data-ttu-id="7ed44-112">Absence de certains éléments requis dans le message (par exemple, horodateur ou bloc de données chiffrées manquant).</span><span class="sxs-lookup"><span data-stu-id="7ed44-112">Some required elements (for example,, missing timestamp or encrypted data block) are missing from the message.</span></span>  
  
- <span data-ttu-id="7ed44-113">Erreurs lors de la négociation TLSNEGO/SPNEGO.</span><span class="sxs-lookup"><span data-stu-id="7ed44-113">Errors have occurred during TLSNEGO/SPNEGO handshake.</span></span>
