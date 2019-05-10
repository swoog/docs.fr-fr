---
title: Architecture du client
ms.date: 03/30/2017
ms.assetid: 02624403-0d77-41cb-9a86-ab55e98c7966
ms.openlocfilehash: 6ed00054de45abc23fdd9ad69f61c758f567b973
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64656055"
---
# <a name="client-architecture"></a>Architecture du client
Applications utilisent des objets de client Windows Communication Foundation (WCF) pour appeler des opérations de service. Cette rubrique traite des objets de client WCF, canaux de client WCF et leurs relations à l’architecture de canal sous-jacente. Pour obtenir une vue d’ensemble d’objets de client WCF, consultez [WCF Client Overview](../../../../docs/framework/wcf/wcf-client-overview.md). Pour plus d’informations sur la couche de canal, consultez [extension de la couche de canal](../../../../docs/framework/wcf/extending/extending-the-channel-layer.md).  
  
## <a name="overview"></a>Vue d'ensemble  
 L’exécution de modèle de service crée des clients WCF, qui sont composées des éléments suivants :  
  
- Implémentation de client générée automatiquement d'un contrat de service qui transforme les appels de votre code d'application en messages sortants, les messages de réponse en paramètres de sortie et retourne des valeurs pouvant être récupérées par votre application.  
  
- Implémentation d'une interface de contrôle (<xref:System.ServiceModel.IClientChannel?displayProperty=nameWithType>) qui regroupe différentes interfaces et fournit l'accès au contrôle des fonctionnalités, plus précisément aux fonctionnalités permettant de fermer la session client et de déployer le canal.  
  
- Canal de client construit en fonction des paramètres de configuration spécifiés par la liaison utilisée.  
  
 Applications peuvent créer des clients à la demande, soit par le biais une <xref:System.ServiceModel.ChannelFactory?displayProperty=nameWithType> ou en créant une instance d’un <xref:System.ServiceModel.ClientBase%601> classe dérivée comme il est généré par le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md). Ces classes de client déjà construites encapsulent une implémentation de canal de client construite dynamiquement par un <xref:System.ServiceModel.ChannelFactory> et délèguent vers cette implémentation. Par conséquent, cette rubrique traite principalement des canaux de client et de la fabrication de canal à leur origine.  
  
## <a name="client-objects-and-client-channels"></a>Objets et canaux de client  
 L’interface de base de clients WCF est le <xref:System.ServiceModel.IClientChannel?displayProperty=nameWithType> interface qui expose la fonctionnalité principale de client, ainsi que la fonctionnalité d’objet de communication de base de <xref:System.ServiceModel.ICommunicationObject?displayProperty=nameWithType>, la fonctionnalité de contexte de <xref:System.ServiceModel.IContextChannel?displayProperty=nameWithType>et le comportement extensible de <xref:System.ServiceModel.IExtensibleObject%601?displayProperty=nameWithType>.  
  
 Toutefois, l'interface <xref:System.ServiceModel.IClientChannel> ne définit pas de contrat de service. Ces contrats sont déclarés par l’interface de contrat de service (généralement généré à partir des métadonnées de service à l’aide d’un outil tel que le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)). Types de client WCF étendent à la fois <xref:System.ServiceModel.IClientChannel> et l’interface de contrat de service cible pour permettre aux applications d’appeler des opérations directement et également avoir accès aux fonctionnalités d’exécution côté client. Création d’un client WCF fournit WCF<xref:System.ServiceModel.ChannelFactory?displayProperty=nameWithType> avec les informations nécessaires pour créer un processus d’exécution des objets qui peuvent se connecter et interagir avec le point de terminaison de service configuré.  
  
 Comme mentionné précédemment, les deux types de client WCF doivent être configurés avant de pouvoir les utiliser. Les types de client WCF plus simples sont des objets qui dérivent de <xref:System.ServiceModel.ClientBase%601> (ou <xref:System.ServiceModel.DuplexClientBase%601> si le contrat de service est un contrat duplex). Vous pouvez créer ces types en utilisant un constructeur (ou un fichier de configuration) configuré par un programme, puis appelé directement pour appeler les opérations de service. Pour une vue d’ensemble de <xref:System.ServiceModel.ClientBase%601> , consultez [WCF Client Overview](../../../../docs/framework/wcf/wcf-client-overview.md).  
  
 Le second type est généré pendant l'exécution depuis un appel de la méthode <xref:System.ServiceModel.ChannelFactory%601.CreateChannel%2A>. Applications à obtenir un contrôle plus strict des spécificités de communication généralement utiliser ce type de client, appelé un *objet de canal client*, car elle permet d’interagir plus directement que le runtime sous-jacent client et le canal système.  
  
