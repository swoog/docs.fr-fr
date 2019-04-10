---
title: 'Procédure : activer le streaming'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 6ca2cf4b-c7a1-49d8-a79b-843a90556ba4
ms.openlocfilehash: 5bc4bce984c4159949f840f395005ec9fe746e85
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59227312"
---
# <a name="how-to-enable-streaming"></a>Procédure : activer le streaming
Windows Communication Foundation (WCF) peut envoyer des messages à l’aide de transferts mis en mémoire tampon ou transmis en continu. En mode de transfert par mise en mémoire tampon, un message doit être complètement remis avant qu'un récepteur puisse le lire. En mode de transfert par diffusion en continu, le récepteur peut commencer à traiter le message avant qu'il ne soit complètement remis. Le mode de diffusion en continu est utile lorsque les informations passées sont volumineuses et peuvent être traitées en série. Le mode de diffusion en continu est également utile lorsque le message est trop volumineux pour être mis entièrement en mémoire tampon.  
  
 Pour activer la diffusion en continu, définissez le `OperationContract` convenablement et activez la diffusion en continu au niveau du transport.  
  
### <a name="to-stream-data"></a>Pour transmettre des données en continu  
  
1.  Pour transmettre des données en continu le `OperationContract` du service doit satisfaire deux spécifications :  
  
    1.  Le paramètre qui gère les données diffusées en continu doit être le seul paramètre dans la méthode. Par exemple, si le message d'entrée est celui à diffuser en continu, l'opération ne doit avoir qu'un seul paramètre d'entrée. De la même façon, si le message de sortie doit être diffusé en continu, l'opération ne doit avoir qu'un seul paramètre de sortie ou qu'une seule valeur de retour.  
  
    2.  Au moins l'un des types de paramètre et de valeur de retour doit être <xref:System.IO.Stream>, <xref:System.ServiceModel.Channels.Message>ou <xref:System.Xml.Serialization.IXmlSerializable>.  
  
     Ce qui suit est un exemple de contrat de diffusion des données en continu.  
  
     [!code-csharp[c_HowTo_EnableStreaming#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_enablestreaming/cs/service.cs#1)]
     [!code-vb[c_HowTo_EnableStreaming#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_enablestreaming/vb/service.vb#1)]  
  
     L'opération `GetStream` reçoit des données d'entrée mises en mémoire tampon sous la forme d'une chaîne (`string`) mise en mémoire tampon et retourne `Stream`, soit des données diffusées en continu. Inversement, `UploadStream` utilise `Stream` (transmis en continu) et retourne `bool` (mis en mémoire tampon). `EchoStream` accepte et retourne `Stream` et est un exemple d’une opération dont l’entrée et les messages de sortie sont transmis en continu. Enfin, `GetReversedStream` ne prend pas d'entrée et retourne `Stream` (diffusion en continu).  
  
2.  La diffusion en continu doit être activée sur la liaison. Affectez à une propriété `TransferMode` l'une des valeurs suivantes :  
  
    1.  `Buffered`,  
  
    2.  `Streamed`, ce qui permet la communication de diffusion en continu dans les deux sens.  
  
    3.  `StreamedRequest`, ce qui permet la diffusion en continu de la demande uniquement.  
  
    4.  `StreamedResponse`, ce qui permet la diffusion en continu de la réponse uniquement.  
  
     La `BasicHttpBinding` expose la propriété `TransferMode` sur la liaison, tout comme `NetTcpBinding` et `NetNamedPipeBinding`. La propriété `TransferMode` peut également être définie sur l’élément de liaison de transport et utilisée dans une liaison personnalisée.  
  
     Les exemples suivants indiquent comment définir le `TransferMode` par code et en modifiant le fichier de configuration. Les exemples attribuent également à la propriété `maxReceivedMessageSize` la valeur 64 Mo, qui limite la taille maximale autorisée des messages en réception. La valeur par défaut de `maxReceivedMessageSize` est 64 Ko, ce qui est habituellement trop bas pour les scénarios de diffusion en continu. Définissez ce paramètre de quota correctement selon la taille maximale des messages que votre application est susceptible de recevoir. Notez également que la `maxBufferSize` contrôle la taille maximale mise en mémoire tampon ; il convient de définir convenablement cette valeur.  
  
    1.  L’extrait de code de configuration suivant tiré de l’exemple présente l’affectation du mode de diffusion en continu à la propriété `TransferMode` sur la `basicHttpBinding` et sur une liaison HTTP personnalisée.  
  
         [!code-xml[c_HowTo_EnableStreaming#103](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_enablestreaming/common/app.config#103)]   
  
    2.  L'extrait de code suivant affiche l'affectation à la propriété `TransferMode` la diffusion en continu sur la `basicHttpBinding` et sur une liaison HTTP personnalisée.  
  
         [!code-csharp[c_HowTo_EnableStreaming_code#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_enablestreaming_code/cs/c_howto_enablestreaming_code.cs#2)]
         [!code-vb[c_HowTo_EnableStreaming_code#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_enablestreaming_code/vb/c_howto_enablestreaming_code.vb#2)]  
  
    3.  L’extrait de code suivant affiche l’affectation à la propriété `TransferMode` de la diffusion en continu une liaison TCP personnalisée.  
  
         [!code-csharp[c_HowTo_EnableStreaming_code#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_enablestreaming_code/cs/c_howto_enablestreaming_code.cs#3)]
         [!code-vb[c_HowTo_EnableStreaming_code#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_enablestreaming_code/vb/c_howto_enablestreaming_code.vb#3)]  
  
3.  Les opérations `GetStream`, `UploadStream` et `EchoStream` concernent toutes l'envoi de données directement à partir d'un fichier ou l'enregistrement des données reçues directement dans un fichier. Le code suivant concerne `GetStream`.  
  
     [!code-csharp[c_HowTo_EnableStreaming#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_enablestreaming/cs/service.cs#4)]
     [!code-vb[c_HowTo_EnableStreaming#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_enablestreaming/vb/service.vb#4)]  
  
### <a name="writing-a-custom-stream"></a>Écriture d'un flux personnalisé  
  
1.  Pour effectuer un traitement spécial sur chaque bloc d'un flux alors qu'il est envoyé ou reçu, dérivez une classe de flux personnalisé de <xref:System.IO.Stream>. Pour donner un exemple d'un flux personnalisé, le code suivant contient une méthode `GetReversedStream` et une classe `ReverseStream`-.  
  
     `GetReversedStream` Crée et retourne une nouvelle instance de `ReverseStream`. Le traitement réel se produit lorsque le système lit l'objet `ReverseStream`. La méthode `ReverseStream.Read` lit un bloc d'octets du fichier sous-jacent, les inverse, puis retourne les octets inversés. Cette méthode n'inverse pas l'ensemble du contenu du fichier, mais uniquement un bloc d'octets à la fois. Cet exemple montre comment vous pouvez traiter un flux pendant que le contenu est lu ou écrit à partir du flux.  
  
     [!code-csharp[c_HowTo_EnableStreaming#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_enablestreaming/cs/service.cs#2)]
     [!code-vb[c_HowTo_EnableStreaming#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_enablestreaming/vb/service.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- [Données volumineuses et diffusion en continu](../../../../docs/framework/wcf/feature-details/large-data-and-streaming.md)
- [Stream](../../../../docs/framework/wcf/samples/stream.md)
