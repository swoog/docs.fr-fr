---
title: 'Procédure : Effectuer une Action personnalisée basée sur les modifications apportées dans une cellule d’un contrôle de DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- cells [Windows Forms], detecting changes
- DataGridView control [Windows Forms], detecting changes in cells
- data grids [Windows Forms], detecting changes in cells
ms.assetid: 7fa44d01-97f4-4ccb-a149-bc72628d2c36
ms.openlocfilehash: ad1c60c34fc5461de21e2ad5d4d02f5b2abd6dfd
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57705582"
---
# <a name="how-to-perform-a-custom-action-based-on-changes-in-a-cell-of-a-windows-forms-datagridview-control"></a>Procédure : Effectuer une Action personnalisée basée sur les modifications apportées dans une cellule d’un contrôle de DataGridView Windows Forms
Le <xref:System.Windows.Forms.DataGridView> contrôle a un nombre d’événements que vous pouvez utiliser pour détecter des modifications dans l’état de <xref:System.Windows.Forms.DataGridView> cellules. Les deux les plus couramment utilisés sont les <xref:System.Windows.Forms.DataGridView.CellValueChanged> et <xref:System.Windows.Forms.DataGridView.CellStateChanged> événements.  
  
### <a name="to-detect-changes-in-the-values-of-datagridview-cells"></a>Pour détecter des modifications dans les valeurs des cellules DataGridView  
  
-   Écrire un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.CellValueChanged> événement.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#130](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#130)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#130](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#130)]  
  
### <a name="to-detect-changes-in-the-states-of-datagridview-cells"></a>Pour détecter des modifications dans les États des cellules DataGridView  
  
-   Écrire un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.CellStateChanged> événement.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#135](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#135)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#135](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#135)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ; Pour C#, les gestionnaires d’événements doivent être connectés pour les événements correspondants.  
  
-   des références aux assemblys <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.CellValueChanged?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.CellStateChanged?displayProperty=nameWithType>
- [Programmation avec les cellules, lignes et colonnes dans le contrôle DataGridView Windows Forms](programming-with-cells-rows-and-columns-in-the-datagrid.md)
- [Procédure pas à pas : Validation des données dans le contrôle DataGridView Windows Forms](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)
