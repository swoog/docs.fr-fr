---
title: 'Procédure : désactiver des ToolStripMenuItems à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolStripMenuItems [Windows Forms], disabling in designer
- MenuStrip control [Windows Forms], disabling menu items in designer
- menu items [Windows Forms], disabling
- menus [Windows Forms], disabling items
ms.assetid: 985e311e-7d67-4205-b5a3-d045b68a4a03
ms.openlocfilehash: 9965825458afcd50b29699c3b89ed506078e04d9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59338057"
---
# <a name="how-to-disable-toolstripmenuitems-using-the-designer"></a><span data-ttu-id="27439-102">Procédure : désactiver des ToolStripMenuItems à l’aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="27439-102">How to: Disable ToolStripMenuItems Using the Designer</span></span>
<span data-ttu-id="27439-103">Vous pouvez limiter ou élargir les commandes de que l’utilisateur peut effectuer par activation et désactivation des éléments de menu en réponse aux activités de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="27439-103">You can limit or broaden the commands a user may make by enabling and disabling menu items in response to user activities.</span></span> <span data-ttu-id="27439-104">Éléments de menu sont activées par défaut lorsqu’ils sont créés, mais cela peut être ajusté via la <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="27439-104">Menu items are enabled by default when they are created, but this can be adjusted through the <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A> property.</span></span> <span data-ttu-id="27439-105">Vous pouvez manipuler cette propriété au moment du design dans le **propriétés** fenêtre ou par programme en la définissant dans le code.</span><span class="sxs-lookup"><span data-stu-id="27439-105">You can manipulate this property at design time in the **Properties** window or programmatically by setting it in code.</span></span> <span data-ttu-id="27439-106">Pour plus d'informations, voir [Procédure : Désactiver des ToolStripMenuItems](how-to-disable-toolstripmenuitems.md).</span><span class="sxs-lookup"><span data-stu-id="27439-106">For more information, see [How to: Disable ToolStripMenuItems](how-to-disable-toolstripmenuitems.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="27439-107">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="27439-107">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="27439-108">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="27439-108">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="27439-109">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="27439-109">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-disable-a-menu-item-at-design-time"></a><span data-ttu-id="27439-110">Pour désactiver un élément de menu au moment du design</span><span class="sxs-lookup"><span data-stu-id="27439-110">To disable a menu item at design time</span></span>  
  
1. <span data-ttu-id="27439-111">Avec l’élément de menu sélectionné sur le formulaire, définissez la <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A> propriété `false`.</span><span class="sxs-lookup"><span data-stu-id="27439-111">With the menu item selected on the form, set the <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A> property to `false`.</span></span>  
  
    > [!TIP]
    >  <span data-ttu-id="27439-112">La désactivation de l’élément de menu de première ou de niveau supérieur dans un menu désactive tous les éléments de menu contenus dans le menu.</span><span class="sxs-lookup"><span data-stu-id="27439-112">Disabling the first or top-level menu item in a menu disables all the menu items contained within the menu.</span></span> <span data-ttu-id="27439-113">De même, la désactivation d’un élément de menu ayant des éléments de sous-menu désactive les éléments de sous-menu.</span><span class="sxs-lookup"><span data-stu-id="27439-113">Likewise, disabling a menu item that has submenu items disables the submenu items.</span></span> <span data-ttu-id="27439-114">Si toutes les commandes de menu ne sont pas disponibles à l’utilisateur, il est considéré comme bonne pratique de programmation à cacher et désactiver le menu entier, comme cela présente une interface utilisateur propre.</span><span class="sxs-lookup"><span data-stu-id="27439-114">If all the commands on a given menu are unavailable to the user, it is considered good programming practice to both hide and disable the entire menu, as this presents a clean user interface.</span></span> <span data-ttu-id="27439-115">Vous devez à la fois masquer et désactiver le menu, comme simple masquage n’empêche pas l’accès à une commande de menu via une touche de raccourci.</span><span class="sxs-lookup"><span data-stu-id="27439-115">You should both hide and disable the menu, as hiding alone does not prevent access to a menu command via a shortcut key.</span></span> <span data-ttu-id="27439-116">Définir le <xref:System.Windows.Forms.ToolStripItem.Visible%2A> propriété d’un élément de menu de niveau supérieur pour `false` masquer le menu.</span><span class="sxs-lookup"><span data-stu-id="27439-116">Set the <xref:System.Windows.Forms.ToolStripItem.Visible%2A> property of a top-level menu item to `false` to hide the entire menu.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="27439-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27439-117">See also</span></span>

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- [<span data-ttu-id="27439-118">Guide pratique pour Masquer des ToolStripMenuItems</span><span class="sxs-lookup"><span data-stu-id="27439-118">How to: Hide ToolStripMenuItems</span></span>](how-to-hide-toolstripmenuitems.md)
- [<span data-ttu-id="27439-119">Vue d'ensemble du contrôle MenuStrip</span><span class="sxs-lookup"><span data-stu-id="27439-119">MenuStrip Control Overview</span></span>](menustrip-control-overview-windows-forms.md)
