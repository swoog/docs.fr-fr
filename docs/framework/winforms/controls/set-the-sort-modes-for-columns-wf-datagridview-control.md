---
title: 'Procédure : définir les modes de tri des colonnes dans le contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sorting [Windows Forms], data grids
- DataGridView control [Windows Forms], sort mode
- data grids [Windows Forms], sorting data
ms.assetid: 57dfed60-a608-40d5-86f9-d65686ffb325
ms.openlocfilehash: 4894de00a323f70ca244ea877101a5af1cbb37e0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59096366"
---
# <a name="how-to-set-the-sort-modes-for-columns-in-the-windows-forms-datagridview-control"></a>Procédure : définir les modes de tri des colonnes dans le contrôle DataGridView Windows Forms
Dans la <xref:System.Windows.Forms.DataGridView> utilisent des colonnes de zone de texte contrôle, le tri automatique par défaut, tandis que les autres types de colonnes ne sont pas triées automatiquement. Parfois, vous devez remplacer ces valeurs par défaut. Par exemple, vous pouvez afficher des images au lieu de texte, des nombres ou des valeurs de cellule d’énumération. Tandis que les images ne peut pas être triées, les valeurs sous-jacentes qu’ils représentent peuvent être triées.  
  
 Dans le <xref:System.Windows.Forms.DataGridView> contrôle, le <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A> valeur de propriété d’une colonne détermine son comportement de tri.  
  
 La procédure suivante affiche le `Priority` colonne à partir de [Comment : Personnaliser la mise en forme des données dans le contrôle de DataGridView Windows Forms](how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md). Cette colonne est une colonne d’image et n’est pas triable par défaut. Il contient des valeurs de cellules réelles qui sont des chaînes, toutefois, donc il peut être trié automatiquement.  
  
### <a name="to-set-the-sort-mode-for-a-column"></a>Pour définir le mode de tri pour une colonne  
  
-   définir la propriété <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A?displayProperty=nameWithType> ;  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#066](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#066)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#066](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#066)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` qui contient une colonne nommée `Priority` ;  
  
-   des références aux assemblys <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A?displayProperty=nameWithType>
- [Tri des données dans le contrôle DataGridView Windows Forms](sorting-data-in-the-windows-forms-datagridview-control.md)
- [Modes de tri des colonnes du contrôle DataGridView Windows Forms](column-sort-modes-in-the-windows-forms-datagridview-control.md)
- [Guide pratique pour Personnaliser le tri dans le contrôle DataGridView Windows Forms](how-to-customize-sorting-in-the-windows-forms-datagridview-control.md)
