---
title: '>> opérateur - Référence C#'
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- '>>_CSharpKeyword'
helpviewer_keywords:
- '>> operator [C#]'
- right shift operator (>>) [C#]
ms.assetid: a07f8679-d318-4ef8-b38b-65903efb8056
ms.openlocfilehash: 809cd2cab29d3378892ea224cf846e9d0909b073
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219722"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="48319-102">>>, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="48319-102">>> operator (C# Reference)</span></span>

<span data-ttu-id="48319-103">L’opérateur de décalage vers la droite `>>` décale son premier opérande vers la droite du nombre de bits défini par son deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="48319-103">The right-shift operator `>>` shifts its first operand right by the number of bits defined by its second operand.</span></span> <span data-ttu-id="48319-104">Tous les types d’entiers acceptent l’opérateur `>>`.</span><span class="sxs-lookup"><span data-stu-id="48319-104">All integer types support the `>>` operator.</span></span> <span data-ttu-id="48319-105">Cependant, le deuxième opérande doit être de type [int](../keywords/int.md) ou d’un type pour lequel une [conversion numérique implicite](../keywords/implicit-numeric-conversions-table.md) vers `int` est prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="48319-105">However, the type of the second operand must be [int](../keywords/int.md) or a type that has a [predefined implicit numeric conversion](../keywords/implicit-numeric-conversions-table.md) to `int`.</span></span>

<span data-ttu-id="48319-106">L’opération de décalage vers la droite ignore les bits d’ordre inférieur.</span><span class="sxs-lookup"><span data-stu-id="48319-106">The right-shift operation discards the low-order bits.</span></span> <span data-ttu-id="48319-107">Les positions de bits vides d’ordre supérieur sont définies en fonction du type du premier opérande comme suit :</span><span class="sxs-lookup"><span data-stu-id="48319-107">The high-order empty bit positions are set based on the type of the first operand as follows:</span></span>

- <span data-ttu-id="48319-108">si le premier opérande est de type [int](../keywords/int.md) ou [long](../keywords/long.md), l’opérateur de décalage vers la droite effectue un décalage **arithmétique** : la valeur du bit le plus significatif (le bit de signe) du premier opérande est propagée vers les positions des bits vides d’ordre supérieur.</span><span class="sxs-lookup"><span data-stu-id="48319-108">If the first operand is of type [int](../keywords/int.md) or [long](../keywords/long.md), the right-shift operator performs an **arithmetic** shift: the value of the most significant bit (the sign bit) of the first operand is propagated to the high-order empty bit positions.</span></span> <span data-ttu-id="48319-109">Autrement dit, les positions de bits vides d’ordre supérieur sont définies sur zéro si le premier opérande n’est pas négatif et sur un s’il est négatif.</span><span class="sxs-lookup"><span data-stu-id="48319-109">That is, the high-order empty bit positions are set to zero if the first operand is non-negative and set to one if it's negative.</span></span>

- <span data-ttu-id="48319-110">Si le premier opérande est de type [uint](../keywords/uint.md) ou [ulong](../keywords/ulong.md), l’opérateur de décalage vers la droite effectue un décalage **logique** : les positions des bits vides d’ordre supérieur sont toujours définies sur zéro.</span><span class="sxs-lookup"><span data-stu-id="48319-110">If the first operand is of type [uint](../keywords/uint.md) or [ulong](../keywords/ulong.md), the right-shift operator performs a **logical** shift: the high-order empty bit positions are always set to zero.</span></span>

<span data-ttu-id="48319-111">L’exemple suivant illustre ce comportement :</span><span class="sxs-lookup"><span data-stu-id="48319-111">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[right shift example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShift)]

## <a name="shift-count"></a><span data-ttu-id="48319-112">Valeur du décalage</span><span class="sxs-lookup"><span data-stu-id="48319-112">Shift count</span></span>

<span data-ttu-id="48319-113">Pour l’expression `x >> count`, la valeur réelle du décalage varie selon le type de `x` comme suit :</span><span class="sxs-lookup"><span data-stu-id="48319-113">For the expression `x >> count`, the actual shift count depends on the type of `x` as follows:</span></span>

