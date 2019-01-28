---
title: Opérations arithmétiques sur les pointeurs - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], arithmetic operations
ms.assetid: d4f0b623-827e-45ce-8649-cfcebc8692aa
ms.openlocfilehash: b0b75a6aa47cfc169157b229c4386ed7dc1e627b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54710194"
---
# <a name="arithmetic-operations-on-pointers-c-programming-guide"></a><span data-ttu-id="68e21-102">Opérations arithmétiques sur les pointeurs (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="68e21-102">Arithmetic operations on pointers (C# Programming Guide)</span></span>
<span data-ttu-id="68e21-103">Cette rubrique explique comment utiliser les opérateurs arithmétiques `+` et `-` pour manipuler les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="68e21-103">This topic discusses using the arithmetic operators `+` and `-` to manipulate pointers.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="68e21-104">Vous ne pouvez pas effectuer d’opérations arithmétiques sur les pointeurs void.</span><span class="sxs-lookup"><span data-stu-id="68e21-104">You cannot perform any arithmetic operations on void pointers.</span></span>  
  
## <a name="adding-and-subtracting-numeric-values-to-or-from-pointers"></a><span data-ttu-id="68e21-105">Ajouter et soustraire des valeurs numériques aux pointeurs</span><span class="sxs-lookup"><span data-stu-id="68e21-105">Adding and subtracting numeric values to or from pointers</span></span>  
 <span data-ttu-id="68e21-106">Vous pouvez ajouter une valeur `n` de type [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), [long](../../../csharp/language-reference/keywords/long.md) ou [ulong](../../../csharp/language-reference/keywords/ulong.md) à un pointeur.</span><span class="sxs-lookup"><span data-stu-id="68e21-106">You can add a value `n` of type [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), [long](../../../csharp/language-reference/keywords/long.md), or [ulong](../../../csharp/language-reference/keywords/ulong.md) to a pointer.</span></span> <span data-ttu-id="68e21-107">Si `p` est un pointeur de type `pointer-type*`, le résultat `p+n` est le pointeur résultant de l’ajout de `n * sizeof(pointer-type)` à l’adresse de `p`.</span><span class="sxs-lookup"><span data-stu-id="68e21-107">If `p` is a pointer of the type `pointer-type*`, the result `p+n` is the pointer resulting from adding `n * sizeof(pointer-type)` to the address of `p`.</span></span> <span data-ttu-id="68e21-108">De la même façon, `p-n` est le pointeur qui résulte de la soustraction de `n * sizeof(pointer-type)` de l’adresse de `p`.</span><span class="sxs-lookup"><span data-stu-id="68e21-108">Similarly, `p-n` is the pointer resulting from subtracting `n * sizeof(pointer-type)` from the address of `p`.</span></span>  
  
## <a name="subtracting-pointers"></a><span data-ttu-id="68e21-109">Soustraire des pointeurs</span><span class="sxs-lookup"><span data-stu-id="68e21-109">Subtracting pointers</span></span>  
 <span data-ttu-id="68e21-110">Vous pouvez également soustraire des pointeurs du même type.</span><span class="sxs-lookup"><span data-stu-id="68e21-110">You can also subtract pointers of the same type.</span></span> <span data-ttu-id="68e21-111">Le résultat est toujours du type `long`.</span><span class="sxs-lookup"><span data-stu-id="68e21-111">The result is always of the type `long`.</span></span> <span data-ttu-id="68e21-112">Par exemple, si `p1` et `p2` sont des pointeurs du type `pointer-type*`, l’expression `p1-p2` produit le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="68e21-112">For example, if `p1` and `p2` are pointers of the type `pointer-type*`, then the expression `p1-p2` results in:</span></span>  
  
 `((long)p1 - (long)p2)/sizeof(pointer-type)`  
  
 <span data-ttu-id="68e21-113">Aucune exception n’est générée si l’opération arithmétique produit un dépassement de capacité sur le domaine du pointeur, et le résultat dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="68e21-113">No exceptions are generated when the arithmetic operation overflows the domain of the pointer, and the result depends on the implementation.</span></span>  
  
## <a name="example"></a><span data-ttu-id="68e21-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="68e21-114">Example</span></span>  
 [!code-csharp[csProgGuidePointers#14](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/arithmetic-operations-on-pointers_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#15](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/arithmetic-operations-on-pointers_2.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="68e21-115">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="68e21-115">C# language specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="68e21-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68e21-116">See also</span></span>

- [<span data-ttu-id="68e21-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="68e21-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="68e21-118">Pointeurs et code unsafe</span><span class="sxs-lookup"><span data-stu-id="68e21-118">Unsafe Code and Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/index.md)
- [<span data-ttu-id="68e21-119">Expressions de pointeur</span><span class="sxs-lookup"><span data-stu-id="68e21-119">Pointer Expressions</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)
- [<span data-ttu-id="68e21-120">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="68e21-120">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
- [<span data-ttu-id="68e21-121">Manipulation de pointeurs</span><span class="sxs-lookup"><span data-stu-id="68e21-121">Manipulating Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/manipulating-pointers.md)
- [<span data-ttu-id="68e21-122">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="68e21-122">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)
- [<span data-ttu-id="68e21-123">Types</span><span class="sxs-lookup"><span data-stu-id="68e21-123">Types</span></span>](../../../csharp/language-reference/keywords/types.md)
- [<span data-ttu-id="68e21-124">unsafe</span><span class="sxs-lookup"><span data-stu-id="68e21-124">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)
- [<span data-ttu-id="68e21-125">fixed, instruction</span><span class="sxs-lookup"><span data-stu-id="68e21-125">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)
- [<span data-ttu-id="68e21-126">stackalloc</span><span class="sxs-lookup"><span data-stu-id="68e21-126">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
