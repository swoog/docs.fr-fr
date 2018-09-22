---
title: "Comment : définir des styles de ligne en alternance pour le contrôle DataGridView Windows Forms à l'aide du concepteur"
ms.date: 03/30/2017
helpviewer_keywords:
- ledger-like formats
- DataGridView control [Windows Forms], row style alternation
- Windows Forms, rows
- rows [Windows Forms], alternating
- data [Windows Forms], displaying
ms.assetid: 02373442-bf94-4470-9f8a-e44c4a9d5b88
ms.openlocfilehash: 5807df6d11580c22f2b754faf44fb3aa63dee14e
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2018
ms.locfileid: "46584316"
---
# <a name="how-to-set-alternating-row-styles-for-the-windows-forms-datagridview-control-using-the-designer"></a>Comment : définir des styles de ligne en alternance pour le contrôle DataGridView Windows Forms à l'aide du concepteur
Données tabulaires sont souvent présentées dans un format de type livre comptable où les lignes en alternance ont différentes couleurs d’arrière-plan. Avec ce format, il est facile pour les utilisateurs de déterminer quelle cellule appartient à quelle ligne, en particulier dans les tableaux larges qui ont beaucoup de colonnes.  
  
 Avec le contrôle <xref:System.Windows.Forms.DataGridView>, vous pouvez spécifier des informations de style complètes pour les lignes en alternance. Vous pouvez utiliser des caractéristiques de style comme la couleur de premier plan et la police, en plus de la couleur d’arrière-plan, pour différencier les lignes en alternance. Pour plus d’informations, consultez [Styles de cellules dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/cell-styles-in-the-windows-forms-datagridview-control.md).  
  
 La procédure suivante nécessite un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.DataGridView> contrôle. Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : créer un projet d’Application Windows](https://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa) et [Comment : ajouter des contrôles aux Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="define-styles-for-alternating-rows"></a>Définir des styles pour les lignes en alternance  
  
1.  Sélectionnez le <xref:System.Windows.Forms.DataGridView> contrôle dans le concepteur.  
  
2.  Dans le **propriétés** fenêtre, cliquez sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) à côté du <xref:System.Windows.Forms.DataGridView.AlternatingRowsDefaultCellStyle%2A> propriété.  
  
3.  Dans le **Générateur CellStyle** boîte de dialogue Définir le style en définissant les propriétés et utilisez le **aperçu** volet pour confirmer votre choix. Les styles que vous spécifiez sont utilisés pour chaque autre ligne affichée dans le contrôle, en commençant par la deuxième.  
  
4.  Pour définir des styles pour les lignes restantes, répétez les étapes 2 et 3 à l’aide de la <xref:System.Windows.Forms.DataGridView.RowsDefaultCellStyle%2A> propriété.  
  
    > [!NOTE]
    >  Les cellules sont affichés à l’aide de styles hérités de plusieurs propriétés. Pour plus d’informations sur l’héritage de style, consultez [Styles de cellules dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/cell-styles-in-the-windows-forms-datagridview-control.md).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.DataGridView>  
 [Styles de cellules dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/cell-styles-in-the-windows-forms-datagridview-control.md)  
 [Mises en forme et styles de base dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/basic-formatting-and-styling-in-the-windows-forms-datagridview-control.md)  
 [Utilisation du concepteur avec le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/using-the-designer-with-the-windows-forms-datagridview-control.md)  
 [Comment : créer un projet d’Application Windows](https://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa)  
 [Comment : ajouter des contrôles à des Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)
