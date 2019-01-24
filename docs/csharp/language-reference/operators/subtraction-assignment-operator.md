---
title: -=, opérateur - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- -=_CSharpKeyword
helpviewer_keywords:
- subtraction assignment operator (-=) [C#]
- -= operator (subtraction assignment ) [C#]
ms.assetid: 05c7d68a-423f-4de8-891b-cf24e8fb6ed7
ms.openlocfilehash: 3b6890be4460a599a5d2f5f5f6ee1627be933f0b
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333328"
---
# <a name="--operator-c-reference"></a><span data-ttu-id="fb3f2-102">-=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="fb3f2-102">-= operator (C# Reference)</span></span>

<span data-ttu-id="fb3f2-103">Opérateur d’assignation de soustraction.</span><span class="sxs-lookup"><span data-stu-id="fb3f2-103">The subtraction assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb3f2-104">Notes</span><span class="sxs-lookup"><span data-stu-id="fb3f2-104">Remarks</span></span>

<span data-ttu-id="fb3f2-105">Une expression qui utilise l’opérateur d’assignation `-=`, telle que</span><span class="sxs-lookup"><span data-stu-id="fb3f2-105">An expression using the `-=` assignment operator, such as</span></span>

```csharp
x -= y
```

 <span data-ttu-id="fb3f2-106">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="fb3f2-106">is equivalent to</span></span>

```csharp
x = x - y
```

<span data-ttu-id="fb3f2-107">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="fb3f2-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="fb3f2-108">La signification de l’[opérateur -](subtraction-operator.md) dépend des types de `x` et `y` (soustraction pour les opérandes numériques, suppression de délégués pour les opérandes délégués, etc.).</span><span class="sxs-lookup"><span data-stu-id="fb3f2-108">The meaning of the [- operator](subtraction-operator.md) is dependent on the types of `x` and `y` (subtraction for numeric operands, delegate removal for delegate operands, and so forth).</span></span>

<span data-ttu-id="fb3f2-109">L’opérateur `-=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur -](subtraction-operator.md) (voir [opérateur](../keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="fb3f2-109">The `-=` operator cannot be overloaded directly, but user-defined types can overload the [- operator](subtraction-operator.md) (see [operator](../keywords/operator.md)).</span></span>

<span data-ttu-id="fb3f2-110">L’opérateur -= est également utilisé en C# pour annuler l’abonnement à un événement.</span><span class="sxs-lookup"><span data-stu-id="fb3f2-110">The -= operator is also used in C# to unsubscribe from an event.</span></span> <span data-ttu-id="fb3f2-111">Pour plus d'informations, voir [Procédure : s’abonner et se désabonner d’événements](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).</span><span class="sxs-lookup"><span data-stu-id="fb3f2-111">For more information, see [How to: Subscribe to and Unsubscribe from Events](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).</span></span>

## <a name="example"></a><span data-ttu-id="fb3f2-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="fb3f2-112">Example</span></span>

[!code-csharp[csRefOperators#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#6)]

## <a name="see-also"></a><span data-ttu-id="fb3f2-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb3f2-113">See also</span></span>

- [<span data-ttu-id="fb3f2-114">Référence C#</span><span class="sxs-lookup"><span data-stu-id="fb3f2-114">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="fb3f2-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="fb3f2-115">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="fb3f2-116">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="fb3f2-116">C# operators</span></span>](index.md)
