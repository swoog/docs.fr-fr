---
title: 'Procédure : lier un contrôle ComboBox ou ListBox Windows Forms à des données'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data [Windows Forms], binding to controls
- list boxes [Windows Forms], data binding
- ComboBox control [Windows Forms], data binding
- data binding [Windows Forms], combo boxes
- ListBox control [Windows Forms], data binding
- combo boxes [Windows Forms], data binding
- bound controls [Windows Forms], combo boxes
- Windows Forms controls, data binding
- data-bound controls [Windows Forms], Windows Forms
ms.assetid: dfd7f081-8bea-4a41-86a3-86a1934828ef
ms.openlocfilehash: b869898a20008343b6c6cbe4bc7e399fc86fb232
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59306051"
---
# <a name="how-to-bind-a-windows-forms-combobox-or-listbox-control-to-data"></a>Procédure : lier un contrôle ComboBox ou ListBox Windows Forms à des données
Vous pouvez lier le <xref:System.Windows.Forms.ComboBox> et <xref:System.Windows.Forms.ListBox> entrant de nouvelles données aux données pour effectuer des tâches telles que l’exploration de données dans une base de données, ou la modification des données existantes.  
  
### <a name="to-bind-a-combobox-or-listbox-control"></a>Pour lier un contrôle ComboBox ou ListBox  
  
1. Définir le `DataSource` propriété à un objet de source de données. Sources de données possibles incluent un <xref:System.Windows.Forms.BindingSource> lié à des données, une table de données, une vue de données, un jeu de données, une vue de données manager, un tableau ou toute classe qui implémente le <xref:System.Collections.IList> interface. Pour plus d’informations, consultez [Sources de données prises en charge par les Windows Forms](../data-sources-supported-by-windows-forms.md).  
  
2. Si vous liez à une table, définissez la `DisplayMember` propriété le nom d’une colonne dans la source de données.  
  
     \- ou -  
  
     Si vous liez à un <xref:System.Collections.IList>, définissez le membre d’affichage à une propriété publique du type dans la liste.  
  
    ```vb  
    Private Sub BindComboBox()  
      ComboBox1.DataSource = DataSet1.Tables("Suppliers")  
      ComboBox1.DisplayMember = "ProductName"  
    End Sub  
    ```  
  
    ```csharp  
    private void BindComboBox()  
    {  
      comboBox1.DataSource = dataSet1.Tables["Suppliers"];  
      comboBox1.DisplayMember = "ProductName";  
    }  
    ```  
  
    > [!NOTE]
    >  Si vous êtes lié à une source de données qui n’implémente pas le <xref:System.ComponentModel.IBindingList> d’interface, comme un <xref:System.Collections.ArrayList>, données du contrôle lié ne seront pas mis à jour lorsque la source de données est mis à jour. Par exemple, si vous avez une zone de liste déroulante est liée à un <xref:System.Collections.ArrayList> et les données sont ajoutées à la <xref:System.Collections.ArrayList>, ces nouveaux éléments n’apparaîtront pas dans la zone de liste déroulante. Toutefois, vous pouvez forcer la zone de liste déroulante à mettre à jour en appelant le <xref:System.Windows.Forms.BindingManagerBase.SuspendBinding%2A> et <xref:System.Windows.Forms.BindingManagerBase.ResumeBinding%2A> méthodes sur l’instance de la <xref:System.Windows.Forms.BindingContext> classe à laquelle le contrôle est lié.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.ComboBox>
- <xref:System.Windows.Forms.ListBox>
- [Liaison de données Windows Forms](../windows-forms-data-binding.md)
- [Liaison de données et Windows Forms](../data-binding-and-windows-forms.md)
- [Contrôles Windows Forms utilisés pour l'affichage de listes d'options](windows-forms-controls-used-to-list-options.md)
