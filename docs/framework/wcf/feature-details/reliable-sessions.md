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
# <a name="reliable-sessions"></a>Sessions fiables

Cette section décrit les un Windows Communication Foundation (WCF) une session fiable est qu’elle sert, comment et quand utiliser, quelles configurations de liaison prend en charge, et des pointeurs sur les meilleures pratiques. Le tableau suivant résume les détails sur les points essentiels et les rubriques connexes de cette section.

La session fiable WCF fournit featrues en garantissant que les messages envoyés entre des points de terminaison sont transférées via des intermédiaires SOAP ou de transport et sont remis une seule fois et, éventuellement, dans le même ordre que celui dans lequel ils ont été envoyés.

Pour utiliser une session fiable avec une application WCF, utilisez une des liaisons fournies par le système dans WCF qui prennent en charge une session fiable par défaut ou en tant qu’option ou créer votre propre liaison personnalisée qui prend en charge de la session.

## <a name="in-this-section"></a>Dans cette section

[Vue d’ensemble des Sessions fiables](../../../../docs/framework/wcf/feature-details/reliable-sessions-overview.md)   
Décrit des sessions fiables, quand les utiliser, les différentes liaisons qui prennent en charge des sessions fiables, et leur fonctionnement.

[Comment : échanger des Messages dans une Session fiable](../../../../docs/framework/wcf/feature-details/how-to-exchange-messages-within-a-reliable-session.md)   
Décrit comment créer une session fiable sur HTTP à l’aide d’une liaison personnalisée spécifiée dans la configuration.

[Comment : sécuriser des Messages dans des Sessions fiables](../../../../docs/framework/wcf/feature-details/how-to-secure-messages-within-reliable-sessions.md)   
Décrit comment sécuriser une session fiable.

[Comment : créer une liaison personnalisée de Session fiable avec HTTPS](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md)   
Décrit comment créer une session fiable sur HTTPS.

[Meilleures pratiques pour les Sessions fiables](../../../../docs/framework/wcf/feature-details/best-practices-for-reliable-sessions.md)   
Décrit certaines meilleures pratiques associées à l'utilisation d'une session fiable.

## <a name="reference"></a>Référence

<xref:System.ServiceModel.ReliableSession>

## <a name="see-also"></a>Voir aussi

[Les files d’attente et les Sessions fiables](../../../../docs/framework/wcf/feature-details/queues-and-reliable-sessions.md)   
[Sessions, instanciation et accès concurrentiel](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)
