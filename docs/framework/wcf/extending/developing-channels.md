---
title: Développement de canaux
ms.date: 03/30/2017
ms.assetid: 0513af9f-a0c2-457b-9a50-5b6bfee48513
ms.openlocfilehash: 74a54972ffa7d00d702a2339665d18acdcbf93ef
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54519136"
---
# <a name="developing-channels"></a>Développement de canaux
Pour développer un canal de transport ou protocole qui peut être utilisé avec Windows Communication Foundation (WCF), couche d’application nécessite plusieurs étapes. Cette rubrique liste ces étapes et renvoie à des rubriques spécifiques qui vous permettront d'en savoir plus. Pour comprendre le modèle de canal et les différents types qui sont mentionnées dans cette rubrique, consultez [vue d’ensemble du modèle de canal](../../../../docs/framework/wcf/extending/channel-model-overview.md). Pour voir un exemple de canal de transport complet, [Transport : UDP](../../../../docs/framework/wcf/samples/transport-udp.md).  
  
## <a name="the-channel-development-task-list"></a>Liste des tâches à effectuer dans le cadre du développement d’un canal  
 Les étapes pour créer un canal défini par l'utilisateur sont les suivantes : Pour tous les canaux :  
  
1.  Choisissez quel modèle d’échange de messages de canal (<xref:System.ServiceModel.Channels.IOutputChannel>, <xref:System.ServiceModel.Channels.IInputChannel>, <xref:System.ServiceModel.Channels.IDuplexChannel>, <xref:System.ServiceModel.Channels.IRequestChannel> ou <xref:System.ServiceModel.Channels.IReplyChannel>) que vos <xref:System.ServiceModel.Channels.IChannelFactory> et <xref:System.ServiceModel.Channels.IChannelListener> prendront en charge. Décidez également si ces derniers devront prendre en charge les versions avec session de ces interfaces. Pour plus d’informations, consultez [en choisissant un modèle d’échange de Message](../../../../docs/framework/wcf/extending/choosing-a-message-exchange-pattern.md).  
  
2.  Créez une fabrication de canal ainsi qu’un écouteur (<xref:System.ServiceModel.Channels.IChannelFactory> et <xref:System.ServiceModel.Channels.IChannelListener>) qui prennent en charge votre modèle d’échange de messages. Pour plus d’informations sur le développement des fabrications, consultez [Client : Fabriques de canaux et canaux](../../../../docs/framework/wcf/extending/client-channel-factories-and-channels.md). Pour plus d’informations sur le développement des écouteurs, consultez [Service : Écouteurs de canal et canaux](../../../../docs/framework/wcf/extending/service-channel-listeners-and-channels.md).  
  
3.  Assurez-vous que toutes les exceptions spécifiques au réseau sont normalisées en fonction de <xref:System.TimeoutException?displayProperty=nameWithType> ou de la classe dérivée appropriée de <xref:System.ServiceModel.CommunicationException>. Pour plus d’informations, consultez [gestion des Exceptions et erreurs](../../../../docs/framework/wcf/extending/handling-exceptions-and-faults.md).  
  
4.  Pour permettre une utilisation depuis la couche d'application, ajoutez un <xref:System.ServiceModel.Channels.BindingElement> qui ajoute votre canal personnalisé à la pile des canaux. Pour plus d’informations, consultez [création d’un élément BindingElement](../../../../docs/framework/wcf/extending/creating-a-bindingelement.md).  
  
 Les étapes supplémentaires suivantes sont requises pour permettre une prise en charge plus exhaustive au niveau de la couche d'application :  
  
1.  Ajoutez une section d’extension d’élément de liaison afin d’exposer le nouvel élément de liaison au système de configuration. Pour plus d’informations, consultez [Configuration et la prise en charge des métadonnées](../../../../docs/framework/wcf/extending/configuration-and-metadata-support.md).  
  
2.  Ajoutez des extensions de métadonnées pour communiquer des fonctionnalités à d'autres points de terminaison. Pour plus d’informations, consultez [Configuration et la prise en charge des métadonnées](../../../../docs/framework/wcf/extending/configuration-and-metadata-support.md).  
  
3.  Ajoutez une liaison qui préconfigure une pile d’éléments de liaison d’après un profil bien défini. Pour plus d’informations, consultez [Creating liaisons](../../../../docs/framework/wcf/extending/creating-user-defined-bindings.md).  
  
4.  Ajoutez une section de liaison ainsi qu’un élément de configuration de liaison afin d’exposer la liaison au système de configuration. Pour plus d’informations, consultez [Configuration et la prise en charge des métadonnées](../../../../docs/framework/wcf/extending/configuration-and-metadata-support.md).  
  
## <a name="see-also"></a>Voir aussi
- [Extension de liaisons](../../../../docs/framework/wcf/extending/extending-bindings.md)
