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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62012782"
---
# <a name="mainmenu-component-overview-windows-forms"></a><span data-ttu-id="292da-102">Vue d'ensemble du composant MainMenu (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="292da-102">MainMenu Component Overview (Windows Forms)</span></span>
> [!IMPORTANT]
>  <span data-ttu-id="292da-103">Bien que <xref:System.Windows.Forms.MenuStrip> et <xref:System.Windows.Forms.ContextMenuStrip> remplacent et ajoutent des fonctionnalités à la <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> contrôles des versions antérieures, <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> sont conservés pour la compatibilité descendante et l’utilisation future si vous choisissez.</span><span class="sxs-lookup"><span data-stu-id="292da-103">Although <xref:System.Windows.Forms.MenuStrip> and <xref:System.Windows.Forms.ContextMenuStrip> replace and add functionality to the <xref:System.Windows.Forms.MainMenu> and <xref:System.Windows.Forms.ContextMenu> controls of previous versions, <xref:System.Windows.Forms.MainMenu> and <xref:System.Windows.Forms.ContextMenu> are retained for both backward compatibility and future use if you choose.</span></span>  
  
 <span data-ttu-id="292da-104">Les formulaires Windows <xref:System.Windows.Forms.MainMenu> composant affiche un menu en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="292da-104">The Windows Forms <xref:System.Windows.Forms.MainMenu> component displays a menu at run time.</span></span> <span data-ttu-id="292da-105">Tous les sous-menus du menu principal et des éléments individuels sont <xref:System.Windows.Forms.MenuItem> objets.</span><span class="sxs-lookup"><span data-stu-id="292da-105">All submenus of the main menu and individual items are <xref:System.Windows.Forms.MenuItem> objects.</span></span>  
  
## <a name="key-properties"></a><span data-ttu-id="292da-106">Propriétés de clé</span><span class="sxs-lookup"><span data-stu-id="292da-106">Key Properties</span></span>  
 <span data-ttu-id="292da-107">Un élément de menu peut être désigné comme élément par défaut en définissant le <xref:System.Windows.Forms.MenuItem.DefaultItem%2A> propriété `true`.</span><span class="sxs-lookup"><span data-stu-id="292da-107">A menu item can be designated as the default item by setting the <xref:System.Windows.Forms.MenuItem.DefaultItem%2A> property to `true`.</span></span> <span data-ttu-id="292da-108">L’élément par défaut s’affiche en gras lorsque l’utilisateur clique sur le menu.</span><span class="sxs-lookup"><span data-stu-id="292da-108">The default item appears in bold text when the menu is clicked.</span></span> <span data-ttu-id="292da-109">L’élément de menu <xref:System.Windows.Forms.MenuItem.Checked%2A> propriété est `true` ou `false`et indique si l’élément de menu est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="292da-109">The menu item's <xref:System.Windows.Forms.MenuItem.Checked%2A> property is either `true` or `false`, and indicates whether the menu item is selected.</span></span> <span data-ttu-id="292da-110">L’élément de menu <xref:System.Windows.Forms.MenuItem.RadioCheck%2A> propriété personnalise l’apparence de l’élément sélectionné : si <xref:System.Windows.Forms.MenuItem.RadioCheck%2A> a la valeur `true`, une case d’option apparaît en regard de l’élément ; si <xref:System.Windows.Forms.MenuItem.RadioCheck%2A> a la valeur `false`, une coche apparaît en regard de l’élément.</span><span class="sxs-lookup"><span data-stu-id="292da-110">The menu item's <xref:System.Windows.Forms.MenuItem.RadioCheck%2A> property customizes the appearance of the selected item: if <xref:System.Windows.Forms.MenuItem.RadioCheck%2A> is set to `true`, a radio button appears next to the item; if <xref:System.Windows.Forms.MenuItem.RadioCheck%2A> is set to `false`, a check mark appears next to the item.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="292da-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="292da-111">See also</span></span>

- <xref:System.Windows.Forms.MainMenu>
- <xref:System.Windows.Forms.Menu>
- <xref:System.Windows.Forms.MenuItem>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ContextMenuStrip>
- [<span data-ttu-id="292da-112">Vue d'ensemble du contrôle MenuStrip</span><span class="sxs-lookup"><span data-stu-id="292da-112">MenuStrip Control Overview</span></span>](menustrip-control-overview-windows-forms.md)
