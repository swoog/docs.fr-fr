---
title: 'Procédure : Désactiver des ToolStripMenuItems à l’aide du Concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolStripMenuItems [Windows Forms], disabling in designer
- MenuStrip control [Windows Forms], disabling menu items in designer
- menu items [Windows Forms], disabling
- menus [Windows Forms], disabling items
ms.assetid: 985e311e-7d67-4205-b5a3-d045b68a4a03
ms.openlocfilehash: a185fe4421b5b5d7846c7d8cacbfc1cae5f805eb
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57704428"
---
# <a name="how-to-disable-toolstripmenuitems-using-the-designer"></a>Procédure : Désactiver des ToolStripMenuItems à l’aide du Concepteur
Vous pouvez limiter ou élargir les commandes de que l’utilisateur peut effectuer par activation et désactivation des éléments de menu en réponse aux activités de l’utilisateur. Éléments de menu sont activées par défaut lorsqu’ils sont créés, mais cela peut être ajusté via la <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A> propriété. Vous pouvez manipuler cette propriété au moment du design dans le **propriétés** fenêtre ou par programme en la définissant dans le code. Pour plus d'informations, voir [Procédure : Désactiver des ToolStripMenuItems](how-to-disable-toolstripmenuitems.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-disable-a-menu-item-at-design-time"></a>Pour désactiver un élément de menu au moment du design  
  
1.  Avec l’élément de menu sélectionné sur le formulaire, définissez la <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A> propriété `false`.  
  
    > [!TIP]
    >  La désactivation de l’élément de menu de première ou de niveau supérieur dans un menu désactive tous les éléments de menu contenus dans le menu. De même, la désactivation d’un élément de menu ayant des éléments de sous-menu désactive les éléments de sous-menu. Si toutes les commandes de menu ne sont pas disponibles à l’utilisateur, il est considéré comme bonne pratique de programmation à cacher et désactiver le menu entier, comme cela présente une interface utilisateur propre. Vous devez à la fois masquer et désactiver le menu, comme simple masquage n’empêche pas l’accès à une commande de menu via une touche de raccourci. Définir le <xref:System.Windows.Forms.ToolStripItem.Visible%2A> propriété d’un élément de menu de niveau supérieur pour `false` masquer le menu.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- [Guide pratique pour Masquer des ToolStripMenuItems](how-to-hide-toolstripmenuitems.md)
- [Vue d'ensemble du contrôle MenuStrip](menustrip-control-overview-windows-forms.md)
