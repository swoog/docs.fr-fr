---
title: 'Procédure : ajouter et supprimer des éléments dans un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- combo boxes [Windows Forms], adding items
- list boxes [Windows Forms], removing items
- ComboBox control [Windows Forms], adding and removing items
- ListBox control [Windows Forms], adding and removing items
- list boxes [Windows Forms], adding items
- combo boxes [Windows Forms], removing items
- CheckedListBox control [Windows Forms], adding and removing items
ms.assetid: 7224c8d2-4118-443e-ae1e-d7c17d1e69ee
ms.openlocfilehash: bd6614c76c63a44a7367ac7c7113c4db260c9a02
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61640441"
---
# <a name="how-to-add-and-remove-items-from-a-windows-forms-combobox-listbox-or-checkedlistbox-control"></a>Procédure : ajouter et supprimer des éléments dans un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms
Les éléments peuvent être ajoutés à une zone de liste déroulante Windows Forms, zone de liste, ou vérifié la zone de liste de plusieurs façons, étant donné que ces contrôles peuvent être liés à une variété de sources de données. Toutefois, cette rubrique illustre la méthode la plus simple et ne nécessite aucune liaison de données. Les éléments affichés sont généralement des chaînes ; Toutefois, n’importe quel objet peut être utilisé. Le texte qui s’affiche dans le contrôle est la valeur retournée par l’objet `ToString` (méthode).  
  
### <a name="to-add-items"></a>Pour ajouter des éléments  
  
1. Ajouter la chaîne ou l’objet à la liste à l’aide de la `Add` méthode de la `ObjectCollection` classe. La collection est référencée à l’aide de la `Items` propriété :  
  
    ```vb  
    ComboBox1.Items.Add("Tokyo")  
    ```  
  
    ```csharp  
    comboBox1.Items.Add("Tokyo");  
    ```  
  
    ```cpp  
    comboBox1->Items->Add("Tokyo");  
    ```  
  
     - ou  
  
2. Insérer la chaîne ou l’objet à l’endroit souhaité dans la liste avec la `Insert` méthode :  
  
    ```vb  
    CheckedListBox1.Items.Insert(0, "Copenhagen")  
    ```  
  
    ```csharp  
    checkedListBox1.Items.Insert(0, "Copenhagen");  
    ```  
  
    ```cpp  
    checkedListBox1->Items->Insert(0, "Copenhagen");  
    ```  
  
     - ou  
  
3. Assignez tout un tableau à la `Items` collection :  
  
    ```vb  
    Dim ItemObject(9) As System.Object  
    Dim i As Integer  
       For i = 0 To 9  
       ItemObject(i) = "Item" & i  
    Next i  
    ListBox1.Items.AddRange(ItemObject)  
    ```  
  
    ```csharp  
    System.Object[] ItemObject = new System.Object[10];  
    for (int i = 0; i <= 9; i++)  
    {  
       ItemObject[i] = "Item" + i;  
    }  
    listBox1.Items.AddRange(ItemObject);  
    ```  
  
    ```cpp  
    Array<System::Object^>^ ItemObject = gcnew Array<System::Object^>(10);  
    for (int i = 0; i <= 9; i++)  
    {  
       ItemObject[i] = String::Concat("Item", i.ToString());  
    }  
    listBox1->Items->AddRange(ItemObject);  
    ```  
  
### <a name="to-remove-an-item"></a>Pour supprimer un élément  
  
1. Appelez le `Remove` ou `RemoveAt` méthode pour supprimer des éléments.  
  
     `Remove` possède un argument qui spécifie l’élément à supprimer.`RemoveAt` Supprime l’élément avec le numéro d’index spécifié.  
  
    ```vb  
    ' To remove item with index 0:  
    ComboBox1.Items.RemoveAt(0)  
    ' To remove currently selected item:  
    ComboBox1.Items.Remove(ComboBox1.SelectedItem)  
    ' To remove "Tokyo" item:  
    ComboBox1.Items.Remove("Tokyo")  
    ```  
  
    ```csharp  
    // To remove item with index 0:  
    comboBox1.Items.RemoveAt(0);  
    // To remove currently selected item:  
    comboBox1.Items.Remove(comboBox1.SelectedItem);  
    // To remove "Tokyo" item:  
    comboBox1.Items.Remove("Tokyo");  
    ```  
  
    ```cpp  
    // To remove item with index 0:  
    comboBox1->Items->RemoveAt(0);  
    // To remove currently selected item:  
    comboBox1->Items->Remove(comboBox1->SelectedItem);  
    // To remove "Tokyo" item:  
    comboBox1->Items->Remove("Tokyo");  
    ```  
  
### <a name="to-remove-all-items"></a>Pour supprimer tous les éléments  
  
1. Appelez le `Clear` méthode pour supprimer tous les éléments de la collection :  
  
    ```vb  
    ListBox1.Items.Clear()  
    ```  
  
    ```csharp  
    listBox1.Items.Clear();  
    ```  
  
    ```cpp  
    listBox1->Items->Clear();  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.ComboBox>
- <xref:System.Windows.Forms.ListBox>
- <xref:System.Windows.Forms.CheckedListBox>
- [Guide pratique pour Trier le contenu d’un Windows Forms ComboBox, ListBox ou CheckedListBox, contrôle](sort-the-contents-of-a-wf-combobox-listbox-or-checkedlistbox-control.md)
- [Utilisation d'un contrôle ComboBox Windows Forms à la place d'un contrôle ListBox](when-to-use-a-windows-forms-combobox-instead-of-a-listbox.md)
- [Contrôles Windows Forms utilisés pour l’affichage de listes d’options](windows-forms-controls-used-to-list-options.md)
