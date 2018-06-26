---
title: Guide pratique pour héberger et exécuter un service Windows Communication Foundation de base
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF services [WCF]
- WCF services [WCF], running
ms.assetid: 31774d36-923b-4e2d-812e-aa190127266f
ms.openlocfilehash: f1c56ed83fa214cf781a833e05642635ac24b0c5
ms.sourcegitcommit: d8bf4976eafe3289275be3811e7cb721bfff7e1e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34753498"
---
# <a name="how-to-host-and-run-a-basic-windows-communication-foundation-service"></a>Guide pratique pour héberger et exécuter un service Windows Communication Foundation de base
Il s’agit de la troisième des six tâches nécessaires pour créer une application WCF (Windows Communication Foundation). Pour une vue d’ensemble des six tâches, consultez la rubrique [Tutoriel Bien démarrer](../../../docs/framework/wcf/getting-started-tutorial.md).  
  
 Cette rubrique explique comment héberger un service WCF (Windows Communication Foundation) dans une application console. Cette procédure se compose des étapes suivantes :  
  
-   Créez un projet d'application console pour héberger le service.  
  
-   Créer un hôte de service pour le service.  
  
-   Activer l'échange de métadonnées.  
  
-   Ouvrir l'hôte de service.  
  
 La liste complète du code écrit dans cette tâche est fournie dans l'exemple qui suit la procédure.  
  
## <a name="to-create-a-new-console-application-to-host-the-service"></a>Pour créer une nouvelle application console pour héberger le service  
  
1.  Créez un projet d’application console en cliquant avec le bouton droit sur la solution Mise en route, puis en sélectionnant **Ajouter**, **Nouveau projet**. Dans la boîte de dialogue **Ajouter un nouveau projet**, dans la partie gauche de la boîte de dialogue, sélectionnez **Windows** sous **C#** ou **VB**. Dans la section centrale de la boîte de dialogue, sélectionnez **Application console**. Nom du projet GettingStartedHost.  
  
2.  Affectez au framework cible du projet GettingStartedHost le .NET Framework 4.5 en cliquant avec le bouton droit sur **GettingStartedHost** dans l’Explorateur de solutions, puis en sélectionnant **Propriétés**. Dans la zone de liste déroulante **Framework cible**, sélectionnez **.NET Framework 4.5**. Définir le framework cible d’un projet VB est un peu différent. Dans la boîte de dialogue de propriétés du projet GettingStartedHost, cliquez sur l’onglet **Compiler** à gauche de l’écran, puis cliquez sur le bouton **Options avancées de compilation** dans le coin inférieur gauche de la boîte de dialogue. Sélectionnez ensuite **.NET Framework 4.5** dans la liste déroulante **Framework cible**.  
  
     La définition du framework cible entraîne le rechargement de la solution par [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)]. Appuyez sur **OK** quand vous y êtes invité.  
  
3.  Ajoutez une référence au projet GettingStartedLib dans le projet GettingStartedHost en cliquant avec le bouton droit sur le dossier **Références** sous le projet GettingStartedHost dans l’Explorateur de solutions, puis sélectionnez **Ajouter une référence**. Dans la boîte de dialogue **Ajouter une référence**, sélectionnez **Solution** dans la partie gauche de la boîte de dialogue, sélectionnez GettingStartedLib dans la section centrale de la boîte de dialogue, puis cliquez sur **Ajouter**. Cela rend les types définis dans GettingStartedLib disponibles au projet GettingStartedHost.  
  
4.  Ajoutez une référence à System.ServiceModel dans le projet GettingStartedHost en cliquant avec le bouton droit sur le dossier **Référence** sous le projet GettingStartedHost dans l’Explorateur de solutions, puis sélectionnez **Ajouter une référence**. Dans la boîte de dialogue **Ajouter une référence**, sélectionnez **Framework** dans la partie gauche de la boîte de dialogue. Dans la zone de texte Rechercher des assemblys, tapez `System.ServiceModel`. Dans la section centrale de la boîte de dialogue, sélectionnez **System.ServiceModel**, cliquez sur le bouton **Ajouter**, puis sur le bouton **Fermer**. Enregistrez la solution en cliquant sur le bouton Enregistrer tout dans le menu principal.  
  
