---
title: 'Comment : ajouter des améliorations aux ToolStripMenuItems'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- commands [Windows Forms], grouping on menus
- check marks [Windows Forms], adding to menus
- ToolStripMenuItems [Windows Forms], displaying access keys
- menus [Windows Forms], grouping commands
- menu items [Windows Forms], displaying shortcut keys
- ToolStripMenuItems
- separators [Windows Forms], displaying on menus
- menu items [Windows Forms], showing separators
- menu items [Windows Forms], adding check marks
- ToolStripMenuItems [Windows Forms], adding check marks
- menu items [Windows Forms], adding images
- ToolStripSeparators [Windows Forms], displaying on MenuStrips
- menu items [Windows Forms], displaying access keys
- ToolStripMenuItems [Windows Forms], displaying shortcut keys
- ToolStripMenuItems [Windows Forms], adding images
- keyboard shortcuts [Windows Forms], displaying on menus
- images [Windows Forms], adding to menus
- ToolStripMenuItems [Windows Forms], showing separator bars
ms.assetid: aa5f19bb-b545-4378-bfa6-36ba592f0d7c
ms.openlocfilehash: eb55796480bea896383da479fe23a5d8967a52e3
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48582409"
---
# <a name="how-to-add-enhancements-to-toolstripmenuitems"></a>Comment : ajouter des améliorations aux ToolStripMenuItems
Vous pouvez améliorer la facilité d’utilisation de <xref:System.Windows.Forms.MenuStrip> et <xref:System.Windows.Forms.ContextMenuStrip> contrôles comme suit :  
  
-   Ajouter des coches pour désigner si une fonctionnalité est activée ou désactivée, telles que si une règle est affichée le long de la marge d’une application de traitement de texte, ou pour indiquer quel fichier dans une liste de fichiers est affichée, telle que dans un **fenêtre** menu.  
  
-   Ajouter des images qui représentent visuellement des commandes de menu.  
  
-   Afficher les touches de raccourci pour fournir une alternative de clavier à la souris pour exécuter des commandes. Par exemple, en appuyant sur CTRL + C effectue la **copie** commande.  
  
-   Afficher les clés d’accès pour fournir une alternative de clavier à la souris pour la navigation de menu. Par exemple, en appuyant sur ALT + F pour choisir le **fichier** menu.  
  
-   Afficher les barres de séparation pour regrouper les commandes associées et améliorer la lisibilité des menus.  
  
### <a name="to-display-a-check-mark-on-a-menu-command"></a>Pour afficher une coche sur une commande de menu  
  
-   Définissez ses <xref:System.Windows.Forms.ToolStripMenuItem.Checked%2A> propriété `true`.  
  
     Cela définit également le <xref:System.Windows.Forms.ToolStripMenuItem.CheckState%2A> propriété `true`. Utilisez cette procédure uniquement si vous souhaitez que la commande de menu apparaisse comme cochée par défaut, indépendamment de si elle est sélectionnée.  
  
### <a name="to-display-a-check-mark-that-changes-state-with-each-click"></a>Pour afficher une case à cocher qui modifie l’état à chaque clic  
  
-   Définissez la commande de menu <xref:System.Windows.Forms.ToolStripMenuItem.CheckOnClick%2A> propriété `true`.  
  
### <a name="to-add-an-image-to-a-menu-command"></a>Pour ajouter une image à une commande de menu  
  
-   Définissez la commande de menu <xref:System.Windows.Forms.ToolStripItem.Image%2A> propriété le nom de l’image. Si le <xref:System.Windows.Forms.ToolStripItemDisplayStyle> propriété de cette commande de menu est définie sur <xref:System.Windows.Forms.ToolStripItemDisplayStyle.Text> ou <xref:System.Windows.Forms.ToolStripItemDisplayStyle.None>, l’image ne peut pas être affichée.  
  
> [!NOTE]
>  La marge d’image peut également afficher une case à cocher si vous le souhaitez. En outre, vous pouvez définir le <xref:System.Windows.Forms.ToolStripMenuItem.Checked%2A> propriété de l’image à `true`, et l’image s’affiche avec une bordure hachurée au moment de l’exécution.  
  
### <a name="to-display-a-shortcut-key-for-a-menu-command"></a>Pour afficher une touche de raccourci pour une commande de menu  
  
