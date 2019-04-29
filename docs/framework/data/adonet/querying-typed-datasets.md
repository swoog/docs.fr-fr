---
title: Interrogation de DataSets typés
ms.date: 08/15/2018
dev_langs:
- csharp
- vb
ms.assetid: ad712fa1-2baf-462a-b163-574cce6d376a
ms.openlocfilehash: d956fd5f07c108146d20623bcf811266380c132c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61651738"
---
# <a name="query-typed-datasets"></a>Requête de DataSets typés

Si le schéma de la <xref:System.Data.DataSet> est connu au moment du design application, nous vous recommandons d’utiliser un typé <xref:System.Data.DataSet> lors de l’utilisation de LINQ to DataSet. Typé <xref:System.Data.DataSet> est une classe qui dérive un <xref:System.Data.DataSet>. De ce fait, il hérite de l'ensemble des méthodes, événements et propriétés d'un <xref:System.Data.DataSet>. En outre, typé <xref:System.Data.DataSet> fournit des méthodes fortement typées, propriétés et événements. Cela signifie que vous pouvez accéder à des tables et à des colonnes par leur nom au lieu d’utiliser les méthodes associées à des collections. Cela rend les requêtes plus simples et plus lisibles. Pour plus d’informations, consultez [typés](../../../../docs/framework/data/adonet/dataset-datatable-dataview/typed-datasets.md).

LINQ to DataSet prend également en charge les interrogations sur typé <xref:System.Data.DataSet>. Avec un typé <xref:System.Data.DataSet>, il est inutile d’utiliser le modèle générique <xref:System.Data.DataRowExtensions.Field%2A> méthode ou <xref:System.Data.DataRowExtensions.SetField%2A> méthode pour accéder aux données de colonne. Noms de propriété sont disponibles au moment de la compilation, car les informations de type sont incluses dans le <xref:System.Data.DataSet>. LINQ to DataSet fournit l’accès aux valeurs de colonne avec le type approprié, afin que l’interception des erreurs d’incompatibilité de type lorsque le code est compilé à la place de l’exécution.

Avant de procéder à l’interrogation typé <xref:System.Data.DataSet>, vous devez générer la classe à l’aide de la **Concepteur de DataSet** dans Visual Studio. Pour plus d’informations, consultez [créer et configurer des DataSets](/visualstudio/data-tools/create-and-configure-datasets-in-visual-studio).

## <a name="example"></a>Exemple

L'exemple suivant montre une requête sur un <xref:System.Data.DataSet> typé :

```csharp
var query = from o in orders
            where o.OnlineOrderFlag == true
            select new { o.SalesOrderID,
                         o.OrderDate,
                         o.SalesOrderNumber };

foreach(var order in query)
{
    Console.WriteLine("{0}\t{1:d}\t{2}",
      order.SalesOrderID,
      order.OrderDate,
      order.SalesOrderNumber);
}
```

```vb
Dim orders = ds.Tables("SalesOrderHeader")

Dim query = _
       From o In orders _
       Where o.OnlineOrderFlag = True _
       Select New {SalesOrderID := o.SalesOrderID, _
                   OrderDate := o.OrderDate, _
                   SalesOrderNumber := o.SalesOrderNumber}

For Each Dim onlineOrder In query
 Console.WriteLine("{0}\t{1:d}\t{2}", _
 onlineOrder.SalesOrderID, _
 onlineOrder.OrderDate, _
 onlineOrder.SalesOrderNumber)
Next
```

## <a name="see-also"></a>Voir aussi

- [Interrogation de DataSets](../../../../docs/framework/data/adonet/querying-datasets-linq-to-dataset.md)
- [Requêtes de table croisée](../../../../docs/framework/data/adonet/cross-table-queries-linq-to-dataset.md)
- [Requêtes de table unique](../../../../docs/framework/data/adonet/single-table-queries-linq-to-dataset.md)
