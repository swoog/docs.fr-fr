---
title: 'Comment : modifier des colonnes et des lignes dans un contrôle TableLayoutPanel'
ms.date: 03/30/2017
f1_keywords:
- net.ComponentModel.StyleCollectionEditor
helpviewer_keywords:
- columns [Windows Forms], editing
- TableLayoutPanel control [Windows Forms], editing
- rows [Windows Forms], editing
ms.assetid: c367ed43-40dc-49eb-9e0f-ba70e83dfec0
ms.openlocfilehash: 820d2f98290650bfaf377bd2d4b863dfb2e6e704
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43500782"
---
# <a name="how-to-edit-columns-and-rows-in-a-tablelayoutpanel-control"></a>Comment : modifier des colonnes et des lignes dans un contrôle TableLayoutPanel
Vous pouvez utiliser l’éditeur de collections de la <xref:System.Windows.Forms.TableLayoutPanel> contrôle, appelé le **Styles de ligne et colonne** boîte de dialogue pour modifier les lignes et colonnes de vos contrôles.  
  
> [!NOTE]
>  Si vous souhaitez un contrôle pour s’étendre sur plusieurs lignes ou colonnes, définissez la `RowSpan` et `ColumnSpan` propriétés sur le contrôle. Pour plus d'informations, consultez [Walkthrough: Arranging Controls on Windows Forms Using a TableLayoutPanel](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md).  
>   
>  Si vous souhaitez aligner un contrôle dans une cellule, ou si vous souhaitez un contrôle à étendre au sein d’une cellule, utilisez le contrôle <xref:System.Windows.Forms.Control.Anchor%2A> propriété. Pour plus d'informations, consultez [Walkthrough: Arranging Controls on Windows Forms Using a TableLayoutPanel](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md).  
>   
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-edit-rows-and-columns"></a>Pour modifier les lignes et colonnes  
  
1.  Faites glisser un <xref:System.Windows.Forms.TableLayoutPanel> contrôle depuis la **boîte à outils** vers votre formulaire.  
  
2.  Cliquez sur le <xref:System.Windows.Forms.TableLayoutPanel> glyphe de balise active du contrôle (![glyphe de balise active](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) et sélectionnez **modifier les lignes et colonnes** pour ouvrir le  **Styles de ligne et colonne** boîte de dialogue. Vous pouvez également avec le bouton droit sur le <xref:System.Windows.Forms.TableLayoutPanel> contrôler et sélectionnez **modifier les lignes et colonnes** dans le menu contextuel.  
  
3.  Pour ajouter ou supprimer des colonnes, sélectionnez **colonnes** à partir de la **type de membre** zone de liste déroulante.  
  
4.  Pour ajouter ou supprimer des lignes, sélectionnez **lignes** à partir de la **type de membre** zone de liste déroulante.  
  
5.  Cliquez sur le **ajouter** pour ajouter une ligne ou une colonne à la fin de la **membre** liste.  
  
6.  Cliquez sur le **insérer** pour ajouter une ligne ou une colonne avant l’élément actuellement sélectionné dans la liste.  
  
7.  Si vous ajoutez une ligne ou colonne, sélectionnez le **taille Type** pour la nouvelle ligne ou la colonne. Pour plus d'informations, consultez <xref:System.Windows.Forms.SizeType>.  
  
8.  Pour supprimer une ligne ou colonne, cliquez sur le **supprimer** bouton pour supprimer l’élément actuellement sélectionné dans le **membre** liste.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.SizeType>  
 [TableLayoutPanel, contrôle](../../../../docs/framework/winforms/controls/tablelayoutpanel-control-windows-forms.md)
