---
title: 'Procédure pas à pas : gestion des erreurs qui se produisent lors de l’entrée de données dans le contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- error handling [Windows Forms], dataGridView control
- data grids [Windows Forms], error handling
- DataGridView control [Windows Forms], error handling
- data entry [Windows Forms], error handling
- error handling [Windows Forms], data entry
- walkthroughs [Windows Forms], DataGridView control
ms.assetid: 30a68b85-d3af-4946-83c1-1e2d010d0511
ms.openlocfilehash: 9e803b6450fb8c9ade4adde5bf98fb1c3c62c861
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59313209"
---
# <a name="walkthrough-handling-errors-that-occur-during-data-entry-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="5bd36-102">Procédure pas à pas : gestion des erreurs qui se produisent lors de l’entrée de données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5bd36-102">Walkthrough: Handling Errors that Occur During Data Entry in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="5bd36-103">Gestion des erreurs dans le magasin de données sous-jacent sont une fonctionnalité requise pour une application de saisie de données.</span><span class="sxs-lookup"><span data-stu-id="5bd36-103">Handling errors from the underlying data store is a required feature for a data-entry application.</span></span> <span data-ttu-id="5bd36-104">Les formulaires Windows <xref:System.Windows.Forms.DataGridView> contrôle facilite cette procédure en exposant les <xref:System.Windows.Forms.DataGridView.DataError> événement, qui est déclenché lorsque le magasin de données détecte une violation de contrainte ou une règle métier.</span><span class="sxs-lookup"><span data-stu-id="5bd36-104">The Windows Forms <xref:System.Windows.Forms.DataGridView> control makes this easy by exposing the <xref:System.Windows.Forms.DataGridView.DataError> event, which is raised when the data store detects a constraint violation or a broken business rule.</span></span>  
  
 <span data-ttu-id="5bd36-105">Dans cette procédure pas à pas, vous allez récupérer des lignes à partir de la `Customers` table dans la base de données Northwind et les afficher dans un <xref:System.Windows.Forms.DataGridView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="5bd36-105">In this walkthrough, you will retrieve rows from the `Customers` table in the Northwind sample database and display them in a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="5bd36-106">Lorsqu’un doublon `CustomerID` est détectée dans une nouvelle ligne ou une ligne existante modifiée, le <xref:System.Windows.Forms.DataGridView.DataError> événement se produit, et sera géré en affichant un <xref:System.Windows.Forms.MessageBox> qui décrit l’exception.</span><span class="sxs-lookup"><span data-stu-id="5bd36-106">When a duplicate `CustomerID` value is detected in a new row or an edited existing row, the <xref:System.Windows.Forms.DataGridView.DataError> event will occur, which will be handled by displaying a <xref:System.Windows.Forms.MessageBox> that describes the exception.</span></span>  
  
 <span data-ttu-id="5bd36-107">Pour copier le code dans cette rubrique sous la forme d’une liste unique, consultez [Guide pratique pour Gérer les erreurs qui se produisent lors de la saisie de données dans les Windows Forms DataGridView Control](handle-errors-that-occur-during-data-entry-in-the-datagrid.md).</span><span class="sxs-lookup"><span data-stu-id="5bd36-107">To copy the code in this topic as a single listing, see [How to: Handle Errors That Occur During Data Entry in the Windows Forms DataGridView Control](handle-errors-that-occur-during-data-entry-in-the-datagrid.md).</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="5bd36-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="5bd36-108">Prerequisites</span></span>  
 <span data-ttu-id="5bd36-109">Pour exécuter cette procédure pas à pas, vous avez besoin des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5bd36-109">In order to complete this walkthrough, you will need:</span></span>  
  
-   <span data-ttu-id="5bd36-110">Accès à un serveur doté de la base de données Northwind SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5bd36-110">Access to a server that has the Northwind SQL Server sample database.</span></span>  
  
## <a name="creating-the-form"></a><span data-ttu-id="5bd36-111">Création du formulaire</span><span class="sxs-lookup"><span data-stu-id="5bd36-111">Creating the Form</span></span>  
  
