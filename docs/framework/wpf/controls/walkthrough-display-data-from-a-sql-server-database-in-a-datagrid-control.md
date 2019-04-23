---
title: 'Procédure pas à pas : afficher des données à partir d’une base de données SQL Server dans un contrôle DataGrid'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGrid [WPF], displaying data from SQL Server
- controls [WPF], DataGrid
ms.assetid: 6810b048-0a23-4f86-bfa5-97f92b3cfab4
ms.openlocfilehash: 274ec2e8ef16190da53061bb197bc3b1a1fadcf8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59336107"
---
# <a name="walkthrough-display-data-from-a-sql-server-database-in-a-datagrid-control"></a><span data-ttu-id="caae8-102">Procédure pas à pas : Afficher des données à partir d’une base de données SQL Server dans un contrôle DataGrid</span><span class="sxs-lookup"><span data-stu-id="caae8-102">Walkthrough: Display data from a SQL Server database in a DataGrid control</span></span>

<span data-ttu-id="caae8-103">Dans cette procédure pas à pas, vous récupérer des données à partir d’une base de données SQL Server et afficher ces données dans un <xref:System.Windows.Controls.DataGrid> contrôle.</span><span class="sxs-lookup"><span data-stu-id="caae8-103">In this walkthrough, you retrieve data from a SQL Server database and display that data in a <xref:System.Windows.Controls.DataGrid> control.</span></span> <span data-ttu-id="caae8-104">ADO.NET Entity Framework vous permet de créer les classes d’entité qui représentent les données et utilisent LINQ pour écrire une requête qui Récupère les données spécifiées à partir d’une classe d’entité.</span><span class="sxs-lookup"><span data-stu-id="caae8-104">You use the ADO.NET Entity Framework to create the entity classes that represent the data, and use LINQ to write a query that retrieves the specified data from an entity class.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="caae8-105">Prérequis</span><span class="sxs-lookup"><span data-stu-id="caae8-105">Prerequisites</span></span>

<span data-ttu-id="caae8-106">Pour exécuter cette procédure pas à pas, vous devez disposer des composants suivants :</span><span class="sxs-lookup"><span data-stu-id="caae8-106">You need the following components to complete this walkthrough:</span></span>

-   <span data-ttu-id="caae8-107">Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="caae8-107">Visual Studio.</span></span>

