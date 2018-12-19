---
title: /, opérateur - Référence C#
ms.custom: seodec18
ms.date: 12/13/2018
f1_keywords:
- /_CSharpKeyword
helpviewer_keywords:
- / operator [C#]
- division operator [C#]
ms.assetid: d155e496-678f-4efa-bebe-2bd08da2c5af
ms.openlocfilehash: 45bcd64b60e7d13f389064faefeda815ea1f32c9
ms.sourcegitcommit: d6e419f9d9cd7e8f21ebf5acde6d016c16332579
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2018
ms.locfileid: "53286531"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="df134-102">/, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="df134-102">/ Operator (C# Reference)</span></span>

<span data-ttu-id="df134-103">L’opérateur de division `/` divise son premier opérande par son deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="df134-103">The division operator `/` divides its first operand by its second operand.</span></span> <span data-ttu-id="df134-104">Tous les types numériques prennent en charge l’opérateur de division.</span><span class="sxs-lookup"><span data-stu-id="df134-104">All numeric types support the division operator.</span></span>

## <a name="integer-division"></a><span data-ttu-id="df134-105">Division d'entier</span><span class="sxs-lookup"><span data-stu-id="df134-105">Integer division</span></span>

<span data-ttu-id="df134-106">Pour les opérandes des types entiers, le résultat de l’opérateur `/` est de type entier et égal au quotient de deux opérandes arrondis vers le zéro :</span><span class="sxs-lookup"><span data-stu-id="df134-106">For the operands of integer types, the result of the `/` operator is of an integer type and equals the quotient of the two operands rounded towards zero:</span></span>

[!code-csharp-interactive[integer division](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#Integer)]

<span data-ttu-id="df134-107">Pour obtenir le quotient de deux opérandes comme un nombre à virgule flottante, utilisez le type `float`, `double` ou `decimal` :</span><span class="sxs-lookup"><span data-stu-id="df134-107">To obtain the quotient of the two operands as a floating-point number, use the `float`, `double`, or `decimal` type:</span></span>

[!code-csharp-interactive[integer as floating-point division](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#IntegerAsFloatingPoint)]

## <a name="floating-point-division"></a><span data-ttu-id="df134-108">Division à virgule flottante</span><span class="sxs-lookup"><span data-stu-id="df134-108">Floating-point division</span></span>

<span data-ttu-id="df134-109">Pour les types `float`, `double` et `decimal`, le résultat de l’opérateur `/` est le quotient de deux opérandes :</span><span class="sxs-lookup"><span data-stu-id="df134-109">For the `float`, `double`, and `decimal` types, the result of the `/` operator is the quotient of the two operands:</span></span>

[!code-csharp-interactive[floating-point division](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#FloatingPoint)]

<span data-ttu-id="df134-110">Si l’un des opérandes est `decimal`, un autre opérande ne peut être `float` ni `double`, car ni `float` ni `double` ne sont implicitement convertibles en `decimal`.</span><span class="sxs-lookup"><span data-stu-id="df134-110">If one of the operands is `decimal`, another operand can be neither `float` nor `double`, because neither `float` nor `double` is implicitly convertible to `decimal`.</span></span> <span data-ttu-id="df134-111">Vous devez convertir explicitement l’opérande `float` ou `double` en type `decimal`.</span><span class="sxs-lookup"><span data-stu-id="df134-111">You must explicitly convert the `float` or `double` operand to the `decimal` type.</span></span> <span data-ttu-id="df134-112">Pour plus d’informations sur les conversions implicites entre des types numériques, consultez [Tableau des conversions numériques implicites](../keywords/implicit-numeric-conversions-table.md).</span><span class="sxs-lookup"><span data-stu-id="df134-112">For more information about implicit conversions between numeric types, see [Implicit numeric conversions table](../keywords/implicit-numeric-conversions-table.md).</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="df134-113">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="df134-113">Operator overloadability</span></span>

<span data-ttu-id="df134-114">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `/`.</span><span class="sxs-lookup"><span data-stu-id="df134-114">User-defined types can [overload](../keywords/operator.md) the `/` operator.</span></span> <span data-ttu-id="df134-115">Quand l’opérateur `/` est surchargé, [l’opérateur d’assignation de division](division-assignment-operator.md) `/=` est aussi implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="df134-115">When the `/` operator is overloaded, the [division assignment operator](division-assignment-operator.md) `/=` is also implicitly overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="df134-116">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="df134-116">C# language specification</span></span>

<span data-ttu-id="df134-117">Pour plus d’informations, voir la section [Opérateur de division](~/_csharplang/spec/expressions.md#division-operator) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="df134-117">For more information, see the [Division operator](~/_csharplang/spec/expressions.md#division-operator) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="df134-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df134-118">See also</span></span>

- [<span data-ttu-id="df134-119">Référence C#</span><span class="sxs-lookup"><span data-stu-id="df134-119">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="df134-120">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="df134-120">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="df134-121">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="df134-121">C# Operators</span></span>](index.md)
- [<span data-ttu-id="df134-122">%, opérateur</span><span class="sxs-lookup"><span data-stu-id="df134-122">% Operator</span></span>](remainder-operator.md)
