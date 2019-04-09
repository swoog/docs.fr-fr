---
title: 'Procédure : empêcher l’ajout et la suppression de lignes dans le contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], disabling data entry
- data entry [Windows Forms], disabling in grids
- data grids [Windows Forms], disabling data entry
ms.assetid: ef9539ce-539b-404e-84b6-ac282b64b88c
ms.openlocfilehash: a80b10f2d3c2b6dea198fea83f1ffaaa358b68ea
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59147886"
---
# <a name="how-to-prevent-row-addition-and-deletion-in-the-windows-forms-datagridview-control"></a>Procédure : empêcher l’ajout et la suppression de lignes dans le contrôle DataGridView Windows Forms
Vous pouvez vouloir empêcher les utilisateurs d'ajouter de nouvelles lignes de données à votre contrôle <xref:System.Windows.Forms.DataGridView> ou d'en supprimer des lignes existantes. La propriété <xref:System.Windows.Forms.DataGridView.AllowUserToAddRows%2A> indique si la ligne des nouveaux enregistrements est présente au bas du contrôle, tandis que la propriété <xref:System.Windows.Forms.DataGridView.AllowUserToDeleteRows%2A> indique si les lignes peuvent être supprimées. L'exemple de code suivant utilise ces propriétés et définit également la propriété <xref:System.Windows.Forms.DataGridView.ReadOnly%2A> pour rendre le contrôle entièrement en lecture seule.  
  
 Cette tâche est prise en charge dans Visual Studio. Voir également [Guide pratique pour Empêcher l’ajout de ligne et de suppression dans les Windows Forms DataGridView Control à l’aide du concepteur](prevent-row-addition-and-deletion-in-the-datagrid-using-the-designer.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#090](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#090)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#090](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#090)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ;  
  
-   des références aux assemblys <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.AllowUserToAddRows%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.ReadOnly%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.AllowUserToAddRows%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.AllowUserToDeleteRows%2A?displayProperty=nameWithType>
- [Fonctionnalités de base liées aux colonnes, lignes et cellules dans le contrôle DataGridView Windows Forms](basic-column-row-and-cell-features-wf-datagridview-control.md)
