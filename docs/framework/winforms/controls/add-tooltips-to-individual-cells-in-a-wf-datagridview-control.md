---
title: 'Procédure : Ajouter des info-bulles à des cellules dans un contrôle de DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- tooltips [Windows Forms], adding to data grids
- DataGridView control [Windows Forms], adding tooltips
- data grids [Windows Forms], adding tooltips
ms.assetid: 2a81f9de-d58b-4ea8-bc0b-8d93c2f4cf78
ms.openlocfilehash: 5198bec11142e31d60f9127ecebc4ffc8ee8b8ec
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57717412"
---
# <a name="how-to-add-tooltips-to-individual-cells-in-a-windows-forms-datagridview-control"></a>Procédure : Ajouter des info-bulles à des cellules dans un contrôle de DataGridView Windows Forms
Par défaut, les info-bulles sont utilisés pour afficher les valeurs de <xref:System.Windows.Forms.DataGridView> cellules qui sont trop petits pour afficher leur contenu entier. Vous pouvez remplacer ce comportement, toutefois, pour définir les valeurs de texte d’info-bulle pour les cellules individuelles. Cela est utile à afficher aux utilisateurs plus d’informations sur une cellule ou pour fournir aux utilisateurs une autre description du contenu de cellule. Par exemple, si vous avez une ligne qui affiche des icônes d’état, vous souhaiterez fournir des explications de texte à l’aide des info-bulles.  
  
 Vous pouvez également désactiver l’affichage des info-bulles de niveau de la cellule en définissant le <xref:System.Windows.Forms.DataGridView.ShowCellToolTips%2A?displayProperty=nameWithType> propriété `false`.  
  
### <a name="to-add-a-tooltip-to-a-cell"></a>Pour ajouter une info-bulle à une cellule  
  
-   définir la propriété <xref:System.Windows.Forms.DataGridViewCell.ToolTipText%2A?displayProperty=nameWithType> ;  
  
     [!code-cpp[System.Windows.Forms.DataGridViewCell.ToolTipText#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCell.ToolTipText/cpp/datagridviewcell.tooltiptext.cpp#1)]
     [!code-csharp[System.Windows.Forms.DataGridViewCell.ToolTipText#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCell.ToolTipText/CS/datagridviewcell.tooltiptext.cs#1)]
     [!code-vb[System.Windows.Forms.DataGridViewCell.ToolTipText#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCell.ToolTipText/VB/datagridviewcell.tooltiptext.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
  
-   Cet exemple nécessite :  
  
-   Un <xref:System.Windows.Forms.DataGridView> contrôle nommé `dataGridView1` qui contient une colonne nommée `Rating` pour afficher des valeurs de chaîne d’un à quatre astérisque (« * ») symboles. Le <xref:System.Windows.Forms.DataGridView.CellFormatting> événement du contrôle doit être associé à la méthode de gestionnaire d’événements dans l’exemple.  
  
-   des références aux assemblys <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Lorsque vous liez le <xref:System.Windows.Forms.DataGridView> le contrôle à une source de données externe ou fournir votre propre source de données en implémentant le mode virtuel, vous pouvez rencontrer des problèmes de performances. Pour éviter une altération des performances lorsque vous travaillez avec grandes quantités de données, gérer les <xref:System.Windows.Forms.DataGridView.CellToolTipTextNeeded> événements au lieu de définir le <xref:System.Windows.Forms.DataGridViewCell.ToolTipText%2A> propriété de plusieurs cellules. Lorsque vous gérez cet événement, l’obtention de la valeur d’une cellule <xref:System.Windows.Forms.DataGridViewCell.ToolTipText%2A> propriété déclenche l’événement et retourne la valeur de la <xref:System.Windows.Forms.DataGridViewCellToolTipTextNeededEventArgs.ToolTipText%2A?displayProperty=nameWithType> de la propriété spécifiée de l’événement gestionnaire.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.ShowCellToolTips%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.CellToolTipTextNeeded?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewCell>
- <xref:System.Windows.Forms.DataGridViewCell.ToolTipText%2A?displayProperty=nameWithType>
- [Programmation avec les cellules, lignes et colonnes dans le contrôle DataGridView Windows Forms](programming-with-cells-rows-and-columns-in-the-datagrid.md)
