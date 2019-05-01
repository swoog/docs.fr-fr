---
title: Vue d'ensemble des sessions fiables
ms.date: 03/30/2017
ms.assetid: a7fc4146-ee2c-444c-82d4-ef6faffccc2d
ms.openlocfilehash: 6dd90ef800daf236d77c419d48c0857ac2d78aa2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61962654"
---
# <a name="reliable-sessions-overview"></a>Vue d'ensemble des sessions fiables

Windows Communication Foundation (WCF) de messagerie fiable SOAP fournit la fiabilité de transfert de message de bout en bout entre les points de terminaison SOAP. Elle permet cela sur des réseaux peu fiables en remédiant aux échecs de transport et aux échecs au niveau du message SOAP. Notamment, elle fournit une remise basée sur session, unique et ordonnée (facultativement) pour les messages envoyés via SOAP ou des intermédiaires de transport. La remise basée sur session fournit pour le regroupement des messages dans une session avec un ordonnancement facultatif des messages.

Cette rubrique décrit les sessions fiables, comment et quand les utiliser et comment les sécuriser.

## <a name="wcf-reliable-sessions"></a>Sessions fiables WCF

Les sessions fiables WCF est une implémentation de SOAP reliable messaging tel que défini par le protocole WS-ReliableMessaging.

Messagerie fiable SOAP WCF fournit une session fiable de bout en bout entre deux points de terminaison, quel que soit le nombre ou le type d’intermédiaires qui séparent les points de terminaison de messagerie. Cela inclut tous les transports qui n’utilisent pas SOAP (par exemple, les proxys HTTP) ou intermédiaires qui utilisent le protocole SOAP (par exemple, les routeurs SOAP ou les ponts) qui sont requis pour les messages de circuler entre les points de terminaison. Un canal de session fiable prend en charge *interactive* communication afin que les services connectés par ce canal s’exécuteront simultanément et échanger et traiter des messages dans des conditions de latence basse, autrement dit, au sein de relativement courts intervalles de temps. Ce couplage signifie que ces composants progressent ensemble ou échouent ensemble, donc il n’existe aucune isolation assurée entre eux.

Une session fiable masque deux types d'échecs :

- Échecs au niveau du message SOAP, incluant les messages perdus ou dupliqués et les messages qui arrivent dans un ordre différent de l'ordre dans lequel ils ont été envoyés.

- Échecs de transport

Une session fiable implémente le protocole WS-ReliableMessaging et une fenêtre de transfert en mémoire pour masquer les échecs au niveau du message SOAP et rétablit des connexions en cas d'échecs de transport.

Une session fiable gère les messages SOAP de la même façon que TCP gère les paquets IP. Une connexion de socket TCP fournit un transfert unique et symétrique des paquets IP entre les nœuds. Le canal fiable fournit le même type de transfert fiable, mais il diffère de la fiabilité fournie par le socket TCP des façons suivantes :

- La fiabilité est fournie au niveau du message SOAP, non pour un paquet d'octets arbitrairement dimensionné.

- La fiabilité est indépendant du transport, pas seulement pour le transfert sur TCP.

- La fiabilité n’est pas liée à une session de transport particulier (par exemple, la session fournit une connexion TCP) et plusieurs sessions de transport peut utiliser simultanément ou séquentiellement sur la durée de vie de la session fiable.

- La session fiable existe entre les points de terminaison SOAP de l'expéditeur et du récepteur, indépendamment du nombre de connexions de transport requis pour la connectivité entre eux. En bref, la fiabilité TCP termine où la connexion de transport se termine, pendant une session fiable fournit une fiabilité de bout en bout.

## <a name="reliable-sessions-and-bindings"></a>Liaisons et les sessions fiables

Comme mentionné précédemment, une session fiable est indépendant du transport. En outre, vous pouvez établir une session fiable sur nombreux modèles d’échange de message, telles que la demande-réponse ou duplex. Une session fiable de WCF est exposée en tant que propriété d’un ensemble de liaisons.

Utiliser une session fiable sur les points de terminaison qui utilisent :

- Des liaisons standard de transport basées sur HTTP :

  - `WsHttpBinding` et expose des contrats demande-réponse ou unidirectionnels.

  - Lors de l’utilisation de session fiable sur une demande-réponse ou d’un contrat de service unidirectionnel simple.

  - `WsDualHttpBinding` et expose des contrats duplex, demande-réponse ou unidirectionnels.

  - `WsFederationHttpBinding` et expose des contrats demande-réponse ou unidirectionnels.

- Des liaisons standard de transport basées sur TCP :

  - `NetTcpBinding` et expose des contrats duplex, demande-réponse ou unidirectionnels.

Utiliser une session fiable sur toutes les autres liaisons en créant une liaison personnalisée, tel que HTTPS (pour plus d’informations sur les problèmes, consultez <a href="#reliable-sessions-and-security">les sessions fiables et sécurité</a>) ou une liaison de canal nommé.

Vous pouvez empiler une session fiable sur différents types de canaux sous-jacente, et la forme de canal de session fiable résultante varie. Sur le client et le serveur, le type de canal de session fiable pris en charge varie selon le type de canal sous-jacent utilisé. Le tableau suivant répertorie les types de canaux de session pris en charge sur le client en fonction du type de canal sous-jacent.

