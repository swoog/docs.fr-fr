---
title: 'Exemples de syntaxe de requête fondée sur une méthode : Opérateurs d’agrégation (LINQ to DataSet)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 5ed5f01d-acb2-4dd4-be60-f04c2d570fa8
ms.openlocfilehash: 88d9c7299c9dbf024a07f223ef7ec7d03f8066d8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772318"
---
# <a name="method-based-query-syntax-examples-aggregate-operators-linq-to-dataset"></a>Exemples de syntaxe de requête fondée sur une méthode : Opérateurs d’agrégation (LINQ to DataSet)
Les exemples de cette rubrique montrent comment utiliser les opérateurs <xref:System.Linq.Enumerable.Aggregate%2A>, <xref:System.Linq.Enumerable.Average%2A>, <xref:System.Linq.Enumerable.Count%2A>, <xref:System.Linq.Enumerable.LongCount%2A>, <xref:System.Linq.Enumerable.Max%2A>, <xref:System.Linq.Enumerable.Min%2A> et <xref:System.Linq.Enumerable.Sum%2A> pour interroger un <xref:System.Data.DataSet> et agréger des données à l'aide de la syntaxe de requête de méthode.  
  
 Le `FillDataSet` méthode utilisé dans ces exemples est spécifiée dans [chargement des données dans un jeu de données](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md).  
  
 Les exemples de cette rubrique utilisent les tables Contact, Address, Product, SalesOrderHeader et SalesOrderDetail de l'exemple de base de données AdventureWorks.  
  
 Les exemples de cette rubrique utilisent les éléments suivants `using` / `Imports` instructions :  
  
 [!code-csharp[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#importsusing)]  
  
 Pour plus d'informations, voir [Procédure : Créer un projet LINQ to DataSet dans Visual Studio](../../../../docs/framework/data/adonet/how-to-create-a-linq-to-dataset-project-in-vs.md).  
  
## <a name="aggregate"></a>Aggregate  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Aggregate%2A> pour obtenir les cinq premiers contacts de la table `Contact` et créer une liste de noms délimités par des virgules.  
  
 [!code-csharp[DP LINQ to DataSet Examples#Aggregate_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#aggregate_mq)]
 [!code-vb[DP LINQ to DataSet Examples#Aggregate_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#aggregate_mq)]  
  
## <a name="average"></a>Average  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Average%2A> pour trouver le prix moyen courant des produits.  
  
 [!code-csharp[DP LINQ to DataSet Examples#Average_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#average_mq)]
 [!code-vb[DP LINQ to DataSet Examples#Average_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#average_mq)]  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Average%2A> pour trouver le prix moyen courant des produits de chaque style.  
  
 [!code-csharp[DP LINQ to DataSet Examples#Average2_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#average2_mq)]
 [!code-vb[DP LINQ to DataSet Examples#Average2_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#average2_mq)]  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Average%2A> pour trouver le montant total moyen dû.  
  
 [!code-csharp[DP LINQ to DataSet Examples#AverageProjection_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#averageprojection_mq)]
 [!code-vb[DP LINQ to DataSet Examples#AverageProjection_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#averageprojection_mq)]  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Average%2A> pour obtenir le montant total moyen dû pour chaque ID de contact.  
  
 [!code-csharp[DP LINQ to DataSet Examples#AverageGrouped_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#averagegrouped_mq)]
 [!code-vb[DP LINQ to DataSet Examples#AverageGrouped_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#averagegrouped_mq)]  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Average%2A> pour obtenir les commandes avec le `TotalDue` moyen pour chaque contact.  
  
 [!code-csharp[DP LINQ to DataSet Examples#AverageElements_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#averageelements_mq)]
 [!code-vb[DP LINQ to DataSet Examples#AverageElements_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#averageelements_mq)]  
  
## <a name="count"></a>Nombre  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Count%2A> pour retourner le nombre de produits dans la table `Product`.  
  
 [!code-csharp[DP LINQ to DataSet Examples#Count](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#count)]
 [!code-vb[DP LINQ to DataSet Examples#Count](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#count)]  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Count%2A> pour retourner une liste des ID de contact ID et du nombre de commandes de chaque ID de contact.  
  
 [!code-csharp[DP LINQ to DataSet Examples#CountNested](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#countnested)]
 [!code-vb[DP LINQ to DataSet Examples#CountNested](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#countnested)]  
  
### <a name="example"></a>Exemple  
 Cet exemple regroupe les produits par couleur et utilise la méthode <xref:System.Linq.Enumerable.Count%2A> pour retourner le nombre de produits dans chaque groupe de couleur.  
  
 [!code-csharp[DP LINQ to DataSet Examples#CountGrouped](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#countgrouped)]
 [!code-vb[DP LINQ to DataSet Examples#CountGrouped](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#countgrouped)]  
  
## <a name="longcount"></a>LongCount  
  
### <a name="example"></a>Exemple  
 Cet exemple obtient le nombre de contacts sous la forme d'un entier long.  
  
 [!code-csharp[DP LINQ to DataSet Examples#LongCountSimple](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#longcountsimple)]
 [!code-vb[DP LINQ to DataSet Examples#LongCountSimple](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#longcountsimple)]  
  
## <a name="max"></a>Max  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Max%2A> pour obtenir le montant total dû le plus élevé.  
  
 [!code-csharp[DP LINQ to DataSet Examples#MaxProjection_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#maxprojection_mq)]
 [!code-vb[DP LINQ to DataSet Examples#MaxProjection_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#maxprojection_mq)]  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Max%2A> pour obtenir le montant total dû le plus élevé pour chaque ID de contact.  
  
 [!code-csharp[DP LINQ to DataSet Examples#MaxGrouped_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#maxgrouped_mq)]
 [!code-vb[DP LINQ to DataSet Examples#MaxGrouped_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#maxgrouped_mq)]  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Max%2A> pour obtenir les commandes présentant le `TotalDue` le plus élevé pour chaque ID de contact.  
  
 [!code-csharp[DP LINQ to DataSet Examples#MaxElements_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#maxelements_mq)]
 [!code-vb[DP LINQ to DataSet Examples#MaxElements_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#maxelements_mq)]  
  
## <a name="min"></a>Min  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Min%2A> pour obtenir le montant total dû le plus bas.  
  
 [!code-csharp[DP LINQ to DataSet Examples#MinProjection_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#minprojection_mq)]
 [!code-vb[DP LINQ to DataSet Examples#MinProjection_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#minprojection_mq)]  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Min%2A> pour obtenir le montant total dû le plus bas pour chaque ID de contact.  
  
 [!code-csharp[DP LINQ to DataSet Examples#MinGrouped_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#mingrouped_mq)]
 [!code-vb[DP LINQ to DataSet Examples#MinGrouped_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#mingrouped_mq)]  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Min%2A> pour obtenir les commandes présentant le montant total dû le plus bas pour chaque ID de contact.  
  
 [!code-csharp[DP LINQ to DataSet Examples#MinElements_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#minelements_mq)]
 [!code-vb[DP LINQ to DataSet Examples#MinElements_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#minelements_mq)]  
  
## <a name="sum"></a>Sum  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Sum%2A> pour obtenir le total des quantités commandées de la table `SalesOrderDetail`.  
  
 [!code-csharp[DP LINQ to DataSet Examples#SumProjection_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#sumprojection_mq)]  
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Sum%2A> pour obtenir le montant total dû de chaque ID de contact.  
  
 [!code-csharp[DP LINQ to DataSet Examples#SumGrouped_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#sumgrouped_mq)]
 [!code-vb[DP LINQ to DataSet Examples#SumGrouped_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#sumgrouped_mq)]  
  
## <a name="see-also"></a>Voir aussi

- [Chargement de données dans un DataSet](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)
- [Exemples LINQ to DataSet](../../../../docs/framework/data/adonet/linq-to-dataset-examples.md)
- [Vue d’ensemble des opérateurs de requête standard (C#)](../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [Vue d’ensemble des opérateurs de requête standard (Visual Basic)](../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
