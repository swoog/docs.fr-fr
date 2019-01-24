---
title: 'Procédure : Appeler une procédure stockée à l’aide de LINQ (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- queries [LINQ in Visual Basic], stored procedure calls
- stored procedures sample [Visual Basic]
- stored procedures [LINQ to SQL]
- queries [LINQ in Visual Basic], how-to topics
ms.assetid: 6436d384-d1e0-40aa-8afd-451007477260
ms.openlocfilehash: bd1a3b0b163d3ab0fcc7eb9616e88c11381ff189
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54552045"
---
# <a name="how-to-call-a-stored-procedure-by-using-linq-visual-basic"></a><span data-ttu-id="92a43-102">Procédure : Appeler une procédure stockée à l’aide de LINQ (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="92a43-102">How to: Call a Stored Procedure by Using LINQ (Visual Basic)</span></span>
<span data-ttu-id="92a43-103">Language-Integrated Query (LINQ) rend plus facile d’accéder aux informations de base de données, y compris les procédures stockées comme des objets de base de données.</span><span class="sxs-lookup"><span data-stu-id="92a43-103">Language-Integrated Query (LINQ) makes it easy to access database information, including database objects such as stored procedures.</span></span>  
  
 <span data-ttu-id="92a43-104">L’exemple suivant montre comment créer une application qui appelle une procédure stockée dans une base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="92a43-104">The following example shows how to create an application that calls a stored procedure in a SQL Server database.</span></span> <span data-ttu-id="92a43-105">L’exemple montre comment appeler deux procédures stockées différentes dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="92a43-105">The sample shows how to call two different stored procedures in the database.</span></span> <span data-ttu-id="92a43-106">Chaque procédure retourne les résultats d’une requête.</span><span class="sxs-lookup"><span data-stu-id="92a43-106">Each procedure returns the results of a query.</span></span> <span data-ttu-id="92a43-107">Une procédure accepte des paramètres d’entrée, et l’autre procédure n’accepte pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="92a43-107">One procedure takes input parameters, and the other procedure does not take parameters.</span></span>  
  
 <span data-ttu-id="92a43-108">Les exemples de cette rubrique utilisent la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="92a43-108">The examples in this topic use the Northwind sample database.</span></span> <span data-ttu-id="92a43-109">Si vous n’avez pas de cette base de données sur votre ordinateur de développement, vous pouvez le télécharger à partir du Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="92a43-109">If you do not have this database on your development computer, you can download it from the Microsoft Download Center.</span></span> <span data-ttu-id="92a43-110">Pour obtenir des instructions, consultez [téléchargement d’exemples de bases de données](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md).</span><span class="sxs-lookup"><span data-stu-id="92a43-110">For instructions, see [Downloading Sample Databases](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md).</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-a-connection-to-a-database"></a><span data-ttu-id="92a43-111">Pour créer une connexion à une base de données</span><span class="sxs-lookup"><span data-stu-id="92a43-111">To create a connection to a database</span></span>  
  
1.  <span data-ttu-id="92a43-112">Dans Visual Studio, ouvrez **Explorateur de serveurs**/**Database Explorer** en cliquant sur **Explorateur de serveurs**/**base de données Explorer** sur le **vue** menu.</span><span class="sxs-lookup"><span data-stu-id="92a43-112">In Visual Studio, open **Server Explorer**/**Database Explorer** by clicking **Server Explorer**/**Database Explorer** on the **View** menu.</span></span>  
  
2.  <span data-ttu-id="92a43-113">Avec le bouton droit **des connexions de données** dans **Explorateur de serveurs**/**Database Explorer** puis cliquez sur **ajouter une connexion**.</span><span class="sxs-lookup"><span data-stu-id="92a43-113">Right-click **Data Connections** in **Server Explorer**/**Database Explorer** and then click **Add Connection**.</span></span>  
  
3.  <span data-ttu-id="92a43-114">Spécifiez une connexion valide à la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="92a43-114">Specify a valid connection to the Northwind sample database.</span></span>  
  
### <a name="to-add-a-project-that-contains-a-linq-to-sql-file"></a><span data-ttu-id="92a43-115">Pour ajouter un projet qui contient un fichier LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="92a43-115">To add a project that contains a LINQ to SQL file</span></span>  
  
1.  <span data-ttu-id="92a43-116">Dans Visual Studio, dans le menu **Fichier**,pointez sur **Nouveau**, puis cliquez sur **Projet**.</span><span class="sxs-lookup"><span data-stu-id="92a43-116">In Visual Studio, on the **File** menu, point to **New** and then click **Project**.</span></span> <span data-ttu-id="92a43-117">Sélectionnez Visual Basic **Windows Forms Application** comme type de projet.</span><span class="sxs-lookup"><span data-stu-id="92a43-117">Select Visual Basic **Windows Forms Application** as the project type.</span></span>  
  
