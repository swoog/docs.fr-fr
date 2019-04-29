---
title: Vue d'ensemble d'un client WCF
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- clients [WCF], architecture
ms.assetid: f60d9bc5-8ade-4471-8ecf-5a07a936c82d
ms.openlocfilehash: 5cb73dfeaac4f1c23724dc71b0f1f5d07fd28b5b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61791233"
---
# <a name="wcf-client-overview"></a>Vue d'ensemble d'un client WCF
Cette section décrit comment les applications clientes, comment configurer, créer et utiliser un client Windows Communication Foundation (WCF) et comment sécuriser les applications clientes.  
  
## <a name="using-wcf-client-objects"></a>Utilisation des objets clients WCF  
 Une application cliente est une application managée qui utilise un client WCF pour communiquer avec une autre application. Pour créer un client application pour un service WCF requiert les étapes suivantes :  
  
1. Obtenez le contrat de service, les informations de liaison et d'adresse pour un point de terminaison de service.  
  
2. Créer un client WCF à l’aide de ces informations.  
  
3. Appelez les opérations.  
  
4. Fermez l’objet de client WCF.  
  
 Les sections suivantes traitent de ces étapes et fournissent de brèves introductions aux problèmes suivants :  
  
- Gestion des erreurs.  
  
- Configuration et sécurisation des clients.  
  
- Création d'objets de rappel pour les services duplex.  
  
- Appels des services de façon asynchrone.  
  
- Appels des services à l'aide de canaux clients.  
  
## <a name="obtain-the-service-contract-bindings-and-addresses"></a>Obtenir le contrat de service, les liaisons et les adresses  
 Dans WCF, les services et les clients modèlent des contrats d’à l’aide des attributs managés, les interfaces et méthodes. Pour se connecter à un service dans une application cliente, vous devez obtenir les informations de type pour le contrat de service. En règle générale, procéder à l’aide de la [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md), qui télécharge les métadonnées à partir du service, le convertit en un fichier de code source managé dans le langage de votre choix et crée un client fichier de configuration d’application que vous pouvez utiliser pour configurer votre objet de client WCF. Par exemple, si vous vous apprêtez à créer un objet de client WCF pour appeler un `MyCalculatorService`, et que vous savez que les métadonnées pour ce service sont publiée à `http://computerName/MyCalculatorService/Service.svc?wsdl`, puis l’exemple de code suivant montre comment utiliser Svcutil.exe pour obtenir un `ClientCode.vb` fichier contient le contrat de service dans le code managé.  
  
```  
svcutil /language:vb /out:ClientCode.vb /config:app.config http://computerName/MyCalculatorService/Service.svc?wsdl  
```  
  
 Vous pouvez compiler ce code de contrat dans l’application cliente ou dans un autre assembly que l’application cliente peut ensuite utiliser pour créer un objet de client WCF. Vous pouvez utiliser le fichier de configuration pour configurer l'objet client pour se connecter correctement au service.  
  
 Pour obtenir un exemple de ce processus, consultez [Comment : Créer un Client](../../../docs/framework/wcf/how-to-create-a-wcf-client.md). Pour plus d’informations sur les contrats, consultez [contrats](../../../docs/framework/wcf/feature-details/contracts.md).  
  
## <a name="create-a-wcf-client-object"></a>Créer un objet client WCF  
 Un client WCF est un objet local qui représente un service WCF dans un formulaire que le client peut utiliser pour communiquer avec le service distant. Types de client WCF implémentent le service cible de contrat, donc lorsque vous créez un et configurez, vous pouvez ensuite utiliser l’objet client directement pour appeler des opérations de service. La durée d’exécution de WCF convertit les appels de méthode en messages, les envoie au service, écoute la réponse et retourne ces valeurs à l’objet de client WCF en tant que valeurs de retour ou `out` ou `ref` paramètres.  
  
 Vous pouvez également utiliser des objets de canal de client WCF pour vous connecter et utiliser les services. Pour plus d’informations, consultez [Architecture du Client WCF](../../../docs/framework/wcf/feature-details/client-architecture.md).  
  
#### <a name="creating-a-new-wcf-object"></a>Création d'un nouvel objet WCF  
 Pour illustrer l'utilisation d'une classe <xref:System.ServiceModel.ClientBase%601>, supposons que le contrat de service simple suivant a été généré depuis une application de service.  
  
