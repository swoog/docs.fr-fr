---
title: '&amp;, opérateur (référence C#)'
ms.date: 10/29/2018
f1_keywords:
- '&_CSharpKeyword'
helpviewer_keywords:
- bitwise AND operator [C#]
- ampersand operator (&) [C#]
- '& operator [C#]'
- AND operator (&) [C#]
ms.assetid: afa346d5-90ec-4b1f-a2c8-3881f018741d
ms.openlocfilehash: a8f76ded0ef9f8e8099838a903d90f1695324991
ms.sourcegitcommit: b5cd9d5d3b75a5537fc9ad8a3f085f0bb1845ee0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "43510976"
---
# <a name="amp-operator-c-reference"></a><span data-ttu-id="08ebc-102">&amp;, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="08ebc-102">&amp; Operator (C# Reference)</span></span>

<span data-ttu-id="08ebc-103">L’opérateur `&` est pris en charge sous deux formes : un opérateur address-of unaire ou un opérateur logique binaire.</span><span class="sxs-lookup"><span data-stu-id="08ebc-103">The `&` operator is supported in two forms: a unary address-of operator or a binary logical operator.</span></span>

## <a name="unary-address-of-operator"></a><span data-ttu-id="08ebc-104">address-of, opérateur unaire</span><span class="sxs-lookup"><span data-stu-id="08ebc-104">Unary address-of operator</span></span>

<span data-ttu-id="08ebc-105">L’opérateur unaire `&` retourne l’adresse de son opérande.</span><span class="sxs-lookup"><span data-stu-id="08ebc-105">The unary `&` operator returns the address of its operand.</span></span> <span data-ttu-id="08ebc-106">Pour plus d’informations, consultez [Guide pratique pour obtenir l’adresse d’une variable](../../programming-guide/unsafe-code-pointers/how-to-obtain-the-address-of-a-variable.md)</span><span class="sxs-lookup"><span data-stu-id="08ebc-106">For more information, see [How to: obtain the address of a variable](../../programming-guide/unsafe-code-pointers/how-to-obtain-the-address-of-a-variable.md).</span></span>

<span data-ttu-id="08ebc-107">L’opérateur address-of `&` nécessite un contexte [unsafe](../keywords/unsafe.md).</span><span class="sxs-lookup"><span data-stu-id="08ebc-107">The address-of operator `&` requires [unsafe](../keywords/unsafe.md) context.</span></span>

## <a name="integer-logical-bitwise-and-operator"></a><span data-ttu-id="08ebc-108">Opérateur logique AND au niveau du bit pour les types entier</span><span class="sxs-lookup"><span data-stu-id="08ebc-108">Integer logical bitwise AND operator</span></span>

<span data-ttu-id="08ebc-109">Pour les types entier, l’opérateur `&` calcule l’opération logique AND au niveau du bit de ses opérandes :</span><span class="sxs-lookup"><span data-stu-id="08ebc-109">For integer types, the `&` operator computes the logical bitwise AND of its operands:</span></span>

[!code-csharp-interactive[integer logical bitwise AND](~/samples/snippets/csharp/language-reference/operators/AndOperatorExamples.cs#IntegerOperands)]

> [!NOTE]
> <span data-ttu-id="08ebc-110">L’exemple précédent utilise les littéraux binaires [introduits dans C# 7.0](../../whats-new/csharp-7.md#numeric-literal-syntax-improvements) et [améliorés dans C# 7.2](../../whats-new/csharp-7-2.md#leading-underscores-in-numeric-literals).</span><span class="sxs-lookup"><span data-stu-id="08ebc-110">The preceding example uses the binary literals [introduced in C# 7.0](../../whats-new/csharp-7.md#numeric-literal-syntax-improvements) and [enhanced in C# 7.2](../../whats-new/csharp-7-2.md#leading-underscores-in-numeric-literals).</span></span>

<span data-ttu-id="08ebc-111">Étant donné que les opérations sur les types entier sont généralement autorisées sur les types énumération, l’opérateur `&` prend également en charge les opérandes [enum](../keywords/enum.md).</span><span class="sxs-lookup"><span data-stu-id="08ebc-111">Because operations on integer types are generally allowed on enumeration types, the `&` operator also supports [enum](../keywords/enum.md) operands.</span></span>

## <a name="boolean-logical-and-operator"></a><span data-ttu-id="08ebc-112">Opérateur logique booléen AND</span><span class="sxs-lookup"><span data-stu-id="08ebc-112">Boolean logical AND operator</span></span>

<span data-ttu-id="08ebc-113">Pour les opérandes [bool](../keywords/bool.md), l’opérateur `&` calcule l’opération logique AND de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="08ebc-113">For [bool](../keywords/bool.md) operands, the `&` operator computes the logical AND of its operands.</span></span> <span data-ttu-id="08ebc-114">Le résultat de `x & y` est `true` si `x` et `y` sont `true`.</span><span class="sxs-lookup"><span data-stu-id="08ebc-114">The result of `x & y` is `true` if both `x` and `y` are `true`.</span></span> <span data-ttu-id="08ebc-115">Sinon, le résultat est `false`.</span><span class="sxs-lookup"><span data-stu-id="08ebc-115">Otherwise, the result is `false`.</span></span>

<span data-ttu-id="08ebc-116">L’opérateur `&` évalue les deux opérandes, même si le premier opérande prend la valeur `false`. Le résultat est donc `false` quelle que soit la valeur du deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="08ebc-116">The `&` operator evaluates both operands even if the first operand evaluates to `false`, so that the result must be `false` regardless of the value of the second operand.</span></span> <span data-ttu-id="08ebc-117">L’exemple suivant illustre ce comportement :</span><span class="sxs-lookup"><span data-stu-id="08ebc-117">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[bool logical AND](~/samples/snippets/csharp/language-reference/operators/AndOperatorExamples.cs#BooleanOperands)]

<span data-ttu-id="08ebc-118">[L’opérateur conditionnel AND](conditional-and-operator.md) `&&` calcule également l’opération logique AND de ses opérandes, mais évalue uniquement le deuxième opérande si le premier prend la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="08ebc-118">The [conditional AND operator](conditional-and-operator.md) `&&` also computes the logical AND of its operands, but evaluates the second operand only if the first operand evaluates to `true`.</span></span>

<span data-ttu-id="08ebc-119">Pour les opérandes bool nullables, le comportement de l’opérateur `&` est cohérent avec la logique ternaire de SQL.</span><span class="sxs-lookup"><span data-stu-id="08ebc-119">For nullable bool operands, the behavior of the `&` operator is consistent with SQL's three-valued logic.</span></span> <span data-ttu-id="08ebc-120">Pour plus d’informations, consultez la section [Type bool?](../../programming-guide/nullable-types/using-nullable-types.md#the-bool-type) de l’article [Utilisation de types nullable](../../programming-guide/nullable-types/using-nullable-types.md).</span><span class="sxs-lookup"><span data-stu-id="08ebc-120">For more information, see the [The bool? type](../../programming-guide/nullable-types/using-nullable-types.md#the-bool-type) section of the [Using nullable types](../../programming-guide/nullable-types/using-nullable-types.md) article.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="08ebc-121">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="08ebc-121">Operator overloadability</span></span>

<span data-ttu-id="08ebc-122">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur binaire `&`.</span><span class="sxs-lookup"><span data-stu-id="08ebc-122">User-defined types can [overload](../keywords/operator.md) the binary `&` operator.</span></span> <span data-ttu-id="08ebc-123">Quand un opérateur binaire `&` est surchargé, [l’opérateur d’assignation AND](and-assignment-operator.md) `&=` est aussi implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="08ebc-123">When a binary `&` operator is overloaded, the [AND assignment operator](and-assignment-operator.md) `&=` is also implicitly overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="08ebc-124">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="08ebc-124">C# language specification</span></span>

<span data-ttu-id="08ebc-125">Pour plus d’informations, consultez les sections [Opérateur address-of](~/_csharplang/spec/unsafe-code.md#the-address-of-operator) et [Opérateurs logiques](~/_csharplang/spec/expressions.md#logical-operators) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="08ebc-125">For more information, see [The address-of operator](~/_csharplang/spec/unsafe-code.md#the-address-of-operator) and [Logical operators](~/_csharplang/spec/expressions.md#logical-operators) sections of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="08ebc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08ebc-126">See also</span></span>

- [<span data-ttu-id="08ebc-127">Référence C#</span><span class="sxs-lookup"><span data-stu-id="08ebc-127">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="08ebc-128">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="08ebc-128">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="08ebc-129">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="08ebc-129">C# Operators</span></span>](index.md)
- [<span data-ttu-id="08ebc-130">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="08ebc-130">Pointer types</span></span>](../../programming-guide/unsafe-code-pointers/pointer-types.md)
- [<span data-ttu-id="08ebc-131">|, opérateur</span><span class="sxs-lookup"><span data-stu-id="08ebc-131">| operator</span></span>](or-operator.md)
- [<span data-ttu-id="08ebc-132">^, opérateur</span><span class="sxs-lookup"><span data-stu-id="08ebc-132">^ operator</span></span>](xor-operator.md)
- [<span data-ttu-id="08ebc-133">~, opérateur</span><span class="sxs-lookup"><span data-stu-id="08ebc-133">~ operator</span></span>](bitwise-complement-operator.md)
- [<span data-ttu-id="08ebc-134">&&, opérateur</span><span class="sxs-lookup"><span data-stu-id="08ebc-134">&& operator</span></span>](conditional-and-operator.md)
