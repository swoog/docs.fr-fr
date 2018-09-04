---
title: "Comment : filtrer les résultats d'une requête à l'aide de LINQ (Visual Basic)"
ms.date: 07/20/2015
helpviewer_keywords:
- filtering [Visual Basic]
- filtering data [LINQ in Visual Basic]
- filtering [LINQ in Visual Basic]
- queries [LINQ in Visual Basic], filtering results
- querying databases [LINQ]
- queries [LINQ in Visual Basic], how-to topics
- query samples [Visual Basic]
- filtering data [Visual Basic]
ms.assetid: ef103092-9bed-4134-97f4-2db696e83c12
ms.openlocfilehash: f9854650b1f89a2330cfa81910187e3fb01c54b4
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43519646"
---
# <a name="how-to-filter-query-results-by-using-linq-visual-basic"></a><span data-ttu-id="3b6bc-102">Comment : filtrer les résultats d'une requête à l'aide de LINQ (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="3b6bc-102">How to: Filter Query Results by Using LINQ (Visual Basic)</span></span>
<span data-ttu-id="3b6bc-103">Language-Integrated Query (LINQ) facilite l’accès aux informations de base de données et exécuter des requêtes.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-103">Language-Integrated Query (LINQ) makes it easy to access database information and execute queries.</span></span>  
  
 <span data-ttu-id="3b6bc-104">L’exemple suivant montre comment créer une application qui effectue des requêtes sur une base de données SQL Server et filtre les résultats par une valeur particulière à l’aide de la `Where` clause.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-104">The following example shows how to create a new application that performs queries against a SQL Server database and filters the results by a particular value by using the `Where` clause.</span></span> <span data-ttu-id="3b6bc-105">Pour plus d’informations, consultez [une Clause Where](../../../../visual-basic/language-reference/queries/where-clause.md).</span><span class="sxs-lookup"><span data-stu-id="3b6bc-105">For more information, see [Where Clause](../../../../visual-basic/language-reference/queries/where-clause.md).</span></span>  
  
 <span data-ttu-id="3b6bc-106">Les exemples de cette rubrique utilisent la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-106">The examples in this topic use the Northwind sample database.</span></span> <span data-ttu-id="3b6bc-107">Si vous n’avez pas de cette base de données sur votre ordinateur de développement, vous pouvez le télécharger à partir du Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-107">If you do not have this database on your development computer, you can download it from the Microsoft Download Center.</span></span> <span data-ttu-id="3b6bc-108">Pour obtenir des instructions, consultez [téléchargement d’exemples de bases de données](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md).</span><span class="sxs-lookup"><span data-stu-id="3b6bc-108">For instructions, see [Downloading Sample Databases](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md).</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-a-connection-to-a-database"></a><span data-ttu-id="3b6bc-109">Pour créer une connexion à une base de données</span><span class="sxs-lookup"><span data-stu-id="3b6bc-109">To create a connection to a database</span></span>  
  
1.  <span data-ttu-id="3b6bc-110">Dans Visual Studio, ouvrez **Explorateur de serveurs**/**Database Explorer** en cliquant sur **Explorateur de serveurs**/**base de données Explorer** sur le **vue** menu.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-110">In Visual Studio, open **Server Explorer**/**Database Explorer** by clicking **Server Explorer**/**Database Explorer** on the **View** menu.</span></span>  
  
2.  <span data-ttu-id="3b6bc-111">Avec le bouton droit **des connexions de données** dans **Explorateur de serveurs**/**Database Explorer** puis cliquez sur **ajouter une connexion**.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-111">Right-click **Data Connections** in **Server Explorer**/**Database Explorer** and then click **Add Connection**.</span></span>  
  
3.  <span data-ttu-id="3b6bc-112">Spécifiez une connexion valide à la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-112">Specify a valid connection to the Northwind sample database.</span></span>  
  
### <a name="to-add-a-project-that-contains-a-linq-to-sql-file"></a><span data-ttu-id="3b6bc-113">Pour ajouter un projet qui contient un fichier LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="3b6bc-113">To add a project that contains a LINQ to SQL file</span></span>  
  
