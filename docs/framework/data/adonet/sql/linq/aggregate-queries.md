---
title: Requêtes d'agrégation
ms.date: 03/30/2017
ms.assetid: 13ec5580-05ce-4a1f-9d3d-8660be7891a2
ms.openlocfilehash: e4d5e0a9dc1ffb0bf1857fee788d46947f3901d4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="aggregate-queries"></a>Requêtes d'agrégation
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] prend en charge les opérateurs d'agrégation `Average`, `Count`, `Max`, `Min` et `Sum`. Notez les caractéristiques suivantes des opérateurs d'agrégation dans [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] :  
  
-   Les requêtes d'agrégation sont exécutées immédiatement.  
  
     Pour plus d’informations, consultez [Introduction aux requêtes LINQ (C#)](~/docs/csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md).  
  
-   Les requêtes d’agrégation retournent généralement un nombre au lieu d’une collection.  
  
     Pour plus d’informations, consultez [opérations d’agrégation](http://msdn.microsoft.com/library/36d97c83-5de5-457d-971d-10a69365e7c4).  
  
-   Vous ne pouvez pas appeler d'agrégats à l'aide de types anonymes.  
  
 Les exemples des rubriques suivantes dérivent de l'exemple de base de données Northwind. Pour plus d’informations, consultez [téléchargement d’exemples de bases de données](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md).  
  
## <a name="in-this-section"></a>Dans cette section  
 [Retourner la valeur moyenne d’une séquence numérique](../../../../../../docs/framework/data/adonet/sql/linq/return-the-average-value-from-a-numeric-sequence.md)  
 Montre comment utiliser l'opérateur <xref:System.Linq.Enumerable.Average%2A>.  
  
 [Dénombrer les éléments d’une séquence](../../../../../../docs/framework/data/adonet/sql/linq/count-the-number-of-elements-in-a-sequence.md)  
 Montre comment utiliser l'opérateur <xref:System.Linq.Enumerable.Count%2A>.  
  
 [Rechercher la valeur maximale dans une séquence numérique](../../../../../../docs/framework/data/adonet/sql/linq/find-the-maximum-value-in-a-numeric-sequence.md)  
 Montre comment utiliser l'opérateur <xref:System.Linq.Enumerable.Max%2A>.  
  
 [Rechercher la valeur minimale dans une séquence numérique](../../../../../../docs/framework/data/adonet/sql/linq/find-the-minimum-value-in-a-numeric-sequence.md)  
 Montre comment utiliser l'opérateur <xref:System.Linq.Enumerable.Min%2A>.  
  
 [Calculer la somme de valeurs dans une séquence numérique](../../../../../../docs/framework/data/adonet/sql/linq/compute-the-sum-of-values-in-a-numeric-sequence.md)  
 Montre comment utiliser l'opérateur <xref:System.Linq.Enumerable.Sum%2A>.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Exemples de requêtes](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)  
 Fournit des liens vers les requêtes [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] dans Visual Basic et C#.  
  
 [Concepts relatifs aux requêtes](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)  
 Fournit des liens vers des rubriques qui présentent des concepts pour la conception de requêtes [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)] dans [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].  
  
 [Introduction aux requêtes LINQ (C#)](~/docs/csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md)  
 Explique le fonctionnement des requêtes dans [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)].
