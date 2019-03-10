---
title: 'Procédure : Personnaliser l’apparence des cellules dans le contrôle de DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], customizing cells
- DataGridView control [Windows Forms], customizing cells
- cells [Windows Forms], customizing in DataGridView control
ms.assetid: 478b20c9-625c-4116-9c5c-5a16e6f4ec67
ms.openlocfilehash: add865eedc54253ad257e0e142e555da52f341dd
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57703346"
---
# <a name="how-to-customize-the-appearance-of-cells-in-the-windows-forms-datagridview-control"></a>Procédure : Personnaliser l’apparence des cellules dans le contrôle de DataGridView Windows Forms
Vous pouvez personnaliser l’apparence de n’importe quelle cellule en gérant la <xref:System.Windows.Forms.DataGridView> du contrôle <xref:System.Windows.Forms.DataGridView.CellPainting> événement. Vous pouvez extraire le <xref:System.Windows.Forms.DataGridView> du contrôle <xref:System.Drawing.Graphics> à partir de la <xref:System.Windows.Forms.DataGridViewCellPaintingEventArgs.Graphics%2A> propriété de la <xref:System.Windows.Forms.DataGridViewCellPaintingEventArgs>. Avec cette <xref:System.Drawing.Graphics>, vous pouvez affecter l’apparence de tout le <xref:System.Windows.Forms.DataGridView> contrôle, mais vous souhaiterez habituellement affectent uniquement l’apparence de la cellule qui est actuellement peint. Le <xref:System.Windows.Forms.DataGridViewCellPaintingEventArgs.ClipBounds%2A> propriété de la <xref:System.Windows.Forms.DataGridViewCellPaintingEventArgs> vous permet de limiter vos opérations de peinture à la cellule qui est actuellement peint.  
  
 Dans l’exemple de code suivant, vous sera chargée de peindre toutes les cellules dans un `ContactName` à l’aide de la colonne la <xref:System.Windows.Forms.DataGridView> modèle de couleurs du contrôle. Contenu de texte de chaque cellule est peint dans <xref:System.Drawing.Color.Crimson%2A>, et un rectangle d’incrustation est dessiné dans la même couleur que le <xref:System.Windows.Forms.DataGridView> du contrôle <xref:System.Windows.Forms.DataGridView.GridColor%2A> propriété.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.DataGridViewCellPainting#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCellPainting/CS/form1.cs#10)]
 [!code-vb[System.Windows.Forms.DataGridViewCellPainting#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCellPainting/VB/form1.vb#10)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Un <xref:System.Windows.Forms.DataGridView> contrôle nommé `dataGridView1` avec un `ContactName` colonne tel que celui de la table Customers dans la base de données Northwind.  
  
-   Références aux assemblys System, System.Windows.Form et System.Drawing.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.CellPainting>
- [Personnalisation du contrôle DataGridView Windows Forms](customizing-the-windows-forms-datagridview-control.md)
