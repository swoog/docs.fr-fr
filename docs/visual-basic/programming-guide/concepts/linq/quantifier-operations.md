---
title: Opérations de quantificateur (Visual Basic)
ms.date: 07/20/2015
ms.assetid: ae1a2b73-503c-4f4b-a3fd-31b5adbee67c
ms.openlocfilehash: e871a77caf0b7cfe361f11462085180c17bf2057
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61766559"
---
# <a name="quantifier-operations-visual-basic"></a>Opérations de quantificateur (Visual Basic)
Les opérations de quantificateur retournent une valeur <xref:System.Boolean> qui indique si certains ou tous les éléments d’une séquence remplissent une condition.  
  
 L’illustration suivante représente deux opérations de quantificateur différentes sur deux séquences sources différentes. La première opération demande si un ou plusieurs des éléments sont le caractère 'A' et le résultat est `true`. La deuxième opération demande si tous les éléments sont le caractère 'A' et le résultat est `true`.  
  
 ![Opérations de quantificateur LINQ](./media/quantifier-operations/linq-quantifier-operations.png)  
  
 Les méthodes d’opérateur de requête standard qui effectuent des opérations de quantificateur sont répertoriées dans la section suivante.  
  
## <a name="methods"></a>Méthodes  
  
|Nom de la méthode|Description|Syntaxe d’Expression de requête de Visual Basic|Informations complémentaires|  
|-----------------|-----------------|------------------------------------------|----------------------|  
|Tous|Détermine si tous les éléments d’une séquence remplissent une condition.|`Aggregate … In … Into All(…)`|<xref:System.Linq.Enumerable.All%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.All%2A?displayProperty=nameWithType>|  
|Any|Détermine si certains éléments d’une séquence remplissent une condition.|`Aggregate … In … Into Any()`|<xref:System.Linq.Enumerable.Any%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Any%2A?displayProperty=nameWithType>|  
|Contient|Détermine si une séquence contient un élément spécifié.|Non applicable.|<xref:System.Linq.Enumerable.Contains%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Contains%2A?displayProperty=nameWithType>|  
  
## <a name="query-expression-syntax-examples"></a>Exemples de syntaxe d'expression de requête  
 Ces exemples utilisent la `Aggregate` clause en Visual Basic en tant que partie de la condition de filtrage dans une requête LINQ.  
  
 L’exemple suivant utilise le `Aggregate` clause et la <xref:System.Linq.Enumerable.All%2A> méthode d’extension pour retourner à partir d’une collection de ces personnes dont les animaux domestiques sont tous dépassés un âge spécifié.  
  
 [!code-vb[CsLINQAnyAll#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/CsLINQAnyAll/VB/AnyAll.vb#1)]  
  
 L’exemple suivant utilise le `Aggregate` clause et la <xref:System.Linq.Enumerable.Any%2A> méthode d’extension pour retourner à partir d’une collection, les personnes qui ont au moins un animal domestique qui a dépassé un âge spécifié.  
  
 [!code-vb[CsLINQAnyAll#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/CsLINQAnyAll/VB/AnyAll.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Linq>
- [Vue d’ensemble des opérateurs de requête standard (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [Aggregate (clause)](../../../../visual-basic/language-reference/queries/aggregate-clause.md)
- [Guide pratique pour Rechercher des phrases qui contiennent un ensemble spécifié de mots (LINQ) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-query-for-sentences-that-contain-a-specified-set-of-words.md)
