---
title: Création de l'application cliente .NET Framework (démarrage rapide des services de données WCF)
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 41ade767-eeab-437d-9121-9797e8fb8045
ms.openlocfilehash: 86ded7351d435b3a7077f0354d8a923b33a3f2b6
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44216501"
---
# <a name="creating-the-net-framework-client-application-wcf-data-services-quickstart"></a><span data-ttu-id="188e4-102">Création de l'application cliente .NET Framework (démarrage rapide des services de données WCF)</span><span class="sxs-lookup"><span data-stu-id="188e4-102">Creating the .NET Framework Client Application (WCF Data Services Quickstart)</span></span>

<span data-ttu-id="188e4-103">Il s’agit de la dernière tâche du démarrage rapide WCF Data Services.</span><span class="sxs-lookup"><span data-stu-id="188e4-103">This is the final task of the WCF Data Services quickstart.</span></span> <span data-ttu-id="188e4-104">Dans cette tâche, vous ajoutez une application console à la solution, ajoutez une référence à la [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] alimenter cette nouvelle application cliente et accéder au flux à partir de l’application cliente en utilisant les classes de service de données client générées et les bibliothèques clientes OData .</span><span class="sxs-lookup"><span data-stu-id="188e4-104">In this task, you will add a console application to the solution, add a reference to the [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] feed into this new client application, and access the OData feed from the client application by using the generated client data service classes and client libraries.</span></span>

> [!NOTE]
> <span data-ttu-id="188e4-105">Il n'est pas obligatoire pour une application cliente .NET Framework d'accéder à un flux de données.</span><span class="sxs-lookup"><span data-stu-id="188e4-105">A .NET Framework-based client application is not required to access a data feed.</span></span> <span data-ttu-id="188e4-106">Le service de données est accessible par n’importe quel composant d’application qui consomme un flux OData.</span><span class="sxs-lookup"><span data-stu-id="188e4-106">The data service can be accessed by any application component that consumes an OData feed.</span></span> <span data-ttu-id="188e4-107">Pour plus d’informations, consultez [à l’aide d’un Service de données dans une Application cliente](../../../../docs/framework/data/wcf/using-a-data-service-in-a-client-application-wcf-data-services.md).</span><span class="sxs-lookup"><span data-stu-id="188e4-107">For more information, see [Using a Data Service in a Client Application](../../../../docs/framework/data/wcf/using-a-data-service-in-a-client-application-wcf-data-services.md).</span></span>

## <a name="to-create-the-client-application-by-using-visual-studio"></a><span data-ttu-id="188e4-108">Pour créer l'application cliente à l'aide de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="188e4-108">To create the client application by using Visual Studio</span></span>

1.  <span data-ttu-id="188e4-109">Dans **l’Explorateur de solutions**, avec le bouton droit de la solution, cliquez sur **ajouter**, puis cliquez sur **nouveau projet**.</span><span class="sxs-lookup"><span data-stu-id="188e4-109">In **Solution Explorer**, right-click the solution, click **Add**, and then click **New Project**.</span></span>

