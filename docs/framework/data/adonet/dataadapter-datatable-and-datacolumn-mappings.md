---
title: Mappages de DataAdapter DataTable et DataColumn
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d023260a-a66a-4c39-b8f4-090cd130e730
ms.openlocfilehash: 9f33ae085bef2b611d1ce95bed1b26f9101a10b9
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43385224"
---
# <a name="dataadapter-datatable-and-datacolumn-mappings"></a>Mappages de DataAdapter DataTable et DataColumn
Un **DataAdapter** contient une collection de zéro ou plusieurs <xref:System.Data.Common.DataTableMapping> objets dans son **TableMappings** propriété. Un **DataTableMapping** fournit un mappage principal entre les données retournées à partir d’une requête sur une source de données et un <xref:System.Data.DataTable>. Le **DataTableMapping** nom peut être passé à la place de la **DataTable** nom pour le **remplir** méthode de la **DataAdapter**. L’exemple suivant crée un **DataTableMapping** nommé **AuthorsMapping** pour le **auteurs** table.  
  
```vb  
workAdapter.TableMappings.Add("AuthorsMapping", "Authors")  
```  
  
```csharp  
workAdapter.TableMappings.Add("AuthorsMapping", "Authors");  
```  
  
 Un **DataTableMapping** vous permet d’utiliser des noms de colonne dans un **DataTable** qui sont différentes de celles figurant dans la base de données. Le **DataAdapter** utilise le mappage pour faire correspondre les colonnes lorsque la table est mise à jour.  
  
 Si vous ne spécifiez pas un **TableName** ou un **DataTableMapping** nom lors de l’appel le **remplir** ou **mise à jour** méthode de la  **DataAdapter**, le **DataAdapter** recherche un **DataTableMapping** nommé « Table ». Si le problème **DataTableMapping** n’existe pas, le **TableName** de la **DataTable** est « Table ». Vous pouvez spécifier une valeur par défaut **DataTableMapping** en créant un **DataTableMapping** par le nom de « Table ».  
  
 L’exemple de code suivant crée un **DataTableMapping** (à partir de la <xref:System.Data.Common> espace de noms) et le rend le mappage par défaut pour le texte spécifié **DataAdapter** en le nommant « Table ». L’exemple mappe ensuite les colonnes de la première table dans le résultat de requête (le **clients** table de la **Northwind** base de données) à un ensemble de noms plus conviviaux dans la **Customers de Northwind**  table dans le <xref:System.Data.DataSet>. Pour les colonnes qui ne sont pas mappées, le nom de la colonne de la source de données est utilisé.  
  
```vb  
Dim mapping As DataTableMapping = _  
  adapter.TableMappings.Add("Table", "NorthwindCustomers")  
mapping.ColumnMappings.Add("CompanyName", "Company")  
mapping.ColumnMappings.Add("ContactName", "Contact")  
mapping.ColumnMappings.Add("PostalCode", "ZIPCode")  
  
adapter.Fill(custDS)  
```  
  
```csharp  
DataTableMapping mapping =   
  adapter.TableMappings.Add("Table", "NorthwindCustomers");  
mapping.ColumnMappings.Add("CompanyName", "Company");  
mapping.ColumnMappings.Add("ContactName", "Contact");  
mapping.ColumnMappings.Add("PostalCode", "ZIPCode");  
  
adapter.Fill(custDS);  
```  
  
 Dans les situations plus évoluées, vous pouvez décider que vous voulez que le même **DataAdapter** pour prendre en charge le chargement de différentes tables avec différents mappages. Pour ce faire, ajoutez simplement d’autres **DataTableMapping** objets.  
  
 Lorsque le **remplir** méthode reçoit une instance d’un **DataSet** et un **DataTableMapping** nom, s’il existe un mappage portant ce nom, il est utilisé ; sinon, un  **DataTable** avec qui le nom est utilisé.  
  
 Les exemples suivants créent un **DataTableMapping** avec un nom de **clients** et un **DataTable** nom de **BizTalkSchema**. L’exemple mappe ensuite les lignes retournées par l’instruction SELECT à la **BizTalkSchema** **DataTable**.  
  
```vb  
Dim mapping As ITableMapping = _  
  adapter.TableMappings.Add("Customers", "BizTalkSchema")  
mapping.ColumnMappings.Add("CustomerID", "ClientID")  
mapping.ColumnMappings.Add("CompanyName", "ClientName")  
mapping.ColumnMappings.Add("ContactName", "Contact")  
mapping.ColumnMappings.Add("PostalCode", "ZIP")  
  
adapter.Fill(custDS, "Customers")  
```  
  
```csharp  
ITableMapping mapping =   
  adapter.TableMappings.Add("Customers", "BizTalkSchema");  
mapping.ColumnMappings.Add("CustomerID", "ClientID");  
mapping.ColumnMappings.Add("CompanyName", "ClientName");  
mapping.ColumnMappings.Add("ContactName", "Contact");  
mapping.ColumnMappings.Add("PostalCode", "ZIP");  
  
adapter.Fill(custDS, "Customers");  
```  
  
> [!NOTE]
>  Si aucun nom de colonne source n'est fourni pour un mappage de colonne ou aucun nom de table source n'est fourni pour un mappage de table, les noms par défaut sont automatiquement générés. Si aucune colonne source n’est fourni pour un mappage de colonnes, le mappage de colonne porte un nom incrémentiel par défaut **SourceColumn** *N,* compter **SourceColumn1**. Si aucun nom de table source n’est fournie pour un mappage de table, le mappage de table porte un nom incrémentiel par défaut **SourceTable** *N*, en commençant par **SourceTable1**.  
  
> [!NOTE]
>  Nous vous recommandons d’éviter la convention d’affectation de noms de **SourceColumn** *N* pour un mappage de colonne, ou **SourceTable** *N* pour une table mappage, car le nom fourni peut entrer en conflit avec un nom de mappage de colonne par défaut existant dans le **ColumnMappingCollection** ou le nom de mappage de table dans le **DataTableMappingCollection** . Si le nom fourni existe déjà, une exception sera levée.  
  
## <a name="handling-multiple-result-sets"></a>Gestion de jeux de résultats multiples  
 Si votre **SelectCommand** retourne plusieurs tables, **remplir** génère automatiquement des noms de table avec des valeurs incrémentielles pour les tables dans le **DataSet**, à compter du spécifié le nom de la table et en continuant sur sous la forme **TableName** *N*, en commençant par **TableName1**. Vous pouvez utiliser les mappages de table pour mapper le nom de table généré automatiquement à un nom que vous souhaitez spécifier pour la table dans le **DataSet**. Par exemple, pour un **SelectCommand** qui retourne deux tables, **clients** et **commandes**, émettre l’appel suivant à **remplir**.  
  
```  
adapter.Fill(customersDataSet, "Customers")  
```  
  
 Deux tables sont créées dans le **DataSet**: **clients** et **Customers1**. Vous pouvez utiliser les mappages de table pour vous assurer que la deuxième table est nommée **commandes** au lieu de **Customers1**. Pour ce faire, mappez la table de source de **Customers1** à la **DataSet** table **commandes**, comme illustré dans l’exemple suivant.  
  
```  
adapter.TableMappings.Add("Customers1", "Orders")  
adapter.Fill(customersDataSet, "Customers")  
```  
  
## <a name="see-also"></a>Voir aussi  
 [DataAdapters et DataReaders](../../../../docs/framework/data/adonet/dataadapters-and-datareaders.md)  
 [Extraction et modification de données dans ADO.NET](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)  
 [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
