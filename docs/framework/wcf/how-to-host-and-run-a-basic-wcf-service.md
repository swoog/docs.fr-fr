---
title: 'Comment : héberger et exécuter un service Windows Communication Foundation de base'
ms.date: 09/14/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF services [WCF]
- WCF services [WCF], running
ms.assetid: 31774d36-923b-4e2d-812e-aa190127266f
ms.openlocfilehash: b79c3246b7c12a3a99a5c68586387fc30573dcb6
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46562292"
---
# <a name="how-to-host-and-run-a-basic-windows-communication-foundation-service"></a>Comment : héberger et exécuter un service Windows Communication Foundation de base

Il s’agit de la troisième des six tâches nécessaires pour créer une application WCF (Windows Communication Foundation). Pour une vue d’ensemble des six tâches, consultez la rubrique [Tutoriel Bien démarrer](../../../docs/framework/wcf/getting-started-tutorial.md).

Cette rubrique explique comment héberger un service WCF (Windows Communication Foundation) dans une application console. Cette procédure se compose des étapes suivantes :

- Créez un projet d'application console pour héberger le service.

- Créer un hôte de service pour le service.

- Activer l'échange de métadonnées.

- Ouvrir l'hôte de service.

La liste complète du code écrit dans cette tâche est fournie dans l’exemple qui suit la procédure.

## <a name="create-a-new-console-application-to-host-the-service"></a>Créer une nouvelle application de console pour héberger le service

1. Créer un nouveau projet d’Application de Console dans Visual Studio en effectuant un clic droit sur la solution de mise en route et en sélectionnant **ajouter** > **nouveau projet**. Dans le **ajouter un nouveau projet** boîte de dialogue, sur le côté gauche, sélectionnez le **Windows Desktop** catégorie sous **Visual C#** ou **Visual Basic**. Sélectionnez le **application Console (.NET Framework)** modèle, puis nommez le projet **GettingStartedHost**.

2. Ajoutez une référence au projet GettingStartedLib dans le projet GettingStartedHost. Avec le bouton droit sur le **références** dossier sous le projet GettingStartedHost dans **l’Explorateur de solutions**, puis sélectionnez **ajouter une référence**. Dans le **ajouter une référence** boîte de dialogue, sélectionnez **Solution** sur le côté gauche de la boîte de dialogue, sélectionnez GettingStartedLib dans la section centrale de la boîte de dialogue, puis choisissez **ajouter**. Cela rend les types définis dans GettingStartedLib disponibles au projet GettingStartedHost.

3. Ajoutez une référence à System.ServiceModel dans le projet GettingStartedHost. Avec le bouton droit le **références** dossier sous le projet GettingStartedHost dans **l’Explorateur de solutions** et sélectionnez **ajouter une référence**. Dans le **ajouter une référence** boîte de dialogue, sélectionnez **Framework** sur le côté gauche de la boîte de dialogue **assemblys**. Recherchez et sélectionnez **System.ServiceModel**, puis choisissez **OK**. Enregistrez la solution en sélectionnant **fichier** > **Enregistrer tout**.

## <a name="host-the-service"></a>Héberger le service

Ouvrez le fichier Program.cs ou Module.vb et entrez le code suivant :

```csharp
using System;
using System.ServiceModel;
using System.ServiceModel.Description;
using GettingStartedLib;

namespace GettingStartedHost
{
    class Program
    {
        static void Main(string[] args)
        {
            // Step 1 Create a URI to serve as the base address.
            Uri baseAddress = new Uri("http://localhost:8000/GettingStarted/");

            // Step 2 Create a ServiceHost instance
            ServiceHost selfHost = new ServiceHost(typeof(CalculatorService), baseAddress);

            try
            {
                // Step 3 Add a service endpoint.
                selfHost.AddServiceEndpoint(typeof(ICalculator), new WSHttpBinding(), "CalculatorService");

                // Step 4 Enable metadata exchange.
                ServiceMetadataBehavior smb = new ServiceMetadataBehavior();
                smb.HttpGetEnabled = true;
                selfHost.Description.Behaviors.Add(smb);

                // Step 5 Start the service.
                selfHost.Open();
                Console.WriteLine("The service is ready.");
                Console.WriteLine("Press <ENTER> to terminate service.");
                Console.WriteLine();
                Console.ReadLine();

                // Close the ServiceHostBase to shutdown the service.
                selfHost.Close();
            }
            catch (CommunicationException ce)
            {
                Console.WriteLine("An exception occurred: {0}", ce.Message);
                selfHost.Abort();
            }
        }
    }
}
```

