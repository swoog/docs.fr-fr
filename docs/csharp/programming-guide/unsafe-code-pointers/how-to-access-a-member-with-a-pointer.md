---
title: Guide pratique pour accéder à un membre à l’aide d’un pointeur - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], member access
ms.assetid: 1e998498-8c85-4a78-8ce2-4d8c20f08342
ms.openlocfilehash: d0ca4a0b2189ee652ad1d9c2b63690306a651df4
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65635075"
---
# <a name="how-to-access-a-member-with-a-pointer-c-programming-guide"></a><span data-ttu-id="65ebd-102">Guide pratique pour accéder à un membre à l’aide d’un pointeur (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="65ebd-102">How to: access a member with a pointer (C# Programming Guide)</span></span>
<span data-ttu-id="65ebd-103">Pour accéder à un membre d’un struct déclaré dans un contexte unsafe, vous pouvez utiliser l’opérateur d’accès au membre comme illustré dans l’exemple suivant où `p` est un pointeur vers un [struct](../../../csharp/language-reference/keywords/struct.md) qui contient un membre `x`.</span><span class="sxs-lookup"><span data-stu-id="65ebd-103">To access a member of a struct that is declared in an unsafe context, you can use the member access operator as shown in the following example in which `p` is a pointer to a [struct](../../../csharp/language-reference/keywords/struct.md) that contains a member `x`.</span></span>  
  
```  
CoOrds* p = &home;  
p -> x = 25; //member access operator ->  
```  
  
## <a name="example"></a><span data-ttu-id="65ebd-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="65ebd-104">Example</span></span>  
 <span data-ttu-id="65ebd-105">Dans cet exemple, un [struct](../../../csharp/language-reference/keywords/struct.md), `CoOrds`, qui contient les deux coordonnées `x` et `y`, est déclaré et instancié.</span><span class="sxs-lookup"><span data-stu-id="65ebd-105">In this example, a [struct](../../../csharp/language-reference/keywords/struct.md), `CoOrds`, that contains the two coordinates `x` and `y` is declared and instantiated.</span></span> <span data-ttu-id="65ebd-106">En utilisant l’opérateur d’accès au membre `->` et un pointeur vers l’instance `home`, `x` et `y` sont des valeurs assignées.</span><span class="sxs-lookup"><span data-stu-id="65ebd-106">By using the member access operator `->` and a pointer to the instance `home`, `x` and `y` are assigned values.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="65ebd-107">Remarquez que l’expression `p->x` équivaut à l’expression `(*p).x`, et vous pouvez obtenir le même résultat en utilisant l’une ou l’autre expression.</span><span class="sxs-lookup"><span data-stu-id="65ebd-107">Notice that the expression `p->x` is equivalent to the expression `(*p).x`, and you can obtain the same result by using either of the two expressions.</span></span>  
  
 [!code-csharp[csProgGuidePointers#9](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuidePointers/CS/Pointers2.cs#9)]  
  
 [!code-csharp[csProgGuidePointers#10](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuidePointers/CS/Pointers.cs#10)]  
  
## <a name="see-also"></a><span data-ttu-id="65ebd-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65ebd-108">See also</span></span>

- [<span data-ttu-id="65ebd-109">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="65ebd-109">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="65ebd-110">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="65ebd-110">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)
- [<span data-ttu-id="65ebd-111">Types</span><span class="sxs-lookup"><span data-stu-id="65ebd-111">Types</span></span>](../../../csharp/language-reference/keywords/types.md)
- [<span data-ttu-id="65ebd-112">unsafe</span><span class="sxs-lookup"><span data-stu-id="65ebd-112">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)
- [<span data-ttu-id="65ebd-113">fixed, instruction</span><span class="sxs-lookup"><span data-stu-id="65ebd-113">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)
- [<span data-ttu-id="65ebd-114">stackalloc</span><span class="sxs-lookup"><span data-stu-id="65ebd-114">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
