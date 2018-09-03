---
title: '&lt;, opérateur (référence C#)'
ms.date: 07/20/2015
f1_keywords:
- <_CSharpKeyword
helpviewer_keywords:
- less than operator (<) [C#]
- < operator [C#]
ms.assetid: 38cb91e6-79a6-48ec-9c1e-7b71fd8d2b41
ms.openlocfilehash: 382110985eaffd7ca4cf014d7991fc5ee87dc031
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43467404"
---
# <a name="lt-operator-c-reference"></a><span data-ttu-id="c824b-102">&lt;, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="c824b-102">&lt; Operator (C# Reference)</span></span>
<span data-ttu-id="c824b-103">Tous les types numériques et d’énumération définissent un opérateur relationnel « inférieur à » (`<`) qui retourne `true` si le premier opérande est inférieur au deuxième et `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c824b-103">All numeric and enumeration types define a "less than" relational operator (`<`) that returns `true` if the first operand is less than the second, `false` otherwise.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c824b-104">Notes</span><span class="sxs-lookup"><span data-stu-id="c824b-104">Remarks</span></span>  
 <span data-ttu-id="c824b-105">Les types définis par l’utilisateur peuvent surcharger l’opérateur `<` (voir [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="c824b-105">User-defined types can overload the `<` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="c824b-106">Si `<` est surchargé, [>](../../../csharp/language-reference/operators/greater-than-operator.md) doit aussi l’être.</span><span class="sxs-lookup"><span data-stu-id="c824b-106">If `<` is overloaded, [>](../../../csharp/language-reference/operators/greater-than-operator.md) must also be overloaded.</span></span>
  
## <a name="example"></a><span data-ttu-id="c824b-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="c824b-107">Example</span></span>  
 [!code-csharp[csRefOperators#24](../../../csharp/language-reference/operators/codesnippet/CSharp/less-than-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="c824b-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c824b-108">See Also</span></span>

- [<span data-ttu-id="c824b-109">Référence C#</span><span class="sxs-lookup"><span data-stu-id="c824b-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="c824b-110">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="c824b-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="c824b-111">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="c824b-111">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
