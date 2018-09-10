---
title: /=, opérateur (référence C#)
ms.date: 07/20/2015
f1_keywords:
- /=_CSharpKeyword
helpviewer_keywords:
- division assignment operator (/=) [C#]
- /= (division assignment operator) [C#]
ms.assetid: 50fc02b0-ee9c-4c3e-b58d-d591282caf1c
ms.openlocfilehash: 8fff048cc441181aa3f0e3c0c638d501aaf9de3f
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43526306"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="8d60b-102">/=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="8d60b-102">/= Operator (C# Reference)</span></span>
<span data-ttu-id="8d60b-103">Opérateur d’assignation de division.</span><span class="sxs-lookup"><span data-stu-id="8d60b-103">The division assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8d60b-104">Notes</span><span class="sxs-lookup"><span data-stu-id="8d60b-104">Remarks</span></span>  
 <span data-ttu-id="8d60b-105">Une expression qui utilise l’opérateur d’assignation `/=`, telle que</span><span class="sxs-lookup"><span data-stu-id="8d60b-105">An expression using the `/=` assignment operator, such as</span></span>  
  
```csharp  
x /= y  
```  
  
 <span data-ttu-id="8d60b-106">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="8d60b-106">is equivalent to</span></span>  
  
```csharp  
x = x / y  
```  
  
 <span data-ttu-id="8d60b-107">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="8d60b-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="8d60b-108">L’[opérateur /](../../../csharp/language-reference/operators/division-operator.md) est prédéfini pour les types numériques afin d’effectuer une division.</span><span class="sxs-lookup"><span data-stu-id="8d60b-108">The [/ operator](../../../csharp/language-reference/operators/division-operator.md) is predefined for numeric types to perform division.</span></span>  
  
 <span data-ttu-id="8d60b-109">Vous ne pouvez pas surcharger directement l’opérateur `/=`, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur /](../../../csharp/language-reference/operators/division-operator.md) (voir [opérateur](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="8d60b-109">The `/=` operator cannot be overloaded directly, but user-defined types can overload the [/ operator](../../../csharp/language-reference/operators/division-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="8d60b-110">Sur tous les opérateurs d’assignation composée, le fait de surcharger l’opérateur binaire surcharge implicitement l’assignation composée équivalente.</span><span class="sxs-lookup"><span data-stu-id="8d60b-110">On all compound assignment operators, overloading the binary operator implicitly overloads the equivalent compound assignment.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8d60b-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="8d60b-111">Example</span></span>  
 [!code-csharp[csRefOperators#5](codesnippet/CSharp/division-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="8d60b-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d60b-112">See Also</span></span>

- [<span data-ttu-id="8d60b-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="8d60b-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="8d60b-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="8d60b-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="8d60b-115">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="8d60b-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