```vb
Imports System.ServiceModel
Imports System.ServiceModel.Description
Imports GettingStartedLibVB.GettingStartedLib

Module Service

    Class Program
        Shared Sub Main()
            ' Step 1 Create a URI to serve as the base address
            Dim baseAddress As New Uri("http://localhost:8000/ServiceModelSamples/Service")

            ' Step 2 Create a ServiceHost instance
            Dim selfHost As New ServiceHost(GetType(CalculatorService), baseAddress)
           Try

                ' Step 3 Add a service endpoint
                ' Add a service endpoint
                selfHost.AddServiceEndpoint( _
                    GetType(ICalculator), _
                    New WSHttpBinding(), _
                    "CalculatorService")

                ' Step 4 Enable metadata exchange.
                Dim smb As New ServiceMetadataBehavior()
                smb.HttpGetEnabled = True
                selfHost.Description.Behaviors.Add(smb)

                ' Step 5 Start the service
                selfHost.Open()
                Console.WriteLine("The service is ready.")
                Console.WriteLine("Press <ENTER> to terminate service.")
                Console.WriteLine()
                Console.ReadLine()

                ' Close the ServiceHostBase to shutdown the service.
                selfHost.Close()
            Catch ce As CommunicationException
                Console.WriteLine("An exception occurred: {0}", ce.Message)
                selfHost.Abort()
            End Try
        End Sub
    End Class

End Module
```

**Étape 1** -crée une instance de la classe Uri pour contenir l’adresse de base du service. Les services sont identifiés par une URL, qui contient une adresse de base et un URI facultatif. L’adresse de base est mise en forme comme suit : [transport]://[nom de machine ou domaine][:n° de port facultatif]/[segment d’URI facultatif]L’adresse de base du service de calculatrice utilise le transport HTTP, localhost, le port 8000 et le segment d’URI « GettingStarted »

**Étape 2** – crée une instance de la <xref:System.ServiceModel.ServiceHost> classe pour héberger le service. Le constructeur prend deux paramètres, le type de la classe qui implémente le contrat de service et l'adresse de base du service.

**Étape 3** – crée un <xref:System.ServiceModel.Description.ServiceEndpoint> instance. Un point de terminaison de service est composé d’une adresse, d’une liaison et d’un contrat de service. Le constructeur <xref:System.ServiceModel.Description.ServiceEndpoint> prend donc le type d'interface de contrat de service, une liaison et une adresse. Le contrat de service est `ICalculator`, que vous définissez et implémentez dans le type de service. La liaison utilisée dans cet exemple est <xref:System.ServiceModel.WSHttpBinding>, qui est une liaison intégrée utilisée pour se connecter aux points de terminaison qui sont conformes aux spécifications WS-*. Pour plus d’informations sur les liaisons WCF, consultez [Vue d’ensemble des liaisons WCF](../../../docs/framework/wcf/bindings-overview.md). L'adresse est ajoutée à l'adresse de base pour identifier le point de terminaison. L’adresse spécifiée dans ce code est « CalculatorService », par conséquent, l’adresse complète du point de terminaison est `"http://localhost:8000/GettingStarted/CalculatorService"`.

    > [!IMPORTANT]
    > Adding a service endpoint is optional when using .NET Framework 4 or later. In these versions, if no endpoints are added in code or configuration, WCF adds one default endpoint for each combination of base address and contract implemented by the service. For more information about default endpoints see [Specifying an Endpoint Address](../../../docs/framework/wcf/specifying-an-endpoint-address.md). For more information about default endpoints, bindings, and behaviors, see [Simplified Configuration](../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).

**Étape 4** – activer l’échange de métadonnées. Les clients utilisent l'échange de métadonnées pour générer des proxys qui seront utilisés pour appeler les opérations de service. Pour permettre l’échange de métadonnées, créez une instance de <xref:System.ServiceModel.Description.ServiceMetadataBehavior>, affectez à sa propriété <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> la valeur `true`, puis ajoutez le comportement à la collection <!--zz <xref:System.ServiceModel.ServiceHost.Behaviors%2A>  -->`System.ServiceModel.ServiceHost.Behaviors%2A` de l’instance <xref:System.ServiceModel.ServiceHost>.

