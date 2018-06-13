---
title: Sessions fiables
ms.date: 03/30/2017
f1_keywords:
- Windows Communication Foundation, sessions and instances
- WCF, sessions and instances
- sessions and instances [WCF]
helpviewer_keywords:
- instances [WCF]
- sessions [WCF]
ms.assetid: 143951b3-3aa0-4540-b4b7-d33e77e874a1
ms.openlocfilehash: 396c76cbdb8eada881a5c87edfc2500dcdab3ad4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33497163"
---
# <a name="reliable-sessions"></a><span data-ttu-id="9051b-102">Sessions fiables</span><span class="sxs-lookup"><span data-stu-id="9051b-102">Reliable Sessions</span></span>

<span data-ttu-id="9051b-103">Cette section décrit les un Windows Communication Foundation (WCF) une session fiable est qu’elle sert, comment et quand utiliser, quelles configurations de liaison prend en charge, et des pointeurs sur les meilleures pratiques.</span><span class="sxs-lookup"><span data-stu-id="9051b-103">This section describes what a Windows Communication Foundation (WCF) reliable session is, what it's used for, how and when to use one, what binding configurations support it, and pointers on best practices.</span></span> <span data-ttu-id="9051b-104">Le tableau suivant résume les détails sur les points essentiels et les rubriques connexes de cette section.</span><span class="sxs-lookup"><span data-stu-id="9051b-104">The following table summarizes details about the essential points and related topics in this section.</span></span>

<span data-ttu-id="9051b-105">La session fiable WCF fournit featrues en garantissant que les messages envoyés entre des points de terminaison sont transférées via des intermédiaires SOAP ou de transport et sont remis une seule fois et, éventuellement, dans le même ordre que celui dans lequel ils ont été envoyés.</span><span class="sxs-lookup"><span data-stu-id="9051b-105">The reliable session WCF provides featrues ensuring that messages sent between endpoints are transferred across SOAP or transport intermediaries and are delivered only once and, optionally, in the same order in which they were sent.</span></span>

<span data-ttu-id="9051b-106">Pour utiliser une session fiable avec une application WCF, utilisez une des liaisons fournies par le système dans WCF qui prennent en charge une session fiable par défaut ou en tant qu’option ou créer votre propre liaison personnalisée qui prend en charge de la session.</span><span class="sxs-lookup"><span data-stu-id="9051b-106">To use a reliable session with a WCF application, either use one of the system-provided bindings in WCF that support a reliable session by default or as an option, or create your own custom binding that supports the session.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9051b-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="9051b-107">In This Section</span></span>

<span data-ttu-id="9051b-108">[Vue d’ensemble des Sessions fiables](../../../../docs/framework/wcf/feature-details/reliable-sessions-overview.md) </span><span class="sxs-lookup"><span data-stu-id="9051b-108">[Reliable Sessions Overview](../../../../docs/framework/wcf/feature-details/reliable-sessions-overview.md) </span></span>  
<span data-ttu-id="9051b-109">Décrit des sessions fiables, quand les utiliser, les différentes liaisons qui prennent en charge des sessions fiables, et leur fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="9051b-109">Describes reliable sessions, when to use them, the different bindings that support reliable sessions, and how they work.</span></span>

<span data-ttu-id="9051b-110">[Comment : échanger des Messages dans une Session fiable](../../../../docs/framework/wcf/feature-details/how-to-exchange-messages-within-a-reliable-session.md) </span><span class="sxs-lookup"><span data-stu-id="9051b-110">[How to: Exchange Messages Within a Reliable Session](../../../../docs/framework/wcf/feature-details/how-to-exchange-messages-within-a-reliable-session.md) </span></span>  
<span data-ttu-id="9051b-111">Décrit comment créer une session fiable sur HTTP à l’aide d’une liaison personnalisée spécifiée dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="9051b-111">Describes how to create a reliable session over HTTP using a custom binding specified in the configuration.</span></span>

<span data-ttu-id="9051b-112">[Comment : sécuriser des Messages dans des Sessions fiables](../../../../docs/framework/wcf/feature-details/how-to-secure-messages-within-reliable-sessions.md) </span><span class="sxs-lookup"><span data-stu-id="9051b-112">[How to: Secure Messages within Reliable Sessions](../../../../docs/framework/wcf/feature-details/how-to-secure-messages-within-reliable-sessions.md) </span></span>  
<span data-ttu-id="9051b-113">Décrit comment sécuriser une session fiable.</span><span class="sxs-lookup"><span data-stu-id="9051b-113">Describes how to secure a reliable session.</span></span>

<span data-ttu-id="9051b-114">[Comment : créer une liaison personnalisée de Session fiable avec HTTPS](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md) </span><span class="sxs-lookup"><span data-stu-id="9051b-114">[How to: Create a Custom Reliable Session Binding with HTTPS](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md) </span></span>  
<span data-ttu-id="9051b-115">Décrit comment créer une session fiable sur HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9051b-115">Describes how to create a reliable session over HTTPS.</span></span>

<span data-ttu-id="9051b-116">[Meilleures pratiques pour les Sessions fiables](../../../../docs/framework/wcf/feature-details/best-practices-for-reliable-sessions.md) </span><span class="sxs-lookup"><span data-stu-id="9051b-116">[Best Practices for Reliable Sessions](../../../../docs/framework/wcf/feature-details/best-practices-for-reliable-sessions.md) </span></span>  
<span data-ttu-id="9051b-117">Décrit certaines meilleures pratiques associées à l'utilisation d'une session fiable.</span><span class="sxs-lookup"><span data-stu-id="9051b-117">Describes some of the best practices associated with using a reliable session.</span></span>

## <a name="reference"></a><span data-ttu-id="9051b-118">Référence</span><span class="sxs-lookup"><span data-stu-id="9051b-118">Reference</span></span>

<xref:System.ServiceModel.ReliableSession>

## <a name="see-also"></a><span data-ttu-id="9051b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9051b-119">See Also</span></span>

<span data-ttu-id="9051b-120">[Les files d’attente et les Sessions fiables](../../../../docs/framework/wcf/feature-details/queues-and-reliable-sessions.md) </span><span class="sxs-lookup"><span data-stu-id="9051b-120">[Queues and Reliable Sessions](../../../../docs/framework/wcf/feature-details/queues-and-reliable-sessions.md) </span></span>  
[<span data-ttu-id="9051b-121">Sessions, instanciation et accès concurrentiel</span><span class="sxs-lookup"><span data-stu-id="9051b-121">Sessions, Instancing, and Concurrency</span></span>](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)