| Prise en charge des types de canaux de session fiable&#8224; | `IRequestChannel` | `IRequestSessionChannel` | `IDuplexChannel` | `IDuplexSessionChannel` |
| ----------------------------------------------- | :---------------: | :----------------------: | :--------------: | :---------------------: |
| `IOutputSessionChannel`                         | Oui               | Oui                      | Oui              | Oui                     |
| `IRequestSessionChannel`                        | Oui               | Oui                      | Non               | Non                      |
| `IDuplexSessionChannel`                         | Non                | Non                       | Oui              | Oui                     |

&#8224;Les types de canaux pris en charge sont les valeurs disponibles pour le modèle générique `TChannel` valeur du paramètre qui est passé dans le <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.BuildChannelFactory%60%601%28System.ServiceModel.Channels.BindingContext%29> (méthode).

Le tableau suivant répertorie les types de canaux de session pris en charge sur le serveur en fonction du type de canal sous-jacent.

| Prise en charge des types de canaux de session fiable&#8225; | `IReplyChannel` | `IReplySessionChannel` | `IDuplexChannel` | `IDuplexSessionChannel` |
| ----------------------------------------------- | :-------------: | :--------------------: | :--------------: | :---------------------: |
| `IInputSessionChannel`                          | Oui             | Oui                    | Oui              | Oui                     |
| `IReplySessionChannel`                          | Oui             | Oui                    | Non               | Non                      |
| `IDuplexSessionChannel`                         | Non              | Non                     | Oui              | Oui                     |

&#8225;Les types de canaux pris en charge sont les valeurs disponibles pour le modèle générique `TChannel` valeur du paramètre qui est passé dans le <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.BuildChannelListener%60%601%28System.ServiceModel.Channels.BindingContext%29> (méthode).

## <a name="reliable-sessions-and-security"></a>Sécurité et les sessions fiables

La sécurisation d’une session fiable est important de s’assurer que les parties qui communiquent (service et client) sont authentifiés et que les messages échangés dans la session ne sont pas falsifiés. En outre, il est important de garantir l’intégrité de chaque session fiable. Une session fiable est sécurisée en la liant à un contexte de sécurité qui a représenté et géré par un canal de session de sécurité. Le canal de sécurité fournit une session de sécurité. Les jetons de sécurité échangés pendant l'établissement de la session sont ensuite utilisés pour sécuriser les messages dans la session fiable.

Lorsqu’une session fiable est sur TCP-S, la session TCP est liée à la session fiable. Par conséquent, la sécurité de transport garantit que sécurité est également liée à la session fiable. Dans ce cas, le rétablissement de la connexion est désactivé.

La seule exception est l'utilisation du protocole HTTPS. La session de Secure Sockets Layer (SSL) n’est pas liée à la session fiable. Cela constitue une menace, car les sessions qui partagent un contexte de sécurité (la session SSL) ne sont pas protégées entre eux ; Cela peut ou peut ne pas être une véritable menace, selon l’application.

## <a name="using-reliable-sessions"></a>À l’aide de sessions fiables

Pour utiliser des sessions fiables WCF, créez un point de terminaison avec une liaison qui prend en charge une session fiable. Utilisez une des liaisons fournies par le système WCF offre de la session fiable est activée ou créer votre propre liaison personnalisée qui s’en charge.

Les liaisons définies par le système qui prennent en charge et activent une session fiable par défaut incluent :

- <xref:System.ServiceModel.WSDualHttpBinding>

Les liaisons fournies par le système qui prennent en charge une session fiable en option mais ne l’activez un par défaut sont les suivantes :

- <xref:System.ServiceModel.WSHttpBinding>

- <xref:System.ServiceModel.WSFederationHttpBinding>

- <xref:System.ServiceModel.NetTcpBinding>

Pour obtenir un exemple montrant comment créer une liaison personnalisée, consultez [Comment : Créer une liaison de Session fiable personnalisée avec le protocole HTTPS](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md).

Pour une discussion des liaisons WCF qui prennent en charge des sessions fiables, consultez [System-Provided Bindings](../../../../docs/framework/wcf/system-provided-bindings.md).

## <a name="when-to-use-reliable-sessions"></a>Quand utiliser des sessions fiables

Il est important de comprendre quand utiliser des sessions fiables dans votre application. WCF prend en charge les sessions fiables entre les points de terminaison qui sont actifs en même temps. Si votre application nécessite un point de terminaison soit indisponible pour une certaine durée, puis utiliser les files d’attente pour assurer la fiabilité.

Si le scénario requiert deux points de terminaison connectés via TCP, TCP peut-être être suffisante pour fournir des échanges de messages fiable. Bien qu’il n’est pas nécessaire d’utiliser une session fiable, étant donné que TCP garantit que les paquets arrivent dans l’ordre et une seule fois.

Si votre scénario présente l’une des caractéristiques suivantes, vous devez sérieusement envisager à l’aide d’une session fiable.

- Intermédiaires SOAP, tels que les routeurs SOAP

- Intermédiaires proxy ou ponts de transport

- Connectivité intermittente

- Sessions sur HTTP

## <a name="see-also"></a>Voir aussi

- [Utilisation de liaisons pour configurer des services et des clients](../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [Session fiable WS](../../../../docs/framework/wcf/samples/ws-reliable-session.md)
