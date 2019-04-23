---
title: 'Procédure : modifier l’ordre des colonnes dans le contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- columns [Windows Forms], changing order
- DataGridView control [Windows Forms], column order
- data grids [Windows Forms], changing column order
ms.assetid: 5e9ac3bc-b0f0-48cb-a3d5-b005af905395
ms.openlocfilehash: 90d262e738f092215e88e38e31169d74059e4401
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59228794"
---
# <a name="how-to-change-the-order-of-columns-in-the-windows-forms-datagridview-control"></a>Procédure : modifier l’ordre des colonnes dans le contrôle DataGridView Windows Forms
Quand vous utilisez un <xref:System.Windows.Forms.DataGridView> pour afficher des données à partir d'une source de données, les colonnes du schéma de la source de données apparaissent parfois dans un ordre différent de celui souhaité. Vous pouvez modifier l'ordre des colonnes à l'aide de la propriété <xref:System.Windows.Forms.DataGridViewColumn.DisplayIndex%2A> de la classe <xref:System.Windows.Forms.DataGridViewColumn>.  
  
 L’exemple de code suivant repositionne quelques-unes des colonnes générées automatiquement lors de la liaison à la table Customers dans l’exemple de base de données Northwind. Pour plus d’informations sur la façon de lier le <xref:System.Windows.Forms.DataGridView> le contrôle à une table de base de données, consultez [Comment : Lier des données pour les Windows Forms DataGridView Control](how-to-bind-data-to-the-windows-forms-datagridview-control.md).  
  
 Cette tâche est prise en charge dans Visual Studio.  Voir également [Guide pratique pour Modifier l’ordre des colonnes dans le contrôle de DataGridView Windows Forms à l’aide du concepteur](change-the-order-of-columns-in-the-datagrid-using-the-designer.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#040](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#040)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#040](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#040)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   un contrôle <xref:System.Windows.Forms.DataGridView> nommé `customersDataGridView` qui est lié à une table avec les noms de colonnes indiqués, comme la table `Customers` dans la base de données Northwind ;  
  
-   des références aux assemblys <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, <xref:System.Data?displayProperty=nameWithType> et <xref:System.Xml?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn>
- <xref:System.Windows.Forms.DataGridViewColumn.DisplayIndex%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.Visible%2A?displayProperty=nameWithType>
- [Affichage des données dans le contrôle DataGridView Windows Forms](displaying-data-in-the-windows-forms-datagridview-control.md)
- [Guide pratique pour Lier des données au contrôle DataGridView Windows Forms](how-to-bind-data-to-the-windows-forms-datagridview-control.md)