2.  <span data-ttu-id="188e4-110">Dans le volet gauche, sélectionnez **installé** > [**Visual C#** ou **Visual Basic**] > **Windows Desktop**, puis sélectionnez le **Application WPF** modèle.</span><span class="sxs-lookup"><span data-stu-id="188e4-110">In the left pane, select **Installed** > [**Visual C#** or **Visual Basic**] > **Windows Desktop**, and then select the **WPF App** template.</span></span>

3.  <span data-ttu-id="188e4-111">Entrez `NorthwindClient` pour le nom du projet, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="188e4-111">Enter `NorthwindClient` for the project name, and then click **OK**.</span></span>

4.  <span data-ttu-id="188e4-112">Ouvrez le fichier MainWindow.xaml et remplacez le code XAML par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="188e4-112">Open the file MainWindow.xaml and replace the XAML code with the following code:</span></span>

     [!code-xaml[Astoria Quickstart Client#Window1Xaml](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria quickstart client/vb/window1.xaml#window1xaml)]

## <a name="to-add-a-data-service-reference-to-the-project"></a><span data-ttu-id="188e4-113">Pour ajouter une référence de service de données au projet</span><span class="sxs-lookup"><span data-stu-id="188e4-113">To add a data service reference to the project</span></span>

1.  <span data-ttu-id="188e4-114">Dans **l’Explorateur de solutions**, cliquez sur le projet NorthwindClient, cliquez sur **ajouter** > **une référence de Service**, puis cliquez sur **Discover** .</span><span class="sxs-lookup"><span data-stu-id="188e4-114">In **Solution Explorer**, right-click the NorthwindClient project, click **Add** > **Service Reference**, and then click **Discover**.</span></span>

     <span data-ttu-id="188e4-115">Cette opération affiche le service de données Northwind que vous avez créé dans la première tâche.</span><span class="sxs-lookup"><span data-stu-id="188e4-115">This displays the Northwind data service that you created in the first task.</span></span>

2.  <span data-ttu-id="188e4-116">Dans le **Namespace** zone de texte, tapez `Northwind`, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="188e4-116">In the **Namespace** text box, type `Northwind`, and then click **OK**.</span></span>

     <span data-ttu-id="188e4-117">Cette opération ajoute un nouveau fichier de code au projet qui contient les classes de données utilisées pour accéder et interagir avec les ressources du service de données sous la forme d'objets.</span><span class="sxs-lookup"><span data-stu-id="188e4-117">This adds a new code file to the project, which contains the data classes that are used to access and interact with data service resources as objects.</span></span> <span data-ttu-id="188e4-118">Les classes de données sont créées dans l'espace de noms `NorthwindClient.Northwind`.</span><span class="sxs-lookup"><span data-stu-id="188e4-118">The data classes are created in the namespace `NorthwindClient.Northwind`.</span></span>

## <a name="to-access-data-service-data-in-the-wpf-application"></a><span data-ttu-id="188e4-119">Pour accéder aux données du service des données dans l'application WPF</span><span class="sxs-lookup"><span data-stu-id="188e4-119">To access data service data in the WPF application</span></span>

1.  <span data-ttu-id="188e4-120">Dans **l’Explorateur de solutions** sous **NorthwindClient**, cliquez sur le projet, puis cliquez sur **ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="188e4-120">In **Solution Explorer** under **NorthwindClient**, right-click the project and click **Add Reference**.</span></span>

2.  <span data-ttu-id="188e4-121">Dans le **ajouter une référence** boîte de dialogue, cliquez sur le **.NET** onglet, sélectionnez l’assembly System.Data.Services.Client.dll, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="188e4-121">In the **Add Reference** dialog box, click the **.NET** tab, select the System.Data.Services.Client.dll assembly, and then click **OK**.</span></span>

3. <span data-ttu-id="188e4-122">Dans **l’Explorateur de solutions** sous **NorthwindClient**, ouvrez la page de codes pour le fichier MainWindow.xaml et ajoutez le code suivant `using` instruction (`Imports` en Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="188e4-122">In **Solution Explorer** under **NorthwindClient**, open the code page for the MainWindow.xaml file, and add the following `using` statement (`Imports` in Visual Basic).</span></span>

     [!code-csharp[Astoria Quickstart Client#Using](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria quickstart client/cs/window1.xaml.cs#using)]
     [!code-vb[Astoria Quickstart Client#Using](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria quickstart client/vb/window1.xaml.vb#using)]

3.  <span data-ttu-id="188e4-123">Insérez le code suivant qui interroge le service de données et lie le résultat à une <xref:System.Data.Services.Client.DataServiceCollection%601> dans la classe `MainWindow`:</span><span class="sxs-lookup"><span data-stu-id="188e4-123">Insert the following code that queries that data service and binds the result to a <xref:System.Data.Services.Client.DataServiceCollection%601> into the `MainWindow` class:</span></span>

    > [!NOTE]
    > <span data-ttu-id="188e4-124">Vous devez remplacer le nom d'hôte `localhost:12345` par le serveur et le port qui hébergent votre instance du service de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="188e4-124">You must replace the host name `localhost:12345` with the server and port that is hosting your instance of the Northwind data service.</span></span>

     [!code-csharp[Astoria Quickstart Client#QueryCode](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria quickstart client/cs/window1.xaml.cs#querycode)]
     [!code-vb[Astoria Quickstart Client#QueryCode](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria quickstart client/vb/window1.xaml.vb#querycode)]

4.  <span data-ttu-id="188e4-125">Insérez le code suivant qui enregistre les modifications dans la classe `MainWindow` :</span><span class="sxs-lookup"><span data-stu-id="188e4-125">Insert the following code that saves changes into the `MainWindow` class:</span></span>

     [!code-csharp[Astoria Quickstart Client#SaveChanges](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria quickstart client/cs/window1.xaml.cs#savechanges)]
     [!code-vb[Astoria Quickstart Client#SaveChanges](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria quickstart client/vb/window1.xaml.vb#savechanges)]

## <a name="to-build-and-run-the-northwindclient-application"></a><span data-ttu-id="188e4-126">Pour générer et exécuter l'application NothwindClient</span><span class="sxs-lookup"><span data-stu-id="188e4-126">To build and run the NorthwindClient application</span></span>

1.  <span data-ttu-id="188e4-127">Dans **l’Explorateur de solutions**, cliquez sur le projet NorthwindClient et sélectionnez **définir comme projet de démarrage**.</span><span class="sxs-lookup"><span data-stu-id="188e4-127">In **Solution Explorer**, right-click the NorthwindClient project and select **Set as startup project**.</span></span>

2.  <span data-ttu-id="188e4-128">Appuyez sur **F5** pour démarrer l’application.</span><span class="sxs-lookup"><span data-stu-id="188e4-128">Press **F5** to start the application.</span></span>

     <span data-ttu-id="188e4-129">Cette opération génère et démarre l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="188e4-129">This builds the solution and starts the client application.</span></span> <span data-ttu-id="188e4-130">Les données sont demandées auprès du service et s'affichent dans la console.</span><span class="sxs-lookup"><span data-stu-id="188e4-130">Data is requested from the service and displayed in the console.</span></span>

3.  <span data-ttu-id="188e4-131">Modifier une valeur dans le **quantité** colonne de la grille de données, puis cliquez sur **enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="188e4-131">Edit a value in the **Quantity** column of the data grid, and then click **Save**.</span></span>

     <span data-ttu-id="188e4-132">Les modifications sont enregistrées sur le service de données.</span><span class="sxs-lookup"><span data-stu-id="188e4-132">Changes are saved to the data service.</span></span>

    > [!NOTE]
    > <span data-ttu-id="188e4-133">Cette version de l'application NorthwindClient ne prend pas en charge l'ajout et la suppression d'entités.</span><span class="sxs-lookup"><span data-stu-id="188e4-133">This version of the NorthwindClient application does not support adding and deleting of entities.</span></span>

## <a name="next-steps"></a><span data-ttu-id="188e4-134">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="188e4-134">Next Steps</span></span>

<span data-ttu-id="188e4-135">Vous avez créé avec succès l’application cliente qui accède à l’exemple de que flux OData de Northwind.</span><span class="sxs-lookup"><span data-stu-id="188e4-135">You have successfully created the client application that accesses the sample Northwind OData feed.</span></span> <span data-ttu-id="188e4-136">Vous avez également terminé le démarrage rapide WCF Data Services.</span><span class="sxs-lookup"><span data-stu-id="188e4-136">You've also completed the WCF Data Services quickstart!</span></span>

<span data-ttu-id="188e4-137">Pour plus d’informations sur l’accès à un OData flux à partir d’un [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] application, consultez [bibliothèque de Client WCF Data Services](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md).</span><span class="sxs-lookup"><span data-stu-id="188e4-137">For more information about accessing an OData feed from a [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] application, see [WCF Data Services Client Library](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="188e4-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="188e4-138">See Also</span></span>

- [<span data-ttu-id="188e4-139">Prise en main</span><span class="sxs-lookup"><span data-stu-id="188e4-139">Getting Started</span></span>](../../../../docs/framework/data/wcf/getting-started-with-wcf-data-services.md)
- [<span data-ttu-id="188e4-140">Ressources</span><span class="sxs-lookup"><span data-stu-id="188e4-140">Resources</span></span>](../../../../docs/framework/data/wcf/wcf-data-services-resources.md)
