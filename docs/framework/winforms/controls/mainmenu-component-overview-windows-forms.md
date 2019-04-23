---
title: Vue d'ensemble du composant MainMenu (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- MenuItem
- MainMenu
helpviewer_keywords:
- MainMenu control [Windows Forms], about MainMenu control
- menus
ms.assetid: b41cc5a3-cc59-4996-aa3c-8dd9c17d3c90
ms.openlocfilehash: da1b76a7019f364e7463a8345aa80d9a9bd6089e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59168478"
---
# <a name="mainmenu-component-overview-windows-forms"></a>Vue d'ensemble du composant MainMenu (Windows Forms)
> [!IMPORTANT]
>  Bien que <xref:System.Windows.Forms.MenuStrip> et <xref:System.Windows.Forms.ContextMenuStrip> remplacent et ajoutent des fonctionnalités à la <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> contrôles des versions antérieures, <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> sont conservés pour la compatibilité descendante et l’utilisation future si vous choisissez.  
  
 Les formulaires Windows <xref:System.Windows.Forms.MainMenu> composant affiche un menu en cours d’exécution. Tous les sous-menus du menu principal et des éléments individuels sont <xref:System.Windows.Forms.MenuItem> objets.  
  
## <a name="key-properties"></a>Propriétés de clé  
 Un élément de menu peut être désigné comme élément par défaut en définissant le <xref:System.Windows.Forms.MenuItem.DefaultItem%2A> propriété `true`. L’élément par défaut s’affiche en gras lorsque l’utilisateur clique sur le menu. L’élément de menu <xref:System.Windows.Forms.MenuItem.Checked%2A> propriété est `true` ou `false`et indique si l’élément de menu est sélectionné. L’élément de menu <xref:System.Windows.Forms.MenuItem.RadioCheck%2A> propriété personnalise l’apparence de l’élément sélectionné : si <xref:System.Windows.Forms.MenuItem.RadioCheck%2A> a la valeur `true`, une case d’option apparaît en regard de l’élément ; si <xref:System.Windows.Forms.MenuItem.RadioCheck%2A> a la valeur `false`, une coche apparaît en regard de l’élément.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.MainMenu>
- <xref:System.Windows.Forms.Menu>
- <xref:System.Windows.Forms.MenuItem>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ContextMenuStrip>
- [Vue d'ensemble du contrôle MenuStrip](menustrip-control-overview-windows-forms.md)
