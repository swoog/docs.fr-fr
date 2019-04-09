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
ms.openlocfilehash: e02a187edc1392f15fe98354bb2e5c43843e430c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59094461"
---
# <a name="how-to-add-and-remove-menu-items-with-the-windows-forms-contextmenu-component"></a><span data-ttu-id="e3ace-102">Procédure : ajouter et supprimer des éléments de menu avec le composant ContextMenu de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e3ace-102">How to: Add and Remove Menu Items with the Windows Forms ContextMenu Component</span></span>
<span data-ttu-id="e3ace-103">Explique comment ajouter et supprimer des éléments de menu contextuel dans les Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="e3ace-103">Explains how to add and remove shortcut menu items in Windows Forms.</span></span>  
  
 <span data-ttu-id="e3ace-104">Les formulaires Windows <xref:System.Windows.Forms.ContextMenu> composant fournit un menu des commandes fréquemment utilisées qui sont pertinents pour l’objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e3ace-104">The Windows Forms <xref:System.Windows.Forms.ContextMenu> component provides a menu of frequently used commands that are relevant to the selected object.</span></span> <span data-ttu-id="e3ace-105">Vous pouvez ajouter des éléments au menu contextuel en ajoutant <xref:System.Windows.Forms.MenuItem> des objets sur le <xref:System.Windows.Forms.Menu.MenuItems%2A> collection.</span><span class="sxs-lookup"><span data-stu-id="e3ace-105">You can add items to the shortcut menu by adding <xref:System.Windows.Forms.MenuItem> objects to the <xref:System.Windows.Forms.Menu.MenuItems%2A> collection.</span></span>  
  
 <span data-ttu-id="e3ace-106">Vous pouvez supprimer des éléments dans un menu contextuel définitivement ; Toutefois, au moment de l’exécution, il peut être plus approprié de masquer ou désactiver les éléments à la place.</span><span class="sxs-lookup"><span data-stu-id="e3ace-106">You can remove items from a shortcut menu permanently; however, at run time it may be more appropriate to hide or disable the items instead.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="e3ace-107">Bien que <xref:System.Windows.Forms.MenuStrip> et <xref:System.Windows.Forms.ContextMenuStrip> remplacent et ajoutent des fonctionnalités à la <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> contrôles des versions antérieures, <xref:System.Windows.Forms.MainMenu> et <xref:System.Windows.Forms.ContextMenu> sont conservés pour la compatibilité descendante et l’utilisation future si vous choisissez.</span><span class="sxs-lookup"><span data-stu-id="e3ace-107">Although <xref:System.Windows.Forms.MenuStrip> and <xref:System.Windows.Forms.ContextMenuStrip> replace and add functionality to the <xref:System.Windows.Forms.MainMenu> and <xref:System.Windows.Forms.ContextMenu> controls of previous versions, <xref:System.Windows.Forms.MainMenu> and <xref:System.Windows.Forms.ContextMenu> are retained for both backward compatibility and future use if you choose.</span></span>  
  
### <a name="to-remove-items-from-a-shortcut-menu"></a><span data-ttu-id="e3ace-108">Pour supprimer des éléments dans un menu contextuel</span><span class="sxs-lookup"><span data-stu-id="e3ace-108">To remove items from a shortcut menu</span></span>  
  
1.  <span data-ttu-id="e3ace-109">Utilisez le <xref:System.Windows.Forms.Menu.MenuItemCollection.Remove%2A> ou <xref:System.Windows.Forms.Menu.MenuItemCollection.RemoveAt%2A> méthode de la <xref:System.Windows.Forms.Menu.MenuItems%2A> collection de la <xref:System.Windows.Forms.ContextMenu> composant à supprimer un élément de menu particulier.</span><span class="sxs-lookup"><span data-stu-id="e3ace-109">Use the <xref:System.Windows.Forms.Menu.MenuItemCollection.Remove%2A> or <xref:System.Windows.Forms.Menu.MenuItemCollection.RemoveAt%2A> method of the <xref:System.Windows.Forms.Menu.MenuItems%2A> collection of the <xref:System.Windows.Forms.ContextMenu> component to remove a particular menu item.</span></span>  
  
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
  
     <span data-ttu-id="e3ace-110">- ou -</span><span class="sxs-lookup"><span data-stu-id="e3ace-110">-or-</span></span>  
  
2.  <span data-ttu-id="e3ace-111">Utilisez le `Clear` méthode de la `MenuItems` collection de la <xref:System.Windows.Forms.ContextMenu> composant à supprimer tous les éléments dans le menu.</span><span class="sxs-lookup"><span data-stu-id="e3ace-111">Use the `Clear` method of the `MenuItems` collection of the <xref:System.Windows.Forms.ContextMenu> component to remove all items from the menu.</span></span>  
  
    ```vb  
    ContextMenu1.MenuItems.Clear()  
    ```  
  
    ```csharp  
    contextMenu1.MenuItems.Clear();  
    ```  
  
    ```cpp  
    contextMenu1->MenuItems->Clear();  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="e3ace-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3ace-112">See also</span></span>

- <xref:System.Windows.Forms.ContextMenu>
- [<span data-ttu-id="e3ace-113">ContextMenu, composant</span><span class="sxs-lookup"><span data-stu-id="e3ace-113">ContextMenu Component</span></span>](contextmenu-component-windows-forms.md)
- [<span data-ttu-id="e3ace-114">Vue d’ensemble du composant ContextMenu</span><span class="sxs-lookup"><span data-stu-id="e3ace-114">ContextMenu Component Overview</span></span>](contextmenu-component-overview-windows-forms.md)
