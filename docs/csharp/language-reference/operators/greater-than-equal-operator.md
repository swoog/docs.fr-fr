---
title: '&gt;=, opérateur (référence C#)'
ms.date: 07/20/2015
f1_keywords:
- '>=_CSharpKeyword'
helpviewer_keywords:
- greater than or equal to operator (>=) [C#]
- '>= operator [C#]'
ms.assetid: 0db4dcaf-56a3-4884-a7ad-35f64978a58d
ms.openlocfilehash: 8749d1dc0670a5a76bda5ee0d69a4a142671c1e6
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "43000283"
---
# <a name="gt-operator-c-reference"></a><span data-ttu-id="880cf-102">&gt;=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="880cf-102">&gt;= Operator (C# Reference)</span></span>
<span data-ttu-id="880cf-103">Tous les types numériques et d’énumération définissent un opérateur relationnel « supérieur ou égal à », `>=`, qui retourne `true` si le premier opérande est supérieur ou égal au second, et `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="880cf-103">All numeric and enumeration types define a "greater than or equal" relational operator, `>=` that returns `true` if the first operand is greater than or equal to the second, `false` otherwise.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="880cf-104">Notes</span><span class="sxs-lookup"><span data-stu-id="880cf-104">Remarks</span></span>  
 <span data-ttu-id="880cf-105">Les types définis par l’utilisateur peuvent surcharger l’opérateur `>=`.</span><span class="sxs-lookup"><span data-stu-id="880cf-105">User-defined types can overload the `>=` operator.</span></span> <span data-ttu-id="880cf-106">Pour plus d’informations, consultez [operator](../../../csharp/language-reference/keywords/operator.md).</span><span class="sxs-lookup"><span data-stu-id="880cf-106">For more information, see [operator](../../../csharp/language-reference/keywords/operator.md).</span></span> <span data-ttu-id="880cf-107">Si `>=` est surchargé, [<=](../../../csharp/language-reference/operators/less-than-equal-operator.md) doit aussi l’être.</span><span class="sxs-lookup"><span data-stu-id="880cf-107">If `>=` is overloaded, [<=](../../../csharp/language-reference/operators/less-than-equal-operator.md) must also be overloaded.</span></span> <span data-ttu-id="880cf-108">Les opérations sur les types intégraux sont en général autorisées sur l’énumération.</span><span class="sxs-lookup"><span data-stu-id="880cf-108">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="880cf-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="880cf-109">Example</span></span>  
 [!code-csharp[csRefOperators#39](../../../csharp/language-reference/operators/codesnippet/CSharp/greater-than-equal-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="880cf-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="880cf-110">See Also</span></span>

- [<span data-ttu-id="880cf-111">Référence C#</span><span class="sxs-lookup"><span data-stu-id="880cf-111">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="880cf-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="880cf-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="880cf-113">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="880cf-113">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
