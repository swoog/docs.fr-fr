---
title: 'Procédure : accéder à des éléments spécifiques dans un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ComboBox control [Windows Forms], accessing items
- ListBox control [Windows Forms], returning item information
- list boxes [Windows Forms], accessing items
- ListBox control [Windows Forms], accessing items
- combo boxes [Windows Forms], accessing items
- CheckedListBox control [Windows Forms], accessing items
ms.assetid: 1216742f-bcf9-4ff8-8a62-d7c9053c2b96
ms.openlocfilehash: 3d61a9b38f809d16e95b485893acaadcf04d826f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59077210"
---
# <a name="how-to-access-specific-items-in-a-windows-forms-combobox-listbox-or-checkedlistbox-control"></a>Procédure : accéder à des éléments spécifiques dans un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms
Accès aux éléments d’une zone de liste déroulante Windows Forms, la zone de liste ou la zone de liste vérifiés est une tâche essentielle. Il vous permet de déterminer par programme les nouveautés dans la liste, à n’importe quelle position donnée.  
  
### <a name="to-access-a-specific-item"></a>Pour accéder à un élément spécifique  
  
1.  Requête la `Items` collection à l’aide de l’index de l’élément spécifique :  
  
    ```vb  
    Private Function GetItemText(i As Integer) As String  
       ' Return the text of the item using the index:  
       Return ComboBox1.Items(i).ToString  
    End Function  
    ```  
  
    ```csharp  
    private string GetItemText(int i)  
    {  
       // Return the text of the item using the index:  
       return (comboBox1.Items[i].ToString());  
    }  
    ```  
  
    ```cpp  
    private:  
       String^ GetItemText(int i)  
       {  
          // Return the text of the item using the index:  
          return (comboBox1->Items->Item[i]->ToString());  
       }  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.ComboBox>
- <xref:System.Windows.Forms.ListBox>
- <xref:System.Windows.Forms.CheckedListBox>
- [Contrôles Windows Forms utilisés pour l'affichage de listes d'options](windows-forms-controls-used-to-list-options.md)