- <span data-ttu-id="48319-114">si le type `x` est [int ](../keywords/int.md) ou [uint](../keywords/uint.md), la valeur du décalage est donnée par les *cinq* bits d’ordre inférieur du deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="48319-114">If the type of `x` is [int](../keywords/int.md) or [uint](../keywords/uint.md), the shift count is given by the low-order *five* bits of the second operand.</span></span> <span data-ttu-id="48319-115">La valeur de décalage est donc calculée à partir de `count & 0x1F` (ou de `count & 0b_1_1111`).</span><span class="sxs-lookup"><span data-stu-id="48319-115">That is, the shift count is computed from `count & 0x1F` (or `count & 0b_1_1111`).</span></span>

- <span data-ttu-id="48319-116">Si le type `x` est [long ](../keywords/long.md) ou [ulong](../keywords/ulong.md), la valeur du décalage est donnée par les *six* bits d’ordre inférieur du deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="48319-116">If the type of `x` is [long](../keywords/long.md) or [ulong](../keywords/ulong.md), the shift count is given by the low-order *six* bits of the second operand.</span></span> <span data-ttu-id="48319-117">La valeur de décalage est donc calculée à partir de `count & 0x3F` (ou de `count & 0b_11_1111`).</span><span class="sxs-lookup"><span data-stu-id="48319-117">That is, the shift count is computed from `count & 0x3F` (or `count & 0b_11_1111`).</span></span>

<span data-ttu-id="48319-118">L’exemple suivant illustre ce comportement :</span><span class="sxs-lookup"><span data-stu-id="48319-118">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[shift count example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShiftByLargeCount)]

## <a name="remarks"></a><span data-ttu-id="48319-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="48319-119">Remarks</span></span>

<span data-ttu-id="48319-120">Les opérations de décalage ne provoquent jamais de dépassements de capacité et donnent les mêmes résultats dans des contextes [checked and unchecked](../keywords/checked-and-unchecked.md).</span><span class="sxs-lookup"><span data-stu-id="48319-120">Shift operations never cause overflows and produce the same results in [checked and unchecked](../keywords/checked-and-unchecked.md) contexts.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="48319-121">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="48319-121">Operator overloadability</span></span>

<span data-ttu-id="48319-122">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `>>`.</span><span class="sxs-lookup"><span data-stu-id="48319-122">User-defined types can [overload](../keywords/operator.md) the `>>` operator.</span></span> <span data-ttu-id="48319-123">Si un type `T` défini par l’utilisateur surcharge l’opérateur `>>`, le premier opérande doit être de type `T` et le deuxième de type `int`.</span><span class="sxs-lookup"><span data-stu-id="48319-123">If a user-defined type `T` overloads the `>>` operator, the type of the first operand must be `T` and the type of the second operand must be `int`.</span></span> <span data-ttu-id="48319-124">Quand l’opérateur `>>` est surchargé, [l’opérateur d’assignation de décalage vers la droite](right-shift-assignment-operator.md) `>>=` est aussi implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="48319-124">When the `>>` operator is overloaded, the [right-shift assignment operator](right-shift-assignment-operator.md) `>>=` is also implicitly overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="48319-125">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="48319-125">C# language specification</span></span>

<span data-ttu-id="48319-126">Pour plus d’informations, voir la section [Opérateurs de décalage](~/_csharplang/spec/expressions.md#shift-operators) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="48319-126">For more information, see the [Shift operators](~/_csharplang/spec/expressions.md#shift-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="48319-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48319-127">See also</span></span>

- [<span data-ttu-id="48319-128">Référence C#</span><span class="sxs-lookup"><span data-stu-id="48319-128">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="48319-129">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="48319-129">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="48319-130">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="48319-130">C# operators</span></span>](index.md)
- [<span data-ttu-id="48319-131"><< opérateur</span><span class="sxs-lookup"><span data-stu-id="48319-131"><< operator</span></span>](left-shift-operator.md)