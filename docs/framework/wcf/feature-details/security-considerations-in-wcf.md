---
title: Considérations relatives à la sécurité dans WCF
ms.date: 03/30/2017
helpviewer_keywords:
- security [WCF]
- Windows Communication Foundation, security
- WCF, security
ms.assetid: 42055ee0-6d0c-443d-9d89-788dfc345d6d
ms.openlocfilehash: 16b3afe9540f3e2953311f602408fce5412be2eb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62000764"
---
# <a name="security-considerations-in-wcf"></a><span data-ttu-id="984b6-102">Considérations relatives à la sécurité dans WCF</span><span class="sxs-lookup"><span data-stu-id="984b6-102">Security Considerations in WCF</span></span>
<span data-ttu-id="984b6-103">Les rubriques de cette section répertorient les divers éléments relatifs à la sécurité à prendre en compte lorsque vous concevez une application Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="984b6-103">The topics in this section list various security-related items to consider when designing a Windows Communication Foundation (WCF) application.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="984b6-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="984b6-104">In This Section</span></span>  
 [<span data-ttu-id="984b6-105">Divulgation d’informations</span><span class="sxs-lookup"><span data-stu-id="984b6-105">Information Disclosure</span></span>](../../../../docs/framework/wcf/feature-details/information-disclosure.md)  
 <span data-ttu-id="984b6-106">Traite des diverses manières dont les informations peuvent être divulguées ou attaquées, et de la manière de limiter ce risque.</span><span class="sxs-lookup"><span data-stu-id="984b6-106">Discusses the various ways that information can be disclosed or attacked, and how to mitigate this.</span></span>  
  
 [<span data-ttu-id="984b6-107">Élévation de privilèges</span><span class="sxs-lookup"><span data-stu-id="984b6-107">Elevation of Privilege</span></span>](../../../../docs/framework/wcf/feature-details/elevation-of-privilege.md)  
 <span data-ttu-id="984b6-108">Traite des conséquences de l'attribution à un intrus d'autorisations plus étendues celles accordées initialement, et de la manière de limiter ce risque.</span><span class="sxs-lookup"><span data-stu-id="984b6-108">Discusses the effects of giving an attacker authorization permissions beyond those initially granted and how to mitigate this.</span></span>  
  
 [<span data-ttu-id="984b6-109">Déni de service</span><span class="sxs-lookup"><span data-stu-id="984b6-109">Denial of Service</span></span>](../../../../docs/framework/wcf/feature-details/denial-of-service.md)  
 <span data-ttu-id="984b6-110">Traite de ce qui arrive lorsqu'un système ne peut pas traiter des messages convenablement, et de la manière de limiter ce risque.</span><span class="sxs-lookup"><span data-stu-id="984b6-110">Discusses what happens when a system is unable to process messages appropriately and how to mitigate it.</span></span>  
  
 [<span data-ttu-id="984b6-111">Falsification</span><span class="sxs-lookup"><span data-stu-id="984b6-111">Tampering</span></span>](../../../../docs/framework/wcf/feature-details/tampering.md)  
 <span data-ttu-id="984b6-112">Traite de la modification des messages ou de la remise des messages, et de la manière de limiter ce risque.</span><span class="sxs-lookup"><span data-stu-id="984b6-112">Discusses the altering of messages or the delivery of messages and how to mitigate it.</span></span>  
  
 [<span data-ttu-id="984b6-113">Attaques par relecture</span><span class="sxs-lookup"><span data-stu-id="984b6-113">Replay Attacks</span></span>](../../../../docs/framework/wcf/feature-details/replay-attacks.md)  
 <span data-ttu-id="984b6-114">Traite de ce qui arrive lorsqu'un intrus copie un flux de messages entre deux correspondants et relit le flux à l'un des correspondants ou les deux, et de la manière de limiter ce risque.</span><span class="sxs-lookup"><span data-stu-id="984b6-114">Discusses what happens when an attacker copies a stream of messages between two parties and replays the stream to one or more of the parties, and how to mitigate this.</span></span>  
  
 [<span data-ttu-id="984b6-115">Considérations sur la sécurité pour les sessions sécurisées</span><span class="sxs-lookup"><span data-stu-id="984b6-115">Security Considerations for Secure Sessions</span></span>](../../../../docs/framework/wcf/feature-details/security-considerations-for-secure-sessions.md)  
 <span data-ttu-id="984b6-116">Traite des éléments suivants qui affectent la sécurité lors de l'implémentation de sessions sécurisées.</span><span class="sxs-lookup"><span data-stu-id="984b6-116">Discusses the following items that affect security when implementing secure sessions.</span></span>  
  
 [<span data-ttu-id="984b6-117">Scénarios non pris en charge</span><span class="sxs-lookup"><span data-stu-id="984b6-117">Unsupported Scenarios</span></span>](../../../../docs/framework/wcf/feature-details/unsupported-scenarios.md)  
 <span data-ttu-id="984b6-118">Répertorie différents scénarios qui ne prennent pas en charge un aspect particulier de la sécurité et qui doivent être évités ou pris en compte.</span><span class="sxs-lookup"><span data-stu-id="984b6-118">Lists various scenarios that do not support a particular aspect of security and should be avoided or considered.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="984b6-119">Référence</span><span class="sxs-lookup"><span data-stu-id="984b6-119">Reference</span></span>  
 <xref:System.IdentityModel.Tokens>  
  
 <xref:System.IdentityModel.Claims>  
  
 <xref:System.ServiceModel.Security>  
  
 <xref:System.ServiceModel>  
  
## <a name="related-sections"></a><span data-ttu-id="984b6-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="984b6-120">Related Sections</span></span>  
 [<span data-ttu-id="984b6-121">Aide sur la sécurité et bonnes pratiques</span><span class="sxs-lookup"><span data-stu-id="984b6-121">Security Guidance and Best Practices</span></span>](../../../../docs/framework/wcf/feature-details/security-guidance-and-best-practices.md)  
  
## <a name="see-also"></a><span data-ttu-id="984b6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="984b6-122">See also</span></span>

- [<span data-ttu-id="984b6-123">Sécurité</span><span class="sxs-lookup"><span data-stu-id="984b6-123">Security</span></span>](../../../../docs/framework/wcf/feature-details/security.md)
