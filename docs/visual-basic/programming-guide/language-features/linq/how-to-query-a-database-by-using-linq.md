---
title: 'Procédure : Interroger une base de données à l’aide de LINQ (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- query samples [LINQ]
- database querying [LINQ]
- queries [LINQ in Visual Basic], database querying
- querying databases [LINQ]
- queries [LINQ in Visual Basic], how-to topics
- query samples [Visual Basic]
ms.assetid: bcf5e9c3-a236-4399-9a7f-3991eca7cf56
ms.openlocfilehash: 29986c703fd83919ffda9a39d6dbdbf28d778bd6
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56981892"
---
# <a name="how-to-query-a-database-by-using-linq-visual-basic"></a><span data-ttu-id="919bc-102">Procédure : Interroger une base de données à l’aide de LINQ (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="919bc-102">How to: Query a Database by Using LINQ (Visual Basic)</span></span>
<span data-ttu-id="919bc-103">Language-Integrated Query (LINQ) facilite l’accès aux informations de base de données et exécuter des requêtes.</span><span class="sxs-lookup"><span data-stu-id="919bc-103">Language-Integrated Query (LINQ) makes it easy to access database information and execute queries.</span></span>  
  
 <span data-ttu-id="919bc-104">L’exemple suivant montre comment créer une application qui effectue des requêtes sur une base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="919bc-104">The following example shows how to create a new application that performs queries against a SQL Server database.</span></span>  
  
 <span data-ttu-id="919bc-105">Les exemples de cette rubrique utilisent la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="919bc-105">The examples in this topic use the Northwind sample database.</span></span> <span data-ttu-id="919bc-106">Si vous n’avez pas de cette base de données sur votre ordinateur de développement, vous pouvez le télécharger à partir du Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="919bc-106">If you do not have this database on your development computer, you can download it from the Microsoft Download Center.</span></span> <span data-ttu-id="919bc-107">Pour obtenir des instructions, consultez [téléchargement d’exemples de bases de données](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md).</span><span class="sxs-lookup"><span data-stu-id="919bc-107">For instructions, see [Downloading Sample Databases](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md).</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
## <a name="to-create-a-connection-to-a-database"></a><span data-ttu-id="919bc-108">Pour créer une connexion à une base de données</span><span class="sxs-lookup"><span data-stu-id="919bc-108">To create a connection to a database</span></span>  
  
1.  <span data-ttu-id="919bc-109">Dans Visual Studio, ouvrez **Explorateur de serveurs**/**Database Explorer** en cliquant sur **Explorateur de serveurs**/**base de données Explorer** sur le **vue** menu.</span><span class="sxs-lookup"><span data-stu-id="919bc-109">In Visual Studio, open **Server Explorer**/**Database Explorer** by clicking **Server Explorer**/**Database Explorer** on the **View** menu.</span></span>  
  
2.  <span data-ttu-id="919bc-110">Avec le bouton droit **des connexions de données** dans **Explorateur de serveurs**/**Database Explorer** puis cliquez sur **ajouter une connexion**.</span><span class="sxs-lookup"><span data-stu-id="919bc-110">Right-click **Data Connections** in **Server Explorer**/**Database Explorer** and then click **Add Connection**.</span></span>  
  
3.  <span data-ttu-id="919bc-111">Spécifiez une connexion valide à la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="919bc-111">Specify a valid connection to the Northwind sample database.</span></span>  
  
## <a name="to-add-a-project-that-contains-a-linq-to-sql-file"></a><span data-ttu-id="919bc-112">Pour ajouter un projet qui contient un fichier LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="919bc-112">To add a project that contains a LINQ to SQL file</span></span>  
  
1.  <span data-ttu-id="919bc-113">Dans Visual Studio, dans le menu **Fichier**,pointez sur **Nouveau**, puis cliquez sur **Projet**.</span><span class="sxs-lookup"><span data-stu-id="919bc-113">In Visual Studio, on the **File** menu, point to **New** and then click **Project**.</span></span> <span data-ttu-id="919bc-114">Sélectionnez Visual Basic **Windows Forms Application** comme type de projet.</span><span class="sxs-lookup"><span data-stu-id="919bc-114">Select Visual Basic **Windows Forms Application** as the project type.</span></span>  
  
