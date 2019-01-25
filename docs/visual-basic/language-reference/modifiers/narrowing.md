---
title: Narrowing (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.narrowing
helpviewer_keywords:
- conversions [Visual Basic], type
- type conversion [Visual Basic]
- conversions [Visual Basic], data type
- Narrowing keyword [Visual Basic]
- data type conversion [Visual Basic]
ms.assetid: a207ee91-aca4-4771-b4e2-713f029bf2bb
ms.openlocfilehash: bd88c05f16a2027b0367effebef809cb5e5abfe8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54617433"
---
# <a name="narrowing-visual-basic"></a>Narrowing (Visual Basic)
Indique qu’un opérateur de conversion (`CType`) convertit une classe ou structure à un type qui peut ne pas pouvoir contenir certaines des valeurs possibles de la classe ou la structure d’origine.  
  
## <a name="converting-with-the-narrowing-keyword"></a>Conversion avec le mot clé restrictive  
 La procédure de conversion doit spécifier `Public Shared` outre `Narrowing`.  
  
 Les conversions restrictives ne pas toujours réussisse au moment de l’exécution et peut échouer ou entraîner une perte de données. Sont des exemples `Long` à `Integer`, `String` à `Date`et un type de base en un type dérivé. Cette dernière conversion est restrictive, car le type de base ne peut pas contenir tous les membres du type dérivé et n’est donc pas une instance du type dérivé.  
  
 Si `Option Strict` est `On`, le code utilisateur doit utiliser `CType` pour toutes les conversions restrictives.  
  
 Le `Narrowing` mot clé peut être utilisé dans ce contexte :  
  
 [Operator (instruction)](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
## <a name="see-also"></a>Voir aussi
- [Operator (instruction)](../../../visual-basic/language-reference/statements/operator-statement.md)
- [Widening](../../../visual-basic/language-reference/modifiers/widening.md)
- [Conversions étendues et restrictives](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [Guide pratique pour Définir un opérateur](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [CType (fonction)](../../../visual-basic/language-reference/functions/ctype-function.md)
- [Option Strict (instruction)](../../../visual-basic/language-reference/statements/option-strict-statement.md)
