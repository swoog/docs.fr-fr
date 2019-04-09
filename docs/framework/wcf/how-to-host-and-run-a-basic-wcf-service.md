---
title: 'Tutoriel : Héberger et exécuter un service Windows Communication Foundation de base'
ms.date: 03/19/2019
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF services [WCF]
- WCF services [WCF], running
ms.assetid: 31774d36-923b-4e2d-812e-aa190127266f
ms.openlocfilehash: ad9536b1f27ba3945bf76d0474de4825033a1e8b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59197904"
---
# <a name="tutorial-host-and-run-a-basic-windows-communication-foundation-service"></a><span data-ttu-id="33a15-102">Tutoriel : Héberger et exécuter un service Windows Communication Foundation de base</span><span class="sxs-lookup"><span data-stu-id="33a15-102">Tutorial: Host and run a basic Windows Communication Foundation service</span></span>

<span data-ttu-id="33a15-103">Ce didacticiel décrit la troisième des cinq tâches requises pour créer une application Windows Communication Foundation (WCF) de base.</span><span class="sxs-lookup"><span data-stu-id="33a15-103">This tutorial describes the third of five tasks required to create a basic Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="33a15-104">Pour une vue d’ensemble des didacticiels, consultez [didacticiel : Prise en main les applications Windows Communication Foundation](getting-started-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="33a15-104">For an overview of the tutorials, see [Tutorial: Get started with Windows Communication Foundation applications](getting-started-tutorial.md).</span></span>

<span data-ttu-id="33a15-105">La tâche suivante pour créer une application WCF consiste à héberger un service WCF dans une application console.</span><span class="sxs-lookup"><span data-stu-id="33a15-105">The next task for creating a WCF application is to host a WCF service in a console application.</span></span> <span data-ttu-id="33a15-106">Un service WCF expose un ou plusieurs *points de terminaison*, chacun d'entre eux exposant une ou plusieurs opérations de service.</span><span class="sxs-lookup"><span data-stu-id="33a15-106">A WCF service exposes one or more *endpoints*, each of which exposes one or more service operations.</span></span> <span data-ttu-id="33a15-107">Un point de terminaison de service spécifie les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="33a15-107">A service endpoint specifies the following information:</span></span> 
- <span data-ttu-id="33a15-108">Une adresse où vous pouvez trouver le service.</span><span class="sxs-lookup"><span data-stu-id="33a15-108">An address where you can find the service.</span></span>
- <span data-ttu-id="33a15-109">Une liaison qui contient les informations qui décrivent comment un client doit communiquer avec le service.</span><span class="sxs-lookup"><span data-stu-id="33a15-109">A binding that contains the information that describes how a client must communicate with the service.</span></span> 
- <span data-ttu-id="33a15-110">Un contrat qui définit les fonctionnalités fournies par le service à ses clients.</span><span class="sxs-lookup"><span data-stu-id="33a15-110">A contract that defines the functionality that the service provides to its clients.</span></span>

<span data-ttu-id="33a15-111">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="33a15-111">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> - <span data-ttu-id="33a15-112">Créez et configurez un projet d’application console pour l’hébergement d’un service WCF.</span><span class="sxs-lookup"><span data-stu-id="33a15-112">Create and configure a console app project for hosting a WCF service.</span></span>
> - <span data-ttu-id="33a15-113">Ajoutez le code pour héberger le service WCF.</span><span class="sxs-lookup"><span data-stu-id="33a15-113">Add code to host the WCF service.</span></span>
> - <span data-ttu-id="33a15-114">Mettre à jour le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="33a15-114">Update the configuration file.</span></span>
> - <span data-ttu-id="33a15-115">Démarrer le service WCF et vérifier qu’il est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="33a15-115">Start the WCF service and verify it's running.</span></span>

## <a name="create-and-configure-a-console-app-project-for-hosting-the-service"></a><span data-ttu-id="33a15-116">Créer et configurer un projet d’application console pour héberger le service</span><span class="sxs-lookup"><span data-stu-id="33a15-116">Create and configure a console app project for hosting the service</span></span>

1. <span data-ttu-id="33a15-117">Créer un projet d’application console dans Visual Studio :</span><span class="sxs-lookup"><span data-stu-id="33a15-117">Create a console app project in Visual Studio:</span></span> 
 
    1. <span data-ttu-id="33a15-118">À partir de la **fichier** menu, sélectionnez **Open** > **projet/Solution** et accédez à la **GettingStarted** solution vous créé précédemment (*GettingStarted.sln*).</span><span class="sxs-lookup"><span data-stu-id="33a15-118">From the **File** menu, select **Open** > **Project/Solution** and browse to the **GettingStarted** solution you previously created (*GettingStarted.sln*).</span></span> <span data-ttu-id="33a15-119">Sélectionnez **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="33a15-119">Select **Open**.</span></span>

    2. <span data-ttu-id="33a15-120">À partir de la **vue** menu, sélectionnez **l’Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="33a15-120">From the **View** menu, select **Solution Explorer**.</span></span>
    
    3. <span data-ttu-id="33a15-121">Dans le **l’Explorateur de solutions** fenêtre, sélectionnez le **GettingStarted** solution (nœud supérieur) et sélectionnez **ajouter** > **denouveauprojet** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="33a15-121">In the **Solution Explorer** window, select the **GettingStarted** solution (top node), and then select **Add** > **New Project** from the shortcut menu.</span></span> 

    4. <span data-ttu-id="33a15-122">Dans le **ajouter un nouveau projet** fenêtre, sur le côté gauche, sélectionnez le **Windows Desktop** catégorie sous **Visual C#**  ou **Visual Basic**.</span><span class="sxs-lookup"><span data-stu-id="33a15-122">In the **Add New Project** window, on the left side, select the **Windows Desktop** category under **Visual C#** or **Visual Basic**.</span></span> 

    5. <span data-ttu-id="33a15-123">Sélectionnez le **application Console (.NET Framework)** modèle, puis entrez *GettingStartedHost* pour le **nom**.</span><span class="sxs-lookup"><span data-stu-id="33a15-123">Select the **Console App (.NET Framework)** template, and enter *GettingStartedHost* for the **Name**.</span></span> <span data-ttu-id="33a15-124">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="33a15-124">Select **OK**.</span></span>

2. <span data-ttu-id="33a15-125">Ajouter une référence dans le **GettingStartedHost** de projet pour le **GettingStartedLib** projet :</span><span class="sxs-lookup"><span data-stu-id="33a15-125">Add a reference in the **GettingStartedHost** project to the **GettingStartedLib** project:</span></span> 

    1. <span data-ttu-id="33a15-126">Dans le **l’Explorateur de solutions** fenêtre, sélectionnez le **références** dossier sous le **GettingStartedHost** de projet, puis sélectionnez **ajouter une référence** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="33a15-126">In the **Solution Explorer** window, select the **References** folder under the **GettingStartedHost** project, and then select **Add Reference** from the shortcut menu.</span></span> 

    2. <span data-ttu-id="33a15-127">Dans le **ajouter une référence** boîte de dialogue, sous **projets** sur le côté gauche de la fenêtre, sélectionnez **Solution**.</span><span class="sxs-lookup"><span data-stu-id="33a15-127">In the **Add Reference** dialog, under **Projects** on the left side of the window, select **Solution**.</span></span> 
 
    3. <span data-ttu-id="33a15-128">Sélectionnez **GettingStartedLib** dans la section centrale de la fenêtre, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="33a15-128">Select **GettingStartedLib** in the center section of the window, and then select **OK**.</span></span> 

       <span data-ttu-id="33a15-129">Cette action rend les types définis dans le **GettingStartedLib** projet disponible à la **GettingStartedHost** projet.</span><span class="sxs-lookup"><span data-stu-id="33a15-129">This action makes the types defined in the **GettingStartedLib** project available to the **GettingStartedHost** project.</span></span>

3. <span data-ttu-id="33a15-130">Ajouter une référence dans le **GettingStartedHost** de projet pour le <xref:System.ServiceModel> assembly :</span><span class="sxs-lookup"><span data-stu-id="33a15-130">Add a reference in the **GettingStartedHost** project to the <xref:System.ServiceModel> assembly:</span></span> 

    1. <span data-ttu-id="33a15-131">Dans le **l’Explorateur de solutions** fenêtre, sélectionnez le **références** dossier sous le **GettingStartedHost** de projet, puis sélectionnez **ajouter une référence** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="33a15-131">In the **Solution Explorer** window, select the **References** folder under the **GettingStartedHost** project, and then select **Add Reference** from the shortcut menu.</span></span>
    
    2. <span data-ttu-id="33a15-132">Dans le **ajouter une référence** fenêtre, sous **assemblys** sur le côté gauche de la fenêtre, sélectionnez **Framework**.</span><span class="sxs-lookup"><span data-stu-id="33a15-132">In the **Add Reference** window, under **Assemblies** on the left side of the window, select **Framework**.</span></span> 

    3. <span data-ttu-id="33a15-133">Sélectionnez **System.ServiceModel**, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="33a15-133">Select **System.ServiceModel**, and then select **OK**.</span></span> 
    
    4. <span data-ttu-id="33a15-134">Enregistrez la solution en sélectionnant **fichier** > **Enregistrer tout**.</span><span class="sxs-lookup"><span data-stu-id="33a15-134">Save the solution by selecting **File** > **Save All**.</span></span>

## <a name="add-code-to-host-the-service"></a><span data-ttu-id="33a15-135">Ajoutez le code pour héberger le service</span><span class="sxs-lookup"><span data-stu-id="33a15-135">Add code to host the service</span></span>

<span data-ttu-id="33a15-136">Pour héberger le service, vous ajoutez le code pour effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="33a15-136">To host the service, you add code to do the following steps:</span></span> 
   1. <span data-ttu-id="33a15-137">Créer un URI pour l’adresse de base.</span><span class="sxs-lookup"><span data-stu-id="33a15-137">Create a URI for the base address.</span></span>
   2. <span data-ttu-id="33a15-138">Créer une instance de classe pour héberger le service.</span><span class="sxs-lookup"><span data-stu-id="33a15-138">Create a class instance for hosting the service.</span></span>
   3. <span data-ttu-id="33a15-139">Créer un point de terminaison de service.</span><span class="sxs-lookup"><span data-stu-id="33a15-139">Create a service endpoint.</span></span>
   4. <span data-ttu-id="33a15-140">Activer l'échange de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="33a15-140">Enable metadata exchange.</span></span>
   5. <span data-ttu-id="33a15-141">Ouvrez l’hôte de service pour écouter les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="33a15-141">Open the service host to listen for incoming messages.</span></span>
  
<span data-ttu-id="33a15-142">Apportez les modifications suivantes au code :</span><span class="sxs-lookup"><span data-stu-id="33a15-142">Make the following changes to the code:</span></span>

1. <span data-ttu-id="33a15-143">Ouvrez le **Program.cs** ou **Module1.vb** de fichiers dans le **GettingStartedHost** de projet et remplacez son code par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="33a15-143">Open the **Program.cs** or **Module1.vb** file in the **GettingStartedHost** project and replace its code with the following code:</span></span>

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
                // Step 1: Create a URI to serve as the base address.
                Uri baseAddress = new Uri("http://localhost:8000/GettingStarted/");

                // Step 2: Create a ServiceHost instance.
                ServiceHost selfHost = new ServiceHost(typeof(CalculatorService), baseAddress);

                try
                {
                    // Step 3: Add a service endpoint.
                    selfHost.AddServiceEndpoint(typeof(ICalculator), new WSHttpBinding(), "CalculatorService");

                    // Step 4: Enable metadata exchange.
                    ServiceMetadataBehavior smb = new ServiceMetadataBehavior();
                    smb.HttpGetEnabled = true;
                    selfHost.Description.Behaviors.Add(smb)    ;

                    // Step 5: Start the service.
                    selfHost.Open();
                    Console.WriteLine("The service is ready.");

                    // Close the ServiceHost to stop the service.
                    Console.WriteLine("Press <Enter> to terminate the service.");
                    Console.WriteLine();
                    Console.ReadLine();
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
    Imports GettingStartedLib.GettingStartedLib

    Module Service

        Class Program
            Shared Sub Main()
                ' Step 1: Create a URI to serve as the base address.
                Dim baseAddress As New Uri("http://localhost:8000/GettingStarted/")

                ' Step 2: Create a ServiceHost instance.
                Dim selfHost As New ServiceHost(GetType(CalculatorService), baseAddress)
               Try

                    ' Step 3: Add a service endpoint.
                    selfHost.AddServiceEndpoint( _
                        GetType(ICalculator), _
                        New WSHttpBinding(), _
                        "CalculatorService")

                    ' Step 4: Enable metadata exchange.
                    Dim smb As New ServiceMetadataBehavior()
                    smb.HttpGetEnabled = True
                    selfHost.Description.Behaviors.Add(smb)

                    ' Step 5: Start the service.
                    selfHost.Open()
                    Console.WriteLine("The service is ready.")

                    ' Close the ServiceHost to stop the service.
                    Console.WriteLine("Press <Enter> to terminate the service.")
                    Console.WriteLine()
                    Console.ReadLine()
                    selfHost.Close()

                Catch ce As CommunicationException
                    Console.WriteLine("An exception occurred: {0}", ce.Message)
                    selfHost.Abort()
                End Try
            End Sub
        End Class

    End Module
    ```
    
    <span data-ttu-id="33a15-144">Pour plus d’informations sur le fonctionne de ce code, consultez [Service étapes du programme d’hébergement](#service-hosting-program-steps).</span><span class="sxs-lookup"><span data-stu-id="33a15-144">For information about how this code works, see [Service hosting program steps](#service-hosting-program-steps).</span></span>

2. <span data-ttu-id="33a15-145">Mettre à jour les propriétés du projet :</span><span class="sxs-lookup"><span data-stu-id="33a15-145">Update the project properties:</span></span>

   1. <span data-ttu-id="33a15-146">Dans le **l’Explorateur de solutions** fenêtre, sélectionnez le **GettingStartedHost** dossier, puis sélectionnez **propriétés** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="33a15-146">In the **Solution Explorer** window, select the **GettingStartedHost** folder, and then select **Properties** from the shortcut menu.</span></span>

   2. <span data-ttu-id="33a15-147">Sur le **GettingStartedHost** page de propriétés, sélectionnez le **Application** onglet :</span><span class="sxs-lookup"><span data-stu-id="33a15-147">On the **GettingStartedHost** properties page, select the **Application** tab:</span></span>

      - <span data-ttu-id="33a15-148">Pour C# projets, sélectionnez **GettingStartedHost.Program** à partir de la **objet de démarrage** liste.</span><span class="sxs-lookup"><span data-stu-id="33a15-148">For C# projects, select **GettingStartedHost.Program** from the **Startup object** list.</span></span>

      - <span data-ttu-id="33a15-149">Pour les projets Visual Basic, sélectionnez **Service.Program** à partir de la **objet de démarrage** liste.</span><span class="sxs-lookup"><span data-stu-id="33a15-149">For Visual Basic projects, select **Service.Program** from the **Startup object** list.</span></span>

   3. <span data-ttu-id="33a15-150">À partir de la **fichier** menu, sélectionnez **Enregistrer tout**.</span><span class="sxs-lookup"><span data-stu-id="33a15-150">From the **File** menu, select **Save All**.</span></span>

## <a name="verify-the-service-is-working"></a><span data-ttu-id="33a15-151">Vérifiez que le service fonctionne</span><span class="sxs-lookup"><span data-stu-id="33a15-151">Verify the service is working</span></span>

1. <span data-ttu-id="33a15-152">Générez la solution, puis exécutez le **GettingStartedHost** console application à partir de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="33a15-152">Build the solution, and then run the **GettingStartedHost** console application from inside Visual Studio.</span></span> 

    <span data-ttu-id="33a15-153">Le service doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="33a15-153">The service must be run with administrator privileges.</span></span> <span data-ttu-id="33a15-154">Étant donné que vous avez ouvert Visual Studio avec des privilèges d’administrateur, lorsque vous exécutez **GettingStartedHost** dans Visual Studio, l’application est exécutée avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="33a15-154">Because you opened Visual Studio with administrator privileges, when you run **GettingStartedHost** in Visual Studio, the application is run with administrator privileges as well.</span></span> <span data-ttu-id="33a15-155">Comme alternative, vous pouvez ouvrir une nouvelle invite de commandes en tant qu’administrateur (sélectionnez **plus** > **exécuter en tant qu’administrateur** dans le menu contextuel) et exécutez **GettingStartedHost.exe**  qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="33a15-155">As an alternative, you can open a new command prompt as an administrator (select **More** > **Run as administrator** from the shortcut menu) and run **GettingStartedHost.exe** within it.</span></span>

2. <span data-ttu-id="33a15-156">Ouvrez un navigateur web et accédez à la page du service à `http://localhost:8000/GettingStarted/CalculatorService`.</span><span class="sxs-lookup"><span data-stu-id="33a15-156">Open a web browser and browse to the service's page at `http://localhost:8000/GettingStarted/CalculatorService`.</span></span>
   
   > [!NOTE]
   > <span data-ttu-id="33a15-157">Services tels que celui-ci requièrent l’autorisation appropriée pour enregistrer des adresses HTTP sur l’ordinateur pour l’écoute.</span><span class="sxs-lookup"><span data-stu-id="33a15-157">Services such as this one require the proper permission to register HTTP addresses on the machine for listening.</span></span> <span data-ttu-id="33a15-158">Les comptes Administrateur possèdent cette autorisation, mais l'autorisation pour les espaces de noms HTTP doit être accordée aux comptes qui ne sont pas administrateur.</span><span class="sxs-lookup"><span data-stu-id="33a15-158">Administrator accounts have this permission, but non-administrator accounts must be granted permission for HTTP namespaces.</span></span> <span data-ttu-id="33a15-159">Pour plus d’informations sur la configuration des réservations d’espaces de noms, consultez [Configuration de HTTP et HTTPS](feature-details/configuring-http-and-https.md).</span><span class="sxs-lookup"><span data-stu-id="33a15-159">For more information about how to configure namespace reservations, see [Configuring HTTP and HTTPS](feature-details/configuring-http-and-https.md).</span></span> 

## <a name="service-hosting-program-steps"></a><span data-ttu-id="33a15-160">Étapes de programme hébergement de service</span><span class="sxs-lookup"><span data-stu-id="33a15-160">Service hosting program steps</span></span>

<span data-ttu-id="33a15-161">Les étapes dans le code que vous avez ajouté pour héberger le service sont décrits comme suit :</span><span class="sxs-lookup"><span data-stu-id="33a15-161">The steps in the code you added to host the service are described as follows:</span></span>

- <span data-ttu-id="33a15-162">**Étape 1**: Créez une instance de la `Uri` classe destinée à contenir l’adresse de base du service.</span><span class="sxs-lookup"><span data-stu-id="33a15-162">**Step 1**: Create an instance of the `Uri` class to hold the base address of the service.</span></span> <span data-ttu-id="33a15-163">Une URL qui contient une adresse de base a un URI facultatif qui identifie un service.</span><span class="sxs-lookup"><span data-stu-id="33a15-163">A URL that contains a base address has an optional URI that identifies a service.</span></span> <span data-ttu-id="33a15-164">L’adresse de base est formatée comme suit : `<transport>://<machine-name or domain><:optional port #>/<optional URI segment>`.</span><span class="sxs-lookup"><span data-stu-id="33a15-164">The base address is formatted as follows: `<transport>://<machine-name or domain><:optional port #>/<optional URI segment>`.</span></span> <span data-ttu-id="33a15-165">L’adresse de base pour le service de calculatrice utilise le transport HTTP, localhost, port 8000 et le segment d’URI, mise en route.</span><span class="sxs-lookup"><span data-stu-id="33a15-165">The base address for the calculator service uses the HTTP transport, localhost, port 8000, and the URI segment, GettingStarted.</span></span>

- <span data-ttu-id="33a15-166">**Étape 2**: Créez une instance de la <xref:System.ServiceModel.ServiceHost> (classe), qui vous permet d’héberger le service.</span><span class="sxs-lookup"><span data-stu-id="33a15-166">**Step 2**: Create an instance of the <xref:System.ServiceModel.ServiceHost> class, which you use to host the service.</span></span> <span data-ttu-id="33a15-167">Le constructeur accepte deux paramètres : le type de la classe qui implémente le contrat de service et l’adresse de base du service.</span><span class="sxs-lookup"><span data-stu-id="33a15-167">The constructor takes two parameters: the type of the class that implements the service contract and the base address of the service.</span></span>

- <span data-ttu-id="33a15-168">**Étape 3**: Créez une instance <xref:System.ServiceModel.Description.ServiceEndpoint>.</span><span class="sxs-lookup"><span data-stu-id="33a15-168">**Step 3**: Create a <xref:System.ServiceModel.Description.ServiceEndpoint> instance.</span></span> <span data-ttu-id="33a15-169">Un point de terminaison de service est composé d'une adresse, d'une liaison et d'un contrat de service.</span><span class="sxs-lookup"><span data-stu-id="33a15-169">A service endpoint is composed of an address, a binding, and a service contract.</span></span> <span data-ttu-id="33a15-170">Le <xref:System.ServiceModel.Description.ServiceEndpoint> constructeur se compose de type interface de contrat de service, une liaison et une adresse.</span><span class="sxs-lookup"><span data-stu-id="33a15-170">The <xref:System.ServiceModel.Description.ServiceEndpoint> constructor is composed of the service contract interface type, a binding, and an address.</span></span> <span data-ttu-id="33a15-171">Le contrat de service est `ICalculator`, que vous définissez et implémentez dans le type de service.</span><span class="sxs-lookup"><span data-stu-id="33a15-171">The service contract is `ICalculator`, which you defined and implement in the service type.</span></span> <span data-ttu-id="33a15-172">La liaison pour cet exemple est <xref:System.ServiceModel.WSHttpBinding>, qui est une liaison intégrée et se connecte aux points de terminaison qui se conforment à WS-\* spécifications.</span><span class="sxs-lookup"><span data-stu-id="33a15-172">The binding for this sample is <xref:System.ServiceModel.WSHttpBinding>, which is a built-in binding and connects to endpoints that conform to the WS-\* specifications.</span></span> <span data-ttu-id="33a15-173">Pour plus d’informations sur les liaisons WCF, consultez [vue d’ensemble des liaisons WCF](bindings-overview.md).</span><span class="sxs-lookup"><span data-stu-id="33a15-173">For more information about WCF bindings, see [WCF bindings overview](bindings-overview.md).</span></span> <span data-ttu-id="33a15-174">Vous ajoutez l’adresse à l’adresse de base pour identifier le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="33a15-174">You append the address to the base address to identify the endpoint.</span></span> <span data-ttu-id="33a15-175">Le code spécifie l’adresse en tant que CalculatorService et l’adresse complète du point de terminaison en tant que `http://localhost:8000/GettingStarted/CalculatorService`.</span><span class="sxs-lookup"><span data-stu-id="33a15-175">The code specifies the address as CalculatorService and the fully qualified address for the endpoint as `http://localhost:8000/GettingStarted/CalculatorService`.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="33a15-176">Pour .NET Framework Version 4 et versions ultérieures, l’ajout d’un point de terminaison de service est facultative.</span><span class="sxs-lookup"><span data-stu-id="33a15-176">For .NET Framework Version 4 and later, adding a service endpoint is optional.</span></span> <span data-ttu-id="33a15-177">Pour ces versions, si vous n’ajoutez pas votre code ou configuration, WCF ajoute un point de terminaison par défaut pour chaque combinaison d’adresse de base et contrat implémenté par le service.</span><span class="sxs-lookup"><span data-stu-id="33a15-177">For these versions, if you don't add your code or configuration, WCF adds one default endpoint for each combination of base address and contract implemented by the service.</span></span> <span data-ttu-id="33a15-178">Pour plus d’informations sur les points de terminaison par défaut, consultez [spécification d’une adresse de point de terminaison](specifying-an-endpoint-address.md).</span><span class="sxs-lookup"><span data-stu-id="33a15-178">For more information about default endpoints, see [Specifying an endpoint address](specifying-an-endpoint-address.md).</span></span> <span data-ttu-id="33a15-179">Pour plus d’informations sur les points de terminaison par défaut, les liaisons et comportements, consultez [configuration simplifiée](simplified-configuration.md) et [configuration simplifiée pour les services WCF](samples/simplified-configuration-for-wcf-services.md).</span><span class="sxs-lookup"><span data-stu-id="33a15-179">For more information about default endpoints, bindings, and behaviors, see [Simplified configuration](simplified-configuration.md) and [Simplified configuration for WCF services](samples/simplified-configuration-for-wcf-services.md).</span></span>

- <span data-ttu-id="33a15-180">**Étape 4**: Activer l'échange de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="33a15-180">**Step 4**: Enable metadata exchange.</span></span> <span data-ttu-id="33a15-181">Les clients utilisent échange de métadonnées pour générer des proxys pour appeler les opérations de service.</span><span class="sxs-lookup"><span data-stu-id="33a15-181">Clients use metadata exchange to generate proxies for calling the service operations.</span></span> <span data-ttu-id="33a15-182">Pour activer l’échange de métadonnées, créez un <xref:System.ServiceModel.Description.ServiceMetadataBehavior> instance, définissez son <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled> propriété `true`et ajoutez le `ServiceMetadataBehavior` de l’objet à la <xref:System.ServiceModel.Description.ServiceDescription.Behaviors%2A> collection de la <xref:System.ServiceModel.ServiceHost> instance.</span><span class="sxs-lookup"><span data-stu-id="33a15-182">To enable metadata exchange, create a <xref:System.ServiceModel.Description.ServiceMetadataBehavior> instance, set its <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled> property to `true`, and add the `ServiceMetadataBehavior` object to the <xref:System.ServiceModel.Description.ServiceDescription.Behaviors%2A> collection of the <xref:System.ServiceModel.ServiceHost> instance.</span></span>

- <span data-ttu-id="33a15-183">**Étape 5**: Ouvrez <xref:System.ServiceModel.ServiceHost> pour écouter les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="33a15-183">**Step 5**: Open <xref:System.ServiceModel.ServiceHost> to listen for incoming messages.</span></span> <span data-ttu-id="33a15-184">L’application attend que vous appuyiez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="33a15-184">The application waits for you to press **Enter**.</span></span> <span data-ttu-id="33a15-185">Une fois que l’application instancie <xref:System.ServiceModel.ServiceHost>, il exécute un bloc try/catch.</span><span class="sxs-lookup"><span data-stu-id="33a15-185">After the application instantiates <xref:System.ServiceModel.ServiceHost>, it executes a try/catch block.</span></span> <span data-ttu-id="33a15-186">Pour plus d’informations sur l’interception en toute sécurité les exceptions levées par <xref:System.ServiceModel.ServiceHost>, consultez [utilisez fermer et abandon pour libérer les ressources de client WCF](samples/use-close-abort-release-wcf-client-resources.md).</span><span class="sxs-lookup"><span data-stu-id="33a15-186">For more information about safely catching exceptions thrown by <xref:System.ServiceModel.ServiceHost>, see [Use Close and Abort to release WCF client resources](samples/use-close-abort-release-wcf-client-resources.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33a15-187">Lorsque vous ajoutez une bibliothèque de service WCF, Visual Studio héberge il pour vous si vous le déboguez en démarrant un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="33a15-187">When you add a WCF service library, Visual Studio hosts it for you if you debug it by starting a service host.</span></span> <span data-ttu-id="33a15-188">Pour éviter les conflits, vous pouvez empêcher Visual Studio à partir de l’hébergement de la bibliothèque de service WCF.</span><span class="sxs-lookup"><span data-stu-id="33a15-188">To avoid conflicts, you can prevent Visual Studio from hosting the WCF service library.</span></span> 
> 1. <span data-ttu-id="33a15-189">Sélectionnez le **GettingStartedLib** projet **l’Explorateur de solutions** et choisissez **propriétés** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="33a15-189">Select the **GettingStartedLib** project in **Solution Explorer** and choose **Properties** from the shortcut menu.</span></span>
> 2. <span data-ttu-id="33a15-190">Sélectionnez **Options WCF** et décochez la case **démarrer WCF Service hôte lors du débogage d’un autre projet dans la même solution**.</span><span class="sxs-lookup"><span data-stu-id="33a15-190">Select **WCF Options** and uncheck **Start WCF Service Host when debugging another project in the same solution**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="33a15-191">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="33a15-191">Next steps</span></span>

<span data-ttu-id="33a15-192">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="33a15-192">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> - <span data-ttu-id="33a15-193">Créez et configurez un projet d’application console pour l’hébergement d’un service WCF.</span><span class="sxs-lookup"><span data-stu-id="33a15-193">Create and configure a console app project for hosting a WCF service.</span></span>
> - <span data-ttu-id="33a15-194">Ajoutez le code pour héberger le service WCF.</span><span class="sxs-lookup"><span data-stu-id="33a15-194">Add code to host the WCF service.</span></span>
> - <span data-ttu-id="33a15-195">Mettre à jour le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="33a15-195">Update the configuration file.</span></span>
> - <span data-ttu-id="33a15-196">Démarrer le service WCF et vérifier qu’il est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="33a15-196">Start the WCF service and verify it's running.</span></span>

<span data-ttu-id="33a15-197">Passez au didacticiel suivant pour apprendre à créer un client WCF.</span><span class="sxs-lookup"><span data-stu-id="33a15-197">Advance to the next tutorial to learn how to create a WCF client.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="33a15-198">Tutoriel : Créer un client WCF</span><span class="sxs-lookup"><span data-stu-id="33a15-198">Tutorial: Create a WCF client</span></span>](how-to-create-a-wcf-client.md)
