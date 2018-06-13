---
title: '&lt;=, opérateur (référence C#)'
ms.date: 07/20/2015
f1_keywords:
- <=_CSharpKeyword
helpviewer_keywords:
- less than or equal to operator (<=) [C#]
- <= operator [C#]
ms.assetid: bb0caec9-d253-4105-b8bc-5252233251e4
ms.openlocfilehash: 24bf274bfcb0a8e19a79aafb3bd7920054044be0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33271160"
---
# <a name="lt-operator-c-reference"></a><span data-ttu-id="940b6-102">&lt;=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="940b6-102">&lt;= Operator (C# Reference)</span></span>
<span data-ttu-id="940b6-103">Tous les types numériques et d’énumération définissent un opérateur relationnel « inférieur ou égal à » (`<=`) qui retourne `true` si le premier opérande est inférieur ou égal au deuxième et `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="940b6-103">All numeric and enumeration types define a "less than or equal" relational operator (`<=`) that returns `true` if the first operand is less than or equal to the second, `false` otherwise.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="940b6-104">Notes</span><span class="sxs-lookup"><span data-stu-id="940b6-104">Remarks</span></span>  
 <span data-ttu-id="940b6-105">Les types définis par l’utilisateur peuvent surcharger l’opérateur `<=`.</span><span class="sxs-lookup"><span data-stu-id="940b6-105">User-defined types can overload the `<=` operator.</span></span> <span data-ttu-id="940b6-106">Pour plus d’informations, consultez [operator](../../../csharp/language-reference/keywords/operator.md).</span><span class="sxs-lookup"><span data-stu-id="940b6-106">For more information, see [operator](../../../csharp/language-reference/keywords/operator.md).</span></span> <span data-ttu-id="940b6-107">Si `<=` est surchargé, [>=](../../../csharp/language-reference/operators/greater-than-equal-operator.md) doit aussi l’être.</span><span class="sxs-lookup"><span data-stu-id="940b6-107">If `<=` is overloaded, [>=](../../../csharp/language-reference/operators/greater-than-equal-operator.md) must also be overloaded.</span></span> <span data-ttu-id="940b6-108">Les opérations sur les types intégraux sont en général autorisées sur l’énumération.</span><span class="sxs-lookup"><span data-stu-id="940b6-108">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="940b6-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="940b6-109">Example</span></span>  
 [!code-csharp[csRefOperators#32](../../../csharp/language-reference/operators/codesnippet/CSharp/less-than-equal-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="940b6-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="940b6-110">See Also</span></span>  
 [<span data-ttu-id="940b6-111">Référence C#</span><span class="sxs-lookup"><span data-stu-id="940b6-111">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="940b6-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="940b6-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="940b6-113">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="940b6-113">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
 [<span data-ttu-id="940b6-114">explicit</span><span class="sxs-lookup"><span data-stu-id="940b6-114">explicit</span></span>](../../../csharp/language-reference/keywords/explicit.md)
