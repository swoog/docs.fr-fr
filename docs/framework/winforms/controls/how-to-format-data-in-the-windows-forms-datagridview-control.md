---
title: 'Procédure : Format des données dans les Windows Forms DataGridView Control'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], formatting data
- data [Windows Forms], formatting in DataGridView control
- data grids [Windows Forms], enabling wordwrap
- currency values [Windows Forms], formatting in data grids
- data grids [Windows Forms], currency values
- data grids [Windows Forms], formatting data
- data grids [Windows Forms], text alignment
- data grids [Windows Forms], date values
- cells [Windows Forms], text alignment
ms.assetid: 8c33543c-9c08-4636-a65a-fdf714a529b7
ms.openlocfilehash: fa029a46f1553d8d371fd574c21e7a016e7b5500
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54598119"
---
# <a name="how-to-format-data-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="cc4f0-102">Procédure : Format des données dans les Windows Forms DataGridView Control</span><span class="sxs-lookup"><span data-stu-id="cc4f0-102">How to: Format Data in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="cc4f0-103">Les procédures suivantes montrent la base de la mise en forme des valeurs de cellule à l’aide de la <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A> propriété d’un <xref:System.Windows.Forms.DataGridView> contrôle et de colonnes spécifiques dans un contrôle.</span><span class="sxs-lookup"><span data-stu-id="cc4f0-103">The following procedures demonstrate basic formatting of cell values using the <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A> property of a <xref:System.Windows.Forms.DataGridView> control and of specific columns in a control.</span></span> <span data-ttu-id="cc4f0-104">Pour plus d’informations sur la mise en forme de données avancés, consultez [Comment : Personnaliser la mise en forme des données dans le contrôle de DataGridView Windows Forms](../../../../docs/framework/winforms/controls/how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="cc4f0-104">For information about advanced data formatting, see [How to: Customize Data Formatting in the Windows Forms DataGridView Control](../../../../docs/framework/winforms/controls/how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md).</span></span>  
  
### <a name="to-format-currency-and-date-values"></a><span data-ttu-id="cc4f0-105">Pour mettre en forme monétaire et les valeurs de date</span><span class="sxs-lookup"><span data-stu-id="cc4f0-105">To format currency and date values</span></span>  
  
-   <span data-ttu-id="cc4f0-106">Définissez la propriété <xref:System.Windows.Forms.DataGridViewCellStyle.Format%2A> d'un <xref:System.Windows.Forms.DataGridViewCellStyle>.</span><span class="sxs-lookup"><span data-stu-id="cc4f0-106">Set the <xref:System.Windows.Forms.DataGridViewCellStyle.Format%2A> property of a <xref:System.Windows.Forms.DataGridViewCellStyle>.</span></span> <span data-ttu-id="cc4f0-107">L’exemple de code suivant définit le format pour des colonnes spécifiques à l’aide de la <xref:System.Windows.Forms.DataGridViewColumn.DefaultCellStyle%2A> propriété des colonnes.</span><span class="sxs-lookup"><span data-stu-id="cc4f0-107">The following code example sets the format for specific columns using the <xref:System.Windows.Forms.DataGridViewColumn.DefaultCellStyle%2A> property of the columns.</span></span> <span data-ttu-id="cc4f0-108">Les valeurs dans le `UnitPrice` colonne apparaissent dans le format monétaire spécifique à la culture actuelle, les valeurs négatives entourés parenthèses.</span><span class="sxs-lookup"><span data-stu-id="cc4f0-108">Values in the `UnitPrice` column appear in the current culture-specific currency format, with negative values surrounded by parentheses.</span></span> <span data-ttu-id="cc4f0-109">Les valeurs dans le `ShipDate` colonne apparaissent dans le format de date courte de spécifiques à la culture actuelle.</span><span class="sxs-lookup"><span data-stu-id="cc4f0-109">Values in the `ShipDate` column appear in the current culture-specific short date format.</span></span> <span data-ttu-id="cc4f0-110">Pour plus d’informations sur <xref:System.Windows.Forms.DataGridViewCellStyle.Format%2A> valeurs, consultez [mise en forme des Types](../../../../docs/standard/base-types/formatting-types.md).</span><span class="sxs-lookup"><span data-stu-id="cc4f0-110">For more information about <xref:System.Windows.Forms.DataGridViewCellStyle.Format%2A> values, see [Formatting Types](../../../../docs/standard/base-types/formatting-types.md).</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#071](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#071)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#071](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#071)]  
  
### <a name="to-customize-the-display-of-null-database-values"></a><span data-ttu-id="cc4f0-111">Pour personnaliser l’affichage des valeurs null de base de données</span><span class="sxs-lookup"><span data-stu-id="cc4f0-111">To customize the display of null database values</span></span>  
  
-   <span data-ttu-id="cc4f0-112">Définissez la propriété <xref:System.Windows.Forms.DataGridViewCellStyle.NullValue%2A> d'un <xref:System.Windows.Forms.DataGridViewCellStyle>.</span><span class="sxs-lookup"><span data-stu-id="cc4f0-112">Set the <xref:System.Windows.Forms.DataGridViewCellStyle.NullValue%2A> property of a <xref:System.Windows.Forms.DataGridViewCellStyle>.</span></span> <span data-ttu-id="cc4f0-113">Le code suivant exemple utilise le <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType> propriété à n’afficher « aucune entrée » dans toutes les cellules contenant les valeurs sont égales à <xref:System.DBNull.Value?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="cc4f0-113">The following code example uses the <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType> property to display "no entry" in all cells containing values equal to <xref:System.DBNull.Value?displayProperty=nameWithType>.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#073](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#073)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#073](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#073)]  
  
