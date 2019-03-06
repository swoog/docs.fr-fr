---
title: Affichage des données dans un DataTable
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1d26e0fb-f6e0-4afa-9a9c-b8d55b8f20dc
ms.openlocfilehash: fa8749550e10256ee0623714cc95e03a838655c8
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57364487"
---
# <a name="viewing-data-in-a-datatable"></a><span data-ttu-id="628a3-102">Affichage des données dans un DataTable</span><span class="sxs-lookup"><span data-stu-id="628a3-102">Viewing Data in a DataTable</span></span>

<span data-ttu-id="628a3-103">Vous pouvez accéder au contenu d’un <xref:System.Data.DataTable> à l’aide de la **lignes** et **colonnes** collections de la **DataTable**.</span><span class="sxs-lookup"><span data-stu-id="628a3-103">You can access the contents of a <xref:System.Data.DataTable> by using the **Rows** and **Columns** collections of the **DataTable**.</span></span> <span data-ttu-id="628a3-104">Vous pouvez également utiliser le <xref:System.Data.DataTable.Select%2A> méthode pour retourner des sous-ensembles des données dans un **DataTable** en fonction des critères, y compris les critères de recherche, l’ordre de tri et l’état de la ligne.</span><span class="sxs-lookup"><span data-stu-id="628a3-104">You can also use the <xref:System.Data.DataTable.Select%2A> method to return subsets of the data in a **DataTable** according to criteria including search criteria, sort order, and row state.</span></span> <span data-ttu-id="628a3-105">En outre, vous pouvez utiliser la <xref:System.Data.DataRowCollection.Find%2A> méthode de la **DataRowCollection** lors de la recherche pour une ligne particulière à l’aide d’une valeur de clé primaire.</span><span class="sxs-lookup"><span data-stu-id="628a3-105">Additionally, you can use the <xref:System.Data.DataRowCollection.Find%2A> method of the **DataRowCollection** when searching for a particular row using a primary key value.</span></span>

<span data-ttu-id="628a3-106">Le **sélectionnez** méthode de la **DataTable** objet retourne un jeu de <xref:System.Data.DataRow> objets qui correspondent aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="628a3-106">The **Select** method of the **DataTable** object returns a set of <xref:System.Data.DataRow> objects that match the specified criteria.</span></span> <span data-ttu-id="628a3-107">**Sélectionnez** prend des arguments facultatifs d’une expression de filtre, l’expression de tri, et **DataViewRowState**.</span><span class="sxs-lookup"><span data-stu-id="628a3-107">**Select** takes optional arguments of a filter expression, sort expression, and **DataViewRowState**.</span></span> <span data-ttu-id="628a3-108">L’expression de filtre identifie la ligne à retourner en fonction **DataColumn** valeurs, telles que `LastName = 'Smith'`.</span><span class="sxs-lookup"><span data-stu-id="628a3-108">The filter expression identifies which rows to return based on **DataColumn** values, such as `LastName = 'Smith'`.</span></span> <span data-ttu-id="628a3-109">L'expression de tri respecte les conventions SQL standard de tri des colonnes, comme `LastName ASC, FirstName ASC`.</span><span class="sxs-lookup"><span data-stu-id="628a3-109">The sort expression follows standard SQL conventions for ordering columns, for example `LastName ASC, FirstName ASC`.</span></span> <span data-ttu-id="628a3-110">Pour plus d’informations sur l’écriture d’expressions, consultez la <xref:System.Data.DataColumn.Expression%2A> propriété de la **DataColumn** classe.</span><span class="sxs-lookup"><span data-stu-id="628a3-110">For rules about writing expressions, see the <xref:System.Data.DataColumn.Expression%2A> property of the **DataColumn** class.</span></span>

> [!TIP]
> <span data-ttu-id="628a3-111">Si vous effectuez un nombre d’appels à la **sélectionnez** méthode d’un **DataTable**, vous pouvez augmenter les performances en créant tout d’abord un <xref:System.Data.DataView> pour le **DataTable**.</span><span class="sxs-lookup"><span data-stu-id="628a3-111">If you are performing a number of calls to the **Select** method of a **DataTable**, you can increase performance by first creating a <xref:System.Data.DataView> for the **DataTable**.</span></span> <span data-ttu-id="628a3-112">Création de la **DataView** indexe les lignes de la table.</span><span class="sxs-lookup"><span data-stu-id="628a3-112">Creating the **DataView** indexes the rows of the table.</span></span> <span data-ttu-id="628a3-113">Le **sélectionnez** méthode utilise ensuite cet index, ce qui réduit considérablement le temps de générer le résultat de la requête.</span><span class="sxs-lookup"><span data-stu-id="628a3-113">The **Select** method then uses that index, significantly reducing the time to generate the query result.</span></span> <span data-ttu-id="628a3-114">Pour plus d’informations sur la création d’un **DataView** pour un **DataTable**, consultez [DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/dataviews.md).</span><span class="sxs-lookup"><span data-stu-id="628a3-114">For information about creating a **DataView** for a **DataTable**, see [DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/dataviews.md).</span></span>

