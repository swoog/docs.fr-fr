---
title: 'Exemples de syntaxe de requête fondée sur une méthode : Opérateurs de jeu (LINQ to DataSet)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: fa93af15-28af-4b5e-846b-897308410edb
ms.openlocfilehash: 31421b1e6ece783f52021c1af22b819f8aacea66
ms.sourcegitcommit: c6f69b0cf149f6b54483a6d5c2ece222913f43ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55903428"
---
# <a name="method-based-query-syntax-examples-set-operators-linq-to-dataset"></a>Exemples de syntaxe de requête fondée sur une méthode : Opérateurs de jeu (LINQ to DataSet)
Les exemples de cette rubrique montrent comment utiliser le <xref:System.Linq.Enumerable.Distinct%2A>, <xref:System.Linq.Enumerable.Except%2A>, <xref:System.Linq.Enumerable.Intersect%2A>, et <xref:System.Linq.Enumerable.Union%2A> opérateurs pour effectuer des opérations de comparaison basée sur des ensembles de lignes de données.[ Chargement des données dans un jeu de données](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md) consultez [comparaison de DataRows](../../../../docs/framework/data/adonet/comparing-datarows-linq-to-dataset.md) pour plus d’informations sur <xref:System.Data.DataRowComparer>.  
  
 Le `FillDataSet` méthode utilisé dans ces exemples est spécifiée dans [chargement des données dans un jeu de données](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md).  
  
 Les exemples de cette rubrique utilisent les tables Contact, Address, Product, SalesOrderHeader et SalesOrderDetail de l'exemple de base de données AdventureWorks.  
  
 Les exemples de cette rubrique utilisent les éléments suivants `using` / `Imports` instructions :  
  
 [!code-csharp[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#importsusing)]  
  
 Pour plus d'informations, voir [Procédure : Créer un projet LINQ to DataSet dans Visual Studio](../../../../docs/framework/data/adonet/how-to-create-a-linq-to-dataset-project-in-vs.md).  
  
## <a name="distinct"></a>distinct  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Distinct%2A> pour supprimer des éléments en double dans une séquence.  
  
 [!code-csharp[DP LINQ to DataSet Examples#DistinctRows](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#distinctrows)]
 [!code-vb[DP LINQ to DataSet Examples#DistinctRows](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#distinctrows)]  
  
## <a name="except"></a>Except  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Except%2A> pour retourner les contacts qui apparaissent dans la première table, mais pas dans la seconde.  
  
 [!code-csharp[DP LINQ to DataSet Examples#Except2](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#except2)]
 [!code-vb[DP LINQ to DataSet Examples#Except2](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#except2)]  
  
## <a name="intersect"></a>Intersection  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Intersect%2A> pour retourner les contacts qui apparaissent dans les deux tables.  
  
 [!code-csharp[DP LINQ to DataSet Examples#Intersect2](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#intersect2)]
 [!code-vb[DP LINQ to DataSet Examples#Intersect2](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#intersect2)]  
  
## <a name="union"></a>Union  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Union%2A> pour retourner des contacts uniques dans l'une ou l'autre des tables.  
  
 [!code-csharp[DP LINQ to DataSet Examples#Union2](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#union2)]
 [!code-vb[DP LINQ to DataSet Examples#Union2](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#union2)]  
  
## <a name="see-also"></a>Voir aussi
- [Chargement de données dans un DataSet](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)
- [Exemples LINQ to DataSet](../../../../docs/framework/data/adonet/linq-to-dataset-examples.md)
- [Vue d’ensemble des opérateurs de requête standard (C#)](../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [Vue d’ensemble des opérateurs de requête standard (Visual Basic)](../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
