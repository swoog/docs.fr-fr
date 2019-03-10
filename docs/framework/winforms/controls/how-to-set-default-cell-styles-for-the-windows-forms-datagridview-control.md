---
title: 'Procédure : Définir des Styles de cellules par défaut pour le contrôle de DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], cell styles
- cells [Windows Forms], styles
- data grids [Windows Forms], cell styles
ms.assetid: 1aaaca43-5340-447e-99c0-9177d9776aa1
ms.openlocfilehash: c7ece81e193f29960f29b749438280bbff0591f9
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57703125"
---
# <a name="how-to-set-default-cell-styles-for-the-windows-forms-datagridview-control"></a><span data-ttu-id="28e17-102">Procédure : Définir des Styles de cellules par défaut pour le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="28e17-102">How to: Set Default Cell Styles for the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="28e17-103">Avec le contrôle <xref:System.Windows.Forms.DataGridView>, vous pouvez spécifier des styles de cellules par défaut pour le contrôle entier et pour des colonnes et des lignes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="28e17-103">With the <xref:System.Windows.Forms.DataGridView> control, you can specify default cell styles for the entire control and for specific columns and rows.</span></span> <span data-ttu-id="28e17-104">Ces valeurs par défaut sont propagées du niveau contrôle au niveau colonne, puis au niveau ligne, et enfin au niveau cellule.</span><span class="sxs-lookup"><span data-stu-id="28e17-104">These defaults filter down from the control level to the column level, then to the row level, then to the cell level.</span></span> <span data-ttu-id="28e17-105">Si une propriété <xref:System.Windows.Forms.DataGridViewCellStyle> spécifique n'est pas définie au niveau de la cellule, le paramètre de propriété par défaut au niveau de la ligne est utilisé.</span><span class="sxs-lookup"><span data-stu-id="28e17-105">If a particular <xref:System.Windows.Forms.DataGridViewCellStyle> property is not set at the cell level, the default property setting at the row level is used.</span></span> <span data-ttu-id="28e17-106">Si la propriété n'est pas définie non plus au niveau de la ligne, le paramètre de colonne par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="28e17-106">If the property is also not set at the row level, the default column setting is used.</span></span> <span data-ttu-id="28e17-107">Pour finir, si la propriété n'est pas non plus définie au niveau de la colonne, le paramètre <xref:System.Windows.Forms.DataGridView> par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="28e17-107">Finally, if the property is also not set at the column level, the default <xref:System.Windows.Forms.DataGridView> setting is used.</span></span> <span data-ttu-id="28e17-108">Avec ce paramètre, vous pouvez éviter de devoir dupliquer les paramètres de propriétés à plusieurs niveaux.</span><span class="sxs-lookup"><span data-stu-id="28e17-108">With this setting, you can avoid having to duplicate the property settings at multiple levels.</span></span> <span data-ttu-id="28e17-109">À chaque niveau, il vous suffit de spécifier les styles qui diffèrent des niveaux au-dessus de lui.</span><span class="sxs-lookup"><span data-stu-id="28e17-109">At each level, simply specify the styles that differ from the levels above it.</span></span> <span data-ttu-id="28e17-110">Pour plus d’informations, consultez [Styles de cellules dans le contrôle DataGridView Windows Forms](cell-styles-in-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="28e17-110">For more information, see [Cell Styles in the Windows Forms DataGridView Control](cell-styles-in-the-windows-forms-datagridview-control.md).</span></span>  
  
 <span data-ttu-id="28e17-111">Cette tâche est très bien prise en charge dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="28e17-111">There is extensive support for this task in Visual Studio.</span></span>  <span data-ttu-id="28e17-112">Voir également [Guide pratique pour Définir des Styles de cellules par défaut et les Formats de données pour les Windows Forms DataGridView Control à l’aide du concepteur](default-cell-styles-datagridview.md).</span><span class="sxs-lookup"><span data-stu-id="28e17-112">Also see [How to: Set Default Cell Styles and Data Formats for the Windows Forms DataGridView Control Using the Designer](default-cell-styles-datagridview.md).</span></span>  
  
### <a name="to-set-the-default-cell-styles-programmatically"></a><span data-ttu-id="28e17-113">Pour définir les styles de cellules par défaut par programmation</span><span class="sxs-lookup"><span data-stu-id="28e17-113">To set the default cell styles programmatically</span></span>  
  
