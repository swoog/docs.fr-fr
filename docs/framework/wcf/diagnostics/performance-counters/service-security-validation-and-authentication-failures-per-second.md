---
title: 'Service : nombre d’échecs de la validation de la sécurité et de l’authentification par seconde'
ms.date: 03/30/2017
ms.assetid: 4af18009-e778-490b-9ba6-e76485285830
author: BrucePerlerMS
ms.openlocfilehash: 2e67a2222f3d605fdd7bb408380743203a551dd6
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47110461"
---
# <a name="service-security-validation-and-authentication-failures-per-second"></a><span data-ttu-id="0781a-102">Service : nombre d’échecs de la validation de la sécurité et de l’authentification par seconde</span><span class="sxs-lookup"><span data-stu-id="0781a-102">Service: Security Validation and Authentication Failures Per Second</span></span>
<span data-ttu-id="0781a-103">Nom du compteur : nombre d’échecs de la validation de la sécurité et de l’authentification par seconde.</span><span class="sxs-lookup"><span data-stu-id="0781a-103">Counter name: Security Validation and Authentication Failures Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="0781a-104">Description</span><span class="sxs-lookup"><span data-stu-id="0781a-104">Description</span></span>  
 <span data-ttu-id="0781a-105">Ce compteur est incrémenté chaque fois qu'un message est rejeté en raison d'un problème de sécurité non couvert par le compteur « Appels de sécurité non autorisés ».</span><span class="sxs-lookup"><span data-stu-id="0781a-105">This counter is incremented whenever a message is rejected due to a security problem not covered by the "Security Calls Not Authorized" counter.</span></span> <span data-ttu-id="0781a-106">Ces problèmes sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="0781a-106">Such problems include:</span></span>  
  
-   <span data-ttu-id="0781a-107">Impossibilité de lire le jeton client depuis le message.</span><span class="sxs-lookup"><span data-stu-id="0781a-107">Client token cannot be read from the message.</span></span>  
  
-   <span data-ttu-id="0781a-108">Échec de l'authentification du jeton client (par exemple, mot de passe incorrect).</span><span class="sxs-lookup"><span data-stu-id="0781a-108">Client token has failed authentication (for example, bad password).</span></span>  
  
-   <span data-ttu-id="0781a-109">Échec de la vérification de signature (par exemple, falsification du message).</span><span class="sxs-lookup"><span data-stu-id="0781a-109">Signature verification has failed (for example, the message has been tampered).</span></span>  
  
-   <span data-ttu-id="0781a-110">Le message est un doublon d'un message précédent, ce qui peut se produire lors d'une attaque par relecture.</span><span class="sxs-lookup"><span data-stu-id="0781a-110">The message is a duplicate from a previous one, which can happen during a replay attack.</span></span>  
  
-   <span data-ttu-id="0781a-111">Impossibilité de déchiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="0781a-111">A decryption failure has occurred.</span></span>  
  
-   <span data-ttu-id="0781a-112">Absence de certains éléments requis dans le message (par exemple, horodatage ou bloc des données chiffrées manquant).</span><span class="sxs-lookup"><span data-stu-id="0781a-112">Some required elements (for example, missing timestamp or encrypted data block) are missing from the message.</span></span>  
  
-   <span data-ttu-id="0781a-113">Erreurs lors de la négociation TLSNEGO/SPNEGO.</span><span class="sxs-lookup"><span data-stu-id="0781a-113">Errors have occurred during TLSNEGO/SPNEGO handshake.</span></span>  
  
 <span data-ttu-id="0781a-114">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante,</span><span class="sxs-lookup"><span data-stu-id="0781a-114">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula,</span></span>  
  
 <span data-ttu-id="0781a-115">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="0781a-115">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
