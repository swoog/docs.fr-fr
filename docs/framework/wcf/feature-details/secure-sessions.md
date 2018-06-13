---
title: Sessions sécurisées
ms.date: 03/30/2017
ms.assetid: 7b50602f-d7b5-42e9-8e92-1f0413df0d8b
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 1c7229fba8e30632f08834eb36c1fb177de7a294
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33497540"
---
# <a name="secure-sessions"></a><span data-ttu-id="d838e-102">Sessions sécurisées</span><span class="sxs-lookup"><span data-stu-id="d838e-102">Secure Sessions</span></span>
<span data-ttu-id="d838e-103">Une fonctionnalité de Windows Communication Foundation (WCF) est sessions fiables garantissent que les messages sont reçus dans l’ordre qu’ils ont été envoyés.</span><span class="sxs-lookup"><span data-stu-id="d838e-103">A feature of Windows Communication Foundation (WCF) is reliable sessions that guarantee messages are received in the order they were sent.</span></span> <span data-ttu-id="d838e-104">Les rubriques de cette section traitent des implications de sécurité à considérer lors de la création d'une session fiable.</span><span class="sxs-lookup"><span data-stu-id="d838e-104">The topics in this section discuss the security implications to consider when creating a reliable session.</span></span> <span data-ttu-id="d838e-105">Pour plus d’informations sur les sessions fiables, consultez [à l’aide de Sessions](../../../../docs/framework/wcf/using-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="d838e-105">For more information about reliable sessions, see [Using Sessions](../../../../docs/framework/wcf/using-sessions.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d838e-106">Lorsque l’emprunt d’identité est requis sur Windows XP, utilisez une session sécurisée sans jeton de contexte de sécurité avec état (SCT).</span><span class="sxs-lookup"><span data-stu-id="d838e-106">When impersonation is required on Windows XP, use a secure session without a stateful security context token (SCT).</span></span> <span data-ttu-id="d838e-107">Lorsque des SCT avec état sont utilisés avec l'emprunt d'identité, une <xref:System.InvalidOperationException> est levée.</span><span class="sxs-lookup"><span data-stu-id="d838e-107">When stateful SCTs are used with impersonation, an <xref:System.InvalidOperationException> is thrown.</span></span> <span data-ttu-id="d838e-108">Pour plus d’informations, consultez [scénarios non pris en charge](../../../../docs/framework/wcf/feature-details/unsupported-scenarios.md).</span><span class="sxs-lookup"><span data-stu-id="d838e-108">For more information, see [Unsupported Scenarios](../../../../docs/framework/wcf/feature-details/unsupported-scenarios.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="d838e-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d838e-109">In This Section</span></span>  
  
|||  
|-|-|  
|[<span data-ttu-id="d838e-110">Conversations sécurisées et sessions sécurisées</span><span class="sxs-lookup"><span data-stu-id="d838e-110">Secure Conversations and Secure Sessions</span></span>](../../../../docs/framework/wcf/feature-details/secure-conversations-and-secure-sessions.md)|<span data-ttu-id="d838e-111">Les termes « conversations sécurisées » et « sessions sécurisées » sont synonymes.</span><span class="sxs-lookup"><span data-stu-id="d838e-111">Secure conversations and secure sessions are synonymous.</span></span> <span data-ttu-id="d838e-112">Cette rubrique explique le fonctionnement d’une conversation sécurisée et quand et pourquoi utiliser le modèle.</span><span class="sxs-lookup"><span data-stu-id="d838e-112">This topic explains the way a secure conversation works, and when and why to use the pattern.</span></span>|  
|[<span data-ttu-id="d838e-113">Guide pratique pour créer une session sécurisée</span><span class="sxs-lookup"><span data-stu-id="d838e-113">How to: Create a Secure Session</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-secure-session.md)|<span data-ttu-id="d838e-114">Présente les étapes essentielles de la création d'une session sécurisée.</span><span class="sxs-lookup"><span data-stu-id="d838e-114">Walks through of the basics of creating a secure session.</span></span>|  
|[<span data-ttu-id="d838e-115">Guide pratique pour créer un jeton de contexte de sécurité pour une session sécurisée</span><span class="sxs-lookup"><span data-stu-id="d838e-115">How to: Create a Security Context Token for a Secure Session</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-security-context-token-for-a-secure-session.md)|<span data-ttu-id="d838e-116">Présente les étapes nécessaires à la création d'une batterie de serveurs Web qui maintiendra l'état et les sessions avec les clients.</span><span class="sxs-lookup"><span data-stu-id="d838e-116">Walks through the steps of creating a Web farm that will maintain state and sessions with clients.</span></span>|  
|[<span data-ttu-id="d838e-117">Considérations sur la sécurité pour les sessions sécurisées</span><span class="sxs-lookup"><span data-stu-id="d838e-117">Security Considerations for Secure Sessions</span></span>](../../../../docs/framework/wcf/feature-details/security-considerations-for-secure-sessions.md)|<span data-ttu-id="d838e-118">Décrit des considérations spéciales relatives aux sessions sécurisées.</span><span class="sxs-lookup"><span data-stu-id="d838e-118">Describes special considerations for secure sessions.</span></span>|  
  
## <a name="reference"></a><span data-ttu-id="d838e-119">Référence</span><span class="sxs-lookup"><span data-stu-id="d838e-119">Reference</span></span>  
 <xref:System.ServiceModel>  
  
 <xref:System.ServiceModel.Channels>  
  
## <a name="related-sections"></a><span data-ttu-id="d838e-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d838e-120">Related Sections</span></span>  
 [<span data-ttu-id="d838e-121">Sessions, instanciation et accès concurrentiel</span><span class="sxs-lookup"><span data-stu-id="d838e-121">Sessions, Instancing, and Concurrency</span></span>](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)  
  
 [<span data-ttu-id="d838e-122">Conception et implémentation de services</span><span class="sxs-lookup"><span data-stu-id="d838e-122">Designing and Implementing Services</span></span>](../../../../docs/framework/wcf/designing-and-implementing-services.md)  
  
## <a name="see-also"></a><span data-ttu-id="d838e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d838e-123">See Also</span></span>  
 [<span data-ttu-id="d838e-124">Guide pratique pour activer la détection de relecture des messages</span><span class="sxs-lookup"><span data-stu-id="d838e-124">How to: Enable Message Replay Detection</span></span>](../../../../docs/framework/wcf/feature-details/how-to-enable-message-replay-detection.md)  
 [<span data-ttu-id="d838e-125">Attaques par relecture</span><span class="sxs-lookup"><span data-stu-id="d838e-125">Replay Attacks</span></span>](../../../../docs/framework/wcf/feature-details/replay-attacks.md)  
 [<span data-ttu-id="d838e-126">Guide pratique pour créer un service qui requiert des sessions</span><span class="sxs-lookup"><span data-stu-id="d838e-126">How to: Create a Service That Requires Sessions</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-service-that-requires-sessions.md)
