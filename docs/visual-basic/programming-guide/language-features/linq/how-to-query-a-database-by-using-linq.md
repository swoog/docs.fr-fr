---
title: "Comment : interroger une base de données à l'aide de LINQ (Visual Basic)"
ms.date: 07/20/2015
helpviewer_keywords:
- query samples [LINQ]
- database querying [LINQ]
- queries [LINQ in Visual Basic], database querying
- querying databases [LINQ]
- queries [LINQ in Visual Basic], how-to topics
- query samples [Visual Basic]
ms.assetid: bcf5e9c3-a236-4399-9a7f-3991eca7cf56
ms.openlocfilehash: 75f3d71e76c81a016a4e2c6fac754b91db31873e
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2018
ms.locfileid: "42924875"
---
# <a name="how-to-query-a-database-by-using-linq-visual-basic"></a><span data-ttu-id="c593d-102">Comment : interroger une base de données à l'aide de LINQ (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c593d-102">How to: Query a Database by Using LINQ (Visual Basic)</span></span>
<span data-ttu-id="c593d-103">Language-Integrated Query (LINQ) facilite l’accès aux informations de base de données et exécuter des requêtes.</span><span class="sxs-lookup"><span data-stu-id="c593d-103">Language-Integrated Query (LINQ) makes it easy to access database information and execute queries.</span></span>  
  
 <span data-ttu-id="c593d-104">L’exemple suivant montre comment créer une application qui effectue des requêtes sur une base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c593d-104">The following example shows how to create a new application that performs queries against a SQL Server database.</span></span>  
  
 <span data-ttu-id="c593d-105">Les exemples de cette rubrique utilisent la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="c593d-105">The examples in this topic use the Northwind sample database.</span></span> <span data-ttu-id="c593d-106">Si vous n’avez pas de cette base de données sur votre ordinateur de développement, vous pouvez le télécharger à partir du Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="c593d-106">If you do not have this database on your development computer, you can download it from the Microsoft Download Center.</span></span> <span data-ttu-id="c593d-107">Pour obtenir des instructions, consultez [téléchargement d’exemples de bases de données](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md).</span><span class="sxs-lookup"><span data-stu-id="c593d-107">For instructions, see [Downloading Sample Databases](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md).</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
## <a name="to-create-a-connection-to-a-database"></a><span data-ttu-id="c593d-108">Pour créer une connexion à une base de données</span><span class="sxs-lookup"><span data-stu-id="c593d-108">To create a connection to a database</span></span>  
  
1.  <span data-ttu-id="c593d-109">Dans Visual Studio, ouvrez **Explorateur de serveurs**/**Database Explorer** en cliquant sur **Explorateur de serveurs**/**base de données Explorer** sur le **vue** menu.</span><span class="sxs-lookup"><span data-stu-id="c593d-109">In Visual Studio, open **Server Explorer**/**Database Explorer** by clicking **Server Explorer**/**Database Explorer** on the **View** menu.</span></span>  
  
2.  <span data-ttu-id="c593d-110">Avec le bouton droit **des connexions de données** dans **Explorateur de serveurs**/**Database Explorer** puis cliquez sur **ajouter une connexion**.</span><span class="sxs-lookup"><span data-stu-id="c593d-110">Right-click **Data Connections** in **Server Explorer**/**Database Explorer** and then click **Add Connection**.</span></span>  
  
3.  <span data-ttu-id="c593d-111">Spécifiez une connexion valide à la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="c593d-111">Specify a valid connection to the Northwind sample database.</span></span>  
  
## <a name="to-add-a-project-that-contains-a-linq-to-sql-file"></a><span data-ttu-id="c593d-112">Pour ajouter un projet qui contient un fichier LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="c593d-112">To add a project that contains a LINQ to SQL file</span></span>  
  
1.  <span data-ttu-id="c593d-113">Dans Visual Studio, dans le menu **Fichier**,pointez sur **Nouveau**, puis cliquez sur **Projet**.</span><span class="sxs-lookup"><span data-stu-id="c593d-113">In Visual Studio, on the **File** menu, point to **New** and then click **Project**.</span></span> <span data-ttu-id="c593d-114">Sélectionnez Visual Basic **Windows Forms Application** comme type de projet.</span><span class="sxs-lookup"><span data-stu-id="c593d-114">Select Visual Basic **Windows Forms Application** as the project type.</span></span>  
  