1.  <span data-ttu-id="3b6bc-114">Dans Visual Studio, dans le menu **Fichier**,pointez sur **Nouveau**, puis cliquez sur **Projet**.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-114">In Visual Studio, on the **File** menu, point to **New** and then click **Project**.</span></span> <span data-ttu-id="3b6bc-115">Sélectionnez Visual Basic **Windows Forms Application** comme type de projet.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-115">Select Visual Basic **Windows Forms Application** as the project type.</span></span>  
  
2.  <span data-ttu-id="3b6bc-116">Dans le menu **Projet** , cliquez sur **Ajouter un nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-116">On the **Project** menu, click **Add New Item**.</span></span> <span data-ttu-id="3b6bc-117">Sélectionnez le **Classes LINQ to SQL** modèle d’élément.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-117">Select the **LINQ to SQL Classes** item template.</span></span>  
  
3.  <span data-ttu-id="3b6bc-118">Nommez le fichier `northwind.dbml`.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-118">Name the file `northwind.dbml`.</span></span> <span data-ttu-id="3b6bc-119">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-119">Click **Add**.</span></span> <span data-ttu-id="3b6bc-120">Le Concepteur Objet/Relationnel (Concepteur O/R) s’ouvre pour le fichier northwind.dbml.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-120">The Object Relational Designer (O/R Designer) opens for the northwind.dbml file.</span></span>  
  
### <a name="to-add-tables-to-query-to-the-or-designer"></a><span data-ttu-id="3b6bc-121">Pour ajouter des tables à interroger au Concepteur O/R</span><span class="sxs-lookup"><span data-stu-id="3b6bc-121">To add tables to query to the O/R Designer</span></span>  
  
1.  <span data-ttu-id="3b6bc-122">Dans **Explorateur de serveurs**/**Database Explorer**, développez la connexion à la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-122">In **Server Explorer**/**Database Explorer**, expand the connection to the Northwind database.</span></span> <span data-ttu-id="3b6bc-123">Développez le **Tables** dossier.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-123">Expand the **Tables** folder.</span></span>  
  
     <span data-ttu-id="3b6bc-124">Si vous avez fermé le Concepteur O/R, vous pouvez le rouvrir en double-cliquant sur le fichier northwind.dbml que vous avez ajouté précédemment.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-124">If you have closed the O/R Designer, you can reopen it by double-clicking the northwind.dbml file that you added earlier.</span></span>  
  
2.  <span data-ttu-id="3b6bc-125">Cliquez sur la table Customers et faites-le glisser vers le volet gauche du concepteur.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-125">Click the Customers table and drag it to the left pane of the designer.</span></span> <span data-ttu-id="3b6bc-126">Cliquez sur la table Orders et faites-le glisser vers le volet gauche du concepteur.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-126">Click the Orders table and drag it to the left pane of the designer.</span></span>  
  
     <span data-ttu-id="3b6bc-127">Le concepteur crée de nouveaux `Customer` et `Order` objets pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-127">The designer creates new `Customer` and `Order` objects for your project.</span></span> <span data-ttu-id="3b6bc-128">Notez que le concepteur détecte les relations entre les tables automatiquement et crée des propriétés pour les objets enfants.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-128">Notice that the designer automatically detects relationships between the tables and creates child properties for related objects.</span></span> <span data-ttu-id="3b6bc-129">Par exemple, IntelliSense qui affichera le `Customer` objet possède un `Orders` propriété pour toutes les commandes associées à ce client.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-129">For example, IntelliSense will show that the `Customer` object has an `Orders` property for all orders related to that customer.</span></span>  
  
3.  <span data-ttu-id="3b6bc-130">Enregistrez vos modifications et fermez le concepteur.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-130">Save your changes and close the designer.</span></span>  
  
4.  <span data-ttu-id="3b6bc-131">Enregistrez votre projet.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-131">Save your project.</span></span>  
  
### <a name="to-add-code-to-query-the-database-and-display-the-results"></a><span data-ttu-id="3b6bc-132">Pour ajouter du code pour interroger la base de données et afficher les résultats</span><span class="sxs-lookup"><span data-stu-id="3b6bc-132">To add code to query the database and display the results</span></span>  
  
