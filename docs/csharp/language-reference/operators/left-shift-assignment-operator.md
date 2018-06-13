---
title: '&lt;&lt;=, opérateur (référence C#)'
ms.date: 07/20/2015
f1_keywords:
- <<=_CSharpKeyword
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
ms.openlocfilehash: e5f3886670baa34b0360501ee15280b93fac36bc
ms.sourcegitcommit: 89c93d05c2281b4c834f48f6c8df1047e1410980
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2018
ms.locfileid: "34171791"
---
# <a name="ltlt-operator-c-reference"></a><span data-ttu-id="0d12b-102">&lt;&lt;=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="0d12b-102">&lt;&lt;= Operator (C# Reference)</span></span>
<span data-ttu-id="0d12b-103">Opérateur d’assignation de décalage vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="0d12b-103">The left-shift assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0d12b-104">Notes</span><span class="sxs-lookup"><span data-stu-id="0d12b-104">Remarks</span></span>  
 <span data-ttu-id="0d12b-105">Une expression sous la forme</span><span class="sxs-lookup"><span data-stu-id="0d12b-105">An expression of the form</span></span>  
  
```csharp  
x <<= y  
```  
  
 <span data-ttu-id="0d12b-106">est évaluée comme étant</span><span class="sxs-lookup"><span data-stu-id="0d12b-106">is evaluated as</span></span>  
  
```csharp  
x = x << y  
```  
  
 <span data-ttu-id="0d12b-107">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="0d12b-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="0d12b-108">L’[opérateur << ](../../../csharp/language-reference/operators/left-shift-operator.md) déplace `x` vers la gauche du nombre de bits spécifié par `y`.</span><span class="sxs-lookup"><span data-stu-id="0d12b-108">The [<< operator](../../../csharp/language-reference/operators/left-shift-operator.md) shifts `x` left by the number of bits specified by `y`.</span></span>  
  
 <span data-ttu-id="0d12b-109">L’opérateur `<<=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur <<](../../../csharp/language-reference/operators/left-shift-operator.md) (consultez [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="0d12b-109">The `<<=` operator cannot be overloaded directly, but user-defined types can overload the [<< operator](../../../csharp/language-reference/operators/left-shift-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="0d12b-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="0d12b-110">Example</span></span>  
 [!code-csharp[csRefOperators#12](../../../csharp/language-reference/operators/codesnippet/CSharp/left-shift-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="0d12b-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d12b-111">See Also</span></span>  
 [<span data-ttu-id="0d12b-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="0d12b-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="0d12b-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0d12b-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="0d12b-114">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="0d12b-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
