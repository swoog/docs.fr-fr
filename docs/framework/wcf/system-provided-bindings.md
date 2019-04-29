---
title: Liaisons fournies par le système
description: Découvrez toutes les liaisons WCF (Windows Communication Foundation) fournies par le système.
ms.date: 06/05/2018
helpviewer_keywords:
- bindings [WCF], system-provided
ms.assetid: 2c243746-45ce-4588-995e-c17126a579a6
ms.openlocfilehash: 3c6c6b628d208aede8c547dcfa66fc189a26ae01
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61791506"
---
# <a name="system-provided-bindings"></a>Liaisons fournies par le système

Les liaisons spécifient le mécanisme de communication à utiliser pour communiquer avec un point de terminaison et indiquer comment se connecter à un point de terminaison. Une liaison contient les éléments suivants :

- La pile de protocole détermine la sécurité, la fiabilité et les paramètres de flux de contexte à utiliser pour les messages envoyés au point de terminaison.

- Le transport détermine le protocole de transport sous-jacent à utiliser lors de l'envoi des messages au point de terminaison, par exemple, TCP ou HTTP.

- L’encodage détermine l’encodage de câble à utiliser pour les messages envoyés au point de terminaison. Par exemple, texte/XML, binaire ou MTOM (Message Transmission Optimization Mechanism).

 Cet article présente toutes les liaisons WCF (Windows Communication Foundation) fournies par le système. Si aucune de ces liaisons ne répond aux critères exacts de votre application, vous pouvez créer une liaison personnalisée. Pour plus d’informations sur la création de liaisons personnalisées, consultez [Liaisons personnalisées](./extending/custom-bindings.md).

 Une liaison sécurisée et interopérable qui prend en charge le protocole WS-Federation permet aux organisations qui sont dans une fédération d’authentifier et d’autoriser efficacement les utilisateurs.

> [!IMPORTANT]
> Sélectionnez toujours une liaison qui inclut la sécurité. Par défaut, la sécurité est activée pour toutes les liaisons, à l’exception de l’élément [\<basicHttpBinding>](../configure-apps/file-schema/wcf/basichttpbinding.md). Si vous ne sélectionnez pas de liaison sécurisée ou désactivez la sécurité, veillez à protéger vos données d’une manière ou d’une autre, telle que le stockage dans un centre de données sécurisé ou sur un réseau isolé.

> [!IMPORTANT]
> N’utilisez jamais des contrats duplex avec les liaisons qui ne prennent pas en charge la sécurité ou dont la sécurité est désactivée sauf si vous sécurisez les données d’un moyen ou un autre.

Les liaisons suivantes sont fournies avec WCF :

