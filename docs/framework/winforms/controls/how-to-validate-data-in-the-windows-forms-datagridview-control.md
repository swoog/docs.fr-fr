---
title: 'Procédure : valider les données dans le contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data [Windows Forms], validation
- DataGridView control [Windows Forms], data validation
- data grids [Windows Forms], validating data
- data validation [Windows Forms], Windows Forms
ms.assetid: d10aef35-701e-4a3c-a684-2a2ed1aeaca6
ms.openlocfilehash: dae254c14790841b37162fca9f998be429006125
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61785734"
---
# <a name="how-to-validate-data-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="93c61-102">Procédure : valider les données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="93c61-102">How to: Validate Data in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="93c61-103">L'exemple de code suivant montre comment valider les données entrées par un utilisateur dans un contrôle <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="93c61-103">The following code example demonstrates how to validate data entered by a user into a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="93c61-104">Dans cet exemple, le <xref:System.Windows.Forms.DataGridView> est rempli avec des lignes de la table `Customers` de la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="93c61-104">In this example, the <xref:System.Windows.Forms.DataGridView> is populated with rows from the `Customers` table of the Northwind sample database.</span></span> <span data-ttu-id="93c61-105">Quand l'utilisateur modifie une cellule dans la colonne `CompanyName`, la validité de sa valeur est testée en vérifiant qu'elle n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="93c61-105">When the user edits a cell in the `CompanyName` column, its value is tested for validity by checking that it is not empty.</span></span> <span data-ttu-id="93c61-106">Si le gestionnaire d'événements de l'événement <xref:System.Windows.Forms.DataGridView.CellValidating> détecte que la valeur est une chaîne vide, le <xref:System.Windows.Forms.DataGridView> empêche l'utilisateur de quitter la cellule tant qu'il n'a pas entré une chaîne non vide.</span><span class="sxs-lookup"><span data-stu-id="93c61-106">If the event handler for the <xref:System.Windows.Forms.DataGridView.CellValidating> event finds that the value is an empty string, the <xref:System.Windows.Forms.DataGridView> prevents the user from exiting the cell until a non-empty string is entered.</span></span>  
  
 <span data-ttu-id="93c61-107">Pour obtenir une explication complète de cet exemple de code, consultez [procédure pas à pas : Validation des données dans les Windows Forms DataGridView Control](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="93c61-107">For a complete explanation of this code example, see [Walkthrough: Validating Data in the Windows Forms DataGridView Control](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="93c61-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="93c61-108">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewDataValidation#00](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/CS/datavalidation.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewDataValidation#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/VB/datavalidation.vb#00)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="93c61-109">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="93c61-109">Compiling the Code</span></span>  
 <span data-ttu-id="93c61-110">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="93c61-110">This example requires:</span></span>  
  
- <span data-ttu-id="93c61-111">Références aux assemblys System, System.Data, System.Windows.Forms et System.XML.</span><span class="sxs-lookup"><span data-stu-id="93c61-111">References to the System, System.Data, System.Windows.Forms and System.XML assemblies.</span></span>  
  
 <span data-ttu-id="93c61-112">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="93c61-112">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="93c61-113">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="93c61-113">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="93c61-114">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="93c61-114">.NET Framework Security</span></span>  
 <span data-ttu-id="93c61-115">Le stockage d'informations sensibles (telles qu'un mot de passe) dans la chaîne de connexion peut affecter la sécurité de votre application.</span><span class="sxs-lookup"><span data-stu-id="93c61-115">Storing sensitive information, such as a password, within the connection string can affect the security of your application.</span></span> <span data-ttu-id="93c61-116">L'utilisation de l'authentification Windows (également appelée sécurité intégrée) offre un moyen plus sûr de contrôler l'accès à une base de données.</span><span class="sxs-lookup"><span data-stu-id="93c61-116">Using Windows Authentication (also known as integrated security) is a more secure way to control access to a database.</span></span> <span data-ttu-id="93c61-117">Pour plus d’informations, consultez [Protection des informations de connexion](../../data/adonet/protecting-connection-information.md).</span><span class="sxs-lookup"><span data-stu-id="93c61-117">For more information, see [Protecting Connection Information](../../data/adonet/protecting-connection-information.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93c61-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93c61-118">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [<span data-ttu-id="93c61-119">Procédure pas à pas : Validation des données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="93c61-119">Walkthrough: Validating Data in the Windows Forms DataGridView Control</span></span>](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="93c61-120">Saisie de données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="93c61-120">Data Entry in the Windows Forms DataGridView Control</span></span>](data-entry-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="93c61-121">Procédure pas à pas : Gestion des erreurs qui se produisent lors de la saisie de données dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="93c61-121">Walkthrough: Handling Errors that Occur During Data Entry in the Windows Forms DataGridView Control</span></span>](handling-errors-that-occur-during-data-entry-in-the-datagrid.md)
- [<span data-ttu-id="93c61-122">Protection des informations de connexion</span><span class="sxs-lookup"><span data-stu-id="93c61-122">Protecting Connection Information</span></span>](../../data/adonet/protecting-connection-information.md)
