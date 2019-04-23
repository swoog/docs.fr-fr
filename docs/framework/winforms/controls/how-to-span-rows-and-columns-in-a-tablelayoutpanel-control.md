---
title: 'Procédure : étendre des lignes et des colonnes dans un contrôle TableLayoutPanel'
ms.date: 03/30/2017
f1_keywords:
- net.ComponentModel.StyleCollectionEditor.TLP.SpanRowsColumns
helpviewer_keywords:
- columns [Windows Forms], spanning
- merging cells
- TableLayoutPanel control [Windows Forms], spanning rows and columns
- rows [Windows Forms], spanning
- cells [Windows Forms], merging
ms.assetid: a8a2fdd3-a848-48b0-a4cd-4e85ebded87e
ms.openlocfilehash: 02db78b07930676235e55e535fb24f6ff618d823
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59339019"
---
# <a name="how-to-span-rows-and-columns-in-a-tablelayoutpanel-control"></a>Procédure : étendre des lignes et des colonnes dans un contrôle TableLayoutPanel
Contrôles dans un <xref:System.Windows.Forms.TableLayoutPanel> contrôle peut s’étendre sur les lignes et colonnes adjacentes.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-span-columns-and-rows"></a>Pour couvrir des colonnes et lignes  
  
1. Faites glisser un contrôle <xref:System.Windows.Forms.TableLayoutPanel> de la **boîte à outils** vers le formulaire.  
  
2. Faites glisser un <xref:System.Windows.Forms.Button> contrôler à partir de la **boîte à outils** dans la cellule supérieure gauche de la <xref:System.Windows.Forms.TableLayoutPanel> contrôle.  
  
3. Définir le <xref:System.Windows.Forms.Button> du contrôle **ColumnSpan** propriété **2**. Notez que le <xref:System.Windows.Forms.Button> contrôle s’étend sur les première et deuxième colonnes.  
  
4. Définir le <xref:System.Windows.Forms.Button> du contrôle **RowSpan** propriété **2**. Notez que le <xref:System.Windows.Forms.Button> contrôle s’étend sur les première et deuxième lignes.  
  
5. Définir le <xref:System.Windows.Forms.Button> du contrôle **ColumnSpan** propriété **1**. Notez que le <xref:System.Windows.Forms.Button> contrôle se déplace dans la première colonne et couvre les première et deuxième lignes.  
  
## <a name="see-also"></a>Voir aussi

- [TableLayoutPanel, contrôle](tablelayoutpanel-control-windows-forms.md)
