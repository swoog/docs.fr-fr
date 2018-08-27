---
title: '||, opérateur (référence C#)'
ms.date: 07/20/2015
f1_keywords:
- '||_CSharpKeyword'
helpviewer_keywords:
- logical OR operator [C#]
- conditional-OR operator (||) [C#]
- '|| operator [C#]'
ms.assetid: 7d442d8e-400d-421f-b4d2-034bf82bcbdc
ms.openlocfilehash: 58e5fd72a3748e7af0894093fc461c4efb543608
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2018
ms.locfileid: "42925538"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="a49fc-102">||, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="a49fc-102">|| Operator (C# Reference)</span></span>
<span data-ttu-id="a49fc-103">L’opérateur conditionnel OR (`||`) effectue une opération OR logique de ses opérandes `bool`.</span><span class="sxs-lookup"><span data-stu-id="a49fc-103">The conditional-OR operator (`||`) performs a logical-OR of its `bool` operands.</span></span> <span data-ttu-id="a49fc-104">Si le premier opérande prend la valeur `true`, le deuxième opérande n’est pas évalué.</span><span class="sxs-lookup"><span data-stu-id="a49fc-104">If the first operand evaluates to `true`, the second operand isn't evaluated.</span></span> <span data-ttu-id="a49fc-105">Si le premier opérande prend la valeur `false`, le deuxième opérateur détermine si l’expression OR dans son ensemble prend la valeur `true` ou `false`.</span><span class="sxs-lookup"><span data-stu-id="a49fc-105">If the first operand evaluates to `false`, the second operator determines whether the OR expression as a whole evaluates to `true` or `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a49fc-106">Notes</span><span class="sxs-lookup"><span data-stu-id="a49fc-106">Remarks</span></span>  
 <span data-ttu-id="a49fc-107">L’opération</span><span class="sxs-lookup"><span data-stu-id="a49fc-107">The operation</span></span>  
  
```csharp  
x || y  
```  
  
 <span data-ttu-id="a49fc-108">correspond à l’opération</span><span class="sxs-lookup"><span data-stu-id="a49fc-108">corresponds to the operation</span></span>  
  
```csharp  
x | y  
```  
  
 <span data-ttu-id="a49fc-109">sauf si `x` a la valeur `true`, auquel cas `y` n’est pas évalué, car l’opération OR a la valeur `true`, indépendamment de la valeur d’`y`.</span><span class="sxs-lookup"><span data-stu-id="a49fc-109">except that if `x` is `true`, `y` is not evaluated because the OR operation is `true` regardless of the value of `y`.</span></span> <span data-ttu-id="a49fc-110">Ce concept est connu sous le nom d’évaluation de « court-circuit ».</span><span class="sxs-lookup"><span data-stu-id="a49fc-110">This concept is known as "short-circuit" evaluation.</span></span>  
  
 <span data-ttu-id="a49fc-111">L’opérateur OR conditionnel ne peut pas être surchargé, mais les surcharges des opérateurs logiques normaux et des opérateurs [true](../../../csharp/language-reference/keywords/true.md) et [false](../../../csharp/language-reference/keywords/false.md) sont, avec certaines restrictions, également considérées comme des surcharges des opérateurs logiques conditionnels.</span><span class="sxs-lookup"><span data-stu-id="a49fc-111">The conditional-OR operator cannot be overloaded, but overloads of the regular logical operators and the [true](../../../csharp/language-reference/keywords/true.md) and [false](../../../csharp/language-reference/keywords/false.md) operators are, with certain restrictions, also considered to be overloads of the conditional logical operators.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a49fc-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="a49fc-112">Example</span></span>  
 <span data-ttu-id="a49fc-113">Dans les exemples suivants, l’expression qui utilise `||` évalue seulement le premier opérande.</span><span class="sxs-lookup"><span data-stu-id="a49fc-113">In the following examples, the expression that uses `||` evaluates only the first operand.</span></span> <span data-ttu-id="a49fc-114">L’expression qui utilise `|` évalue les deux opérandes.</span><span class="sxs-lookup"><span data-stu-id="a49fc-114">The expression that uses `|` evaluates both operands.</span></span> <span data-ttu-id="a49fc-115">Dans le deuxième exemple, une exception runtime se produit si les deux opérandes sont évalués.</span><span class="sxs-lookup"><span data-stu-id="a49fc-115">In the second example, a run-time exception occurs if both operands are evaluated.</span></span>  
  
 [!code-csharp[csRefOperators#52](../../../csharp/language-reference/operators/codesnippet/CSharp/conditional-or-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="a49fc-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a49fc-116">See Also</span></span>

- [<span data-ttu-id="a49fc-117">Référence C#</span><span class="sxs-lookup"><span data-stu-id="a49fc-117">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="a49fc-118">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="a49fc-118">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="a49fc-119">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="a49fc-119">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