|Liaison|Élément de configuration|Description|
|-------------|---------------------------|-----------------|
|<xref:System.ServiceModel.BasicHttpBinding>|[\<basicHttpBinding>](../configure-apps/file-schema/wcf/basichttpbinding.md)|Liaison appropriée à la communication avec les services web conformes au profil WS-Basic, par exemple les services basés sur les services web ASP.NET (ASMX). Cette liaison utilise HTTP comme le transport et texte/XML comme encodage de message par défaut.|
|<xref:System.ServiceModel.WSHttpBinding>|[\<wsHttpBinding>](../configure-apps/file-schema/wcf/wshttpbinding.md)|Une liaison sécurisée et interopérable adaptée aux contrats de service non duplex.|
|<xref:System.ServiceModel.WSDualHttpBinding>|[\<wsDualHttpBinding>](../configure-apps/file-schema/wcf/wsdualhttpbinding.md)|Une liaison sécurisée et interopérable appropriée pour les contrats de service duplex ou les communications par le biais des intermédiaires SOAP.|
|<xref:System.ServiceModel.WSFederationHttpBinding>|[\<wsFederationHttpBinding>](../configure-apps/file-schema/wcf/wsfederationhttpbinding.md)|Liaison sécurisée et interopérable prenant en charge le protocole WS-Federation, ce qui permet aux organisations membres d’une fédération d’appliquer efficacement des procédures d’authentification et d’autorisation aux utilisateurs.|
|<xref:System.ServiceModel.NetHttpBinding>|[\<netHttpBinding>](../configure-apps/file-schema/wcf/nethttpbinding.md)|Liaison conçue pour consommer des services HTTP ou WebSocket qui utilise l’encodage binaire par défaut.|
|<xref:System.ServiceModel.NetHttpsBinding>|[\<netHttpsBinding>](../configure-apps/file-schema/wcf/nethttpsbinding.md)|Liaison sécurisée conçue pour consommer des services HTTP ou WebSocket qui utilise l'encodage binaire par défaut.|
|<xref:System.ServiceModel.NetTcpBinding>|[\<netTcpBinding>](../configure-apps/file-schema/wcf/nettcpbinding.md)|Liaison sécurisée et optimisée, adaptée à la communication des applications WCF entre les machines.|
|<xref:System.ServiceModel.NetNamedPipeBinding>|[\<netNamedPipeBinding>](../configure-apps/file-schema/wcf/netnamedpipebinding.md)|Liaison sécurisée, fiable et optimisée adaptée à la communication des applications WCF sur les machines.|
|<xref:System.ServiceModel.NetMsmqBinding>|[\<netMsmqBinding>](../configure-apps/file-schema/wcf/netmsmqbinding.md)|Liaison en file d’attente adaptée à la communication des applications WCF entre les machines.|
|<xref:System.ServiceModel.NetPeerTcpBinding>|[\<netPeerTcpBinding>](../configure-apps/file-schema/wcf/netpeertcpbinding.md)|Une liaison qui permet la communication sécurisée entre plusieurs ordinateurs.|
|<xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding>|[\<msmqIntegrationBinding>](../configure-apps/file-schema/wcf/msmqintegrationbinding.md)|Liaison adaptée à la communication d’une application WCF avec des applications Message Queuing entre les machines.|
|<xref:System.ServiceModel.BasicHttpContextBinding>|[\<basicHttpContextBinding>](../configure-apps/file-schema/wcf/basichttpcontextbinding.md)|Liaison adaptée à la communication avec les services web conformes au profil WS-Basic, ce qui permet l’utilisation de cookies HTTP pour l’échange de contexte.|
|<xref:System.ServiceModel.NetTcpContextBinding>|[\<netTcpContextBinding>](../configure-apps/file-schema/wcf/nettcpcontextbinding.md)|Liaison sécurisée et optimisée adaptée à la communication des applications WCF entre les machines, ce qui permet l’utilisation d’en-têtes SOAP pour l’échange de contexte.|
|<xref:System.ServiceModel.WebHttpBinding>|[\<webHttpBinding>](../configure-apps/file-schema/wcf/webhttpbinding.md)|Liaison utilisée afin de configurer des points de terminaison pour les services web WCF qui sont exposés via des requêtes HTTP au lieu de messages SOAP.|
|<xref:System.ServiceModel.WSHttpContextBinding>|[\<wsHttpContextBinding>](../configure-apps/file-schema/wcf/wshttpcontextbinding.md)|Liaison sécurisée et interopérable adaptée aux contrats de service non duplex, ce qui permet l’utilisation d’en-têtes SOAP pour l’échange de contexte.|
|<xref:System.ServiceModel.UdpBinding>|[\<udpBinding>](../configure-apps/file-schema/wcf/udpbinding.md)|Liaison à utiliser lors de l'envoi d'une rafale de messages simples à un grand nombre de clients simultanément.|

 Le tableau suivant affiche les fonctionnalités de chacune des liaisons fournies par le système. Les liaisons figurent dans les colonnes du tableau ; les fonctionnalités sont répertoriées dans les lignes et décrites dans un deuxième tableau. Le tableau suivant fournit une clé pour les abréviations de liaison utilisées. Pour sélectionner une liaison, déterminez quelle colonne satisfait toutes les fonctionnalités de ligne dont vous avez besoin.

|Liaison|Interopérabilité|Sécurité (valeur par défaut)|Session<br />(Default)|Transactions|Duplex|Encodage (Valeur par défaut)|Diffusion en continu<br />(Default)|
|-------------|----------------------|--------------------------|-----------------------------|------------------|------------|--------------------------|-------------------------------|
|<xref:System.ServiceModel.BasicHttpBinding>|Basic Profile 1.1|(Aucun), transport, message, mixte|(Aucun)|(Aucun)|N/A|Texte, (MTOM)|Oui<br />(mis en mémoire tampon)|
|<xref:System.ServiceModel.WSHttpBinding>|WS|Transport, (message), mixte|(Aucun), session fiable, session de sécurité|(Aucun), oui|N/A|(Texte), MTOM|Non|
|<xref:System.ServiceModel.WSDualHttpBinding>|WS|(Message), aucun|(Session fiable), session de sécurité|(Aucun), oui|Oui|(Texte), MTOM|Non|
|<xref:System.ServiceModel.WSFederationHttpBinding>|WS-Federation|(Message), mixte, aucun|(Aucun), session fiable, session de sécurité|(Aucun), oui|Non|(Texte), MTOM|Non|
|<xref:System.ServiceModel.NetHttpBinding>|.NET|(None), Transport, Message, TransportWithMessageCredential, TransportCredentialOnly|Voir la remarque ci-dessous|Aucun.|Voir la remarque ci-dessous|(Binaire), Texte, MTOM|Oui (mis en mémoire tampon)|
|<xref:System.ServiceModel.NetHttpsBinding>|.NET|(Transport), TransportWithMessageCredential|Voir la remarque ci-dessous|Aucun.|Voir la remarque ci-dessous|(Binaire), Texte, MTOM|Oui<br />(mis en mémoire tampon)|
|<xref:System.ServiceModel.NetTcpBinding>|.NET|(Transport), message, aucun, mixte|(Transport), session fiable, session de sécurité|(Aucun), oui|Oui|Binaire|Oui<br />(mis en mémoire tampon)|
|<xref:System.ServiceModel.NetNamedPipeBinding>|.NET|(Transport), aucun|Aucun, (Transport)|(Aucun), oui|Oui|Binaire|Oui<br />(mis en mémoire tampon)|
|<xref:System.ServiceModel.NetMsmqBinding>|.NET|Message, (Transport), Aucun|(Aucun), Transport|Aucun, (Oui)|Non|Binaire|Non|
|<xref:System.ServiceModel.NetPeerTcpBinding>|Peer|(Transport)|(Aucun)|(Aucun)|Oui||Non|
|<xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding>|MSMQ|(Transport)|(Aucun)|Aucun, (Oui)|N/A|N/A|Non|
|<xref:System.ServiceModel.BasicHttpContextBinding>|Basic Profile 1.1|(Aucun), transport, message, mixte|(Aucun)|(Aucun)|N/A|Texte, (MTOM)|Oui<br />(mis en mémoire tampon)|
|<xref:System.ServiceModel.NetTcpContextBinding>|.NET|(Transport), message, aucun, mixte|(Transport), session fiable, session de sécurité|(Aucun), oui|Oui|Binaire|Oui<br />(mis en mémoire tampon)|
|<xref:System.ServiceModel.WSHttpContextBinding>|WS|Transport, (message), mixte|(Aucun), session fiable, session de sécurité|(Aucun), oui|N/A|Texte, (MTOM)|Non|
|<xref:System.ServiceModel.UdpBinding> <br /><br /> **Remarque :**  L’interopérabilité peut être obtenue en implémentant la spécification standard SOAP sur UDP implémentée par cette liaison.|.NET|(Aucun)|(Aucun)|(Aucun)|N/A|(Texte)|Non|

