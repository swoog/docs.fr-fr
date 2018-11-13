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
ms.openlocfilehash: 3e45ff6eaaefa5829c3ed9415abe1a12b7a1d069
ms.sourcegitcommit: 4bca8f7e172fd019ef437a4803bf5895c6bc4781
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "50980620"
---
# <a name="-operator-c-reference"></a>?:, opérateur (référence C#)

L’opérateur conditionnel (`?:`), connu sous le nom d’opérateur conditionnel ternaire, retourne une valeur parmi deux, en fonction de la valeur d’une expression booléenne. Voici la syntaxe de l'opérateur conditionnel.  

```csharp
condition ? first_expression : second_expression;  
```

À compter de C# 7.2, `first_expression` et `second_expression` peuvent être des [expressions](https://github.com/dotnet/csharplang/blob/master/proposals/csharp-7.2/conditional-ref.md) `ref` :

```csharp
ref condition ? ref first_expression : ref second_expression;  
```

Le résultat peut être assigné à une variable `ref` ou `ref readonly`, ou à une variable sans modificateur.

## <a name="remarks"></a>Notes

La `condition` est évaluée entre `true` ou `false`. Si `condition` est `true`, `first_expression` est évaluée et devient le résultat. Si `condition` est `false`, `second_expression` est évaluée et devient le résultat. Seule une des deux expressions peut être évaluée. Cela est particulièrement important pour les expressions où le résultat est un `ref`, car ce qui suit est valide :

```csharp
ref (storage != null) ? ref storage[3] : ref defaultValue;
```

La référence à `storage` n’est pas évaluée quand `storage` est null.

Si le résultat est une valeur, soit `first_expression` et `second_expression` doivent être du même type, soit une conversion implicite doit exister d’un type à l’autre. Si le résultat est un `ref`, `first_expression` et `second_expression` doivent être du même type.

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

L’exemple suivant montre l’opérateur conditionnel dont le résultat est une valeur :

[!code-csharp[csRefOperators?:](~/samples/snippets/csharp/language-reference/operators/ConditionalExamples.cs#ConditionalValue)]

L’alternative suivante montre l’opérateur conditionnel où le résultat est une référence :

[!code-csharp[csRefOperatorsRef?:](~/samples/snippets/csharp/language-reference/operators/ConditionalExamples.cs#ConditionalRef)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Opérateurs C#](../../../csharp/language-reference/operators/index.md)  
- [if-else](../../../csharp/language-reference/keywords/if-else.md)  
- [Opérateurs ?. et ?[]](../../../csharp/language-reference/operators/null-conditional-operators.md)  
- [?? Opérateur](../../../csharp/language-reference/operators/null-coalescing-operator.md)
