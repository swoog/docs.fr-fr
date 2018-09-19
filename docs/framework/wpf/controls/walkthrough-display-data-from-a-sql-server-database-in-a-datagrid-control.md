---
title: "Procédure pas à pas : affichage de données d'une base de données SQL Server dans un contrôle DataGrid"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGrid [WPF], displaying data from SQL Server
- controls [WPF], DataGrid
ms.assetid: 6810b048-0a23-4f86-bfa5-97f92b3cfab4
ms.openlocfilehash: dba2ec98b25c9c65a795c462b18504a799df04bc
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "45972265"
---
# <a name="walkthrough-display-data-from-a-sql-server-database-in-a-datagrid-control"></a><span data-ttu-id="ecf87-102">Procédure pas à pas : affichage de données d'une base de données SQL Server dans un contrôle DataGrid</span><span class="sxs-lookup"><span data-stu-id="ecf87-102">Walkthrough: Display Data from a SQL Server Database in a DataGrid Control</span></span>
<span data-ttu-id="ecf87-103">Dans cette procédure pas à pas, vous récupérer des données à partir d’une base de données SQL Server et afficher ces données dans un <xref:System.Windows.Controls.DataGrid> contrôle.</span><span class="sxs-lookup"><span data-stu-id="ecf87-103">In this walkthrough, you retrieve data from a SQL Server database and display that data in a <xref:System.Windows.Controls.DataGrid> control.</span></span> <span data-ttu-id="ecf87-104">ADO.NET Entity Framework vous permet de créer les classes d’entité qui représentent les données et utilisent LINQ pour écrire une requête qui Récupère les données spécifiées à partir d’une classe d’entité.</span><span class="sxs-lookup"><span data-stu-id="ecf87-104">You use the ADO.NET Entity Framework to create the entity classes that represent the data, and use LINQ to write a query that retrieves the specified data from an entity class.</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="ecf87-105">Prérequis</span><span class="sxs-lookup"><span data-stu-id="ecf87-105">Prerequisites</span></span>  
 <span data-ttu-id="ecf87-106">Pour exécuter cette procédure pas à pas, vous devez disposer des composants suivants :</span><span class="sxs-lookup"><span data-stu-id="ecf87-106">You need the following components to complete this walkthrough:</span></span>  
  
-   [!INCLUDE[vs_dev11_long](../../../../includes/vs-dev11-long-md.md)]<span data-ttu-id="ecf87-107">.</span><span class="sxs-lookup"><span data-stu-id="ecf87-107">.</span></span>  
  
