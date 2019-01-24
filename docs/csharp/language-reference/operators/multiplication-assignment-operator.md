---
title: '*=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '*=_CSharpKeyword'
helpviewer_keywords:
- '*= operator [C#]'
- binary multiplication assignment operator (*=) [C#]
ms.assetid: 2e472155-59db-4dbf-bb94-bcccfa1a794d
ms.openlocfilehash: 2038f3b55d46f3503496275b3d25b17663b8c1db
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333432"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="4c301-102">\*=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="4c301-102">\*= Operator (C# Reference)</span></span>

<span data-ttu-id="4c301-103">Opérateur d’assignation de multiplication binaire.</span><span class="sxs-lookup"><span data-stu-id="4c301-103">The binary multiplication assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c301-104">Notes</span><span class="sxs-lookup"><span data-stu-id="4c301-104">Remarks</span></span>

<span data-ttu-id="4c301-105">Une expression qui utilise l’opérateur d’assignation `*=`, telle que</span><span class="sxs-lookup"><span data-stu-id="4c301-105">An expression using the `*=` assignment operator, such as</span></span>

```csharp
x *= y
```

<span data-ttu-id="4c301-106">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="4c301-106">is equivalent to</span></span>

```csharp
x = x * y
```

<span data-ttu-id="4c301-107">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="4c301-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="4c301-108">L’[opérateur \*](multiplication-operator.md) est prédéfini pour les types numériques de façon à effectuer une multiplication.</span><span class="sxs-lookup"><span data-stu-id="4c301-108">The [\* operator](multiplication-operator.md) is predefined for numeric types to perform multiplication.</span></span>

<span data-ttu-id="4c301-109">L’opérateur `*=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur \*](multiplication-operator.md) (voir [operator](../keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="4c301-109">The `*=` operator cannot be overloaded directly, but user-defined types can overload the [\* operator](multiplication-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="4c301-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="4c301-110">Example</span></span>

[!code-csharp[csRefOperators#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#13)]

## <a name="see-also"></a><span data-ttu-id="4c301-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c301-111">See also</span></span>

- [<span data-ttu-id="4c301-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="4c301-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="4c301-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="4c301-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="4c301-114">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="4c301-114">C# Operators</span></span>](index.md)
