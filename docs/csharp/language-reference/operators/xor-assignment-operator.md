---
title: ^=, opérateur - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ^=_CSharpKeyword
helpviewer_keywords:
- ^= operator [C#]
ms.assetid: 3658ff9a-61cd-467e-ad6b-8fbf1cfbaae4
ms.openlocfilehash: cf39c8e8586e9d4f537fe38d8b28f55542db6ab8
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237153"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="f9c25-102">^=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="f9c25-102">^= Operator (C# Reference)</span></span>
<span data-ttu-id="f9c25-103">Opérateur d’assignation OR exclusif.</span><span class="sxs-lookup"><span data-stu-id="f9c25-103">The exclusive-OR assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f9c25-104">Notes</span><span class="sxs-lookup"><span data-stu-id="f9c25-104">Remarks</span></span>  
 <span data-ttu-id="f9c25-105">Une expression sous la forme</span><span class="sxs-lookup"><span data-stu-id="f9c25-105">An expression of the form</span></span>  
  
```csharp  
x ^= y  
```  
  
 <span data-ttu-id="f9c25-106">est évaluée comme étant</span><span class="sxs-lookup"><span data-stu-id="f9c25-106">is evaluated as</span></span>  
  
```csharp  
x = x ^ y  
```  
  
 <span data-ttu-id="f9c25-107">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="f9c25-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="f9c25-108">L’[opérateur ^](../../../csharp/language-reference/operators/xor-operator.md) effectue une opération de bits OR exclusif sur les opérandes de type intégral et une opération OR exclusif logique sur les opérandes de type [bool](../../../csharp/language-reference/keywords/bool.md).</span><span class="sxs-lookup"><span data-stu-id="f9c25-108">The [^ operator](../../../csharp/language-reference/operators/xor-operator.md) performs a bitwise exclusive-OR operation on integral operands and logical exclusive-OR on [bool](../../../csharp/language-reference/keywords/bool.md) operands.</span></span>  
  
 <span data-ttu-id="f9c25-109">L’opérateur ^= ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur ^](../../../csharp/language-reference/operators/xor-operator.md) (voir [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="f9c25-109">The ^= operator cannot be overloaded directly, but user-defined types can overload the [^ operator](../../../csharp/language-reference/operators/xor-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="f9c25-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="f9c25-110">Example</span></span>  
 [!code-csharp[csRefOperators#23](../../../csharp/language-reference/operators/codesnippet/CSharp/xor-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="f9c25-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9c25-111">See Also</span></span>

- [<span data-ttu-id="f9c25-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="f9c25-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="f9c25-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="f9c25-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="f9c25-114">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="f9c25-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
