---
title: 'Procédure : redimensionner automatiquement les cellules quand le contenu change dans le contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- data grids [Windows Forms], resizing cells automatically
- cells [Windows Forms], resizing automatically
- DataGridView control [Windows Forms], resizing cells
ms.assetid: 1d68934d-a04c-4b12-9e66-c856c6828131
ms.openlocfilehash: 436f5d4a77a3119fe5b16afa1a4e71c55b3751dc
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64587636"
---
# <a name="how-to-automatically-resize-cells-when-content-changes-in-the-windows-forms-datagridview-control"></a>Procédure : redimensionner automatiquement les cellules quand le contenu change dans le contrôle DataGridView Windows Forms
Vous pouvez configurer le contrôle <xref:System.Windows.Forms.DataGridView> pour redimensionner ses lignes, colonnes et en-têtes automatiquement chaque fois que du contenu change, pour que les cellules soient toujours assez grandes pour afficher leurs valeurs sans être découpées.  
  
 Vous disposez de nombreuses options pour limiter les cellules qui sont utilisées pour déterminer les nouvelles tailles. Par exemple, vous pouvez configurer le contrôle pour redimensionner automatiquement la largeur de ses colonnes uniquement en fonction des valeurs figurant sur les lignes qui sont affichées actuellement. Vous optimiserez ainsi les opérations lors de l'utilisation d'un nombre de lignes, bien que dans ce cas vous souhaiterez peut-être utiliser des méthodes de dimensionnement telles que <xref:System.Windows.Forms.DataGridView.AutoResizeColumns%2A> pour ajuster la taille quand bon vous semble.  
  
 Pour plus d’informations sur le redimensionnement automatique, consultez [les Options de dimensionnement dans le contrôle de DataGridView Windows Forms](sizing-options-in-the-windows-forms-datagridview-control.md).  
  
 L'exemple de code suivant illustre les options disponibles pour le redimensionnement automatique.  
  
## <a name="example"></a>Exemple  
 [!code-cpp[System.Windows.Forms.DataGridView.AutoSizing#0](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.AutoSizing/CPP/autosizing.cpp#0)]
 [!code-csharp[System.Windows.Forms.DataGridView.AutoSizing#0](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.AutoSizing/CS/autosizing.cs#0)]
 [!code-vb[System.Windows.Forms.DataGridView.AutoSizing#0](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.AutoSizing/VB/autosizing.vb#0)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
- Références aux assemblys System, System.Drawing et System.Windows.Forms.  
  
- Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.ColumnHeadersHeightSizeMode%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.RowHeadersWidthSizeMode%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.AutoSizeColumnsMode%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.AutoSizeRowsMode%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.AutoSizeMode%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.InheritedAutoSizeMode%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewAutoSizeRowsMode>
- <xref:System.Windows.Forms.DataGridViewAutoSizeColumnMode>
- <xref:System.Windows.Forms.DataGridViewAutoSizeColumnsMode>
- <xref:System.Windows.Forms.DataGridViewColumnHeadersHeightSizeMode>
- <xref:System.Windows.Forms.DataGridViewRowHeadersWidthSizeMode>
- [Redimensionnement des colonnes et des lignes dans le contrôle DataGridView Windows Forms](resizing-columns-and-rows-in-the-windows-forms-datagridview-control.md)
- [Options de dimensionnement dans le contrôle DataGridView Windows Forms](sizing-options-in-the-windows-forms-datagridview-control.md)
- [Guide pratique pour Redimensionner par programme les cellules en fonction du contenu dans le contrôle de DataGridView Windows Forms](programmatically-resize-cells-to-fit-content-in-the-datagrid.md)
