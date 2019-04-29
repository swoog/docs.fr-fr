---
title: Suivis principaux
ms.date: 03/30/2017
ms.assetid: 40a1770e-3b09-4142-b0dd-f9ef73642074
ms.openlocfilehash: c230c65b4d3fd45c4905d4ae5f4cbbf90e10faad
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61784947"
---
# <a name="significant-traces"></a>Suivis principaux
Cette rubrique répertorie certains des suivis principaux émis par Windows Communication Foundation (WCF).  
  
## <a name="significant-traces"></a>Suivis principaux  
  
|Suivi|Description|  
|-----------|-----------------|  
|Suivi du journal des messages|Le suivi est émis lorsqu’un message WCF est enregistré par la journalisation des messages fonctionnalité lors la `System.ServiceModel.MessageLogging` source de suivi est activé. Un clic sur ce suivi permet d'afficher le message. Il existe quatre points d'enregistrement configurables pour un message : `ServiceLevelSendRequest`, `TransportSend`, `TransportReceive`, `ServiceLevelReceiveRequest`, également indiqués par l'attribut Message Source dans le suivi du journal des messages.|  
|Suivi de message reçu|Ce suivi est émis lorsqu’un message WCF est reçu si le `System.ServiceModel` source de suivi est activé au niveau des informations ou commentaires. Ce suivi est nécessaire pour consulter la flèche de corrélation du message dans la vue du graphique d'activité.|  
|Suivi de message envoyé|Ce suivi est émis lorsqu’un message WCF est envoyé si le `System.ServiceModel` source de suivi est activé au niveau des informations ou commentaires. Ce suivi est nécessaire pour consulter la flèche de corrélation du message dans la vue du graphique d'activité.|  
|Obtenir ChannelEndpointElement|Ce suivi est émis dans la fabrication de canal Construct, au niveau des informations. Il fournit une description du point de terminaison auquel le client parle (adresse distante, liaison, nom de contrat).|  
|Obtenir ServiceElement|Ce suivi est émis dans l'hôte du service Construct, au niveau des informations. Elle fournit une description du contrat de service et de la liaison.|  
|Créer SocketConnection|Ce suivi est émis dans la première action Process exécutée par le client et dans l'activité Receive bytes du service. Il fournit les adresses IP locales et distantes. Il est émis au niveau Informations.|
