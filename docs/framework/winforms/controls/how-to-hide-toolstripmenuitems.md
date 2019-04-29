---
title: 'Procédure : masquer des ToolStripMenuItems'
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
ms.openlocfilehash: dc9daa945f2a546548f2cc6ea033378bd9ceff93
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61941219"
---
# <a name="how-to-hide-toolstripmenuitems"></a><span data-ttu-id="7dfee-102">Procédure : masquer des ToolStripMenuItems</span><span class="sxs-lookup"><span data-stu-id="7dfee-102">How to: Hide ToolStripMenuItems</span></span>
<span data-ttu-id="7dfee-103">Masquage d’éléments de menu est un moyen de contrôler l’interface utilisateur de votre application et de restreindre les commandes de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7dfee-103">Hiding menu items is a way to control the user interface of your application and restrict user commands.</span></span> <span data-ttu-id="7dfee-104">Souvent, vous devez masquer un menu quand tous les éléments de menu sur ce dernier ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="7dfee-104">Often, you will want to hide an entire menu when all of the menu items on it are unavailable.</span></span> <span data-ttu-id="7dfee-105">Cela est moins distrait pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7dfee-105">This presents fewer distractions for the user.</span></span> <span data-ttu-id="7dfee-106">En outre, vous souhaiterez peut-être cacher et désactiver le menu ou un élément de menu, comme simple masquage n’empêche pas l’utilisateur d’accéder à une commande de menu à l’aide d’une touche de raccourci.</span><span class="sxs-lookup"><span data-stu-id="7dfee-106">Furthermore, you might want to both hide and disable the menu or menu item, as hiding alone does not prevent the user from accessing a menu command by using a shortcut key.</span></span>  
  
### <a name="to-hide-any-menu-item-programmatically"></a><span data-ttu-id="7dfee-107">Pour masquer un élément de menu par programme</span><span class="sxs-lookup"><span data-stu-id="7dfee-107">To hide any menu item programmatically</span></span>  
  
- <span data-ttu-id="7dfee-108">Dans la méthode où vous définissez les propriétés de l’élément de menu, ajoutez le code pour définir le <xref:System.Windows.Forms.ToolStripItem.Visible%2A> propriété `false`.</span><span class="sxs-lookup"><span data-stu-id="7dfee-108">Within the method where you set the properties of the menu item, add code to set the <xref:System.Windows.Forms.ToolStripItem.Visible%2A> property to `false`.</span></span>  
  
    ```vb  
    MenuItem3.Visible = False  
    ```  
  
    ```csharp  
    menuItem3.Visible = false;  
    ```  
  
    ```cpp  
    menuItem3->Visible = false;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="7dfee-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dfee-109">See also</span></span>

- <xref:System.Windows.Forms.ToolStripItem.Visible%2A>
- <xref:System.Windows.Forms.MenuStrip>
- [<span data-ttu-id="7dfee-110">Vue d'ensemble du contrôle MenuStrip</span><span class="sxs-lookup"><span data-stu-id="7dfee-110">MenuStrip Control Overview</span></span>](menustrip-control-overview-windows-forms.md)
- [<span data-ttu-id="7dfee-111">Guide pratique pour Désactiver des ToolStripMenuItems</span><span class="sxs-lookup"><span data-stu-id="7dfee-111">How to: Disable ToolStripMenuItems</span></span>](how-to-disable-toolstripmenuitems.md)
