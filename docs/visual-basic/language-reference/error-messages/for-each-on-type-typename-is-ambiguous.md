---
title: '&#39;Pour chaque&#39; sur le type &#39; &lt;typename&gt; &#39; est ambigu, car le type implémente plusieurs instanciations de &#39;System.Collections.Generic.IEnumerable (Of T)&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc32096
- bc32096
helpviewer_keywords:
- BC32096
ms.assetid: ed20d09c-913f-482e-89f8-c0a596c3ec24
ms.openlocfilehash: 8c48a7134eb8da83fb418b9aa91d55dcbe8e8bcb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33590963"
---
# <a name="39for-each39-on-type-39lttypenamegt39-is-ambiguous-because-the-type-implements-multiple-instantiations-of-39systemcollectionsgenericienumerableof-t39"></a>&#39;Pour chaque&#39; sur le type &#39; &lt;typename&gt; &#39; est ambigu, car le type implémente plusieurs instanciations de &#39;System.Collections.Generic.IEnumerable (Of T)&#39;
A `For Each` instruction spécifie une variable itérateur qui a plusieurs <xref:System.Collections.IEnumerable.GetEnumerator%2A> (méthode).  
  
 La variable d’itérateur doit être d’un type qui implémente le <xref:System.Collections.IEnumerable?displayProperty=nameWithType> ou <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> interface dans un de le `Collections` espaces de noms de la [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]. Il est possible qu’une classe implémente plusieurs interfaces génériques construits, à l’aide d’un argument de type différent pour chaque construction. Si une classe qui effectue l’opération est utilisée pour la variable d’itérateur, cette variable a plusieurs <xref:System.Collections.IEnumerable.GetEnumerator%2A> (méthode). Dans ce cas, Visual Basic ne peut pas choisir la méthode à appeler.  
  
 **ID d’erreur :** BC32096  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Utilisez [opérateur DirectCast](../../../visual-basic/language-reference/operators/directcast-operator.md) ou [opérateur TryCast](../../../visual-basic/language-reference/operators/trycast-operator.md) pour effectuer un cast du type de variable itérateur vers l’interface qui définit la <xref:System.Collections.IEnumerable.GetEnumerator%2A> méthode que vous souhaitez utiliser.  
  
## <a name="see-also"></a>Voir aussi  
 [For Each...Next (instruction)](../../../visual-basic/language-reference/statements/for-each-next-statement.md)  
 [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
