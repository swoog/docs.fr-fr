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
ms.openlocfilehash: 38fd9b89e2719be8ce4d33b1b50f68171d587369
ms.sourcegitcommit: 3630c2515809e6f4b7dbb697a3354efec105a5cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2019
ms.locfileid: "58410093"
---
# <a name="tutorial-host-and-run-a-basic-windows-communication-foundation-service"></a>Tutoriel : Héberger et exécuter un service Windows Communication Foundation de base

Ce didacticiel décrit la troisième des cinq tâches requises pour créer une application Windows Communication Foundation (WCF) de base. Pour une vue d’ensemble des didacticiels, consultez [didacticiel : Prise en main les applications Windows Communication Foundation](getting-started-tutorial.md).

La tâche suivante pour créer une application WCF consiste à héberger un service WCF dans une application console. Un service WCF expose un ou plusieurs *points de terminaison*, chacun d'entre eux exposant une ou plusieurs opérations de service. Un point de terminaison de service spécifie les informations suivantes : 
- Une adresse où vous pouvez trouver le service.
- Une liaison qui contient les informations qui décrivent comment un client doit communiquer avec le service. 
- Un contrat qui définit les fonctionnalités fournies par le service à ses clients.

Dans ce didacticiel, vous apprendrez à :
> [!div class="checklist"]
> - Créez et configurez un projet d’application console pour l’hébergement d’un service WCF.
> - Ajoutez le code pour héberger le service WCF.
> - Mettre à jour le fichier de configuration.
> - Démarrer le service WCF et vérifier qu’il est en cours d’exécution.


## <a name="create-and-configure-a-console-app-project-for-hosting-the-service"></a>Créer et configurer un projet d’application console pour héberger le service

1. Créer un projet d’application console dans Visual Studio : 
 
    1. À partir de la **fichier** menu, sélectionnez **Open** > **projet/Solution** et accédez à la **GettingStarted** solution vous créé précédemment (*GettingStarted.sln*). Sélectionnez **Ouvrir**.

    2. À partir de la **vue** menu, sélectionnez **l’Explorateur de solutions**.
    
    3. Dans le **l’Explorateur de solutions** fenêtre, sélectionnez le **GettingStarted** solution (nœud supérieur) et sélectionnez **ajouter** > **denouveauprojet** dans le menu contextuel. 

    4. Dans le **ajouter un nouveau projet** fenêtre, sur le côté gauche, sélectionnez le **Windows Desktop** catégorie sous **Visual C#**  ou **Visual Basic**. 

    5. Sélectionnez le **application Console (.NET Framework)** modèle, puis entrez *GettingStartedHost* pour le **nom**. Sélectionnez **OK**.

2. Ajouter une référence dans le **GettingStartedHost** de projet pour le **GettingStartedLib** projet : 

    1. Dans le **l’Explorateur de solutions** fenêtre, sélectionnez le **références** dossier sous le **GettingStartedHost** de projet, puis sélectionnez **ajouter une référence** dans le menu contextuel. 

    2. Dans le **ajouter une référence** boîte de dialogue, sous **projets** sur le côté gauche de la fenêtre, sélectionnez **Solution**. 
 
    3. Sélectionnez **GettingStartedLib** dans la section centrale de la fenêtre, puis sélectionnez **OK**. 

       Cette action rend les types définis dans le **GettingStartedLib** projet disponible à la **GettingStartedHost** projet.

3. Ajouter une référence dans le **GettingStartedHost** de projet pour le <xref:System.ServiceModel> assembly : 

    1. Dans le **l’Explorateur de solutions** fenêtre, sélectionnez le **références** dossier sous le **GettingStartedHost** de projet, puis sélectionnez **ajouter une référence** dans le menu contextuel.
    
    2. Dans le **ajouter une référence** fenêtre, sous **assemblys** sur le côté gauche de la fenêtre, sélectionnez **Framework**. 

    3. Sélectionnez **System.ServiceModel**, puis sélectionnez **OK**. 
    
    4. Enregistrez la solution en sélectionnant **fichier** > **Enregistrer tout**.

