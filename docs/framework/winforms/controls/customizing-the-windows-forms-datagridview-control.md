---
title: Personnalisation du contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- data grids [Windows Forms], customization
- DataGridView control [Windows Forms], customization
ms.assetid: 01ea5d4c-a736-4596-b0e9-a67a1b86e15f
ms.openlocfilehash: ab8d1f07c608aca4f14f5e73860f8c3e263a4610
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59091380"
---
# <a name="customizing-the-windows-forms-datagridview-control"></a>Personnalisation du contrôle DataGridView Windows Forms
Le `DataGridView` contrôle fournit plusieurs propriétés que vous pouvez utiliser pour ajuster l’apparence et le comportement de base (aspect) de ses cellules, lignes et des colonnes. Si vous avez des besoins particuliers qui vont au-delà des capacités de la <xref:System.Windows.Forms.DataGridViewCellStyle> class, toutefois, vous pouvez également implémenter le dessin owner-drawn pour le contrôle ou étendre ses fonctionnalités en créant des cellules personnalisés, des colonnes et des lignes.  
  
 Pour peindre des cellules et des lignes vous-même, vous pouvez gérer différents `DataGridView` événements de peinture. Pour modifier des fonctionnalités existantes ou fournir de nouvelles fonctionnalités, vous pouvez créer vos propres types dérivés d’existant `DataGridViewCell`, `DataGridViewColumn`, et `DataGridViewRow` types. Vous pouvez également fournir les nouvelles fonctionnalités de modification en créant des types dérivés qui affichent un contrôle de votre choix lorsqu’une cellule est en mode édition.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Procédure : personnaliser l’aspect des cellules dans le contrôle DataGridView Windows Forms](customize-the-appearance-of-cells-in-the-datagrid.md)  
 Décrit comment gérer les <xref:System.Windows.Forms.DataGridView.CellPainting> événement pour peindre les cellules manuellement.  
  
 [Procédure : personnaliser l’aspect des lignes dans le contrôle DataGridView Windows Forms](customize-the-appearance-of-rows-in-the-datagrid.md)  
 Décrit comment gérer les <xref:System.Windows.Forms.DataGridView.RowPrePaint> et <xref:System.Windows.Forms.DataGridView.RowPostPaint> événements afin de peindre les lignes avec un arrière-plan dégradé personnalisé et un contenu qui s’étend sur plusieurs colonnes.  
  
 [Procédure : personnaliser des cellules et des colonnes dans le contrôle DataGridView Windows Forms en développant leur comportement et leur aspect](customize-cells-and-columns-in-the-datagrid-by-extending-behavior.md)  
 Décrit comment créer des types personnalisés dérivés de `DataGridViewCell` et `DataGridViewColumn` afin de mettre en surbrillance les cellules lorsque le pointeur de la souris est placé dessus.  
  
 [Procédure : désactiver des boutons dans une colonne de boutons dans le contrôle DataGridView Windows Forms](disable-buttons-in-a-button-column-in-the-datagrid.md)  
 Décrit comment créer des types personnalisés dérivés de <xref:System.Windows.Forms.DataGridViewButtonCell> et <xref:System.Windows.Forms.DataGridViewButtonColumn> afin d’afficher les boutons désactivés dans une colonne de boutons.  
  
 [Procédure : héberger des contrôles dans des cellules DataGridView Windows Forms](how-to-host-controls-in-windows-forms-datagridview-cells.md)  
 Décrit comment implémenter le `IDataGridViewEditingControl` interface et créer des types personnalisés dérivés de `DataGridViewCell` et `DataGridViewColumn` afin d’afficher un <xref:System.Windows.Forms.DateTimePicker> contrôler lorsqu’une cellule est en mode édition.  
  
## <a name="reference"></a>Référence  
 <xref:System.Windows.Forms.DataGridView>  
 Fournit une documentation de référence pour le contrôle <xref:System.Windows.Forms.DataGridView>.  
  
 <xref:System.Windows.Forms.DataGridViewCell>  
 Fournit la documentation de référence pour la <xref:System.Windows.Forms.DataGridViewCell> classe.  
  
 <xref:System.Windows.Forms.DataGridViewRow>  
 Fournit la documentation de référence pour la <xref:System.Windows.Forms.DataGridViewRow> classe.  
  
 <xref:System.Windows.Forms.DataGridViewColumn>  
 Fournit la documentation de référence pour la <xref:System.Windows.Forms.DataGridViewColumn> classe.  
  
 <xref:System.Windows.Forms.IDataGridViewEditingControl>  
 Fournit la documentation de référence pour le <xref:System.Windows.Forms.IDataGridViewEditingControl> interface.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Mises en forme et styles de base dans le contrôle DataGridView Windows Forms](basic-formatting-and-styling-in-the-windows-forms-datagridview-control.md)  
 Fournit des rubriques qui décrivent comment modifier l'apparence de base du contrôle et le format d'affichage des données de cellules.  
  
## <a name="see-also"></a>Voir aussi

- [DataGridView, contrôle](datagridview-control-windows-forms.md)
- [Types de colonnes dans le contrôle DataGridView Windows Forms](column-types-in-the-windows-forms-datagridview-control.md)
