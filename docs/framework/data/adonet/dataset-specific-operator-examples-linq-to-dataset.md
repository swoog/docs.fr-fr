---
title: Exemples d'opérateurs spécifiques aux DataSets (LINQ to DataSet)
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8fdd64af-6ad0-46cd-91c8-dbe26620eeb1
ms.openlocfilehash: 27a48b7ffe5466c52f19f15cf3c1a6cb558028b2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59097334"
---
# <a name="dataset-specific-operator-examples-linq-to-dataset"></a><span data-ttu-id="6d3fc-102">Exemples d'opérateurs spécifiques aux DataSets (LINQ to DataSet)</span><span class="sxs-lookup"><span data-stu-id="6d3fc-102">DataSet-Specific Operator Examples (LINQ to DataSet)</span></span>
<span data-ttu-id="6d3fc-103">Les exemples de cette rubrique montrent comment utiliser la méthode <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> et la classe <xref:System.Data.DataRowComparer>.</span><span class="sxs-lookup"><span data-stu-id="6d3fc-103">The examples in this topic demonstrate how to use the <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> method and the <xref:System.Data.DataRowComparer> class.</span></span>  
  
 <span data-ttu-id="6d3fc-104">Le `FillDataSet` méthode utilisé dans ces exemples est spécifiée dans [chargement des données dans un jeu de données](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md).</span><span class="sxs-lookup"><span data-stu-id="6d3fc-104">The `FillDataSet` method used in these examples is specified in [Loading Data Into a DataSet](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md).</span></span>  
  
 <span data-ttu-id="6d3fc-105">Les exemples de cette rubrique utilisent les tables Contact, Address, Product, SalesOrderHeader et SalesOrderDetail de l'exemple de base de données AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="6d3fc-105">The examples in this topic use the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="6d3fc-106">Les exemples de cette rubrique utilisent les éléments suivants `using` / `Imports` instructions :</span><span class="sxs-lookup"><span data-stu-id="6d3fc-106">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#importsusing)]  
  
 <span data-ttu-id="6d3fc-107">Pour plus d'informations, voir [Procédure : Créer un projet LINQ to DataSet dans Visual Studio](../../../../docs/framework/data/adonet/how-to-create-a-linq-to-dataset-project-in-vs.md).</span><span class="sxs-lookup"><span data-stu-id="6d3fc-107">For more information, see [How to: Create a LINQ to DataSet Project In Visual Studio](../../../../docs/framework/data/adonet/how-to-create-a-linq-to-dataset-project-in-vs.md).</span></span>  
  
## <a name="copytodatatable"></a><span data-ttu-id="6d3fc-108">CopyToDataTable</span><span class="sxs-lookup"><span data-stu-id="6d3fc-108">CopyToDataTable</span></span>  
  
### <a name="example"></a><span data-ttu-id="6d3fc-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="6d3fc-109">Example</span></span>  
 <span data-ttu-id="6d3fc-110">Cet exemple montre comment charger un <xref:System.Data.DataTable> avec les résultats de la requête à l'aide de la méthode <xref:System.Data.DataTableExtensions.CopyToDataTable%2A>.</span><span class="sxs-lookup"><span data-stu-id="6d3fc-110">This example loads a <xref:System.Data.DataTable> with query results by using the <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> method.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#LoadDataTableWithQueryResults](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#loaddatatablewithqueryresults)]
 [!code-vb[DP LINQ to DataSet Examples#LoadDataTableWithQueryResults](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#loaddatatablewithqueryresults)]  
  
## <a name="datarowcomparer"></a><span data-ttu-id="6d3fc-111">DataRowComparer</span><span class="sxs-lookup"><span data-stu-id="6d3fc-111">DataRowComparer</span></span>  
  
### <a name="example"></a><span data-ttu-id="6d3fc-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="6d3fc-112">Example</span></span>  
 <span data-ttu-id="6d3fc-113">Cet exemple montre comment comparer deux lignes de données différentes à l'aide de <xref:System.Data.DataRowComparer>.</span><span class="sxs-lookup"><span data-stu-id="6d3fc-113">This example compares two different data rows by using <xref:System.Data.DataRowComparer>.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#CompareDifferentDataRows](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#comparedifferentdatarows)]  
  
## <a name="see-also"></a><span data-ttu-id="6d3fc-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d3fc-114">See also</span></span>

- [<span data-ttu-id="6d3fc-115">Chargement de données dans un DataSet</span><span class="sxs-lookup"><span data-stu-id="6d3fc-115">Loading Data Into a DataSet</span></span>](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)
- [<span data-ttu-id="6d3fc-116">Exemples LINQ to DataSet</span><span class="sxs-lookup"><span data-stu-id="6d3fc-116">LINQ to DataSet Examples</span></span>](../../../../docs/framework/data/adonet/linq-to-dataset-examples.md)
