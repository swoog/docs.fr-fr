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
ms.openlocfilehash: dc3cedafc57e1c6ec9bc34ca4e2c2aa9c604848c
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53239577"
---
# <a name="--operator-c-reference"></a><span data-ttu-id="b38bb-102">-=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="b38bb-102">-= Operator (C# Reference)</span></span>
<span data-ttu-id="b38bb-103">Opérateur d’assignation de soustraction.</span><span class="sxs-lookup"><span data-stu-id="b38bb-103">The subtraction assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b38bb-104">Notes</span><span class="sxs-lookup"><span data-stu-id="b38bb-104">Remarks</span></span>  
 <span data-ttu-id="b38bb-105">Une expression qui utilise l’opérateur d’assignation `-=`, telle que</span><span class="sxs-lookup"><span data-stu-id="b38bb-105">An expression using the `-=` assignment operator, such as</span></span>  
  
```csharp  
x -= y  
```  
  
 <span data-ttu-id="b38bb-106">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="b38bb-106">is equivalent to</span></span>  
  
```csharp  
x = x - y  
```  
  
 <span data-ttu-id="b38bb-107">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="b38bb-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="b38bb-108">La signification de l’[opérateur -](../../../csharp/language-reference/operators/subtraction-operator.md) dépend des types de `x` et `y` (soustraction pour les opérandes numériques, suppression de délégués pour les opérandes délégués, etc.).</span><span class="sxs-lookup"><span data-stu-id="b38bb-108">The meaning of the [- operator](../../../csharp/language-reference/operators/subtraction-operator.md) is dependent on the types of `x` and `y` (subtraction for numeric operands, delegate removal for delegate operands, and so forth).</span></span>  
  
 <span data-ttu-id="b38bb-109">L’opérateur `-=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur -](../../../csharp/language-reference/operators/subtraction-operator.md) (voir [opérateur](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="b38bb-109">The `-=` operator cannot be overloaded directly, but user-defined types can overload the [- operator](../../../csharp/language-reference/operators/subtraction-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
 <span data-ttu-id="b38bb-110">L’opérateur -= est également utilisé en C# pour annuler l’abonnement à un événement.</span><span class="sxs-lookup"><span data-stu-id="b38bb-110">The -= operator is also used in C# to unsubscribe from an event.</span></span> <span data-ttu-id="b38bb-111">Pour plus d'informations, voir [Procédure : s’abonner et se désabonner d’événements](../../../csharp/programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).</span><span class="sxs-lookup"><span data-stu-id="b38bb-111">For more information, see [How to: Subscribe to and Unsubscribe from Events](../../../csharp/programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="b38bb-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="b38bb-112">Example</span></span>  
 [!code-csharp[csRefOperators#6](codesnippet/CSharp/subtraction-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="b38bb-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b38bb-113">See Also</span></span>

- [<span data-ttu-id="b38bb-114">Référence C#</span><span class="sxs-lookup"><span data-stu-id="b38bb-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="b38bb-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b38bb-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="b38bb-116">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="b38bb-116">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
