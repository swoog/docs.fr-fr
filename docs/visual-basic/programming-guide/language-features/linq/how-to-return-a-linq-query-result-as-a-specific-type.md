---
title: 'Procédure : Retourner un résultat de requête LINQ comme un Type spécifique (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- queries [LINQ in Visual Basic], specific type returned
- projection [LINQ in Visual Basic]
- anonymous types [Visual Basic]
- querying databases [LINQ]
- queries [LINQ in Visual Basic], how-to topics
- query samples [Visual Basic]
ms.assetid: 621bb10a-e5d7-44fb-a025-317964b19d92
ms.openlocfilehash: 7d281de2005f1ee9227b3e3496125c8af9acba35
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54500614"
---
# <a name="how-to-return-a-linq-query-result-as-a-specific-type-visual-basic"></a><span data-ttu-id="34965-102">Procédure : Retourner un résultat de requête LINQ comme un Type spécifique (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="34965-102">How to: Return a LINQ Query Result as a Specific Type (Visual Basic)</span></span>
<span data-ttu-id="34965-103">Language-Integrated Query (LINQ) facilite l’accès aux informations de base de données et exécuter des requêtes.</span><span class="sxs-lookup"><span data-stu-id="34965-103">Language-Integrated Query (LINQ) makes it easy to access database information and execute queries.</span></span> <span data-ttu-id="34965-104">Par défaut, les requêtes LINQ retournent une liste d’objets comme un type anonyme.</span><span class="sxs-lookup"><span data-stu-id="34965-104">By default, LINQ queries return a list of objects as an anonymous type.</span></span> <span data-ttu-id="34965-105">Vous pouvez également spécifier qu’une requête retourne une liste d’un type spécifique à l’aide de la `Select` clause.</span><span class="sxs-lookup"><span data-stu-id="34965-105">You can also specify that a query return a list of a specific type by using the `Select` clause.</span></span>  
  
 <span data-ttu-id="34965-106">L’exemple suivant montre comment créer une application qui effectue des requêtes sur une base de données SQL Server et projette les résultats comme un type nommé spécifique.</span><span class="sxs-lookup"><span data-stu-id="34965-106">The following example shows how to create a new application that performs queries against a SQL Server database and projects the results as a specific named type.</span></span> <span data-ttu-id="34965-107">Pour plus d’informations, consultez [Types anonymes](../../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md) et [Clause Select](../../../../visual-basic/language-reference/queries/select-clause.md).</span><span class="sxs-lookup"><span data-stu-id="34965-107">For more information, see [Anonymous Types](../../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md) and [Select Clause](../../../../visual-basic/language-reference/queries/select-clause.md).</span></span>  
  
 <span data-ttu-id="34965-108">Les exemples de cette rubrique utilisent la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="34965-108">The examples in this topic use the Northwind sample database.</span></span> <span data-ttu-id="34965-109">Si vous n’avez pas de cette base de données sur votre ordinateur de développement, vous pouvez le télécharger à partir du Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="34965-109">If you do not have this database on your development computer, you can download it from the Microsoft Download Center.</span></span> <span data-ttu-id="34965-110">Pour obtenir des instructions, consultez [téléchargement d’exemples de bases de données](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md).</span><span class="sxs-lookup"><span data-stu-id="34965-110">For instructions, see [Downloading Sample Databases](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md).</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-a-connection-to-a-database"></a><span data-ttu-id="34965-111">Pour créer une connexion à une base de données</span><span class="sxs-lookup"><span data-stu-id="34965-111">To create a connection to a database</span></span>  
  
1.  <span data-ttu-id="34965-112">Dans Visual Studio, ouvrez **Explorateur de serveurs**/**Database Explorer** en cliquant sur **Explorateur de serveurs**/**base de données Explorer** sur le **vue** menu.</span><span class="sxs-lookup"><span data-stu-id="34965-112">In Visual Studio, open **Server Explorer**/**Database Explorer** by clicking **Server Explorer**/**Database Explorer** on the **View** menu.</span></span>  
  
2.  <span data-ttu-id="34965-113">Avec le bouton droit **des connexions de données** dans **Explorateur de serveurs**/**Database Explorer** puis cliquez sur **ajouter une connexion**.</span><span class="sxs-lookup"><span data-stu-id="34965-113">Right-click **Data Connections** in **Server Explorer**/**Database Explorer** and then click **Add Connection**.</span></span>  
  
3.  <span data-ttu-id="34965-114">Spécifiez une connexion valide à la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="34965-114">Specify a valid connection to the Northwind sample database.</span></span>  
  
### <a name="to-add-a-project-that-contains-a-linq-to-sql-file"></a><span data-ttu-id="34965-115">Pour ajouter un projet qui contient un fichier LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="34965-115">To add a project that contains a LINQ to SQL file</span></span>  
  
