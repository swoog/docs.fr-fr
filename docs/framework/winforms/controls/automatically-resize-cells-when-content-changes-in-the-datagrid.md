---
title: 'Procédure : redimensionner automatiquement les cellules quand le contenu change dans le contrôle DataGridView Windows Forms'
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
ms.openlocfilehash: 7acd7777ede726b9dfed2b821e4248a0ebf7797f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59182492"
---
# <a name="how-to-automatically-resize-cells-when-content-changes-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="2f677-102">Procédure : redimensionner automatiquement les cellules quand le contenu change dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2f677-102">How to: Automatically Resize Cells When Content Changes in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="2f677-103">Vous pouvez configurer le contrôle <xref:System.Windows.Forms.DataGridView> pour redimensionner ses lignes, colonnes et en-têtes automatiquement chaque fois que du contenu change, pour que les cellules soient toujours assez grandes pour afficher leurs valeurs sans être découpées.</span><span class="sxs-lookup"><span data-stu-id="2f677-103">You can configure the <xref:System.Windows.Forms.DataGridView> control to resize its rows, columns, and headers automatically whenever content changes, so that cells are always large enough to display their values without clipping.</span></span>  
  
 <span data-ttu-id="2f677-104">Vous disposez de nombreuses options pour limiter les cellules qui sont utilisées pour déterminer les nouvelles tailles.</span><span class="sxs-lookup"><span data-stu-id="2f677-104">You have many options to restrict which cells are used to determine the new sizes.</span></span> <span data-ttu-id="2f677-105">Par exemple, vous pouvez configurer le contrôle pour redimensionner automatiquement la largeur de ses colonnes uniquement en fonction des valeurs figurant sur les lignes qui sont affichées actuellement.</span><span class="sxs-lookup"><span data-stu-id="2f677-105">For example, you can configure the control to automatically resize the width of its columns based only on the values in rows that are currently displayed.</span></span> <span data-ttu-id="2f677-106">Vous optimiserez ainsi les opérations lors de l'utilisation d'un nombre de lignes, bien que dans ce cas vous souhaiterez peut-être utiliser des méthodes de dimensionnement telles que <xref:System.Windows.Forms.DataGridView.AutoResizeColumns%2A> pour ajuster la taille quand bon vous semble.</span><span class="sxs-lookup"><span data-stu-id="2f677-106">With this, you can avoid inefficiency when working with large numbers of rows, although in this case, you might want to use sizing methods such as <xref:System.Windows.Forms.DataGridView.AutoResizeColumns%2A> to adjust sizes at times of your choosing.</span></span>  
  
 <span data-ttu-id="2f677-107">Pour plus d’informations sur le redimensionnement automatique, consultez [les Options de dimensionnement dans le contrôle de DataGridView Windows Forms](sizing-options-in-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="2f677-107">For more information about automatic resizing, see [Sizing Options in the Windows Forms DataGridView Control](sizing-options-in-the-windows-forms-datagridview-control.md).</span></span>  
  
 <span data-ttu-id="2f677-108">L'exemple de code suivant illustre les options disponibles pour le redimensionnement automatique.</span><span class="sxs-lookup"><span data-stu-id="2f677-108">The following code example demonstrates the options available for automatic resizing.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2f677-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="2f677-109">Example</span></span>  
 [!code-cpp[System.Windows.Forms.DataGridView.AutoSizing#0](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.AutoSizing/CPP/autosizing.cpp#0)]
 [!code-csharp[System.Windows.Forms.DataGridView.AutoSizing#0](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.AutoSizing/CS/autosizing.cs#0)]
 [!code-vb[System.Windows.Forms.DataGridView.AutoSizing#0](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.AutoSizing/VB/autosizing.vb#0)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="2f677-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="2f677-110">Compiling the Code</span></span>  
 <span data-ttu-id="2f677-111">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="2f677-111">This example requires:</span></span>  
  
-   <span data-ttu-id="2f677-112">Références aux assemblys System, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="2f677-112">References to the System, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
-   <span data-ttu-id="2f677-113">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="2f677-113">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="2f677-114">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="2f677-114">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2f677-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f677-115">See also</span></span>

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
- [<span data-ttu-id="2f677-116">Redimensionnement des colonnes et des lignes dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2f677-116">Resizing Columns and Rows in the Windows Forms DataGridView Control</span></span>](resizing-columns-and-rows-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="2f677-117">Options de dimensionnement dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2f677-117">Sizing Options in the Windows Forms DataGridView Control</span></span>](sizing-options-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="2f677-118">Procédure : redimensionner par programmation des cellules pour les adapter au contenu du contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2f677-118">How to: Programmatically Resize Cells to Fit Content in the Windows Forms DataGridView Control</span></span>](programmatically-resize-cells-to-fit-content-in-the-datagrid.md)
