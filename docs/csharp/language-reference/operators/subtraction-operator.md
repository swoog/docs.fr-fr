---
title: '- opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- -_CSharpKeyword
helpviewer_keywords:
- '- operator [C#]'
- subtraction operator (-) [C#]
ms.assetid: 4de7a4fa-c69d-48e6-aff1-3130af970b2d
ms.openlocfilehash: 8cf6e8871a88e2b37b9531ecbd616289523473c7
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333757"
---
# <a name="--operator-c-reference"></a><span data-ttu-id="18f4c-102">-, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="18f4c-102">- operator (C# Reference)</span></span>

<span data-ttu-id="18f4c-103">L’opérateur `-` peut être utilisé comme opérateur unaire ou opérateur binaire.</span><span class="sxs-lookup"><span data-stu-id="18f4c-103">The `-` operator can function as either a unary or a binary operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="18f4c-104">Notes</span><span class="sxs-lookup"><span data-stu-id="18f4c-104">Remarks</span></span>

<span data-ttu-id="18f4c-105">Les opérateurs `-` sont prédéfinis pour tous les types numériques.</span><span class="sxs-lookup"><span data-stu-id="18f4c-105">Unary `-` operators are predefined for all numeric types.</span></span> <span data-ttu-id="18f4c-106">Le résultat d’une opération `-` unaire sur un type numérique correspond à la négation numérique de l’opérande.</span><span class="sxs-lookup"><span data-stu-id="18f4c-106">The result of a unary `-` operation on a numeric type is the numeric negation of the operand.</span></span>

<span data-ttu-id="18f4c-107">Les opérateurs `-` binaires sont prédéfinis pour tous les types numériques et d’énumérations pour soustraire le second opérande au premier.</span><span class="sxs-lookup"><span data-stu-id="18f4c-107">Binary `-` operators are predefined for all numeric and enumeration types to subtract the second operand from the first.</span></span>

<span data-ttu-id="18f4c-108">Les types délégués fournissent également un opérateur `-` binaire, qui effectue une suppression de délégué.</span><span class="sxs-lookup"><span data-stu-id="18f4c-108">Delegate types also provide a binary `-` operator, which performs delegate removal.</span></span>

<span data-ttu-id="18f4c-109">Les types définis par l’utilisateur peuvent surcharger les opérateurs `-` unaires et `-` binaires.</span><span class="sxs-lookup"><span data-stu-id="18f4c-109">User-defined types can overload the unary `-` and binary `-` operators.</span></span> <span data-ttu-id="18f4c-110">Pour plus d’informations, consultez [operator, mot clé](../keywords/operator.md).</span><span class="sxs-lookup"><span data-stu-id="18f4c-110">For more information, see [operator keyword](../keywords/operator.md).</span></span>

## <a name="example"></a><span data-ttu-id="18f4c-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="18f4c-111">Example</span></span>

[!code-csharp[csRefOperators#40](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#40)]

## <a name="see-also"></a><span data-ttu-id="18f4c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18f4c-112">See also</span></span>

- [<span data-ttu-id="18f4c-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="18f4c-113">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="18f4c-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="18f4c-114">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="18f4c-115">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="18f4c-115">C# operators</span></span>](index.md)