> [!NOTE]
>  Si vous utilisez Visual Studio pour créer votre client WCF, les objets sont chargés automatiquement dans l’Explorateur d’objets lorsque vous ajoutez une référence de service à votre projet.  
  
 [!code-csharp[C_GeneratedCodeFiles#12](../../../samples/snippets/csharp/VS_Snippets_CFX/c_generatedcodefiles/cs/proxycode.cs#12)]  
  
 Si vous n’utilisez pas Visual Studio, examinez le code de contrat généré pour rechercher le type qui étend <xref:System.ServiceModel.ClientBase%601> et l’interface de contrat de service `ISampleService`. Dans ce cas, ce type ressemble au code suivant :  
  
 [!code-csharp[C_GeneratedCodeFiles#14](../../../samples/snippets/csharp/VS_Snippets_CFX/c_generatedcodefiles/cs/proxycode.cs#14)]  
  
 Cette classe peut être créée comme un objet local à l'aide de l'un des constructeurs, elle peut être configurée, puis utilisée pour se connecter à un service du type `ISampleService`.  
  
 Il est recommandé que vous créez votre objet de client WCF tout d’abord, puis utilisez et fermez à l’intérieur d’un bloc try/catch unique. Vous ne devez pas utiliser le `using` instruction (`Using` en Visual Basic), car elle peut masquer des exceptions dans certains modes d’échec. Pour plus d’informations, consultez les sections suivantes ainsi que [utilisez fermer et abandon pour libérer les ressources de client WCF](../../../docs/framework/wcf/samples/use-close-abort-release-wcf-client-resources.md).  
  
### <a name="contracts-bindings-and-addresses"></a>Contrats, liaisons et adresses  
 Avant de pouvoir créer un objet de client WCF, vous devez configurer l’objet client. Plus précisément, il doit avoir un service *point de terminaison* à utiliser. Un point de terminaison est la combinaison d’un contrat de service, d’une liaison et d’une adresse. (Pour plus d’informations sur les points de terminaison, consultez [points de terminaison : Adresses, liaisons et contrats](../../../docs/framework/wcf/feature-details/endpoints-addresses-bindings-and-contracts.md).) En règle générale, ces informations se trouvent dans le [ \<point de terminaison >](../../../docs/framework/configure-apps/file-schema/wcf/endpoint-of-client.md) élément dans un fichier de configuration d’application de client, tel que celui de l’outil Svcutil.exe génère et est chargé automatiquement lorsque vous créez votre client objet. Les deux types de client WCF ont également des surcharges qui vous permettent de spécifier par programme ces informations.  
  
 Par exemple, un fichier de configuration généré pour un `ISampleService` utilisé dans les exemples précédents contient les informations suivantes sur le point de terminaison.  
  
 [!code-xml[C_GeneratedCodeFiles#19](../../../samples/snippets/csharp/VS_Snippets_CFX/c_generatedcodefiles/common/client.exe.config#19)]  
  
 Ce fichier de configuration spécifie un point de terminaison cible dans l'élément `<client>`. Pour plus d’informations sur l’utilisation de plusieurs points de terminaison cibles, consultez le <xref:System.ServiceModel.ClientBase%601.%23ctor%2A?displayProperty=nameWithType> ou <xref:System.ServiceModel.ChannelFactory%601.%23ctor%2A?displayProperty=nameWithType> constructeurs.  
  
## <a name="calling-operations"></a>Opérations appelantes  
 Une fois vous avez un objet client créé et configuré, créez un bloc try/catch, appeler des opérations dans la même façon que vous le feriez si l’objet était local et fermer l’objet de client WCF. Lorsque l’application cliente appelle la première opération, WCF s’ouvre automatiquement le canal sous-jacent, et le canal sous-jacent est fermé lorsque l’objet est recyclé. (Vous pouvez également ouvrir et fermer explicitement le canal avant ou après l'appel des autres opérations.)  
  
 Par exemple, si vous avez le contrat de service suivant :  
  
```csharp  
namespace Microsoft.ServiceModel.Samples  
{  
    using System;  
    using System.ServiceModel;  
  
    [ServiceContract(Namespace = "http://Microsoft.ServiceModel.Samples")]  
    public interface ICalculator  
   {  
        [OperationContract]  
        double Add(double n1, double n2);  
        [OperationContract]  
        double Subtract(double n1, double n2);  
        [OperationContract]  
        double Multiply(double n1, double n2);  
        [OperationContract]  
        double Divide(double n1, double n2);  
    }  
}  
```  
  
```vb  
Namespace Microsoft.ServiceModel.Samples  
  
    Imports System  
    Imports System.ServiceModel  
  
    <ServiceContract(Namespace:= _  
    "http://Microsoft.ServiceModel.Samples")> _   
   Public Interface ICalculator  
        <OperationContract> _   
        Function Add(n1 As Double, n2 As Double) As Double  
        <OperationContract> _   
        Function Subtract(n1 As Double, n2 As Double) As Double  
        <OperationContract> _   
        Function Multiply(n1 As Double, n2 As Double) As Double  
        <OperationContract> _   
     Function Divide(n1 As Double, n2 As Double) As Double  
End Interface  
```  
  
 Vous pouvez appeler des opérations en créant un objet de client WCF et appeler ses méthodes, comme l’exemple de code suivant montre. Notez que l’ouverture, l’appel et fermeture de l’objet de client WCF se produit dans un bloc try/catch unique. Pour plus d’informations, consultez [Services d’accès à l’aide d’un Client WCF](../../../docs/framework/wcf/feature-details/accessing-services-using-a-client.md) et [utilisez fermer et abandon pour libérer les ressources de client WCF](../../../docs/framework/wcf/samples/use-close-abort-release-wcf-client-resources.md).  
  
 [!code-csharp[C_GeneratedCodeFiles#20](../../../samples/snippets/csharp/VS_Snippets_CFX/c_generatedcodefiles/cs/proxycode.cs#20)]  
  
## <a name="handling-errors"></a>Gestion des erreurs  
 Des exceptions peuvent se produire dans une application cliente lors de l'ouverture du canal client sous-jacent (en appelant explicitement ou automatiquement une opération), lors de l'utilisation de l'objet client ou de canal pour appeler des opérations, ou lors de la fermeture du canal client sous-jacent. Il est recommandé que les applications gèrent au minimum les exceptions <xref:System.TimeoutException?displayProperty=nameWithType> et <xref:System.ServiceModel.CommunicationException?displayProperty=nameWithType> possibles en plus de tous les objets <xref:System.ServiceModel.FaultException?displayProperty=nameWithType> levés suite aux erreurs SOAP retournées par les opérations. Les erreurs SOAP spécifiées dans le contrat d’opération sont levées aux applications clientes sous la forme d’une <xref:System.ServiceModel.FaultException%601?displayProperty=nameWithType> où le paramètre de type représente le type de détail de l’erreur SOAP. Pour plus d’informations sur la gestion des conditions d’erreur dans une application cliente, consultez [Sending and Receiving Faults](../../../docs/framework/wcf/sending-and-receiving-faults.md). Pour un exemple complet illustrant comment gérer les erreurs dans un client, consultez [attendu des Exceptions](../../../docs/framework/wcf/samples/expected-exceptions.md).  
  
## <a name="configuring-and-securing-clients"></a>Configuration et sécurisation des clients  
 La configuration d'un client démarre par le chargement nécessaire des informations de point de terminaison cibles pour l'objet client ou de canal, généralement depuis un fichier de configuration, même s'il est possible aussi de charger ces informations par programme à l'aide des constructeurs et des propriétés du client. Toutefois, des étapes de configuration supplémentaires sont nécessaires pour activer certain comportement client et pour de nombreux scénarios de sécurité.  
  
 Par exemple, les conditions de sécurité pour les contrats de service sont déclarées dans l’interface de contrat de service, et si Svcutil.exe a créé un fichier de configuration, ce fichier contient généralement une liaison qui peut prendre en charge les spécifications de sécurité du service. Dans certains cas, toutefois, davantage de configuration de sécurité peut être requis, tel que configurer des informations d'identification du client. Pour obtenir des informations complètes sur la configuration de sécurité pour les clients WCF, consultez [sécurisation des Clients](../../../docs/framework/wcf/securing-clients.md).  
  
 De plus, certaines modifications personnalisées peuvent être activées dans des applications clientes, telles que les comportements d'exécution personnalisés. Pour plus d’informations sur la configuration d’un comportement client personnalisé, consultez [configuration des comportements clients](../../../docs/framework/wcf/configuring-client-behaviors.md).  
  
## <a name="creating-callback-objects-for-duplex-services"></a>Création d'objets de rappel pour les services duplex  
 Les services duplex spécifient un contrat de rappel que l'application cliente doit implémenter afin de fournir un objet de rappel pour le service à appeler selon les spécifications du contrat. Bien que les objets de rappel ne soient pas des services complets (par exemple, vous ne pouvez pas initialiser de canal avec un objet de rappel), pour les besoins de l'implémentation et de la configuration ils peuvent être considérés comme un type de service.  
  
 Les clients de services duplex doivent :  
  
- Implémenter une classe de contrat de rappel.  
  
- Créer une instance de la classe de mise en œuvre de contrat de rappel et l’utiliser pour créer le <xref:System.ServiceModel.InstanceContext?displayProperty=nameWithType> objet que vous passez au constructeur client WCF.  
  
- Appeler des opérations et traiter des rappels d'opération.  
  
 Duplex WCF client objets fonction comme leurs équivalents non-duplex, sauf qu’elles exposent les fonctionnalités nécessaires pour prendre en charge les rappels, y compris la configuration du service de rappel.  
  
 Par exemple, vous pouvez contrôler différents aspects de comportement à l'exécution de l'objet de rappel en utilisant des propriétés de l'attribut <xref:System.ServiceModel.CallbackBehaviorAttribute?displayProperty=nameWithType> sur la classe de rappel. Un autre exemple est l'utilisation de la classe <xref:System.ServiceModel.Description.CallbackDebugBehavior?displayProperty=nameWithType> pour permettre le retour d'informations sur les exceptions aux services qui appellent l'objet de rappel. Pour plus d’informations, consultez [Services Duplex](../../../docs/framework/wcf/feature-details/duplex-services.md). Pour obtenir un exemple complet, consultez [Duplex](../../../docs/framework/wcf/samples/duplex.md).  
  
 Sur les ordinateurs Windows XP qui exécutent les services IIS (Internet Information Services) 5.1, les clients duplex doivent spécifier une adresse de base cliente à l'aide de la classe <xref:System.ServiceModel.WSDualHttpBinding?displayProperty=nameWithType> ou une exception est levée. L'exemple de code suivant montre comment procéder.  
  
 [!code-csharp[S_DualHttp#8](../../../samples/snippets/csharp/VS_Snippets_CFX/s_dualhttp/cs/program.cs#8)]
 [!code-vb[S_DualHttp#8](../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_dualhttp/vb/module1.vb#8)]  
  
 Le code suivant montre comment effectuer cette opération dans un fichier de configuration  
  
 [!code-csharp[S_DualHttp#134](../../../samples/snippets/csharp/VS_Snippets_CFX/s_dualhttp/cs/program.cs#134)]  
  
## <a name="calling-services-asynchronously"></a>Appels des services de façon asynchrone.  
 Le mode d'appel des opérations dépend entièrement du développeur du client. En effet, les messages qui composent une opération peuvent être mappés aux méthodes synchrones ou asynchrones lorsqu’ils sont exprimés dans le code managé. Par conséquent, si vous souhaitez générer un client qui appelle des opérations de façon asynchrone, vous pouvez utiliser Svcutil.exe pour générer le code client asynchrone à l'aide de l'option `/async`. Pour plus d'informations, voir [Procédure : Appeler des opérations de Service de façon asynchrone](../../../docs/framework/wcf/feature-details/how-to-call-wcf-service-operations-asynchronously.md).  
  
## <a name="calling-services-using-wcf-client-channels"></a>Appels des services à l'aide des canaux clients WCF  
 Étendent des types de client WCF <xref:System.ServiceModel.ClientBase%601>, elle-même dérivée de <xref:System.ServiceModel.IClientChannel?displayProperty=nameWithType> interface à exposer le système de canal sous-jacent. Vous pouvez appeler des services à l'aide du contrat de service cible avec la classe <xref:System.ServiceModel.ChannelFactory%601?displayProperty=nameWithType>. Pour plus d’informations, consultez [Architecture du Client WCF](../../../docs/framework/wcf/feature-details/client-architecture.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.ClientBase%601?displayProperty=nameWithType>
- <xref:System.ServiceModel.ChannelFactory%601?displayProperty=nameWithType>
