---
title: 'Procédure : Attacher un Menu contextuel à un nœud TreeView'
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
ms.openlocfilehash: 537593399db7deb775929cd742a749ce47890db6
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57703612"
---
# <a name="how-to-attach-a-shortcut-menu-to-a-treeview-node"></a>Procédure : Attacher un Menu contextuel à un nœud TreeView
Les formulaires Windows <xref:System.Windows.Forms.TreeView> contrôle affiche une hiérarchie de nœuds, similaires aux fichiers et dossiers affichés dans le volet gauche de l’Explorateur Windows. En définissant le <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> propriété, vous pouvez fournir des opérations contextuelles à l’utilisateur lorsqu’ils avec le bouton droit le <xref:System.Windows.Forms.TreeView> contrôle. En associant un <xref:System.Windows.Forms.ContextMenuStrip> composant individuels <xref:System.Windows.Forms.TreeNode> éléments, vous pouvez ajouter un niveau personnalisé de fonctionnalités de menu contextuel à votre <xref:System.Windows.Forms.TreeView> contrôles.  
  
### <a name="to-associate-a-shortcut-menu-with-a-treenode-programmatically"></a>Pour associer un menu contextuel à un TreeNode par programmation  
  
1.  Instancier un <xref:System.Windows.Forms.TreeView> contrôler avec les paramètres de propriété approprié, créez une racine <xref:System.Windows.Forms.TreeNode>, puis ajoutez des sous-nœuds.  
  
2.  Instancier un <xref:System.Windows.Forms.ContextMenuStrip> composant, puis ajoutez un <xref:System.Windows.Forms.ToolStripMenuItem> pour chaque opération que vous souhaitez rendre disponible au moment de l’exécution.  
  
3.  Définir le <xref:System.Windows.Forms.TreeNode.ContextMenuStrip%2A> propriété d’approprié <xref:System.Windows.Forms.TreeNode> au menu contextuel que vous créez.  
  
4.  Lorsque cette propriété est définie, le menu contextuel s’affichera lorsque vous cliquez sur le nœud.  
  
 L’exemple de code suivant crée un base <xref:System.Windows.Forms.TreeView> et <xref:System.Windows.Forms.ContextMenuStrip> associée à la racine <xref:System.Windows.Forms.TreeNode> de la <xref:System.Windows.Forms.TreeView>. Vous devrez personnaliser les options de menu à ceux qui correspondent à la <xref:System.Windows.Forms.TreeView> vous développez. En outre, vous devez écrire du code pour gérer le <xref:System.Windows.Forms.ToolStripItem.Click> événements pour ces éléments de menu.  
  
 [!code-cpp[System.Windows.Forms.TreeNodeContextMenuStrip#1](~/samples/snippets/cpp/VS_Snippets_Winforms/system.windows.forms.TreeNodeContextMenuStrip/cpp/Form1.cpp#1)]
 [!code-csharp[System.Windows.Forms.TreeNodeContextMenuStrip#1](~/samples/snippets/csharp/VS_Snippets_Winforms/system.windows.forms.TreeNodeContextMenuStrip/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.TreeNodeContextMenuStrip#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/system.windows.forms.TreeNodeContextMenuStrip/VB/Form1.vb#1)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ContextMenuStrip>
- [TreeView, contrôle](treeview-control-windows-forms.md)
