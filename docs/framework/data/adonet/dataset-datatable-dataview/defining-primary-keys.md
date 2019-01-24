---
title: Définition des clés primaires
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 2ea85959-e763-4669-8bd9-46a9dab894bd
ms.openlocfilehash: 3b9e8835c50ea6c1795fc33aa46bac51cd77defc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54650598"
---
# <a name="defining-primary-keys"></a><span data-ttu-id="e137a-102">Définition des clés primaires</span><span class="sxs-lookup"><span data-stu-id="e137a-102">Defining Primary Keys</span></span>
<span data-ttu-id="e137a-103">Une table de base de données a généralement une colonne ou un groupe de colonnes identifiant de façon unique chaque ligne de la table.</span><span class="sxs-lookup"><span data-stu-id="e137a-103">A database table commonly has a column or group of columns that uniquely identifies each row in the table.</span></span> <span data-ttu-id="e137a-104">Cette colonne ou ce groupe de colonnes d'identification s'appelle la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="e137a-104">This identifying column or group of columns is called the primary key.</span></span>  
  
 <span data-ttu-id="e137a-105">Lorsque vous identifiez un seul <xref:System.Data.DataColumn> en tant que le <xref:System.Data.DataTable.PrimaryKey%2A> pour un <xref:System.Data.DataTable>, la table attribue automatiquement la <xref:System.Data.DataColumn.AllowDBNull%2A> propriété de la colonne à **false** et <xref:System.Data.DataColumn.Unique%2A> propriété  **true**.</span><span class="sxs-lookup"><span data-stu-id="e137a-105">When you identify a single <xref:System.Data.DataColumn> as the <xref:System.Data.DataTable.PrimaryKey%2A> for a <xref:System.Data.DataTable>, the table automatically sets the <xref:System.Data.DataColumn.AllowDBNull%2A> property of the column to **false** and the <xref:System.Data.DataColumn.Unique%2A> property to **true**.</span></span> <span data-ttu-id="e137a-106">Pour plusieurs colonnes les clés primaires, uniquement le **AllowDBNull** propriété est automatiquement définie sur **false**.</span><span class="sxs-lookup"><span data-stu-id="e137a-106">For multiple-column primary keys, only the **AllowDBNull** property is automatically set to **false**.</span></span>  
  
 <span data-ttu-id="e137a-107">Le **PrimaryKey** propriété d’un <xref:System.Data.DataTable> reçoit comme valeur un tableau d’une ou plusieurs **DataColumn** objets, comme indiqué dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="e137a-107">The **PrimaryKey** property of a <xref:System.Data.DataTable> receives as its value an array of one or more **DataColumn** objects, as shown in the following examples.</span></span> <span data-ttu-id="e137a-108">Le premier exemple définit une colonne unique comme clé primaire.</span><span class="sxs-lookup"><span data-stu-id="e137a-108">The first example defines a single column as the primary key.</span></span>  
  
```vb  
workTable.PrimaryKey = New DataColumn() {workTable.Columns("CustID")}  
  
' Or  
  
Dim columns(1) As DataColumn  
columns(0) = workTable.Columns("CustID")  
workTable.PrimaryKey = columns  
```  
  
```csharp  
workTable.PrimaryKey = new DataColumn[] {workTable.Columns["CustID"]};  
  
// Or  
  
DataColumn[] columns = new DataColumn[1];  
columns[0] = workTable.Columns["CustID"];  
workTable.PrimaryKey = columns;  
```  
  
 <span data-ttu-id="e137a-109">L'exemple suivant définit deux colonnes comme clé primaire.</span><span class="sxs-lookup"><span data-stu-id="e137a-109">The following example defines two columns as a primary key.</span></span>  
  
```vb  
workTable.PrimaryKey = New DataColumn() {workTable.Columns("CustLName"), _  
                                         workTable.Columns("CustFName")}  
  
' Or  
  
Dim keyColumn(2) As DataColumn  
keyColumn(0) = workTable.Columns("CustLName")  
keyColumn(1) = workTable.Columns("CustFName")  
workTable.PrimaryKey = keyColumn  
```  
  
```csharp  
workTable.PrimaryKey = new DataColumn[] {workTable.Columns["CustLName"],   
                                         workTable.Columns["CustFName"]};  
  
// Or  
  
DataColumn[] keyColumn = new DataColumn[2];  
keyColumn[0] = workTable.Columns["CustLName"];  
keyColumn[1] = workTable.Columns["CustFName"];  
workTable.PrimaryKey = keyColumn;  
```  
  
## <a name="see-also"></a><span data-ttu-id="e137a-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e137a-110">See also</span></span>
- <xref:System.Data.DataTable>
- [<span data-ttu-id="e137a-111">Définition de schéma de DataTable</span><span class="sxs-lookup"><span data-stu-id="e137a-111">DataTable Schema Definition</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatable-schema-definition.md)
- [<span data-ttu-id="e137a-112">DataTables</span><span class="sxs-lookup"><span data-stu-id="e137a-112">DataTables</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatables.md)
- [<span data-ttu-id="e137a-113">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="e137a-113">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
