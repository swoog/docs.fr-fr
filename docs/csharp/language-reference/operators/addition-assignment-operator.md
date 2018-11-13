---
title: +=, opérateur (référence C#)
ms.date: 10/29/2018
f1_keywords:
- +=_CSharpKeyword
helpviewer_keywords:
- += operator [C#]
- addition assignment operator (+=) [C#]
- event subscription [C#]
ms.assetid: 9cdf97e6-331d-492b-85e1-3ec3171484e9
ms.openlocfilehash: ac9330e283cb58ae4e0ee7b644aa2c22bdf64c46
ms.sourcegitcommit: 3b1cb8467bd73dee854b604e306c0e7e3882d91a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "50192029"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="57e30-102">+=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="57e30-102">+= Operator (C# Reference)</span></span>

<span data-ttu-id="57e30-103">Opérateur d’assignation d’addition.</span><span class="sxs-lookup"><span data-stu-id="57e30-103">The addition assignment operator.</span></span>

<span data-ttu-id="57e30-104">Expression utilisant l’opérateur `+=`, par exemple</span><span class="sxs-lookup"><span data-stu-id="57e30-104">An expression using the `+=` operator, such as</span></span>

```csharp
x += y
```

<span data-ttu-id="57e30-105">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="57e30-105">is equivalent to</span></span>

```csharp
x = x + y
```

<span data-ttu-id="57e30-106">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="57e30-106">except that `x` is only evaluated once.</span></span>
  
<span data-ttu-id="57e30-107">Pour les types numériques, [l’opérateur d’addition](addition-operator.md) `+` calcule la somme de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="57e30-107">For numeric types, the [addition operator](addition-operator.md) `+` computes the sum of its operands.</span></span> <span data-ttu-id="57e30-108">Quand les deux opérandes ou l’un d’entre eux sont de type [chaîne](../keywords/string.md), il concatène les représentations sous forme de chaîne des opérandes.</span><span class="sxs-lookup"><span data-stu-id="57e30-108">If one or both operands is of type [string](../keywords/string.md), it concatenates the string representations of its operands.</span></span> <span data-ttu-id="57e30-109">Pour les types délégués, l’opérateur `+` retourne une nouvelle instance de délégué qui est la combinaison de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="57e30-109">For delegate types, the `+` operator returns a new delegate instance that is combination of its operands.</span></span>

<span data-ttu-id="57e30-110">Vous utilisez également l’opérateur `+=` pour spécifier une méthode de gestionnaire d’événements lorsque vous vous abonnez à un [événement](../keywords/event.md).</span><span class="sxs-lookup"><span data-stu-id="57e30-110">You also use the `+=` operator to specify an event handler method when you subscribe to an [event](../keywords/event.md).</span></span> <span data-ttu-id="57e30-111">Pour plus d’informations, consultez [Guide pratique pour s’abonner et annuler l’abonnement à des événements](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).</span><span class="sxs-lookup"><span data-stu-id="57e30-111">For more information, see [How to: Subscribe to and Unsubscribe from Events](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).</span></span>

<span data-ttu-id="57e30-112">L’exemple suivant illustre l’utilisation de l’opérateur `+=` :</span><span class="sxs-lookup"><span data-stu-id="57e30-112">The following example demonstrates the usage of the `+=` operator:</span></span>

[!code-csharp-interactive[+= examples](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddAndAssign)]

## <a name="operator-overloadability"></a><span data-ttu-id="57e30-113">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="57e30-113">Operator overloadability</span></span>

<span data-ttu-id="57e30-114">Si un type défini par l’utilisateur [surcharge](../keywords/operator.md) [l’opérateur d’addition](addition-operator.md) `+`, l’opérateur d’assignation d’addition `+=` est implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="57e30-114">If a user-defined type [overloads](../keywords/operator.md) the [addition operator](addition-operator.md) `+`, the addition assignment operator `+=` is implicitly overloaded.</span></span> <span data-ttu-id="57e30-115">Un type défini par l’utilisateur ne peut pas surcharger explicitement l’opérateur d’assignation d’addition.</span><span class="sxs-lookup"><span data-stu-id="57e30-115">A user-defined type cannot explicitly overload the addition assignment operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="57e30-116">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="57e30-116">C# language specification</span></span>

<span data-ttu-id="57e30-117">Pour plus d’informations, consultez les sections [Assignation composée](~/_csharplang/spec/expressions.md#compound-assignment) et [Assignation d’événement](~/_csharplang/spec/expressions.md#event-assignment) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="57e30-117">For more information, see the [Compound assignment](~/_csharplang/spec/expressions.md#compound-assignment) and [Event assignment](~/_csharplang/spec/expressions.md#event-assignment) sections of the [C# language specification](../language-specification/index.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57e30-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57e30-118">See also</span></span>

- [<span data-ttu-id="57e30-119">Référence C#</span><span class="sxs-lookup"><span data-stu-id="57e30-119">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="57e30-120">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="57e30-120">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="57e30-121">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="57e30-121">C# Operators</span></span>](index.md)
- [<span data-ttu-id="57e30-122">Événements</span><span class="sxs-lookup"><span data-stu-id="57e30-122">Events</span></span>](../../programming-guide/events/index.md)
- [<span data-ttu-id="57e30-123">Délégués</span><span class="sxs-lookup"><span data-stu-id="57e30-123">Delegates</span></span>](../../programming-guide/delegates/index.md)
