---
title: (), opérateur - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ()_CSharpKeyword
helpviewer_keywords:
- type conversion [C#], () operator
- cast operator [C#]
- () operator [C#]
ms.assetid: 846e1f94-8a8c-42fc-a42c-fbd38e70d8cc
ms.openlocfilehash: 57c23dbd6ee95597514dba92e7217bdcc3e38f24
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236451"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="da042-102">(), opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="da042-102">() Operator (C# Reference)</span></span>
<span data-ttu-id="da042-103">En plus d’être utilisées pour spécifier l’ordre des opérations dans une expression, les parenthèses sont utilisées pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="da042-103">In addition to being used to specify the order of operations in an expression, parentheses are used to perform the following tasks:</span></span>  
  
1.  <span data-ttu-id="da042-104">Spécifier des casts ou conversions de type</span><span class="sxs-lookup"><span data-stu-id="da042-104">Specify casts, or type conversions.</span></span>  
  
     [!code-csharp[csRefOperators#1](../../../csharp/language-reference/operators/codesnippet/CSharp/invocation-operator_1.cs)]  
  
2.  <span data-ttu-id="da042-105">Appeler des méthodes ou des délégués</span><span class="sxs-lookup"><span data-stu-id="da042-105">Invoke methods or delegates.</span></span>  
  
     [!code-csharp[csRefOperators#2](../../../csharp/language-reference/operators/codesnippet/CSharp/invocation-operator_2.cs)]  
  
## <a name="remarks"></a><span data-ttu-id="da042-106">Notes</span><span class="sxs-lookup"><span data-stu-id="da042-106">Remarks</span></span>  
 <span data-ttu-id="da042-107">Un cast appelle explicitement l’opérateur de conversion d’un type à l’autre. Le cast échoue si aucun opérateur de conversion n’est défini.</span><span class="sxs-lookup"><span data-stu-id="da042-107">A cast explicitly invokes the conversion operator from one type to another; the cast fails if no such conversion operator is defined.</span></span> <span data-ttu-id="da042-108">Pour définir un opérateur de conversion, consultez [explicit](../../../csharp/language-reference/keywords/explicit.md) et [implicit](../../../csharp/language-reference/keywords/implicit.md).</span><span class="sxs-lookup"><span data-stu-id="da042-108">To define a conversion operator, see [explicit](../../../csharp/language-reference/keywords/explicit.md) and [implicit](../../../csharp/language-reference/keywords/implicit.md).</span></span>  
  
 <span data-ttu-id="da042-109">L’opérateur `()` ne peut pas être surchargé.</span><span class="sxs-lookup"><span data-stu-id="da042-109">The `()` operator cannot be overloaded.</span></span>  
  
 <span data-ttu-id="da042-110">Pour plus d’informations, consultez [Cast et conversions de types](../../../csharp/programming-guide/types/casting-and-type-conversions.md).</span><span class="sxs-lookup"><span data-stu-id="da042-110">For more information, see [Casting and Type Conversions](../../../csharp/programming-guide/types/casting-and-type-conversions.md).</span></span>  
  
 <span data-ttu-id="da042-111">Pour plus d’informations sur l’appel de méthode, consultez [Méthodes](../../../csharp/programming-guide/classes-and-structs/methods.md).</span><span class="sxs-lookup"><span data-stu-id="da042-111">For more information about method invocation, see [Methods](../../../csharp/programming-guide/classes-and-structs/methods.md).</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="da042-112">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="da042-112">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="da042-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da042-113">See Also</span></span>

- [<span data-ttu-id="da042-114">Référence C#</span><span class="sxs-lookup"><span data-stu-id="da042-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="da042-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="da042-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="da042-116">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="da042-116">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