2.  <span data-ttu-id="c593d-115">Dans le menu **Projet** , cliquez sur **Ajouter un nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="c593d-115">On the **Project** menu, click **Add New Item**.</span></span> <span data-ttu-id="c593d-116">Sélectionnez le **Classes LINQ to SQL** modèle d’élément.</span><span class="sxs-lookup"><span data-stu-id="c593d-116">Select the **LINQ to SQL Classes** item template.</span></span>  
  
3.  <span data-ttu-id="c593d-117">Nommez le fichier `northwind.dbml`.</span><span class="sxs-lookup"><span data-stu-id="c593d-117">Name the file `northwind.dbml`.</span></span> <span data-ttu-id="c593d-118">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="c593d-118">Click **Add**.</span></span> <span data-ttu-id="c593d-119">Le Concepteur Objet/Relationnel (Concepteur O/R) est ouvert pour le fichier northwind.dbml.</span><span class="sxs-lookup"><span data-stu-id="c593d-119">The Object Relational Designer (O/R Designer) is opened for the northwind.dbml file.</span></span>  
  
## <a name="to-add-tables-to-query-to-the-or-designer"></a><span data-ttu-id="c593d-120">Pour ajouter des tables à interroger au Concepteur O/R</span><span class="sxs-lookup"><span data-stu-id="c593d-120">To add tables to query to the O/R Designer</span></span>  
  
1.  <span data-ttu-id="c593d-121">Dans **Explorateur de serveurs**/**Database Explorer**, développez la connexion à la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="c593d-121">In **Server Explorer**/**Database Explorer**, expand the connection to the Northwind database.</span></span> <span data-ttu-id="c593d-122">Développez le **Tables** dossier.</span><span class="sxs-lookup"><span data-stu-id="c593d-122">Expand the **Tables** folder.</span></span>  
  
     <span data-ttu-id="c593d-123">Si vous avez fermé le Concepteur O/R, vous pouvez le rouvrir en double-cliquant sur le fichier northwind.dbml que vous avez ajouté précédemment.</span><span class="sxs-lookup"><span data-stu-id="c593d-123">If you have closed the O/R Designer, you can reopen it by double-clicking the northwind.dbml file that you added earlier.</span></span>  
  
2.  <span data-ttu-id="c593d-124">Cliquez sur la table Customers et faites-le glisser vers le volet gauche du concepteur.</span><span class="sxs-lookup"><span data-stu-id="c593d-124">Click the Customers table and drag it to the left pane of the designer.</span></span> <span data-ttu-id="c593d-125">Cliquez sur la table Orders et faites-le glisser vers le volet gauche du concepteur.</span><span class="sxs-lookup"><span data-stu-id="c593d-125">Click the Orders table and drag it to the left pane of the designer.</span></span>  
  
     <span data-ttu-id="c593d-126">Le concepteur crée de nouveaux `Customer` et `Order` objets pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="c593d-126">The designer creates new `Customer` and `Order` objects for your project.</span></span> <span data-ttu-id="c593d-127">Notez que le concepteur détecte les relations entre les tables automatiquement et crée des propriétés pour les objets enfants.</span><span class="sxs-lookup"><span data-stu-id="c593d-127">Notice that the designer automatically detects relationships between the tables and creates child properties for related objects.</span></span> <span data-ttu-id="c593d-128">Par exemple, IntelliSense qui affichera le `Customer` objet possède un `Orders` propriété pour toutes les commandes associées à ce client.</span><span class="sxs-lookup"><span data-stu-id="c593d-128">For example, IntelliSense will show that the `Customer` object has an `Orders` property for all orders related to that customer.</span></span>  
  
3.  <span data-ttu-id="c593d-129">Enregistrez vos modifications et fermez le concepteur.</span><span class="sxs-lookup"><span data-stu-id="c593d-129">Save your changes and close the designer.</span></span>  
  
4.  <span data-ttu-id="c593d-130">Enregistrez votre projet.</span><span class="sxs-lookup"><span data-stu-id="c593d-130">Save your project.</span></span>  
  
## <a name="to-add-code-to-query-the-database-and-display-the-results"></a><span data-ttu-id="c593d-131">Pour ajouter du code pour interroger la base de données et afficher les résultats</span><span class="sxs-lookup"><span data-stu-id="c593d-131">To add code to query the database and display the results</span></span>  
  
1.  <span data-ttu-id="c593d-132">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.DataGridView> contrôle sur le formulaire de Windows par défaut pour votre projet, Form1.</span><span class="sxs-lookup"><span data-stu-id="c593d-132">From the **Toolbox**, drag a <xref:System.Windows.Forms.DataGridView> control onto the default Windows Form for your project, Form1.</span></span>  
  
