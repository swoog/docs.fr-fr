---
title: "'For Each' pour le type '<typename>' est ambigu, car le type implémente plusieurs instanciations de 'System.Collections.Generic.IEnumerable(Of T)'"
ms.date: 07/20/2015
f1_keywords:
- vbc32096
- bc32096
helpviewer_keywords:
- BC32096
ms.assetid: ed20d09c-913f-482e-89f8-c0a596c3ec24
ms.openlocfilehash: bdfb6e9b1332db1f049bb2575e97215026efe0dd
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65591760"
---
# <a name="for-each-on-type-typename-is-ambiguous-because-the-type-implements-multiple-instantiations-of-systemcollectionsgenericienumerableof-t"></a>'For Each' pour le type '\<nom_type >' est ambigu, car le type implémente plusieurs instanciations de 'System.Collections.Generic.IEnumerable (Of T)'
Un `For Each` instruction spécifie une variable d’itérateur qui a plusieurs <xref:System.Collections.IEnumerable.GetEnumerator%2A> (méthode).  
  
 La variable d’itérateur doit être d’un type qui implémente le <xref:System.Collections.IEnumerable?displayProperty=nameWithType> ou <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> interface dans un de le `Collections` espaces de noms du .NET Framework. Il est possible pour une classe implémenter plusieurs interfaces génériques construits, à l’aide d’un argument de type différent pour chaque construction. Si une classe qui s’en charge est utilisée pour la variable d’itérateur, cette variable a plusieurs <xref:System.Collections.IEnumerable.GetEnumerator%2A> (méthode). Dans ce cas, Visual Basic ne peut pas choisir la méthode à appeler.  
  
 **ID d’erreur :** BC32096  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Utilisez [opérateur DirectCast](../../../visual-basic/language-reference/operators/directcast-operator.md) ou [opérateur TryCast](../../../visual-basic/language-reference/operators/trycast-operator.md) un cast du type de variable itérateur vers l’interface définissant le <xref:System.Collections.IEnumerable.GetEnumerator%2A> méthode que vous souhaitez utiliser.  
  
## <a name="see-also"></a>Voir aussi

- [For Each...Next (instruction)](../../../visual-basic/language-reference/statements/for-each-next-statement.md)
- [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
