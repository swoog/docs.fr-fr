---
title: 'Guide pratique : Obtenir l’adresse d’une variable - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- variables [C#], address of
- pointers [C#], & operator
- pointer expressions [C#], address-of operator
ms.assetid: 44fe2cd9-a64f-4ef5-be2a-09ce807c0182
ms.openlocfilehash: b12d3bf99f32a3526bd4a1ec8c49b1fd88afd68a
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58832344"
---
# <a name="how-to-obtain-the-address-of-a-variable-c-programming-guide"></a><span data-ttu-id="84061-102">Guide pratique : Obtenir l'adresse d'une variable (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="84061-102">How to: obtain the address of a variable (C# Programming Guide)</span></span>

<span data-ttu-id="84061-103">Pour obtenir l’adresse d’une expression unaire, qui est évaluée en tant que variable fixe, utilisez l’opérateur address-of `&` :</span><span class="sxs-lookup"><span data-stu-id="84061-103">To obtain the address of a unary expression, which evaluates to a fixed variable, use the address-of operator `&`:</span></span>  
  
```csharp  
int number;  
int* p = &number; //address-of operator &  
```  
  
 <span data-ttu-id="84061-104">L’opérateur address-of peut être appliqué à une seule variable uniquement.</span><span class="sxs-lookup"><span data-stu-id="84061-104">The address-of operator can only be applied to a variable.</span></span> <span data-ttu-id="84061-105">Si la variable peut être déplacée, vous pouvez utiliser l’[instruction fixed](../../../csharp/language-reference/keywords/fixed-statement.md) pour fixer temporairement la variable avant d’obtenir son adresse.</span><span class="sxs-lookup"><span data-stu-id="84061-105">If the variable is a moveable variable, you can use the [fixed statement](../../../csharp/language-reference/keywords/fixed-statement.md) to temporarily fix the variable before obtaining its address.</span></span> <span data-ttu-id="84061-106">Pour plus d’informations sur les variables déplaçables, voir [Variables fixes et déplaçables](/dotnet/csharp/language-reference/language-specification/unsafe-code#fixed-and-moveable-variables).</span><span class="sxs-lookup"><span data-stu-id="84061-106">For more information about moveable variables, see [Fixed and moveable variables](/dotnet/csharp/language-reference/language-specification/unsafe-code#fixed-and-moveable-variables).</span></span> 
  
 <span data-ttu-id="84061-107">Il vous appartient de vérifier que la variable est initialisée.</span><span class="sxs-lookup"><span data-stu-id="84061-107">It's your responsibility to ensure that the variable is initialized.</span></span> <span data-ttu-id="84061-108">Le compilateur ne génère pas de message d’erreur si la variable n’est pas initialisée.</span><span class="sxs-lookup"><span data-stu-id="84061-108">The compiler doesn't issue an error message if the variable is not initialized.</span></span>  
  
 <span data-ttu-id="84061-109">Vous ne pouvez pas obtenir l’adresse d’une constante ou d’une valeur.</span><span class="sxs-lookup"><span data-stu-id="84061-109">You can't get the address of a constant or a value.</span></span>  
  
## <a name="example"></a><span data-ttu-id="84061-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="84061-110">Example</span></span>  
 <span data-ttu-id="84061-111">Dans cet exemple, un pointeur désignant `int`, `p`, est déclaré et se voit assigner l’adresse d’une variable entière, `number`.</span><span class="sxs-lookup"><span data-stu-id="84061-111">In this example, a pointer to `int`, `p`, is declared and assigned the address of an integer variable, `number`.</span></span> <span data-ttu-id="84061-112">La variable `number` est initialisée à la suite de l’assignation à `*p`.</span><span class="sxs-lookup"><span data-stu-id="84061-112">The variable `number` is initialized as a result of the assignment to `*p`.</span></span> <span data-ttu-id="84061-113">Si vous décommentez cette instruction d’assignation, l’initialisation de la variable `number` est supprimée, mais aucune erreur n’est émise au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="84061-113">If you comment out this assignment statement, the initialization of the variable `number` is removed, but no compile-time error is issued.</span></span>  

> [!NOTE]
> <span data-ttu-id="84061-114">Compilez cet exemple avec l’option de compilateur [`-unsafe`](../../language-reference/compiler-options/unsafe-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="84061-114">Compile this example with the [`-unsafe`](../../language-reference/compiler-options/unsafe-compiler-option.md) compiler option.</span></span>
  
 [!code-csharp[address-of-a-variable](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuidePointers/CS/Pointers.cs#8)]  
  
## <a name="see-also"></a><span data-ttu-id="84061-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84061-115">See also</span></span>

- [<span data-ttu-id="84061-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="84061-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="84061-117">Expressions de pointeur</span><span class="sxs-lookup"><span data-stu-id="84061-117">Pointer Expressions</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)
- [<span data-ttu-id="84061-118">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="84061-118">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)
- [<span data-ttu-id="84061-119">Types</span><span class="sxs-lookup"><span data-stu-id="84061-119">Types</span></span>](../../../csharp/language-reference/keywords/types.md)
- [<span data-ttu-id="84061-120">unsafe</span><span class="sxs-lookup"><span data-stu-id="84061-120">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)
- [<span data-ttu-id="84061-121">fixed, instruction</span><span class="sxs-lookup"><span data-stu-id="84061-121">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)
- [<span data-ttu-id="84061-122">stackalloc</span><span class="sxs-lookup"><span data-stu-id="84061-122">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
