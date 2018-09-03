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
# <a name="-operator-c-reference"></a><span data-ttu-id="805f2-102">?:, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="805f2-102">?: Operator (C# Reference)</span></span>
<span data-ttu-id="805f2-103">L’opérateur conditionnel (`?:`), connu sous le nom d’opérateur conditionnel ternaire, retourne une valeur parmi deux, en fonction de la valeur d’une expression booléenne.</span><span class="sxs-lookup"><span data-stu-id="805f2-103">The conditional operator (`?:`), commonly known as the ternary conditional operator, returns one of two values depending on the value of a Boolean expression.</span></span> <span data-ttu-id="805f2-104">Voici la syntaxe de l'opérateur conditionnel.</span><span class="sxs-lookup"><span data-stu-id="805f2-104">Following is the syntax for the conditional operator.</span></span>  
  
```  
condition ? first_expression : second_expression;  
```  
  
## <a name="remarks"></a><span data-ttu-id="805f2-105">Notes</span><span class="sxs-lookup"><span data-stu-id="805f2-105">Remarks</span></span>  
 <span data-ttu-id="805f2-106">La `condition` est évaluée entre `true` ou `false`.</span><span class="sxs-lookup"><span data-stu-id="805f2-106">The `condition` must evaluate to `true` or `false`.</span></span> <span data-ttu-id="805f2-107">Si `condition` est `true`, `first_expression` est évaluée et devient le résultat.</span><span class="sxs-lookup"><span data-stu-id="805f2-107">If `condition` is `true`, `first_expression` is evaluated and becomes the result.</span></span> <span data-ttu-id="805f2-108">Si `condition` est `false`, `second_expression` est évaluée et devient le résultat.</span><span class="sxs-lookup"><span data-stu-id="805f2-108">If `condition` is `false`, `second_expression` is evaluated and becomes the result.</span></span> <span data-ttu-id="805f2-109">Seule une des deux expressions peut être évaluée.</span><span class="sxs-lookup"><span data-stu-id="805f2-109">Only one of the two expressions is evaluated.</span></span>  
  
 <span data-ttu-id="805f2-110">Soit le type de `first_expression` et `second_expression` doivent être identiques, soit une conversion implicite doit exister d'un type à un autre.</span><span class="sxs-lookup"><span data-stu-id="805f2-110">Either the type of `first_expression` and `second_expression` must be the same, or an implicit conversion must exist from one type to the other.</span></span>  
  
 <span data-ttu-id="805f2-111">Vous pouvez exprimer des calculs qui pourraient sinon requérir une construction `if-else` plus concise en utilisant l'opérateur conditionnel.</span><span class="sxs-lookup"><span data-stu-id="805f2-111">You can express calculations that might otherwise require an `if-else` construction more concisely by using the conditional operator.</span></span> <span data-ttu-id="805f2-112">Par exemple, le code suivant utilise en premier lieu une instruction `if`, puis un opérateur conditionnel pour classifier un entier positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="805f2-112">For example, the following code uses first an `if` statement and then a conditional operator to classify an integer as positive or negative.</span></span>  
  
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
  
 <span data-ttu-id="805f2-113">L'opérateur conditionnel est associatif sur sa droite.</span><span class="sxs-lookup"><span data-stu-id="805f2-113">The conditional operator is right-associative.</span></span> <span data-ttu-id="805f2-114">L'expression `a ? b : c ? d : e` est évaluée comme `a ? b : (c ? d : e)`, et non pas sous la forme `(a ? b : c) ? d : e`.</span><span class="sxs-lookup"><span data-stu-id="805f2-114">The expression `a ? b : c ? d : e` is evaluated as `a ? b : (c ? d : e)`, not as `(a ? b : c) ? d : e`.</span></span>  
  
 <span data-ttu-id="805f2-115">L'opérateur conditionnel ne peut pas être surchargé.</span><span class="sxs-lookup"><span data-stu-id="805f2-115">The conditional operator cannot be overloaded.</span></span>  
  
## <a name="example"></a><span data-ttu-id="805f2-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="805f2-116">Example</span></span>  
 [!code-csharp[csRefOperators#41](../../../csharp/language-reference/operators/codesnippet/CSharp/conditional-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="805f2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="805f2-117">See Also</span></span>

- [<span data-ttu-id="805f2-118">Référence C#</span><span class="sxs-lookup"><span data-stu-id="805f2-118">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="805f2-119">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="805f2-119">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="805f2-120">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="805f2-120">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="805f2-121">if-else</span><span class="sxs-lookup"><span data-stu-id="805f2-121">if-else</span></span>](../../../csharp/language-reference/keywords/if-else.md)  
- <span data-ttu-id="805f2-122">[Opérateurs ?. et ?[]](../../../csharp/language-reference/operators/null-conditional-operators.md)</span><span class="sxs-lookup"><span data-stu-id="805f2-122">[?. and ?[] Operators](../../../csharp/language-reference/operators/null-conditional-operators.md)</span></span>  
- [<span data-ttu-id="805f2-123">?? Opérateur</span><span class="sxs-lookup"><span data-stu-id="805f2-123">?? Operator</span></span>](../../../csharp/language-reference/operators/null-coalescing-operator.md)
