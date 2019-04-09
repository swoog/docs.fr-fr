---
title: 'Procédure pas à pas : exécution d’une opération glisser-déplacer dans Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Forms, drag and drop operations
- drag and drop [Windows Forms], Windows Forms
ms.assetid: eb66f6bf-4a7d-4c2d-b276-40fefb2d3b6c
ms.openlocfilehash: e9b21d7bfa188ebb053f36e2637ffce5d6fa0dd7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59189025"
---
# <a name="walkthrough-performing-a-drag-and-drop-operation-in-windows-forms"></a>Procédure pas à pas : exécution d’une opération glisser-déplacer dans Windows Forms
Pour effectuer des opérations de glisser-déplacer dans des applications Windows vous devez gérer une série d’événements, plus particulièrement la <xref:System.Windows.Forms.Control.DragEnter>, <xref:System.Windows.Forms.Control.DragLeave>, et <xref:System.Windows.Forms.Control.DragDrop> événements. En utilisant les informations disponibles dans les arguments de ces événements, vous pouvez faciliter les opérations de glisser-déplacer.  
  
## <a name="dragging-data"></a>Faire glisser des données  
 Toutes les opérations de glisser-déplacer commencent par un glisser. La fonctionnalité pour activer les données puissent être collectées quand le glisser commence est implémentée dans le <xref:System.Windows.Forms.Control.DoDragDrop%2A> (méthode).  
  
 Dans l’exemple suivant, le <xref:System.Windows.Forms.Control.MouseDown> événement est utilisé pour démarrer l’opération glisser, car il est le plus intuitif (la plupart des actions de glisser-déplacer commencent par le bouton de la souris est enfoncé). N’oubliez cependant pas que n’importe quel événement peut être utilisé pour lancer une procédure de glisser-déplacer.  
  
> [!NOTE]
>  Certains contrôles ont des événements personnalisés spécifiques au glisser. Le <xref:System.Windows.Forms.ListView> et <xref:System.Windows.Forms.TreeView> contrôles, par exemple, ont un <xref:System.Windows.Forms.TreeView.ItemDrag> événement.  
  
#### <a name="to-start-a-drag-operation"></a>Pour démarrer une opération de glisser  
  
1.  Dans le <xref:System.Windows.Forms.Control.MouseDown> événement pour le contrôle où l’opération glisser commence, utilisez le `DoDragDrop` auront de méthode pour définir les données à faire glisser et l’effet autorisé du glissement. Pour plus d’informations, consultez <xref:System.Windows.Forms.DragEventArgs.Data%2A> et <xref:System.Windows.Forms.DragEventArgs.AllowedEffect%2A>.  
  
     L’exemple suivant montre comment initier une opération glisser. Le contrôle où l’opération glisser commence est un <xref:System.Windows.Forms.Button> contrôle, les données glissées est la chaîne qui représente le <xref:System.Windows.Forms.Control.Text%2A> propriété de la <xref:System.Windows.Forms.Button> contrôle et les effets autorisés soit copie ou de déplacement.  
  
    ```vb  
    Private Sub Button1_MouseDown(ByVal sender As Object, ByVal e As System.Windows.Forms.MouseEventArgs) Handles Button1.MouseDown  
       Button1.DoDragDrop(Button1.Text, DragDropEffects.Copy Or DragDropEffects.Move)  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_MouseDown(object sender,   
    System.Windows.Forms.MouseEventArgs e)  
    {  
       button1.DoDragDrop(button1.Text, DragDropEffects.Copy |   
          DragDropEffects.Move);  
    }  
    ```  
  
    > [!NOTE]
    >  Toutes les données peuvent être utilisées en tant que paramètre dans le `DoDragDrop` (méthode) ; dans l’exemple ci-dessus, le <xref:System.Windows.Forms.Control.Text%2A> propriété de la <xref:System.Windows.Forms.Button> contrôle a été utilisé (au lieu de coder en dur une valeur ou la récupération des données à partir d’un jeu de données), car la propriété était liée à la emplacement qui est glissé à partir de (la <xref:System.Windows.Forms.Button> contrôle). Gardez cela à l’esprit quand vous incorporez des opérations de glisser-déplacer dans vos applications Windows.  
  
 Pendant qu’une opération glisser est en vigueur, vous pouvez gérer le <xref:System.Windows.Forms.Control.QueryContinueDrag> événement, qui « demande l’autorisation » du système pour continuer l’opération glisser. Lors du traitement de cette méthode, il est également le moment approprié pour vous permettre d’appeler des méthodes qui ont une incidence sur l’opération glisser, telles que le développement un <xref:System.Windows.Forms.TreeNode> dans un <xref:System.Windows.Forms.TreeView> contrôler quand le curseur passe dessus.  
  
