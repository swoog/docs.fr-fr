---
title: ++, opérateur (référence C#)
ms.date: 07/20/2015
f1_keywords:
- ++_CSharpKeyword
helpviewer_keywords:
- increment operator (++) [C#]
- ++ operator [C#]
ms.assetid: e9dec353-070b-44fb-98ed-eb8fdf753feb
ms.openlocfilehash: a52f614ce1bbfb8e9d9be686b277c1e69f6f9d35
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2018
ms.locfileid: "47202249"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="a05b7-102">++, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="a05b7-102">++ Operator (C# Reference)</span></span>
<span data-ttu-id="a05b7-103">L’opérateur d’incrément (`++`) incrémente son opérande de 1.</span><span class="sxs-lookup"><span data-stu-id="a05b7-103">The increment operator (`++`) increments its operand by 1.</span></span> <span data-ttu-id="a05b7-104">L’opérateur d’incrément peut figurer avant ou après son opérande : `++variable` et `variable++`.</span><span class="sxs-lookup"><span data-stu-id="a05b7-104">The increment operator can appear before or after its operand: `++variable` and `variable++`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a05b7-105">Notes</span><span class="sxs-lookup"><span data-stu-id="a05b7-105">Remarks</span></span>  
 <span data-ttu-id="a05b7-106">La première forme est une opération d’incrément préfixé.</span><span class="sxs-lookup"><span data-stu-id="a05b7-106">The first form is a prefix increment operation.</span></span> <span data-ttu-id="a05b7-107">Le résultat de l’opération est la valeur de l’opérande après qu’il a été incrémenté.</span><span class="sxs-lookup"><span data-stu-id="a05b7-107">The result of the operation is the value of the operand after it has been incremented.</span></span>  
  
 <span data-ttu-id="a05b7-108">La deuxième forme est une opération d’incrément suffixé.</span><span class="sxs-lookup"><span data-stu-id="a05b7-108">The second form is a postfix increment operation.</span></span> <span data-ttu-id="a05b7-109">Le résultat de l’opération est la valeur de l’opérande avant qu’il ait été incrémenté.</span><span class="sxs-lookup"><span data-stu-id="a05b7-109">The result of the operation is the value of the operand before it has been incremented.</span></span>  
  
 <span data-ttu-id="a05b7-110">Les types numériques et d’énumération ont des opérateurs d’incrément prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="a05b7-110">Numeric and enumeration types have predefined increment operators.</span></span> <span data-ttu-id="a05b7-111">Les types définis par l’utilisateur peuvent surcharger l’opérateur `++` .</span><span class="sxs-lookup"><span data-stu-id="a05b7-111">User-defined types can overload the `++` operator.</span></span> <span data-ttu-id="a05b7-112">Les opérations sur les types intégraux sont en général autorisées sur l’énumération.</span><span class="sxs-lookup"><span data-stu-id="a05b7-112">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a05b7-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="a05b7-113">Example</span></span>  
 [!code-csharp[csRefOperators#3](../../../csharp/language-reference/operators/codesnippet/CSharp/increment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="a05b7-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a05b7-114">See Also</span></span>

- [<span data-ttu-id="a05b7-115">Référence C#</span><span class="sxs-lookup"><span data-stu-id="a05b7-115">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="a05b7-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="a05b7-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="a05b7-117">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="a05b7-117">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