2.  <span data-ttu-id="92a43-118">Dans le menu **Projet** , cliquez sur **Ajouter un nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="92a43-118">On the **Project** menu, click **Add New Item**.</span></span> <span data-ttu-id="92a43-119">Sélectionnez le **Classes LINQ to SQL** modèle d’élément.</span><span class="sxs-lookup"><span data-stu-id="92a43-119">Select the **LINQ to SQL Classes** item template.</span></span>  
  
3.  <span data-ttu-id="92a43-120">Nommez le fichier `northwind.dbml`.</span><span class="sxs-lookup"><span data-stu-id="92a43-120">Name the file `northwind.dbml`.</span></span> <span data-ttu-id="92a43-121">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="92a43-121">Click **Add**.</span></span> <span data-ttu-id="92a43-122">Le Concepteur Objet/Relationnel (Concepteur O/R) est ouvert pour le fichier northwind.dbml.</span><span class="sxs-lookup"><span data-stu-id="92a43-122">The Object Relational Designer (O/R Designer) is opened for the northwind.dbml file.</span></span>  
  
### <a name="to-add-stored-procedures-to-the-or-designer"></a><span data-ttu-id="92a43-123">Pour ajouter des procédures stockées au Concepteur O/R</span><span class="sxs-lookup"><span data-stu-id="92a43-123">To add stored procedures to the O/R Designer</span></span>  
  
1.  <span data-ttu-id="92a43-124">Dans **Explorateur de serveurs**/**Database Explorer**, développez la connexion à la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="92a43-124">In **Server Explorer**/**Database Explorer**, expand the connection to the Northwind database.</span></span> <span data-ttu-id="92a43-125">Développez le **Stored Procedures** dossier.</span><span class="sxs-lookup"><span data-stu-id="92a43-125">Expand the **Stored Procedures** folder.</span></span>  
  
     <span data-ttu-id="92a43-126">Si vous avez fermé le Concepteur O/R, vous pouvez le rouvrir en double-cliquant sur le fichier northwind.dbml que vous avez ajouté précédemment.</span><span class="sxs-lookup"><span data-stu-id="92a43-126">If you have closed the O/R Designer, you can reopen it by double-clicking the northwind.dbml file that you added earlier.</span></span>  
  
2.  <span data-ttu-id="92a43-127">Cliquez sur le **ventes par année** procédure stockée et faites-le glisser vers le volet droit du concepteur.</span><span class="sxs-lookup"><span data-stu-id="92a43-127">Click the **Sales by Year** stored procedure and drag it to the right pane of the designer.</span></span> <span data-ttu-id="92a43-128">Cliquez sur le **Ten Most Expensive Products** procédure stockée faites-le glisser vers le volet droit du concepteur.</span><span class="sxs-lookup"><span data-stu-id="92a43-128">Click the **Ten Most Expensive Products** stored procedure drag it to the right pane of the designer.</span></span>  
  
3.  <span data-ttu-id="92a43-129">Enregistrez vos modifications et fermez le concepteur.</span><span class="sxs-lookup"><span data-stu-id="92a43-129">Save your changes and close the designer.</span></span>  
  
4.  <span data-ttu-id="92a43-130">Enregistrez votre projet.</span><span class="sxs-lookup"><span data-stu-id="92a43-130">Save your project.</span></span>  
  
### <a name="to-add-code-to-display-the-results-of-the-stored-procedures"></a><span data-ttu-id="92a43-131">Pour ajouter du code pour afficher les résultats des procédures stockées</span><span class="sxs-lookup"><span data-stu-id="92a43-131">To add code to display the results of the stored procedures</span></span>  
  
1.  <span data-ttu-id="92a43-132">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.DataGridView> contrôle sur le formulaire de Windows par défaut pour votre projet, Form1.</span><span class="sxs-lookup"><span data-stu-id="92a43-132">From the **Toolbox**, drag a <xref:System.Windows.Forms.DataGridView> control onto the default Windows Form for your project, Form1.</span></span>  
  
2.  <span data-ttu-id="92a43-133">Double-cliquez sur Form1 pour ajouter du code à son `Load` événement.</span><span class="sxs-lookup"><span data-stu-id="92a43-133">Double-click Form1 to add code to its `Load` event.</span></span>  
  
