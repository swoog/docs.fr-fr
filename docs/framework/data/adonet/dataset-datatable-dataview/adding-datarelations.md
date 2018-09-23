---
title: Ajout de DataRelations
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: a4a564fb-c1c4-4135-b6c2-b030e51195e4
ms.openlocfilehash: d0f481979ead7af775d462a2624ec43080e2c5a9
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/23/2018
ms.locfileid: "46706237"
---
# <a name="adding-datarelations"></a>Ajout de DataRelations
Dans un objet <xref:System.Data.DataSet> contenant plusieurs objets <xref:System.Data.DataTable>, vous pouvez utiliser des objets <xref:System.Data.DataRelation> pour associer une table à une autre, pour vous déplacer dans les tables et pour retourner les lignes enfants ou parentes d'une table associée.  
  
 Les arguments requis pour créer un **DataRelation** sont un nom pour le **DataRelation** est créé et un tableau d’un ou plusieurs <xref:System.Data.DataColumn> références aux colonnes qui servent de parent et enfant colonnes dans la relation. Après avoir créé un **DataRelation**, vous pouvez l’utiliser pour naviguer entre les tables et de récupérer des valeurs.  
  
 Ajout d’un **DataRelation** à un <xref:System.Data.DataSet> ajoute, par défaut, un <xref:System.Data.UniqueConstraint> à la table parente et une <xref:System.Data.ForeignKeyConstraint> à la table enfant. Pour plus d’informations sur ces contraintes par défaut, consultez [contraintes de DataTable](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatable-constraints.md).  
  
 L’exemple de code suivant crée un **DataRelation** à l’aide de deux <xref:System.Data.DataTable> des objets dans un <xref:System.Data.DataSet>. Chaque <xref:System.Data.DataTable> contient une colonne nommée **CustID**, qui sert de lien entre les deux <xref:System.Data.DataTable> objets. L’exemple ajoute un seul **DataRelation** à la **Relations** collection de la <xref:System.Data.DataSet>. Le premier argument dans l’exemple spécifie le nom de la **DataRelation** en cours de création. Le deuxième argument définit le parent **DataColumn** et le troisième argument définit l’enfant **DataColumn**.  
  
```vb  
customerOrders.Relations.Add("CustOrders", _  
  customerOrders.Tables("Customers").Columns("CustID"), _  
  customerOrders.Tables("Orders").Columns("CustID"))  
```  
  
```csharp  
customerOrders.Relations.Add("CustOrders",  
  customerOrders.Tables["Customers"].Columns["CustID"],  
  customerOrders.Tables["Orders"].Columns["CustID"]);  
```  
  
 Un **DataRelation** a également un **Nested** propriété qui, lorsque la valeur **true**, imbrique les lignes de la table enfant dans la ligne associée de la table parente lors de l’écriture en tant qu’éléments XML à l’aide de <xref:System.Data.DataSet.WriteXml%2A> . Pour plus d’informations, consultez [Utilisation de XML dans un DataSet](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md).  
  
## <a name="see-also"></a>Voir aussi  
 [DataSets, DataTables et DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)  
 [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
