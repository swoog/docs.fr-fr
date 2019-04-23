---
title: 'Procédure : accéder à des objets liés à des lignes DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- object binding [Windows Forms], accessing bound objects
- data grids [Windows Forms], accessing bound objects
- DataGridView control [Windows Forms], accessing objects bound to rows
ms.assetid: 0e05748f-4403-4eb8-8b2f-b098108181b5
ms.openlocfilehash: 50882ab9a1a498bf8f76381e3f4aac53876abbb8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59217404"
---
# <a name="how-to-access-objects-bound-to-windows-forms-datagridview-rows"></a>Procédure : accéder à des objets liés à des lignes DataGridView Windows Forms
Il est parfois utile d’afficher une table d’informations stockée dans une collection d’objets métier. Quand vous liez un contrôle <xref:System.Windows.Forms.DataGridView> à une telle collection, chaque propriété publique est affichée dans sa propre colonne, à moins que la propriété n'ait été marquée comme non consultable avec un <xref:System.ComponentModel.BrowsableAttribute>. Par exemple, une collection d’objets `Customer` aurait des colonnes telles que **Nom** et **Adresse**.  
  
 Si ces objets contiennent des informations supplémentaires et du code auquel vous souhaitez accéder, vous pouvez l'atteindre via des objets de ligne. Dans l'exemple de code suivant, les utilisateurs peuvent sélectionner plusieurs lignes et cliquer sur un bouton pour envoyer une facture à chacun des clients correspondants.  
  
### <a name="to-access-row-bound-objects"></a>Pour accéder à des objets liés à une ligne  
  
-   Utilisez la propriété <xref:System.Windows.Forms.DataGridViewRow.DataBoundItem%2A?displayProperty=nameWithType>.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewObjectBinding#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewObjectBinding/CS/datagridviewobjectbinding.cs#10)]
     [!code-vb[System.Windows.Forms.DataGridViewObjectBinding#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewObjectBinding/VB/datagridviewobjectbinding.vb#10)]  
  
## <a name="example"></a>Exemple  
 L'exemple de code complet comprend une implémentation `Customer` simple et lie le <xref:System.Windows.Forms.DataGridView> à un <xref:System.Collections.ArrayList> contenant quelques objets `Customer`. Le gestionnaire d’événements <xref:System.Windows.Forms.Control.Click> du <xref:System.Windows.Forms.Button?displayProperty=nameWithType> doit accéder aux objets `Customer` par l’intermédiaire des lignes, car la collection de clients n’est pas accessible en dehors du gestionnaire d’événements <xref:System.Windows.Forms.Form.Load?displayProperty=nameWithType>.  
  
 [!code-csharp[System.Windows.Forms.DataGridViewObjectBinding#00](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewObjectBinding/CS/datagridviewobjectbinding.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewObjectBinding#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewObjectBinding/VB/datagridviewobjectbinding.vb#00)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   des références aux assemblys System et System.Windows.Forms ;  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewRow>
- <xref:System.Windows.Forms.DataGridViewRow.DataBoundItem%2A?displayProperty=nameWithType>
- [Affichage des données dans le contrôle DataGridView Windows Forms](displaying-data-in-the-windows-forms-datagridview-control.md)
- [Guide pratique pour Lier des objets aux contrôles DataGridView de Windows Forms](how-to-bind-objects-to-windows-forms-datagridview-controls.md)
