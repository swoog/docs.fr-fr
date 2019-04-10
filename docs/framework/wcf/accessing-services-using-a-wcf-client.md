---
title: Accès aux services à l'aide d'un client WCF
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- clients [WCF], consuming services
ms.assetid: d780af9f-73c5-42db-9e52-077a5e4de7fe
ms.openlocfilehash: 6bf683cdd0a03a5d1dbc452c28e7b33911464f09
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59297250"
---
# <a name="accessing-services-using-a-wcf-client"></a>Accès aux services à l'aide d'un client WCF

Une fois que vous créez un service, l’étape suivante consiste à créer un proxy de client WCF. Une application cliente utilise le proxy client WCF pour communiquer avec le service. Les applications clientes généralement importer des métadonnées d’un service pour générer le code de client WCF peut être utilisé pour appeler le service.

 Les étapes de base pour la création d’un client WCF sont les suivantes :

1. Compiler le code de service.

2. Générer le proxy client WCF.

3. Instanciez le proxy client WCF.

Le proxy client WCF peut être généré manuellement à l’aide du Service Model Metadata Utility Tool (SvcUtil.exe) pour plus d’informations, consultez [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md). Le proxy client WCF peut également être généré dans Visual Studio à l’aide de la **ajouter une référence de Service** fonctionnalité. Pour générer le proxy client WCF à l'aide de l'une de ces méthodes, le service doit s'exécuter. Si le service est auto-hébergé, vous devez exécuter l'hôte. Si le service est hébergé dans IIS/WAS, aucune action n'est nécessaire.

## <a name="servicemodel-metadata-utility-tool"></a>Outil Service Model Metadata Tool
 Le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) est un outil de ligne de commande pour générer du code à partir des métadonnées. Voici un exemple d'utilisation d'une commande Svcutil.exe de base.

```
Svcutil.exe <service's Metadata Exchange (MEX) address or HTTP GET address>
```

 Vous pouvez également utiliser Svcutil.exe avec des fichiers WSDL (Web Services Description Language) et XSD (XML Schema Definition) sur le système de fichiers.

```
Svcutil.exe <list of WSDL and XSD files on file system>
```

 Le résultat est un fichier de code qui contient le code du client WCF que l’application cliente peut utiliser pour appeler le service.

 L'outil permet également de générer des fichiers de configuration.

```
Svcutil.exe <file1 [,file2]>
```

 Si un seul nom de fichier est fourni, il s'agit du nom du fichier de sortie. Si deux noms de fichiers sont fournis, le premier est un fichier de configuration d’entrée dont le contenu est fusionné avec la configuration générée et écrit dans le deuxième fichier. Pour plus d’informations sur la configuration, consultez [configuration des liaisons pour les Services](../../../docs/framework/wcf/configuring-bindings-for-wcf-services.md).

> [!IMPORTANT]
> Demandes de métadonnées non sécurisées représentent certains risques dans la même manière que toute demande réseau non sécurisé : Si vous n’êtes pas certain que le point de terminaison avec laquelle vous communiquez est qui elle prétend, les informations que vous récupérez peut-être les métadonnées à partir d’un service malveillant.

## <a name="add-service-reference-in-visual-studio"></a>Ajouter une référence de service dans Visual Studio

 Avec le service est exécuté, le bouton droit sur le projet qui contiendra le proxy client WCF, puis sélectionnez **ajouter** > **une référence de Service**. Dans le **boîte de dialogue référence de Service ajouter**, tapez l’URL pour le service que vous souhaitez appeler et cliquez sur le **accédez** bouton. La boîte de dialogue affiche une liste de services disponibles à l'adresse que vous spécifiez. Double-cliquez sur le service pour afficher les contrats et les opérations disponibles, spécifiez un espace de noms pour le code généré, puis cliquez sur le **OK** bouton.

## <a name="example"></a>Exemple
 L'exemple de code suivant montre un contrat de service créé pour un service.

```csharp
// Define a service contract.
[ServiceContract(Namespace="http://Microsoft.ServiceModel.Samples")]
public interface ICalculator
{
    [OperationContract]
    double Add(double n1, double n2);
    // Other methods are not shown here.
}
```

```vb
' Define a service contract.
<ServiceContract(Namespace:="http://Microsoft.ServiceModel.Samples")> _
Public Interface ICalculator
    <OperationContract()>  _
    Function Add(ByVal n1 As Double, ByVal n2 As Double) As Double
    ' Other methods are not shown here.
End Interface
```

 L’outil Metadata de ServiceModel tool et **ajouter une référence de Service** dans Visual Studio génère la classe de client WCF suivante. La classe hérite de la classe générique <xref:System.ServiceModel.ClientBase%601> et implémente l'interface `ICalculator`. L'outil génère également l'interface `ICalculator` (qui n'est pas présentée ici).

