---
title: '%, opérateur (référence C#)'
ms.date: 04/04/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- '%_CSharpKeyword'
helpviewer_keywords:
- remainder operator [C#]
- '% operator [C#]'
ms.assetid: 3b74f4f9-fd9c-45e7-84fa-c8d71a0dfad7
caps.latest.revision: 15
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 796b4a40347fc5881db27a8a8a28404c7c4e8c5b
ms.sourcegitcommit: b750a8e3979749b214e7e10c82efb0a0524dfcb1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2018
---
# <a name="-operator-c-reference"></a><span data-ttu-id="242db-102">%, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="242db-102">% Operator (C# Reference)</span></span>
<span data-ttu-id="242db-103">L’opérateur de reste (`%`) calcule le reste de la division du premier opérande par le deuxième.</span><span class="sxs-lookup"><span data-stu-id="242db-103">The remainder operator (`%`) computes the remainder after dividing its first operand by its second.</span></span> <span data-ttu-id="242db-104">Tous les types numériques ont des opérateurs de reste prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="242db-104">All numeric types have predefined remainder operators.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="242db-105">Notes</span><span class="sxs-lookup"><span data-stu-id="242db-105">Remarks</span></span>  
 <span data-ttu-id="242db-106">La formule `a % b` retourne toujours une valeur de la plage `(-b, b)`, de manière exclusive (elle ne retourne jamais `b` ou `-b`), en conservant le signe du dividende.</span><span class="sxs-lookup"><span data-stu-id="242db-106">The formula `a % b` will always return a value on the range `(-b, b)`, exclusive (it can never return `b` or `-b`), keeping the sign of the dividend.</span></span> <span data-ttu-id="242db-107">Pour la division entière, l’opérateur de reste applique la règle `a % b = a - (a / b) * b`.</span><span class="sxs-lookup"><span data-stu-id="242db-107">For integer division, the remainder operator satisfies the rule `a % b = a - (a / b) * b`.</span></span>
  
 <span data-ttu-id="242db-108">Cela est différent du modulo canonique, qui applique une règle similaire avec une division plancher et retourne des valeurs de la plage `[0, b)`.</span><span class="sxs-lookup"><span data-stu-id="242db-108">This is not to be confused with canonical modulus, which satisfies a similar rule but with floored division and returns values on the range `[0, b)`.</span></span> <span data-ttu-id="242db-109">C# ne fournit pas d’opérateur de modulo canonique.</span><span class="sxs-lookup"><span data-stu-id="242db-109">C# does not have an operator for canonical modulus.</span></span> <span data-ttu-id="242db-110">Toutefois, le comportement est le même pour les dividendes positifs.</span><span class="sxs-lookup"><span data-stu-id="242db-110">However, the behavior is the same for positive dividends.</span></span>
  
 <span data-ttu-id="242db-111">Les types définis par l’utilisateur peuvent surcharger l’opérateur `%` (voir [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="242db-111">User-defined types can overload the `%` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="242db-112">Quand un opérateur binaire est surchargé, l’opérateur d’assignation correspondant, le cas échéant, est aussi implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="242db-112">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>  
  
## <a name="example"></a><span data-ttu-id="242db-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="242db-113">Example</span></span>  
 [!code-csharp[csRefOperators#9](../../../csharp/language-reference/operators/codesnippet/CSharp/remainder-operator_1.cs)]  
  
## <a name="comments"></a><span data-ttu-id="242db-114">Commentaires</span><span class="sxs-lookup"><span data-stu-id="242db-114">Comments</span></span>  
 <span data-ttu-id="242db-115">Notez les erreurs d’arrondi associées au type double.</span><span class="sxs-lookup"><span data-stu-id="242db-115">Note the round-off errors associated with the double type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="242db-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="242db-116">See Also</span></span>  
 [<span data-ttu-id="242db-117">Référence C#</span><span class="sxs-lookup"><span data-stu-id="242db-117">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="242db-118">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="242db-118">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="242db-119">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="242db-119">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