-   <span data-ttu-id="caae8-108">Accès à une instance en cours d’exécution de SQL Server ou SQL Server Express qui a la base de données AdventureWorks attachée.</span><span class="sxs-lookup"><span data-stu-id="caae8-108">Access to a running instance of SQL Server or SQL Server Express that has the AdventureWorks sample database attached to it.</span></span> <span data-ttu-id="caae8-109">Vous pouvez télécharger la base de données AdventureWorks à partir de la [GitHub](https://github.com/Microsoft/sql-server-samples/releases).</span><span class="sxs-lookup"><span data-stu-id="caae8-109">You can download the AdventureWorks database from the [GitHub](https://github.com/Microsoft/sql-server-samples/releases).</span></span>

## <a name="create-entity-classes"></a><span data-ttu-id="caae8-110">Créer des classes d’entité</span><span class="sxs-lookup"><span data-stu-id="caae8-110">Create entity classes</span></span>

1. <span data-ttu-id="caae8-111">Créez un nouveau projet d’Application WPF en Visual Basic ou c# et nommez-le `DataGridSQLExample`.</span><span class="sxs-lookup"><span data-stu-id="caae8-111">Create a new WPF Application project in Visual Basic or C#, and name it `DataGridSQLExample`.</span></span>

2. <span data-ttu-id="caae8-112">Dans l’Explorateur de solutions, cliquez sur votre projet, pointez sur **ajouter**, puis sélectionnez **un nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="caae8-112">In Solution Explorer, right-click your project, point to **Add**, and then select **New Item**.</span></span>

     <span data-ttu-id="caae8-113">La boîte de dialogue Ajouter un nouvel élément s’affiche.</span><span class="sxs-lookup"><span data-stu-id="caae8-113">The Add New Item dialog box appears.</span></span>

3. <span data-ttu-id="caae8-114">Dans le volet Modèles installés, sélectionnez **données** et dans la liste des modèles, sélectionnez **ADO.NET Entity Data Model**.</span><span class="sxs-lookup"><span data-stu-id="caae8-114">In the Installed Templates pane, select **Data** and in the list of templates, select **ADO.NET Entity Data Model**.</span></span>

     ![Modèle d’élément ADO.NET Entity Data Model](../../wcf/feature-details/./media/ado-net-entity-data-model-item-template.png)

4. <span data-ttu-id="caae8-116">Nommez le fichier `AdventureWorksModel.edmx` puis cliquez sur **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="caae8-116">Name the file `AdventureWorksModel.edmx` and then click **Add**.</span></span>

     <span data-ttu-id="caae8-117">L'Assistant Entity Data Model s'affiche.</span><span class="sxs-lookup"><span data-stu-id="caae8-117">The Entity Data Model Wizard appears.</span></span>

5. <span data-ttu-id="caae8-118">Dans l’écran Choisir le contenu du modèle, sélectionnez **Entity Framework Designer à partir de la base de données** puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="caae8-118">In the Choose Model Contents screen, select **EF Designer from database** and then click **Next**.</span></span>

6. <span data-ttu-id="caae8-119">Dans l’écran Choisir votre connexion de données, fournissez la connexion à votre base de données AdventureWorksLT2008.</span><span class="sxs-lookup"><span data-stu-id="caae8-119">In the Choose Your Data Connection screen, provide the connection to your AdventureWorksLT2008 database.</span></span> <span data-ttu-id="caae8-120">Pour plus d’informations, consultez [boîte de dialogue Choisir votre connexion de données](https://go.microsoft.com/fwlink/?LinkId=160190).</span><span class="sxs-lookup"><span data-stu-id="caae8-120">For more information, see [Choose Your Data Connection Dialog Box](https://go.microsoft.com/fwlink/?LinkId=160190).</span></span>

    <span data-ttu-id="caae8-121">Assurez-vous que le nom est `AdventureWorksLT2008Entities` et que le **enregistrer des paramètres de connexion entity dans App.Config en tant que** case à cocher est sélectionnée, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="caae8-121">Make sure that the name is `AdventureWorksLT2008Entities` and that the **Save entity connection settings in App.Config as** check box is selected, and then click **Next**.</span></span>

7. <span data-ttu-id="caae8-122">Dans l’écran Choisir vos objets de base de données, développez le nœud Tables, puis sélectionnez le **produit** et **ProductCategory** tables.</span><span class="sxs-lookup"><span data-stu-id="caae8-122">In the Choose Your Database Objects screen, expand the Tables node, and select the **Product** and **ProductCategory** tables.</span></span>

     <span data-ttu-id="caae8-123">Vous pouvez générer des classes d’entités pour toutes les tables ; Toutefois, dans cet exemple vous uniquement récupérer des données à partir de ces deux tables.</span><span class="sxs-lookup"><span data-stu-id="caae8-123">You can generate entity classes for all of the tables; however, in this example you only retrieve data from those two tables.</span></span>

     <span data-ttu-id="caae8-124">![Sélectionner Product et ProductCategory à partir des tables](./media/datagrid-sql-ef-step4.png "DataGrid_SQL_EF_Step4")</span><span class="sxs-lookup"><span data-stu-id="caae8-124">![Select Product and ProductCategory from tables](./media/datagrid-sql-ef-step4.png "DataGrid_SQL_EF_Step4")</span></span>

8. <span data-ttu-id="caae8-125">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="caae8-125">Click **Finish**.</span></span>

     <span data-ttu-id="caae8-126">Les entités Product et ProductCategory sont affichées dans le Concepteur d’entités.</span><span class="sxs-lookup"><span data-stu-id="caae8-126">The Product and ProductCategory entities are displayed in the Entity Designer.</span></span>

     <span data-ttu-id="caae8-127">![Modèles d’entité Product et ProductCategory](./media/datagrid-sql-ef-step5.png "DataGrid_SQL_EF_Step5")</span><span class="sxs-lookup"><span data-stu-id="caae8-127">![Product and ProductCategory entity models](./media/datagrid-sql-ef-step5.png "DataGrid_SQL_EF_Step5")</span></span>

## <a name="retrieve-and-present-the-data"></a><span data-ttu-id="caae8-128">Récupérer et de présenter les données</span><span class="sxs-lookup"><span data-stu-id="caae8-128">Retrieve and present the data</span></span>

1. <span data-ttu-id="caae8-129">Ouvrez le fichier MainWindow.xaml.</span><span class="sxs-lookup"><span data-stu-id="caae8-129">Open the MainWindow.xaml file.</span></span>

2. <span data-ttu-id="caae8-130">Définir le <xref:System.Windows.FrameworkElement.Width%2A> propriété sur le <xref:System.Windows.Window> à 450.</span><span class="sxs-lookup"><span data-stu-id="caae8-130">Set the <xref:System.Windows.FrameworkElement.Width%2A> property on the <xref:System.Windows.Window> to 450.</span></span>

3. <span data-ttu-id="caae8-131">Dans l’éditeur XAML, ajoutez le code suivant <xref:System.Windows.Controls.DataGrid> balise entre les `<Grid>` et `</Grid>` balises pour ajouter un <xref:System.Windows.Controls.DataGrid> nommé `dataGrid1`.</span><span class="sxs-lookup"><span data-stu-id="caae8-131">In the XAML editor, add the following <xref:System.Windows.Controls.DataGrid> tag between the `<Grid>` and `</Grid>` tags to add a <xref:System.Windows.Controls.DataGrid> named `dataGrid1`.</span></span>

     [!code-xaml[DataGrid_SQL_EF_Walkthrough#3](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_SQL_EF_Walkthrough/CS/MainWindow.xaml#3)]

     <span data-ttu-id="caae8-132">![Fenêtre avec DataGrid](./media/datagrid-sql-ef-step6.png "DataGrid_SQL_EF_Step6")</span><span class="sxs-lookup"><span data-stu-id="caae8-132">![Window with DataGrid](./media/datagrid-sql-ef-step6.png "DataGrid_SQL_EF_Step6")</span></span>

4. <span data-ttu-id="caae8-133">Sélectionnez le contrôle <xref:System.Windows.Window>.</span><span class="sxs-lookup"><span data-stu-id="caae8-133">Select the <xref:System.Windows.Window>.</span></span>

5. <span data-ttu-id="caae8-134">À l’aide de la fenêtre Propriétés ou l’éditeur XAML, créez un gestionnaire d’événements pour le <xref:System.Windows.Window> nommé `Window_Loaded` pour le <xref:System.Windows.FrameworkElement.Loaded> événement.</span><span class="sxs-lookup"><span data-stu-id="caae8-134">Using the Properties window or XAML editor, create an event handler for the <xref:System.Windows.Window> named `Window_Loaded` for the <xref:System.Windows.FrameworkElement.Loaded> event.</span></span> <span data-ttu-id="caae8-135">Pour plus d'informations, voir [Procédure : Créez un gestionnaire d’événements Simple](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb675300(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="caae8-135">For more information, see [How to: Create a Simple Event Handler](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb675300(v=vs.100)).</span></span>

     <span data-ttu-id="caae8-136">L’exemple suivant montre le XAML pour MainWindow.xaml.</span><span class="sxs-lookup"><span data-stu-id="caae8-136">The following shows the XAML for MainWindow.xaml.</span></span>

    > [!NOTE]
    > <span data-ttu-id="caae8-137">Si vous utilisez Visual Basic, dans la première ligne de MainWindow.xaml, remplacez `x:Class="DataGridSQLExample.MainWindow"` avec `x:Class="MainWindow"`.</span><span class="sxs-lookup"><span data-stu-id="caae8-137">If you are using Visual Basic, in the first line of MainWindow.xaml, replace `x:Class="DataGridSQLExample.MainWindow"` with `x:Class="MainWindow"`.</span></span>

     [!code-xaml[DataGrid_SQL_EF_Walkthrough#1](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_SQL_EF_Walkthrough/CS/MainWindow.xaml#1)]

6. <span data-ttu-id="caae8-138">Ouvrez le fichier code-behind (MainWindow.xaml.vb ou MainWindow.xaml.cs) pour le <xref:System.Windows.Window>.</span><span class="sxs-lookup"><span data-stu-id="caae8-138">Open the code-behind file (MainWindow.xaml.vb or MainWindow.xaml.cs) for the <xref:System.Windows.Window>.</span></span>

7. <span data-ttu-id="caae8-139">Ajoutez le code suivant pour récupérer uniquement les valeurs spécifiques des tables jointes et définir le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> propriété de la <xref:System.Windows.Controls.DataGrid> aux résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="caae8-139">Add the following code to retrieve only specific values from the joined tables and set the <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> property of the <xref:System.Windows.Controls.DataGrid> to the results of the query.</span></span>

     [!code-csharp[DataGrid_SQL_EF_Walkthrough#2](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_SQL_EF_Walkthrough/CS/MainWindow.xaml.cs#2)]
     [!code-vb[DataGrid_SQL_EF_Walkthrough#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DataGrid_SQL_EF_Walkthrough/VB/MainWindow.xaml.vb#2)]

8. <span data-ttu-id="caae8-140">Exécutez l'exemple.</span><span class="sxs-lookup"><span data-stu-id="caae8-140">Run the example.</span></span>

     <span data-ttu-id="caae8-141">Vous devez voir un <xref:System.Windows.Controls.DataGrid> qui affiche des données.</span><span class="sxs-lookup"><span data-stu-id="caae8-141">You should see a <xref:System.Windows.Controls.DataGrid> that displays data.</span></span>

     <span data-ttu-id="caae8-142">![DataGrid avec des données à partir de la base de données SQL](./media/datagrid-sql-ef-step7.png "DataGrid_SQL_EF_Step7")</span><span class="sxs-lookup"><span data-stu-id="caae8-142">![DataGrid with data from SQL database](./media/datagrid-sql-ef-step7.png "DataGrid_SQL_EF_Step7")</span></span>

## <a name="see-also"></a><span data-ttu-id="caae8-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="caae8-143">See also</span></span>

- <xref:System.Windows.Controls.DataGrid>
- [<span data-ttu-id="caae8-144">Comment faire Bien démarrer avec Entity Framework dans les Applications WPF ?</span><span class="sxs-lookup"><span data-stu-id="caae8-144">How Do I: Get Started with Entity Framework in WPF Applications?</span></span>](https://go.microsoft.com/fwlink/?LinkId=159868)