---
title: 'Procédure : personnaliser la mise en forme des données dans le contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], formatting data
- DataGridView control [Windows Forms], cell styles
- cells [Windows Forms], changing colors in DataGridView control [Windows Forms]
- colors [Windows Forms], changing in DataGridView control [Windows Forms]
- data [Windows Forms], formatting in DataGridView control
- DataGridView control [Windows Forms], cell customization
- DataGridView control [Windows Forms], changing cell colors
- Windows Forms, changing colors of DataGridView cells
- DataGridView control [Windows Forms], substituting cell values for display
- data grids [Windows Forms], formatting data
ms.assetid: a6e72c70-ce18-425f-828d-d57be6f96ab6
ms.openlocfilehash: dfd02e3e575c06bf7c37720fa3d6ecf4a3193491
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64666380"
---
# <a name="how-to-customize-data-formatting-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="2527e-102">Procédure : personnaliser la mise en forme des données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2527e-102">How to: Customize Data Formatting in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="2527e-103">L'exemple de code suivant montre comment implémenter un gestionnaire pour l'événement <xref:System.Windows.Forms.DataGridView.CellFormatting?displayProperty=nameWithType> qui modifie le mode d'affichage des cellules en fonction de leurs colonnes et de leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="2527e-103">The following code example demonstrates how to implement a handler for the <xref:System.Windows.Forms.DataGridView.CellFormatting?displayProperty=nameWithType> event that changes how cells are displayed depending on their columns and values.</span></span>  
  
 <span data-ttu-id="2527e-104">Les cellules de la colonne `Balance` qui contiennent des nombres négatifs ont un arrière-plan rouge.</span><span class="sxs-lookup"><span data-stu-id="2527e-104">Cells in the `Balance` column that contain negative numbers are given a red background.</span></span> <span data-ttu-id="2527e-105">Vous pouvez également appliquer la mise en forme « Monnaie » à ces cellules pour afficher les valeurs négatives entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="2527e-105">You can also format these cells as currency to display parentheses around negative values.</span></span> <span data-ttu-id="2527e-106">Pour plus d'informations, voir [Procédure : Format des données dans les Windows Forms DataGridView Control](how-to-format-data-in-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="2527e-106">For more information, see [How to: Format Data in the Windows Forms DataGridView Control](how-to-format-data-in-the-windows-forms-datagridview-control.md).</span></span>  
  
 <span data-ttu-id="2527e-107">Les cellules de la colonne `Priority` affichent des images au lieu des valeurs de cellules textuelles correspondantes.</span><span class="sxs-lookup"><span data-stu-id="2527e-107">Cells in the `Priority` column display images in place of corresponding textual cell values.</span></span> <span data-ttu-id="2527e-108">La propriété <xref:System.Windows.Forms.ConvertEventArgs.Value%2A> de <xref:System.Windows.Forms.DataGridViewCellFormattingEventArgs> sert à obtenir la valeur de la cellule textuelle et à définir la valeur d'affichage d'image correspondante.</span><span class="sxs-lookup"><span data-stu-id="2527e-108">The <xref:System.Windows.Forms.ConvertEventArgs.Value%2A> property of the <xref:System.Windows.Forms.DataGridViewCellFormattingEventArgs> is used both to get the textual cell value and to set the corresponding image display value.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2527e-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="2527e-109">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewCustomizeDataFormatting#00](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCustomizeDataFormatting/cs/customFormatting.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewCustomizeDataFormatting#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCustomizeDataFormatting/vb/customFormatting.vb#00)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="2527e-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="2527e-110">Compiling the Code</span></span>  
 <span data-ttu-id="2527e-111">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="2527e-111">This example requires:</span></span>  
  
- <span data-ttu-id="2527e-112">des références aux assemblys System, System.Drawing et System.Windows.Forms ;</span><span class="sxs-lookup"><span data-stu-id="2527e-112">References to the System, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
- <span data-ttu-id="2527e-113">des images <xref:System.Drawing.Bitmap> nommées `highPri.bmp`, `mediumPri.bmp` et `lowPri.bmp` résidant dans le même répertoire que le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="2527e-113"><xref:System.Drawing.Bitmap> images named `highPri.bmp`, `mediumPri.bmp`, and `lowPri.bmp` residing in the same directory as the executable file.</span></span>  
  
 <span data-ttu-id="2527e-114">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="2527e-114">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="2527e-115">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="2527e-115">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2527e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2527e-116">See also</span></span>

- <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewBand.DefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewCellStyle>
- <xref:System.Drawing.Bitmap>
- [<span data-ttu-id="2527e-117">Affichage des données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2527e-117">Displaying Data in the Windows Forms DataGridView Control</span></span>](displaying-data-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="2527e-118">Guide pratique pour Format des données dans les Windows Forms DataGridView Control</span><span class="sxs-lookup"><span data-stu-id="2527e-118">How to: Format Data in the Windows Forms DataGridView Control</span></span>](how-to-format-data-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="2527e-119">Styles de cellules dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2527e-119">Cell Styles in the Windows Forms DataGridView Control</span></span>](cell-styles-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="2527e-120">Mise en forme de données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2527e-120">Data Formatting in the Windows Forms DataGridView Control</span></span>](data-formatting-in-the-windows-forms-datagridview-control.md)