### <a name="to-host-the-service"></a>Pour héberger le service  
  
-   Ouvrez le fichier Program.cs ou Module.vb et entrez le code suivant :  
  
    ```csharp
    // program.cs  
    using System;  
    using System.Collections.Generic;  
    using System.Linq;  
    using System.Text;  
    using System.ServiceModel;  
    using GettingStartedLib;  
    using System.ServiceModel.Description;   
  
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
    'Module1.vb  
    Imports System  
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
  
    1.  Étape 1 - Crée une instance de la classe URI pour contenir l'adresse de base du service. Les services sont identifiés par une URL, qui contient une adresse de base et un URI facultatif. L’adresse de base est mise en forme comme suit : [transport]://[nom de machine ou domaine][:n° de port facultatif]/[segment d’URI facultatif]L’adresse de base du service de calculatrice utilise le transport HTTP, localhost, le port 8000 et le segment d’URI « GettingStarted »  
  
    2.  Étape 2 – Crée une instance de la classe <xref:System.ServiceModel.ServiceHost> pour héberger le service. Le constructeur prend deux paramètres, le type de la classe qui implémente le contrat de service et l'adresse de base du service.  
  
    3.  Étape 3 - Crée une instance <xref:System.ServiceModel.Description.ServiceEndpoint>. Un point de terminaison de service est composé d’une adresse, d’une liaison et d’un contrat de service. Le constructeur <xref:System.ServiceModel.Description.ServiceEndpoint> prend donc le type d'interface de contrat de service, une liaison et une adresse. Le contrat de service est `ICalculator`, que vous définissez et implémentez dans le type de service. La liaison utilisée dans cet exemple est <xref:System.ServiceModel.WSHttpBinding>, qui est une liaison intégrée utilisée pour se connecter aux points de terminaison qui sont conformes aux spécifications WS-*. Pour plus d’informations sur les liaisons WCF, consultez [Vue d’ensemble des liaisons WCF](../../../docs/framework/wcf/bindings-overview.md). L'adresse est ajoutée à l'adresse de base pour identifier le point de terminaison. L’adresse spécifiée dans ce code est « CalculatorService ». L’adresse complète du point de terminaison est donc `"http://localhost:8000/GettingStarted/CalculatorService"`. L’ajout d’un point de terminaison de service est facultatif avec .NET Framework 4.0 ou une version ultérieure. Dans ces versions, si aucun point de terminaison n'est ajouté dans le code ou dans la configuration, WCF ajoute un point de terminaison par défaut pour chaque combinaison d'adresse de base et de contrat implémentée par le service. Pour plus d’informations sur les points de terminaison par défaut, consultez [Spécification d’une adresse de point de terminaison](../../../docs/framework/wcf/specifying-an-endpoint-address.md). Pour plus d’informations sur les points de terminaison, les liaisons et les comportements par défaut, consultez [Configuration simplifiée](../../../docs/framework/wcf/simplified-configuration.md) et [Configuration simplifiée pour les services WCF](../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).  
  
        > [!IMPORTANT]
        >  L'ajout d'un point de terminaison de service est facultatif lorsque vous utilisez .NET Framework 4 ou version ultérieure. Dans ces versions, si aucun point de terminaison n'est ajouté dans le code ou dans la configuration, WCF ajoute un point de terminaison par défaut pour chaque combinaison d'adresse de base et de contrat implémentée par le service. Pour plus d’informations sur les points de terminaison par défaut, consultez [Spécification d’une adresse de point de terminaison](../../../docs/framework/wcf/specifying-an-endpoint-address.md). Pour plus d’informations sur les points de terminaison, les liaisons et les comportements par défaut, consultez [Configuration simplifiée](../../../docs/framework/wcf/simplified-configuration.md) et [Configuration simplifiée pour les services WCF](../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).  
  
    4.  Étape 4 – Activer l'échange de métadonnées. Les clients utilisent l'échange de métadonnées pour générer des proxys qui seront utilisés pour appeler les opérations de service. Pour permettre l’échange de métadonnées, créez une instance de <xref:System.ServiceModel.Description.ServiceMetadataBehavior>, affectez à sa propriété <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> la valeur `true`, puis ajoutez le comportement à la collection <!--zz <xref:System.ServiceModel.ServiceHost.Behaviors%2A>  -->`System.ServiceModel.ServiceHost.Behaviors%2A` de l’instance <xref:System.ServiceModel.ServiceHost>.  
  
    5.  Étape 5 - Ouvrir <xref:System.ServiceModel.ServiceHost> pour écouter les messages entrants. Notez que le code attend que l'utilisateur appuie sur Entrée. Si vous n'effectuez pas cette opération, l'application se ferme immédiatement et le service s'arrête. Notez également le bloc try/catch utilisé. Une fois que <xref:System.ServiceModel.ServiceHost> a été instancié, le reste du code est placé dans un bloc try/catch. Pour plus d’informations sur l’interception en toute sécurité des exceptions levées par <xref:System.ServiceModel.ServiceHost>, consultez la section [Éviter les problèmes avec l’instruction Using](../../../docs/framework/wcf/samples/avoiding-problems-with-the-using-statement.md)  
  
### <a name="to-verify-the-service-is-working"></a>Pour vérifier que le service fonctionne  
  
1.  Exécutez l'application console GettingStartedHost à partir de [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)]. Lors de l'exécution sur [!INCLUDE[wv](../../../includes/wv-md.md)] et les systèmes d'exploitation ultérieurs, le service doit être exécuté avec des privilèges d'administrateur. Dans la mesure où Visual Studio a été exécuté avec des privilèges d’administrateur, GettingStartedHost est également exécuté avec des privilèges d’administrateur. Vous pouvez aussi démarrer une nouvelle invite de commandes qui l'exécute avec les privilèges d'administrateur et y exécuter service.exe.  
  
2.  Ouvrez Internet Explorer et accédez à la page de débogage du service à l'adresse `http://localhost:8000/GettingStarted/CalculatorService`.  
  
