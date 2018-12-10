---
title: '%, opérateur (référence C#)'
ms.date: 09/04/2018
f1_keywords:
- '%_CSharpKeyword'
helpviewer_keywords:
- remainder operator [C#]
- '% operator [C#]'
ms.assetid: 3b74f4f9-fd9c-45e7-84fa-c8d71a0dfad7
ms.openlocfilehash: cd6d49b69d40f3b45aae060d46b58632dc8448f8
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53144197"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="d3d96-102">%, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="d3d96-102">% Operator (C# Reference)</span></span>

<span data-ttu-id="d3d96-103">L’opérateur de reste `%` calcule le reste après avoir divisé son premier opérande par son second opérande.</span><span class="sxs-lookup"><span data-stu-id="d3d96-103">The remainder operator `%` computes the remainder after dividing its first operand by its second operand.</span></span>

<span data-ttu-id="d3d96-104">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `%`.</span><span class="sxs-lookup"><span data-stu-id="d3d96-104">User-defined types can [overload](../keywords/operator.md) the `%` operator.</span></span> <span data-ttu-id="d3d96-105">Quand `%` est surchargé, l’[opérateur d’assignation de reste](remainder-assignment-operator.md) `%=` est également surchargé implicitement.</span><span class="sxs-lookup"><span data-stu-id="d3d96-105">When the `%` is overloaded, the [remainder assignment operator](remainder-assignment-operator.md) `%=` is also implicitly overloaded.</span></span>

<span data-ttu-id="d3d96-106">Tous les types numériques prennent en charge l’opérateur de reste.</span><span class="sxs-lookup"><span data-stu-id="d3d96-106">All numeric types support the remainder operator.</span></span>

## <a name="integer-remainder"></a><span data-ttu-id="d3d96-107">Reste entier</span><span class="sxs-lookup"><span data-stu-id="d3d96-107">Integer remainder</span></span>
  
<span data-ttu-id="d3d96-108">Pour les opérandes entiers, le résultat de `a % b` est la valeur produite par `a - (a / b) * b`.</span><span class="sxs-lookup"><span data-stu-id="d3d96-108">For the integer operands, the result of `a % b` is the value produced by `a - (a / b) * b`.</span></span> <span data-ttu-id="d3d96-109">Le signe du reste non nul est le même que celui du premier opérande, comme le montre l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="d3d96-109">The sign of the non-zero remainder is the same as that of the first operand, as the following example shows:</span></span>

[!code-csharp-interactive[integer remainder](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#1)]

## <a name="floating-point-remainder"></a><span data-ttu-id="d3d96-110">Reste à virgule flottante</span><span class="sxs-lookup"><span data-stu-id="d3d96-110">Floating-point remainder</span></span>

<span data-ttu-id="d3d96-111">En ce qui concerne les opérandes [float](../keywords/float.md) et [double](../keywords/double.md), le résultat de `x % y` pour le `x` et le `y` finis est la valeur `z` afin que</span><span class="sxs-lookup"><span data-stu-id="d3d96-111">For the [float](../keywords/float.md) and [double](../keywords/double.md) operands, the result of `x % y` for the finite `x` and `y` is the value `z` such that</span></span>

- <span data-ttu-id="d3d96-112">Le signe de `z`, s’il est différent de zéro, soit identique au signe de `x`</span><span class="sxs-lookup"><span data-stu-id="d3d96-112">the sign of `z`, if non-zero, is the same as the sign of `x`;</span></span>
- <span data-ttu-id="d3d96-113">La valeur absolue de `z` soit la valeur produite par `|x| - n * |y|`, où `n` représente le plus grand entier possible inférieur ou égal à `|x| / |y|`, et où `|x|` et `|y|` sont les valeurs absolues de `x` et `y`, respectivement</span><span class="sxs-lookup"><span data-stu-id="d3d96-113">the absolute value of `z` is the value produced by `|x| - n * |y|` where `n` is the largest possible integer that is less than or equal to `|x| / |y|` and `|x|` and `|y|` are the absolute values of `x` and `y`, respectively.</span></span>

<span data-ttu-id="d3d96-114">Pour plus d’informations sur le comportement de l’opérateur `%` avec des opérandes non finis, consultez la section [Opérateur de reste](~/_csharplang/spec/expressions.md#remainder-operator) dans la [Spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="d3d96-114">For information about the behavior of the `%` operator with non-finite operands, see the [Remainder operator](~/_csharplang/spec/expressions.md#remainder-operator) section of the [C# language specification](../language-specification/index.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d3d96-115">Cette méthode de calcul du reste est analogue à celle utilisée pour les opérandes entiers. Toutefois, elle ne suit pas la norme IEEE 754.</span><span class="sxs-lookup"><span data-stu-id="d3d96-115">This method of computing the remainder is analogous to that used for integer operands, but differs from the IEEE 754.</span></span> <span data-ttu-id="d3d96-116">Si l’opération de reste doit être conforme à la norme IEEE 754, utilisez la méthode <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="d3d96-116">If you need the remainder operation that complies with the IEEE 754, use the <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType> method.</span></span>

<span data-ttu-id="d3d96-117">L’exemple suivant illustre le comportement de l’opérateur de reste pour les opérandes `float` et `double` :</span><span class="sxs-lookup"><span data-stu-id="d3d96-117">The following example demonstrates the behavior of the remainder operator for `float` and `double` operands:</span></span>

[!code-csharp-interactive[float and double remainder](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#2)]

<span data-ttu-id="d3d96-118">Notez les erreurs d’arrondi qui peuvent être associées aux types à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d3d96-118">Note the round-off errors that can be associated with the floating-point types.</span></span>

<span data-ttu-id="d3d96-119">Pour les opérandes [decimal](../keywords/decimal.md), l’opérateur de reste `%` équivaut à l’[opérateur de reste](<xref:System.Decimal.op_Modulus(System.Decimal,System.Decimal)>) de type <xref:System.Decimal?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="d3d96-119">For the [decimal](../keywords/decimal.md) operands, the remainder operator `%` is equivalent to the [remainder operator](<xref:System.Decimal.op_Modulus(System.Decimal,System.Decimal)>) of the <xref:System.Decimal?displayProperty=nameWithType> type.</span></span>

## <a name="see-also"></a><span data-ttu-id="d3d96-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3d96-120">See also</span></span>

- [<span data-ttu-id="d3d96-121">Référence C#</span><span class="sxs-lookup"><span data-stu-id="d3d96-121">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="d3d96-122">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="d3d96-122">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="d3d96-123">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="d3d96-123">C# Operators</span></span>](index.md)
- <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType>
- <xref:System.Math.DivRem%2A?displayProperty=nameWithType>
