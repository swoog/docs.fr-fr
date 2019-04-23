---
title: 'Exemples de syntaxe d’expression de requête : Restriction (LINQ to DataSet)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1daf42c2-c9f4-4cda-b291-7641b9c6d3fe
ms.openlocfilehash: 0c711a2d9edbc3b462048272dd7dd138fd934a89
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59160571"
---
# <a name="query-expression-syntax-examples-restriction-linq-to-dataset"></a>Exemples de syntaxe d’expression de requête : Restriction (LINQ to DataSet)
Les exemples de cette rubrique montrent comment utiliser la méthode <xref:System.Linq.Enumerable.Where%2A> pour interroger un <xref:System.Data.DataSet> à l'aide de la syntaxe d'expression de requête.  
  
 Le `FillDataSet` méthode utilisé dans ces exemples est spécifiée dans [chargement des données dans un jeu de données](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md).  
  
 Les exemples de cette rubrique utilisent les tables Contact, Address, Product, SalesOrderHeader et SalesOrderDetail de l'exemple de base de données AdventureWorks.  
  
 Les exemples de cette rubrique utilisent les éléments suivants `using` / `Imports` instructions :  
  
[!code-csharp[DP LINQ to DataSetExamples#ImportsUsing](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#importsusing)]        
  
 Pour plus d'informations, voir [Procédure : Créer un projet LINQ to DataSet dans Visual Studio](../../../../docs/framework/data/adonet/how-to-create-a-linq-to-dataset-project-in-vs.md).  
  
## <a name="where"></a>Où  
  
### <a name="example"></a>Exemple  
 Cet exemple retourne toutes les commandes en ligne.  
  
 [!code-csharp[DP LINQ to DataSet Examples#Where1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#where1)]  
 [!code-vb[DP LINQ to DataSet Examples#Where1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#where1)]     
  
### <a name="example"></a>Exemple  
 Cet exemple retourne les commandes où la quantité commandée est supérieure à 2 et inférieure à 6.  
  
 [!code-csharp[DP LINQ to DataSet Examples#Where2](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#where2)]  
 [!code-vb[DP LINQ to DataSet Examples#Where2](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#where2)]     
  
### <a name="example"></a>Exemple  
 Cet exemple retourne tous les produits de couleur rouge.  
  
 [!code-csharp[DP LINQ to DataSet Examples#Where3](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#where3)]  
 [!code-vb[DP LINQ to DataSet Examples#Where3](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#where3)]     
  
### <a name="example"></a>Exemple  
 Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Where%2A> pour rechercher des commandes qui ont été passées après le 1er décembre 2002, puis utilise la méthode <xref:System.Data.DataRow.GetChildRows%2A> pour obtenir les détails de chaque commande.  
  
 [!code-csharp[DP LINQ to DataSetExamples#WhereDrillDown](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#wheredrilldown)]       
 [!code-vb[DP LINQ to DataSet Examples#WhereDrillDown](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#wheredrilldown)]  
  
## <a name="see-also"></a>Voir aussi

- [Chargement de données dans un DataSet](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)
- [Exemples LINQ to DataSet](../../../../docs/framework/data/adonet/linq-to-dataset-examples.md)
- [Vue d’ensemble des opérateurs de requête standard (C#)](../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [Vue d’ensemble des opérateurs de requête standard (Visual Basic)](../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
