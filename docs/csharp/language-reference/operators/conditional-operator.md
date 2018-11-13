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
# <a name="-operator-c-reference"></a><span data-ttu-id="f91bb-102">?:, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="f91bb-102">?: Operator (C# Reference)</span></span>

<span data-ttu-id="f91bb-103">L’opérateur conditionnel (`?:`), connu sous le nom d’opérateur conditionnel ternaire, retourne une valeur parmi deux, en fonction de la valeur d’une expression booléenne.</span><span class="sxs-lookup"><span data-stu-id="f91bb-103">The conditional operator (`?:`), commonly known as the ternary conditional operator, returns one of two values depending on the value of a Boolean expression.</span></span> <span data-ttu-id="f91bb-104">Voici la syntaxe de l'opérateur conditionnel.</span><span class="sxs-lookup"><span data-stu-id="f91bb-104">Following is the syntax for the conditional operator.</span></span>  

```csharp
condition ? first_expression : second_expression;  
```

<span data-ttu-id="f91bb-105">À compter de C# 7.2, `first_expression` et `second_expression` peuvent être des [expressions](https://github.com/dotnet/csharplang/blob/master/proposals/csharp-7.2/conditional-ref.md) `ref` :</span><span class="sxs-lookup"><span data-stu-id="f91bb-105">Beginning with C# 7.2, the `first_expression` and `second_expression` my be [`ref` expressions](https://github.com/dotnet/csharplang/blob/master/proposals/csharp-7.2/conditional-ref.md):</span></span>

```csharp
ref condition ? ref first_expression : ref second_expression;  
```

<span data-ttu-id="f91bb-106">Le résultat peut être assigné à une variable `ref` ou `ref readonly`, ou à une variable sans modificateur.</span><span class="sxs-lookup"><span data-stu-id="f91bb-106">The result may be assigned to a `ref` or `ref readonly` variable, or to a variable with neither modifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="f91bb-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f91bb-107">Remarks</span></span>

<span data-ttu-id="f91bb-108">La `condition` est évaluée entre `true` ou `false`.</span><span class="sxs-lookup"><span data-stu-id="f91bb-108">The `condition` must evaluate to `true` or `false`.</span></span> <span data-ttu-id="f91bb-109">Si `condition` est `true`, `first_expression` est évaluée et devient le résultat.</span><span class="sxs-lookup"><span data-stu-id="f91bb-109">If `condition` is `true`, `first_expression` is evaluated and becomes the result.</span></span> <span data-ttu-id="f91bb-110">Si `condition` est `false`, `second_expression` est évaluée et devient le résultat.</span><span class="sxs-lookup"><span data-stu-id="f91bb-110">If `condition` is `false`, `second_expression` is evaluated and becomes the result.</span></span> <span data-ttu-id="f91bb-111">Seule une des deux expressions peut être évaluée.</span><span class="sxs-lookup"><span data-stu-id="f91bb-111">Only one of the two expressions is evaluated.</span></span> <span data-ttu-id="f91bb-112">Cela est particulièrement important pour les expressions où le résultat est un `ref`, car ce qui suit est valide :</span><span class="sxs-lookup"><span data-stu-id="f91bb-112">This is particularly important for expressions where the result is a `ref`, as the following is valid:</span></span>

```csharp
ref (storage != null) ? ref storage[3] : ref defaultValue;
```

<span data-ttu-id="f91bb-113">La référence à `storage` n’est pas évaluée quand `storage` est null.</span><span class="sxs-lookup"><span data-stu-id="f91bb-113">The reference to `storage` is not evaluated when `storage` is null.</span></span>

<span data-ttu-id="f91bb-114">Si le résultat est une valeur, soit `first_expression` et `second_expression` doivent être du même type, soit une conversion implicite doit exister d’un type à l’autre.</span><span class="sxs-lookup"><span data-stu-id="f91bb-114">When the result is a value, the type of `first_expression` and `second_expression` must be the same, or there must be an implicit conversion from one type to the other.</span></span> <span data-ttu-id="f91bb-115">Si le résultat est un `ref`, `first_expression` et `second_expression` doivent être du même type.</span><span class="sxs-lookup"><span data-stu-id="f91bb-115">When the result is a `ref`, the type of `first_expression` and `second_expression` must be the same.</span></span>

