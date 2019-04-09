---
title: 'Procédure : attacher un menu contextuel à un nœud TreeView'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- shortcut menus [Windows Forms], adding to TreeView controls
- TreeView control [Windows Forms], adding shortcut menus
- tree nodes in TreeView control [Windows Forms], shortcut menus
ms.assetid: a23c6752-fd8f-44ad-b781-bab37962fc7c
ms.openlocfilehash: ba29e86f62c8d56b0d300d1841a70f434087dd84
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59100015"
---
# <a name="how-to-attach-a-shortcut-menu-to-a-treeview-node"></a><span data-ttu-id="0c17f-102">Procédure : attacher un menu contextuel à un nœud TreeView</span><span class="sxs-lookup"><span data-stu-id="0c17f-102">How to: Attach a ShortCut Menu to a TreeView Node</span></span>
<span data-ttu-id="0c17f-103">Les formulaires Windows <xref:System.Windows.Forms.TreeView> contrôle affiche une hiérarchie de nœuds, similaires aux fichiers et dossiers affichés dans le volet gauche de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="0c17f-103">The Windows Forms <xref:System.Windows.Forms.TreeView> control displays a hierarchy of nodes, similar to the files and folders displayed in the left pane of Windows Explorer.</span></span> <span data-ttu-id="0c17f-104">En définissant le <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> propriété, vous pouvez fournir des opérations contextuelles à l’utilisateur lorsqu’ils avec le bouton droit le <xref:System.Windows.Forms.TreeView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="0c17f-104">By setting the <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> property, you can provide context-sensitive operations to the user when they right-click the <xref:System.Windows.Forms.TreeView> control.</span></span> <span data-ttu-id="0c17f-105">En associant un <xref:System.Windows.Forms.ContextMenuStrip> composant individuels <xref:System.Windows.Forms.TreeNode> éléments, vous pouvez ajouter un niveau personnalisé de fonctionnalités de menu contextuel à votre <xref:System.Windows.Forms.TreeView> contrôles.</span><span class="sxs-lookup"><span data-stu-id="0c17f-105">By associating a <xref:System.Windows.Forms.ContextMenuStrip> component with individual <xref:System.Windows.Forms.TreeNode> items, you can add a customized level of shortcut menu functionality to your <xref:System.Windows.Forms.TreeView> controls.</span></span>  
  
### <a name="to-associate-a-shortcut-menu-with-a-treenode-programmatically"></a><span data-ttu-id="0c17f-106">Pour associer un menu contextuel à un TreeNode par programmation</span><span class="sxs-lookup"><span data-stu-id="0c17f-106">To associate a shortcut menu with a TreeNode programmatically</span></span>  
  
1.  <span data-ttu-id="0c17f-107">Instancier un <xref:System.Windows.Forms.TreeView> contrôler avec les paramètres de propriété approprié, créez une racine <xref:System.Windows.Forms.TreeNode>, puis ajoutez des sous-nœuds.</span><span class="sxs-lookup"><span data-stu-id="0c17f-107">Instantiate a <xref:System.Windows.Forms.TreeView> control with the appropriate property settings, create a root <xref:System.Windows.Forms.TreeNode>, and then add subnodes.</span></span>  
  
2.  <span data-ttu-id="0c17f-108">Instancier un <xref:System.Windows.Forms.ContextMenuStrip> composant, puis ajoutez un <xref:System.Windows.Forms.ToolStripMenuItem> pour chaque opération que vous souhaitez rendre disponible au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="0c17f-108">Instantiate a <xref:System.Windows.Forms.ContextMenuStrip> component, and then add a <xref:System.Windows.Forms.ToolStripMenuItem> for each operation you want to make available at run time.</span></span>  
  
3.  <span data-ttu-id="0c17f-109">Définir le <xref:System.Windows.Forms.TreeNode.ContextMenuStrip%2A> propriété d’approprié <xref:System.Windows.Forms.TreeNode> au menu contextuel que vous créez.</span><span class="sxs-lookup"><span data-stu-id="0c17f-109">Set the <xref:System.Windows.Forms.TreeNode.ContextMenuStrip%2A> property of the appropriate <xref:System.Windows.Forms.TreeNode> to the shortcut menu you create.</span></span>  
  
4.  <span data-ttu-id="0c17f-110">Lorsque cette propriété est définie, le menu contextuel s’affichera lorsque vous cliquez sur le nœud.</span><span class="sxs-lookup"><span data-stu-id="0c17f-110">When this property is set, the shortcut menu will be displayed when you right-click the node.</span></span>  
  
 <span data-ttu-id="0c17f-111">L’exemple de code suivant crée un base <xref:System.Windows.Forms.TreeView> et <xref:System.Windows.Forms.ContextMenuStrip> associée à la racine <xref:System.Windows.Forms.TreeNode> de la <xref:System.Windows.Forms.TreeView>.</span><span class="sxs-lookup"><span data-stu-id="0c17f-111">The following code example creates a basic <xref:System.Windows.Forms.TreeView> and <xref:System.Windows.Forms.ContextMenuStrip> associated with the root <xref:System.Windows.Forms.TreeNode> of the <xref:System.Windows.Forms.TreeView>.</span></span> <span data-ttu-id="0c17f-112">Vous devrez personnaliser les options de menu à ceux qui correspondent à la <xref:System.Windows.Forms.TreeView> vous développez.</span><span class="sxs-lookup"><span data-stu-id="0c17f-112">You will need to customize the menu choices to those that fit the <xref:System.Windows.Forms.TreeView> you are developing.</span></span> <span data-ttu-id="0c17f-113">En outre, vous devez écrire du code pour gérer le <xref:System.Windows.Forms.ToolStripItem.Click> événements pour ces éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="0c17f-113">Additionally, you will want to write code to handle the <xref:System.Windows.Forms.ToolStripItem.Click> events for these menu items.</span></span>  
  
 [!code-cpp[System.Windows.Forms.TreeNodeContextMenuStrip#1](~/samples/snippets/cpp/VS_Snippets_Winforms/system.windows.forms.TreeNodeContextMenuStrip/cpp/Form1.cpp#1)]
 [!code-csharp[System.Windows.Forms.TreeNodeContextMenuStrip#1](~/samples/snippets/csharp/VS_Snippets_Winforms/system.windows.forms.TreeNodeContextMenuStrip/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.TreeNodeContextMenuStrip#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/system.windows.forms.TreeNodeContextMenuStrip/VB/Form1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="0c17f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c17f-114">See also</span></span>

- <xref:System.Windows.Forms.ContextMenuStrip>
- [<span data-ttu-id="0c17f-115">TreeView, contrôle</span><span class="sxs-lookup"><span data-stu-id="0c17f-115">TreeView Control</span></span>](treeview-control-windows-forms.md)
