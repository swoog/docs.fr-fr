---
title: 'Service : nombre d’échecs de la validation de la sécurité et de l’authentification'
ms.date: 03/30/2017
ms.assetid: 55c98268-b1ad-459d-851b-25ef52248187
ms.openlocfilehash: ba8da3ae6be6bd089690359f19e153da1e0b54fc
ms.sourcegitcommit: 5fd80619c760fa8c25d33a6f5661247cb65da465
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2018
ms.locfileid: "50744247"
---
# <a name="service-security-validation-and-authentication-failures"></a><span data-ttu-id="f1682-102">Service : nombre d’échecs de la validation de la sécurité et de l’authentification</span><span class="sxs-lookup"><span data-stu-id="f1682-102">Service: Security Validation and Authentication Failures</span></span>
<span data-ttu-id="f1682-103">Nom de compteur : nombre d’échecs de la validation de la sécurité et de l’authentification</span><span class="sxs-lookup"><span data-stu-id="f1682-103">Counter name: Security Validation and Authentication Failures</span></span>  
  
## <a name="description"></a><span data-ttu-id="f1682-104">Description</span><span class="sxs-lookup"><span data-stu-id="f1682-104">Description</span></span>  
 <span data-ttu-id="f1682-105">Ce compteur est incrémenté chaque fois qu'un message est rejeté en raison d'un problème de sécurité non couvert par le compteur « Appels de sécurité non autorisés ».</span><span class="sxs-lookup"><span data-stu-id="f1682-105">This counter is incremented whenever a message is rejected due to a security problem not covered by the "Security Calls Not Authorized" counter.</span></span> <span data-ttu-id="f1682-106">Ces problèmes sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="f1682-106">Such problems include:</span></span>  
  
-   <span data-ttu-id="f1682-107">Impossibilité de lire le jeton client depuis le message.</span><span class="sxs-lookup"><span data-stu-id="f1682-107">Client token cannot be read from the message.</span></span>  
  
-   <span data-ttu-id="f1682-108">Échec de l'authentification du jeton client (par exemple, mot de passe incorrect).</span><span class="sxs-lookup"><span data-stu-id="f1682-108">Client token has failed authentication (for example,, bad password).</span></span>  
  
-   <span data-ttu-id="f1682-109">Échec de la vérification de signature (par exemple, falsification du message).</span><span class="sxs-lookup"><span data-stu-id="f1682-109">Signature verification has failed (for example,, the message has been tampered).</span></span>  
  
-   <span data-ttu-id="f1682-110">Le message est un doublon d'un message précédent, ce qui peut se produire lors d'une attaque par relecture.</span><span class="sxs-lookup"><span data-stu-id="f1682-110">The message is a duplicate from a previous one, which can happen during a replay attack.</span></span>  
  
-   <span data-ttu-id="f1682-111">Impossibilité de déchiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="f1682-111">A decryption failure has occurred.</span></span>  
  
-   <span data-ttu-id="f1682-112">Absence de certains éléments requis dans le message (par exemple, horodateur ou bloc de données chiffrées manquant).</span><span class="sxs-lookup"><span data-stu-id="f1682-112">Some required elements (for example,, missing timestamp or encrypted data block) are missing from the message.</span></span>  
  
-   <span data-ttu-id="f1682-113">Erreurs lors de la négociation TLSNEGO/SPNEGO.</span><span class="sxs-lookup"><span data-stu-id="f1682-113">Errors have occurred during TLSNEGO/SPNEGO handshake.</span></span>
