---
title: 'Procédure : Ajouter et supprimer des nœuds avec le contrôle TreeView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- examples [Windows Forms], TreeView control
- TreeView control [Windows Forms], removing nodes
- tree nodes in TreeView control
- TreeView control [Windows Forms], adding nodes
ms.assetid: de1b82db-4905-449a-9f59-af271a6b6673
ms.openlocfilehash: 30dbe55711d92ea1fdbbbfd147a65b27d0dc9a50
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54711503"
---
# <a name="how-to-add-and-remove-nodes-with-the-windows-forms-treeview-control"></a>Procédure : Ajouter et supprimer des nœuds avec le contrôle TreeView Windows Forms
Les formulaires Windows <xref:System.Windows.Forms.TreeView> contrôle stocke les nœuds de niveau supérieur dans son <xref:System.Windows.Forms.TreeView.Nodes%2A> collection. Chaque <xref:System.Windows.Forms.TreeNode> possède également son propre <xref:System.Windows.Forms.TreeNode.Nodes%2A> collection pour stocker ses nœuds enfants. Les deux propriétés de collection sont de type <xref:System.Windows.Forms.TreeNodeCollection>, qui fournit des membres de collection standard qui vous permettent d’ajouter, supprimer et réorganiser les nœuds à un seul niveau de la hiérarchie de nœuds.  
  
### <a name="to-add-nodes-programmatically"></a>Pour ajouter des nœuds par programmation  
  
1.  Utilisez le <xref:System.Windows.Forms.TreeNodeCollection.Add%2A> (méthode) de l’arborescence <xref:System.Windows.Forms.TreeView.Nodes%2A> propriété.  
  
    ```vb  
    ' Adds new node as a child node of the currently selected node.  
    Dim newNode As TreeNode = New TreeNode("Text for new node")  
    TreeView1.SelectedNode.Nodes.Add(newNode)  
    ```  
  
    ```csharp  
    // Adds new node as a child node of the currently selected node.  
    TreeNode newNode = new TreeNode("Text for new node");  
    treeView1.SelectedNode.Nodes.Add(newNode);  
    ```  
  
    ```cpp  
    // Adds new node as a child node of the currently selected node.  
    TreeNode ^ newNode = new TreeNode("Text for new node");  
    treeView1->SelectedNode->Nodes->Add(newNode);  
    ```  
  
### <a name="to-remove-nodes-programmatically"></a>Pour supprimer des nœuds par programme  
  
1.  Utilisez le <xref:System.Windows.Forms.TreeNodeCollection.Remove%2A> (méthode) de l’arborescence <xref:System.Windows.Forms.TreeView.Nodes%2A> propriété à supprimer un nœud unique, ou le <xref:System.Windows.Forms.TreeNodeCollection.Clear%2A> méthode pour effacer tous les nœuds.  
  
    ```vb  
    ' Removes currently selected node, or root if nothing is selected.  
    TreeView1.Nodes.Remove(TreeView1.SelectedNode)  
    ' Clears all nodes.  
    TreeView1.Nodes.Clear()  
    ```  
  
    ```csharp  
    // Removes currently selected node, or root if nothing   
    // is selected.  
    treeView1.Nodes.Remove(treeView1.SelectedNode);  
    // Clears all nodes.  
    TreeView1.Nodes.Clear();  
    ```  
  
    ```cpp  
    // Removes currently selected node, or root if nothing  
    // is selected.  
    treeView1->Nodes->Remove(treeView1->SelectedNode);  
    // Clears all nodes.  
    treeView1->Nodes->Clear();  
    ```  
  
## <a name="see-also"></a>Voir aussi
- [TreeView, contrôle](../../../../docs/framework/winforms/controls/treeview-control-windows-forms.md)
- [Vue d’ensemble du contrôle TreeView](../../../../docs/framework/winforms/controls/treeview-control-overview-windows-forms.md)
- [Guide pratique pour Définir des icônes pour le contrôle TreeView Windows Forms](../../../../docs/framework/winforms/controls/how-to-set-icons-for-the-windows-forms-treeview-control.md)
- [Guide pratique pour Effectuer une itération dans tous les nœuds d’un contrôle de TreeView Windows Forms](../../../../docs/framework/winforms/controls/how-to-iterate-through-all-nodes-of-a-windows-forms-treeview-control.md)
- [Guide pratique pour Déterminer l’utilisateur a cliqué sur le nœud de TreeView](../../../../docs/framework/winforms/controls/how-to-determine-which-treeview-node-was-clicked-windows-forms.md)
- [Guide pratique pour Ajouter des informations personnalisées à un contrôle TreeView ou ListView (Windows Forms)](../../../../docs/framework/winforms/controls/add-custom-information-to-a-treeview-or-listview-control-wf.md)