2.  <span data-ttu-id="919bc-115">Dans le menu **Projet** , cliquez sur **Ajouter un nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="919bc-115">On the **Project** menu, click **Add New Item**.</span></span> <span data-ttu-id="919bc-116">Sélectionnez le **Classes LINQ to SQL** modèle d’élément.</span><span class="sxs-lookup"><span data-stu-id="919bc-116">Select the **LINQ to SQL Classes** item template.</span></span>  
  
3.  <span data-ttu-id="919bc-117">Nommez le fichier `northwind.dbml`.</span><span class="sxs-lookup"><span data-stu-id="919bc-117">Name the file `northwind.dbml`.</span></span> <span data-ttu-id="919bc-118">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="919bc-118">Click **Add**.</span></span> <span data-ttu-id="919bc-119">Le Concepteur Objet/Relationnel (Concepteur O/R) est ouvert pour le fichier northwind.dbml.</span><span class="sxs-lookup"><span data-stu-id="919bc-119">The Object Relational Designer (O/R Designer) is opened for the northwind.dbml file.</span></span>  
  
## <a name="to-add-tables-to-query-to-the-or-designer"></a><span data-ttu-id="919bc-120">Pour ajouter des tables à interroger au Concepteur O/R</span><span class="sxs-lookup"><span data-stu-id="919bc-120">To add tables to query to the O/R Designer</span></span>  
  
1.  <span data-ttu-id="919bc-121">Dans **Explorateur de serveurs**/**Database Explorer**, développez la connexion à la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="919bc-121">In **Server Explorer**/**Database Explorer**, expand the connection to the Northwind database.</span></span> <span data-ttu-id="919bc-122">Développez le **Tables** dossier.</span><span class="sxs-lookup"><span data-stu-id="919bc-122">Expand the **Tables** folder.</span></span>  
  
     <span data-ttu-id="919bc-123">Si vous avez fermé le Concepteur O/R, vous pouvez le rouvrir en double-cliquant sur le fichier northwind.dbml que vous avez ajouté précédemment.</span><span class="sxs-lookup"><span data-stu-id="919bc-123">If you have closed the O/R Designer, you can reopen it by double-clicking the northwind.dbml file that you added earlier.</span></span>  
  
2.  <span data-ttu-id="919bc-124">Cliquez sur la table Customers et faites-le glisser vers le volet gauche du concepteur.</span><span class="sxs-lookup"><span data-stu-id="919bc-124">Click the Customers table and drag it to the left pane of the designer.</span></span> <span data-ttu-id="919bc-125">Cliquez sur la table Orders et faites-le glisser vers le volet gauche du concepteur.</span><span class="sxs-lookup"><span data-stu-id="919bc-125">Click the Orders table and drag it to the left pane of the designer.</span></span>  
  
     <span data-ttu-id="919bc-126">Le concepteur crée de nouveaux `Customer` et `Order` objets pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="919bc-126">The designer creates new `Customer` and `Order` objects for your project.</span></span> <span data-ttu-id="919bc-127">Notez que le concepteur détecte les relations entre les tables automatiquement et crée des propriétés pour les objets enfants.</span><span class="sxs-lookup"><span data-stu-id="919bc-127">Notice that the designer automatically detects relationships between the tables and creates child properties for related objects.</span></span> <span data-ttu-id="919bc-128">Par exemple, IntelliSense qui affichera le `Customer` objet possède un `Orders` propriété pour toutes les commandes associées à ce client.</span><span class="sxs-lookup"><span data-stu-id="919bc-128">For example, IntelliSense will show that the `Customer` object has an `Orders` property for all orders related to that customer.</span></span>  
  
3.  <span data-ttu-id="919bc-129">Enregistrez vos modifications et fermez le concepteur.</span><span class="sxs-lookup"><span data-stu-id="919bc-129">Save your changes and close the designer.</span></span>  
  
4.  <span data-ttu-id="919bc-130">Enregistrez votre projet.</span><span class="sxs-lookup"><span data-stu-id="919bc-130">Save your project.</span></span>  
  
## <a name="to-add-code-to-query-the-database-and-display-the-results"></a><span data-ttu-id="919bc-131">Pour ajouter du code pour interroger la base de données et afficher les résultats</span><span class="sxs-lookup"><span data-stu-id="919bc-131">To add code to query the database and display the results</span></span>  
  