<span data-ttu-id="628a3-115">Le **sélectionnez** méthode détermine quelle version des lignes à afficher ou manipuler selon un <xref:System.Data.DataViewRowState>.</span><span class="sxs-lookup"><span data-stu-id="628a3-115">The **Select** method determines which version of the rows to view or manipulate based on a <xref:System.Data.DataViewRowState>.</span></span> <span data-ttu-id="628a3-116">Le tableau suivant décrit les possibles **DataViewRowState** valeurs d’énumération.</span><span class="sxs-lookup"><span data-stu-id="628a3-116">The following table describes the possible **DataViewRowState** enumeration values.</span></span>

|<span data-ttu-id="628a3-117">Valeur DataViewRowState</span><span class="sxs-lookup"><span data-stu-id="628a3-117">DataViewRowState value</span></span>|<span data-ttu-id="628a3-118">Description</span><span class="sxs-lookup"><span data-stu-id="628a3-118">Description</span></span>|
|----------------------------|-----------------|
|<span data-ttu-id="628a3-119">**CurrentRows**</span><span class="sxs-lookup"><span data-stu-id="628a3-119">**CurrentRows**</span></span>|<span data-ttu-id="628a3-120">Les lignes en cours comprennent les lignes non modifiées, les lignes ajoutées et les lignes modifiées.</span><span class="sxs-lookup"><span data-stu-id="628a3-120">Current rows including unchanged, added, and modified rows.</span></span>|
|<span data-ttu-id="628a3-121">**Deleted**</span><span class="sxs-lookup"><span data-stu-id="628a3-121">**Deleted**</span></span>|<span data-ttu-id="628a3-122">Ligne supprimée.</span><span class="sxs-lookup"><span data-stu-id="628a3-122">A deleted row.</span></span>|
|<span data-ttu-id="628a3-123">**ModifiedCurrent**</span><span class="sxs-lookup"><span data-stu-id="628a3-123">**ModifiedCurrent**</span></span>|<span data-ttu-id="628a3-124">Une version actuelle, qui est une version modifiée des données d'origine.</span><span class="sxs-lookup"><span data-stu-id="628a3-124">A current version, which is a modified version of original data.</span></span> <span data-ttu-id="628a3-125">(Consultez **ModifiedOriginal**.)</span><span class="sxs-lookup"><span data-stu-id="628a3-125">(See **ModifiedOriginal**.)</span></span>|
|<span data-ttu-id="628a3-126">**ModifiedOriginal**</span><span class="sxs-lookup"><span data-stu-id="628a3-126">**ModifiedOriginal**</span></span>|<span data-ttu-id="628a3-127">La version d'origine de toutes les lignes modifiées.</span><span class="sxs-lookup"><span data-stu-id="628a3-127">The original version of all modified rows.</span></span> <span data-ttu-id="628a3-128">La version actuelle est disponible à l’aide **ModifiedCurrent**.</span><span class="sxs-lookup"><span data-stu-id="628a3-128">The current version is available using **ModifiedCurrent**.</span></span>|
|<span data-ttu-id="628a3-129">**Added**</span><span class="sxs-lookup"><span data-stu-id="628a3-129">**Added**</span></span>|<span data-ttu-id="628a3-130">Nouvelle ligne.</span><span class="sxs-lookup"><span data-stu-id="628a3-130">A new row.</span></span>|
|<span data-ttu-id="628a3-131">**Aucun**</span><span class="sxs-lookup"><span data-stu-id="628a3-131">**None**</span></span>|<span data-ttu-id="628a3-132">Aucun.</span><span class="sxs-lookup"><span data-stu-id="628a3-132">None.</span></span>|
|<span data-ttu-id="628a3-133">**OriginalRows**</span><span class="sxs-lookup"><span data-stu-id="628a3-133">**OriginalRows**</span></span>|<span data-ttu-id="628a3-134">Les lignes d'origine, notamment les lignes non modifiées et les lignes supprimées.</span><span class="sxs-lookup"><span data-stu-id="628a3-134">Original rows, including unchanged and deleted rows.</span></span>|
|<span data-ttu-id="628a3-135">**inchangé**</span><span class="sxs-lookup"><span data-stu-id="628a3-135">**Unchanged**</span></span>|<span data-ttu-id="628a3-136">Ligne non modifiée.</span><span class="sxs-lookup"><span data-stu-id="628a3-136">An unchanged row.</span></span>|

