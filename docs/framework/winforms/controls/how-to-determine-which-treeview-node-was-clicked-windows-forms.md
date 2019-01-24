---
title: 'Procédure : Déterminer le nœud de TreeView cliqué (Windows Forms)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- TreeNode
helpviewer_keywords:
- examples [Windows Forms], TreeView control
- tree nodes in TreeView control [Windows Forms], determining node clicked
- TreeView control [Windows Forms], determining node clicked
ms.assetid: 06a4a191-d918-42af-9f49-956c93eff261
ms.openlocfilehash: 802367c26562d1b5aaf2398ed122cb97afbff255
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54580109"
---
# <a name="how-to-determine-which-treeview-node-was-clicked-windows-forms"></a>Procédure : Déterminer le nœud de TreeView cliqué (Windows Forms)
Lorsque vous travaillez avec les formulaires Windows <xref:System.Windows.Forms.TreeView> contrôle, une tâche courante consiste à déterminer le nœud sur lequel l’utilisateur a cliqué et réagir de façon appropriée.  
  
### <a name="to-determine-which-treeview-node-was-clicked"></a>Pour déterminer l’utilisateur a cliqué sur le nœud de TreeView  
  
1.  Utilisez le <xref:System.EventArgs> objet pour retourner une référence à l’objet de nœud cliqué.  
  
2.  Déterminer le nœud sur lequel l’utilisateur a cliqué en vérifiant la <xref:System.Windows.Forms.TreeViewEventArgs> classe, qui contient les données associées à l’événement.  
  
    ```vb  
    Private Sub TreeView1_AfterSelect(ByVal sender As System.Object, _  
    ByVal e As System.Windows.Forms.TreeViewEventArgs) Handles TreeView1.AfterSelect  
       ' Determine by checking the Node property of the TreeViewEventArgs.  
       MessageBox.Show(e.Node.Text)  
    End Sub  
    ```  
  
    ```csharp  
    protected void treeView1_AfterSelect (object sender,   
    System.Windows.Forms.TreeViewEventArgs e)  
    {  
       // Determine by checking the Text property.  
       MessageBox.Show(e.Node.Text);  
    }  
    ```  
  
    ```cpp  
    private:  
       void treeView1_AfterSelect(System::Object ^  sender,  
          System::Windows::Forms::TreeViewEventArgs ^  e)  
       {  
          // Determine by checking the Text property.  
          MessageBox::Show(e->Node->Text);  
       }  
    ```  
  
    > [!NOTE]
    >  Comme alternative, vous pouvez utiliser la <xref:System.Windows.Forms.MouseEventArgs> de la <xref:System.Windows.Forms.Control.MouseDown> ou <xref:System.Windows.Forms.Control.MouseUp> événement pour obtenir le <xref:System.Drawing.Point.X%2A> et <xref:System.Drawing.Point.Y%2A> coordonner les valeurs de la <xref:System.Drawing.Point> où le clic s’est produite. Ensuite, utilisez le <xref:System.Windows.Forms.TreeView> du contrôle <xref:System.Windows.Forms.TreeView.GetNodeAt%2A> méthode pour déterminer le nœud sur lequel l’utilisateur a cliqué.  
  
## <a name="see-also"></a>Voir aussi
- [TreeView, contrôle](../../../../docs/framework/winforms/controls/treeview-control-windows-forms.md)
