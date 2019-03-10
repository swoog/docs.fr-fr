---
title: 'Procédure : Lier des objets aux contrôles DataGridView de Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], object binding
- data grids [Windows Forms], object binding
- object binding [Windows Forms], DataGridView control
ms.assetid: cb8f29fa-577e-4e2b-883f-3a01c6189b9c
ms.openlocfilehash: 9f3ce61b3692f0b83298bdf9a19cb98fb5d5ab7f
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57723801"
---
# <a name="how-to-bind-objects-to-windows-forms-datagridview-controls"></a><span data-ttu-id="9ff81-102">Procédure : Lier des objets aux contrôles DataGridView de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9ff81-102">How to: Bind Objects to Windows Forms DataGridView Controls</span></span>
<span data-ttu-id="9ff81-103">L'exemple de code suivant montre comment lier une collection d'objets à un contrôle <xref:System.Windows.Forms.DataGridView> pour que chaque objet soit affichée sur une ligne distincte.</span><span class="sxs-lookup"><span data-stu-id="9ff81-103">The following code example demonstrates how to bind a collection of objects to a <xref:System.Windows.Forms.DataGridView> control so that each object displays as a separate row.</span></span> <span data-ttu-id="9ff81-104">Cet exemple illustre également comment afficher une propriété avec un type énumération dans un <xref:System.Windows.Forms.DataGridViewComboBoxColumn> pour que la zone de liste déroulante modifiable contienne les valeurs d'énumération.</span><span class="sxs-lookup"><span data-stu-id="9ff81-104">This example also illustrates how to display a property with an enumeration type in a <xref:System.Windows.Forms.DataGridViewComboBoxColumn> so that the combo box drop-down list contains the enumeration values.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9ff81-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="9ff81-105">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridView._CollectionBound#00](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView._CollectionBound/CS/collectionbound.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridView._CollectionBound#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView._CollectionBound/VB/collectionbound.vb#00)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="9ff81-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="9ff81-106">Compiling the Code</span></span>  
 <span data-ttu-id="9ff81-107">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="9ff81-107">This example requires:</span></span>  
  
-   <span data-ttu-id="9ff81-108">des références aux assemblys System et System.Windows.Forms ;</span><span class="sxs-lookup"><span data-stu-id="9ff81-108">References to the System and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="9ff81-109">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="9ff81-109">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="9ff81-110">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="9ff81-110">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ff81-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ff81-111">See also</span></span>
- <xref:System.Windows.Forms.DataGridView>
- [<span data-ttu-id="9ff81-112">Affichage des données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9ff81-112">Displaying Data in the Windows Forms DataGridView Control</span></span>](displaying-data-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="9ff81-113">Guide pratique pour Accéder aux objets liés à des Windows Forms DataGridView lignes</span><span class="sxs-lookup"><span data-stu-id="9ff81-113">How to: Access Objects Bound to Windows Forms DataGridView Rows</span></span>](how-to-access-objects-bound-to-windows-forms-datagridview-rows.md)