1.  <span data-ttu-id="919bc-132">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.DataGridView> contrôle sur le formulaire de Windows par défaut pour votre projet, Form1.</span><span class="sxs-lookup"><span data-stu-id="919bc-132">From the **Toolbox**, drag a <xref:System.Windows.Forms.DataGridView> control onto the default Windows Form for your project, Form1.</span></span>  
  
2.  <span data-ttu-id="919bc-133">Double-cliquez sur Form1 pour ajouter du code pour le `Load` événement sous la forme.</span><span class="sxs-lookup"><span data-stu-id="919bc-133">Double-click Form1 to add code to the `Load` event of the form.</span></span>  
  
3.  <span data-ttu-id="919bc-134">Lorsque vous avez ajouté des tables au Concepteur O/R, le concepteur a ajouté un <xref:System.Data.Linq.DataContext> objet pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="919bc-134">When you added tables to the O/R Designer, the designer added a <xref:System.Data.Linq.DataContext> object for your project.</span></span> <span data-ttu-id="919bc-135">Cet objet contient le code dont vous devez disposer pour accéder à ces tables, en plus des collections et des objets individuels de chaque table.</span><span class="sxs-lookup"><span data-stu-id="919bc-135">This object contains the code that you must have to access those tables, in addition to individual objects and collections for each table.</span></span> <span data-ttu-id="919bc-136">Le <xref:System.Data.Linq.DataContext> objet pour votre projet est nommé d’après le nom de votre fichier .dbml.</span><span class="sxs-lookup"><span data-stu-id="919bc-136">The <xref:System.Data.Linq.DataContext> object for your project is named based on the name of your .dbml file.</span></span> <span data-ttu-id="919bc-137">Pour ce projet, le <xref:System.Data.Linq.DataContext> objet est nommé `northwindDataContext`.</span><span class="sxs-lookup"><span data-stu-id="919bc-137">For this project, the <xref:System.Data.Linq.DataContext> object is named `northwindDataContext`.</span></span>  
  
     <span data-ttu-id="919bc-138">Vous pouvez créer une instance de la <xref:System.Data.Linq.DataContext> dans votre code et interroger les tables spécifiées par le Concepteur O/R.</span><span class="sxs-lookup"><span data-stu-id="919bc-138">You can create an instance of the <xref:System.Data.Linq.DataContext> in your code and query the tables specified by the O/R Designer.</span></span>  
  
     <span data-ttu-id="919bc-139">Ajoutez le code suivant à la `Load` événement à interroger les tables qui sont exposées en tant que propriétés de votre contexte de données.</span><span class="sxs-lookup"><span data-stu-id="919bc-139">Add the following code to the `Load` event to query the tables that are exposed as properties of your data context.</span></span>  
  
     [!code-vb[VbLINQToSQLHowTos#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQtoSQLHowTos/VB/Form2.vb#3)]  
  
4.  <span data-ttu-id="919bc-140">Appuyez sur F5 pour exécuter votre projet et afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="919bc-140">Press F5 to run your project and view the results.</span></span>  
  
5.  <span data-ttu-id="919bc-141">Voici quelques requêtes supplémentaires que vous pouvez essayer :</span><span class="sxs-lookup"><span data-stu-id="919bc-141">Following are some additional queries that you can try:</span></span>  
  
     [!code-vb[VbLINQToSQLHowTos#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQtoSQLHowTos/VB/Form2.vb#4)]  
    [!code-vb[VbLINQToSQLHowTos#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQtoSQLHowTos/VB/Form2.vb#5)]  
  
## <a name="see-also"></a><span data-ttu-id="919bc-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="919bc-142">See also</span></span>
- [<span data-ttu-id="919bc-143">LINQ</span><span class="sxs-lookup"><span data-stu-id="919bc-143">LINQ</span></span>](../../../../visual-basic/programming-guide/language-features/linq/index.md)
- [<span data-ttu-id="919bc-144">Requêtes</span><span class="sxs-lookup"><span data-stu-id="919bc-144">Queries</span></span>](../../../../visual-basic/language-reference/queries/index.md)
- [<span data-ttu-id="919bc-145">LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="919bc-145">LINQ to SQL</span></span>](../../../../framework/data/adonet/sql/linq/index.md)
- [<span data-ttu-id="919bc-146">DataContext, méthodes (Concepteur O/R)</span><span class="sxs-lookup"><span data-stu-id="919bc-146">DataContext Methods (O/R Designer)</span></span>](/visualstudio/data-tools/datacontext-methods-o-r-designer)
