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
ms.openlocfilehash: 920981addd5c779c9ad1c666ef45e1de5cd23408
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65633000"
---
# <a name="--operator-c-reference"></a><span data-ttu-id="c5cc0-102">-, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="c5cc0-102">- operator (C# Reference)</span></span>

<span data-ttu-id="c5cc0-103">L’opérateur `-` peut être utilisé comme opérateur unaire ou opérateur binaire.</span><span class="sxs-lookup"><span data-stu-id="c5cc0-103">The `-` operator can function as either a unary or a binary operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5cc0-104">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5cc0-104">Remarks</span></span>

<span data-ttu-id="c5cc0-105">Les opérateurs `-` sont prédéfinis pour tous les types numériques.</span><span class="sxs-lookup"><span data-stu-id="c5cc0-105">Unary `-` operators are predefined for all numeric types.</span></span> <span data-ttu-id="c5cc0-106">Le résultat d’une opération `-` unaire sur un type numérique correspond à la négation numérique de l’opérande.</span><span class="sxs-lookup"><span data-stu-id="c5cc0-106">The result of a unary `-` operation on a numeric type is the numeric negation of the operand.</span></span>

<span data-ttu-id="c5cc0-107">Les opérateurs `-` binaires sont prédéfinis pour tous les types numériques et d’énumérations pour soustraire le second opérande au premier.</span><span class="sxs-lookup"><span data-stu-id="c5cc0-107">Binary `-` operators are predefined for all numeric and enumeration types to subtract the second operand from the first.</span></span>

<span data-ttu-id="c5cc0-108">Les types délégués fournissent également un opérateur `-` binaire, qui effectue une suppression de délégué.</span><span class="sxs-lookup"><span data-stu-id="c5cc0-108">Delegate types also provide a binary `-` operator, which performs delegate removal.</span></span>

<span data-ttu-id="c5cc0-109">Les types définis par l’utilisateur peuvent surcharger les opérateurs `-` unaires et `-` binaires.</span><span class="sxs-lookup"><span data-stu-id="c5cc0-109">User-defined types can overload the unary `-` and binary `-` operators.</span></span> <span data-ttu-id="c5cc0-110">Pour plus d’informations, consultez [operator, mot clé](../keywords/operator.md).</span><span class="sxs-lookup"><span data-stu-id="c5cc0-110">For more information, see [operator keyword](../keywords/operator.md).</span></span>

## <a name="example"></a><span data-ttu-id="c5cc0-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="c5cc0-111">Example</span></span>

[!code-csharp[csRefOperators#40](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#40)]

## <a name="see-also"></a><span data-ttu-id="c5cc0-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5cc0-112">See also</span></span>

- [<span data-ttu-id="c5cc0-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="c5cc0-113">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="c5cc0-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="c5cc0-114">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="c5cc0-115">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="c5cc0-115">C# operators</span></span>](index.md)
