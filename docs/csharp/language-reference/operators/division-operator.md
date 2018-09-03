---
title: /, opérateur (référence C#)
ms.date: 04/04/2018
f1_keywords:
- /_CSharpKeyword
helpviewer_keywords:
- / operator [C#]
- division operator [C#]
ms.assetid: d155e496-678f-4efa-bebe-2bd08da2c5af
ms.openlocfilehash: bddf6d234f3536ad64f0cd876cc7ade4494916d9
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43394851"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="99e9a-102">/, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="99e9a-102">/ Operator (C# Reference)</span></span>
<span data-ttu-id="99e9a-103">L’opérateur de division (`/`) divise son premier opérande par son deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="99e9a-103">The division operator (`/`) divides its first operand by its second operand.</span></span> <span data-ttu-id="99e9a-104">Tous les types numériques ont des opérateurs de division prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="99e9a-104">All numeric types have predefined division operators.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="99e9a-105">Notes</span><span class="sxs-lookup"><span data-stu-id="99e9a-105">Remarks</span></span>  
 <span data-ttu-id="99e9a-106">Les types définis par l’utilisateur peuvent surcharger l’opérateur `/` (voir [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="99e9a-106">User-defined types can overload the `/` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="99e9a-107">Une surcharge de l’opérateur `/` surcharge implicitement l’[opérateur /=](division-assignment-operator.md).</span><span class="sxs-lookup"><span data-stu-id="99e9a-107">An overload of the `/` operator implicitly overloads the [/= operator](division-assignment-operator.md).</span></span>  
  
 <span data-ttu-id="99e9a-108">Quand vous divisez deux entiers, le résultat est toujours un entier.</span><span class="sxs-lookup"><span data-stu-id="99e9a-108">When you divide two integers, the result is always an integer.</span></span> <span data-ttu-id="99e9a-109">Par exemple, le résultat de 7 / 3 est 2.</span><span class="sxs-lookup"><span data-stu-id="99e9a-109">For example, the result of 7 / 3 is 2.</span></span> <span data-ttu-id="99e9a-110">Il ne faut pas confondre avec la division plancher, car l’opérateur `/` arrondit le résultat vers zéro : -7 / 3 donne le résultat -2.</span><span class="sxs-lookup"><span data-stu-id="99e9a-110">This is not to be confused with floored division, as the `/` operator rounds towards zero: -7 / 3 is -2.</span></span>  
  
 <span data-ttu-id="99e9a-111">Pour obtenir un quotient sous forme de nombre rationnel, utilisez les types `float`, `double` ou `decimal`.</span><span class="sxs-lookup"><span data-stu-id="99e9a-111">To obtain a quotient as a rational number, use the `float`, `double`, or `decimal` types.</span></span> <span data-ttu-id="99e9a-112">Il existe de nombreuses façons d’effectuer des conversions entre des [types numériques intégrés](../../../csharp/language-reference/keywords/reference-tables-for-types.md).</span><span class="sxs-lookup"><span data-stu-id="99e9a-112">There are many ways to convert between [built in numeric types](../../../csharp/language-reference/keywords/reference-tables-for-types.md).</span></span>  
  
 <span data-ttu-id="99e9a-113">Pour déterminer le reste, utilisez l’[opérateur de reste](../../../csharp/language-reference/operators/remainder-operator.md) `%`.</span><span class="sxs-lookup"><span data-stu-id="99e9a-113">To determine the remainder, use the [remainder operator](../../../csharp/language-reference/operators/remainder-operator.md) `%`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="99e9a-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="99e9a-114">Example</span></span>  
 [!code-csharp[csRefOperators#42](../../../csharp/language-reference/operators/codesnippet/CSharp/division-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="99e9a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99e9a-115">See Also</span></span>

- [<span data-ttu-id="99e9a-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="99e9a-116">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="99e9a-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="99e9a-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="99e9a-118">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="99e9a-118">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
