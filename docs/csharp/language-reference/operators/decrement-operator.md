---
title: --, opérateur - Référence C#
ms.custom: seodec18
ms.date: 11/26/2018
f1_keywords:
- --_CSharpKeyword
helpviewer_keywords:
- -- operator [C#]
- decrement operator (--) [C#]
ms.assetid: 6b9cfe86-63c7-421f-9379-c9690fea8720
ms.openlocfilehash: 4fba014e8dabc13cd874e17f23515dc29d93f24b
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236919"
---
# <a name="---operator-c-reference"></a><span data-ttu-id="b9653-102">--, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="b9653-102">-- Operator (C# Reference)</span></span>

<span data-ttu-id="b9653-103">L’opérateur de décrémentation unaire `--` décrémente son opérande de 1.</span><span class="sxs-lookup"><span data-stu-id="b9653-103">The unary decrement operator `--` decrements its operand by 1.</span></span> <span data-ttu-id="b9653-104">Il est pris en charge sous deux formes : l’opérateur de décrémentation suffixé, `x--`, et l’opérateur de décrémentation préfixé, `--x`.</span><span class="sxs-lookup"><span data-stu-id="b9653-104">It's supported in two forms: the postfix decrement operator, `x--`, and the prefix decrement operator, `--x`.</span></span>

## <a name="postfix-decrement-operator"></a><span data-ttu-id="b9653-105">Opérateur de décrémentation suffixé</span><span class="sxs-lookup"><span data-stu-id="b9653-105">Postfix decrement operator</span></span>

<span data-ttu-id="b9653-106">Le résultat de `x--` est la valeur de `x` *avant* l’opération, comme le montre l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="b9653-106">The result of `x--` is the value of `x` *before* the operation, as the following example shows:</span></span>

[!code-csharp-interactive[postfix decrement](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PostfixDecrement)]

## <a name="prefix-decrement-operator"></a><span data-ttu-id="b9653-107">Opérateur de décrémentation préfixé</span><span class="sxs-lookup"><span data-stu-id="b9653-107">Prefix decrement operator</span></span>

<span data-ttu-id="b9653-108">Le résultat de `--x` est la valeur de `x` *après* l’opération, comme le montre l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="b9653-108">The result of `--x` is the value of `x` *after* the operation, as the following example shows:</span></span>

[!code-csharp-interactive[prefix decrement](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PrefixDecrement)]

## <a name="remarks"></a><span data-ttu-id="b9653-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b9653-109">Remarks</span></span>

<span data-ttu-id="b9653-110">L’opérateur de décrémentation est prédéfini pour toutes les [types intégraux](../keywords/integral-types-table.md) (y compris le type [char](../keywords/char.md)), les [types à virgule flottante](../keywords/floating-point-types-table.md) et n’importe quel type [enum](../keywords/enum.md).</span><span class="sxs-lookup"><span data-stu-id="b9653-110">The decrement operator is predefined for all [integral types](../keywords/integral-types-table.md) (including the [char](../keywords/char.md) type), [floating-point types](../keywords/floating-point-types-table.md), and any [enum](../keywords/enum.md) type.</span></span>

<span data-ttu-id="b9653-111">Un opérande de l’opérateur de décrémentation doit être une variable, un accès [propriété](../../programming-guide/classes-and-structs/properties.md) ou un accès [indexeur](../../../csharp/programming-guide/indexers/index.md).</span><span class="sxs-lookup"><span data-stu-id="b9653-111">An operand of the decrement operator must be a variable, a [property](../../programming-guide/classes-and-structs/properties.md) access, or an [indexer](../../../csharp/programming-guide/indexers/index.md) access.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="b9653-112">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="b9653-112">Operator overloadability</span></span>

<span data-ttu-id="b9653-113">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `--`.</span><span class="sxs-lookup"><span data-stu-id="b9653-113">User-defined types can [overload](../keywords/operator.md) the `--` operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="b9653-114">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="b9653-114">C# language specification</span></span>

<span data-ttu-id="b9653-115">Pour plus d’informations, voir les sections [Opérateurs d’incrémentation et de décrémentation](~/_csharplang/spec/expressions.md#postfix-increment-and-decrement-operators) et [Opérateurs d’incrémentation et de décrémentation préfixés](~/_csharplang/spec/expressions.md#prefix-increment-and-decrement-operators) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="b9653-115">For more information, see the [Postfix increment and decrement operators](~/_csharplang/spec/expressions.md#postfix-increment-and-decrement-operators) and [Prefix increment and decrement operators](~/_csharplang/spec/expressions.md#prefix-increment-and-decrement-operators) sections of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b9653-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9653-116">See also</span></span>

- [<span data-ttu-id="b9653-117">Référence C#</span><span class="sxs-lookup"><span data-stu-id="b9653-117">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="b9653-118">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b9653-118">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="b9653-119">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="b9653-119">C# Operators</span></span>](index.md)
- [<span data-ttu-id="b9653-120">++, opérateur</span><span class="sxs-lookup"><span data-stu-id="b9653-120">++ Operator</span></span>](increment-operator.md)
- [<span data-ttu-id="b9653-121">Guide pratique : Incrémenter et décrémenter des pointeurs</span><span class="sxs-lookup"><span data-stu-id="b9653-121">How to: increment and decrement pointers</span></span>](../../programming-guide/unsafe-code-pointers/how-to-increment-and-decrement-pointers.md)
