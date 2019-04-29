---
title: Transports dans Windows Communication Foundation
ms.date: 03/30/2017
helpviewer_keywords:
- transports [WCF]
- WCF, transports
- Windows Communication Foundation, transports
ms.assetid: 005c894b-af70-48aa-a1c1-c99338083c27
ms.openlocfilehash: 6bb8e8b90c26533661684bd403b9ec439f1bb37e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61933729"
---
# <a name="transports-in-windows-communication-foundation"></a>Transports dans Windows Communication Foundation
La couche de transport se situe au niveau le plus bas de la pile des canaux. Les principaux transports utilisés dans Windows Communication Foundation (WCF) sont HTTP, HTTPS, TCP et canaux nommés. Les rubriques de cette section contiennent des conseils et des instructions permettant de savoir quel protocole choisir, de le configurer et de définir les propriétés de réglage afférentes.  
  
 WCF inclut des transports supplémentaires. Pour plus d’informations sur le transport Message Queuing (également appelé MSMQ), consultez [files d’attente et Sessions fiables](../../../../docs/framework/wcf/feature-details/queues-and-reliable-sessions.md). Pour plus d’informations sur le transport de peer-to-peer, consultez [mise en réseau Peer-to-Peer](../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md).  
  
## <a name="in-this-section"></a>Dans cette section  
 [Choix d’un transport](../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)  
 Présente les trois transports principaux et aborde les différents points à prendre en considération lors de leur sélection.  
  
 [Sélection d’un encodeur de message](../../../../docs/framework/wcf/feature-details/choosing-a-message-encoder.md)  
 Aborde les facteurs à prendre en considération lors de la sélection d’un élément de liaison d’encodage de message.  
  
 [Transfert des messages par streaming](../../../../docs/framework/wcf/feature-details/streaming-message-transfer.md)  
 Contient des instructions permettant de configurer la couche de transport pour une diffusion en continu.  
  
 [Configuration de HTTP et HTTPS](../../../../docs/framework/wcf/feature-details/configuring-http-and-https.md)  
 Contient des instructions permettant de configurer les éléments de liaison de transport HTTP et HTTPS.  
  
 [Guide pratique pour Remplacer la réservation d’URL WCF par une réservation restreinte](../../../../docs/framework/wcf/feature-details/how-to-replace-the-wcf-url-reservation-with-a-restricted-reservation.md)  
 Décrit comment utiliser les réservations WCFURL restreint.  
  
 [Quotas de transport](../../../../docs/framework/wcf/feature-details/transport-quotas.md)  
 Aborde les points à prendre en considération lors de la définition de quotas pour la couche de transport.  
  
 [Utilisation des NAT et des pare-feu](../../../../docs/framework/wcf/feature-details/working-with-nats-and-firewalls.md)  
 Contient des instructions permettant de configurer la couche de transport lorsque les messages envoyés ou reçus rencontrent un pare-feu ou lorsqu'un traducteur d'adresses réseau (NAT) est utilisé.  
  
 [Partage de ports Net.TCP](../../../../docs/framework/wcf/feature-details/net-tcp-port-sharing.md)  
 Décrit comment utiliser le composant Partage de Port Net.TCP de WCF.  
  
## <a name="reference"></a>Référence  
 <xref:System.ServiceModel.Channels.HttpTransportBindingElement>  
  
 <xref:System.ServiceModel.Channels.HttpsTransportBindingElement>  
  
 <xref:System.ServiceModel.Channels.TcpTransportBindingElement>  
  
 <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement>  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Liaisons](../../../../docs/framework/wcf/feature-details/bindings.md)  
  
 [Extension de liaisons](../../../../docs/framework/wcf/extending/extending-bindings.md)
