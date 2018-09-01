---
title: 'Comment : ancrer des contrôles aux Windows Forms'
ms.date: 03/30/2017
helpviewer_keywords:
- Anchor property [Windows Forms], enabling resizable forms
- Windows Forms controls, screen resolutions
- resizing forms [Windows Forms]
- Windows Forms controls, size
- screen resolution and control display
- controls [Windows Forms], anchoring
- forms [Windows Forms], resizing
- Windows Forms, resizing
- controls [Windows Forms], positioning
ms.assetid: 59ea914f-fbd3-427a-80fe-decd02f7ae6d
ms.openlocfilehash: c7658eb11e0d9e28c93b0a4b72a248cc42bc705f
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43389853"
---
# <a name="how-to-anchor-controls-on-windows-forms"></a>Comment : ancrer des contrôles aux Windows Forms
Si vous concevez un formulaire que l’utilisateur peut redimensionner en cours d’exécution, les contrôles sur votre formulaire doivent redimensionner et repositionner correctement. Pour redimensionner dynamiquement les contrôles dans le formulaire, vous pouvez utiliser le <xref:System.Windows.Forms.Control.Anchor%2A> propriété des contrôles Windows Forms. Le <xref:System.Windows.Forms.Control.Anchor%2A> propriété définit une position d’ancrage pour le contrôle. Lorsqu’un contrôle est ancré à un formulaire et le formulaire est redimensionné, le contrôle conserve la distance entre le contrôle et les positions d’ancrage. Par exemple, si vous avez un <xref:System.Windows.Forms.TextBox> contrôle est ancré à la gauche, droite et le bas du formulaire, comme le formulaire est redimensionné, le <xref:System.Windows.Forms.TextBox> contrôle est redimensionné horizontalement pour qu’il conserve la même distance entre les côtés gauche et droite du formulaire. En outre, le contrôle se positionne verticalement afin que son emplacement est toujours la même distance entre le bord inférieur du formulaire. Si un contrôle n’est pas ancré et le formulaire est redimensionné, la position du contrôle par rapport aux bords du formulaire est modifiée.  
  
 Le <xref:System.Windows.Forms.Control.Anchor%2A> propriété interagit avec le <xref:System.Windows.Forms.Control.AutoSize%2A> propriété. Pour plus d’informations, consultez [vue d’ensemble de la propriété AutoSize](../../../../docs/framework/winforms/controls/autosize-property-overview.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-anchor-a-control-on-a-form"></a>Pour ancrer un contrôle sur un formulaire  
  
1.  Sélectionnez le contrôle que vous souhaitez ancrer.  
  
    > [!NOTE]
    >  Vous pouvez ancrer plusieurs contrôles simultanément en appuyant sur la touche CTRL enfoncée, en cliquant sur chaque contrôle pour le sélectionner, puis en suivant le reste de cette procédure.  
  
2.  Dans le **propriétés** fenêtre, cliquez sur la flèche à droite de la <xref:System.Windows.Forms.Control.Anchor%2A> propriété.  
  
     Un éditeur qui s’affiche montre une croix.  
  
3.  Pour définir un point d’ancrage, cliquez sur le coin supérieur gauche, droite ou section inférieure de la croix.  
  
     Les contrôles sont ancrés vers le haut et gauche par défaut.  
  
4.  Pour effacer un côté du contrôle qui a été ancré, cliquez sur cette branche de la croix.  
  
5.  Pour fermer la <xref:System.Windows.Forms.Control.Anchor%2A> éditeur de propriétés, cliquez sur le <xref:System.Windows.Forms.Control.Anchor%2A> à nouveau nom de propriété.  
  
 Lorsque votre formulaire est affiché au moment de l’exécution, le contrôle est redimensionné pour rester à la même distance du bord du formulaire. La distance entre le bord ancré reste toujours la même que la distance définie lorsque le contrôle se trouve dans le Concepteur de formulaires Windows.  
  
> [!NOTE]
>  Certains contrôles, tels que le <xref:System.Windows.Forms.ComboBox> , ont une limite quant à leur hauteur. Ancrer le contrôle vers le bas de son formulaire ou un conteneur ne peut pas forcer le contrôle dépassent la limite de hauteur.  
  
 Les contrôles hérités doivent être `Protected` pour pouvoir être ancrée. Pour modifier le niveau d’accès d’un contrôle, définissez son `Modifiers` propriété dans le **propriétés** fenêtre.  
  
## <a name="see-also"></a>Voir aussi  
 [Contrôles Windows Forms](../../../../docs/framework/winforms/controls/index.md)  
 [Disposition des contrôles dans les Windows Forms](../../../../docs/framework/winforms/controls/arranging-controls-on-windows-forms.md)  
 [Vue d’ensemble de la propriété AutoSize](../../../../docs/framework/winforms/controls/autosize-property-overview.md)  
 [Guide pratique pour fixer des contrôles sur des Windows Forms](../../../../docs/framework/winforms/controls/how-to-dock-controls-on-windows-forms.md)  
 [Procédure pas à pas : organisation des contrôles dans les Windows Forms à l’aide d’un FlowLayoutPanel](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)  
 [Procédure pas à pas : organisation des contrôles dans les Windows Forms à l’aide d’un TableLayoutPanel](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)  
 [Procédure pas à pas : disposition des contrôles Windows Forms avec les propriétés Padding, Margins et AutoSize](../../../../docs/framework/winforms/controls/windows-forms-controls-padding-autosize.md)