#### <a name="to-handle-data-entry-errors-in-the-datagridview-control"></a><span data-ttu-id="5bd36-112">Pour gérer les erreurs de saisie de données dans le contrôle DataGridView</span><span class="sxs-lookup"><span data-stu-id="5bd36-112">To handle data-entry errors in the DataGridView control</span></span>  
  
1. <span data-ttu-id="5bd36-113">Créez une classe qui dérive de <xref:System.Windows.Forms.Form> et contient un <xref:System.Windows.Forms.DataGridView> contrôle et un <xref:System.Windows.Forms.BindingSource> composant.</span><span class="sxs-lookup"><span data-stu-id="5bd36-113">Create a class that derives from <xref:System.Windows.Forms.Form> and contains a <xref:System.Windows.Forms.DataGridView> control and a <xref:System.Windows.Forms.BindingSource> component.</span></span>  
  
     <span data-ttu-id="5bd36-114">L’exemple de code suivant fournit l’initialisation de base et inclut un `Main` (méthode).</span><span class="sxs-lookup"><span data-stu-id="5bd36-114">The following code example provides basic initialization and includes a `Main` method.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridView.DataError#01](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#01)]
     [!code-vb[System.Windows.Forms.DataGridView.DataError#01](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#01)]  
    [!code-csharp[System.Windows.Forms.DataGridView.DataError#02](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#02)]
    [!code-vb[System.Windows.Forms.DataGridView.DataError#02](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#02)]  
  
2. <span data-ttu-id="5bd36-115">Implémenter une méthode dans la définition de classe de votre formulaire pour gérer les détails de la connexion à la base de données.</span><span class="sxs-lookup"><span data-stu-id="5bd36-115">Implement a method in your form's class definition for handling the details of connecting to the database.</span></span>  
  
     <span data-ttu-id="5bd36-116">Cet exemple de code utilise un `GetData` méthode qui retourne un remplis <xref:System.Data.DataTable> objet.</span><span class="sxs-lookup"><span data-stu-id="5bd36-116">This code example uses a `GetData` method that returns a populated <xref:System.Data.DataTable> object.</span></span> <span data-ttu-id="5bd36-117">N’oubliez pas que vous avez défini le `connectionString` variable une valeur qui est appropriée pour votre base de données.</span><span class="sxs-lookup"><span data-stu-id="5bd36-117">Be sure that you set the `connectionString` variable to a value that is appropriate for your database.</span></span>  
  
    > [!IMPORTANT]
    >  <span data-ttu-id="5bd36-118">Le stockage d'informations sensibles (telles qu'un mot de passe) dans la chaîne de connexion peut affecter la sécurité de votre application.</span><span class="sxs-lookup"><span data-stu-id="5bd36-118">Storing sensitive information, such as a password, within the connection string can affect the security of your application.</span></span> <span data-ttu-id="5bd36-119">L'utilisation de l'authentification Windows (également appelée sécurité intégrée) offre un moyen plus sûr de contrôler l'accès à une base de données.</span><span class="sxs-lookup"><span data-stu-id="5bd36-119">Using Windows Authentication (also known as integrated security) is a more secure way to control access to a database.</span></span> <span data-ttu-id="5bd36-120">Pour plus d’informations, consultez [Protection des informations de connexion](../../data/adonet/protecting-connection-information.md).</span><span class="sxs-lookup"><span data-stu-id="5bd36-120">For more information, see [Protecting Connection Information](../../data/adonet/protecting-connection-information.md).</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridView.DataError#30](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#30)]
     [!code-vb[System.Windows.Forms.DataGridView.DataError#30](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#30)]  
  
3. <span data-ttu-id="5bd36-121">Implémenter un gestionnaire pour votre formulaire <xref:System.Windows.Forms.Form.Load> événement qui initialise le <xref:System.Windows.Forms.DataGridView> et <xref:System.Windows.Forms.BindingSource> et configure la liaison de données.</span><span class="sxs-lookup"><span data-stu-id="5bd36-121">Implement a handler for your form's <xref:System.Windows.Forms.Form.Load> event that initializes the <xref:System.Windows.Forms.DataGridView> and <xref:System.Windows.Forms.BindingSource> and sets up the data binding.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridView.DataError#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#10)]
     [!code-vb[System.Windows.Forms.DataGridView.DataError#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#10)]  
  
4. <span data-ttu-id="5bd36-122">Gérer le <xref:System.Windows.Forms.DataGridView.DataError> événement sur le <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="5bd36-122">Handle the <xref:System.Windows.Forms.DataGridView.DataError> event on the <xref:System.Windows.Forms.DataGridView>.</span></span>  
  
     <span data-ttu-id="5bd36-123">Si le contexte de l’erreur est une opération de validation, afficher l’erreur dans un <xref:System.Windows.Forms.MessageBox>.</span><span class="sxs-lookup"><span data-stu-id="5bd36-123">If the context for the error is a commit operation, display the error in a <xref:System.Windows.Forms.MessageBox>.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridView.DataError#20](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#20)]
     [!code-vb[System.Windows.Forms.DataGridView.DataError#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#20)]  
  
## <a name="testing-the-application"></a><span data-ttu-id="5bd36-124">Test de l'application</span><span class="sxs-lookup"><span data-stu-id="5bd36-124">Testing the Application</span></span>  
 <span data-ttu-id="5bd36-125">Vous pouvez maintenant tester le formulaire pour vous assurer qu’il se comporte comme prévu.</span><span class="sxs-lookup"><span data-stu-id="5bd36-125">You can now test the form to make sure it behaves as expected.</span></span>  
  
#### <a name="to-test-the-form"></a><span data-ttu-id="5bd36-126">Pour tester le formulaire</span><span class="sxs-lookup"><span data-stu-id="5bd36-126">To test the form</span></span>  
  
-   <span data-ttu-id="5bd36-127">Appuyez sur F5 pour exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="5bd36-127">Press F5 to run the application.</span></span>  
  
     <span data-ttu-id="5bd36-128">Vous verrez un <xref:System.Windows.Forms.DataGridView> contrôle rempli avec des données à partir de la table Customers.</span><span class="sxs-lookup"><span data-stu-id="5bd36-128">You will see a <xref:System.Windows.Forms.DataGridView> control filled with data from the Customers table.</span></span> <span data-ttu-id="5bd36-129">Si vous entrez une valeur en double pour `CustomerID` et valider la modification, la valeur de cellule reprendra automatiquement et vous verrez un <xref:System.Windows.Forms.MessageBox> qui affiche l’erreur de saisie de données.</span><span class="sxs-lookup"><span data-stu-id="5bd36-129">If you enter a duplicate value for `CustomerID` and commit the edit, the cell value will revert automatically and you will see a <xref:System.Windows.Forms.MessageBox> that displays the data entry error.</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="5bd36-130">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="5bd36-130">Next Steps</span></span>  
 <span data-ttu-id="5bd36-131">Cette application vous donne une connaissance élémentaire de la <xref:System.Windows.Forms.DataGridView> fonctionnalités du contrôle.</span><span class="sxs-lookup"><span data-stu-id="5bd36-131">This application gives you a basic understanding of the <xref:System.Windows.Forms.DataGridView> control's capabilities.</span></span> <span data-ttu-id="5bd36-132">Vous pouvez personnaliser l’apparence et le comportement de la <xref:System.Windows.Forms.DataGridView> contrôle de plusieurs manières :</span><span class="sxs-lookup"><span data-stu-id="5bd36-132">You can customize the appearance and behavior of the <xref:System.Windows.Forms.DataGridView> control in several ways:</span></span>  
  
-   <span data-ttu-id="5bd36-133">Modifier les styles de bordure et en-tête.</span><span class="sxs-lookup"><span data-stu-id="5bd36-133">Change border and header styles.</span></span> <span data-ttu-id="5bd36-134">Pour plus d'informations, voir [Procédure : Modifier la bordure et de Styles de quadrillage dans les Windows Forms DataGridView Control](change-the-border-and-gridline-styles-in-the-datagrid.md).</span><span class="sxs-lookup"><span data-stu-id="5bd36-134">For more information, see [How to: Change the Border and Gridline Styles in the Windows Forms DataGridView Control](change-the-border-and-gridline-styles-in-the-datagrid.md).</span></span>  
  
-   <span data-ttu-id="5bd36-135">Activer ou restreindre l’entrée utilisateur et le <xref:System.Windows.Forms.DataGridView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="5bd36-135">Enable or restrict user input to the <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="5bd36-136">Pour plus d'informations, voir [Procédure : Empêcher l’ajout de ligne et de suppression dans les Windows Forms DataGridView Control](prevent-row-addition-and-deletion-datagridview.md), et [Comment : Définir une colonne en lecture seule dans les Windows Forms DataGridView Control](how-to-make-columns-read-only-in-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="5bd36-136">For more information, see [How to: Prevent Row Addition and Deletion in the Windows Forms DataGridView Control](prevent-row-addition-and-deletion-datagridview.md), and [How to: Make Columns Read-Only in the Windows Forms DataGridView Control](how-to-make-columns-read-only-in-the-windows-forms-datagridview-control.md).</span></span>  
  
-   <span data-ttu-id="5bd36-137">Valider l’entrée utilisateur pour le <xref:System.Windows.Forms.DataGridView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="5bd36-137">Validate user input to the <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="5bd36-138">Pour plus d’informations, consultez [Procédure pas à pas : Validation des données dans les Windows Forms DataGridView Control](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="5bd36-138">For more information, see [Walkthrough: Validating Data in the Windows Forms DataGridView Control](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md).</span></span>  
  
-   <span data-ttu-id="5bd36-139">Gérer des jeux de données très volumineux à l’aide du mode virtuel.</span><span class="sxs-lookup"><span data-stu-id="5bd36-139">Handle very large data sets using virtual mode.</span></span> <span data-ttu-id="5bd36-140">Pour plus d’informations, consultez [Procédure pas à pas : Implémentation du Mode virtuel dans les Windows Forms DataGridView Control](implementing-virtual-mode-wf-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="5bd36-140">For more information, see [Walkthrough: Implementing Virtual Mode in the Windows Forms DataGridView Control](implementing-virtual-mode-wf-datagridview-control.md).</span></span>  
  
-   <span data-ttu-id="5bd36-141">Personnaliser l’apparence des cellules.</span><span class="sxs-lookup"><span data-stu-id="5bd36-141">Customize the appearance of cells.</span></span> <span data-ttu-id="5bd36-142">Pour plus d'informations, voir [Procédure : Personnaliser l’apparence des cellules dans le contrôle de DataGridView Windows Forms](customize-the-appearance-of-cells-in-the-datagrid.md) et [Comment : Définir des Styles de cellules par défaut pour les Windows Forms DataGridView Control](how-to-set-default-cell-styles-for-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="5bd36-142">For more information, see [How to: Customize the Appearance of Cells in the Windows Forms DataGridView Control](customize-the-appearance-of-cells-in-the-datagrid.md) and [How to: Set Default Cell Styles for the Windows Forms DataGridView Control](how-to-set-default-cell-styles-for-the-windows-forms-datagridview-control.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5bd36-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bd36-143">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [<span data-ttu-id="5bd36-144">Saisie de données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5bd36-144">Data Entry in the Windows Forms DataGridView Control</span></span>](data-entry-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="5bd36-145">Procédure : gérer les erreurs qui se produisent lors de l’entrée de données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5bd36-145">How to: Handle Errors That Occur During Data Entry in the Windows Forms DataGridView Control</span></span>](handle-errors-that-occur-during-data-entry-in-the-datagrid.md)
- [<span data-ttu-id="5bd36-146">Procédure pas à pas : validation des données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5bd36-146">Walkthrough: Validating Data in the Windows Forms DataGridView Control</span></span>](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="5bd36-147">Protection des informations de connexion</span><span class="sxs-lookup"><span data-stu-id="5bd36-147">Protecting Connection Information</span></span>](../../data/adonet/protecting-connection-information.md)