## <a name="dropping-data"></a>Déposer des données  
 Une fois que vous avez commencé à faire glisser des données à partir d’un emplacement sur un Windows Form ou un contrôle, vous voulez naturellement les déposer quelque part. Le curseur change quand il passe sur une zone d’un formulaire ou d’un contrôle qui est correctement configuré pour le dépôt des données. Toute zone dans un Windows Form ou un contrôle peut être configurée pour accepter les données déplacées en définissant le <xref:System.Windows.Forms.Control.AllowDrop%2A> propriété et la gestion de la <xref:System.Windows.Forms.Control.DragEnter> et <xref:System.Windows.Forms.Control.DragDrop> événements.  
  
#### <a name="to-perform-a-drop"></a>Pour effectuer un dépôt  
  
1.  Définir le <xref:System.Windows.Forms.Control.AllowDrop%2A> true à la propriété.  
  
2.  Dans le `DragEnter` événement pour le contrôle où le déplacement se produira, assurez-vous que les données glissées sont d’un type acceptable (dans ce cas, <xref:System.Windows.Forms.Control.Text%2A>). Le code définit ensuite l’effet produit lorsque le déplacement se produit sur une valeur dans la <xref:System.Windows.Forms.DragDropEffects> énumération. Pour plus d'informations, consultez <xref:System.Windows.Forms.DragEventArgs.Effect%2A>.  
  
    ```vb  
    Private Sub TextBox1_DragEnter(ByVal sender As Object, ByVal e As System.Windows.Forms.DragEventArgs) Handles TextBox1.DragEnter  
       If (e.Data.GetDataPresent(DataFormats.Text)) Then  
         e.Effect = DragDropEffects.Copy  
       Else  
         e.Effect = DragDropEffects.None  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void textBox1_DragEnter(object sender,   
    System.Windows.Forms.DragEventArgs e)  
    {  
       if (e.Data.GetDataPresent(DataFormats.Text))   
          e.Effect = DragDropEffects.Copy;  
       else  
          e.Effect = DragDropEffects.None;  
    }  
    ```  
  
    > [!NOTE]
    >  Vous pouvez définir vos propres <xref:System.Windows.Forms.DataFormats> en spécifiant votre propre objet en tant que le <xref:System.Object> paramètre de la <xref:System.Windows.Forms.DataObject.SetData%2A> (méthode). Pour cela, vérifiez que l’objet spécifié est sérialisable. Pour plus d'informations, consultez <xref:System.Runtime.Serialization.ISerializable>.  
  
3.  Dans le <xref:System.Windows.Forms.Control.DragDrop> événement pour le contrôle où le déplacement se produira, utilisez la <xref:System.Windows.Forms.DataObject.GetData%2A> méthode pour récupérer les données glissées. Pour plus d'informations, consultez <xref:System.Security.Cryptography.Xml.DataObject.Data%2A>.  
  
     Dans l’exemple ci-dessous, un <xref:System.Windows.Forms.TextBox> contrôle est le contrôle de destination du glisser (où le dépôt sera effectué). Le code définit le <xref:System.Windows.Forms.Control.Text%2A> propriété de la <xref:System.Windows.Forms.TextBox> contrôler égale aux données glissées.  
  
    ```vb  
    Private Sub TextBox1_DragDrop(ByVal sender As Object, ByVal e As System.Windows.Forms.DragEventArgs) Handles TextBox1.DragDrop  
       TextBox1.Text = e.Data.GetData(DataFormats.Text).ToString  
    End Sub  
    ```  
  
    ```csharp  
    private void textBox1_DragDrop(object sender,   
    System.Windows.Forms.DragEventArgs e)  
    {  
       textBox1.Text = e.Data.GetData(DataFormats.Text).ToString();  
    }  
    ```  
  
    > [!NOTE]
    >  En outre, vous pouvez travailler avec le <xref:System.Windows.Forms.DragEventArgs.KeyState%2A> propriété, afin que, selon les touches enfoncées pendant l’opération de glisser-déplacer, certains effets se produisent (par exemple, il est standard pour copier les données glissées quand la touche CTRL est enfoncée).  
  
## <a name="see-also"></a>Voir aussi

- [Procédure : ajouter des données au Presse-papiers](how-to-add-data-to-the-clipboard.md)
- [Procédure : récupérer des données dans le Presse-papiers](how-to-retrieve-data-from-the-clipboard.md)
- [Opérations glisser-déposer et prise en charge du Presse-papiers](drag-and-drop-operations-and-clipboard-support.md)
