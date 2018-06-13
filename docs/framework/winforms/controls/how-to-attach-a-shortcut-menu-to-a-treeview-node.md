---
title: 'Comment : attacher un menu contextuel à un nœud TreeView'
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
ms.openlocfilehash: 737e74184b0763ed84b4e585f2508d69944d0e77
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33528218"
---
# <a name="how-to-attach-a-shortcut-menu-to-a-treeview-node"></a>Comment : attacher un menu contextuel à un nœud TreeView
Windows Forms <xref:System.Windows.Forms.TreeView> contrôle affiche une hiérarchie de nœuds, semblables aux fichiers et dossiers affichés dans le volet gauche de l’Explorateur Windows. En définissant le <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> propriété, vous pouvez fournir opérations contextuelles à l’utilisateur lorsque leur droit le <xref:System.Windows.Forms.TreeView> contrôle. En associant un <xref:System.Windows.Forms.ContextMenuStrip> composant avec une personne <xref:System.Windows.Forms.TreeNode> éléments, vous pouvez ajouter un niveau personnalisé de fonctionnalités de menu contextuel à votre <xref:System.Windows.Forms.TreeView> contrôles.  
  
### <a name="to-associate-a-shortcut-menu-with-a-treenode-programmatically"></a>Pour associer un menu contextuel à un TreeNode par programmation  
  
1.  Instancier une <xref:System.Windows.Forms.TreeView> contrôler avec des paramètres de propriété appropriés, créez une racine <xref:System.Windows.Forms.TreeNode>, puis ajoutez les sous-nœuds.  
  
2.  Instancier une <xref:System.Windows.Forms.ContextMenuStrip> composant, puis ajoutez un <xref:System.Windows.Forms.ToolStripMenuItem> pour chaque opération que vous souhaitez rendre disponible au moment de l’exécution.  
  
3.  Définir le <xref:System.Windows.Forms.TreeNode.ContextMenuStrip%2A> propriété d’approprié <xref:System.Windows.Forms.TreeNode> dans le menu contextuel que vous créez.  
  
4.  Lorsque cette propriété est définie, le menu contextuel s’affichera lorsque vous cliquez sur le nœud.  
  
 L’exemple de code suivant crée un base <xref:System.Windows.Forms.TreeView> et <xref:System.Windows.Forms.ContextMenuStrip> associée à la racine <xref:System.Windows.Forms.TreeNode> de la <xref:System.Windows.Forms.TreeView>. Vous devrez personnaliser les options de menu à ceux qui correspondent à la <xref:System.Windows.Forms.TreeView> vous développez. En outre, vous souhaitez écrire du code pour gérer les <xref:System.Windows.Forms.ToolStripItem.Click> événements pour ces éléments de menu.  
  
 [!code-cpp[System.Windows.Forms.TreeNodeContextMenuStrip#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/system.windows.forms.TreeNodeContextMenuStrip/cpp/Form1.cpp#1)]
 [!code-csharp[System.Windows.Forms.TreeNodeContextMenuStrip#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/system.windows.forms.TreeNodeContextMenuStrip/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.TreeNodeContextMenuStrip#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/system.windows.forms.TreeNodeContextMenuStrip/VB/Form1.vb#1)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.ContextMenuStrip>  
 [TreeView, contrôle](../../../../docs/framework/winforms/controls/treeview-control-windows-forms.md)
