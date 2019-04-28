---
title: Modifications de DataTable
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: f08008a9-042e-4de9-94f3-4f0e502b1eb5
ms.openlocfilehash: 0300ceab16d9a94bd04468f7acd105e69d13e643
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61879838"
---
# <a name="datatable-edits"></a>Modifications de DataTable
Lorsque vous modifiez les valeurs de colonne d'un objet <xref:System.Data.DataRow>, les modifications sont immédiatement placées dans l'état actuel de la ligne. Le <xref:System.Data.DataRowState> est ensuite définie sur **Modified**, et les modifications sont acceptées ou rejetées à l’aide de la <xref:System.Data.DataRow.AcceptChanges%2A> ou <xref:System.Data.DataRow.RejectChanges%2A> méthodes de la **DataRow**. Le **DataRow** fournit également des trois méthodes que vous pouvez utiliser pour suspendre l’état de la ligne pendant sa modification. Ces méthodes sont <xref:System.Data.DataRow.BeginEdit%2A>, <xref:System.Data.DataRow.EndEdit%2A> et <xref:System.Data.DataRow.CancelEdit%2A>.  
  
 Lorsque vous modifiez les valeurs de colonne dans un **DataRow** directement, le **DataRow** gère les valeurs de colonne à l’aide de la **actuel**, **par défaut**, et **D’origine** versions de ligne. En plus de ces versions de ligne, le **BeginEdit**, **EndEdit**, et **CancelEdit** méthodes utilisent une quatrième : **Proposée**. Pour plus d’informations sur les versions de ligne, consultez [États des lignes et des Versions de ligne](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/row-states-and-row-versions.md).  
  
 Le **Proposed** version de ligne existe pendant une opération de modification commencée en appelant **BeginEdit** et qui termine à l’aide de **EndEdit** ou **CancelEdit,**  ou en appelant **AcceptChanges** ou **RejectChanges**.  
  
 Pendant l’opération de modification, vous pouvez appliquer la logique de validation à des colonnes individuelles en évaluant le **ProposedValue** dans le **ColumnChanged** événements de la **DataTable**. Le **ColumnChanged** contient des événements **DataColumnChangeEventArgs** qui conserve une référence à la colonne qui est en cours de modification et à la **ProposedValue**. Après avoir évalué la valeur proposée, vous pouvez la modifier ou annuler la modification. Lorsque la modification est terminée, la ligne quitte le **Proposed** état.  
  
 Vous pouvez confirmer les modifications en appelant **EndEdit**, ou vous pouvez les annuler en appelant **CancelEdit**. Notez que pendant **EndEdit** confirme vos modifications, le **DataSet** ne les accepte les modifications jusqu'à ce que **AcceptChanges** est appelée. Notez également que si vous appelez **AcceptChanges** avant de terminer la modification avec **EndEdit** ou **CancelEdit**, la modification est terminée et le **Proposed** les valeurs de ligne sont acceptées pour les deux le **actuel** et **d’origine** versions de ligne. De la même manière, l’appel **RejectChanges** termine la modification et ignore le **actuel** et **Proposed** versions de ligne. Appel **EndEdit** ou **CancelEdit** après avoir appelé **AcceptChanges** ou **RejectChanges** n’a aucun effet car la modification a déjà s’est terminée.  
  
 L’exemple suivant montre comment utiliser **BeginEdit** avec **EndEdit** et **CancelEdit**. L’exemple vérifie également la **ProposedValue** dans le **ColumnChanged** événement et décide s’il faut annuler la modification.  
  
```vb  
Dim workTable As DataTable = New DataTable  
workTable.Columns.Add("LastName", Type.GetType("System.String"))  
  
AddHandler workTable.ColumnChanged, _  
  New DataColumnChangeEventHandler(AddressOf OnColumnChanged)  
  
Dim workRow As DataRow = workTable.NewRow()  
workRow(0) = "Smith"  
workTable.Rows.Add(workRow)  
  
workRow.BeginEdit()  
' Causes the ColumnChanged event to write a message and cancel the edit.  
workRow(0) = ""       
workRow.EndEdit()  
  
' Displays "Smith, New".  
Console.WriteLine("{0}, {1}", workRow(0), workRow.RowState)  
  
Private Shared Sub OnColumnChanged( _  
  sender As Object, args As DataColumnChangeEventArgs)  
  If args.Column.ColumnName = "LastName" Then  
    If args.ProposedValue.ToString() = "" Then  
      Console.WriteLine("Last Name cannot be blank.  Edit canceled.")  
      args.Row.CancelEdit()  
    End If  
  End If  
End Sub  
```  
  
```csharp  
DataTable workTable  = new DataTable();  
workTable.Columns.Add("LastName", typeof(String));  
  
workTable.ColumnChanged +=   
  new DataColumnChangeEventHandler(OnColumnChanged);  
  
DataRow workRow = workTable.NewRow();  
workRow[0] = "Smith";  
workTable.Rows.Add(workRow);  
  
workRow.BeginEdit();  
// Causes the ColumnChanged event to write a message and cancel the edit.  
workRow[0] = "";       
workRow.EndEdit();  
  
// Displays "Smith, New".  
Console.WriteLine("{0}, {1}", workRow[0], workRow.RowState);    
  
protected static void OnColumnChanged(  
  Object sender, DataColumnChangeEventArgs args)  
{  
  if (args.Column.ColumnName == "LastName")  
    if (args.ProposedValue.ToString() == "")  
    {  
      Console.WriteLine("Last Name cannot be blank. Edit canceled.");  
      args.Row.CancelEdit();  
    }  
}  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Data.DataRow>
- <xref:System.Data.DataTable>
- <xref:System.Data.DataRowVersion>
- [Manipulation des données dans un DataTable](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/manipulating-data-in-a-datatable.md)
- [Gestion des événements de DataTable](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/handling-datatable-events.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
