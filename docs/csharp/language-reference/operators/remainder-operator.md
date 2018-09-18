---
title: '%, opérateur (référence C#)'
ms.date: 09/04/2018
f1_keywords:
- '%_CSharpKeyword'
helpviewer_keywords:
- remainder operator [C#]
- '% operator [C#]'
ms.assetid: 3b74f4f9-fd9c-45e7-84fa-c8d71a0dfad7
ms.openlocfilehash: 9cd2f7ad3856feb34667686979c942ecb21887c2
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45645916"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="d67ab-102">%, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="d67ab-102">% Operator (C# Reference)</span></span>

<span data-ttu-id="d67ab-103">L’opérateur de reste `%` calcule le reste après avoir divisé son premier opérande par son second opérande.</span><span class="sxs-lookup"><span data-stu-id="d67ab-103">The remainder operator `%` computes the remainder after dividing its first operand by its second operand.</span></span> <span data-ttu-id="d67ab-104">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `%`.</span><span class="sxs-lookup"><span data-stu-id="d67ab-104">User-defined types can [overload](../keywords/operator.md) the `%` operator.</span></span> <span data-ttu-id="d67ab-105">Quand `%` est surchargé, l’[opérateur d’assignation de reste](remainder-assignment-operator.md) `%=` est également surchargé implicitement.</span><span class="sxs-lookup"><span data-stu-id="d67ab-105">When the `%` is overloaded, the [remainder assignment operator](remainder-assignment-operator.md) `%=` is also implicitly overloaded.</span></span>

<span data-ttu-id="d67ab-106">Tous les types numériques prennent en charge l’opérateur de reste.</span><span class="sxs-lookup"><span data-stu-id="d67ab-106">All numeric types support the remainder operator.</span></span>

## <a name="integer-remainder"></a><span data-ttu-id="d67ab-107">Reste entier</span><span class="sxs-lookup"><span data-stu-id="d67ab-107">Integer remainder</span></span>
  
<span data-ttu-id="d67ab-108">Pour les opérandes entiers, le résultat de `a % b` est la valeur produite par `a - (a / b) * b`.</span><span class="sxs-lookup"><span data-stu-id="d67ab-108">For the integer operands, the result of `a % b` is the value produced by `a - (a / b) * b`.</span></span> <span data-ttu-id="d67ab-109">Le signe du reste non nul est le même que celui du premier opérande, comme le montre l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="d67ab-109">The sign of the non-zero remainder is the same as that of the first operand, as the following example shows:</span></span>

[!code-csharp-interactive[integer remainder](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#1)]

## <a name="floating-point-remainder"></a><span data-ttu-id="d67ab-110">Reste à virgule flottante</span><span class="sxs-lookup"><span data-stu-id="d67ab-110">Floating-point remainder</span></span>

<span data-ttu-id="d67ab-111">En ce qui concerne les opérandes [float](../keywords/float.md) et [double](../keywords/double.md), le résultat de `x % y` pour le `x` et le `y` finis est la valeur `z` afin que</span><span class="sxs-lookup"><span data-stu-id="d67ab-111">For the [float](../keywords/float.md) and [double](../keywords/double.md) operands, the result of `x % y` for the finite `x` and `y` is the value `z` such that</span></span>

- <span data-ttu-id="d67ab-112">Le signe de `z`, s’il est différent de zéro, soit identique au signe de `x`</span><span class="sxs-lookup"><span data-stu-id="d67ab-112">the sign of `z`, if non-zero, is the same as the sign of `x`;</span></span>
- <span data-ttu-id="d67ab-113">La valeur absolue de `z` soit la valeur produite par `|x| - n * |y|`, où `n` représente le plus grand entier possible inférieur ou égal à `|x| / |y|`, et où `|x|` et `|y|` sont les valeurs absolues de `x` et `y`, respectivement</span><span class="sxs-lookup"><span data-stu-id="d67ab-113">the absolute value of `z` is the value produced by `|x| - n * |y|` where `n` is the largest possible integer that is less than or equal to `|x| / |y|` and `|x|` and `|y|` are the absolute values of `x` and `y`, respectively.</span></span>

<span data-ttu-id="d67ab-114">Pour plus d’informations sur le comportement de l’opérateur `%` dans le cas d’opérandes non finis, consultez la section [Opérateur de reste](/dotnet/csharp/language-reference/language-specification/expressions#remainder-operator) dans la [Spécification du langage C#](/dotnet/csharp/language-reference/language-specification/index).</span><span class="sxs-lookup"><span data-stu-id="d67ab-114">For information about behavior of the `%` operator in case of non-finite operands, see the [Remainder operator](/dotnet/csharp/language-reference/language-specification/expressions#remainder-operator) section of the [C# language specification](/dotnet/csharp/language-reference/language-specification/index).</span></span>

> [!NOTE]
> <span data-ttu-id="d67ab-115">Cette méthode de calcul du reste est analogue à celle utilisée pour les opérandes entiers. Toutefois, elle ne suit pas la norme IEEE 754.</span><span class="sxs-lookup"><span data-stu-id="d67ab-115">This method of computing the remainder is analogous to that used for integer operands, but differs from the IEEE 754.</span></span> <span data-ttu-id="d67ab-116">Si l’opération de reste doit être conforme à la norme IEEE 754, utilisez la méthode <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="d67ab-116">If you need the remainder operation that complies with the IEEE 754, use the <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType> method.</span></span>

<span data-ttu-id="d67ab-117">L’exemple suivant illustre le comportement de l’opérateur de reste pour les opérandes `float` et `double` :</span><span class="sxs-lookup"><span data-stu-id="d67ab-117">The following example demonstrates the behavior of the remainder operator for `float` and `double` operands:</span></span>

[!code-csharp-interactive[float and double remainder](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#2)]

<span data-ttu-id="d67ab-118">Notez les erreurs d’arrondi qui peuvent être associées aux types à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d67ab-118">Note the round-off errors that can be associated with the floating-point types.</span></span>

<span data-ttu-id="d67ab-119">Pour les opérandes [decimal](../keywords/decimal.md), l’opérateur de reste `%` équivaut à l’[opérateur de reste](<xref:System.Decimal.op_Modulus(System.Decimal,System.Decimal)>) de type <xref:System.Decimal?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="d67ab-119">For the [decimal](../keywords/decimal.md) operands, the remainder operator `%` is equivalent to the [remainder operator](<xref:System.Decimal.op_Modulus(System.Decimal,System.Decimal)>) of the <xref:System.Decimal?displayProperty=nameWithType> type.</span></span>

## <a name="see-also"></a><span data-ttu-id="d67ab-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d67ab-120">See also</span></span>

- [<span data-ttu-id="d67ab-121">Référence C#</span><span class="sxs-lookup"><span data-stu-id="d67ab-121">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="d67ab-122">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="d67ab-122">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="d67ab-123">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="d67ab-123">C# Operators</span></span>](index.md)
- <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType>
- <xref:System.Math.DivRem%2A?displayProperty=nameWithType>