### <a name="to-enable-wordwrap-in-text-based-cells"></a><span data-ttu-id="cc4f0-114">Pour activer wordwrap dans les cellules textuelles</span><span class="sxs-lookup"><span data-stu-id="cc4f0-114">To enable wordwrap in text-based cells</span></span>  
  
-   <span data-ttu-id="cc4f0-115">Définir le <xref:System.Windows.Forms.DataGridViewCellStyle.WrapMode%2A> propriété d’un <xref:System.Windows.Forms.DataGridViewCellStyle> à un de la <xref:System.Windows.Forms.DataGridViewTriState> valeurs d’énumération.</span><span class="sxs-lookup"><span data-stu-id="cc4f0-115">Set the <xref:System.Windows.Forms.DataGridViewCellStyle.WrapMode%2A> property of a <xref:System.Windows.Forms.DataGridViewCellStyle> to one of the <xref:System.Windows.Forms.DataGridViewTriState> enumeration values.</span></span> <span data-ttu-id="cc4f0-116">Le code suivant exemple utilise le <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType> propriété à définir le mode habillage pour l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="cc4f0-116">The following code example uses the <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType> property to set the wrap mode for the entire control.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#074](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#074)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#074](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#074)]  
  
### <a name="to-specify-the-text-alignment-of-datagridview-cells"></a><span data-ttu-id="cc4f0-117">Pour spécifier l’alignement du texte des cellules DataGridView</span><span class="sxs-lookup"><span data-stu-id="cc4f0-117">To specify the text alignment of DataGridView cells</span></span>  
  
-   <span data-ttu-id="cc4f0-118">Définir le <xref:System.Windows.Forms.DataGridViewCellStyle.Alignment%2A> propriété d’un <xref:System.Windows.Forms.DataGridViewCellStyle> à un de la <xref:System.Windows.Forms.DataGridViewContentAlignment> valeurs d’énumération.</span><span class="sxs-lookup"><span data-stu-id="cc4f0-118">Set the <xref:System.Windows.Forms.DataGridViewCellStyle.Alignment%2A> property of a <xref:System.Windows.Forms.DataGridViewCellStyle> to one of the <xref:System.Windows.Forms.DataGridViewContentAlignment> enumeration values.</span></span> <span data-ttu-id="cc4f0-119">L’exemple de code suivant définit l’alignement pour une colonne spécifique à l’aide de la <xref:System.Windows.Forms.DataGridViewColumn.DefaultCellStyle%2A> propriété de la colonne.</span><span class="sxs-lookup"><span data-stu-id="cc4f0-119">The following code example sets the alignment for a specific column using the <xref:System.Windows.Forms.DataGridViewColumn.DefaultCellStyle%2A> property of the column.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#072](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#072)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#072](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#072)]  
  
## <a name="example"></a><span data-ttu-id="cc4f0-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="cc4f0-120">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#070](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#070)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#070](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#070)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="cc4f0-121">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="cc4f0-121">Compiling the Code</span></span>  
 <span data-ttu-id="cc4f0-122">Ces exemples nécessitent :</span><span class="sxs-lookup"><span data-stu-id="cc4f0-122">These examples require:</span></span>  
  
-   <span data-ttu-id="cc4f0-123">Un <xref:System.Windows.Forms.DataGridView> contrôle nommé `dataGridView1` qui contient une colonne nommée `UnitPrice`, une colonne nommée `ShipDate`et une colonne nommée `CustomerName`.</span><span class="sxs-lookup"><span data-stu-id="cc4f0-123">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1` that contains a column named `UnitPrice`, a column named `ShipDate`, and a column named `CustomerName`.</span></span>  
  
-   <span data-ttu-id="cc4f0-124">des références aux assemblys <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="cc4f0-124">References to the <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType>, and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="cc4f0-125">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="cc4f0-125">Robust Programming</span></span>  
 <span data-ttu-id="cc4f0-126">Pour optimiser l’évolutivité, vous devez partager <xref:System.Windows.Forms.DataGridViewCellStyle> objets sur plusieurs lignes, colonnes ou cellules qui utilisent les mêmes styles, plutôt que de définir les propriétés de style pour chaque élément séparément.</span><span class="sxs-lookup"><span data-stu-id="cc4f0-126">For maximum scalability, you should share <xref:System.Windows.Forms.DataGridViewCellStyle> objects across multiple rows, columns, or cells that use the same styles rather than setting the style properties for each element separately.</span></span> <span data-ttu-id="cc4f0-127">Pour plus d’informations, consultez [meilleures pratiques pour la mise à l’échelle le contrôle de DataGridView Windows Forms](../../../../docs/framework/winforms/controls/best-practices-for-scaling-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="cc4f0-127">For more information, see [Best Practices for Scaling the Windows Forms DataGridView Control](../../../../docs/framework/winforms/controls/best-practices-for-scaling-the-windows-forms-datagridview-control.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc4f0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc4f0-128">See also</span></span>
- <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewBand.DefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewCellStyle>
- [<span data-ttu-id="cc4f0-129">Mises en forme et styles de base dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cc4f0-129">Basic Formatting and Styling in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/basic-formatting-and-styling-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="cc4f0-130">Styles de cellules dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cc4f0-130">Cell Styles in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/cell-styles-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="cc4f0-131">Mise en forme de données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cc4f0-131">Data Formatting in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/data-formatting-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="cc4f0-132">Guide pratique pour Personnaliser la mise en forme des données dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cc4f0-132">How to: Customize Data Formatting in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="cc4f0-133">Mise en forme des types</span><span class="sxs-lookup"><span data-stu-id="cc4f0-133">Formatting Types</span></span>](../../../../docs/standard/base-types/formatting-types.md)
