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
ms.openlocfilehash: 9a2cd06c4c5a73d9fb5c4c7f09632e10c3eb0d87
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61991157"
---
# <a name="reliable-sessions"></a>Sessions fiables

Cette section décrit quelles un Windows Communication Foundation (WCF) est de la session fiable, à quoi il sert, comment et quand utiliser, quelles configurations de liaison prennent en charge et des pointeurs sur les meilleures pratiques. Le tableau suivant résume les détails sur les points essentiels et les rubriques connexes de cette section.

La session fiable WCF fournit des fonctionnalités en vous assurant que les messages envoyés entre les points de terminaison sont transférés via des intermédiaires SOAP ou de transport et sont remis une seule fois et, éventuellement, dans le même ordre que celui dans lequel ils ont été envoyés.

Pour utiliser une session fiable avec une application WCF, utilisez une des liaisons fournies par le système dans WCF qui prennent en charge une session fiable par défaut ou en tant qu’option ou créer votre propre liaison personnalisée qui prend en charge de la session.

## <a name="in-this-section"></a>Dans cette section

[Vue d’ensemble des Sessions fiables](../../../../docs/framework/wcf/feature-details/reliable-sessions-overview.md) décrit des sessions fiables, quand les utiliser, les différentes liaisons qui prennent en charge des sessions fiables, et leur fonctionnement.

[Guide pratique pour Exchange Messages au sein d’une Session fiable](../../../../docs/framework/wcf/feature-details/how-to-exchange-messages-within-a-reliable-session.md) décrit comment créer une session fiable sur HTTP à l’aide d’une liaison personnalisée spécifiée dans la configuration.

[Guide pratique pour Sécuriser des Messages au sein de Sessions fiables](../../../../docs/framework/wcf/feature-details/how-to-secure-messages-within-reliable-sessions.md) explique comment sécuriser une session fiable.

[Guide pratique pour Créer une liaison Session fiable personnalisée avec le protocole HTTPS](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md) décrit comment créer une session fiable sur HTTPS.

[Meilleures pratiques pour les Sessions fiables](../../../../docs/framework/wcf/feature-details/best-practices-for-reliable-sessions.md) décrit quelques-unes des meilleures pratiques associées à l’aide d’une session fiable.

## <a name="reference"></a>Référence

<xref:System.ServiceModel.ReliableSession>

## <a name="see-also"></a>Voir aussi

- [Files d’attente et sessions fiables](../../../../docs/framework/wcf/feature-details/queues-and-reliable-sessions.md)
- [Sessions, instanciation et accès concurrentiel](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)