## <a name="channel-factories"></a>Fabrication de canal  
 La classe qui est chargée de créer le processus d'exécution sous-jacent prenant en charge les appels de client correspond à <xref:System.ServiceModel.ChannelFactory%601?displayProperty=nameWithType>. Utilisation d’objets de canal à la fois les objets de client WCF et client WCF un <xref:System.ServiceModel.ChannelFactory%601> objet pour créer des instances ; le <xref:System.ServiceModel.ClientBase%601> objet de client dérivé encapsule la gestion de la fabrication de canal, mais pour un nombre de scénarios, il est tout à fait raisonnable d’utiliser le fabrique de canaux directement. Vous souhaiterez le plus souvent créer à plusieurs reprises de nouveaux canaux de client à partir de la fabrication de canal existante. Si vous utilisez un objet client, vous pouvez obtenir la fabrique de canal sous-jacente à partir d’un objet de client WCF en appelant le <xref:System.ServiceModel.ClientBase%601.ChannelFactory%2A?displayProperty=nameWithType> propriété.  
  
 Concernant les fabrications de canaux, il est important de garder à l'esprit qu'elles créent des nouvelles instances de canaux de client pour la configuration fournie avant l'appel de la méthode <xref:System.ServiceModel.ChannelFactory%601.CreateChannel%2A?displayProperty=nameWithType>. Une fois que vous appelez <xref:System.ServiceModel.ChannelFactory%601.CreateChannel%2A> (ou <xref:System.ServiceModel.ClientBase%601.Open%2A?displayProperty=nameWithType>, <xref:System.ServiceModel.ClientBase%601.CreateChannel%2A?displayProperty=nameWithType>, ou de toute opération sur un objet de client WCF), vous ne pouvez pas modifier la fabrique de canaux et s’attendre à obtenir des canaux vers différentes instances de service, même si vous modifiez l’adresse de point de terminaison cible. Si vous souhaitez créer un objet de client ou un canal de client avec une configuration différente, vous devez d'abord créer une nouvelle fabrication de canal.  
  
 Pour plus d’informations sur les différents problèmes à l’aide d’objets de client WCF et les canaux de client WCF, consultez [Services d’accès à l’aide d’un Client WCF](../../../../docs/framework/wcf/feature-details/accessing-services-using-a-client.md).  
  
 Les deux sections suivantes décrivent la création et l’utilisation d’objets de canal de client WCF.  
  
#### <a name="creating-a-new-wcf-client-channel-object"></a>Création d'un nouvel objet de canal de client WCF  
 Dans notre exemple illustrant l'utilisation d'un canal de client, nous supposons que le contrat de service suivant a été généré.  
  
 [!code-csharp[C_GeneratedCodeFiles#12](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_generatedcodefiles/cs/proxycode.cs#12)]  
  
 Pour vous connecter à un service `ISampleService`, utilisez l'interface de contrat générée directement avec une fabrication de canal (<xref:System.ServiceModel.ChannelFactory%601>). Après avoir créé et configuré une fabrication de canal pour un contrat particulier, vous pouvez appeler la méthode <xref:System.ServiceModel.ChannelFactory%601.CreateChannel%2A> pour retourner des objets de canal de client qui vous permettront de communiquer avec un service `ISampleService`.  
  
 Lorsque vous utilisez la classe <xref:System.ServiceModel.ChannelFactory%601> avec une interface de contrat de service, vous devez effectuer une conversion de type dans l'interface <xref:System.ServiceModel.IClientChannel> pour ouvrir, fermer ou abandonner le canal de manière explicite. Pour faciliter son utilisation, l'outil Svcutil.exe génère également une interface d'assistance qui implémente à la fois l'interface de contrat de service et <xref:System.ServiceModel.IClientChannel> afin de vous permettre d'interagir avec l'infrastructure de canal client sans devoir convertir de type. Le code suivant illustre la définition d'un canal client d'assistance qui implémente le contrat de service précédent.  
  
 [!code-csharp[C_GeneratedCodeFiles#13](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_generatedcodefiles/cs/proxycode.cs#13)]  
  
#### <a name="creating-a-new-wcf-client-channel-object"></a>Création d'un nouvel objet de canal de client WCF  
 Pour utiliser un canal client et se connecter à un service `ISampleService`, utilisez directement l’interface de contrat générée (ou la version d’assistance) avec une fabrication de canal, en passant le type de l’interface de contrat comme paramètre de type. Après avoir créé et configuré une fabrication de canal pour un contrat particulier, vous pouvez appeler la méthode <xref:System.ServiceModel.ChannelFactory%601.CreateChannel%2A?displayProperty=nameWithType> pour retourner des objets de canal client qui vous permettront de communiquer avec un service `ISampleService`.  
  
 Une fois créés, les objets de canal de client implémentent <xref:System.ServiceModel.IClientChannel> ainsi que l'interface de contrat. Par conséquent, vous pouvez les utiliser directement pour appeler les opérations qui interagissent avec un service prenant en charge le contrat.  
  
 La différence entre les objets de client et les objets de canal de client réside dans leurs modalités de contrôle et leur simplicité d'utilisation. De nombreux développeurs qui sont à l’aise utilisation des classes et objets préfèrent utiliser l’objet de client WCF au lieu du canal de client WCF.  
  
 Pour voir un exemple, consultez [Comment : Utiliser la classe ChannelFactory](../../../../docs/framework/wcf/feature-details/how-to-use-the-channelfactory.md).
