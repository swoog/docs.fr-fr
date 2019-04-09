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
ms.openlocfilehash: 2acbcc9197a630a993471c22e572a4f3ed682c64
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59090561"
---
# <a name="contextmenu-component-overview-windows-forms"></a><span data-ttu-id="fa011-102">Vue d'ensemble du composant ContextMenu (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="fa011-102">ContextMenu Component Overview (Windows Forms)</span></span>
> [!IMPORTANT]
>  <span data-ttu-id="fa011-103">Bien que <xref:System.Windows.Forms.MenuStrip> et <xref:System.Windows.Forms.ContextMenuStrip> remplacent et ajoutent des fonctionnalités à la <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> contrôles des versions antérieures, <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> sont conservés pour la compatibilité descendante et l’utilisation future si vous choisissez.</span><span class="sxs-lookup"><span data-stu-id="fa011-103">Although <xref:System.Windows.Forms.MenuStrip> and <xref:System.Windows.Forms.ContextMenuStrip> replace and add functionality to the <xref:System.Windows.Forms.MainMenu> and <xref:System.Windows.Forms.ContextMenu> controls of previous versions, <xref:System.Windows.Forms.MainMenu> and <xref:System.Windows.Forms.ContextMenu> are retained for both backward compatibility and future use if you choose.</span></span>  
  
 <span data-ttu-id="fa011-104">Avec les formulaires Windows <xref:System.Windows.Forms.ContextMenu> composant, vous pouvez fournir aux utilisateurs un menu contextuel facilement accessible des commandes fréquemment utilisées qui sont associés à l’objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="fa011-104">With the Windows Forms <xref:System.Windows.Forms.ContextMenu> component, you can provide users with an easily accessible shortcut menu of frequently used commands that are associated with the selected object.</span></span> <span data-ttu-id="fa011-105">Les éléments dans un menu contextuel constituent souvent un sous-ensemble des éléments des menus principaux qui apparaissent ailleurs dans l’application.</span><span class="sxs-lookup"><span data-stu-id="fa011-105">The items in a shortcut menu are frequently a subset of the items from main menus that appear elsewhere in the application.</span></span> <span data-ttu-id="fa011-106">Un utilisateur peut accéder en général d’un menu contextuel en cliquant sur la souris.</span><span class="sxs-lookup"><span data-stu-id="fa011-106">A user can typically access a shortcut menu by right-clicking the mouse.</span></span> <span data-ttu-id="fa011-107">Dans les Windows Forms, les menus contextuels sont associés aux contrôles.</span><span class="sxs-lookup"><span data-stu-id="fa011-107">On Windows Forms, shortcut menus are associated with controls.</span></span>  
  
## <a name="key-properties"></a><span data-ttu-id="fa011-108">Propriétés de clé</span><span class="sxs-lookup"><span data-stu-id="fa011-108">Key Properties</span></span>  
 <span data-ttu-id="fa011-109">Vous pouvez associer un menu contextuel à un contrôle en définissant le contrôle <xref:System.Windows.Forms.Control.ContextMenu%2A> propriété le <xref:System.Windows.Forms.ContextMenu> composant.</span><span class="sxs-lookup"><span data-stu-id="fa011-109">You can associate a shortcut menu with a control by setting the control's <xref:System.Windows.Forms.Control.ContextMenu%2A> property to the <xref:System.Windows.Forms.ContextMenu> component.</span></span> <span data-ttu-id="fa011-110">Un menu contextuel unique peut être associé à plusieurs contrôles, mais chaque contrôle peut avoir qu’un seul menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="fa011-110">A single shortcut menu can be associated with multiple controls, but each control can have only one shortcut menu.</span></span>  
  
 <span data-ttu-id="fa011-111">La propriété de clé de la <xref:System.Windows.Forms.ContextMenu> composant est le <xref:System.Windows.Forms.Menu.MenuItems%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="fa011-111">The key property of the <xref:System.Windows.Forms.ContextMenu> component is the <xref:System.Windows.Forms.Menu.MenuItems%2A> property.</span></span> <span data-ttu-id="fa011-112">Vous pouvez ajouter des éléments de menu en créant par programmation <xref:System.Windows.Forms.MenuItem> objets et en les ajoutant à la <xref:System.Windows.Forms.Menu.MenuItemCollection> du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="fa011-112">You can add menu items by programmatically creating <xref:System.Windows.Forms.MenuItem> objects and adding them to the <xref:System.Windows.Forms.Menu.MenuItemCollection> of the shortcut menu.</span></span> <span data-ttu-id="fa011-113">Étant donné que les éléments dans un menu contextuel sont habituellement extraites d’autres menus, vous allez ajouter plus fréquemment des éléments à un menu contextuel en les copiant.</span><span class="sxs-lookup"><span data-stu-id="fa011-113">Because the items in a shortcut menu are usually drawn from other menus, you will most frequently add items to a shortcut menu by copying them.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa011-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa011-114">See also</span></span>

- <xref:System.Windows.Forms.ContextMenu>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ContextMenuStrip>
