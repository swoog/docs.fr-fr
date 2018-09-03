---
title: Affichage des données dans un DataTable
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1d26e0fb-f6e0-4afa-9a9c-b8d55b8f20dc
ms.openlocfilehash: de745633060dd4f7b1610492d0ff57ec7a4f545b
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43478089"
---
# <a name="viewing-data-in-a-datatable"></a>Affichage des données dans un DataTable
Vous pouvez accéder au contenu d’un <xref:System.Data.DataTable> à l’aide de la **lignes** et **colonnes** collections de la **DataTable**. Vous pouvez également utiliser le <xref:System.Data.DataTable.Select%2A> méthode pour retourner des sous-ensembles des données dans un **DataTable** en fonction des critères, y compris les critères de recherche, l’ordre de tri et l’état de la ligne. En outre, vous pouvez utiliser la <xref:System.Data.DataRowCollection.Find%2A> méthode de la **DataRowCollection** lors de la recherche pour une ligne particulière à l’aide d’une valeur de clé primaire.  
  
 Le **sélectionnez** méthode de la **DataTable** objet retourne un jeu de <xref:System.Data.DataRow> objets qui correspondent aux critères spécifiés. **Sélectionnez** prend des arguments facultatifs d’une expression de filtre, l’expression de tri, et **DataViewRowState**. L’expression de filtre identifie la ligne à retourner en fonction **DataColumn** valeurs, telles que `LastName = 'Smith'`. L'expression de tri respecte les conventions SQL standard de tri des colonnes, comme `LastName ASC, FirstName ASC`. Pour plus d’informations sur l’écriture d’expressions, consultez la <xref:System.Data.DataColumn.Expression%2A> propriété de la **DataColumn** classe.  
  
> [!TIP]
>  Si vous effectuez un nombre d’appels à la **sélectionnez** méthode d’un **DataTable**, vous pouvez augmenter les performances en créant tout d’abord un <xref:System.Data.DataView> pour le **DataTable**. Création de la **DataView** indexe les lignes de la table. Le **sélectionnez** méthode utilise ensuite cet index, ce qui réduit considérablement le temps de générer le résultat de la requête. Pour plus d’informations sur la création d’un **DataView** pour un **DataTable**, consultez [DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/dataviews.md).  
  
 Le **sélectionnez** méthode détermine quelle version des lignes à afficher ou manipuler selon un <xref:System.Data.DataViewRowState>. Le tableau suivant décrit les possibles **DataViewRowState** valeurs d’énumération.  
  
|Valeur DataViewRowState|Description|  
|----------------------------|-----------------|  
|**CurrentRows**|Les lignes en cours comprennent les lignes non modifiées, les lignes ajoutées et les lignes modifiées.|  
|**Supprimé**|Ligne supprimée.|  
|**ModifiedCurrent**|Une version actuelle, qui est une version modifiée des données d'origine. (Consultez **ModifiedOriginal**.)|  
|**ModifiedOriginal**|La version d'origine de toutes les lignes modifiées. La version actuelle est disponible à l’aide **ModifiedCurrent**.|  
|**Ajouté**|Nouvelle ligne.|  
|**Aucun**|Aucun.|  
|**OriginalRows**|Les lignes d'origine, notamment les lignes non modifiées et les lignes supprimées.|  
|**inchangé**|Ligne non modifiée.|  
  
 Dans l’exemple suivant, le **DataSet** objet est filtré afin que vous travaillez uniquement avec les lignes dont la propriété **DataViewRowState** a la valeur **CurrentRows**.  
  
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
  
 Le **sélectionnez** méthode peut être utilisée pour retourner les lignes avec des différentes **RowState** valeurs ou des valeurs de champ. L’exemple suivant retourne un **DataRow** tableau qui référence toutes les lignes qui ont été supprimés, ainsient qu’un autre **DataRow** tableau qui référence toutes les lignes, classées par **CustLName**, où le **CustID** colonne est supérieure à 5. Pour plus d’informations sur la façon d’afficher les informations contenues dans le **Deleted** de ligne, consultez [États des lignes et des Versions de ligne](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/row-states-and-row-versions.md).  
  
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
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Data.DataRow>  
 <xref:System.Data.DataSet>  
 <xref:System.Data.DataTable>  
 <xref:System.Data.DataViewRowState>  
 [Manipulation des données dans un DataTable](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/manipulating-data-in-a-datatable.md)  
 [États des lignes et versions des lignes](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/row-states-and-row-versions.md)  
 [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
