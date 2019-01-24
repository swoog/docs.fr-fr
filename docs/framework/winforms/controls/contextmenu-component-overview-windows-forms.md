---
title: Vue d'ensemble du composant ContextMenu (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- ContextMenu
helpviewer_keywords:
- ContextMenu component [Windows Forms], about ContextMenu component
- context menus [Windows Forms], ContextMenu component
- shortcut menus [Windows Forms], ContextMenu component
ms.assetid: 49d6398f-d3c4-4679-84fa-1de07b68b05e
ms.openlocfilehash: 7da0522dae00608ead356484a31d219a67ec4ba9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54545671"
---
# <a name="contextmenu-component-overview-windows-forms"></a>Vue d'ensemble du composant ContextMenu (Windows Forms)
> [!IMPORTANT]
>  Bien que <xref:System.Windows.Forms.MenuStrip> et <xref:System.Windows.Forms.ContextMenuStrip> remplacent et ajoutent des fonctionnalités à la <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> contrôles des versions antérieures, <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> sont conservés pour la compatibilité descendante et l’utilisation future si vous choisissez.  
  
 Avec les formulaires Windows <xref:System.Windows.Forms.ContextMenu> composant, vous pouvez fournir aux utilisateurs un menu contextuel facilement accessible des commandes fréquemment utilisées qui sont associés à l’objet sélectionné. Les éléments dans un menu contextuel constituent souvent un sous-ensemble des éléments des menus principaux qui apparaissent ailleurs dans l’application. Un utilisateur peut accéder en général d’un menu contextuel en cliquant sur la souris. Dans les Windows Forms, les menus contextuels sont associés aux contrôles.  
  
## <a name="key-properties"></a>Propriétés de clé  
 Vous pouvez associer un menu contextuel à un contrôle en définissant le contrôle <xref:System.Windows.Forms.Control.ContextMenu%2A> propriété le <xref:System.Windows.Forms.ContextMenu> composant. Un menu contextuel unique peut être associé à plusieurs contrôles, mais chaque contrôle peut avoir qu’un seul menu contextuel.  
  
 La propriété de clé de la <xref:System.Windows.Forms.ContextMenu> composant est le <xref:System.Windows.Forms.Menu.MenuItems%2A> propriété. Vous pouvez ajouter des éléments de menu en créant par programmation <xref:System.Windows.Forms.MenuItem> objets et en les ajoutant à la <xref:System.Windows.Forms.Menu.MenuItemCollection> du menu contextuel. Étant donné que les éléments dans un menu contextuel sont habituellement extraites d’autres menus, vous allez ajouter plus fréquemment des éléments à un menu contextuel en les copiant.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ContextMenu>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ContextMenuStrip>
