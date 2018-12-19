---
title: '&lt;=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- <=_CSharpKeyword
helpviewer_keywords:
- less than or equal to operator (<=) [C#]
- <= operator [C#]
ms.assetid: bb0caec9-d253-4105-b8bc-5252233251e4
ms.openlocfilehash: 950ba3fc02e015f2574d123d1fd9adc116aae045
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243450"
---
# <a name="lt-operator-c-reference"></a><span data-ttu-id="e3599-102">&lt;=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="e3599-102">&lt;= Operator (C# Reference)</span></span>
<span data-ttu-id="e3599-103">Tous les types numériques et d’énumération définissent un opérateur relationnel « inférieur ou égal à » (`<=`) qui retourne `true` si le premier opérande est inférieur ou égal au deuxième et `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e3599-103">All numeric and enumeration types define a "less than or equal" relational operator (`<=`) that returns `true` if the first operand is less than or equal to the second, `false` otherwise.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e3599-104">Notes</span><span class="sxs-lookup"><span data-stu-id="e3599-104">Remarks</span></span>  
 <span data-ttu-id="e3599-105">Les types définis par l’utilisateur peuvent surcharger l’opérateur `<=`.</span><span class="sxs-lookup"><span data-stu-id="e3599-105">User-defined types can overload the `<=` operator.</span></span> <span data-ttu-id="e3599-106">Pour plus d’informations, consultez [operator](../../../csharp/language-reference/keywords/operator.md).</span><span class="sxs-lookup"><span data-stu-id="e3599-106">For more information, see [operator](../../../csharp/language-reference/keywords/operator.md).</span></span> <span data-ttu-id="e3599-107">Si `<=` est surchargé, [>=](../../../csharp/language-reference/operators/greater-than-equal-operator.md) doit aussi l’être.</span><span class="sxs-lookup"><span data-stu-id="e3599-107">If `<=` is overloaded, [>=](../../../csharp/language-reference/operators/greater-than-equal-operator.md) must also be overloaded.</span></span> <span data-ttu-id="e3599-108">Les opérations sur les types intégraux sont en général autorisées sur l’énumération.</span><span class="sxs-lookup"><span data-stu-id="e3599-108">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e3599-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="e3599-109">Example</span></span>  
 [!code-csharp[csRefOperators#32](../../../csharp/language-reference/operators/codesnippet/CSharp/less-than-equal-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="e3599-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3599-110">See Also</span></span>

- [<span data-ttu-id="e3599-111">Référence C#</span><span class="sxs-lookup"><span data-stu-id="e3599-111">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="e3599-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="e3599-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="e3599-113">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="e3599-113">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="e3599-114">explicit</span><span class="sxs-lookup"><span data-stu-id="e3599-114">explicit</span></span>](../../../csharp/language-reference/keywords/explicit.md)
