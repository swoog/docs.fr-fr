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
# <a name="how-to-add-and-remove-nodes-with-the-windows-forms-treeview-control"></a><span data-ttu-id="ab991-102">Procédure : Ajouter et supprimer des nœuds avec le contrôle TreeView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ab991-102">How to: Add and Remove Nodes with the Windows Forms TreeView Control</span></span>
<span data-ttu-id="ab991-103">Les formulaires Windows <xref:System.Windows.Forms.TreeView> contrôle stocke les nœuds de niveau supérieur dans son <xref:System.Windows.Forms.TreeView.Nodes%2A> collection.</span><span class="sxs-lookup"><span data-stu-id="ab991-103">The Windows Forms <xref:System.Windows.Forms.TreeView> control stores the top-level nodes in its <xref:System.Windows.Forms.TreeView.Nodes%2A> collection.</span></span> <span data-ttu-id="ab991-104">Chaque <xref:System.Windows.Forms.TreeNode> possède également son propre <xref:System.Windows.Forms.TreeNode.Nodes%2A> collection pour stocker ses nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="ab991-104">Each <xref:System.Windows.Forms.TreeNode> also has its own <xref:System.Windows.Forms.TreeNode.Nodes%2A> collection to store its child nodes.</span></span> <span data-ttu-id="ab991-105">Les deux propriétés de collection sont de type <xref:System.Windows.Forms.TreeNodeCollection>, qui fournit des membres de collection standard qui vous permettent d’ajouter, supprimer et réorganiser les nœuds à un seul niveau de la hiérarchie de nœuds.</span><span class="sxs-lookup"><span data-stu-id="ab991-105">Both collection properties are of type <xref:System.Windows.Forms.TreeNodeCollection>, which provides standard collection members that enable you to add, remove, and rearrange the nodes at a single level of the node hierarchy.</span></span>  
  
### <a name="to-add-nodes-programmatically"></a><span data-ttu-id="ab991-106">Pour ajouter des nœuds par programmation</span><span class="sxs-lookup"><span data-stu-id="ab991-106">To add nodes programmatically</span></span>  
  
1.  <span data-ttu-id="ab991-107">Utilisez le <xref:System.Windows.Forms.TreeNodeCollection.Add%2A> (méthode) de l’arborescence <xref:System.Windows.Forms.TreeView.Nodes%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="ab991-107">Use the <xref:System.Windows.Forms.TreeNodeCollection.Add%2A> method of the tree view's <xref:System.Windows.Forms.TreeView.Nodes%2A> property.</span></span>  
  
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
  
### <a name="to-remove-nodes-programmatically"></a><span data-ttu-id="ab991-108">Pour supprimer des nœuds par programme</span><span class="sxs-lookup"><span data-stu-id="ab991-108">To remove nodes programmatically</span></span>  
  
1.  <span data-ttu-id="ab991-109">Utilisez le <xref:System.Windows.Forms.TreeNodeCollection.Remove%2A> (méthode) de l’arborescence <xref:System.Windows.Forms.TreeView.Nodes%2A> propriété à supprimer un nœud unique, ou le <xref:System.Windows.Forms.TreeNodeCollection.Clear%2A> méthode pour effacer tous les nœuds.</span><span class="sxs-lookup"><span data-stu-id="ab991-109">Use the <xref:System.Windows.Forms.TreeNodeCollection.Remove%2A> method of the tree view's <xref:System.Windows.Forms.TreeView.Nodes%2A> property to remove a single node, or the <xref:System.Windows.Forms.TreeNodeCollection.Clear%2A> method to clear all nodes.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="ab991-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab991-110">See also</span></span>
- [<span data-ttu-id="ab991-111">TreeView, contrôle</span><span class="sxs-lookup"><span data-stu-id="ab991-111">TreeView Control</span></span>](../../../../docs/framework/winforms/controls/treeview-control-windows-forms.md)
- [<span data-ttu-id="ab991-112">Vue d’ensemble du contrôle TreeView</span><span class="sxs-lookup"><span data-stu-id="ab991-112">TreeView Control Overview</span></span>](../../../../docs/framework/winforms/controls/treeview-control-overview-windows-forms.md)
- [<span data-ttu-id="ab991-113">Guide pratique pour Définir des icônes pour le contrôle TreeView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ab991-113">How to: Set Icons for the Windows Forms TreeView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-set-icons-for-the-windows-forms-treeview-control.md)
- [<span data-ttu-id="ab991-114">Guide pratique pour Effectuer une itération dans tous les nœuds d’un contrôle de TreeView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ab991-114">How to: Iterate Through All Nodes of a Windows Forms TreeView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-iterate-through-all-nodes-of-a-windows-forms-treeview-control.md)
- [<span data-ttu-id="ab991-115">Guide pratique pour Déterminer l’utilisateur a cliqué sur le nœud de TreeView</span><span class="sxs-lookup"><span data-stu-id="ab991-115">How to: Determine Which TreeView Node Was Clicked</span></span>](../../../../docs/framework/winforms/controls/how-to-determine-which-treeview-node-was-clicked-windows-forms.md)
- [<span data-ttu-id="ab991-116">Guide pratique pour Ajouter des informations personnalisées à un contrôle TreeView ou ListView (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="ab991-116">How to: Add Custom Information to a TreeView or ListView Control (Windows Forms)</span></span>](../../../../docs/framework/winforms/controls/add-custom-information-to-a-treeview-or-listview-control-wf.md)