-   Définir la commande de menu <xref:System.Windows.Forms.ToolStripMenuItem.ShortcutKeys%2A> propriété à la combinaison de clavier désiré, tels que CTRL + O pour la **Open** commande de menu et définissez la <xref:System.Windows.Forms.ToolStripMenuItem.ShowShortcutKeys%2A> propriété `true`.  
  
### <a name="to-display-custom-shortcut-keys-for-a-menu-command"></a>Pour afficher les touches de raccourci personnalisées pour une commande de menu  
  
-   Définissez la commande de menu <xref:System.Windows.Forms.ToolStripMenuItem.ShortcutKeyDisplayString%2A> propriété à la combinaison de clavier désiré, tels que CTRL + MAJ + O plutôt que MAJ + CTRL + O et ensemble la <xref:System.Windows.Forms.ToolStripMenuItem.ShowShortcutKeys%2A> propriété `true`.  
  
### <a name="to-display-an-access-key-for-a-menu-command"></a>Pour afficher une clé d’accès pour une commande de menu  
  
-   Lorsque vous définissez le <xref:System.Windows.Forms.ToolStripItem.Text%2A> propriété pour la commande de menu, entrez une esperluette (&) avant la lettre que vous souhaitez être soulignées comme touche d’accès. Par exemple, si vous saisissez `&Open` en tant que le <xref:System.Windows.Forms.ToolStripItem.Text%2A> génère dans une commande de menu qui s’affiche en tant que propriété d’un élément de menu <u>O</u>stylet.
  
     Pour accéder à cette commande de menu, appuyez sur ALT pour donner le focus à la <xref:System.Windows.Forms.MenuStrip>, appuyez sur la touche d’accès du nom de menu. Lorsque le menu s’ouvre et affiche les éléments avec des clés d’accès, il vous suffit d’appuyer sur la clé d’accès pour sélectionner la commande de menu.  
  
> [!NOTE]
>  Évitez de définir des clés d’accès en double, telles que la définition ALT + F à deux reprises dans le même système de menu. L’ordre de sélection des clés d’accès en double ne peut pas être garantie.  
  
### <a name="to-display-a-separator-bar-between-menu-commands"></a>Pour afficher une barre de séparation entre les commandes de menu  
  
-   Après avoir défini votre <xref:System.Windows.Forms.MenuStrip> et les éléments qu’il contient, utilisez le <xref:System.Windows.Forms.ToolStripItemCollection.AddRange%2A> ou <xref:System.Windows.Forms.ToolStripItemCollection.Add%2A> méthode pour ajouter les commandes de menu et <xref:System.Windows.Forms.ToolStripSeparator> de contrôles à la <xref:System.Windows.Forms.MenuStrip> dans l’ordre souhaité.  
  
    ```vb  
    ' This code adds a top-level File menu to the MenuStrip.  
    Me.menuStrip1.Items.Add(New ToolStripMenuItem() _  
    {Me.fileToolStripMenuItem})  
  
    ' This code adds the New and Open menu commands, a separator bar,   
    ' and the Save and Exit menu commands to the top-level File menu,   
    ' in that order.  
    Me.fileToolStripMenuItem.DropDownItems.AddRange(New _  
    ToolStripMenuItem() {Me.newToolStripMenuItem, _  
    Me.openToolStripMenuItem, Me.toolStripSeparator1, _  
    Me.saveToolStripMenuItem, Me.exitToolStripMenuItem})  
    ```  
  
    ```csharp  
    // This code adds a top-level File menu to the MenuStrip.  
    this.menuStrip1.Items.Add(new ToolStripItem[]_  
    {this.fileToolStripMenuItem});  
  
    // This code adds the New and Open menu commands, a separator bar,   
    // and the Save and Exit menu commands to the top-level File menu,   
    // in that order.  
    this.fileToolStripMenuItem.DropDownItems.AddRange(new _  
    ToolStripItem[] {  
    this.newToolStripMenuItem,  
    this.openToolStripMenuItem,  
    this.toolStripSeparator1,  
    this.saveToolStripMenuItem,  
    this.exitToolStripMenuItem});  
    ```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.MenuStrip>  
 <xref:System.Windows.Forms.ToolStripMenuItem>  
 [Vue d'ensemble du contrôle MenuStrip](../../../../docs/framework/winforms/controls/menustrip-control-overview-windows-forms.md)
