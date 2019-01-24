---
title: 'Procédure : Obtenir les cellules sélectionnées, les lignes et les colonnes dans le contrôle de DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- selection [Windows Forms], DataGridView control [Windows Forms]
- DataGridView control [Windows Forms], getting selection
- getting selection [Windows Forms], DataGridView control [Windows Forms]
ms.assetid: d93c4b5b-498e-49bc-982a-2229d61778e4
ms.openlocfilehash: 95229f1915b25962a700a7d6aced0a012bbe6657
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54626912"
---
# <a name="how-to-get-the-selected-cells-rows-and-columns-in-the-windows-forms-datagridview-control"></a>Procédure : Obtenir les cellules sélectionnées, les lignes et les colonnes dans le contrôle de DataGridView Windows Forms
Vous pouvez obtenir les cellules sélectionnées, les lignes ou les colonnes à partir d’un <xref:System.Windows.Forms.DataGridView> contrôle en utilisant les propriétés correspondantes : <xref:System.Windows.Forms.DataGridView.SelectedCells%2A>, <xref:System.Windows.Forms.DataGridView.SelectedRows%2A>, et <xref:System.Windows.Forms.DataGridView.SelectedColumns%2A>. Dans les procédures suivantes, vous les cellules sélectionnées et afficher leurs index de ligne et de colonne dans un <xref:System.Windows.Forms.MessageBox>.  
  
### <a name="to-get-the-selected-cells-in-a-datagridview-control"></a>Pour obtenir les cellules sélectionnées dans un contrôle DataGridView  
  
-   Utilisez la propriété <xref:System.Windows.Forms.DataGridView.SelectedCells%2A>.  
  
    > [!NOTE]
    >  Utilisez le <xref:System.Windows.Forms.DataGridView.AreAllCellsSelected%2A> méthode pour éviter d’afficher un nombre potentiellement important de cellules.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewSelectedCollections#10](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSelectedCollections/CS/DataGridViewSelectedCollections.cs#10)]
     [!code-vb[System.Windows.Forms.DataGridViewSelectedCollections#10](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSelectedCollections/VB/DataGridViewSelectedCollections.vb#10)]  
  
### <a name="to-get-the-selected-rows-in-a-datagridview-control"></a>Pour obtenir les lignes sélectionnées dans un contrôle DataGridView  
  
-   Utilisez la propriété <xref:System.Windows.Forms.DataGridView.SelectedRows%2A>. Pour permettre aux utilisateurs de sélectionner des lignes, vous devez définir le <xref:System.Windows.Forms.DataGridView.SelectionMode%2A> propriété <xref:System.Windows.Forms.DataGridViewSelectionMode.FullRowSelect> ou <xref:System.Windows.Forms.DataGridViewSelectionMode.RowHeaderSelect>.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewSelectedCollections#20](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSelectedCollections/CS/DataGridViewSelectedCollections.cs#20)]
     [!code-vb[System.Windows.Forms.DataGridViewSelectedCollections#20](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSelectedCollections/VB/DataGridViewSelectedCollections.vb#20)]  
  
### <a name="to-get-the-selected-columns-in-a-datagridview-control"></a>Pour obtenir les colonnes sélectionnées dans un contrôle DataGridView  
  
-   Utilisez la propriété <xref:System.Windows.Forms.DataGridView.SelectedColumns%2A>. Pour permettre aux utilisateurs de sélectionner des colonnes, vous devez définir le <xref:System.Windows.Forms.DataGridView.SelectionMode%2A> propriété <xref:System.Windows.Forms.DataGridViewSelectionMode.FullColumnSelect> ou <xref:System.Windows.Forms.DataGridViewSelectionMode.ColumnHeaderSelect>.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewSelectedCollections#30](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSelectedCollections/CS/DataGridViewSelectedCollections.cs#30)]
     [!code-vb[System.Windows.Forms.DataGridViewSelectedCollections#30](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSelectedCollections/VB/DataGridViewSelectedCollections.vb#30)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   <xref:System.Windows.Forms.Button> contrôles nommés `selectedCellsButton`, `selectedRowsButton`, et `selectedColumnsButton`, chacun avec les gestionnaires pour les <xref:System.Windows.Forms.Control.Click> événement attaché.  
  
-   un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ;  
  
-   des références aux assemblys <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType> et <xref:System.Text?displayProperty=nameWithType>.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Les collections décrites dans cette rubrique n’effectuent pas efficacement quand un grand nombre de cellules, lignes ou colonnes est sélectionnées. Pour plus d’informations sur l’utilisation de ces collections avec grandes quantités de données, consultez [meilleures pratiques pour la mise à l’échelle le contrôle de DataGridView Windows Forms](../../../../docs/framework/winforms/controls/best-practices-for-scaling-the-windows-forms-datagridview-control.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.SelectionMode%2A>
- <xref:System.Windows.Forms.DataGridView.AreAllCellsSelected%2A>
- <xref:System.Windows.Forms.DataGridView.SelectedCells%2A>
- <xref:System.Windows.Forms.DataGridView.SelectedRows%2A>
- <xref:System.Windows.Forms.DataGridView.SelectedColumns%2A>
- [Sélection et utilisation du Presse-papiers avec le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/selection-and-clipboard-use-with-the-windows-forms-datagridview-control.md)
