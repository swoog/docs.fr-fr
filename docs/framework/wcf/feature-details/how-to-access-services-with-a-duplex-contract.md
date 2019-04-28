---
title: 'Procédure : Access services avec un contrat duplex'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- duplex contracts [WCF]
ms.assetid: 746a9d64-f21c-426c-b85d-972e916ec6c5
ms.openlocfilehash: 366fd9d6aa220bcbec1ee8fb2a04d1b84755800a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61855138"
---
# <a name="how-to-access-services-with-a-duplex-contract"></a>Procédure : Access services avec un contrat duplex

L’une des fonctionnalités de Windows Communication Foundation (WCF) sont la possibilité de créer un service qui utilise un modèle de messagerie duplex. Ce modèle permet à un service de communiquer avec un client via un rappel. Cette rubrique montre comment créer un client WCF dans une classe de client qui implémente l’interface de rappel.

Une liaison double expose l'adresse IP du client au service. Ce client doit utiliser un mode de sécurité afin de garantir sa connexion à un service fiable.

Pour obtenir un didacticiel sur la création d’un service WCF de base et un client, consultez [Getting Started Tutorial](../../../../docs/framework/wcf/getting-started-tutorial.md).

## <a name="to-access-a-duplex-service"></a>Pour accéder à un service duplex

1. Créez un service qui contient deux interfaces. La première interface est pour le service, la deuxième est pour le rappel. Pour plus d’informations sur la création d’un service duplex, consultez [Comment : Créer un contrat Duplex](../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md).

2. Exécutez le service.

3. Utilisez le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour générer des contrats (interfaces) pour le client. Pour savoir comment procéder, consultez [Comment : Créer un Client](../../../../docs/framework/wcf/how-to-create-a-wcf-client.md).

4. Implémentez l'interface de rappel dans la classe client, comme illustré dans l'exemple suivant.

    ```csharp
    public class CallbackHandler : ICalculatorDuplexCallback
    {
        public void Result(double result)
        {
            Console.WriteLine("Result ({0})", result);
        }
        public void Equation(string equation)
        {
            Console.WriteLine("Equation({0})", equation);
        }
    }
    ```

    ```vb
    Public Class CallbackHandler
    Implements ICalculatorDuplexCallback
       Public Sub Result (ByVal result As Double)
          Console.WriteLine("Result ({0})", result)
       End Sub
        Public Sub Equation(ByVal equation As String)
            Console.WriteLine("Equation({0})", equation)
        End Sub
    End Class
    ```

5. Créez une instance de la classe <xref:System.ServiceModel.InstanceContext>. Le constructeur a besoin d'une instance de la classe client.

    ```csharp
    InstanceContext site = new InstanceContext(new CallbackHandler());
    ```

    ```vb
    Dim site As InstanceContext = New InstanceContext(new CallbackHandler())
    ```

6. Créez une instance du client WCF à l’aide du constructeur qui nécessite un <xref:System.ServiceModel.InstanceContext> objet. Le second paramètre du constructeur correspond au nom du point de terminaison trouvé dans le fichier de configuration.

    ```csharp
    CalculatorDuplexClient wcfClient = new CalculatorDuplexClient(site, "default");
    ```

    ```vb
    Dim wcfClient As New CalculatorDuplexClient(site, "default")
    ```

7. Appelez les méthodes du client WCF en fonction des besoins.

## <a name="example"></a>Exemple

L'exemple de code suivant illustre comment créer une classe client qui accède à un contrat duplex.

[!code-csharp[S_DuplexClients#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_duplexclients/cs/client.cs#1)]
[!code-vb[S_DuplexClients#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_duplexclients/vb/client.vb#1)]

## <a name="see-also"></a>Voir aussi

- [Didacticiel Bien démarrer](../../../../docs/framework/wcf/getting-started-tutorial.md)
- [Guide pratique pour Créer un contrat Duplex](../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md)
- [Outil ServiceModel Metadata Utility (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [Guide pratique pour Créer un Client](../../../../docs/framework/wcf/how-to-create-a-wcf-client.md)
- [Guide pratique pour Utiliser la classe ChannelFactory](../../../../docs/framework/wcf/feature-details/how-to-use-the-channelfactory.md)
