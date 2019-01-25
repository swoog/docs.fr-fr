---
title: 'Procédure : Personnaliser l’apparence des lignes dans le contrôle de DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], customizing rows
- rows [Windows Forms], customizing in DataGridView control
- DataGridView control [Windows Forms], customizing rows
ms.assetid: d40b53d2-7e7c-48c5-8570-6e79d15c3bbb
ms.openlocfilehash: 6ec3765eb667f8a249afa815400eb7f1edbec3dc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54632944"
---
# <a name="how-to-customize-the-appearance-of-rows-in-the-windows-forms-datagridview-control"></a>Procédure : Personnaliser l’apparence des lignes dans le contrôle de DataGridView Windows Forms
Vous pouvez contrôler l'apparence des lignes <xref:System.Windows.Forms.DataGridView> en gérant l'un ou l'autre des événements <xref:System.Windows.Forms.DataGridView.RowPrePaint?displayProperty=nameWithType> et <xref:System.Windows.Forms.DataGridView.RowPostPaint?displayProperty=nameWithType> (ou les deux). Ces événements sont conçus pour que vous puissiez peindre uniquement ce que vous souhaitez, tout en laissant le contrôle <xref:System.Windows.Forms.DataGridView> peindre le reste. Par exemple, si vous souhaitez peindre un arrière-plan personnalisé, vous pouvez gérer l'événement <xref:System.Windows.Forms.DataGridView.RowPrePaint?displayProperty=nameWithType> et laisser chaque cellule peindre son propre contenu de premier plan. Vous pouvez également laisser les cellules se peindre elles-mêmes et ajouter du contenu de premier plan personnalisé dans un gestionnaire pour l'événement <xref:System.Windows.Forms.DataGridView.RowPostPaint?displayProperty=nameWithType>. Vous pouvez aussi désactiver la peinture des cellules et peindre tout vous-même dans un gestionnaire d'événements <xref:System.Windows.Forms.DataGridView.RowPrePaint?displayProperty=nameWithType>.  
  
 L'exemple de code suivant implémente des gestionnaires pour les deux événements pour fournir un arrière-plan de sélection dégradé et du contenu de premier plan personnalisé qui s'étend sur plusieurs colonnes.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.DataGridViewRowPainting#00](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRowPainting/CS/datagridviewrowpainting.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewRowPainting#00](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRowPainting/VB/datagridviewrowpainting.vb#00)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux assemblys System, System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  Voir également [Guide pratique pour Compiler et exécuter un exemple de Code complet de Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.RowPrePaint?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.RowPostPaint?displayProperty=nameWithType>
- [Personnalisation du contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/customizing-the-windows-forms-datagridview-control.md)
- [Architecture du contrôle DataGridView](../../../../docs/framework/winforms/controls/datagridview-control-architecture-windows-forms.md)
