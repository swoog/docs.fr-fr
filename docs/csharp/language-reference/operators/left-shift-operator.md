---
title: <<, opérateur - Référence C#
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- <<_CSharpKeyword
helpviewer_keywords:
- left shift operator (<<) [C#]
- << operator [C#]
ms.assetid: a654eb56-1ff7-4bf3-9064-b631be0cdccc
ms.openlocfilehash: deea2d0f720ba7f096e65c67378586bc88f24673
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219435"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="0687c-102">\<\<, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="0687c-102">\<\< operator (C# Reference)</span></span>

<span data-ttu-id="0687c-103">L’opérateur de décalage vers la gauche `<<` décale son premier opérande vers la gauche du nombre de bits défini par son deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="0687c-103">The left-shift operator `<<` shifts its first operand left by the number of bits defined by its second operand.</span></span> <span data-ttu-id="0687c-104">Tous les types d’entiers acceptent l’opérateur `<<`.</span><span class="sxs-lookup"><span data-stu-id="0687c-104">All integer types support the `<<` operator.</span></span> <span data-ttu-id="0687c-105">Cependant, le deuxième opérande doit être de type [int](../keywords/int.md) ou d’un type pour lequel une [conversion numérique implicite](../keywords/implicit-numeric-conversions-table.md) vers `int` est prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="0687c-105">However, the type of the second operand must be [int](../keywords/int.md) or a type that has a [predefined implicit numeric conversion](../keywords/implicit-numeric-conversions-table.md) to `int`.</span></span>

<span data-ttu-id="0687c-106">Les bits d’ordre supérieur qui sont en dehors de la plage du type de résultat sont ignorés, et les positions de bits vides d’ordre inférieur sont définies sur zéro, comme le montre l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="0687c-106">The high-order bits that are outside the range of the result type are discarded, and the low-order empty bit positions are set to zero, as the following example shows:</span></span>

[!code-csharp-interactive[left shift example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#LeftShift)]

## <a name="shift-count"></a><span data-ttu-id="0687c-107">Valeur du décalage</span><span class="sxs-lookup"><span data-stu-id="0687c-107">Shift count</span></span>

<span data-ttu-id="0687c-108">Pour l’expression `x << count`, la valeur réelle du décalage varie selon le type de `x` comme suit :</span><span class="sxs-lookup"><span data-stu-id="0687c-108">For the expression `x << count`, the actual shift count depends on the type of `x` as follows:</span></span>

- <span data-ttu-id="0687c-109">si le type `x` est [int ](../keywords/int.md) ou [uint](../keywords/uint.md), la valeur du décalage est donnée par les *cinq* bits d’ordre inférieur du deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="0687c-109">If the type of `x` is [int](../keywords/int.md) or [uint](../keywords/uint.md), the shift count is given by the low-order *five* bits of the second operand.</span></span> <span data-ttu-id="0687c-110">La valeur de décalage est donc calculée à partir de `count & 0x1F` (ou de `count & 0b_1_1111`).</span><span class="sxs-lookup"><span data-stu-id="0687c-110">That is, the shift count is computed from `count & 0x1F` (or `count & 0b_1_1111`).</span></span>

- <span data-ttu-id="0687c-111">si le type `x` est [long ](../keywords/long.md) ou [ulong](../keywords/ulong.md), la valeur du décalage est donnée par les *six* bits d’ordre inférieur du deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="0687c-111">If the type of `x` is [long](../keywords/long.md) or [ulong](../keywords/ulong.md), the shift count is given by the low-order *six* bits of the second operand.</span></span> <span data-ttu-id="0687c-112">La valeur de décalage est donc calculée à partir de `count & 0x3F` (ou de `count & 0b_11_1111`).</span><span class="sxs-lookup"><span data-stu-id="0687c-112">That is, the shift count is computed from `count & 0x3F` (or `count & 0b_11_1111`).</span></span>

<span data-ttu-id="0687c-113">L’exemple suivant illustre ce comportement :</span><span class="sxs-lookup"><span data-stu-id="0687c-113">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[shift count example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#LeftShiftByLargeCount)]

## <a name="remarks"></a><span data-ttu-id="0687c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0687c-114">Remarks</span></span>

<span data-ttu-id="0687c-115">Les opérations de décalage ne provoquent jamais de dépassements de capacité et donnent les mêmes résultats dans des contextes [checked and unchecked](../keywords/checked-and-unchecked.md).</span><span class="sxs-lookup"><span data-stu-id="0687c-115">Shift operations never cause overflows and produce the same results in [checked and unchecked](../keywords/checked-and-unchecked.md) contexts.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="0687c-116">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="0687c-116">Operator overloadability</span></span>

<span data-ttu-id="0687c-117">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `<<`.</span><span class="sxs-lookup"><span data-stu-id="0687c-117">User-defined types can [overload](../keywords/operator.md) the `<<` operator.</span></span> <span data-ttu-id="0687c-118">Si un type `T` défini par l’utilisateur surcharge l’opérateur `<<`, le premier opérande doit être de type `T` et le deuxième de type `int`.</span><span class="sxs-lookup"><span data-stu-id="0687c-118">If a user-defined type `T` overloads the `<<` operator, the type of the first operand must be `T` and the type of the second operand must be `int`.</span></span> <span data-ttu-id="0687c-119">Quand l’opérateur `<<` est surchargé, [l’opérateur d’assignation de décalage vers la gauche](left-shift-assignment-operator.md) `<<=` est aussi implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="0687c-119">When the `<<` operator is overloaded, the [left-shift assignment operator](left-shift-assignment-operator.md) `<<=` is also implicitly overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="0687c-120">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="0687c-120">C# language specification</span></span>

<span data-ttu-id="0687c-121">Pour plus d’informations, voir la section [Opérateurs de décalage](~/_csharplang/spec/expressions.md#shift-operators) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="0687c-121">For more information, see the [Shift operators](~/_csharplang/spec/expressions.md#shift-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0687c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0687c-122">See also</span></span>

- [<span data-ttu-id="0687c-123">Référence C#</span><span class="sxs-lookup"><span data-stu-id="0687c-123">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="0687c-124">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0687c-124">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="0687c-125">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="0687c-125">C# Operators</span></span>](index.md)
- [<span data-ttu-id="0687c-126">>> opérateur</span><span class="sxs-lookup"><span data-stu-id="0687c-126">>> operator</span></span>](right-shift-operator.md)
