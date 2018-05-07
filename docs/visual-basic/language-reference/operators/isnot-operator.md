---
title: Opérateur IsNot (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.isnot
helpviewer_keywords:
- IsNot operator [Visual Basic]
ms.assetid: 8dd2bcdb-0166-48a2-9094-60dfb448f36c
ms.openlocfilehash: babee364d350ca84a8379f675acc4b5c87f98303
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="isnot-operator-visual-basic"></a>Opérateur IsNot (Visual Basic)
Compare deux variables de référence d’objet.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
result = object1 IsNot object2  
```  
  
## <a name="parts"></a>Composants  
 `result`  
 Obligatoire. Valeur `Boolean`.  
  
 `object1`  
 Obligatoire. N’importe quel `Object` variable ou une expression.  
  
 `object2`  
 Obligatoire. N’importe quel `Object` variable ou une expression.  
  
## <a name="remarks"></a>Notes  
 Le `IsNot` opérateur détermine si deux références d’objet font référence à des objets différents. Toutefois, il n’effectue pas de comparaisons de valeurs. Si `object1` et `object2` se rapportent à la même instance d’objet, `result` est `False`; le cas contraire, `result` est `True`.  
  
 `IsNot` est le contraire de la `Is` opérateur. L’avantage de `IsNot` est que vous pouvez éviter la syntaxe difficile avec `Not` et `Is`, qui peut être difficile à lire.  
  
 Vous pouvez utiliser la `Is` et `IsNot` opérateurs pour tester des objets à liaison anticipée et liaison tardive.  
  
> [!NOTE]
>  Le `IsNot` opérateur ne peut pas être utilisé pour comparer des expressions retournées par la `TypeOf` opérateur. Au lieu de cela, vous devez utiliser le `Not` et `Is` opérateurs.  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant utilise à la fois le `Is` opérateur et la `IsNot` opérateur pour effectuer la même comparaison.  
  
 [!code-vb[VbVbalrOperators#29](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/isnot-operator_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Is (opérateur)](../../../visual-basic/language-reference/operators/is-operator.md)  
 [TypeOf (opérateur)](../../../visual-basic/language-reference/operators/typeof-operator.md)  
 [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)  
 [Guide pratique : déterminer si deux objets sont identiques](../../../visual-basic/programming-guide/language-features/operators-and-expressions/how-to-test-whether-two-objects-are-the-same.md)
