---
title: Création de colonnes d'expressions
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 0af3bd64-92a2-4b47-ae62-f5df35f131a6
ms.openlocfilehash: 6e19e4e7cc0ea92e9d93e45c2a50d009e46b78c5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59175498"
---
# <a name="creating-expression-columns"></a><span data-ttu-id="47ee6-102">Création de colonnes d'expressions</span><span class="sxs-lookup"><span data-stu-id="47ee6-102">Creating Expression Columns</span></span>
<span data-ttu-id="47ee6-103">Vous pouvez définir une expression pour une colonne lui permettant de contenir une valeur calculée à partir d'autres valeurs de colonne de la même ligne ou de valeurs de colonne de plusieurs lignes de la table.</span><span class="sxs-lookup"><span data-stu-id="47ee6-103">You can define an expression for a column, enabling it to contain a value calculated from other column values in the same row or from the column values of multiple rows in the table.</span></span> <span data-ttu-id="47ee6-104">Pour définir l'expression à évaluer, utilisez la propriété <xref:System.Data.DataColumn.Expression%2A> de la colonne cible. Utilisez la propriété <xref:System.Data.DataColumn.ColumnName%2A> pour faire référence à d'autres colonnes dans l'expression.</span><span class="sxs-lookup"><span data-stu-id="47ee6-104">To define the expression to be evaluated, use the <xref:System.Data.DataColumn.Expression%2A> property of the target column, and use the <xref:System.Data.DataColumn.ColumnName%2A> property to refer to other columns in the expression.</span></span> <span data-ttu-id="47ee6-105">La propriété <xref:System.Data.DataColumn.DataType%2A> de la colonne d'expression doit être appropriée pour la valeur que l'expression retournera.</span><span class="sxs-lookup"><span data-stu-id="47ee6-105">The <xref:System.Data.DataColumn.DataType%2A> for the expression column must be appropriate for the value that the expression returns.</span></span>  
  
 <span data-ttu-id="47ee6-106">Le tableau suivant énumère différentes utilisations possibles des colonnes d'expression dans une table.</span><span class="sxs-lookup"><span data-stu-id="47ee6-106">The following table lists several possible uses for expression columns in a table.</span></span>  
  
|<span data-ttu-id="47ee6-107">Type d'expression</span><span class="sxs-lookup"><span data-stu-id="47ee6-107">Expression type</span></span>|<span data-ttu-id="47ee6-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="47ee6-108">Example</span></span>|  
|---------------------|-------------|  
|<span data-ttu-id="47ee6-109">Comparaison</span><span class="sxs-lookup"><span data-stu-id="47ee6-109">Comparison</span></span>|<span data-ttu-id="47ee6-110">"Total >= 500"</span><span class="sxs-lookup"><span data-stu-id="47ee6-110">"Total >= 500"</span></span>|  
|<span data-ttu-id="47ee6-111">Calcul</span><span class="sxs-lookup"><span data-stu-id="47ee6-111">Computation</span></span>|<span data-ttu-id="47ee6-112">"UnitPrice \* Quantity"</span><span class="sxs-lookup"><span data-stu-id="47ee6-112">"UnitPrice \* Quantity"</span></span>|  
|<span data-ttu-id="47ee6-113">Agrégation</span><span class="sxs-lookup"><span data-stu-id="47ee6-113">Aggregation</span></span>|<span data-ttu-id="47ee6-114">Sum(Price)</span><span class="sxs-lookup"><span data-stu-id="47ee6-114">Sum(Price)</span></span>|  
  
 <span data-ttu-id="47ee6-115">Vous pouvez définir le **Expression** propriété sur un existant **DataColumn** objet, ou vous pouvez inclure la propriété comme troisième argument passé à la <xref:System.Data.DataColumn> constructeur, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="47ee6-115">You can set the **Expression** property on an existing **DataColumn** object, or you can include the property as the third argument passed to the <xref:System.Data.DataColumn> constructor, as shown in the following example.</span></span>  
  
```vb  
workTable.Columns.Add("Total",Type.GetType("System.Double"))  
workTable.Columns.Add("SalesTax", Type.GetType("System.Double"), _  
  "Total * 0.086")  
```  
  
```csharp  
workTable.Columns.Add("Total", typeof(Double));  
workTable.Columns.Add("SalesTax", typeof(Double), "Total * 0.086");  
```  
  
 <span data-ttu-id="47ee6-116">Les expressions peuvent faire référence à d'autres colonnes d'expression ; cependant, une référence circulaire, dans laquelle deux expressions se référencent mutuellement, générera une exception.</span><span class="sxs-lookup"><span data-stu-id="47ee6-116">Expressions can reference other expression columns; however, a circular reference, in which two expressions reference each other, will generate an exception.</span></span> <span data-ttu-id="47ee6-117">Pour plus d’informations sur l’écriture d’expressions, consultez la <xref:System.Data.DataColumn.Expression%2A> propriété de la **DataColumn** classe.</span><span class="sxs-lookup"><span data-stu-id="47ee6-117">For rules about writing expressions, see the <xref:System.Data.DataColumn.Expression%2A> property of the **DataColumn** class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="47ee6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47ee6-118">See also</span></span>

- <xref:System.Data.DataColumn>
- <xref:System.Data.DataSet>
- <xref:System.Data.DataTable>
- [<span data-ttu-id="47ee6-119">Définition de schéma de DataTable</span><span class="sxs-lookup"><span data-stu-id="47ee6-119">DataTable Schema Definition</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatable-schema-definition.md)
- [<span data-ttu-id="47ee6-120">DataTables</span><span class="sxs-lookup"><span data-stu-id="47ee6-120">DataTables</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatables.md)
- [<span data-ttu-id="47ee6-121">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="47ee6-121">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
