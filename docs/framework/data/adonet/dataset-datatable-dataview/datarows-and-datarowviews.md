---
title: DataRows et DataRowViews
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8f5eec26-b809-4aca-8778-7e202356d856
ms.openlocfilehash: 14e210c36ee2ab8ddba7451ac7b346ad72288d94
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59096353"
---
# <a name="datarows-and-datarowviews"></a><span data-ttu-id="3e98c-102">DataRows et DataRowViews</span><span class="sxs-lookup"><span data-stu-id="3e98c-102">DataRows and DataRowViews</span></span>
<span data-ttu-id="3e98c-103">Un objet <xref:System.Data.DataView> expose une collection énumérable d’objets <xref:System.Data.DataRowView>.</span><span class="sxs-lookup"><span data-stu-id="3e98c-103">A <xref:System.Data.DataView> exposes an enumerable collection of <xref:System.Data.DataRowView> objects.</span></span> <span data-ttu-id="3e98c-104">Le **DataRowView** objets exposent des valeurs en tant que tableaux d’objets qui sont indexées par le nom ou la référence ordinale de la colonne dans la table sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="3e98c-104">The **DataRowView** objects expose values as object arrays that are indexed by either the name or the ordinal reference of the column in the underlying table.</span></span> <span data-ttu-id="3e98c-105">Vous pouvez accéder à la <xref:System.Data.DataRow> qui est exposé par le **DataRowView** à l’aide de la <xref:System.Data.DataRowView.Row%2A> propriété de la **DataRowView**.</span><span class="sxs-lookup"><span data-stu-id="3e98c-105">You can access the <xref:System.Data.DataRow> that is exposed by the **DataRowView** by using the <xref:System.Data.DataRowView.Row%2A> property of the **DataRowView**.</span></span>  
  
 <span data-ttu-id="3e98c-106">Lorsque vous affichez des valeurs à l’aide un **DataRowView**, le <xref:System.Data.DataView.RowStateFilter%2A> propriété de la **DataView** détermine la version de ligne de sous-jacent **DataRow** est exposé.</span><span class="sxs-lookup"><span data-stu-id="3e98c-106">When you view values by using a **DataRowView**, the <xref:System.Data.DataView.RowStateFilter%2A> property of the **DataView** determines which row version of the underlying **DataRow** is exposed.</span></span> <span data-ttu-id="3e98c-107">Pour plus d’informations sur différentes versions de ligne à l’aide de l’accès à un **DataRow**, consultez [États des lignes et des Versions de ligne](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/row-states-and-row-versions.md).</span><span class="sxs-lookup"><span data-stu-id="3e98c-107">For information about accessing different row versions using a **DataRow**, see [Row States and Row Versions](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/row-states-and-row-versions.md).</span></span>  
  
 <span data-ttu-id="3e98c-108">L'exemple de code suivant affiche toutes les valeurs actuelles et d'origine d'une table.</span><span class="sxs-lookup"><span data-stu-id="3e98c-108">The following code example displays all the current and original values in a table.</span></span>  
  
```vb  
Dim catView As DataView = New DataView(catDS.Tables("Categories"))  
Console.WriteLine("Current Values:")  
WriteView(catView)  
Console.WriteLine("Original Values:")  
catView.RowStateFilter = DataViewRowState.ModifiedOriginal  
WriteView(catView)      
  
Public Shared Sub WriteView(thisDataView As DataView)  
  Dim rowView As DataRowView  
  Dim i As Integer  
  
  For Each rowView In thisDataView  
    For i = 0 To thisDataView.Table.Columns.Count - 1  
      Console.Write(rowView(i) & vbTab)  
    Next  
    Console.WriteLine()  
  Next  
End Sub  
```  
  
```csharp  
DataView catView = new DataView(catDS.Tables["Categories"]);  
Console.WriteLine("Current Values:");  
WriteView(catView);  
Console.WriteLine("Original Values:");  
catView.RowStateFilter = DataViewRowState.ModifiedOriginal;  
WriteView(catView);  
  
public static void WriteView(DataView thisDataView)  
{  
  foreach (DataRowView rowView in thisDataView)  
  {  
    for (int i = 0; i < thisDataView.Table.Columns.Count; i++)  
      Console.Write(rowView[i] + "\t");  
    Console.WriteLine();  
  }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="3e98c-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e98c-109">See also</span></span>

- <xref:System.Data.DataRowVersion>
- <xref:System.Data.DataViewRowState>
- <xref:System.Data.DataView>
- <xref:System.Data.DataRowView>
- [<span data-ttu-id="3e98c-110">DataViews</span><span class="sxs-lookup"><span data-stu-id="3e98c-110">DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/dataviews.md)
- [<span data-ttu-id="3e98c-111">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="3e98c-111">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
