---
title: AcceptChanges et RejectChanges
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e2d1a6fe-31f9-4b83-9728-06c406a3394e
ms.openlocfilehash: 65e47bafda3e3e47241405c9c8b8e3b4b0055601
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="acceptchanges-and-rejectchanges"></a><span data-ttu-id="df90b-102">AcceptChanges et RejectChanges</span><span class="sxs-lookup"><span data-stu-id="df90b-102">AcceptChanges and RejectChanges</span></span>
<span data-ttu-id="df90b-103">Après avoir vérifié l’exactitude des modifications apportées aux données dans un <xref:System.Data.DataTable>, vous pouvez accepter les modifications apportées à l’aide de la <xref:System.Data.DataRow.AcceptChanges%2A> méthode de la <xref:System.Data.DataRow>, <xref:System.Data.DataTable>, ou <xref:System.Data.DataSet>, qui définit le **actuel** ligne valeurs de la **d’origine** valeurs et fait passer le **RowState** propriété **Unchanged**.</span><span class="sxs-lookup"><span data-stu-id="df90b-103">After verifying the accuracy of changes made to data in a <xref:System.Data.DataTable>, you can accept the changes using the <xref:System.Data.DataRow.AcceptChanges%2A> method of the <xref:System.Data.DataRow>, <xref:System.Data.DataTable>, or <xref:System.Data.DataSet>, which will set the **Current** row values to be the **Original** values and will set the **RowState** property to **Unchanged**.</span></span> <span data-ttu-id="df90b-104">Acceptation ou rejet des modifications supprime toutes les **RowError** informations et définit les **HasErrors** propriété **false**.</span><span class="sxs-lookup"><span data-stu-id="df90b-104">Accepting or rejecting changes clears out any **RowError** information and sets the **HasErrors** property to **false**.</span></span> <span data-ttu-id="df90b-105">L'acceptation ou le rejet des modifications peut également affecter la mise à jour des données dans la source de données.</span><span class="sxs-lookup"><span data-stu-id="df90b-105">Accepting or rejecting changes can also affect updating data in the data source.</span></span> <span data-ttu-id="df90b-106">Pour plus d’informations, consultez [mise à jour des Sources de données avec DataAdapters](../../../../../docs/framework/data/adonet/updating-data-sources-with-dataadapters.md).</span><span class="sxs-lookup"><span data-stu-id="df90b-106">For more information, see [Updating Data Sources with DataAdapters](../../../../../docs/framework/data/adonet/updating-data-sources-with-dataadapters.md).</span></span>  
  
 <span data-ttu-id="df90b-107">Si les contraintes de clé étrangères existent sur le **DataTable**, modifications acceptées ou rejetées à l’aide de **AcceptChanges** et **RejectChanges** sont propagées aux lignes enfants de la  **DataRow** conformément à la **ForeignKeyConstraint.AcceptRejectRule**.</span><span class="sxs-lookup"><span data-stu-id="df90b-107">If foreign key constraints exist on the **DataTable**, changes accepted or rejected using **AcceptChanges** and **RejectChanges** are propagated to child rows of the **DataRow** according to the **ForeignKeyConstraint.AcceptRejectRule**.</span></span> <span data-ttu-id="df90b-108">Pour plus d’informations, consultez [contraintes DataTable](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatable-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="df90b-108">For more information, see [DataTable Constraints](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatable-constraints.md).</span></span>  
  
 <span data-ttu-id="df90b-109">L'exemple suivant vérifie les lignes ayant des erreurs, résout, le cas échéant, les erreurs et rejette les lignes dans lesquelles les erreurs ne peuvent pas être résolues.</span><span class="sxs-lookup"><span data-stu-id="df90b-109">The following example checks for rows with errors, resolves the errors where applicable, and rejects the rows where the error cannot be resolved.</span></span> <span data-ttu-id="df90b-110">Notez que, pour les erreurs résolues, le **RowError** valeur est réinitialisée à une chaîne vide, provoquant la **HasErrors** propriété à définir **false**.</span><span class="sxs-lookup"><span data-stu-id="df90b-110">Note that, for resolved errors, the **RowError** value is reset to an empty string, causing the **HasErrors** property to be set to **false**.</span></span> <span data-ttu-id="df90b-111">Lorsque toutes les lignes avec des erreurs ont été résolues ou rejetées, **AcceptChanges** est appelée pour accepter toutes les modifications pour l’intégralité de **DataTable**.</span><span class="sxs-lookup"><span data-stu-id="df90b-111">When all the rows with errors have been resolved or rejected, **AcceptChanges** is called to accept all changes for the entire **DataTable**.</span></span>  
  
```vb  
If workTable.HasErrors Then  
  Dim errRow As DataRow  
  
  For Each errRow in workTable.GetErrors()  
  
    If errRow.RowError = "Total cannot exceed 1000." Then  
      errRow("Total") = 1000  
      errRow.RowError = ""    ' Clear the error.  
    Else  
      errRow.RejectChanges()  
    End If  
  Next  
End If  
  
workTable.AcceptChanges()  
```  
  
```csharp  
if (workTable.HasErrors)  
{  
  
  foreach (DataRow errRow in workTable.GetErrors())  
  {  
    if (errRow.RowError == "Total cannot exceed 1000.")  
    {  
      errRow["Total"] = 1000;  
      errRow.RowError = "";    // Clear the error.  
    }  
    else  
      errRow.RejectChanges();  
  }  
}  
  
workTable.AcceptChanges();  
```  
  
## <a name="see-also"></a><span data-ttu-id="df90b-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df90b-112">See Also</span></span>  
 <xref:System.Data.DataRow>  
 <xref:System.Data.DataSet>  
 <xref:System.Data.DataTable>  
 [<span data-ttu-id="df90b-113">Manipulation des données dans un DataTable</span><span class="sxs-lookup"><span data-stu-id="df90b-113">Manipulating Data in a DataTable</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/manipulating-data-in-a-datatable.md)  
 [<span data-ttu-id="df90b-114">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="df90b-114">ADO.NET Managed Providers and DataSet Developer Center</span></span>](http://go.microsoft.com/fwlink/?LinkId=217917)
