---
title: 'Procédure : Spécifiez les valeurs par défaut pour les nouvelles lignes dans le contrôle de DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], default values for new rows
- DataGridView control [Windows Forms], data entry
- rows [Windows Forms], specifying default values
- DataGridView control [Windows Forms], default values for new rows
ms.assetid: 8d127963-d9f8-4e4e-9f7f-beb66688f1f2
ms.openlocfilehash: dab9ba7ca16cf0c886601e3c8fea579e70b2f30d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54596772"
---
# <a name="how-to-specify-default-values-for-new-rows-in-the-windows-forms-datagridview-control"></a>Procédure : Spécifiez les valeurs par défaut pour les nouvelles lignes dans le contrôle de DataGridView Windows Forms
Vous pouvez rendre saisie de données plus pratique lorsque l’application remplit par défaut des valeurs pour les nouvelles lignes ajoutées. Avec le <xref:System.Windows.Forms.DataGridView> (classe), vous pouvez remplir dans valeurs par défaut avec le <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> événement. Cet événement est déclenché lorsque l’utilisateur entre la ligne pour les nouveaux enregistrements. Lorsque votre code gère cet événement, vous pouvez remplir des cellules souhaitées avec des valeurs de votre choix.  
  
 L’exemple de code suivant montre comment spécifier des valeurs par défaut pour les nouvelles lignes à l’aide de la <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> événement.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#120](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#120)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#120](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#120)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ;  
  
-   Un `NewCustomerId` fonction permettant de générer unique `CustomerID` valeurs.  
  
-   des références aux assemblys <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded?displayProperty=nameWithType>
- [Saisie de données dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/data-entry-in-the-windows-forms-datagridview-control.md)
- [Utilisation de la ligne pour les nouveaux enregistrements dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/using-the-row-for-new-records-in-the-windows-forms-datagridview-control.md)
