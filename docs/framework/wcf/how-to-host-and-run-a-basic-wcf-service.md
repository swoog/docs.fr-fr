---
title: Comment héberger et exécuter un service Windows Communication Foundation de base
ms.date: 09/14/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF services [WCF]
- WCF services [WCF], running
ms.assetid: 31774d36-923b-4e2d-812e-aa190127266f
ms.openlocfilehash: 73633c2c6119204f2fb608b32ae794a2e07b27d0
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "56747072"
---
# <a name="how-to-host-and-run-a-basic-windows-communication-foundation-service"></a><span data-ttu-id="d9129-102">Comment héberger et exécuter un service Windows Communication Foundation de base</span><span class="sxs-lookup"><span data-stu-id="d9129-102">How to host and run a basic Windows Communication Foundation service</span></span>

<span data-ttu-id="d9129-103">Il s’agit de la troisième des six tâches nécessaires pour créer une application WCF (Windows Communication Foundation).</span><span class="sxs-lookup"><span data-stu-id="d9129-103">This is the third of six tasks required to create a Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="d9129-104">Pour une vue d’ensemble des six tâches, consultez la rubrique [Tutoriel Bien démarrer](getting-started-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="d9129-104">For an overview of all six of the tasks, see the [Getting Started Tutorial](getting-started-tutorial.md) topic.</span></span>

<span data-ttu-id="d9129-105">Cette rubrique explique comment héberger un service WCF (Windows Communication Foundation) dans une application console.</span><span class="sxs-lookup"><span data-stu-id="d9129-105">This topic describes how to host a Windows Communication Foundation (WCF) service in a console application.</span></span> <span data-ttu-id="d9129-106">Cette procédure se compose des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d9129-106">This procedure consists of the following steps:</span></span>

- <span data-ttu-id="d9129-107">Créez un projet d'application console pour héberger le service.</span><span class="sxs-lookup"><span data-stu-id="d9129-107">Create a console application project to host the service.</span></span>

- <span data-ttu-id="d9129-108">Créer un hôte de service pour le service.</span><span class="sxs-lookup"><span data-stu-id="d9129-108">Create a service host for the service.</span></span>

- <span data-ttu-id="d9129-109">Activer l'échange de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="d9129-109">Enable metadata exchange.</span></span>

- <span data-ttu-id="d9129-110">Ouvrir l'hôte de service.</span><span class="sxs-lookup"><span data-stu-id="d9129-110">Open the service host.</span></span>

<span data-ttu-id="d9129-111">La liste complète du code écrit dans cette tâche est fournie dans l’exemple qui suit la procédure.</span><span class="sxs-lookup"><span data-stu-id="d9129-111">A complete listing of the code written in this task is provided in the example following the procedure.</span></span>

## <a name="create-a-new-console-application-to-host-the-service"></a><span data-ttu-id="d9129-112">Créer une nouvelle application de console pour héberger le service</span><span class="sxs-lookup"><span data-stu-id="d9129-112">Create a new console application to host the service</span></span>

1. <span data-ttu-id="d9129-113">Créer un nouveau projet d’Application de Console dans Visual Studio en effectuant un clic droit sur la solution de mise en route et en sélectionnant **ajouter** > **nouveau projet**.</span><span class="sxs-lookup"><span data-stu-id="d9129-113">Create a new Console Application project in Visual Studio by right-clicking on the Getting Started solution and selecting **Add** > **New Project**.</span></span> <span data-ttu-id="d9129-114">Dans le **ajouter un nouveau projet** boîte de dialogue, sur le côté gauche, sélectionnez le **Windows Desktop** catégorie sous **Visual C#** ou **Visual Basic**.</span><span class="sxs-lookup"><span data-stu-id="d9129-114">In the **Add New Project** dialog, on the left-hand side, select the **Windows Desktop** category under **Visual C#** or **Visual Basic**.</span></span> <span data-ttu-id="d9129-115">Sélectionnez le **application Console (.NET Framework)** modèle, puis nommez le projet **GettingStartedHost**.</span><span class="sxs-lookup"><span data-stu-id="d9129-115">Select the **Console App (.NET Framework)** template, and then name the project **GettingStartedHost**.</span></span>

2. <span data-ttu-id="d9129-116">Ajoutez une référence au projet GettingStartedLib dans le projet GettingStartedHost.</span><span class="sxs-lookup"><span data-stu-id="d9129-116">Add a reference to the GettingStartedLib project to the GettingStartedHost project.</span></span> <span data-ttu-id="d9129-117">Avec le bouton droit sur le **références** dossier sous le projet GettingStartedHost dans **l’Explorateur de solutions**, puis sélectionnez **ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="d9129-117">Right-click on the **References** folder under the GettingStartedHost project in **Solution Explorer**, and then select **Add Reference**.</span></span> <span data-ttu-id="d9129-118">Dans le **ajouter une référence** boîte de dialogue, sélectionnez **Solution** sur le côté gauche de la boîte de dialogue, sélectionnez GettingStartedLib dans la section centrale de la boîte de dialogue, puis choisissez **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d9129-118">In the **Add Reference** dialog, select **Solution** on the left-hand side of the dialog, select GettingStartedLib in the center section of the dialog, and then choose **Add**.</span></span> <span data-ttu-id="d9129-119">Cela rend les types définis dans GettingStartedLib disponibles au projet GettingStartedHost.</span><span class="sxs-lookup"><span data-stu-id="d9129-119">This makes the types defined in GettingStartedLib available to the GettingStartedHost project.</span></span>

3. <span data-ttu-id="d9129-120">Ajoutez une référence à System.ServiceModel dans le projet GettingStartedHost.</span><span class="sxs-lookup"><span data-stu-id="d9129-120">Add a reference to System.ServiceModel to the GettingStartedHost project.</span></span> <span data-ttu-id="d9129-121">Avec le bouton droit le **références** dossier sous le projet GettingStartedHost dans **l’Explorateur de solutions** et sélectionnez **ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="d9129-121">Right-click the **References** folder under the GettingStartedHost project in **Solution Explorer** and select **Add Reference**.</span></span> <span data-ttu-id="d9129-122">Dans le **ajouter une référence** boîte de dialogue, sélectionnez **Framework** sur le côté gauche de la boîte de dialogue **assemblys**.</span><span class="sxs-lookup"><span data-stu-id="d9129-122">In the **Add Reference** dialog, select **Framework** on the left-hand side of the dialog under **Assemblies**.</span></span> <span data-ttu-id="d9129-123">Recherchez et sélectionnez **System.ServiceModel**, puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9129-123">Find and select **System.ServiceModel**, and then choose **OK**.</span></span> <span data-ttu-id="d9129-124">Enregistrez la solution en sélectionnant **fichier** > **Enregistrer tout**.</span><span class="sxs-lookup"><span data-stu-id="d9129-124">Save the solution by selecting **File** > **Save All**.</span></span>

## <a name="host-the-service"></a><span data-ttu-id="d9129-125">Héberger le service</span><span class="sxs-lookup"><span data-stu-id="d9129-125">Host the service</span></span>

<span data-ttu-id="d9129-126">Ouvrez le fichier Program.cs ou Module.vb et entrez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d9129-126">Open the Program.cs or Module.vb file and enter the following code:</span></span>

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
            Dim baseAddress As New Uri("http://localhost:8000/GettingStarted")

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

<span data-ttu-id="d9129-127">**Étape 1** -crée une instance de la classe Uri pour contenir l’adresse de base du service.</span><span class="sxs-lookup"><span data-stu-id="d9129-127">**Step 1** - Creates an instance of the Uri class to hold the base address of the service.</span></span> <span data-ttu-id="d9129-128">Les services sont identifiés par une URL, qui contient une adresse de base et un URI facultatif.</span><span class="sxs-lookup"><span data-stu-id="d9129-128">Services are identified by a URL which contains a base address and an optional URI.</span></span> <span data-ttu-id="d9129-129">L’adresse de base est mise en forme comme suit : [transport]://[nom de machine ou domaine][:n° de port facultatif]/[segment d’URI facultatif]L’adresse de base du service de calculatrice utilise le transport HTTP, localhost, le port 8000 et le segment d’URI « GettingStarted »</span><span class="sxs-lookup"><span data-stu-id="d9129-129">The base address is formatted as follows:[transport]://[machine-name or domain][:optional port #]/[optional URI segment]The base address for the calculator service uses the HTTP transport, localhost, port 8000, and the URI segment "GettingStarted"</span></span>

<span data-ttu-id="d9129-130">**Étape 2** – crée une instance de la <xref:System.ServiceModel.ServiceHost> classe pour héberger le service.</span><span class="sxs-lookup"><span data-stu-id="d9129-130">**Step 2** – Creates an instance of the <xref:System.ServiceModel.ServiceHost> class to host the service.</span></span> <span data-ttu-id="d9129-131">Le constructeur prend deux paramètres, le type de la classe qui implémente le contrat de service et l'adresse de base du service.</span><span class="sxs-lookup"><span data-stu-id="d9129-131">The constructor takes two parameters, the type of the class that implements the service contract, and the base address of the service.</span></span>

<span data-ttu-id="d9129-132">**Étape 3** – crée un <xref:System.ServiceModel.Description.ServiceEndpoint> instance.</span><span class="sxs-lookup"><span data-stu-id="d9129-132">**Step 3** – Creates a <xref:System.ServiceModel.Description.ServiceEndpoint> instance.</span></span> <span data-ttu-id="d9129-133">Un point de terminaison de service est composé d'une adresse, d'une liaison et d'un contrat de service.</span><span class="sxs-lookup"><span data-stu-id="d9129-133">A service endpoint is composed of an address, a binding, and a service contract.</span></span> <span data-ttu-id="d9129-134">Le constructeur <xref:System.ServiceModel.Description.ServiceEndpoint> prend donc le type d’interface de contrat de service, une liaison et une adresse.</span><span class="sxs-lookup"><span data-stu-id="d9129-134">The <xref:System.ServiceModel.Description.ServiceEndpoint> constructor therefore takes the service contract interface type, a binding, and an address.</span></span> <span data-ttu-id="d9129-135">Le contrat de service est `ICalculator`, que vous définissez et implémentez dans le type de service.</span><span class="sxs-lookup"><span data-stu-id="d9129-135">The service contract is `ICalculator`, which you defined and implement in the service type.</span></span> <span data-ttu-id="d9129-136">La liaison utilisée dans cet exemple est <xref:System.ServiceModel.WSHttpBinding>, qui est une liaison intégrée utilisée pour se connecter aux points de terminaison qui sont conformes aux spécifications WS-\*.</span><span class="sxs-lookup"><span data-stu-id="d9129-136">The binding used in this sample is <xref:System.ServiceModel.WSHttpBinding> which is a built-in binding that is used for connecting to endpoints that conform to the WS-\* specifications.</span></span> <span data-ttu-id="d9129-137">Pour plus d’informations sur les liaisons WCF, consultez [Vue d’ensemble des liaisons WCF](bindings-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d9129-137">For more information about WCF bindings, see [WCF Bindings Overview](bindings-overview.md).</span></span> <span data-ttu-id="d9129-138">L'adresse est ajoutée à l'adresse de base pour identifier le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="d9129-138">The address is appended to the base address to identify the endpoint.</span></span> <span data-ttu-id="d9129-139">L’adresse spécifiée dans ce code est « CalculatorService », par conséquent, l’adresse complète du point de terminaison est `"http://localhost:8000/GettingStarted/CalculatorService"`.</span><span class="sxs-lookup"><span data-stu-id="d9129-139">The address specified in this code is "CalculatorService" so the fully qualified address for the endpoint is `"http://localhost:8000/GettingStarted/CalculatorService"`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9129-140">L'ajout d'un point de terminaison de service est facultatif lorsque vous utilisez .NET Framework 4 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d9129-140">Adding a service endpoint is optional when using .NET Framework 4 or later.</span></span> <span data-ttu-id="d9129-141">Dans ces versions, si aucun point de terminaison n'est ajouté dans le code ou dans la configuration, WCF ajoute un point de terminaison par défaut pour chaque combinaison d'adresse de base et de contrat implémentée par le service.</span><span class="sxs-lookup"><span data-stu-id="d9129-141">In these versions, if no endpoints are added in code or configuration, WCF adds one default endpoint for each combination of base address and contract implemented by the service.</span></span> <span data-ttu-id="d9129-142">Pour plus d’informations sur les points de terminaison par défaut, consultez [Spécification d’une adresse de point de terminaison](specifying-an-endpoint-address.md).</span><span class="sxs-lookup"><span data-stu-id="d9129-142">For more information about default endpoints see [Specifying an Endpoint Address](specifying-an-endpoint-address.md).</span></span> <span data-ttu-id="d9129-143">Pour plus d’informations sur les points de terminaison, les liaisons et les comportements par défaut, consultez [Configuration simplifiée](simplified-configuration.md) et [Configuration simplifiée pour les services WCF](./samples/simplified-configuration-for-wcf-services.md).</span><span class="sxs-lookup"><span data-stu-id="d9129-143">For more information about default endpoints, bindings, and behaviors, see [Simplified Configuration](simplified-configuration.md) and [Simplified Configuration for WCF Services](./samples/simplified-configuration-for-wcf-services.md).</span></span>

<span data-ttu-id="d9129-144">**Étape 4** – activer l’échange de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="d9129-144">**Step 4** – Enable metadata exchange.</span></span> <span data-ttu-id="d9129-145">Les clients utilisent l'échange de métadonnées pour générer des proxys qui seront utilisés pour appeler les opérations de service.</span><span class="sxs-lookup"><span data-stu-id="d9129-145">Clients will use metadata exchange to generate proxies that will be used to call the service operations.</span></span> <span data-ttu-id="d9129-146">Pour permettre l’échange de métadonnées, créez une instance <xref:System.ServiceModel.Description.ServiceMetadataBehavior>, affectez la valeur <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> à sa propriété `true` et ajoutez le comportement à la collection <xref:System.ServiceModel.Description.ServiceDescription.Behaviors%2A> de l’instance <xref:System.ServiceModel.ServiceHost>.</span><span class="sxs-lookup"><span data-stu-id="d9129-146">To enable metadata exchange create a <xref:System.ServiceModel.Description.ServiceMetadataBehavior> instance, set it’s <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> property to `true`, and add the behavior to the <xref:System.ServiceModel.Description.ServiceDescription.Behaviors%2A> collection of the <xref:System.ServiceModel.ServiceHost> instance.</span></span>

<span data-ttu-id="d9129-147">**Étape 5** – permet d’ouvrir le <xref:System.ServiceModel.ServiceHost> pour écouter les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="d9129-147">**Step 5** – Open the <xref:System.ServiceModel.ServiceHost> to listen for incoming messages.</span></span> <span data-ttu-id="d9129-148">Notez que le code attend que l'utilisateur appuie sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="d9129-148">Notice the code waits for the user to hit enter.</span></span> <span data-ttu-id="d9129-149">Si vous n'effectuez pas cette opération, l'application se ferme immédiatement et le service s'arrête. Notez également le bloc try/catch utilisé.</span><span class="sxs-lookup"><span data-stu-id="d9129-149">If you do not do this, the app will close immediately and the service will shut down.Also notice a  try/catch block used.</span></span> <span data-ttu-id="d9129-150">Une fois que <xref:System.ServiceModel.ServiceHost> a été instancié, le reste du code est placé dans un bloc try/catch.</span><span class="sxs-lookup"><span data-stu-id="d9129-150">After the <xref:System.ServiceModel.ServiceHost> has been instantiated, all other code is placed in a try/catch block.</span></span> <span data-ttu-id="d9129-151">Pour plus d’informations sur l’interception en toute sécurité les exceptions levées par <xref:System.ServiceModel.ServiceHost>, consultez [utilisation fermer et abandon pour libérer les ressources de client WCF](samples/use-close-abort-release-wcf-client-resources.md)</span><span class="sxs-lookup"><span data-stu-id="d9129-151">For more information about safely catching exceptions thrown by <xref:System.ServiceModel.ServiceHost>, see [Use Close and Abort to release WCF client resources](samples/use-close-abort-release-wcf-client-resources.md)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9129-152">Lorsque vous ajoutez une bibliothèque de Service WCF, Visual Studio peut héberger pour vous lorsque vous déboguez en démarrant un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="d9129-152">When you add a WCF Service Library, Visual Studio can host it for you when you debug by starting a service host.</span></span> <span data-ttu-id="d9129-153">Pour éviter les conflits, vous pouvez désactiver cette.</span><span class="sxs-lookup"><span data-stu-id="d9129-153">To avoid conflicts you can disable this.</span></span> 
> 1. <span data-ttu-id="d9129-154">Ouvrez les propriétés de projet GettingStartedLib.</span><span class="sxs-lookup"><span data-stu-id="d9129-154">Open Project Properties for GettingStartedLib.</span></span>
> 2. <span data-ttu-id="d9129-155">Accédez à **Options WCF** et décochez la case **démarrer WCF Service hôte lors du débogage**.</span><span class="sxs-lookup"><span data-stu-id="d9129-155">Go to **WCF Options** and uncheck **Start WCF Service Host when debugging**.</span></span>

## <a name="verify-the-service-is-working"></a><span data-ttu-id="d9129-156">Vérifiez que le service fonctionne</span><span class="sxs-lookup"><span data-stu-id="d9129-156">Verify the service is working</span></span>

1. <span data-ttu-id="d9129-157">Exécutez la console GettingStartedHost application à partir de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d9129-157">Run the GettingStartedHost console application from inside Visual Studio.</span></span>

   <span data-ttu-id="d9129-158">Le service doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d9129-158">The service must be run with administrator privileges.</span></span> <span data-ttu-id="d9129-159">Étant donné que Visual Studio a été ouverte avec des privilèges d’administrateur, GettingStartedHost est également exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d9129-159">Because Visual Studio was opened with administrator privileges, GettingStartedHost is also run with administrator privileges.</span></span> <span data-ttu-id="d9129-160">Vous pouvez également ouvrir une invite de commandes en utilisant **exécuter en tant qu’administrateur** et exécutez service.exe qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="d9129-160">You can also open a new command prompt using **Run as administrator** and run service.exe within it.</span></span>

2. <span data-ttu-id="d9129-161">Ouvrez un navigateur web et accédez à la page du service debug à `http://localhost:8000/GettingStarted/`.</span><span class="sxs-lookup"><span data-stu-id="d9129-161">Open a web browser and browse to the service's debug page at `http://localhost:8000/GettingStarted/`.</span></span> <span data-ttu-id="d9129-162">**Remarque : Barre oblique de fin est importante.**</span><span class="sxs-lookup"><span data-stu-id="d9129-162">**Note! Ending slash is significant.**</span></span>

## <a name="example"></a><span data-ttu-id="d9129-163">Exemple</span><span class="sxs-lookup"><span data-stu-id="d9129-163">Example</span></span>

<span data-ttu-id="d9129-164">L'exemple suivant inclut le contrat de service et l'implémentation d'étapes précédentes dans le didacticiel et héberge le service dans une application console.</span><span class="sxs-lookup"><span data-stu-id="d9129-164">The following example includes the service contract and implementation from previous steps in the tutorial and hosts the service in a console application.</span></span>

<span data-ttu-id="d9129-165">Pour compiler avec un compilateur de ligne de commande, compilez IService1.cs et Service1.cs dans une bibliothèque de classes qui fait référence à `System.ServiceModel.dll`.</span><span class="sxs-lookup"><span data-stu-id="d9129-165">To compile this with a command-line compiler, compile IService1.cs and Service1.cs into a class library that references `System.ServiceModel.dll`.</span></span> <span data-ttu-id="d9129-166">Compilez le fichier Program.cs comme une application console.</span><span class="sxs-lookup"><span data-stu-id="d9129-166">Compile Program.cs as a console application.</span></span>

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
            Uri baseAddress = new Uri("http://localhost:8000/GettingStarted/");

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
            Dim baseAddress As New Uri("http://localhost:8000/GettingStarted/")

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
> <span data-ttu-id="d9129-167">Les services tels que celui-ci requièrent que l'autorisation enregistre des adresses HTTP sur l'ordinateur pour écouter.</span><span class="sxs-lookup"><span data-stu-id="d9129-167">Services such as this one require permission to register HTTP addresses on the machine for listening.</span></span> <span data-ttu-id="d9129-168">Les comptes Administrateur possèdent cette autorisation, mais l'autorisation pour les espaces de noms HTTP doit être accordée aux comptes qui ne sont pas administrateur.</span><span class="sxs-lookup"><span data-stu-id="d9129-168">Administrator accounts have this permission, but non-administrator accounts must be granted permission for HTTP namespaces.</span></span> <span data-ttu-id="d9129-169">Pour plus d’informations sur la configuration des réservations d’espaces de noms, consultez [Configuration de HTTP et HTTPS](feature-details/configuring-http-and-https.md).</span><span class="sxs-lookup"><span data-stu-id="d9129-169">For more information about how to configure namespace reservations, see [Configuring HTTP and HTTPS](feature-details/configuring-http-and-https.md).</span></span> <span data-ttu-id="d9129-170">Quand il s’exécute dans Visual Studio, le fichier service.exe doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d9129-170">When running under Visual Studio, the service.exe must be run with administrator privileges.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d9129-171">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="d9129-171">Next steps</span></span>

<span data-ttu-id="d9129-172">Le service est en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="d9129-172">Now the service is running.</span></span> <span data-ttu-id="d9129-173">Dans la tâche suivante, vous créez un client WCF.</span><span class="sxs-lookup"><span data-stu-id="d9129-173">In the next task, you create a WCF client.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="d9129-174">Guide pratique pour Créer un client WCF</span><span class="sxs-lookup"><span data-stu-id="d9129-174">How to: Create a WCF client</span></span>](how-to-create-a-wcf-client.md)

<span data-ttu-id="d9129-175">Pour obtenir des informations sur la résolution des problèmes, consultez la section [Dépannage du tutoriel Bien démarrer](troubleshooting-the-getting-started-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="d9129-175">For troubleshooting information, see [Troubleshooting the Getting Started Tutorial](troubleshooting-the-getting-started-tutorial.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d9129-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9129-176">See also</span></span>

- [<span data-ttu-id="d9129-177">Prise en main</span><span class="sxs-lookup"><span data-stu-id="d9129-177">Getting Started</span></span>](samples/getting-started-sample.md)
- [<span data-ttu-id="d9129-178">Auto-hébergement</span><span class="sxs-lookup"><span data-stu-id="d9129-178">Self-Host</span></span>](samples/self-host.md)
- [<span data-ttu-id="d9129-179">Hébergement de services</span><span class="sxs-lookup"><span data-stu-id="d9129-179">Hosting Services</span></span>](hosting-services.md)
