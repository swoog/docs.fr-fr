---
title: 'Procédure : Masquer des ToolStripMenuItems'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ToolStripMenuItems [Windows Forms], hiding
- MenuStrip control [Windows Forms], hiding menu items
- menus [Windows Forms], hiding menu items
- menu items [Windows Forms], hiding
- hiding menu items
ms.assetid: 418a768f-808a-44cd-8cef-f4e161883621
ms.openlocfilehash: 73e49c96c20f145490a2d494177e21bc957605b8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54727623"
---
# <a name="how-to-hide-toolstripmenuitems"></a>Procédure : Masquer des ToolStripMenuItems
Masquage d’éléments de menu est un moyen de contrôler l’interface utilisateur de votre application et de restreindre les commandes de l’utilisateur. Souvent, vous devez masquer un menu quand tous les éléments de menu sur ce dernier ne sont pas disponibles. Cela est moins distrait pour l’utilisateur. En outre, vous souhaiterez peut-être cacher et désactiver le menu ou un élément de menu, comme simple masquage n’empêche pas l’utilisateur d’accéder à une commande de menu à l’aide d’une touche de raccourci.  
  
### <a name="to-hide-any-menu-item-programmatically"></a>Pour masquer un élément de menu par programme  
  
-   Dans la méthode où vous définissez les propriétés de l’élément de menu, ajoutez le code pour définir le <xref:System.Windows.Forms.ToolStripItem.Visible%2A> propriété `false`.  
  
    ```vb  
    MenuItem3.Visible = False  
    ```  
  
    ```csharp  
    menuItem3.Visible = false;  
    ```  
  
    ```cpp  
    menuItem3->Visible = false;  
    ```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ToolStripItem.Visible%2A>
- <xref:System.Windows.Forms.MenuStrip>
- [Vue d'ensemble du contrôle MenuStrip](../../../../docs/framework/winforms/controls/menustrip-control-overview-windows-forms.md)
- [Guide pratique pour Désactiver des ToolStripMenuItems](../../../../docs/framework/winforms/controls/how-to-disable-toolstripmenuitems.md)