1.  <span data-ttu-id="34965-116">Dans Visual Studio, dans le menu **Fichier**,pointez sur **Nouveau**, puis cliquez sur **Projet**.</span><span class="sxs-lookup"><span data-stu-id="34965-116">In Visual Studio, on the **File** menu, point to **New** and then click **Project**.</span></span> <span data-ttu-id="34965-117">Sélectionnez Visual Basic **Windows Forms Application** comme type de projet.</span><span class="sxs-lookup"><span data-stu-id="34965-117">Select Visual Basic **Windows Forms Application** as the project type.</span></span>  
  
2.  <span data-ttu-id="34965-118">Dans le menu **Projet** , cliquez sur **Ajouter un nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="34965-118">On the **Project** menu, click **Add New Item**.</span></span> <span data-ttu-id="34965-119">Sélectionnez le **Classes LINQ to SQL** modèle d’élément.</span><span class="sxs-lookup"><span data-stu-id="34965-119">Select the **LINQ to SQL Classes** item template.</span></span>  
  
3.  <span data-ttu-id="34965-120">Nommez le fichier `northwind.dbml`.</span><span class="sxs-lookup"><span data-stu-id="34965-120">Name the file `northwind.dbml`.</span></span> <span data-ttu-id="34965-121">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="34965-121">Click **Add**.</span></span> <span data-ttu-id="34965-122">Le Concepteur Objet/Relationnel (Concepteur O/R) est ouvert pour le fichier northwind.dbml.</span><span class="sxs-lookup"><span data-stu-id="34965-122">The Object Relational Designer (O/R Designer) is opened for the northwind.dbml file.</span></span>  
  
### <a name="to-add-tables-to-query-to-the-or-designer"></a><span data-ttu-id="34965-123">Pour ajouter des tables à interroger au Concepteur O/R</span><span class="sxs-lookup"><span data-stu-id="34965-123">To add tables to query to the O/R Designer</span></span>  
  
1.  <span data-ttu-id="34965-124">Dans **Explorateur de serveurs**/**Database Explorer**, développez la connexion à la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="34965-124">In **Server Explorer**/**Database Explorer**, expand the connection to the Northwind database.</span></span> <span data-ttu-id="34965-125">Développez le **Tables** dossier.</span><span class="sxs-lookup"><span data-stu-id="34965-125">Expand the **Tables** folder.</span></span>  
  
     <span data-ttu-id="34965-126">Si vous avez fermé le Concepteur O/R, vous pouvez le rouvrir en double-cliquant sur le fichier northwind.dbml que vous avez ajouté précédemment.</span><span class="sxs-lookup"><span data-stu-id="34965-126">If you have closed the O/R Designer, you can reopen it by double-clicking the northwind.dbml file that you added earlier.</span></span>  
  
2.  <span data-ttu-id="34965-127">Cliquez sur la table Customers et faites-le glisser vers le volet gauche du concepteur.</span><span class="sxs-lookup"><span data-stu-id="34965-127">Click the Customers table and drag it to the left pane of the designer.</span></span>  
  
     <span data-ttu-id="34965-128">Le concepteur crée un nouveau `Customer` objet pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="34965-128">The designer creates a new `Customer` object for your project.</span></span> <span data-ttu-id="34965-129">Vous pouvez projeter un résultat de requête le `Customer` type ou en tant que type que vous créez.</span><span class="sxs-lookup"><span data-stu-id="34965-129">You can project a query result as the `Customer` type or as a type that you create.</span></span> <span data-ttu-id="34965-130">Cet exemple crée un nouveau type dans une procédure ultérieure et un résultat de requête en tant que type de projet.</span><span class="sxs-lookup"><span data-stu-id="34965-130">This sample will create a new type in a later procedure and project a query result as that type.</span></span>  
  
3.  <span data-ttu-id="34965-131">Enregistrez vos modifications et fermez le concepteur.</span><span class="sxs-lookup"><span data-stu-id="34965-131">Save your changes and close the designer.</span></span>  
  
4.  <span data-ttu-id="34965-132">Enregistrez votre projet.</span><span class="sxs-lookup"><span data-stu-id="34965-132">Save your project.</span></span>  
  
### <a name="to-add-code-to-query-the-database-and-display-the-results"></a><span data-ttu-id="34965-133">Pour ajouter du code pour interroger la base de données et afficher les résultats</span><span class="sxs-lookup"><span data-stu-id="34965-133">To add code to query the database and display the results</span></span>  
  
1.  <span data-ttu-id="34965-134">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.DataGridView> contrôle sur le formulaire de Windows par défaut pour votre projet, Form1.</span><span class="sxs-lookup"><span data-stu-id="34965-134">From the **Toolbox**, drag a <xref:System.Windows.Forms.DataGridView> control onto the default Windows Form for your project, Form1.</span></span>  
  
