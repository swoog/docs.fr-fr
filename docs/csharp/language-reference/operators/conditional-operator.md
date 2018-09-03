---
title: ?:, opérateur (référence C#)
ms.date: 07/20/2015
f1_keywords:
- ?:_CSharpKeyword
- ?_CSharpKeyword
- :_CSharpKeyword
helpviewer_keywords:
- '?: operator [C#]'
- conditional operator (?:) [C#]
ms.assetid: e83a17f1-7500-48ba-8bee-2fbc4c847af4
ms.openlocfilehash: 150149453a67d8e5319461266865cb25be180347
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43421502"
---
# <a name="-operator-c-reference"></a>?:, opérateur (référence C#)
L’opérateur conditionnel (`?:`), connu sous le nom d’opérateur conditionnel ternaire, retourne une valeur parmi deux, en fonction de la valeur d’une expression booléenne. Voici la syntaxe de l'opérateur conditionnel.  
  
```  
condition ? first_expression : second_expression;  
```  
  
## <a name="remarks"></a>Notes  
 La `condition` est évaluée entre `true` ou `false`. Si `condition` est `true`, `first_expression` est évaluée et devient le résultat. Si `condition` est `false`, `second_expression` est évaluée et devient le résultat. Seule une des deux expressions peut être évaluée.  
  
 Soit le type de `first_expression` et `second_expression` doivent être identiques, soit une conversion implicite doit exister d'un type à un autre.  
  
 Vous pouvez exprimer des calculs qui pourraient sinon requérir une construction `if-else` plus concise en utilisant l'opérateur conditionnel. Par exemple, le code suivant utilise en premier lieu une instruction `if`, puis un opérateur conditionnel pour classifier un entier positif ou négatif.  
  
```csharp
int input = Convert.ToInt32(Console.ReadLine());  
string classify;  
  
// if-else construction.  
if (input > 0)  
    classify = "positive";  
else  
    classify = "negative";  
  
// ?: conditional operator.  
classify = (input > 0) ? "positive" : "negative";  
```  
  
 L'opérateur conditionnel est associatif sur sa droite. L'expression `a ? b : c ? d : e` est évaluée comme `a ? b : (c ? d : e)`, et non pas sous la forme `(a ? b : c) ? d : e`.  
  
 L'opérateur conditionnel ne peut pas être surchargé.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#41](../../../csharp/language-reference/operators/codesnippet/CSharp/conditional-operator_1.cs)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Opérateurs C#](../../../csharp/language-reference/operators/index.md)  
- [if-else](../../../csharp/language-reference/keywords/if-else.md)  
- [Opérateurs ?. et ?[]](../../../csharp/language-reference/operators/null-conditional-operators.md)  
- [?? Opérateur](../../../csharp/language-reference/operators/null-coalescing-operator.md)