**Étape 5** – permet d’ouvrir le <xref:System.ServiceModel.ServiceHost> pour écouter les messages entrants. Notez que le code attend que l'utilisateur appuie sur Entrée. Si vous n'effectuez pas cette opération, l'application se ferme immédiatement et le service s'arrête. Notez également le bloc try/catch utilisé. Une fois que <xref:System.ServiceModel.ServiceHost> a été instancié, le reste du code est placé dans un bloc try/catch. Pour plus d’informations sur l’interception en toute sécurité des exceptions levées par <xref:System.ServiceModel.ServiceHost>, consultez la section [Éviter les problèmes avec l’instruction Using](../../../docs/framework/wcf/samples/avoiding-problems-with-the-using-statement.md)

> [!IMPORTANT]
> Modifiez le fichier App.config dans GettingStartedLib afin de refléter les modifications apportées dans le code :
> 1. Modifiez la ligne 14 pour `<service name="GettingStartedLib.CalculatorService">`
> 2. Modifiez la ligne 17 en `<add baseAddress = "http://localhost:8000/GettingStarted/CalculatorService" />`
> 3. Remplacez la ligne 22 à `<endpoint address="" binding="wsHttpBinding" contract="GettingStartedLib.ICalculator">`

## <a name="verify-the-service-is-working"></a>Vérifiez que le service fonctionne

1. Exécutez la console GettingStartedHost application à partir de Visual Studio.

   Le service doit être exécuté avec des privilèges d’administrateur. Étant donné que Visual Studio a été ouverte avec des privilèges d’administrateur, GettingStartedHost est également exécuté avec des privilèges d’administrateur. Vous pouvez également ouvrir une invite de commandes en utilisant **exécuter en tant qu’administrateur** et exécutez service.exe qu’il contient.

2. Ouvrez un navigateur web et accédez à la page du service debug à `http://localhost:8000/GettingStarted/CalculatorService`.

## <a name="example"></a>Exemple

L'exemple suivant inclut le contrat de service et l'implémentation d'étapes précédentes dans le didacticiel et héberge le service dans une application console.

Pour compiler avec un compilateur de ligne de commande, compilez IService1.cs et Service1.cs dans une bibliothèque de classes qui fait référence à `System.ServiceModel.dll`. Compilez le fichier Program.cs comme une application console.

```csharp
using System;
using System.ServiceModel;

namespace GettingStartedLib
{
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

```csharp
using System;
using System.ServiceModel;

namespace GettingStartedLib
{
    public class CalculatorService : ICalculator
    {
        public double Add(double n1, double n2)
        {
            double result = n1 + n2;
            Console.WriteLine("Received Add({0},{1})", n1, n2);
            // Code added to write output to the console window.
            Console.WriteLine("Return: {0}", result);
            return result;
        }

        public double Subtract(double n1, double n2)
        {
            double result = n1 - n2;
            Console.WriteLine("Received Subtract({0},{1})", n1, n2);
            Console.WriteLine("Return: {0}", result);
            return result;
        }

        public double Multiply(double n1, double n2)
        {
            double result = n1 * n2;
            Console.WriteLine("Received Multiply({0},{1})", n1, n2);
            Console.WriteLine("Return: {0}", result);
            return result;
        }

        public double Divide(double n1, double n2)
        {
            double result = n1 / n2;
            Console.WriteLine("Received Divide({0},{1})", n1, n2);
            Console.WriteLine("Return: {0}", result);
            return result;
        }
    }
}
```

```csharp
using System;
using System.ServiceModel;
using System.ServiceModel.Description;
using GettingStartedLib;

namespace GettingStartedHost
{
    class Program
    {
        static void Main(string[] args)
        {
            // Step 1 of the address configuration procedure: Create a URI to serve as the base address.
            Uri baseAddress = new Uri("http://localhost:8000/ServiceModelSamples/Service");

            // Step 2 of the hosting procedure: Create ServiceHost
            ServiceHost selfHost = new ServiceHost(typeof(CalculatorService), baseAddress);

            try
            {
                // Step 3 of the hosting procedure: Add a service endpoint.
                selfHost.AddServiceEndpoint(typeof(ICalculator), new WSHttpBinding(), "CalculatorService");

                // Step 4 of the hosting procedure: Enable metadata exchange.
                ServiceMetadataBehavior smb = new ServiceMetadataBehavior();
                smb.HttpGetEnabled = true;
                selfHost.Description.Behaviors.Add(smb);

                // Step 5 of the hosting procedure: Start (and then stop) the service.
                selfHost.Open();
                Console.WriteLine("The service is ready.");
                Console.WriteLine("Press <ENTER> to terminate service.");
                Console.WriteLine();
                Console.ReadLine();

                // Close the ServiceHostBase to shutdown the service.
                selfHost.Close();
            }
            catch (CommunicationException ce)
            {
                Console.WriteLine("An exception occurred: {0}", ce.Message);
                selfHost.Abort();
            }
        }
    }
}
```

```vb
Imports System.ServiceModel

