---
title: "?:, opérateur (référence C#)"
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- ?:_CSharpKeyword
- ?_CSharpKeyword
- :_CSharpKeyword
helpviewer_keywords:
- '?: operator [C#]'
- conditional operator (?:) [C#]
ms.assetid: e83a17f1-7500-48ba-8bee-2fbc4c847af4
caps.latest.revision: 
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: bbd434e02ece4843bab4ffded6877f81f622950c
ms.sourcegitcommit: ba765893e3efcece67d99fd6d5ce0074b050d1d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/02/2018
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
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Opérateurs C#](../../../csharp/language-reference/operators/index.md)  
 [if-else](../../../csharp/language-reference/keywords/if-else.md)  
 [Opérateurs ?. et ?](../../../csharp/language-reference/operators/null-conditional-operators.md)  
 [?? Opérateur](../../../csharp/language-reference/operators/null-conditional-operator.md)
