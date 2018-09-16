---
title: Création d'un DataView
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: b1cc02d1-23b1-4439-a998-0da1899f3442
ms.openlocfilehash: b88df66ef2e065d1db8d4033eb1fb0e47ebdd189
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45677511"
---
# <a name="creating-a-dataview"></a><span data-ttu-id="a666b-102">Création d'un DataView</span><span class="sxs-lookup"><span data-stu-id="a666b-102">Creating a DataView</span></span>
<span data-ttu-id="a666b-103">Il existe deux façons de créer un objet <xref:System.Data.DataView>.</span><span class="sxs-lookup"><span data-stu-id="a666b-103">There are two ways to create a <xref:System.Data.DataView>.</span></span> <span data-ttu-id="a666b-104">Vous pouvez utiliser la **DataView** constructeur, ou vous pouvez créer une référence à la <xref:System.Data.DataTable.DefaultView%2A> propriété de la <xref:System.Data.DataTable>.</span><span class="sxs-lookup"><span data-stu-id="a666b-104">You can use the **DataView** constructor, or you can create a reference to the <xref:System.Data.DataTable.DefaultView%2A> property of the <xref:System.Data.DataTable>.</span></span> <span data-ttu-id="a666b-105">Le **DataView** constructeur ne peut être vide ou il peut prendre l’une un **DataTable** comme un argument unique, ou un **DataTable** , ainsi que les critères de filtre, des critères de tri et une ligne filtre d’état.</span><span class="sxs-lookup"><span data-stu-id="a666b-105">The **DataView** constructor can be empty, or it can take either a **DataTable** as a single argument, or a **DataTable** along with filter criteria, sort criteria, and a row state filter.</span></span> <span data-ttu-id="a666b-106">Pour plus d’informations sur les arguments supplémentaires disponibles pour une utilisation avec le **DataView**, consultez [de tri et filtrage des données](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/sorting-and-filtering-data.md).</span><span class="sxs-lookup"><span data-stu-id="a666b-106">For more information about the additional arguments available for use with the **DataView**, see [Sorting and Filtering Data](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/sorting-and-filtering-data.md).</span></span>  
  
 <span data-ttu-id="a666b-107">Étant donné que l’index pour une **DataView** est intégrée à la fois lors la **DataView** est créé et lorsqu’une de la **tri**, **RowFilter**, ou  **RowStateFilter** propriétés sont modifiées, vous obtiendrez de meilleures performances en fournissant n’importe quel ordre de tri initial ou en filtrant les critères en tant qu’arguments de constructeur lorsque vous créez le **DataView**.</span><span class="sxs-lookup"><span data-stu-id="a666b-107">Because the index for a **DataView** is built both when the **DataView** is created, and when any of the **Sort**, **RowFilter**, or **RowStateFilter** properties are modified, you achieve best performance by supplying any initial sort order or filtering criteria as constructor arguments when you create the **DataView**.</span></span> <span data-ttu-id="a666b-108">Création d’un **DataView** sans spécification de critères de tri ou de filtre, puis en définissant le **tri**, **RowFilter**, ou **RowStateFilter** propriétés provoque ultérieurement l’index doit être générée au moins deux fois : une fois lors de la **DataView** est créé, et à nouveau lorsque toutes les propriétés de tri ou de filtre sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="a666b-108">Creating a **DataView** without specifying sort or filter criteria and then setting the **Sort**, **RowFilter**, or **RowStateFilter** properties later causes the index to be built at least twice: once when the **DataView** is created, and again when any of the sort or filter properties are modified.</span></span>  
  
 <span data-ttu-id="a666b-109">Notez que si vous créez un **DataView** à l’aide du constructeur qui n’accepte pas d’arguments, vous serez pas en mesure d’utiliser le **DataView** jusqu'à ce que vous avez défini le **Table** propriété .</span><span class="sxs-lookup"><span data-stu-id="a666b-109">Note that if you create a **DataView** using the constructor that does not take any arguments, you will not be able to use the **DataView** until you have set the **Table** property.</span></span>  
  
 <span data-ttu-id="a666b-110">L’exemple de code suivant montre comment créer un **DataView** à l’aide de la **DataView** constructeur.</span><span class="sxs-lookup"><span data-stu-id="a666b-110">The following code example demonstrates how to create a **DataView** using the **DataView** constructor.</span></span> <span data-ttu-id="a666b-111">Un **RowFilter**, **tri** colonne, et **DataViewRowState** sont fournis avec le **DataTable**.</span><span class="sxs-lookup"><span data-stu-id="a666b-111">A **RowFilter**, **Sort** column, and **DataViewRowState** are supplied along with the **DataTable**.</span></span>  
  
```vb  
Dim custDV As DataView = New DataView(custDS.Tables("Customers"), _  
    "Country = 'USA'", _  
    "ContactName", _  
    DataViewRowState.CurrentRows)  
```  
  
```csharp  
DataView custDV = new DataView(custDS.Tables["Customers"],   
    "Country = 'USA'",   
    "ContactName",   
    DataViewRowState.CurrentRows);  
```  
  
 <span data-ttu-id="a666b-112">L’exemple de code suivant montre comment obtenir une référence à la valeur par défaut **DataView** d’un **DataTable** à l’aide de la **DefaultView** propriété de la table.</span><span class="sxs-lookup"><span data-stu-id="a666b-112">The following code example demonstrates how to obtain a reference to the default **DataView** of a **DataTable** using the **DefaultView** property of the table.</span></span>  
  
```vb  
Dim custDV As DataView = custDS.Tables("Customers").DefaultView  
```  
  
```csharp  
DataView custDV = custDS.Tables["Customers"].DefaultView;  
```  
  
## <a name="see-also"></a><span data-ttu-id="a666b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a666b-113">See Also</span></span>  
 <xref:System.Data.DataTable>  
 <xref:System.Data.DataView>  
 [<span data-ttu-id="a666b-114">DataViews</span><span class="sxs-lookup"><span data-stu-id="a666b-114">DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/dataviews.md)  
 [<span data-ttu-id="a666b-115">Tri et filtre de données</span><span class="sxs-lookup"><span data-stu-id="a666b-115">Sorting and Filtering Data</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/sorting-and-filtering-data.md)  
 [<span data-ttu-id="a666b-116">DataTables</span><span class="sxs-lookup"><span data-stu-id="a666b-116">DataTables</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatables.md)  
 [<span data-ttu-id="a666b-117">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="a666b-117">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