Namespace GettingStartedLib

    <ServiceContract(Namespace:="http://Microsoft.ServiceModel.Samples")> _
    Public Interface ICalculator

        <OperationContract()> _
        Function Add(ByVal n1 As Double, ByVal n2 As Double) As Double
        <OperationContract()> _
        Function Subtract(ByVal n1 As Double, ByVal n2 As Double) As Double
        <OperationContract()> _
        Function Multiply(ByVal n1 As Double, ByVal n2 As Double) As Double
        <OperationContract()> _
        Function Divide(ByVal n1 As Double, ByVal n2 As Double) As Double
    End Interface
End Namespace
```

```vb
Imports System.ServiceModel

Namespace GettingStartedLib

    Public Class CalculatorService
        Implements ICalculator

        Public Function Add(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Add
            Dim result As Double = n1 + n2
            ' Code added to write output to the console window.
            Console.WriteLine("Received Add({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result
        End Function

        Public Function Subtract(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Subtract
            Dim result As Double = n1 - n2
            Console.WriteLine("Received Subtract({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result

        End Function

        Public Function Multiply(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Multiply
            Dim result As Double = n1 * n2
            Console.WriteLine("Received Multiply({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result

        End Function

        Public Function Divide(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Divide
            Dim result As Double = n1 / n2
            Console.WriteLine("Received Divide({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result

        End Function
    End Class
End Namespace
```

```vb
Imports System.ServiceModel
Imports System.ServiceModel.Description
Imports GettingStartedLibVB.GettingStartedLib

Module Service

    Class Program
        Shared Sub Main()
            ' Step 1 of the address configuration procedure: Create a URI to serve as the base address.
            Dim baseAddress As New Uri("http://localhost:8000/ServiceModelSamples/Service")

            ' Step 2 of the hosting procedure: Create ServiceHost
            Dim selfHost As New ServiceHost(GetType(CalculatorService), baseAddress)
            Try

                ' Step 3 of the hosting procedure: Add a service endpoint.
                ' Add a service endpoint
                selfHost.AddServiceEndpoint( _
                    GetType(ICalculator), _
                    New WSHttpBinding(), _
                    "CalculatorService")

                ' Step 4 of the hosting procedure: Enable metadata exchange.
                ' Enable metadata exchange
                Dim smb As New ServiceMetadataBehavior()
                smb.HttpGetEnabled = True
                selfHost.Description.Behaviors.Add(smb)

                ' Step 5 of the hosting procedure: Start (and then stop) the service.
                selfHost.Open()
                Console.WriteLine("The service is ready.")
                Console.WriteLine("Press <ENTER> to terminate service.")
                Console.WriteLine()
                Console.ReadLine()

                ' Close the ServiceHostBase to shutdown the service.
                selfHost.Close()
            Catch ce As CommunicationException
                Console.WriteLine("An exception occurred: {0}", ce.Message)
                selfHost.Abort()
            End Try
        End Sub
    End Class

End Module
```

> [!NOTE]
> Les services tels que celui-ci requièrent que l'autorisation enregistre des adresses HTTP sur l'ordinateur pour écouter. Les comptes Administrateur possèdent cette autorisation, mais l'autorisation pour les espaces de noms HTTP doit être accordée aux comptes qui ne sont pas administrateur. Pour plus d’informations sur la configuration des réservations d’espaces de noms, consultez [Configuration de HTTP et HTTPS](../../../docs/framework/wcf/feature-details/configuring-http-and-https.md). Quand il s’exécute dans Visual Studio, le fichier service.exe doit être exécuté avec des privilèges d’administrateur.

## <a name="next-steps"></a>Étapes suivantes

Le service est en cours d'exécution. Dans la tâche suivante, vous créez un client WCF.

> [!div class="nextstepaction"]
> [Comment : créer un client WCF](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)

Pour obtenir des informations sur la résolution des problèmes, consultez la section [Dépannage du tutoriel Bien démarrer](../../../docs/framework/wcf/troubleshooting-the-getting-started-tutorial.md).

## <a name="see-also"></a>Voir aussi

- [Prise en main](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [Auto-hébergement](../../../docs/framework/wcf/samples/self-host.md)