1.  <span data-ttu-id="28e17-114">Définissez les propriétés du <xref:System.Windows.Forms.DataGridViewCellStyle> récupéré via la propriété <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="28e17-114">Set the properties of the <xref:System.Windows.Forms.DataGridViewCellStyle> retrieved through the <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType> property.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#141](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#141)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#141](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#141)]  
  
2.  <span data-ttu-id="28e17-115">Créez et initialisez de nouveaux objets <xref:System.Windows.Forms.DataGridViewCellStyle> pour une utilisation par plusieurs lignes et colonnes.</span><span class="sxs-lookup"><span data-stu-id="28e17-115">Create and initialize new <xref:System.Windows.Forms.DataGridViewCellStyle> objects for use by multiple rows and columns.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#142](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#142)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#142](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#142)]  
  
3.  <span data-ttu-id="28e17-116">Définissez la propriété `DefaultCellStyle` de lignes et de colonnes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="28e17-116">Set the `DefaultCellStyle` property of specific rows and columns.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#143](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#143)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#143](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#143)]  
  
## <a name="example"></a><span data-ttu-id="28e17-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="28e17-117">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#140](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#140)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#140](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#140)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="28e17-118">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="28e17-118">Compiling the Code</span></span>  
 <span data-ttu-id="28e17-119">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="28e17-119">This example requires:</span></span>  
  
-   <span data-ttu-id="28e17-120">un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ;</span><span class="sxs-lookup"><span data-stu-id="28e17-120">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1`.</span></span>  
  
-   <span data-ttu-id="28e17-121">des références aux assemblys <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="28e17-121">References to the <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType>, and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="28e17-122">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="28e17-122">Robust Programming</span></span>  
 <span data-ttu-id="28e17-123">Pour bénéficier d'une extensibilité maximale quand vous travaillez avec des jeux de données très volumineux, vous devez partager des objets <xref:System.Windows.Forms.DataGridViewCellStyle> sur plusieurs lignes, colonnes ou cellules qui utilisent les mêmes styles, plutôt que définir séparément les propriétés de style pour les différents éléments.</span><span class="sxs-lookup"><span data-stu-id="28e17-123">To achieve maximum scalability when you work with very large data sets, you should share <xref:System.Windows.Forms.DataGridViewCellStyle> objects across multiple rows, columns, or cells that use the same styles, rather than set the style properties for individual elements separately.</span></span> <span data-ttu-id="28e17-124">En outre, vous devez créer des lignes partagées et y accéder à l'aide de la propriété <xref:System.Windows.Forms.DataGridViewRowCollection.SharedRow%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="28e17-124">Additionally, you should create shared rows and access them by using the <xref:System.Windows.Forms.DataGridViewRowCollection.SharedRow%2A?displayProperty=nameWithType> property.</span></span> <span data-ttu-id="28e17-125">Pour plus d’informations, consultez [meilleures pratiques pour la mise à l’échelle le contrôle de DataGridView Windows Forms](best-practices-for-scaling-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="28e17-125">For more information, see [Best Practices for Scaling the Windows Forms DataGridView Control](best-practices-for-scaling-the-windows-forms-datagridview-control.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28e17-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28e17-126">See also</span></span>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewCellStyle>
- <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewBand.DefaultCellStyle%2A?displayProperty=nameWithType>
- [<span data-ttu-id="28e17-127">Mises en forme et styles de base dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="28e17-127">Basic Formatting and Styling in the Windows Forms DataGridView Control</span></span>](basic-formatting-and-styling-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="28e17-128">Styles de cellules dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="28e17-128">Cell Styles in the Windows Forms DataGridView Control</span></span>](cell-styles-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="28e17-129">Meilleures pratiques pour la mise à l'échelle du contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="28e17-129">Best Practices for Scaling the Windows Forms DataGridView Control</span></span>](best-practices-for-scaling-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="28e17-130">Guide pratique pour Définir les Styles de ligne en alternance pour le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="28e17-130">How to: Set Alternating Row Styles for the Windows Forms DataGridView Control</span></span>](how-to-set-alternating-row-styles-for-the-windows-forms-datagridview-control.md)
