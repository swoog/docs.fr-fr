---
title: '&lt;&lt;=, opérateur (référence C#)'
ms.date: 07/20/2015
f1_keywords:
- <<=_CSharpKeyword
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
ms.openlocfilehash: c689aeccdf3ad6cc6c672cc101a4f0aa92f19791
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43406972"
---
# <a name="ltlt-operator-c-reference"></a><span data-ttu-id="1209d-102">&lt;&lt;=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="1209d-102">&lt;&lt;= Operator (C# Reference)</span></span>
<span data-ttu-id="1209d-103">Opérateur d’assignation de décalage vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="1209d-103">The left-shift assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1209d-104">Notes</span><span class="sxs-lookup"><span data-stu-id="1209d-104">Remarks</span></span>  
 <span data-ttu-id="1209d-105">Une expression sous la forme</span><span class="sxs-lookup"><span data-stu-id="1209d-105">An expression of the form</span></span>  
  
```csharp  
x <<= y  
```  
  
 <span data-ttu-id="1209d-106">est évaluée comme étant</span><span class="sxs-lookup"><span data-stu-id="1209d-106">is evaluated as</span></span>  
  
```csharp  
x = x << y  
```  
  
 <span data-ttu-id="1209d-107">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="1209d-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="1209d-108">L’[opérateur << ](../../../csharp/language-reference/operators/left-shift-operator.md) déplace `x` vers la gauche du nombre de bits spécifié par `y`.</span><span class="sxs-lookup"><span data-stu-id="1209d-108">The [<< operator](../../../csharp/language-reference/operators/left-shift-operator.md) shifts `x` left by the number of bits specified by `y`.</span></span>  
  
 <span data-ttu-id="1209d-109">L’opérateur `<<=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur <<](../../../csharp/language-reference/operators/left-shift-operator.md) (consultez [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="1209d-109">The `<<=` operator cannot be overloaded directly, but user-defined types can overload the [<< operator](../../../csharp/language-reference/operators/left-shift-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1209d-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="1209d-110">Example</span></span>  
 [!code-csharp[csRefOperators#12](../../../csharp/language-reference/operators/codesnippet/CSharp/left-shift-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="1209d-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1209d-111">See Also</span></span>

- [<span data-ttu-id="1209d-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="1209d-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="1209d-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="1209d-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="1209d-114">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="1209d-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