<span data-ttu-id="628a3-137">Dans l’exemple suivant, le **DataSet** objet est filtré afin que vous travaillez uniquement avec les lignes dont la propriété **DataViewRowState** a la valeur **CurrentRows**.</span><span class="sxs-lookup"><span data-stu-id="628a3-137">In the following example, the **DataSet** object is filtered so that you are only working with rows whose **DataViewRowState** is set to **CurrentRows**.</span></span>

```vb
Dim column As DataColumn
Dim row As DataRow

Dim currentRows() As DataRow = _
    workTable.Select(Nothing, Nothing, DataViewRowState.CurrentRows)

If (currentRows.Length < 1 ) Then
  Console.WriteLine("No Current Rows Found")
Else
  For Each column in workTable.Columns
    Console.Write(vbTab & column.ColumnName)
  Next

  Console.WriteLine(vbTab & "RowState")

  For Each row In currentRows
    For Each column In workTable.Columns
      Console.Write(vbTab & row(column).ToString())
    Next

    Dim rowState As String = _
        System.Enum.GetName(row.RowState.GetType(), row.RowState)
    Console.WriteLine(vbTab & rowState)
  Next
End If
```

```csharp
DataRow[] currentRows = workTable.Select(
    null, null, DataViewRowState.CurrentRows);

if (currentRows.Length < 1 )
  Console.WriteLine("No Current Rows Found");
else
{
  foreach (DataColumn column in workTable.Columns)
    Console.Write("\t{0}", column.ColumnName);

  Console.WriteLine("\tRowState");

  foreach (DataRow row in currentRows)
  {
    foreach (DataColumn column in workTable.Columns)
      Console.Write("\t{0}", row[column]);

    Console.WriteLine("\t" + row.RowState);
  }
}
```

<span data-ttu-id="628a3-138">Le **sélectionnez** méthode peut être utilisée pour retourner les lignes avec des différentes **RowState** valeurs ou des valeurs de champ.</span><span class="sxs-lookup"><span data-stu-id="628a3-138">The **Select** method can be used to return rows with differing **RowState** values or field values.</span></span> <span data-ttu-id="628a3-139">L’exemple suivant retourne un **DataRow** tableau qui référence toutes les lignes qui ont été supprimés, ainsient qu’un autre **DataRow** tableau qui référence toutes les lignes, classées par **CustLName**, où le **CustID** colonne est supérieure à 5.</span><span class="sxs-lookup"><span data-stu-id="628a3-139">The following example returns a **DataRow** array that references all rows that have been deleted, and returns another **DataRow** array that references all rows, ordered by **CustLName**, where the **CustID** column is greater than 5.</span></span> <span data-ttu-id="628a3-140">Pour plus d’informations sur la façon d’afficher les informations contenues dans le **Deleted** de ligne, consultez [États des lignes et des Versions de ligne](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/row-states-and-row-versions.md).</span><span class="sxs-lookup"><span data-stu-id="628a3-140">For information about how to view the information in the **Deleted** row, see [Row States and Row Versions](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/row-states-and-row-versions.md).</span></span>

```vb
' Retrieve all deleted rows.
Dim deletedRows() As DataRow = workTable.Select(Nothing, Nothing, DataViewRowState.Deleted)

' Retrieve rows where CustID > 5, and order by CustLName.
Dim custRows() As DataRow = workTable.Select( _
    "CustID > 5", "CustLName ASC")
```

```csharp
// Retrieve all deleted rows.
DataRow[] deletedRows = workTable.Select(
    null, null, DataViewRowState.Deleted);

// Retrieve rows where CustID > 5, and order by CustLName.
DataRow[] custRows = workTable.Select("CustID > 5", "CustLName ASC");
```

## <a name="see-also"></a><span data-ttu-id="628a3-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="628a3-141">See also</span></span>

- <xref:System.Data.DataRow>
- <xref:System.Data.DataSet>
- <xref:System.Data.DataTable>
- <xref:System.Data.DataViewRowState>
- [<span data-ttu-id="628a3-142">Manipulation des données dans un DataTable</span><span class="sxs-lookup"><span data-stu-id="628a3-142">Manipulating Data in a DataTable</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/manipulating-data-in-a-datatable.md)
- [<span data-ttu-id="628a3-143">États des lignes et versions des lignes</span><span class="sxs-lookup"><span data-stu-id="628a3-143">Row States and Row Versions</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/row-states-and-row-versions.md)
- [<span data-ttu-id="628a3-144">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="628a3-144">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