2.  <span data-ttu-id="34965-135">Double-cliquez sur Form1 pour modifier la classe Form1.</span><span class="sxs-lookup"><span data-stu-id="34965-135">Double-click Form1 to modify the Form1 class.</span></span>  
  
3.  <span data-ttu-id="34965-136">Après le `End Class` instruction de la classe Form1, ajoutez le code suivant pour créer un `CustomerInfo` type pour stocker les résultats de requête pour cet exemple.</span><span class="sxs-lookup"><span data-stu-id="34965-136">After the `End Class` statement of the Form1 class, add the following code to create a `CustomerInfo` type to hold the query results for this sample.</span></span>  
  
     [!code-vb[VbLINQToSQLHowTos#16](../../../../visual-basic/programming-guide/language-features/linq/codesnippet/VisualBasic/how-to-return-a-linq-query-result-as-a-specific-type_1.vb)]  
  
4.  <span data-ttu-id="34965-137">Lorsque vous avez ajouté des tables au Concepteur O/R, le concepteur a ajouté un <xref:System.Data.Linq.DataContext> objet à votre projet.</span><span class="sxs-lookup"><span data-stu-id="34965-137">When you added tables to the O/R Designer, the designer added a <xref:System.Data.Linq.DataContext> object to your project.</span></span> <span data-ttu-id="34965-138">Cet objet contient le code que vous devez disposer pour accéder à ces tables et pour accéder aux collections et des objets individuels de chaque table.</span><span class="sxs-lookup"><span data-stu-id="34965-138">This object contains the code that you must have to access those tables, and to access individual objects and collections for each table.</span></span> <span data-ttu-id="34965-139">Le <xref:System.Data.Linq.DataContext> objet pour votre projet est nommé d’après le nom de votre fichier .dbml.</span><span class="sxs-lookup"><span data-stu-id="34965-139">The <xref:System.Data.Linq.DataContext> object for your project is named based on the name of your .dbml file.</span></span> <span data-ttu-id="34965-140">Pour ce projet, le <xref:System.Data.Linq.DataContext> objet est nommé `northwindDataContext`.</span><span class="sxs-lookup"><span data-stu-id="34965-140">For this project, the <xref:System.Data.Linq.DataContext> object is named `northwindDataContext`.</span></span>  
  
     <span data-ttu-id="34965-141">Vous pouvez créer une instance de la <xref:System.Data.Linq.DataContext> dans votre code et interroger les tables spécifiées par le Concepteur O/R.</span><span class="sxs-lookup"><span data-stu-id="34965-141">You can create an instance of the <xref:System.Data.Linq.DataContext> in your code and query the tables specified by the O/R Designer.</span></span>  
  
     <span data-ttu-id="34965-142">Dans le `Load` événement de la classe Form1, ajoutez le code suivant pour interroger les tables qui sont exposées en tant que propriétés de votre contexte de données.</span><span class="sxs-lookup"><span data-stu-id="34965-142">In the `Load` event of the Form1 class, add the following code to query the tables that are exposed as properties of your data context.</span></span> <span data-ttu-id="34965-143">Le `Select` clause de la requête créera un nouveau `CustomerInfo` type plutôt qu’un type anonyme pour chaque élément du résultat de requête.</span><span class="sxs-lookup"><span data-stu-id="34965-143">The `Select` clause of the query will create a new `CustomerInfo` type instead of an anonymous type for each item of the query result.</span></span>  
  
     [!code-vb[VbLINQToSQLHowTos#15](../../../../visual-basic/programming-guide/language-features/linq/codesnippet/VisualBasic/how-to-return-a-linq-query-result-as-a-specific-type_2.vb)]  
  
5.  <span data-ttu-id="34965-144">Appuyez sur F5 pour exécuter votre projet et afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="34965-144">Press F5 to run your project and view the results.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="34965-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34965-145">See also</span></span>
- [<span data-ttu-id="34965-146">LINQ</span><span class="sxs-lookup"><span data-stu-id="34965-146">LINQ</span></span>](../../../../visual-basic/programming-guide/language-features/linq/index.md)
- [<span data-ttu-id="34965-147">Requêtes</span><span class="sxs-lookup"><span data-stu-id="34965-147">Queries</span></span>](../../../../visual-basic/language-reference/queries/index.md)
- [<span data-ttu-id="34965-148">LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="34965-148">LINQ to SQL</span></span>](../../../../framework/data/adonet/sql/linq/index.md)
- [<span data-ttu-id="34965-149">DataContext, méthodes (Concepteur O/R)</span><span class="sxs-lookup"><span data-stu-id="34965-149">DataContext Methods (O/R Designer)</span></span>](/visualstudio/data-tools/datacontext-methods-o-r-designer)
