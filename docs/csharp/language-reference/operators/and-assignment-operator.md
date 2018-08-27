---
title: '&amp;=, opérateur (référence C#)'
ms.date: 07/20/2015
f1_keywords:
- '&=_CSharpKeyword'
helpviewer_keywords:
- AND assignment operator (&=) [C#]
- '&= operator [C#]'
ms.assetid: e8d58f3f-72dd-4b5a-b995-452fcce7e6bb
ms.openlocfilehash: f3a6fe20ca89a90b5a64118d73fb39e9a364d1e9
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42933950"
---
# <a name="amp-operator-c-reference"></a><span data-ttu-id="5ecb8-102">&amp;=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="5ecb8-102">&amp;= Operator (C# Reference)</span></span>
<span data-ttu-id="5ecb8-103">Opérateur d’assignation AND.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-103">The AND assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5ecb8-104">Notes</span><span class="sxs-lookup"><span data-stu-id="5ecb8-104">Remarks</span></span>  
 <span data-ttu-id="5ecb8-105">Une expression qui utilise l’opérateur d’assignation `&=`, telle que</span><span class="sxs-lookup"><span data-stu-id="5ecb8-105">An expression using the `&=` assignment operator, such as</span></span>  
  
```csharp  
x &= y  
```  
  
 <span data-ttu-id="5ecb8-106">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="5ecb8-106">is equivalent to</span></span>  
  
```csharp  
x = x & y  
```  
  
 <span data-ttu-id="5ecb8-107">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="5ecb8-108">L’[opérateur &](../../../csharp/language-reference/operators/and-operator.md) effectue une opération AND logique au niveau du bit sur les opérandes de type intégral et une opération AND logique sur les opérandes de type `bool`.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-108">The [& operator](../../../csharp/language-reference/operators/and-operator.md) performs a bitwise logical AND operation on integral operands and logical AND on `bool` operands.</span></span>  
  
 <span data-ttu-id="5ecb8-109">L’opérateur `&=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur &](../../../csharp/language-reference/operators/and-operator.md) binaire (voir [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="5ecb8-109">The `&=` operator cannot be overloaded directly, but user-defined types can overload the binary [& operator](../../../csharp/language-reference/operators/and-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="5ecb8-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="5ecb8-110">Example</span></span>  
 [!code-csharp[csRefOperators#34](../../../csharp/language-reference/operators/codesnippet/CSharp/and-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="5ecb8-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ecb8-111">See Also</span></span>

- [<span data-ttu-id="5ecb8-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="5ecb8-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="5ecb8-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="5ecb8-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="5ecb8-114">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="5ecb8-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