<span data-ttu-id="f91bb-116">Vous pouvez exprimer des calculs qui pourraient sinon requérir une construction `if-else` plus concise en utilisant l'opérateur conditionnel.</span><span class="sxs-lookup"><span data-stu-id="f91bb-116">You can express calculations that might otherwise require an `if-else` construction more concisely by using the conditional operator.</span></span> <span data-ttu-id="f91bb-117">Par exemple, le code suivant utilise en premier lieu une instruction `if`, puis un opérateur conditionnel pour classifier un entier positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="f91bb-117">For example, the following code uses first an `if` statement and then a conditional operator to classify an integer as positive or negative.</span></span>

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

<span data-ttu-id="f91bb-118">L'opérateur conditionnel est associatif sur sa droite.</span><span class="sxs-lookup"><span data-stu-id="f91bb-118">The conditional operator is right-associative.</span></span> <span data-ttu-id="f91bb-119">L'expression `a ? b : c ? d : e` est évaluée comme `a ? b : (c ? d : e)`, et non pas sous la forme `(a ? b : c) ? d : e`.</span><span class="sxs-lookup"><span data-stu-id="f91bb-119">The expression `a ? b : c ? d : e` is evaluated as `a ? b : (c ? d : e)`, not as `(a ? b : c) ? d : e`.</span></span>  
  
<span data-ttu-id="f91bb-120">L'opérateur conditionnel ne peut pas être surchargé.</span><span class="sxs-lookup"><span data-stu-id="f91bb-120">The conditional operator cannot be overloaded.</span></span>
  
## <a name="example"></a><span data-ttu-id="f91bb-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="f91bb-121">Example</span></span>

<span data-ttu-id="f91bb-122">L’exemple suivant montre l’opérateur conditionnel dont le résultat est une valeur :</span><span class="sxs-lookup"><span data-stu-id="f91bb-122">The following example shows the conditional operator whose result is a value:</span></span>

[!code-csharp[csRefOperators?:](~/samples/snippets/csharp/language-reference/operators/ConditionalExamples.cs#ConditionalValue)]

<span data-ttu-id="f91bb-123">L’alternative suivante montre l’opérateur conditionnel où le résultat est une référence :</span><span class="sxs-lookup"><span data-stu-id="f91bb-123">The following alternative shows the conditional operator where the result is a reference:</span></span>

[!code-csharp[csRefOperatorsRef?:](~/samples/snippets/csharp/language-reference/operators/ConditionalExamples.cs#ConditionalRef)]

## <a name="see-also"></a><span data-ttu-id="f91bb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f91bb-124">See Also</span></span>

- [<span data-ttu-id="f91bb-125">Référence C#</span><span class="sxs-lookup"><span data-stu-id="f91bb-125">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="f91bb-126">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="f91bb-126">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="f91bb-127">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="f91bb-127">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="f91bb-128">if-else</span><span class="sxs-lookup"><span data-stu-id="f91bb-128">if-else</span></span>](../../../csharp/language-reference/keywords/if-else.md)  
- <span data-ttu-id="f91bb-129">[Opérateurs ?. et ?[]](../../../csharp/language-reference/operators/null-conditional-operators.md)</span><span class="sxs-lookup"><span data-stu-id="f91bb-129">[?. and ?[] Operators](../../../csharp/language-reference/operators/null-conditional-operators.md)</span></span>  
- [<span data-ttu-id="f91bb-130">?? Opérateur</span><span class="sxs-lookup"><span data-stu-id="f91bb-130">?? Operator</span></span>](../../../csharp/language-reference/operators/null-coalescing-operator.md)
