---
title: Guide pratique pour accéder à un membre à l’aide d’un pointeur (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], member access
ms.assetid: 1e998498-8c85-4a78-8ce2-4d8c20f08342
ms.openlocfilehash: b51239be8da8c45aa2d7f1ff0700884c43c07299
ms.sourcegitcommit: 7f7664837d35320a0bad3f7e4ecd68d6624633b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2018
ms.locfileid: "52671954"
---
# <a name="how-to-access-a-member-with-a-pointer-c-programming-guide"></a><span data-ttu-id="99109-102">Guide pratique pour accéder à un membre à l’aide d’un pointeur (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="99109-102">How to: access a member with a pointer (C# Programming Guide)</span></span>
<span data-ttu-id="99109-103">Pour accéder à un membre d’un struct déclaré dans un contexte unsafe, vous pouvez utiliser l’opérateur d’accès au membre comme illustré dans l’exemple suivant où `p` est un pointeur vers un [struct](../../../csharp/language-reference/keywords/struct.md) qui contient un membre `x`.</span><span class="sxs-lookup"><span data-stu-id="99109-103">To access a member of a struct that is declared in an unsafe context, you can use the member access operator as shown in the following example in which `p` is a pointer to a [struct](../../../csharp/language-reference/keywords/struct.md) that contains a member `x`.</span></span>  
  
```  
CoOrds* p = &home;  
p -> x = 25; //member access operator ->  
```  
  
## <a name="example"></a><span data-ttu-id="99109-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="99109-104">Example</span></span>  
 <span data-ttu-id="99109-105">Dans cet exemple, un [struct](../../../csharp/language-reference/keywords/struct.md), `CoOrds`, qui contient les deux coordonnées `x` et `y`, est déclaré et instancié.</span><span class="sxs-lookup"><span data-stu-id="99109-105">In this example, a [struct](../../../csharp/language-reference/keywords/struct.md), `CoOrds`, that contains the two coordinates `x` and `y` is declared and instantiated.</span></span> <span data-ttu-id="99109-106">En utilisant l’opérateur d’accès au membre `->` et un pointeur vers l’instance `home`, `x` et `y` sont des valeurs assignées.</span><span class="sxs-lookup"><span data-stu-id="99109-106">By using the member access operator `->` and a pointer to the instance `home`, `x` and `y` are assigned values.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="99109-107">Remarquez que l’expression `p->x` équivaut à l’expression `(*p).x`, et vous pouvez obtenir le même résultat en utilisant l’une ou l’autre expression.</span><span class="sxs-lookup"><span data-stu-id="99109-107">Notice that the expression `p->x` is equivalent to the expression `(*p).x`, and you can obtain the same result by using either of the two expressions.</span></span>  
  
 [!code-csharp[csProgGuidePointers#9](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-access-a-member-with-a-pointer_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#10](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-access-a-member-with-a-pointer_2.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="99109-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99109-108">See Also</span></span>

- [<span data-ttu-id="99109-109">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="99109-109">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="99109-110">Expressions de pointeur</span><span class="sxs-lookup"><span data-stu-id="99109-110">Pointer Expressions</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)  
- [<span data-ttu-id="99109-111">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="99109-111">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)  
- [<span data-ttu-id="99109-112">Types</span><span class="sxs-lookup"><span data-stu-id="99109-112">Types</span></span>](../../../csharp/language-reference/keywords/types.md)  
- [<span data-ttu-id="99109-113">unsafe</span><span class="sxs-lookup"><span data-stu-id="99109-113">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)  
- [<span data-ttu-id="99109-114">fixed, instruction</span><span class="sxs-lookup"><span data-stu-id="99109-114">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)  
- [<span data-ttu-id="99109-115">stackalloc</span><span class="sxs-lookup"><span data-stu-id="99109-115">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