2.  <span data-ttu-id="c593d-133">Double-cliquez sur Form1 pour ajouter du code pour le `Load` événement sous la forme.</span><span class="sxs-lookup"><span data-stu-id="c593d-133">Double-click Form1 to add code to the `Load` event of the form.</span></span>  
  
3.  <span data-ttu-id="c593d-134">Lorsque vous avez ajouté des tables au Concepteur O/R, le concepteur a ajouté un <xref:System.Data.Linq.DataContext> objet pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="c593d-134">When you added tables to the O/R Designer, the designer added a <xref:System.Data.Linq.DataContext> object for your project.</span></span> <span data-ttu-id="c593d-135">Cet objet contient le code dont vous devez disposer pour accéder à ces tables, en plus des collections et des objets individuels de chaque table.</span><span class="sxs-lookup"><span data-stu-id="c593d-135">This object contains the code that you must have to access those tables, in addition to individual objects and collections for each table.</span></span> <span data-ttu-id="c593d-136">Le <xref:System.Data.Linq.DataContext> objet pour votre projet est nommé d’après le nom de votre fichier .dbml.</span><span class="sxs-lookup"><span data-stu-id="c593d-136">The <xref:System.Data.Linq.DataContext> object for your project is named based on the name of your .dbml file.</span></span> <span data-ttu-id="c593d-137">Pour ce projet, le <xref:System.Data.Linq.DataContext> objet est nommé `northwindDataContext`.</span><span class="sxs-lookup"><span data-stu-id="c593d-137">For this project, the <xref:System.Data.Linq.DataContext> object is named `northwindDataContext`.</span></span>  
  
     <span data-ttu-id="c593d-138">Vous pouvez créer une instance de la <xref:System.Data.Linq.DataContext> dans votre code et interroger les tables spécifiées par le Concepteur O/R.</span><span class="sxs-lookup"><span data-stu-id="c593d-138">You can create an instance of the <xref:System.Data.Linq.DataContext> in your code and query the tables specified by the O/R Designer.</span></span>  
  
     <span data-ttu-id="c593d-139">Ajoutez le code suivant à la `Load` événement à interroger les tables qui sont exposées en tant que propriétés de votre contexte de données.</span><span class="sxs-lookup"><span data-stu-id="c593d-139">Add the following code to the `Load` event to query the tables that are exposed as properties of your data context.</span></span>  
  
     [!code-vb[VbLINQToSQLHowTos#3](../../../../visual-basic/programming-guide/language-features/linq/codesnippet/VisualBasic/how-to-query-a-database-by-using-linq_1.vb)]  
  
4.  <span data-ttu-id="c593d-140">Appuyez sur F5 pour exécuter votre projet et afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="c593d-140">Press F5 to run your project and view the results.</span></span>  
  
5.  <span data-ttu-id="c593d-141">Voici quelques requêtes supplémentaires que vous pouvez essayer :</span><span class="sxs-lookup"><span data-stu-id="c593d-141">Following are some additional queries that you can try:</span></span>  
  
     [!code-vb[VbLINQToSQLHowTos#4](../../../../visual-basic/programming-guide/language-features/linq/codesnippet/VisualBasic/how-to-query-a-database-by-using-linq_2.vb)]  
    [!code-vb[VbLINQToSQLHowTos#5](../../../../visual-basic/programming-guide/language-features/linq/codesnippet/VisualBasic/how-to-query-a-database-by-using-linq_3.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="c593d-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c593d-142">See Also</span></span>  
 [<span data-ttu-id="c593d-143">LINQ</span><span class="sxs-lookup"><span data-stu-id="c593d-143">LINQ</span></span>](../../../../visual-basic/programming-guide/language-features/linq/index.md)  
 [<span data-ttu-id="c593d-144">Requêtes</span><span class="sxs-lookup"><span data-stu-id="c593d-144">Queries</span></span>](../../../../visual-basic/language-reference/queries/index.md)  
 [<span data-ttu-id="c593d-145">LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="c593d-145">LINQ to SQL</span></span>](../../../../framework/data/adonet/sql/linq/index.md)  
 [<span data-ttu-id="c593d-146">DataContext, méthodes (Concepteur O/R)</span><span class="sxs-lookup"><span data-stu-id="c593d-146">DataContext Methods (O/R Designer)</span></span>](/visualstudio/data-tools/datacontext-methods-o-r-designer)