1.  <span data-ttu-id="3b6bc-133">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.DataGridView> contrôle sur le formulaire de Windows par défaut pour votre projet, Form1.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-133">From the **Toolbox**, drag a <xref:System.Windows.Forms.DataGridView> control onto the default Windows Form for your project, Form1.</span></span>  
  
2.  <span data-ttu-id="3b6bc-134">Double-cliquez sur Form1 pour ajouter du code pour le `Load` événement sous la forme.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-134">Double-click Form1 to add code to the `Load` event of the form.</span></span>  
  
3.  <span data-ttu-id="3b6bc-135">Lorsque vous avez ajouté des tables au Concepteur O/R, le concepteur a ajouté un <xref:System.Data.Linq.DataContext> objet pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-135">When you added tables to the O/R Designer, the designer added a <xref:System.Data.Linq.DataContext> object for your project.</span></span> <span data-ttu-id="3b6bc-136">Cet objet contient le code dont vous devez disposer pour accéder à ces tables, en plus des collections et des objets individuels de chaque table.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-136">This object contains the code that you must have to access those tables, in addition to individual objects and collections for each table.</span></span> <span data-ttu-id="3b6bc-137">Le <xref:System.Data.Linq.DataContext> objet pour votre projet est nommé d’après le nom de votre fichier .dbml.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-137">The <xref:System.Data.Linq.DataContext> object for your project is named based on the name of your .dbml file.</span></span> <span data-ttu-id="3b6bc-138">Pour ce projet, le <xref:System.Data.Linq.DataContext> objet est nommé `northwindDataContext`.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-138">For this project, the <xref:System.Data.Linq.DataContext> object is named `northwindDataContext`.</span></span>  
  
     <span data-ttu-id="3b6bc-139">Vous pouvez créer une instance de la <xref:System.Data.Linq.DataContext> dans votre code et interroger les tables spécifiées par le Concepteur O/R.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-139">You can create an instance of the <xref:System.Data.Linq.DataContext> in your code and query the tables specified by the O/R Designer.</span></span>  
  
     <span data-ttu-id="3b6bc-140">Ajoutez le code suivant à la `Load` événement à interroger les tables qui sont exposées en tant que propriétés de votre contexte de données.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-140">Add the following code to the `Load` event to query the tables that are exposed as properties of your data context.</span></span> <span data-ttu-id="3b6bc-141">La requête filtre les résultats et retourne uniquement les clients qui sont trouvent dans `London`.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-141">The query filters the results and returns only customers that are located in `London`.</span></span>  
  
     [!code-vb[VbLINQToSQLHowTos#11](../../../../visual-basic/programming-guide/language-features/linq/codesnippet/VisualBasic/how-to-filter-query-results-by-using-linq_1.vb)]  
  
4.  <span data-ttu-id="3b6bc-142">Appuyez sur F5 pour exécuter votre projet et afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-142">Press F5 to run your project and view the results.</span></span>  
  
5.  <span data-ttu-id="3b6bc-143">Voici quelques autres filtres que vous pouvez essayer.</span><span class="sxs-lookup"><span data-stu-id="3b6bc-143">Following are some other filters that you can try.</span></span>  
  
     [!code-vb[VbLINQToSQLHowTos#12](../../../../visual-basic/programming-guide/language-features/linq/codesnippet/VisualBasic/how-to-filter-query-results-by-using-linq_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="3b6bc-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b6bc-144">See Also</span></span>  
 [<span data-ttu-id="3b6bc-145">LINQ</span><span class="sxs-lookup"><span data-stu-id="3b6bc-145">LINQ</span></span>](../../../../visual-basic/programming-guide/language-features/linq/index.md)  
 [<span data-ttu-id="3b6bc-146">Requêtes</span><span class="sxs-lookup"><span data-stu-id="3b6bc-146">Queries</span></span>](../../../../visual-basic/language-reference/queries/index.md)  
 [<span data-ttu-id="3b6bc-147">LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="3b6bc-147">LINQ to SQL</span></span>](../../../../framework/data/adonet/sql/linq/index.md)  
 [<span data-ttu-id="3b6bc-148">DataContext, méthodes (Concepteur O/R)</span><span class="sxs-lookup"><span data-stu-id="3b6bc-148">DataContext Methods (O/R Designer)</span></span>](/visualstudio/data-tools/datacontext-methods-o-r-designer)
