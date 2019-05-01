---
title: Ajout de données à un DataTable
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d6aa8474-7bde-48f7-949d-20dc38a1625b
ms.openlocfilehash: ec4ad84a39afe21ef77507732e5e0e417d45f3e7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62034521"
---
# <a name="adding-data-to-a-datatable"></a><span data-ttu-id="71479-102">Ajout de données à un DataTable</span><span class="sxs-lookup"><span data-stu-id="71479-102">Adding Data to a DataTable</span></span>
<span data-ttu-id="71479-103">Après avoir créé un objet <xref:System.Data.DataTable> et défini sa structure à l'aide de colonnes et de contraintes, vous pouvez ajouter de nouvelles lignes de données à la table.</span><span class="sxs-lookup"><span data-stu-id="71479-103">After you create a <xref:System.Data.DataTable> and define its structure using columns and constraints, you can add new rows of data to the table.</span></span> <span data-ttu-id="71479-104">Pour ajouter une nouvelle ligne, déclarez une nouvelle variable comme type <xref:System.Data.DataRow>.</span><span class="sxs-lookup"><span data-stu-id="71479-104">To add a new row, declare a new variable as type <xref:System.Data.DataRow>.</span></span> <span data-ttu-id="71479-105">Un nouveau **DataRow** est retourné lorsque vous appelez le <xref:System.Data.DataTable.NewRow%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="71479-105">A new **DataRow** object is returned when you call the <xref:System.Data.DataTable.NewRow%2A> method.</span></span> <span data-ttu-id="71479-106">Le **DataTable** crée ensuite le **DataRow** objet basé sur la structure de la table, tel que défini par le <xref:System.Data.DataColumnCollection>.</span><span class="sxs-lookup"><span data-stu-id="71479-106">The **DataTable** then creates the **DataRow** object based on the structure of the table, as defined by the <xref:System.Data.DataColumnCollection>.</span></span>  
  
 <span data-ttu-id="71479-107">L’exemple suivant montre comment créer une nouvelle ligne en appelant le **NewRow** (méthode).</span><span class="sxs-lookup"><span data-stu-id="71479-107">The following example demonstrates how to create a new row by calling the **NewRow** method.</span></span>  
  
```vb  
Dim workRow As DataRow = workTable.NewRow()  
```  
  
```csharp  
DataRow workRow = workTable.NewRow();  
```  
  
 <span data-ttu-id="71479-108">Vous pouvez ensuite manipuler la ligne ajoutée en utilisant un index ou le nom de colonne, comme le montre l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="71479-108">You then can manipulate the newly added row using an index or the column name, as shown in the following example.</span></span>  
  
```vb  
workRow("CustLName") = "Smith"  
workRow(1) = "Smith"  
```  
  
```csharp  
workRow["CustLName"] = "Smith";  
workRow[1] = "Smith";  
```  
  
 <span data-ttu-id="71479-109">Une fois que les données sont insérées dans la nouvelle ligne, le **ajouter** méthode est utilisée pour ajouter la ligne à la <xref:System.Data.DataRowCollection>, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="71479-109">After data is inserted into the new row, the **Add** method is used to add the row to the <xref:System.Data.DataRowCollection>, shown in the following code.</span></span>  
  
```vb  
workTable.Rows.Add(workRow)  
```  
  
```csharp  
workTable.Rows.Add(workRow);  
```  
  
 <span data-ttu-id="71479-110">Vous pouvez également appeler le **ajouter** méthode pour ajouter une nouvelle ligne en passant un tableau de valeurs, typé en tant que <xref:System.Object>, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="71479-110">You can also call the **Add** method to add a new row by passing in an array of values, typed as <xref:System.Object>, as shown in the following example.</span></span>  
  
```vb  
workTable.Rows.Add(new Object() {1, "Smith"})  
```  
  
```csharp  
workTable.Rows.Add(new Object[] {1, "Smith"});  
```  
  
 <span data-ttu-id="71479-111">En passant un tableau de valeurs, typé en tant que **objet**, à la **ajouter** méthode crée une nouvelle ligne à l’intérieur de la table et définit ses valeurs de colonne pour les valeurs dans le tableau d’objets.</span><span class="sxs-lookup"><span data-stu-id="71479-111">Passing an array of values, typed as **Object**, to the **Add** method creates a new row inside the table and sets its column values to the values in the object array.</span></span> <span data-ttu-id="71479-112">Notez que les valeurs du tableau correspondent de façon séquentielle aux colonnes, en fonction de leur ordre d'apparition dans la table.</span><span class="sxs-lookup"><span data-stu-id="71479-112">Note that values in the array are matched sequentially to the columns, based on the order in which they appear in the table.</span></span>  
  
 <span data-ttu-id="71479-113">L’exemple suivant ajoute 10 lignes à la nouvelle **clients** table.</span><span class="sxs-lookup"><span data-stu-id="71479-113">The following example adds 10 rows to the newly created **Customers** table.</span></span>  
  
```vb  
Dim workRow As DataRow  
Dim i As Integer  
  
For i = 0 To 9  
  workRow = workTable.NewRow()  
  workRow(0) = i  
  workRow(1) = "CustName" & I.ToString()  
  workTable.Rows.Add(workRow)  
Next  
```  
  
```csharp  
DataRow workRow;  
  
for (int i = 0; i <= 9; i++)   
{  
  workRow = workTable.NewRow();  
  workRow[0] = i;  
  workRow[1] = "CustName" + i.ToString();  
  workTable.Rows.Add(workRow);  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="71479-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71479-114">See also</span></span>

- <xref:System.Data.DataColumnCollection>
- <xref:System.Data.DataRow>
- <xref:System.Data.DataRowCollection>
- <xref:System.Data.DataTable>
- [<span data-ttu-id="71479-115">Manipulation des données dans un DataTable</span><span class="sxs-lookup"><span data-stu-id="71479-115">Manipulating Data in a DataTable</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/manipulating-data-in-a-datatable.md)
- [<span data-ttu-id="71479-116">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="71479-116">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
