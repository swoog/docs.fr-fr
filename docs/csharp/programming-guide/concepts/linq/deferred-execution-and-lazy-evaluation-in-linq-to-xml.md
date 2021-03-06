---
title: Exécution et évaluation différées dans LINQ to XML (C#)
ms.date: 07/20/2015
ms.assetid: 8683d1b4-b7ec-407b-be12-906ebe958a09
ms.openlocfilehash: 940885d6499bd2730c0bd4a5e15a490a9e85deab
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64597431"
---
# <a name="deferred-execution-and-lazy-evaluation-in-linq-to-xml-c"></a>Exécution et évaluation différées dans LINQ to XML (C#)
Les opérations de requête et d'axe sont souvent implémentées pour utiliser l'exécution différée. Cette rubrique explique les conditions requises et les avantages de l'exécution différée et certaines considérations relatives à l'implémentation.  
  
## <a name="deferred-execution"></a>Exécution différée  
 Le terme "exécution différée" signifie que l’évaluation d’une expression est retardée jusqu’à ce que sa valeur *réalisée* soit réellement nécessaire. L'exécution différée peut améliorer sensiblement les performances lorsque vous devez manipuler de grandes collectes de données, en particulier dans les programmes qui contiennent une série de manipulations ou de requêtes chaînées. Dans le meilleur cas, l'exécution différée autorise une seule itération dans la collection source.  
  
 Les technologies LINQ utilisent beaucoup l'exécution différée dans les membres des classes <xref:System.Linq?displayProperty=nameWithType> principales et dans les méthodes d'extension dans les différents espaces de noms LINQ, tels que <xref:System.Xml.Linq.Extensions?displayProperty=nameWithType>.  
  
 L’exécution différée est prise en charge directement dans le langage C# par le mot clé [yield](../../../../csharp/language-reference/keywords/yield.md) (sous la forme de l’instruction `yield-return`) quand elle est utilisée dans un bloc itérateur. Un tel itérateur doit renvoyer une collection de type <xref:System.Collections.IEnumerator> ou <xref:System.Collections.Generic.IEnumerator%601> (ou un type dérivé).  
  
## <a name="eager-vs-lazy-evaluation"></a>Évaluation stricte et évaluation différée  
 Lorsque vous écrivez une méthode qui implémente l'exécution différée, vous devez également décider s'il faut implémenter la méthode à l'aide de l'évaluation différée ou de l'évaluation stricte.  
  
- Avec l’*évaluation différée*, un seul élément de la collection source est traité pendant chaque appel à l’itérateur. Il s'agit du mode d'implémentation par défaut des itérateurs.  
  
- Avec l’*évaluation stricte*, le premier appel à l’itérateur entraîne le traitement de l’ensemble de la collection. Une copie temporaire de la collection source peut également être nécessaire. Par exemple, la méthode <xref:System.Linq.Enumerable.OrderBy%2A> doit trier l'ensemble de la collection avant de renvoyer le premier élément.  
  
 L'évaluation différée procure en général de meilleures performances car elle répartit le traitement de surcharge de manière égale durant l'évaluation de la collection et limite l'utilisation des données temporaires. Bien entendu, pour certaines opérations il est impossible d'éviter la matérialisation de résultats intermédiaires.  
  
## <a name="next-steps"></a>Étapes suivantes  
 La rubrique suivante de ce didacticiel illustre l'exécution différée :  
  
- [Exemple d’exécution différée (C#)](../../../../csharp/programming-guide/concepts/linq/deferred-execution-example.md)  
  
## <a name="see-also"></a>Voir aussi

- [Tutoriel : Chaînage de requêtes (C#)](../../../../csharp/programming-guide/concepts/linq/tutorial-chaining-queries-together.md)
- [Concepts et terminologie (transformation fonctionnelle) (C#)](../../../../csharp/programming-guide/concepts/linq/concepts-and-terminology-functional-transformation.md)
- [Opérations d’agrégation (C#)](../../../../csharp/programming-guide/concepts/linq/aggregation-operations.md)
- [yield](../../../../csharp/language-reference/keywords/yield.md)