3.  <span data-ttu-id="92a43-134">Lorsque vous avez ajouté des procédures stockées au Concepteur O/R, le concepteur a ajouté un <xref:System.Data.Linq.DataContext> objet pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="92a43-134">When you added stored procedures to the O/R Designer, the designer added a <xref:System.Data.Linq.DataContext> object for your project.</span></span> <span data-ttu-id="92a43-135">Cet objet contient le code dont vous devez disposer pour accéder à ces procédures.</span><span class="sxs-lookup"><span data-stu-id="92a43-135">This object contains the code that you must have to access those procedures.</span></span> <span data-ttu-id="92a43-136">Le <xref:System.Data.Linq.DataContext> objet pour le projet est nommé d’après le nom du fichier .dbml.</span><span class="sxs-lookup"><span data-stu-id="92a43-136">The <xref:System.Data.Linq.DataContext> object for the project is named based on the name of the .dbml file.</span></span> <span data-ttu-id="92a43-137">Pour ce projet, le <xref:System.Data.Linq.DataContext> objet est nommé `northwindDataContext`.</span><span class="sxs-lookup"><span data-stu-id="92a43-137">For this project, the <xref:System.Data.Linq.DataContext> object is named `northwindDataContext`.</span></span>  
  
     <span data-ttu-id="92a43-138">Vous pouvez créer une instance de la <xref:System.Data.Linq.DataContext> dans votre code et appeler les méthodes de la procédure stockée spécifiée par le Concepteur O/R.</span><span class="sxs-lookup"><span data-stu-id="92a43-138">You can create an instance of the <xref:System.Data.Linq.DataContext> in your code and call the stored procedure methods specified by the O/R Designer.</span></span> <span data-ttu-id="92a43-139">Pour lier à la <xref:System.Windows.Forms.DataGridView> de l’objet, vous devrez peut-être forcer la requête à exécuter immédiatement en appelant le <xref:System.Linq.Enumerable.ToList%2A> méthode sur les résultats de la procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="92a43-139">To bind to the <xref:System.Windows.Forms.DataGridView> object, you may have to force the query to execute immediately by calling the <xref:System.Linq.Enumerable.ToList%2A> method on the results of the stored procedure.</span></span>  
  
     <span data-ttu-id="92a43-140">Ajoutez le code suivant à la `Load` événements d’appeler une des procédures stockées exposées comme méthodes pour votre contexte de données.</span><span class="sxs-lookup"><span data-stu-id="92a43-140">Add the following code to the `Load` event to call either of the stored procedures exposed as methods for your data context.</span></span>  
  
     [!code-vb[VbLINQtoSQLHowTos#1](../../../../visual-basic/programming-guide/language-features/linq/codesnippet/VisualBasic/how-to-call-a-stored-procedure-by-using-linq_1.vb)]  
    [!code-vb[VbLINQtoSQLHowTos#2](../../../../visual-basic/programming-guide/language-features/linq/codesnippet/VisualBasic/how-to-call-a-stored-procedure-by-using-linq_2.vb)]  
  
4.  <span data-ttu-id="92a43-141">Appuyez sur F5 pour exécuter votre projet et afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="92a43-141">Press F5 to run your project and view the results.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="92a43-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92a43-142">See also</span></span>
- [<span data-ttu-id="92a43-143">LINQ</span><span class="sxs-lookup"><span data-stu-id="92a43-143">LINQ</span></span>](../../../../visual-basic/programming-guide/language-features/linq/index.md)
- [<span data-ttu-id="92a43-144">Requêtes</span><span class="sxs-lookup"><span data-stu-id="92a43-144">Queries</span></span>](../../../../visual-basic/language-reference/queries/index.md)
- [<span data-ttu-id="92a43-145">LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="92a43-145">LINQ to SQL</span></span>](../../../../framework/data/adonet/sql/linq/index.md)
- [<span data-ttu-id="92a43-146">DataContext, méthodes (Concepteur O/R)</span><span class="sxs-lookup"><span data-stu-id="92a43-146">DataContext Methods (O/R Designer)</span></span>](/visualstudio/data-tools/datacontext-methods-o-r-designer)
- [<span data-ttu-id="92a43-147">Guide pratique pour affecter des procédures stockées pour effectuer des mises à jour, des insertions et des suppressions (Concepteur O/R)</span><span class="sxs-lookup"><span data-stu-id="92a43-147">How to: Assign stored procedures to perform updates, inserts, and deletes (O/R Designer)</span></span>](https://msdn.microsoft.com/library/e88224ab-ff61-4a3a-b6b8-6f3694546cac)
