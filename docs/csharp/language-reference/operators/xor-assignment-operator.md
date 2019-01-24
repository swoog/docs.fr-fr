---
title: ^=, opérateur - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ^=_CSharpKeyword
helpviewer_keywords:
- ^= operator [C#]
ms.assetid: 3658ff9a-61cd-467e-ad6b-8fbf1cfbaae4
ms.openlocfilehash: 12189d6469a9716d3b7ebcffef23423a75692d1a
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333549"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="a3479-102">^=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="a3479-102">^= operator (C# Reference)</span></span>

<span data-ttu-id="a3479-103">Opérateur d’assignation OR exclusif.</span><span class="sxs-lookup"><span data-stu-id="a3479-103">The exclusive-OR assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3479-104">Notes</span><span class="sxs-lookup"><span data-stu-id="a3479-104">Remarks</span></span>

<span data-ttu-id="a3479-105">Une expression sous la forme</span><span class="sxs-lookup"><span data-stu-id="a3479-105">An expression of the form</span></span>

```csharp
x ^= y
```

<span data-ttu-id="a3479-106">est évaluée comme étant</span><span class="sxs-lookup"><span data-stu-id="a3479-106">is evaluated as</span></span>

```csharp
x = x ^ y
```

<span data-ttu-id="a3479-107">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="a3479-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="a3479-108">L’[opérateur ^](xor-operator.md) effectue une opération de bits OR exclusif sur les opérandes de type intégral et une opération OR exclusif logique sur les opérandes de type [bool](../keywords/bool.md).</span><span class="sxs-lookup"><span data-stu-id="a3479-108">The [^ operator](xor-operator.md) performs a bitwise exclusive-OR operation on integral operands and logical exclusive-OR on [bool](../keywords/bool.md) operands.</span></span>

<span data-ttu-id="a3479-109">L’opérateur ^= ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur ^](xor-operator.md) (voir [operator](../keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="a3479-109">The ^= operator cannot be overloaded directly, but user-defined types can overload the [^ operator](xor-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="a3479-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="a3479-110">Example</span></span>

[!code-csharp[csRefOperators#23](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#23)]

## <a name="see-also"></a><span data-ttu-id="a3479-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3479-111">See also</span></span>

- [<span data-ttu-id="a3479-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="a3479-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="a3479-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="a3479-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="a3479-114">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="a3479-114">C# operators</span></span>](index.md)