---
title: +=, opérateur (référence C#)
ms.date: 10/22/2018
f1_keywords:
- +=_CSharpKeyword
helpviewer_keywords:
- += operator [C#]
- addition assignment operator (+=) [C#]
- event subscription [C#]
ms.assetid: 9cdf97e6-331d-492b-85e1-3ec3171484e9
ms.openlocfilehash: ee335e3e2e7d352d4e26b802bad2b08a05c666ab
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50192029"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="24102-102">+=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="24102-102">+= Operator (C# Reference)</span></span>

<span data-ttu-id="24102-103">Opérateur d’assignation d’addition.</span><span class="sxs-lookup"><span data-stu-id="24102-103">The addition assignment operator.</span></span>

<span data-ttu-id="24102-104">Expression utilisant l’opérateur `+=`, par exemple</span><span class="sxs-lookup"><span data-stu-id="24102-104">An expression using the `+=` operator, such as</span></span>  

```csharp
x += y
```  

<span data-ttu-id="24102-105">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="24102-105">is equivalent to</span></span>  

```csharp
x = x + y
```  

<span data-ttu-id="24102-106">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="24102-106">except that `x` is only evaluated once.</span></span>
  
<span data-ttu-id="24102-107">Pour les types numériques, [l’opérateur d’addition](addition-operator.md) `+` calcule la somme de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="24102-107">For numeric types, the [addition operator](addition-operator.md) `+` computes the sum of its operands.</span></span> <span data-ttu-id="24102-108">Quand les deux opérandes ou l’un d’entre eux sont de type [chaîne](../keywords/string.md), il concatène les représentations sous forme de chaîne des opérandes.</span><span class="sxs-lookup"><span data-stu-id="24102-108">If one or both operands is of type [string](../keywords/string.md), it concatenates the string representations of its operands.</span></span> <span data-ttu-id="24102-109">Pour les types délégués, l’opérateur `+` retourne une nouvelle instance de délégué qui est la combinaison de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="24102-109">For delegate types, the `+` operator returns a new delegate instance that is combination of its operands.</span></span>

<span data-ttu-id="24102-110">Si un type défini par l’utilisateur [surcharge](../keywords/operator.md) [l’opérateur d’addition](addition-operator.md) `+`, l’opérateur d’assignation d’addition `+=` est implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="24102-110">If a user-defined type [overloads](../keywords/operator.md) the [addition operator](addition-operator.md) `+`, the addition assignment operator `+=` is implicitly overloaded.</span></span>

<span data-ttu-id="24102-111">Vous utilisez également l’opérateur `+=` pour spécifier une méthode de gestionnaire d’événements lorsque vous vous abonnez à un [événement](../keywords/event.md).</span><span class="sxs-lookup"><span data-stu-id="24102-111">You also use the `+=` operator to specify an event handler method when you subscribe to an [event](../keywords/event.md).</span></span> <span data-ttu-id="24102-112">Pour plus d’informations, consultez [Guide pratique pour s’abonner et annuler l’abonnement à des événements](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).</span><span class="sxs-lookup"><span data-stu-id="24102-112">For more information, see [How to: Subscribe to and Unsubscribe from Events](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).</span></span>

<span data-ttu-id="24102-113">L’exemple suivant illustre l’utilisation de l’opérateur `+=` :</span><span class="sxs-lookup"><span data-stu-id="24102-113">The following example demonstrates the usage of the `+=` operator:</span></span>

[!code-csharp-interactive[+= examples](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddAndAssign)]
  
## <a name="see-also"></a><span data-ttu-id="24102-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24102-114">See also</span></span>

- [<span data-ttu-id="24102-115">Référence C#</span><span class="sxs-lookup"><span data-stu-id="24102-115">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="24102-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="24102-116">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="24102-117">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="24102-117">C# Operators</span></span>](index.md)
- [<span data-ttu-id="24102-118">Événements</span><span class="sxs-lookup"><span data-stu-id="24102-118">Events</span></span>](../../programming-guide/events/index.md)
- [<span data-ttu-id="24102-119">Délégués</span><span class="sxs-lookup"><span data-stu-id="24102-119">Delegates</span></span>](../../programming-guide/delegates/index.md)
