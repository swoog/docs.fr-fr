---
title: 'Comment : aligner un contrôle sur les bords des formulaires au moment du design'
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], docking using designer
- Dock property [Windows Forms], aligning controls (using designer)
ms.assetid: 51f08998-5e3b-4330-be58-a4edd0eb60f4
ms.openlocfilehash: 513029c1bd5cc4af52fcee97f7fab961729e613c
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44277086"
---
# <a name="how-to-align-a-control-to-the-edges-of-forms-at-design-time"></a>Comment : aligner un contrôle sur les bords des formulaires au moment du design
Vous pouvez aligner un contrôle sur le bord de vos formulaires en définissant le <xref:System.Windows.Forms.Control.Dock%2A>. Cette propriété désigne l’emplacement de votre contrôle dans le formulaire. La propriété <xref:System.Windows.Forms.Control.Dock%2A> peut avoir les valeurs suivantes :  
  
|Paramètre|Effet sur le contrôle|  
|-------------|----------------------------|  
|<xref:System.Windows.Forms.DockStyle.Bottom>|S'ancre en bas du formulaire.|  
|<xref:System.Windows.Forms.DockStyle.Fill>|Remplit tout l'espace restant dans le formulaire.|  
|<xref:System.Windows.Forms.DockStyle.Left>|S'ancre sur le côté gauche du formulaire.|  
|<xref:System.Windows.Forms.DockStyle.None>|Ne s’ancre en tout lieu et il s’affiche à l’emplacement spécifié par son <xref:System.Windows.Forms.Control.Location%2A>.|  
|<xref:System.Windows.Forms.DockStyle.Right>|S'ancre sur le côté droit du formulaire.|  
|<xref:System.Windows.Forms.DockStyle.Top>|S'ancre en haut du formulaire.|  
  
 Ces valeurs peuvent également être définies dans le code. Pour plus d’informations, consultez [Comment : aligner un contrôle sur les bords des formulaires](../../../../docs/framework/winforms/controls/how-to-align-a-control-to-the-edges-of-forms.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-set-the-dock-property-for-your-control-at-design-time"></a>Pour définir la propriété Dock de votre contrôle au moment du design  
  
1.  Dans le Concepteur Windows Forms, sélectionnez votre contrôle.  
  
2.  Dans le **propriétés** , cliquez sur la liste déroulante située en regard du <xref:System.Windows.Forms.Control.Dock%2A> propriété.  
  
     Une interface graphique représentant les six possibles <xref:System.Windows.Forms.Control.Dock%2A> paramètres s’affiche.  
  
3.  Choisissez le paramètre approprié.  
  
4.  Votre contrôle s’ancre maintenant de la manière spécifiée par le paramètre.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.Control.Dock%2A?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.Control.Anchor%2A?displayProperty=nameWithType>  
 [Guide pratique pour aligner un contrôle sur les bords des formulaires](../../../../docs/framework/winforms/controls/how-to-align-a-control-to-the-edges-of-forms.md)  
 [Procédure pas à pas : organisation des contrôles dans les Windows Forms à l’aide des lignes d’alignement](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)  
 [Guide pratique pour ancrer des contrôles sur des Windows Forms](../../../../docs/framework/winforms/controls/how-to-anchor-controls-on-windows-forms.md)  
 [Guide pratique pour ancrer et arrimer des contrôles enfants dans un contrôle TableLayoutPanel](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)  
 [Guide pratique pour ancrer des contrôles enfants dans un contrôle FlowLayoutPanel](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)  
 [Procédure pas à pas : organisation des contrôles dans les Windows Forms à l’aide d’un TableLayoutPanel](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)  
 [Procédure pas à pas : organisation des contrôles dans les Windows Forms à l’aide d’un FlowLayoutPanel](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)  
 [Développement de contrôles Windows Forms au moment du design](../../../../docs/framework/winforms/controls/developing-windows-forms-controls-at-design-time.md)
