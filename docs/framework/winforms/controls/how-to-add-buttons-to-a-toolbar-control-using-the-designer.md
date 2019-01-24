---
title: 'Procédure : Ajouter des boutons à un contrôle de barre d’outils à l’aide du Concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- toolbars [Windows Forms], adding buttons
- ToolBar control [Windows Forms], adding buttons
- ToolBar control [Windows Forms], adding separators
- examples [Windows Forms], toolbars
- ToolBar control [Windows Forms], adding drop-down menus
ms.assetid: d9ce3040-3e21-4e2d-80ae-b430982b2db8
ms.openlocfilehash: e18a2f9b8c22538bc545388af56ee929bc94d70c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54538906"
---
# <a name="how-to-add-buttons-to-a-toolbar-control-using-the-designer"></a>Procédure : Ajouter des boutons à un contrôle de barre d’outils à l’aide du Concepteur
> [!NOTE]
>  Le contrôle <xref:System.Windows.Forms.ToolStrip> remplace le contrôle <xref:System.Windows.Forms.ToolBar> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.ToolBar> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix.  
  
 Partie intégrante de la <xref:System.Windows.Forms.ToolBar> contrôle est les boutons que vous ajoutez à ce dernier. Ils peuvent être utilisés pour fournir un accès facile aux commandes de menu ou, alternativement, ils peuvent être placés dans une autre zone de l’interface utilisateur de votre application pour exposer à vos utilisateurs qui ne sont pas disponibles dans la structure du menu de commandes.  
  
 La procédure suivante nécessite un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.ToolBar> contrôle. Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’Application Windows](https://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa) et [Comment : Ajouter des contrôles aux Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-add-buttons-at-design-time"></a>Pour ajouter des boutons au moment du design  
  
1.  Sélectionnez le contrôle <xref:System.Windows.Forms.ToolBar>.  
  
2.  Dans le **propriétés** fenêtre, cliquez sur le <xref:System.Windows.Forms.ToolBar.Buttons%2A> propriété pour la sélectionner, puis cliquez sur le **points de suspension** (![d’écran de VisualStudioEllipsesButton](../../../../docs/framework/winforms/media/vbellipsesbutton.png " vbEllipsesButton")) pour ouvrir la **éditeur de collections ToolBarButton**.  
  
3.  Utilisez le **ajouter** et **supprimer** boutons pour ajouter et supprimer des boutons à partir de la <xref:System.Windows.Forms.ToolBar> contrôle.  
  
4.  Configurer les propriétés des boutons individuels dans le **propriétés** fenêtre qui s’affiche dans le volet situé à droite de l’éditeur. Le tableau suivant présente certaines propriétés importantes à prendre en compte.  
  
    |Propriété|Description|  
    |--------------|-----------------|  
    |<xref:System.Windows.Forms.ToolBarButton.DropDownMenu%2A>|Définit le menu à afficher dans le bouton de barre d’outils de la liste déroulante. Le bouton de barre d’outils <xref:System.Windows.Forms.ToolBarButton.Style%2A> propriété doit être définie sur <xref:System.Windows.Forms.ToolBarButtonStyle.DropDownButton>. Cette propriété accepte une instance de la <xref:System.Windows.Forms.ContextMenu> classe en tant que référence.|  
    |<xref:System.Windows.Forms.ToolBarButton.PartialPush%2A>|Définit si un bouton de barre d’outils de style bascule c’est le cas. Le bouton de barre d’outils <xref:System.Windows.Forms.ToolBarButton.Style%2A> propriété doit être définie sur <xref:System.Windows.Forms.ToolBarButtonStyle.ToggleButton>.|  
    |<xref:System.Windows.Forms.ToolBarButton.Pushed%2A>|Définit si un bouton bascule de la barre d’outils est actuellement enfoncé. Le bouton de barre d’outils <xref:System.Windows.Forms.ToolBarButton.Style%2A> propriété doit être définie sur <xref:System.Windows.Forms.ToolBarButtonStyle.ToggleButton> ou <xref:System.Windows.Forms.ToolBarButtonStyle.PushButton>.|  
    |<xref:System.Windows.Forms.ToolBarButton.Style%2A>|Définit le style du bouton de barre d’outils. Doit être une des valeurs dans le <xref:System.Windows.Forms.ToolBarButtonStyle> énumération.|  
    |<xref:System.Windows.Forms.ToolBarButton.Text%2A>|La chaîne de texte affichée par le bouton.|  
    |<xref:System.Windows.Forms.ToolBarButton.ToolTipText%2A>|Le texte qui apparaît sous la forme d’une info-bulle pour le bouton.|  
  
5.  Cliquez sur **OK** pour fermer la boîte de dialogue et créer les volets que vous avez spécifié.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ToolBar>
- [Guide pratique pour Définir une icône pour un bouton de barre d’outils](../../../../docs/framework/winforms/controls/how-to-define-an-icon-for-a-toolbar-button.md)
- [Guide pratique pour Déclencher des événements de Menu pour les boutons de barre d’outils](../../../../docs/framework/winforms/controls/how-to-trigger-menu-events-for-toolbar-buttons.md)
- [Vue d’ensemble du contrôle ToolBar](../../../../docs/framework/winforms/controls/toolbar-control-overview-windows-forms.md)
- [ToolBar, contrôle](../../../../docs/framework/winforms/controls/toolbar-control-windows-forms.md)