> [!IMPORTANT]
> <xref:System.ServiceModel.NetHttpBinding> est une liaison conçue pour consommer des services HTTP ou WebSocket et utilise l'encodage binaire par défaut. <xref:System.ServiceModel.NetHttpBinding> détecte s’il est utilisé avec un contrat de requête-réponse ou un contrat duplex, puis change son comportement de manière appropriée. Il utilise le protocole HTTP pour les contrats de requête-réponse et WebSockets pour les contrats duplex. Ce comportement peut être remplacé à l’aide de le <xref:System.ServiceModel.Channels.WebSocketTransportUsage> paramètre de liaison : WhenDuplex - Il s'agit de la valeur par défaut et elle se comporte de la façon décrite ci-dessus. Jamais - Empêche l'utilisation de WebSockets. Toute tentative d’utilisation d’un contrat duplex avec ce paramètre entraîne une exception. Toujours - Force l'utilisation de WebSockets même pour les contrats de demande-réponse. NetHttpBinding prend en charge les sessions fiables en mode HTTP et en mode WebSocket. Les sessions en mode WebSocket sont fournies par le transport.

 Le tableau suivant explique les fonctionnalités répertoriées dans le tableau précédent.

|Fonctionnalité|Description|
|-------------|-----------------|
|Type d'interopérabilité|Nomme le protocole ou la technologie avec laquelle la liaison garantit l'interopérabilité.|
|Sécurité|Définit le mode de sécurisation du canal :<br />-None : Le message SOAP n’est pas sécurisé et le client n’est pas authentifié.<br />-Transport : Exigences de sécurité sont satisfaites au niveau de la couche de transport.<br />-Message : Exigences de sécurité sont satisfaites au niveau de la couche de message.<br />-Mixte : Revendications sont contenues dans le message. les exigences de l’intégrité et la confidentialité sont satisfaites par la couche de transport.|
|Session|Spécifie si cette liaison prend en charge des contrats de session.|
|Transactions|Spécifie si les transactions sont activées.|
|Duplex|Spécifie si les contrats duplex sont pris en charge. Notez que cette fonctionnalité requiert la prise en charge des sessions dans la liaison.|
|Encodage|Spécifie le format de câble du message. Les valeurs autorisées incluent :<br />- Texte : UTF-8, par exemple.<br />- Binaire<br />-Message Transmission Optimization Mechanism (MTOM) : Une méthode permettant d’encoder efficacement des éléments XML binaires dans le contexte d’une enveloppe SOAP.|
|Diffusion en continu|Spécifie si la diffusion en continu est prise en charge pour les messages entrants et sortants. Utilisez la propriété `TransferMode` sur la liaison pour définir la valeur. Les valeurs autorisées incluent :<br />- <xref:System.ServiceModel.TransferMode.Buffered> : Les messages de demande et de réponse sont mis en mémoire tampon.<br />- <xref:System.ServiceModel.TransferMode.Streamed> : Les messages de demande et de réponse sont transmis en continu.<br />- <xref:System.ServiceModel.TransferMode.StreamedRequest> : Le message de demande est transmis en continu et le message de réponse est mis en mémoire tampon.<br />- <xref:System.ServiceModel.TransferMode.StreamedResponse> : Le message de demande est mis en mémoire tampon et le message de réponse est transmis en continu.|

## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la création de points de terminaison](endpoint-creation-overview.md)
- [Utilisation de liaisons pour configurer des services et des clients](using-bindings-to-configure-services-and-clients.md)
- [Programmation WCF de base](basic-wcf-programming.md)
