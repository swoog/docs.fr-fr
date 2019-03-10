---
title: 'Procédure : Modifier la bordure et les Styles de quadrillage dans le contrôle de DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- gridlines [Windows Forms], changing styles
- data grids [Windows Forms], changing gridline styles
- DataGridView control [Windows Forms], border styles
- data grids [Windows Forms], changing border styles
- DataGridView control [Windows Forms], gridline styles
ms.assetid: 2f413c7a-4025-4171-8e3a-66ef908ea583
ms.openlocfilehash: b4984dca6fb7dc8575b00758f0d61d9ff011e1ca
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57703363"
---
# <a name="how-to-change-the-border-and-gridline-styles-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="627ed-102">Procédure : Modifier la bordure et les Styles de quadrillage dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="627ed-102">How to: Change the Border and Gridline Styles in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="627ed-103">Avec la <xref:System.Windows.Forms.DataGridView> contrôle, vous pouvez personnaliser l’apparence de bordure du contrôle et des quadrillages pour améliorer l’expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="627ed-103">With the <xref:System.Windows.Forms.DataGridView> control, you can customize the appearance of the control's border and gridlines to improve the user experience.</span></span> <span data-ttu-id="627ed-104">Vous pouvez modifier la couleur du quadrillage et le style de bordure de contrôle en plus de styles de bordure des cellules dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="627ed-104">You can modify the gridline color and the control border style in addition to the border styles for the cells within the control.</span></span> <span data-ttu-id="627ed-105">Vous pouvez également appliquer des styles de bordure de cellule différentes pour les cellules ordinaires, les cellules d’en-tête de ligne et les cellules d’en-tête de colonne.</span><span class="sxs-lookup"><span data-stu-id="627ed-105">You can also apply different cell border styles for ordinary cells, row header cells, and column header cells.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="627ed-106">La couleur du quadrillage est utilisée uniquement avec le <xref:System.Windows.Forms.DataGridViewCellBorderStyle.Single>, <xref:System.Windows.Forms.DataGridViewCellBorderStyle.SingleHorizontal>, et <xref:System.Windows.Forms.DataGridViewCellBorderStyle.SingleVertical> les valeurs de la <xref:System.Windows.Forms.DataGridViewCellBorderStyle> énumération et la <xref:System.Windows.Forms.DataGridViewHeaderBorderStyle.Single> valeur de la <xref:System.Windows.Forms.DataGridViewHeaderBorderStyle> énumération.</span><span class="sxs-lookup"><span data-stu-id="627ed-106">The gridline color is used only with the <xref:System.Windows.Forms.DataGridViewCellBorderStyle.Single>, <xref:System.Windows.Forms.DataGridViewCellBorderStyle.SingleHorizontal>, and <xref:System.Windows.Forms.DataGridViewCellBorderStyle.SingleVertical> values of the <xref:System.Windows.Forms.DataGridViewCellBorderStyle> enumeration and the <xref:System.Windows.Forms.DataGridViewHeaderBorderStyle.Single> value of the <xref:System.Windows.Forms.DataGridViewHeaderBorderStyle> enumeration.</span></span> <span data-ttu-id="627ed-107">Les autres valeurs de ces énumérations utilisent des couleurs spécifiées par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="627ed-107">The other values of these enumerations use colors specified by the operating system.</span></span> <span data-ttu-id="627ed-108">En outre, lorsque les styles visuels sont activés sur Windows XP et la famille Windows Server 2003 via les <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType> (méthode), le <xref:System.Windows.Forms.DataGridView.GridColor%2A> valeur de propriété n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="627ed-108">Additionally, when visual styles are enabled on Windows XP and the Windows Server 2003 family through the <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType> method, the <xref:System.Windows.Forms.DataGridView.GridColor%2A> property value is not used.</span></span>  
  
### <a name="to-change-the-gridline-color-programmatically"></a><span data-ttu-id="627ed-109">Pour modifier la couleur du quadrillage par programmation</span><span class="sxs-lookup"><span data-stu-id="627ed-109">To change the gridline color programmatically</span></span>  
  
-   <span data-ttu-id="627ed-110">définir la propriété <xref:System.Windows.Forms.DataGridView.GridColor%2A> ;</span><span class="sxs-lookup"><span data-stu-id="627ed-110">Set the <xref:System.Windows.Forms.DataGridView.GridColor%2A> property.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#031](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#031)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#031](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#031)]  
  
### <a name="to-change-the-border-style-of-the-entire-datagridview-control-programmatically"></a><span data-ttu-id="627ed-111">Pour modifier le style de bordure de l’ensemble du contrôle DataGridView par programmation</span><span class="sxs-lookup"><span data-stu-id="627ed-111">To change the border style of the entire DataGridView control programmatically</span></span>  
  
-   <span data-ttu-id="627ed-112">Affectez l'une des valeurs de l'énumération <xref:System.Windows.Forms.DataGridView.BorderStyle%2A> à la propriété <xref:System.Windows.Forms.BorderStyle>.</span><span class="sxs-lookup"><span data-stu-id="627ed-112">Set the <xref:System.Windows.Forms.DataGridView.BorderStyle%2A> property to one of the <xref:System.Windows.Forms.BorderStyle> enumeration values.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#032](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#032)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#032](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#032)]  
  
### <a name="to-change-the-border-styles-for-datagridview-cells-programmatically"></a><span data-ttu-id="627ed-113">Pour modifier par programmation les styles de bordure des cellules DataGridView</span><span class="sxs-lookup"><span data-stu-id="627ed-113">To change the border styles for DataGridView cells programmatically</span></span>  
  
-   <span data-ttu-id="627ed-114">Définir le <xref:System.Windows.Forms.DataGridView.CellBorderStyle%2A>, <xref:System.Windows.Forms.DataGridView.RowHeadersBorderStyle%2A>, et <xref:System.Windows.Forms.DataGridView.ColumnHeadersBorderStyle%2A> propriétés.</span><span class="sxs-lookup"><span data-stu-id="627ed-114">Set the <xref:System.Windows.Forms.DataGridView.CellBorderStyle%2A>, <xref:System.Windows.Forms.DataGridView.RowHeadersBorderStyle%2A>, and <xref:System.Windows.Forms.DataGridView.ColumnHeadersBorderStyle%2A> properties.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#033](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#033)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#033](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#033)]  
  
## <a name="example"></a><span data-ttu-id="627ed-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="627ed-115">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#030](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#030)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#030](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#030)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="627ed-116">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="627ed-116">Compiling the Code</span></span>  
 <span data-ttu-id="627ed-117">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="627ed-117">This example requires:</span></span>  
  
-   <span data-ttu-id="627ed-118">un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ;</span><span class="sxs-lookup"><span data-stu-id="627ed-118">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1`.</span></span>  
  
-   <span data-ttu-id="627ed-119">des références aux assemblys <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType> et <xref:System.Drawing?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="627ed-119">References to the <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, and <xref:System.Drawing?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="627ed-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="627ed-120">See also</span></span>
- <xref:System.Windows.Forms.BorderStyle>
- <xref:System.Windows.Forms.DataGridView.BorderStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.CellBorderStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.ColumnHeadersBorderStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.GridColor%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.RowHeadersBorderStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewCellBorderStyle>
- <xref:System.Windows.Forms.DataGridViewHeaderBorderStyle>
- [<span data-ttu-id="627ed-121">Mises en forme et styles de base dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="627ed-121">Basic Formatting and Styling in the Windows Forms DataGridView Control</span></span>](basic-formatting-and-styling-in-the-windows-forms-datagridview-control.md)
