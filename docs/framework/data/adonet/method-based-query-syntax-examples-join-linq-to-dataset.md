---
title: 'Exemples de syntaxe de requête fondée sur une méthode : Joindre (LINQ to DataSet)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 4fd5ed2c-b03a-4054-a3ed-3ddb380d7d9d
ms.openlocfilehash: 84bd5f48c993dc5b15104b70081f739a1bec2e5c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772123"
---
# <a name="method-based-query-syntax-examples-join-linq-to-dataset"></a>Exemples de syntaxe de requête fondée sur une méthode : Joindre (LINQ to DataSet)
La jointure est une opération importante dans les requêtes qui ciblent des sources de données qui n'ont pas de relations explorables les unes avec les autres, comme les tables de base de données relationnelles. Une jointure de deux sources de données est l'association d'objets dans une source de données avec des objets qui partagent un attribut commun dans l'autre source de données. Pour plus d’informations, consultez [vue d’ensemble des opérateurs de requête Standard (C#)](../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md) ou [présentation des opérateurs de requête Standard (Visual Basic)](../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md).  
  
 Les exemples de cette rubrique montrent comment utiliser la méthode <xref:System.Linq.Enumerable.Join%2A> pour interroger un <xref:System.Data.DataSet> à l'aide de la syntaxe d'interrogation de méthode.  
  
 Le `FillDataSet` méthode utilisé dans ces exemples est spécifiée dans [chargement des données dans un jeu de données](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md).  
  
 Les exemples de cette rubrique utilisent les tables Contact, Address, Product, SalesOrderHeader et SalesOrderDetail de l'exemple de base de données AdventureWorks.  
  
 Les exemples de cette rubrique utilisent les éléments suivants `using` / `Imports` instructions :  
  
 [!code-csharp[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#importsusing)]  
  
 Pour plus d'informations, voir [Procédure : Créer un projet LINQ to DataSet dans Visual Studio](../../../../docs/framework/data/adonet/how-to-create-a-linq-to-dataset-project-in-vs.md).  
  
## <a name="join"></a>Join  
  
### <a name="example"></a>Exemple  
 Cet exemple effectue une jointure sur les tables `Contact` et `SalesOrderHeader`.  
  
 [!code-csharp[DP LINQ to DataSet Examples#JoinSimple_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#joinsimple_mq)]
 [!code-vb[DP LINQ to DataSet Examples#JoinSimple_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#joinsimple_mq)]  
  
### <a name="example"></a>Exemple  
 Cet exemple effectue une jointure sur les tables `Contact` et `SalesOrderHeader`, en regroupant les résultats par ID de contact.  
  
 [!code-csharp[DP LINQ to DataSet Examples#JoinWithGroupedResults_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#joinwithgroupedresults_mq)]
 [!code-vb[DP LINQ to DataSet Examples#JoinWithGroupedResults_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#joinwithgroupedresults_mq)]  
  
## <a name="see-also"></a>Voir aussi

- [Chargement de données dans un DataSet](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)
- [Exemples LINQ to DataSet](../../../../docs/framework/data/adonet/linq-to-dataset-examples.md)
- [Vue d’ensemble des opérateurs de requête standard (C#)](../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [Vue d’ensemble des opérateurs de requête standard (Visual Basic)](../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [Exemples de jointure](https://go.microsoft.com/fwlink/?LinkId=187357)
- [Exemples de DataSet](https://go.microsoft.com/fwlink/?LinkId=187358)