-   <span data-ttu-id="ecf87-108">Accès à une instance en cours d’exécution de SQL Server ou SQL Server Express qui a la base de données AdventureWorks attachée.</span><span class="sxs-lookup"><span data-stu-id="ecf87-108">Access to a running instance of SQL Server or SQL Server Express that has the AdventureWorks sample database attached to it.</span></span> <span data-ttu-id="ecf87-109">Vous pouvez télécharger la base de données AdventureWorks à partir de la [GitHub](https://github.com/Microsoft/sql-server-samples/releases).</span><span class="sxs-lookup"><span data-stu-id="ecf87-109">You can download the AdventureWorks database from the [GitHub](https://github.com/Microsoft/sql-server-samples/releases).</span></span>  
  
### <a name="to-create-entity-classes"></a><span data-ttu-id="ecf87-110">Pour créer des classes d’entité</span><span class="sxs-lookup"><span data-stu-id="ecf87-110">To create entity classes</span></span>  
  
1.  <span data-ttu-id="ecf87-111">Créez un nouveau projet d’Application WPF en Visual Basic ou c# et nommez-le `DataGridSQLExample`.</span><span class="sxs-lookup"><span data-stu-id="ecf87-111">Create a new WPF Application project in Visual Basic or C#, and name it `DataGridSQLExample`.</span></span>  
  
2.  <span data-ttu-id="ecf87-112">Dans l’Explorateur de solutions, cliquez sur votre projet, pointez sur **ajouter**, puis sélectionnez **un nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="ecf87-112">In Solution Explorer, right-click your project, point to **Add**, and then select **New Item**.</span></span>  
  
     <span data-ttu-id="ecf87-113">La boîte de dialogue Ajouter un nouvel élément s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ecf87-113">The Add New Item dialog box appears.</span></span>  
  
3.  <span data-ttu-id="ecf87-114">Dans le volet Modèles installés, sélectionnez **données** et dans la liste des modèles, sélectionnez **ADO.NET Entity Data Model**.</span><span class="sxs-lookup"><span data-stu-id="ecf87-114">In the Installed Templates pane, select **Data** and in the list of templates, select **ADO.NET Entity Data Model**.</span></span>  
  
     <span data-ttu-id="ecf87-115">![Sélectionnez ADO.NET Entity Data Model](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step1.png "DataGrid_SQL_EF_Step1")</span><span class="sxs-lookup"><span data-stu-id="ecf87-115">![Select ADO.NET Entity Data Model](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step1.png "DataGrid_SQL_EF_Step1")</span></span>  
  
4.  <span data-ttu-id="ecf87-116">Nommez le fichier `AdventureWorksModel.edmx` puis cliquez sur **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ecf87-116">Name the file `AdventureWorksModel.edmx` and then click **Add**.</span></span>  
  
     <span data-ttu-id="ecf87-117">L'Assistant Entity Data Model s'affiche.</span><span class="sxs-lookup"><span data-stu-id="ecf87-117">The Entity Data Model Wizard appears.</span></span>  
  
5.  <span data-ttu-id="ecf87-118">Dans l’écran Choisir le contenu du modèle, sélectionnez **générer à partir de la base de données** puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ecf87-118">In the Choose Model Contents screen, select **Generate from database** and then click **Next**.</span></span>  
  
     <span data-ttu-id="ecf87-119">![Sélectionnez générer à partir de l’option de base de données](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step2.png "DataGrid_SQL_EF_Step2")</span><span class="sxs-lookup"><span data-stu-id="ecf87-119">![Select Generate from database option](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step2.png "DataGrid_SQL_EF_Step2")</span></span>  
  
6.  <span data-ttu-id="ecf87-120">Dans l’écran Choisir votre connexion de données, fournissez la connexion à votre base de données AdventureWorksLT2008.</span><span class="sxs-lookup"><span data-stu-id="ecf87-120">In the Choose Your Data Connection screen, provide the connection to your AdventureWorksLT2008 database.</span></span> <span data-ttu-id="ecf87-121">Pour plus d’informations, consultez [boîte de dialogue Choisir votre connexion de données](https://go.microsoft.com/fwlink/?LinkId=160190).</span><span class="sxs-lookup"><span data-stu-id="ecf87-121">For more information, see [Choose Your Data Connection Dialog Box](https://go.microsoft.com/fwlink/?LinkId=160190).</span></span>  
  
     <span data-ttu-id="ecf87-122">![Fournir la connexion à la base de données](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step3.png "DataGrid_SQL_EF_Step3")</span><span class="sxs-lookup"><span data-stu-id="ecf87-122">![Provide connection to database](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step3.png "DataGrid_SQL_EF_Step3")</span></span>  
  
7.  <span data-ttu-id="ecf87-123">Assurez-vous que le nom est `AdventureWorksLT2008Entities` et que le **enregistrer des paramètres de connexion entity dans App.Config en tant que** case à cocher est sélectionnée, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ecf87-123">Make sure that the name is `AdventureWorksLT2008Entities` and that the **Save entity connection settings in App.Config as** check box is selected, and then click **Next**.</span></span>  
  
8.  <span data-ttu-id="ecf87-124">Dans l’écran Choisir vos objets de base de données, développez le nœud Tables, puis sélectionnez le **produit** et **ProductCategory** tables.</span><span class="sxs-lookup"><span data-stu-id="ecf87-124">In the Choose Your Database Objects screen, expand the Tables node, and select the **Product** and **ProductCategory** tables.</span></span>  
  
     <span data-ttu-id="ecf87-125">Vous pouvez générer des classes d’entités pour toutes les tables ; Toutefois, dans cet exemple vous uniquement récupérer des données à partir de ces deux tables.</span><span class="sxs-lookup"><span data-stu-id="ecf87-125">You can generate entity classes for all of the tables; however, in this example you only retrieve data from those two tables.</span></span>  
  
     <span data-ttu-id="ecf87-126">![Sélectionner Product et ProductCategory à partir des tables](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step4.png "DataGrid_SQL_EF_Step4")</span><span class="sxs-lookup"><span data-stu-id="ecf87-126">![Select Product and ProductCategory from tables](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step4.png "DataGrid_SQL_EF_Step4")</span></span>  
  
9. <span data-ttu-id="ecf87-127">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="ecf87-127">Click **Finish**.</span></span>  
  
     <span data-ttu-id="ecf87-128">Les entités Product et ProductCategory sont affichées dans le Concepteur d’entités.</span><span class="sxs-lookup"><span data-stu-id="ecf87-128">The Product and ProductCategory entities are displayed in the Entity Designer.</span></span>  
  
     <span data-ttu-id="ecf87-129">![Modèles d’entité Product et ProductCategory](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step5.png "DataGrid_SQL_EF_Step5")</span><span class="sxs-lookup"><span data-stu-id="ecf87-129">![Product and ProductCategory entity models](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step5.png "DataGrid_SQL_EF_Step5")</span></span>  
  
### <a name="to-retrieve-and-present-the-data"></a><span data-ttu-id="ecf87-130">Pour récupérer et de présenter les données</span><span class="sxs-lookup"><span data-stu-id="ecf87-130">To retrieve and present the data</span></span>  
  
1.  <span data-ttu-id="ecf87-131">Ouvrez le fichier MainWindow.xaml.</span><span class="sxs-lookup"><span data-stu-id="ecf87-131">Open the MainWindow.xaml file.</span></span>  
  
2.  <span data-ttu-id="ecf87-132">Définir le <xref:System.Windows.FrameworkElement.Width%2A> propriété sur le <xref:System.Windows.Window> à 450.</span><span class="sxs-lookup"><span data-stu-id="ecf87-132">Set the <xref:System.Windows.FrameworkElement.Width%2A> property on the <xref:System.Windows.Window> to 450.</span></span>  
  
3.  <span data-ttu-id="ecf87-133">Dans l’éditeur XAML, ajoutez le code suivant <xref:System.Windows.Controls.DataGrid> balise entre les `<Grid>` et `</Grid>` balises pour ajouter un <xref:System.Windows.Controls.DataGrid> nommé `dataGrid1`.</span><span class="sxs-lookup"><span data-stu-id="ecf87-133">In the XAML editor, add the following <xref:System.Windows.Controls.DataGrid> tag between the `<Grid>` and `</Grid>` tags to add a <xref:System.Windows.Controls.DataGrid> named `dataGrid1`.</span></span>  
  
     [!code-xaml[DataGrid_SQL_EF_Walkthrough#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_SQL_EF_Walkthrough/CS/MainWindow.xaml#3)]  
  
     <span data-ttu-id="ecf87-134">![Fenêtre avec DataGrid](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step6.png "DataGrid_SQL_EF_Step6")</span><span class="sxs-lookup"><span data-stu-id="ecf87-134">![Window with DataGrid](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step6.png "DataGrid_SQL_EF_Step6")</span></span>  
  
4.  <span data-ttu-id="ecf87-135">Sélectionnez le contrôle <xref:System.Windows.Window>.</span><span class="sxs-lookup"><span data-stu-id="ecf87-135">Select the <xref:System.Windows.Window>.</span></span>  
  
5.  <span data-ttu-id="ecf87-136">À l’aide de la fenêtre Propriétés ou l’éditeur XAML, créez un gestionnaire d’événements pour le <xref:System.Windows.Window> nommé `Window_Loaded` pour le <xref:System.Windows.FrameworkElement.Loaded> événement.</span><span class="sxs-lookup"><span data-stu-id="ecf87-136">Using the Properties window or XAML editor, create an event handler for the <xref:System.Windows.Window> named `Window_Loaded` for the <xref:System.Windows.FrameworkElement.Loaded> event.</span></span> <span data-ttu-id="ecf87-137">Pour plus d’informations, consultez [Comment : créer un gestionnaire d’événements Simple](https://msdn.microsoft.com/library/b1456e07-9dec-4354-99cf-18666b64f480).</span><span class="sxs-lookup"><span data-stu-id="ecf87-137">For more information, see [How to: Create a Simple Event Handler](https://msdn.microsoft.com/library/b1456e07-9dec-4354-99cf-18666b64f480).</span></span>  
  
     <span data-ttu-id="ecf87-138">L’exemple suivant montre le XAML pour MainWindow.xaml.</span><span class="sxs-lookup"><span data-stu-id="ecf87-138">The following shows the XAML for MainWindow.xaml.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="ecf87-139">Si vous utilisez Visual Basic, dans la première ligne de MainWindow.xaml, remplacez `x:Class="DataGridSQLExample.MainWindow"` avec `x:Class="MainWindow"`.</span><span class="sxs-lookup"><span data-stu-id="ecf87-139">If you are using Visual Basic, in the first line of MainWindow.xaml, replace `x:Class="DataGridSQLExample.MainWindow"` with `x:Class="MainWindow"`.</span></span>  
  
     [!code-xaml[DataGrid_SQL_EF_Walkthrough#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_SQL_EF_Walkthrough/CS/MainWindow.xaml#1)]  
  
6.  <span data-ttu-id="ecf87-140">Ouvrez le fichier code-behind (MainWindow.xaml.vb ou MainWindow.xaml.cs) pour le <xref:System.Windows.Window>.</span><span class="sxs-lookup"><span data-stu-id="ecf87-140">Open the code-behind file (MainWindow.xaml.vb or MainWindow.xaml.cs) for the <xref:System.Windows.Window>.</span></span>  
  
7.  <span data-ttu-id="ecf87-141">Ajoutez le code suivant pour récupérer uniquement les valeurs spécifiques des tables jointes et définir le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> propriété de la <xref:System.Windows.Controls.DataGrid> aux résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="ecf87-141">Add the following code to retrieve only specific values from the joined tables and set the <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> property of the <xref:System.Windows.Controls.DataGrid> to the results of the query.</span></span>  
  
     [!code-csharp[DataGrid_SQL_EF_Walkthrough#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_SQL_EF_Walkthrough/CS/MainWindow.xaml.cs#2)]
     [!code-vb[DataGrid_SQL_EF_Walkthrough#2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DataGrid_SQL_EF_Walkthrough/VB/MainWindow.xaml.vb#2)]  
  
8.  <span data-ttu-id="ecf87-142">Exécutez l'exemple.</span><span class="sxs-lookup"><span data-stu-id="ecf87-142">Run the example.</span></span>  
  
     <span data-ttu-id="ecf87-143">Vous devez voir un <xref:System.Windows.Controls.DataGrid> qui affiche des données.</span><span class="sxs-lookup"><span data-stu-id="ecf87-143">You should see a <xref:System.Windows.Controls.DataGrid> that displays data.</span></span>  
  
     <span data-ttu-id="ecf87-144">![DataGrid avec des données à partir de la base de données SQL](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step7.png "DataGrid_SQL_EF_Step7")</span><span class="sxs-lookup"><span data-stu-id="ecf87-144">![DataGrid with data from SQL database](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step7.png "DataGrid_SQL_EF_Step7")</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="ecf87-145">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="ecf87-145">Next Steps</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ecf87-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecf87-146">See Also</span></span>  
 <xref:System.Windows.Controls.DataGrid>  
 [<span data-ttu-id="ecf87-147">Comment : comment pour démarrer avec Entity Framework dans les Applications WPF ?</span><span class="sxs-lookup"><span data-stu-id="ecf87-147">How Do I: Get Started with Entity Framework in WPF Applications?</span></span>](https://go.microsoft.com/fwlink/?LinkId=159868)
