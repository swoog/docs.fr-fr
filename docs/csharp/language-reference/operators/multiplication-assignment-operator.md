---
title: '*=, opérateur (référence C#)'
ms.date: 07/20/2015
f1_keywords:
- '*=_CSharpKeyword'
helpviewer_keywords:
- '*= operator [C#]'
- binary multiplication assignment operator (*=) [C#]
ms.assetid: 2e472155-59db-4dbf-bb94-bcccfa1a794d
ms.openlocfilehash: e47bc5c681c94ac3fc5c345c56b3814350ffa5ec
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42932348"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="f8bdc-102">\*=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="f8bdc-102">\*= Operator (C# Reference)</span></span>
<span data-ttu-id="f8bdc-103">Opérateur d’assignation de multiplication binaire.</span><span class="sxs-lookup"><span data-stu-id="f8bdc-103">The binary multiplication assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f8bdc-104">Notes</span><span class="sxs-lookup"><span data-stu-id="f8bdc-104">Remarks</span></span>  
 <span data-ttu-id="f8bdc-105">Une expression qui utilise l’opérateur d’assignation `*=`, telle que</span><span class="sxs-lookup"><span data-stu-id="f8bdc-105">An expression using the `*=` assignment operator, such as</span></span>  
  
```csharp  
x *= y  
```  
  
 <span data-ttu-id="f8bdc-106">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="f8bdc-106">is equivalent to</span></span>  
  
```csharp  
x = x * y  
```  
  
 <span data-ttu-id="f8bdc-107">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="f8bdc-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="f8bdc-108">L’[opérateur \*](../../../csharp/language-reference/operators/multiplication-operator.md) est prédéfini pour les types numériques de façon à effectuer une multiplication.</span><span class="sxs-lookup"><span data-stu-id="f8bdc-108">The [\* operator](../../../csharp/language-reference/operators/multiplication-operator.md) is predefined for numeric types to perform multiplication.</span></span>  
  
 <span data-ttu-id="f8bdc-109">L’opérateur `*=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur *](../../../csharp/language-reference/operators/multiplication-operator.md) (consultez [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="f8bdc-109">The `*=` operator cannot be overloaded directly, but user-defined types can overload the [* operator](../../../csharp/language-reference/operators/multiplication-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="f8bdc-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="f8bdc-110">Example</span></span>  
 [!code-csharp[csRefOperators#13](../../../csharp/language-reference/operators/codesnippet/CSharp/multiplication-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="f8bdc-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8bdc-111">See Also</span></span>

- [<span data-ttu-id="f8bdc-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="f8bdc-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="f8bdc-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="f8bdc-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="f8bdc-114">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="f8bdc-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