## <a name="add-code-to-host-the-service"></a>Ajoutez le code pour héberger le service

Pour héberger le service, vous ajoutez le code pour effectuer les étapes suivantes : 
   1. Créer un URI pour l’adresse de base.
   2. Créer une instance de classe pour héberger le service.
   3. Créer un point de terminaison de service.
   4. Activer l'échange de métadonnées.
   5. Ouvrez l’hôte de service pour écouter les messages entrants.
  
Apportez les modifications suivantes au code :

1. Ouvrez le **Program.cs** ou **Module1.vb** de fichiers dans le **GettingStartedHost** de projet et remplacez son code par le code suivant :

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
    
    Pour plus d’informations sur le fonctionne de ce code, consultez [Service étapes du programme d’hébergement](#service-hosting-program-steps).


2. Mettre à jour les propriétés du projet :

   1. Dans le **l’Explorateur de solutions** fenêtre, sélectionnez le **GettingStartedHost** dossier, puis sélectionnez **propriétés** dans le menu contextuel.

   2. Sur le **GettingStartedHost** page de propriétés, sélectionnez le **Application** onglet :

      - Pour C# projets, sélectionnez **GettingStartedHost.Program** à partir de la **objet de démarrage** liste.

      - Pour les projets Visual Basic, sélectionnez **Service.Program** à partir de la **objet de démarrage** liste.

   3. À partir de la **fichier** menu, sélectionnez **Enregistrer tout**.


## <a name="verify-the-service-is-working"></a>Vérifiez que le service fonctionne

1. Générez la solution, puis exécutez le **GettingStartedHost** console application à partir de Visual Studio. 

    Le service doit être exécuté avec des privilèges d’administrateur. Étant donné que vous avez ouvert Visual Studio avec des privilèges d’administrateur, lorsque vous exécutez **GettingStartedHost** dans Visual Studio, l’application est exécutée avec des privilèges d’administrateur. Comme alternative, vous pouvez ouvrir une nouvelle invite de commandes en tant qu’administrateur (sélectionnez **plus** > **exécuter en tant qu’administrateur** dans le menu contextuel) et exécutez **GettingStartedHost.exe**  qu’il contient.

2. Ouvrez un navigateur web et accédez à la page du service à `http://localhost:8000/GettingStarted/CalculatorService`.
   
   > [!NOTE]
   > Services tels que celui-ci requièrent l’autorisation appropriée pour enregistrer des adresses HTTP sur l’ordinateur pour l’écoute. Les comptes Administrateur possèdent cette autorisation, mais l'autorisation pour les espaces de noms HTTP doit être accordée aux comptes qui ne sont pas administrateur. Pour plus d’informations sur la configuration des réservations d’espaces de noms, consultez [Configuration de HTTP et HTTPS](feature-details/configuring-http-and-https.md). 


## <a name="service-hosting-program-steps"></a>Étapes de programme hébergement de service

Les étapes dans le code que vous avez ajouté pour héberger le service sont décrits comme suit :

- **Étape 1**: Créez une instance de la `Uri` classe destinée à contenir l’adresse de base du service. Une URL qui contient une adresse de base a un URI facultatif qui identifie un service. L’adresse de base est formatée comme suit : `<transport>://<machine-name or domain><:optional port #>/<optional URI segment>`. L’adresse de base pour le service de calculatrice utilise le transport HTTP, localhost, port 8000 et le segment d’URI, mise en route.

- **Étape 2**: Créez une instance de la <xref:System.ServiceModel.ServiceHost> (classe), qui vous permet d’héberger le service. Le constructeur accepte deux paramètres : le type de la classe qui implémente le contrat de service et l’adresse de base du service.

- **Étape 3**: Créez une instance <xref:System.ServiceModel.Description.ServiceEndpoint>. Un point de terminaison de service est composé d'une adresse, d'une liaison et d'un contrat de service. Le <xref:System.ServiceModel.Description.ServiceEndpoint> constructeur se compose de type interface de contrat de service, une liaison et une adresse. Le contrat de service est `ICalculator`, que vous définissez et implémentez dans le type de service. La liaison pour cet exemple est <xref:System.ServiceModel.WSHttpBinding>, qui est une liaison intégrée et se connecte aux points de terminaison qui se conforment à WS-* spécifications. Pour plus d’informations sur les liaisons WCF, consultez [vue d’ensemble des liaisons WCF](bindings-overview.md). Vous ajoutez l’adresse à l’adresse de base pour identifier le point de terminaison. Le code spécifie l’adresse en tant que CalculatorService et l’adresse complète du point de terminaison en tant que `http://localhost:8000/GettingStarted/CalculatorService`.

    > [!IMPORTANT]
    > Pour .NET Framework Version 4 et versions ultérieures, l’ajout d’un point de terminaison de service est facultative. Pour ces versions, si vous n’ajoutez pas votre code ou configuration, WCF ajoute un point de terminaison par défaut pour chaque combinaison d’adresse de base et contrat implémenté par le service. Pour plus d’informations sur les points de terminaison par défaut, consultez [spécification d’une adresse de point de terminaison](specifying-an-endpoint-address.md). Pour plus d’informations sur les points de terminaison par défaut, les liaisons et comportements, consultez [configuration simplifiée](simplified-configuration.md) et [configuration simplifiée pour les services WCF](samples/simplified-configuration-for-wcf-services.md).

- **Étape 4**: Activer l'échange de métadonnées. Les clients utilisent échange de métadonnées pour générer des proxys pour appeler les opérations de service. Pour activer l’échange de métadonnées, créez un <xref:System.ServiceModel.Description.ServiceMetadataBehavior> instance, définissez son <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled> propriété `true`et ajoutez le `ServiceMetadataBehavior` de l’objet à la <xref:System.ServiceModel.Description.ServiceDescription.Behaviors%2A> collection de la <xref:System.ServiceModel.ServiceHost> instance.

- **Étape 5**: Ouvrez <xref:System.ServiceModel.ServiceHost> pour écouter les messages entrants. L’application attend que vous appuyiez sur **entrée**. Une fois que l’application instancie <xref:System.ServiceModel.ServiceHost>, il exécute un bloc try/catch. Pour plus d’informations sur l’interception en toute sécurité les exceptions levées par <xref:System.ServiceModel.ServiceHost>, consultez [utilisez fermer et abandon pour libérer les ressources de client WCF](samples/use-close-abort-release-wcf-client-resources.md).

> [!IMPORTANT]
> Lorsque vous ajoutez une bibliothèque de service WCF, Visual Studio héberge il pour vous si vous le déboguez en démarrant un hôte de service. Pour éviter les conflits, vous pouvez empêcher Visual Studio à partir de l’hébergement de la bibliothèque de service WCF. 
> 1. Sélectionnez le **GettingStartedLib** projet **l’Explorateur de solutions** et choisissez **propriétés** dans le menu contextuel.
> 2. Sélectionnez **Options WCF** et décochez la case **démarrer WCF Service hôte lors du débogage d’un autre projet dans la même solution**.


## <a name="next-steps"></a>Étapes suivantes

Dans ce didacticiel, vous avez appris à :
> [!div class="checklist"]
> - Créez et configurez un projet d’application console pour l’hébergement d’un service WCF.
> - Ajoutez le code pour héberger le service WCF.
> - Mettre à jour le fichier de configuration.
> - Démarrer le service WCF et vérifier qu’il est en cours d’exécution.

Passez au didacticiel suivant pour apprendre à créer un client WCF.

> [!div class="nextstepaction"]
> [Tutoriel : Créer un client WCF](how-to-create-a-wcf-client.md)
