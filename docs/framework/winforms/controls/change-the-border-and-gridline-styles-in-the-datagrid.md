---
title: 'Procédure : modifier les styles de bordure et de quadrillage dans le contrôle DataGridView Windows Forms'
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
ms.openlocfilehash: d24adb98c339f911d6bea0312bce4d4b4f198a61
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61939007"
---
# <a name="how-to-change-the-border-and-gridline-styles-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="b175d-102">Procédure : modifier les styles de bordure et de quadrillage dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b175d-102">How to: Change the Border and Gridline Styles in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="b175d-103">Avec la <xref:System.Windows.Forms.DataGridView> contrôle, vous pouvez personnaliser l’apparence de bordure du contrôle et des quadrillages pour améliorer l’expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b175d-103">With the <xref:System.Windows.Forms.DataGridView> control, you can customize the appearance of the control's border and gridlines to improve the user experience.</span></span> <span data-ttu-id="b175d-104">Vous pouvez modifier la couleur du quadrillage et le style de bordure de contrôle en plus de styles de bordure des cellules dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="b175d-104">You can modify the gridline color and the control border style in addition to the border styles for the cells within the control.</span></span> <span data-ttu-id="b175d-105">Vous pouvez également appliquer des styles de bordure de cellule différentes pour les cellules ordinaires, les cellules d’en-tête de ligne et les cellules d’en-tête de colonne.</span><span class="sxs-lookup"><span data-stu-id="b175d-105">You can also apply different cell border styles for ordinary cells, row header cells, and column header cells.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b175d-106">La couleur du quadrillage est utilisée uniquement avec le <xref:System.Windows.Forms.DataGridViewCellBorderStyle.Single>, <xref:System.Windows.Forms.DataGridViewCellBorderStyle.SingleHorizontal>, et <xref:System.Windows.Forms.DataGridViewCellBorderStyle.SingleVertical> les valeurs de la <xref:System.Windows.Forms.DataGridViewCellBorderStyle> énumération et la <xref:System.Windows.Forms.DataGridViewHeaderBorderStyle.Single> valeur de la <xref:System.Windows.Forms.DataGridViewHeaderBorderStyle> énumération.</span><span class="sxs-lookup"><span data-stu-id="b175d-106">The gridline color is used only with the <xref:System.Windows.Forms.DataGridViewCellBorderStyle.Single>, <xref:System.Windows.Forms.DataGridViewCellBorderStyle.SingleHorizontal>, and <xref:System.Windows.Forms.DataGridViewCellBorderStyle.SingleVertical> values of the <xref:System.Windows.Forms.DataGridViewCellBorderStyle> enumeration and the <xref:System.Windows.Forms.DataGridViewHeaderBorderStyle.Single> value of the <xref:System.Windows.Forms.DataGridViewHeaderBorderStyle> enumeration.</span></span> <span data-ttu-id="b175d-107">Les autres valeurs de ces énumérations utilisent des couleurs spécifiées par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b175d-107">The other values of these enumerations use colors specified by the operating system.</span></span> <span data-ttu-id="b175d-108">En outre, lorsque les styles visuels sont activés sur Windows XP et la famille Windows Server 2003 via les <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType> (méthode), le <xref:System.Windows.Forms.DataGridView.GridColor%2A> valeur de propriété n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="b175d-108">Additionally, when visual styles are enabled on Windows XP and the Windows Server 2003 family through the <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType> method, the <xref:System.Windows.Forms.DataGridView.GridColor%2A> property value is not used.</span></span>  
  
### <a name="to-change-the-gridline-color-programmatically"></a><span data-ttu-id="b175d-109">Pour modifier la couleur du quadrillage par programmation</span><span class="sxs-lookup"><span data-stu-id="b175d-109">To change the gridline color programmatically</span></span>  
  
- <span data-ttu-id="b175d-110">définir la propriété <xref:System.Windows.Forms.DataGridView.GridColor%2A> ;</span><span class="sxs-lookup"><span data-stu-id="b175d-110">Set the <xref:System.Windows.Forms.DataGridView.GridColor%2A> property.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#031](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#031)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#031](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#031)]  
  
### <a name="to-change-the-border-style-of-the-entire-datagridview-control-programmatically"></a><span data-ttu-id="b175d-111">Pour modifier le style de bordure de l’ensemble du contrôle DataGridView par programmation</span><span class="sxs-lookup"><span data-stu-id="b175d-111">To change the border style of the entire DataGridView control programmatically</span></span>  
  
- <span data-ttu-id="b175d-112">Affectez l'une des valeurs de l'énumération <xref:System.Windows.Forms.DataGridView.BorderStyle%2A> à la propriété <xref:System.Windows.Forms.BorderStyle>.</span><span class="sxs-lookup"><span data-stu-id="b175d-112">Set the <xref:System.Windows.Forms.DataGridView.BorderStyle%2A> property to one of the <xref:System.Windows.Forms.BorderStyle> enumeration values.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#032](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#032)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#032](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#032)]  
  
### <a name="to-change-the-border-styles-for-datagridview-cells-programmatically"></a><span data-ttu-id="b175d-113">Pour modifier par programmation les styles de bordure des cellules DataGridView</span><span class="sxs-lookup"><span data-stu-id="b175d-113">To change the border styles for DataGridView cells programmatically</span></span>  
  
- <span data-ttu-id="b175d-114">Définir le <xref:System.Windows.Forms.DataGridView.CellBorderStyle%2A>, <xref:System.Windows.Forms.DataGridView.RowHeadersBorderStyle%2A>, et <xref:System.Windows.Forms.DataGridView.ColumnHeadersBorderStyle%2A> propriétés.</span><span class="sxs-lookup"><span data-stu-id="b175d-114">Set the <xref:System.Windows.Forms.DataGridView.CellBorderStyle%2A>, <xref:System.Windows.Forms.DataGridView.RowHeadersBorderStyle%2A>, and <xref:System.Windows.Forms.DataGridView.ColumnHeadersBorderStyle%2A> properties.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#033](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#033)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#033](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#033)]  
  
## <a name="example"></a><span data-ttu-id="b175d-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="b175d-115">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#030](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#030)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#030](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#030)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="b175d-116">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="b175d-116">Compiling the Code</span></span>  
 <span data-ttu-id="b175d-117">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="b175d-117">This example requires:</span></span>  
  
- <span data-ttu-id="b175d-118">un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ;</span><span class="sxs-lookup"><span data-stu-id="b175d-118">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1`.</span></span>  
  
- <span data-ttu-id="b175d-119">des références aux assemblys <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType> et <xref:System.Drawing?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="b175d-119">References to the <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, and <xref:System.Drawing?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b175d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b175d-120">See also</span></span>

- <xref:System.Windows.Forms.BorderStyle>
- <xref:System.Windows.Forms.DataGridView.BorderStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.CellBorderStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.ColumnHeadersBorderStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.GridColor%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.RowHeadersBorderStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewCellBorderStyle>
- <xref:System.Windows.Forms.DataGridViewHeaderBorderStyle>
- [<span data-ttu-id="b175d-121">Mises en forme et styles de base dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b175d-121">Basic Formatting and Styling in the Windows Forms DataGridView Control</span></span>](basic-formatting-and-styling-in-the-windows-forms-datagridview-control.md)
