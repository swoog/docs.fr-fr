---
title: 'Procédure : Redimensionner automatiquement des cellules lorsque le contenu change dans le contrôle de DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- data grids [Windows Forms], resizing cells automatically
- cells [Windows Forms], resizing automatically
- DataGridView control [Windows Forms], resizing cells
ms.assetid: 1d68934d-a04c-4b12-9e66-c856c6828131
ms.openlocfilehash: c745af77b5608a7b80f96e4d4421745ea28405ad
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54592300"
---
# <a name="how-to-automatically-resize-cells-when-content-changes-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="eb858-102">Procédure : Redimensionner automatiquement des cellules lorsque le contenu change dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="eb858-102">How to: Automatically Resize Cells When Content Changes in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="eb858-103">Vous pouvez configurer le contrôle <xref:System.Windows.Forms.DataGridView> pour redimensionner ses lignes, colonnes et en-têtes automatiquement chaque fois que du contenu change, pour que les cellules soient toujours assez grandes pour afficher leurs valeurs sans être découpées.</span><span class="sxs-lookup"><span data-stu-id="eb858-103">You can configure the <xref:System.Windows.Forms.DataGridView> control to resize its rows, columns, and headers automatically whenever content changes, so that cells are always large enough to display their values without clipping.</span></span>  
  
 <span data-ttu-id="eb858-104">Vous disposez de nombreuses options pour limiter les cellules qui sont utilisées pour déterminer les nouvelles tailles.</span><span class="sxs-lookup"><span data-stu-id="eb858-104">You have many options to restrict which cells are used to determine the new sizes.</span></span> <span data-ttu-id="eb858-105">Par exemple, vous pouvez configurer le contrôle pour redimensionner automatiquement la largeur de ses colonnes uniquement en fonction des valeurs figurant sur les lignes qui sont affichées actuellement.</span><span class="sxs-lookup"><span data-stu-id="eb858-105">For example, you can configure the control to automatically resize the width of its columns based only on the values in rows that are currently displayed.</span></span> <span data-ttu-id="eb858-106">Vous optimiserez ainsi les opérations lors de l'utilisation d'un nombre de lignes, bien que dans ce cas vous souhaiterez peut-être utiliser des méthodes de dimensionnement telles que <xref:System.Windows.Forms.DataGridView.AutoResizeColumns%2A> pour ajuster la taille quand bon vous semble.</span><span class="sxs-lookup"><span data-stu-id="eb858-106">With this, you can avoid inefficiency when working with large numbers of rows, although in this case, you might want to use sizing methods such as <xref:System.Windows.Forms.DataGridView.AutoResizeColumns%2A> to adjust sizes at times of your choosing.</span></span>  
  
 <span data-ttu-id="eb858-107">Pour plus d’informations sur le redimensionnement automatique, consultez [les Options de dimensionnement dans le contrôle de DataGridView Windows Forms](../../../../docs/framework/winforms/controls/sizing-options-in-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="eb858-107">For more information about automatic resizing, see [Sizing Options in the Windows Forms DataGridView Control](../../../../docs/framework/winforms/controls/sizing-options-in-the-windows-forms-datagridview-control.md).</span></span>  
  
 <span data-ttu-id="eb858-108">L'exemple de code suivant illustre les options disponibles pour le redimensionnement automatique.</span><span class="sxs-lookup"><span data-stu-id="eb858-108">The following code example demonstrates the options available for automatic resizing.</span></span>  
  
## <a name="example"></a><span data-ttu-id="eb858-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="eb858-109">Example</span></span>  
 [!code-cpp[System.Windows.Forms.DataGridView.AutoSizing#0](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.AutoSizing/CPP/autosizing.cpp#0)]
 [!code-csharp[System.Windows.Forms.DataGridView.AutoSizing#0](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.AutoSizing/CS/autosizing.cs#0)]
 [!code-vb[System.Windows.Forms.DataGridView.AutoSizing#0](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.AutoSizing/VB/autosizing.vb#0)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="eb858-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="eb858-110">Compiling the Code</span></span>  
 <span data-ttu-id="eb858-111">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="eb858-111">This example requires:</span></span>  
  
-   <span data-ttu-id="eb858-112">Références aux assemblys System, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="eb858-112">References to the System, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
-   <span data-ttu-id="eb858-113">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="eb858-113">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="eb858-114">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="eb858-114">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="eb858-115">Voir également [Guide pratique pour Compiler et exécuter un exemple de Code complet de Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="eb858-115">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eb858-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb858-116">See also</span></span>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.ColumnHeadersHeightSizeMode%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.RowHeadersWidthSizeMode%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.AutoSizeColumnsMode%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.AutoSizeRowsMode%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.AutoSizeMode%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.InheritedAutoSizeMode%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewAutoSizeRowsMode>
- <xref:System.Windows.Forms.DataGridViewAutoSizeColumnMode>
- <xref:System.Windows.Forms.DataGridViewAutoSizeColumnsMode>
- <xref:System.Windows.Forms.DataGridViewColumnHeadersHeightSizeMode>
- <xref:System.Windows.Forms.DataGridViewRowHeadersWidthSizeMode>
- [<span data-ttu-id="eb858-117">Redimensionnement des colonnes et des lignes dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="eb858-117">Resizing Columns and Rows in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/resizing-columns-and-rows-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="eb858-118">Options de dimensionnement dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="eb858-118">Sizing Options in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/sizing-options-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="eb858-119">Guide pratique pour Redimensionner par programme les cellules en fonction du contenu dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="eb858-119">How to: Programmatically Resize Cells to Fit Content in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/programmatically-resize-cells-to-fit-content-in-the-datagrid.md)