```csharp
public partial class CalculatorClient : System.ServiceModel.ClientBase<ICalculator>, ICalculator
{
    public CalculatorClient()
    {}

    public CalculatorClient(string endpointConfigurationName) :
            base(endpointConfigurationName)
    {}

    public CalculatorClient(string endpointConfigurationName, string remoteAddress) :
            base(endpointConfigurationName, remoteAddress)
    {}

    public CalculatorClient(string endpointConfigurationName,
        System.ServiceModel.EndpointAddress remoteAddress) :
            base(endpointConfigurationName, remoteAddress)
    {}

    public CalculatorClient(System.ServiceModel.Channels.Binding binding,
        System.ServiceModel.EndpointAddress remoteAddress) :
            base(binding, remoteAddress)
    {}

    public double Add(double n1, double n2)
    {
        return base.Channel.Add(n1, n2);
    }
}
```

```vb
Partial Public Class CalculatorClient
    Inherits System.ServiceModel.ClientBase(Of ICalculator)
    Implements ICalculator

    Public Sub New()
        MyBase.New
    End Sub

    Public Sub New(ByVal endpointConfigurationName As String)
        MyBase.New(endpointConfigurationName)
    End Sub

    Public Sub New(ByVal endpointConfigurationName As String, ByVal remoteAddress As String)
        MyBase.New(endpointConfigurationName, remoteAddress)
    End Sub

    Public Sub New(ByVal endpointConfigurationName As String,
        ByVal remoteAddress As System.ServiceModel.EndpointAddress)
        MyBase.New(endpointConfigurationName, remoteAddress)
    End Sub

    Public Sub New(ByVal binding As System.ServiceModel.Channels.Binding,
        ByVal remoteAddress As System.ServiceModel.EndpointAddress)
        MyBase.New(binding, remoteAddress)
    End Sub

    Public Function Add(ByVal n1 As Double, ByVal n2 As Double) As Double
        Implements ICalculator.Add
        Return MyBase.Channel.Add(n1, n2)
    End Function
End Class
```

## <a name="using-the-wcf-client"></a>Utilisation du client WCF
 Pour utiliser le client WCF, créez une instance du client WCF, puis appelez ses méthodes, comme indiqué dans le code suivant.

```csharp
// Create a client object with the given client endpoint configuration.
CalculatorClient calcClient = new CalculatorClient("CalculatorEndpoint"));
// Call the Add service operation.
double value1 = 100.00D;
double value2 = 15.99D;
double result = calcClient.Add(value1, value2);
Console.WriteLine("Add({0},{1}) = {2}", value1, value2, result);
```

```vb
' Create a client object with the given client endpoint configuration.
Dim calcClient As CalculatorClient = _
New CalculatorClient("CalculatorEndpoint")

' Call the Add service operation.
Dim value1 As Double = 100.00D
Dim value2 As Double = 15.99D
Dim result As Double = calcClient.Add(value1, value2)
Console.WriteLine("Add({0},{1}) = {2}", value1, value2, result)
```

## <a name="debugging-exceptions-thrown-by-a-client"></a>Débogage d'exceptions levées par un Client

Nombre d’exceptions levée par un client WCF est dues à une exception sur le service. En voici quelques exemples :

-   <xref:System.Net.Sockets.SocketException>: Une connexion existante a dû être fermée par l’hôte distant.

-   <xref:System.ServiceModel.CommunicationException>: La connexion sous-jacente a été fermée de manière inattendue.

-   <xref:System.ServiceModel.CommunicationObjectAbortedException>: La connexion de socket a été abandonnée. Cela peut être dû à une erreur lors du traitement de votre message, l'expiration du délai de réception par l'hôte distant ou un problème de ressource sur le réseau sous-jacent.

Lorsque ces types d'exceptions se produisent, le meilleur moyen de les résoudre consiste à activer le suivi du côté service et de déterminer l'exception qui s'y est produite. Pour plus d’informations sur le suivi, consultez [suivi](../../../docs/framework/wcf/diagnostics/tracing/index.md) et [à l’aide de suivi pour résoudre les problèmes de votre Application](../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md).

## <a name="see-also"></a>Voir aussi

- [Procédure : Créer un client](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)
- [Procédure : accéder aux services avec un contrat duplex](../../../docs/framework/wcf/feature-details/how-to-access-services-with-a-duplex-contract.md)
- [Procédure : appeler des opérations de service de façon asynchrone](../../../docs/framework/wcf/feature-details/how-to-call-wcf-service-operations-asynchronously.md)
- [Procédure : accéder aux services avec des contrats demande-réponse unidirectionnels](../../../docs/framework/wcf/feature-details/how-to-access-wcf-services-with-one-way-and-request-reply-contracts.md)
- [Procédure : accéder à un service WSE 3.0](../../../docs/framework/wcf/feature-details/how-to-access-a-wse-3-0-service-with-a-wcf-client.md)
- [Fonctionnement du code client généré](../../../docs/framework/wcf/feature-details/understanding-generated-client-code.md)
- [Procédure : améliorer le délai de démarrage des applications clientes WCF à l’aide de XmlSerializer](../../../docs/framework/wcf/feature-details/startup-time-of-wcf-client-applications-using-the-xmlserializer.md)
- [Spécification du comportement du client au moment de l'exécution](../../../docs/framework/wcf/specifying-client-run-time-behavior.md)
- [Configuration des comportements clients](../../../docs/framework/wcf/configuring-client-behaviors.md)
