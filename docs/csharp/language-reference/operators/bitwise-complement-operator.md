---
title: ~, opérateur - Référence C#
ms.custom: seodec18
ms.date: 11/05/2018
f1_keywords:
- ~_CSharpKeyword
helpviewer_keywords:
- tilde (~) one's complement operator [C#]
- ~ operator [C#]
- ~ [C#], bitwise complement operator
- bitwise complement operator [C#]
ms.assetid: 11bc078a-50e2-4d7e-9896-67ef669dc602
ms.openlocfilehash: 57e5baee423c0b5d9292d0ad4cbf909646eb3a38
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53235717"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="7d106-102">~, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="7d106-102">~ Operator (C# Reference)</span></span>

<span data-ttu-id="7d106-103">L’opérateur de complément au niveau du bit `~` est un opérateur unaire qui produit un complément au niveau du bit de son opérande en inversant chaque bit.</span><span class="sxs-lookup"><span data-stu-id="7d106-103">The bitwise complement operator `~` is a unary operator that produces a bitwise complement of its operand by reversing each bit.</span></span> <span data-ttu-id="7d106-104">Tous les types d’entiers acceptent l’opérateur `~`.</span><span class="sxs-lookup"><span data-stu-id="7d106-104">All integer types support the `~` operator.</span></span>

> [!NOTE]
> <span data-ttu-id="7d106-105">Le symbole `~` est également utilisé pour déclarer des finaliseurs.</span><span class="sxs-lookup"><span data-stu-id="7d106-105">The `~` symbol is also used to declare finalizers.</span></span> <span data-ttu-id="7d106-106">Pour plus d’informations, consultez [Finaliseurs](../../programming-guide/classes-and-structs/destructors.md).</span><span class="sxs-lookup"><span data-stu-id="7d106-106">For more information, see [Finalizers](../../programming-guide/classes-and-structs/destructors.md).</span></span>

<span data-ttu-id="7d106-107">L’exemple suivant illustre l’utilisation de l’opérateur `~` :</span><span class="sxs-lookup"><span data-stu-id="7d106-107">The following example demonstrates the usage of the `~` operator:</span></span>

[!code-csharp-interactive[bitwise NOT](~/samples/snippets/csharp/language-reference/operators/BitwiseComplementExamples.cs#Example)]

> [!NOTE]
> <span data-ttu-id="7d106-108">L’exemple précédent utilise les littéraux binaires [introduits dans C# 7.0](../../whats-new/csharp-7.md#numeric-literal-syntax-improvements) et [améliorés dans C# 7.2](../../whats-new/csharp-7-2.md#leading-underscores-in-numeric-literals).</span><span class="sxs-lookup"><span data-stu-id="7d106-108">The preceding example uses the binary literals [introduced in C# 7.0](../../whats-new/csharp-7.md#numeric-literal-syntax-improvements) and [enhanced  in C# 7.2](../../whats-new/csharp-7-2.md#leading-underscores-in-numeric-literals).</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="7d106-109">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="7d106-109">Operator overloadability</span></span>

<span data-ttu-id="7d106-110">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `~`.</span><span class="sxs-lookup"><span data-stu-id="7d106-110">User-defined types can [overload](../keywords/operator.md) the `~` operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="7d106-111">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="7d106-111">C# language specification</span></span>

<span data-ttu-id="7d106-112">Pour plus d’informations, voir la section [Opérateur de complément au niveau du bit](~/_csharplang/spec/expressions.md#bitwise-complement-operator) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="7d106-112">For more information, see the [Bitwise complement operator](~/_csharplang/spec/expressions.md#bitwise-complement-operator) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7d106-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d106-113">See also</span></span>

- [<span data-ttu-id="7d106-114">Référence C#</span><span class="sxs-lookup"><span data-stu-id="7d106-114">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="7d106-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="7d106-115">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="7d106-116">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="7d106-116">C# Operators</span></span>](index.md)
- [<span data-ttu-id="7d106-117">Finaliseurs</span><span class="sxs-lookup"><span data-stu-id="7d106-117">Finalizers</span></span>](../../programming-guide/classes-and-structs/destructors.md)
- [<span data-ttu-id="7d106-118">&, opérateur</span><span class="sxs-lookup"><span data-stu-id="7d106-118">& operator</span></span>](and-operator.md)
- [<span data-ttu-id="7d106-119">|, opérateur</span><span class="sxs-lookup"><span data-stu-id="7d106-119">| operator</span></span>](or-operator.md)
- [<span data-ttu-id="7d106-120">^, opérateur</span><span class="sxs-lookup"><span data-stu-id="7d106-120">^ operator</span></span>](xor-operator.md)
