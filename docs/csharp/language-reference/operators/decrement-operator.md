---
title: --, opérateur (référence C#)
ms.date: 07/20/2015
f1_keywords:
- --_CSharpKeyword
helpviewer_keywords:
- -- operator [C#]
- decrement operator (--) [C#]
ms.assetid: 6b9cfe86-63c7-421f-9379-c9690fea8720
ms.openlocfilehash: 25f301bc0b2bc9bf51b0a44f26b2efabae00e452
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33288799"
---
# <a name="---operator-c-reference"></a><span data-ttu-id="d71f7-102">--, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="d71f7-102">-- Operator (C# Reference)</span></span>
<span data-ttu-id="d71f7-103">L’opérateur de décrémentation (`--`) décrémente son opérande de 1.</span><span class="sxs-lookup"><span data-stu-id="d71f7-103">The decrement operator (`--`) decrements its operand by 1.</span></span> <span data-ttu-id="d71f7-104">L’opérateur de décrémentation peut figurer avant ou après son opérande : `--variable` et `variable--`.</span><span class="sxs-lookup"><span data-stu-id="d71f7-104">The decrement operator can appear before or after its operand: `--variable` and `variable--`.</span></span> <span data-ttu-id="d71f7-105">La première forme est une opération de décrément préfixé.</span><span class="sxs-lookup"><span data-stu-id="d71f7-105">The first form is a prefix decrement operation.</span></span> <span data-ttu-id="d71f7-106">Le résultat de l’opération est la valeur de l’opérande « après » sa décrémentation.</span><span class="sxs-lookup"><span data-stu-id="d71f7-106">The result of the operation is the value of the operand "after" it has been decremented.</span></span> <span data-ttu-id="d71f7-107">La deuxième forme est une opération de décrément suffixé.</span><span class="sxs-lookup"><span data-stu-id="d71f7-107">The second form is a postfix decrement operation.</span></span> <span data-ttu-id="d71f7-108">Le résultat de l’opération est la valeur de l’opérande « avant » sa décrémentation.</span><span class="sxs-lookup"><span data-stu-id="d71f7-108">The result of the operation is the value of the operand "before" it has been decremented.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d71f7-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d71f7-109">Remarks</span></span>  
 <span data-ttu-id="d71f7-110">Les types numériques et d’énumération ont des opérateurs de décrémentation prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="d71f7-110">Numeric and enumeration types have predefined decrement operators.</span></span>  
  
 <span data-ttu-id="d71f7-111">Les types définis par l’utilisateur peuvent surcharger l’opérateur `--` (voir [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="d71f7-111">User-defined types can overload the `--` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="d71f7-112">Les opérations sur les types intégraux sont en général autorisées sur l’énumération.</span><span class="sxs-lookup"><span data-stu-id="d71f7-112">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d71f7-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="d71f7-113">Example</span></span>  
 [!code-csharp[csRefOperators#8](../../../csharp/language-reference/operators/codesnippet/CSharp/decrement-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="d71f7-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d71f7-114">See Also</span></span>  
 [<span data-ttu-id="d71f7-115">Référence C#</span><span class="sxs-lookup"><span data-stu-id="d71f7-115">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="d71f7-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="d71f7-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="d71f7-117">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="d71f7-117">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
