---
title: 'Comment : déterminer des éléments cochés dans le contrôle CheckedListBox Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- check boxes [Windows Forms], determining checked state
- CheckedListBox control [Windows Forms], determining checked state
ms.assetid: 178b477d-27c9-489c-8914-44a9623a4d41
ms.openlocfilehash: 70884051ba440c5d0f9d282b7edf189c8f52807e
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43505437"
---
# <a name="how-to-determine-checked-items-in-the-windows-forms-checkedlistbox-control"></a>Comment : déterminer des éléments cochés dans le contrôle CheckedListBox Windows Forms
Lors de la présentation des données dans un formulaire Windows <xref:System.Windows.Forms.CheckedListBox> contrôle, vous pouvez soit itérer sur la collection stockée dans le <xref:System.Windows.Forms.CheckedListBox.CheckedItems%2A> propriété, ou parcourez la liste à l’aide de la <xref:System.Windows.Forms.CheckedListBox.GetItemChecked%2A> méthode pour déterminer quels éléments sont activés. Le <xref:System.Windows.Forms.CheckedListBox.GetItemChecked%2A> méthode prend un numéro d’index comme argument et retourne `true` ou `false`. Contrairement à ce que vous attendez, le <xref:System.Windows.Forms.ListBox.SelectedItems%2A> et <xref:System.Windows.Forms.ListBox.SelectedIndices%2A> propriétés ne déterminent pas quels éléments sont activés ; ils déterminent quels éléments sont mis en surbrillance.  
  
### <a name="to-determine-checked-items-in-a-checkedlistbox-control"></a>Pour déterminer les éléments cochés dans un contrôle CheckedListBox  
  
1.  Effectuer une itération dans le <xref:System.Windows.Forms.CheckedListBox.CheckedItems%2A> collection, en commençant à 0, étant donné que la collection est de base zéro. Notez que cette méthode vous donnera le numéro d’élément dans la liste d’éléments activés, pas la liste globale. Par conséquent, si le premier élément dans la liste n’est pas vérifié et le deuxième élément est activé, le code ci-dessous contient un texte tel que « Checked Item 1 = MyListItem2 ».  
  
    ```vb  
    ' Determine if there are any items checked.  
    If CheckedListBox1.CheckedItems.Count <> 0 Then  
       ' If so, loop through all checked items and print results.  
       Dim x As Integer  
       Dim s As String = ""  
       For x = 0 To CheckedListBox1.CheckedItems.Count - 1  
          s = s & "Checked Item " & (x + 1).ToString & " = " & CheckedListBox1.CheckedItems(x).ToString & ControlChars.CrLf  
       Next x  
       MessageBox.Show(s)  
    End If  
    ```  
  
    ```csharp  
    // Determine if there are any items checked.  
    if(checkedListBox1.CheckedItems.Count != 0)  
    {  
       // If so, loop through all checked items and print results.  
       string s = "";  
       for(int x = 0; x < checkedListBox1.CheckedItems.Count ; x++)  
       {  
          s = s + "Checked Item " + (x+1).ToString() + " = " + checkedListBox1.CheckedItems[x].ToString() + "\n";  
       }  
       MessageBox.Show(s);  
    }  
    ```  
  
    ```cpp  
    // Determine if there are any items checked.  
    if(checkedListBox1->CheckedItems->Count != 0)  
    {  
       // If so, loop through all checked items and print results.  
       String ^ s = "";  
       for(int x = 0; x < checkedListBox1->CheckedItems->Count; x++)  
       {  
          s = String::Concat(s, "Checked Item ", (x+1).ToString(),  
             " = ", checkedListBox1->CheckedItems[x]->ToString(),  
             "\n");  
       }  
       MessageBox::Show(s);  
    }  
    ```  
  
     - ou  
  
2.  Parcourir le <xref:System.Windows.Forms.CheckedListBox.Items%2A> collection, en commençant à 0, étant donné que la collection est de base zéro et appeler le <xref:System.Windows.Forms.CheckedListBox.GetItemChecked%2A> méthode pour chaque élément. Notez que cette méthode vous donnera le numéro d’élément dans la liste globale, afin que si le premier élément dans la liste n’est pas activée et le deuxième élément est activé, il affiche quelque chose comme « élément 2 = MyListItem2 ».  
  
    ```vb  
    Dim i As Integer  
    Dim s As String  
    s = "Checked Items:" & ControlChars.CrLf  
    For i = 0 To (CheckedListBox1.Items.Count - 1)  
       If CheckedListBox1.GetItemChecked(i) = True Then  
          s = s & "Item " & (i + 1).ToString & " = " & CheckedListBox1.Items(i).ToString & ControlChars.CrLf  
       End If  
    Next  
    MessageBox.Show(s)  
    ```  
  
    ```csharp  
    int i;  
    string s;   
    s = "Checked items:\n" ;  
    for (i = 0; i <= (checkedListBox1.Items.Count-1); i++)  
    {  
       if (checkedListBox1.GetItemChecked(i))  
       {  
          s = s + "Item " + (i+1).ToString() + " = " + checkedListBox1.Items[i].ToString() + "\n";  
       }  
    }  
    MessageBox.Show (s);  
    ```  
  
    ```cpp  
    int i;  
    String ^ s;   
    s = "Checked items:\n" ;  
    for (i = 0; i <= (checkedListBox1->Items->Count-1); i++)  
    {  
       if (checkedListBox1->GetItemChecked(i))  
       {  
          s = String::Concat(s, "Item ", (i+1).ToString(), " = ",  
             checkedListBox1->Item[i]->ToString(), "\n");  
       }  
    }  
    MessageBox::Show(s);  
    ```  
  
## <a name="see-also"></a>Voir aussi  
 [Contrôles Windows Forms utilisés pour l’affichage de listes d’options](../../../../docs/framework/winforms/controls/windows-forms-controls-used-to-list-options.md)