## <a name="example"></a>Exemple  
 L'exemple suivant inclut le contrat de service et l'implémentation d'étapes précédentes dans le didacticiel et héberge le service dans une application console.  
  
 Pour le compiler avec un compilateur en ligne de commande, compilez IService1.cs et Service1.cs dans une bibliothèque de classes référençant `System.ServiceModel.dll`. Et compilez le fichier Program.cs dans une application console.  
  
```csharp
// IService1.cs  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using System.Runtime.Serialization;  
using System.ServiceModel;  
using System.Text;  
  
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
// Service1.cs  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using System.Runtime.Serialization;  
using System.ServiceModel;  
using System.Text;  
  
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
//Program.cs  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using System.Text;  
using System.ServiceModel;  
using GettingStartedLib;  
using System.ServiceModel.Description;   
  
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
'IService1.vb  
Imports System  
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
'Service1.vb  
Imports System  
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
'Module1.vb  
Imports System  
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
>  Les services tels que celui-ci requièrent que l'autorisation enregistre des adresses HTTP sur l'ordinateur pour écouter. Les comptes Administrateur possèdent cette autorisation, mais l'autorisation pour les espaces de noms HTTP doit être accordée aux comptes qui ne sont pas administrateur. Pour plus d’informations sur la configuration des réservations d’espaces de noms, consultez [Configuration de HTTP et HTTPS](../../../docs/framework/wcf/feature-details/configuring-http-and-https.md). Quand il s’exécute dans Visual Studio, le fichier service.exe doit être exécuté avec des privilèges d’administrateur.  
  
 Le service est en cours d'exécution. Passez à [Guide pratique pour créer un client](../../../docs/framework/wcf/how-to-create-a-wcf-client.md). Pour obtenir des informations sur la résolution des problèmes, consultez la section [Dépannage du tutoriel Bien démarrer](../../../docs/framework/wcf/troubleshooting-the-getting-started-tutorial.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Prise en main](../../../docs/framework/wcf/samples/getting-started-sample.md)  
 [Auto-hébergement](../../../docs/framework/wcf/samples/self-host.md)
