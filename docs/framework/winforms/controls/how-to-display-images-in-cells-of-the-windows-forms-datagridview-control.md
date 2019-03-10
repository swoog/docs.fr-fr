---
title: 'Procédure : Afficher des Images dans les cellules du contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- cells [Windows Forms], displaying images
- data grids [Windows Forms], displaying in grids
- DataGridView control [Windows Forms], displaying images
- data grids [Windows Forms], displaying images in cells
ms.assetid: 53b13d31-1b56-476d-9ab4-18bfac138a22
ms.openlocfilehash: 280f274a0957f098add7fbf2e3b919c33c4c5233
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57704400"
---
# <a name="how-to-display-images-in-cells-of-the-windows-forms-datagridview-control"></a>Procédure : Afficher des Images dans les cellules du contrôle DataGridView Windows Forms
Une image ou un graphique est une des valeurs que vous pouvez afficher dans une ligne de données. Souvent, ces graphiques prennent la forme d’une photographie de salarié ou un logo de société.  
  
 Incorporation d’images est simple lorsque vous affichez des données dans le <xref:System.Windows.Forms.DataGridView> contrôle. Le <xref:System.Windows.Forms.DataGridView> contrôle gère en mode natif n’importe quel format d’image pris en charge par le <xref:System.Drawing.Image> classe, ainsi que le OLE image format utilisé par certaines bases de données.  
  
 Si le <xref:System.Windows.Forms.DataGridView> source de données du contrôle a une colonne d’images, ils seront affichés automatiquement par le <xref:System.Windows.Forms.DataGridView> contrôle.  
  
 L’exemple de code suivant montre comment extraire une icône d’une ressource incorporée et la convertir en une image bitmap à afficher dans chaque cellule d’une colonne image. Pour un autre exemple qui remplace les valeurs de cellules textuelles avec images correspondantes, consultez [Comment : Personnaliser la mise en forme des données dans le contrôle de DataGridView Windows Forms](how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#050](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#050)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#050](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#050)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ;  
  
-   Une ressource d’icône incorporée nommée `tree.ico`.  
  
-   des références aux assemblys <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType> et <xref:System.Drawing?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- [Fonctionnalités de base liées aux colonnes, lignes et cellules dans le contrôle DataGridView Windows Forms](basic-column-row-and-cell-features-wf-datagridview-control.md)
- [Guide pratique pour Personnaliser la mise en forme des données dans le contrôle de DataGridView Windows Forms](how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md)
