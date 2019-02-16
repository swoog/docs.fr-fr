---
title: 'Procédure : Définir des Styles de cellules par défaut et les Formats de données pour le contrôle de DataGridView Windows Forms à l’aide du Concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], cell styles
- cells [Windows Forms], setting styles
- data formats
- data [Windows Forms], setting formats
ms.assetid: fc6da49f-8942-41da-b49f-b2afc38cc656
ms.openlocfilehash: 4a4cd1e7582e6e7443ceb1f4188eb3359638d8df
ms.sourcegitcommit: 0069cb3de8eed4e92b2195d29e5769a76111acdd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/16/2019
ms.locfileid: "56332206"
---
# <a name="how-to-set-default-cell-styles-and-data-formats-for-the-windows-forms-datagridview-control-using-the-designer"></a>Procédure : Définir des Styles de cellules par défaut et les Formats de données pour le contrôle de DataGridView Windows Forms à l’aide du Concepteur
Le <xref:System.Windows.Forms.DataGridView> contrôle vous permet de spécifier des styles de cellules par défaut et les formats de données pour l’ensemble du contrôle pour des colonnes spécifiques, pour les en-têtes de lignes et de colonnes et de lignes pour créer un effet de livre de remplacement de la cellule. Les styles par défaut définie pour l’ensemble du contrôle sont remplacées par les styles par défaut définis pour les colonnes et lignes en alternance. En outre, les styles que vous définissez dans le code des lignes individuelles et des cellules remplacent les styles par défaut.  
  
 Pour plus d’informations sur les styles de cellules, consultez [Styles de cellules dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/cell-styles-in-the-windows-forms-datagridview-control.md). Pour définir des styles pour les lignes de remplacement, consultez [Comment : Définir des Styles de la ligne en alternance pour le Windows Forms DataGridView Control à l’aide du concepteur](../../../../docs/framework/winforms/controls/set-alternating-row-styles-for-the-datagrid-using-the-designer.md).  
  
 Vous pouvez également définir des styles à l’aide de la <xref:System.Windows.Forms.DataGridView.RowTemplate%2A> affecter toutes les lignes qui seront ajoutés au contrôle. Pour plus d’informations sur le modèle de ligne, consultez [Comment : Utiliser le modèle de ligne pour personnaliser les lignes dans le contrôle de DataGridView Windows Forms](../../../../docs/framework/winforms/controls/use-the-row-template-to-customize-rows-in-the-datagrid.md).  
  
 Les procédures suivantes nécessitent un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.DataGridView> contrôle. Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-set-default-styles-for-all-cells-in-the-control"></a>Pour définir des styles par défaut pour toutes les cellules dans le contrôle  
  
1.  Sélectionnez le <xref:System.Windows.Forms.DataGridView> contrôle dans le concepteur.  
  
2.  Dans le **propriétés** fenêtre, cliquez sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) à côté du <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A>, <xref:System.Windows.Forms.DataGridView.ColumnHeadersDefaultCellStyle%2A>, ou <xref:System.Windows.Forms.DataGridView.RowHeadersDefaultCellStyle%2A> propriété. Le **Générateur CellStyle** boîte de dialogue s’affiche.  
  
3.  Définir le style en définissant les propriétés, à l’aide de la **aperçu** volet pour confirmer votre choix.  
  
> [!NOTE]
>  Si les styles visuels sont activés, les en-têtes de lignes et de colonnes (à l’exception de la <xref:System.Windows.Forms.DataGridView.TopLeftHeaderCell%2A>) sont automatiquement un style du thème actuel, remplaçant la <xref:System.Windows.Forms.DataGridView.ColumnHeadersDefaultCellStyle%2A> et <xref:System.Windows.Forms.DataGridView.RowHeadersDefaultCellStyle%2A> les valeurs de propriété.  
>   
>  Vous pouvez définir des styles de cellules pour plusieurs sélectionné <xref:System.Windows.Forms.DataGridView> contrôle à l’aide du concepteur, mais uniquement s’ils ont des valeurs identiques pour la propriété de style de cellule à modifier. Si les styles de cellules diffèrent pour cette propriété, le **propriétés** windows de le **Générateur CellStyle** boîte de dialogue sera vide.  
  
### <a name="to-set-default-styles-for-cells-in-individual-columns"></a>Pour définir des styles par défaut de cellules dans les colonnes individuelles  
  
1.  Cliquez sur le <xref:System.Windows.Forms.DataGridView> contrôler dans le concepteur et choisissez **modifier les colonnes**.  
  
2.  Sélectionnez une colonne dans la **colonnes sélectionnées** liste.  
  
3.  Dans le **propriétés de la colonne** grille, cliquez sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) à côté du <xref:System.Windows.Forms.DataGridViewColumn.DefaultCellStyle%2A> propriété. Le **Générateur CellStyle** boîte de dialogue s’affiche.  
  
4.  Définir le style en définissant les propriétés, à l’aide de la **aperçu** volet pour confirmer votre choix.  
  
### <a name="to-format-data-in-cells"></a>Mettre en forme les données dans les cellules  
  
1.  Utilisez une des procédures précédentes pour afficher un **Générateur CellStyle** boîte de dialogue liés à une propriété de style de cellule par défaut.  
  
2.  Dans le **Générateur CellStyle** boîte de dialogue, cliquez sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) à côté du <xref:System.Windows.Forms.DataGridViewCellStyle.Format%2A> propriété. Le **chaîne de Format** boîte de dialogue s’affiche.  
  
3.  Sélectionnez un type de format, puis modifier les détails du type (par exemple, le nombre de décimales à afficher), à l’aide de la **exemple** case pour confirmer votre choix.  
  
4.  Si vous liez le <xref:System.Windows.Forms.DataGridView> contrôle à une source de données qui est susceptible de contenir des valeurs null, renseignez le **valeur Null** zone de texte. Cette valeur est affichée lorsque la valeur de cellule est égale à une référence null (`Nothing` en Visual Basic) ou <xref:System.DBNull.Value?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewCellStyle>
- <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.RowsDefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.DefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewCellStyle.Format%2A?displayProperty=nameWithType>
- [Styles de cellules dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/cell-styles-in-the-windows-forms-datagridview-control.md)
- [Guide pratique pour Définir les Styles de ligne en alternance pour le contrôle de DataGridView Windows Forms à l’aide du Concepteur](../../../../docs/framework/winforms/controls/set-alternating-row-styles-for-the-datagrid-using-the-designer.md)
- [Guide pratique pour Créer un projet Application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [Guide pratique pour Ajouter des contrôles aux Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)
