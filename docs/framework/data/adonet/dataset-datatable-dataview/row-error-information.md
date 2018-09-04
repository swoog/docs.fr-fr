---
title: Informations sur l'erreur de ligne
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8b1f9070-d032-48c7-b030-bd8fbb2ca59a
ms.openlocfilehash: cf798ac88ba83e890086cec7424c8c363980718f
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43530543"
---
# <a name="row-error-information"></a>Informations sur l'erreur de ligne
Pour éviter d'avoir à répondre chaque fois qu'une erreur de ligne se produit pendant que vous modifiez des valeurs dans un objet <xref:System.Data.DataTable>, vous pouvez ajouter les informations d'erreur à la ligne pour une utilisation ultérieure. L'objet <xref:System.Data.DataRow> fournit une propriété <xref:System.Data.DataRow.RowError%2A> sur chaque ligne à cette fin. Ajout de données à la **RowError** propriété d’un **DataRow** définit le <xref:System.Data.DataRow.HasErrors%2A> propriété de la **DataRow** à **true**. Si le **DataRow** fait partie d’un **DataTable**, et **DataRow.HasErrors** est **true**, le **DataTable.HasErrors** propriété est également **true**. Cela s’applique également à la **DataSet** auquel le **DataTable** appartient. Lorsque vous testez les erreurs, vous pouvez vérifier le **HasErrors** propriété afin de déterminer si les informations d’erreur a été ajoutées à toutes les lignes. Si **HasErrors** est **true**, vous pouvez utiliser la <xref:System.Data.DataTable.GetErrors%2A> méthode de la **DataTable** à retourner et n’examiner uniquement les lignes avec des erreurs, comme illustré dans l’exemple suivant.  
  
```vb  
Dim workTable As DataTable = New DataTable("Customers")  
workTable.Columns.Add("CustID", Type.GetType("System.Int32"))  
workTable.Columns.Add("Total", Type.GetType("System.Double"))  
  
AddHandler workTable.RowChanged, New DataRowChangeEventHandler(AddressOf OnRowChanged)  
  
Dim i  As Int32  
  
For i  = 0 To 10  
  workTable.Rows.Add(New Object() {i , i *100})  
Next  
  
If workTable.HasErrors Then  
  Console.WriteLine("Errors in Table " & workTable.TableName)  
  
  Dim myRow As DataRow  
  
  For Each myRow In workTable.GetErrors()  
    Console.WriteLine("CustID = " & myRow("CustID").ToString())  
    Console.WriteLine(" Error = " & myRow.RowError & vbCrLf)  
  Next  
End If  
  
Private Shared Sub OnRowChanged( _  
    sender As Object, args As DataRowChangeEventArgs)  
  ' Check for zero values.  
  If CDbl(args.Row("Total")) = 0 Then args.Row.RowError = _  
      "Total cannot be 0."  
End Sub  
```  
  
```csharp  
DataTable  workTable = new DataTable("Customers");  
workTable.Columns.Add("CustID", typeof(Int32));  
workTable.Columns.Add("Total", typeof(Double));  
  
workTable.RowChanged += new DataRowChangeEventHandler(OnRowChanged);  
  
for (int i = 0; i < 10; i++)  
  workTable.Rows.Add(new Object[] {i, i*100});  
  
if (workTable.HasErrors)  
{  
  Console.WriteLine("Errors in Table " + workTable.TableName);  
  
  foreach (DataRow myRow in workTable.GetErrors())  
  {  
    Console.WriteLine("CustID = " + myRow["CustID"]);  
    Console.WriteLine(" Error = " + myRow.RowError + "\n");  
  }  
}  
  
protected static void OnRowChanged(  
    Object sender, DataRowChangeEventArgs args)  
{  
  // Check for zero values.  
  if (args.Row["Total"].Equals(0D))  
    args.Row.RowError = "Total cannot be 0.";  
}  
```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Data.DataColumnCollection>  
 <xref:System.Data.DataRow>  
 <xref:System.Data.DataTable>  
 [Manipulation des données dans un DataTable](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/manipulating-data-in-a-datatable.md)  
 [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
