---
title: Création de colonnes AutoIncrement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: cf09732a-ab54-4d98-89e2-4d0a1f28fbce
ms.openlocfilehash: 9c6b5393e1928828bca001ba1d2336f09e64c22c
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43536613"
---
# <a name="creating-autoincrement-columns"></a><span data-ttu-id="558c6-102">Création de colonnes AutoIncrement</span><span class="sxs-lookup"><span data-stu-id="558c6-102">Creating AutoIncrement Columns</span></span>
<span data-ttu-id="558c6-103">Pour garantir que les valeurs de colonne sont uniques, vous pouvez les définir de sorte qu'elles s'incrémentent automatiquement lors de l'ajout de lignes à la table.</span><span class="sxs-lookup"><span data-stu-id="558c6-103">To ensure unique column values, you can set the column values to increment automatically when new rows are added to the table.</span></span> <span data-ttu-id="558c6-104">Pour créer un auto-incrémentée <xref:System.Data.DataColumn>, définissez le <xref:System.Data.DataColumn.AutoIncrement%2A> propriété de la colonne à **true**.</span><span class="sxs-lookup"><span data-stu-id="558c6-104">To create an auto-incrementing <xref:System.Data.DataColumn>, set the <xref:System.Data.DataColumn.AutoIncrement%2A> property of the column to **true**.</span></span> <span data-ttu-id="558c6-105">Le <xref:System.Data.DataColumn> commence alors avec la valeur définie dans le <xref:System.Data.DataColumn.AutoIncrementSeed%2A> propriété et à chaque ligne ajoutée à la valeur de la **AutoIncrement** colonne augmente la valeur définie dans le <xref:System.Data.DataColumn.AutoIncrementStep%2A> propriété de la colonne.</span><span class="sxs-lookup"><span data-stu-id="558c6-105">The <xref:System.Data.DataColumn> then starts with the value defined in the <xref:System.Data.DataColumn.AutoIncrementSeed%2A> property, and with each row added the value of the **AutoIncrement** column increases by the value defined in the <xref:System.Data.DataColumn.AutoIncrementStep%2A> property of the column.</span></span>  
  
 <span data-ttu-id="558c6-106">Pour **AutoIncrement** colonnes, il est recommandé que le <xref:System.Data.DataColumn.ReadOnly%2A> propriété de la **DataColumn** être définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="558c6-106">For **AutoIncrement** columns, we recommend that the <xref:System.Data.DataColumn.ReadOnly%2A> property of the **DataColumn** be set to **true**.</span></span>  
  
 <span data-ttu-id="558c6-107">L'exemple suivant montre comment créer une colonne commençant par la valeur 200, avec une incrémentation par pas de 3.</span><span class="sxs-lookup"><span data-stu-id="558c6-107">The following example demonstrates how to create a column that starts with a value of 200 and adds incrementally in steps of 3.</span></span>  
  
```vb  
Dim workColumn As DataColumn = workTable.Columns.Add( _  
    "CustomerID", typeof(Int32))  
workColumn.AutoIncrement = true  
workColumn.AutoIncrementSeed = 200  
workColumn.AutoIncrementStep = 3  
```  
  
```csharp  
DataColumn workColumn = workTable.Columns.Add(  
    "CustomerID", typeof(Int32));  
workColumn.AutoIncrement = true;  
workColumn.AutoIncrementSeed = 200;  
workColumn.AutoIncrementStep = 3;  
```  
  
## <a name="see-also"></a><span data-ttu-id="558c6-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="558c6-108">See Also</span></span>  
 <xref:System.Data.DataColumn>  
 [<span data-ttu-id="558c6-109">Définition de schéma de DataTable</span><span class="sxs-lookup"><span data-stu-id="558c6-109">DataTable Schema Definition</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatable-schema-definition.md)  
 [<span data-ttu-id="558c6-110">DataTables</span><span class="sxs-lookup"><span data-stu-id="558c6-110">DataTables</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatables.md)  
 [<span data-ttu-id="558c6-111">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="558c6-111">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
