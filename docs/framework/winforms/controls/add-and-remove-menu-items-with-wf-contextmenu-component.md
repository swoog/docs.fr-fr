---
title: 'Procédure : ajouter et supprimer des éléments de menu avec le composant ContextMenu de Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- context menus [Windows Forms], removing items
- ContextMenu component [Windows Forms], adding items
- shortcut menus [Windows Forms], removing items
- shortcut menus [Windows Forms], examples
- context menus [Windows Forms], adding items
- shortcut menus [Windows Forms], adding items
- ContextMenu component [Windows Forms], removing items
- context menus [Windows Forms], examples
- examples [Windows Forms], context menus
ms.assetid: 426d1eaf-7fb8-4b0b-8a33-5e8721786ea4
ms.openlocfilehash: cf70a5cc426b6c6075d1deb11aa2685c39a065c0
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59332181"
---
# <a name="how-to-add-and-remove-menu-items-with-the-windows-forms-contextmenu-component"></a>Procédure : ajouter et supprimer des éléments de menu avec le composant ContextMenu de Windows Forms
Explique comment ajouter et supprimer des éléments de menu contextuel dans les Windows Forms.  
  
 Les formulaires Windows <xref:System.Windows.Forms.ContextMenu> composant fournit un menu des commandes fréquemment utilisées qui sont pertinents pour l’objet sélectionné. Vous pouvez ajouter des éléments au menu contextuel en ajoutant <xref:System.Windows.Forms.MenuItem> des objets sur le <xref:System.Windows.Forms.Menu.MenuItems%2A> collection.  
  
 Vous pouvez supprimer des éléments dans un menu contextuel définitivement ; Toutefois, au moment de l’exécution, il peut être plus approprié de masquer ou désactiver les éléments à la place.  
  
> [!IMPORTANT]
>  Bien que <xref:System.Windows.Forms.MenuStrip> et <xref:System.Windows.Forms.ContextMenuStrip> remplacent et ajoutent des fonctionnalités à la <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> contrôles des versions antérieures, <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> sont conservés pour la compatibilité descendante et l’utilisation future si vous choisissez.  
  
### <a name="to-remove-items-from-a-shortcut-menu"></a>Pour supprimer des éléments dans un menu contextuel  
  
1. Utilisez le <xref:System.Windows.Forms.Menu.MenuItemCollection.Remove%2A> ou <xref:System.Windows.Forms.Menu.MenuItemCollection.RemoveAt%2A> méthode de la <xref:System.Windows.Forms.Menu.MenuItems%2A> collection de la <xref:System.Windows.Forms.ContextMenu> composant à supprimer un élément de menu particulier.  
  
    ```vb  
    ' Removes the first item in the shortcut menu.  
    ContextMenu1.MenuItems.RemoveAt(0)  
    ' Removes a particular object from the shortcut menu.  
    ContextMenu1.MenuItems.Remove(mnuItemNew)  
    ```  
  
    ```csharp  
    // Removes the first item in the shortcut menu.  
    contextMenu1.MenuItems.RemoveAt(0);  
    // Removes a particular object from the shortcut menu.  
    contextMenu1.MenuItems.Remove(mnuItemNew);  
    ```  
  
    ```cpp  
    // Removes the first item in the shortcut menu.  
    contextMenu1->MenuItems->RemoveAt(0);  
    // Removes a particular object from the shortcut menu.  
    contextMenu1->MenuItems->Remove(mnuItemNew);  
    ```  
  
     - ou -  
  
2. Utilisez le `Clear` méthode de la `MenuItems` collection de la <xref:System.Windows.Forms.ContextMenu> composant à supprimer tous les éléments dans le menu.  
  
    ```vb  
    ContextMenu1.MenuItems.Clear()  
    ```  
  
    ```csharp  
    contextMenu1.MenuItems.Clear();  
    ```  
  
    ```cpp  
    contextMenu1->MenuItems->Clear();  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.ContextMenu>
- [ContextMenu, composant](contextmenu-component-windows-forms.md)
- [Vue d’ensemble du composant ContextMenu](contextmenu-component-overview-windows-forms.md)
