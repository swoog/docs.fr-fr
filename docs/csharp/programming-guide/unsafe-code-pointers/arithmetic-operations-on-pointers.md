---
title: Opérations arithmétiques sur les pointeurs (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], arithmetic operations
ms.assetid: d4f0b623-827e-45ce-8649-cfcebc8692aa
ms.openlocfilehash: c40b125e42649093aa1f1fe860a3e8f5d2690359
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33324299"
---
# <a name="arithmetic-operations-on-pointers-c-programming-guide"></a><span data-ttu-id="1f1b1-102">Opérations arithmétiques sur les pointeurs (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="1f1b1-102">Arithmetic Operations on Pointers (C# Programming Guide)</span></span>
<span data-ttu-id="1f1b1-103">Cette rubrique décrit l’utilisation des opérateurs arithmétiques `+` et **-** pour manipuler les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-103">This topic discusses using the arithmetic operators `+` and **-** to manipulate pointers.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1f1b1-104">Vous ne pouvez pas effectuer d’opérations arithmétiques sur les pointeurs void.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-104">You cannot perform any arithmetic operations on void pointers.</span></span>  
  
## <a name="adding-and-subtracting-numeric-values-to-or-from-pointers"></a><span data-ttu-id="1f1b1-105">Ajout et soustraction de valeurs numériques dans les pointeurs</span><span class="sxs-lookup"><span data-stu-id="1f1b1-105">Adding and Subtracting Numeric Values to or From Pointers</span></span>  
 <span data-ttu-id="1f1b1-106">Vous pouvez ajouter une valeur `n` de type [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), [long](../../../csharp/language-reference/keywords/long.md) ou [ulong](../../../csharp/language-reference/keywords/ulong.md) à un pointeur `p` de n’importe quel type à l’exception de `void*`.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-106">You can add a value `n` of type [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), [long](../../../csharp/language-reference/keywords/long.md), or [ulong](../../../csharp/language-reference/keywords/ulong.md) to a pointer, `p`,of any type except `void*`.</span></span> <span data-ttu-id="1f1b1-107">Le pointeur `p+n` est le résultat de l’ajout de `n * sizeof(p) to the address of p`.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-107">The result `p+n` is the pointer resulting from adding `n * sizeof(p) to the address of p`.</span></span> <span data-ttu-id="1f1b1-108">De la même façon, `p-n` est le pointeur qui résulte de la soustraction de `n * sizeof(p)` de l’adresse de `p`.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-108">Similarly, `p-n` is the pointer resulting from subtracting `n * sizeof(p)` from the address of `p`.</span></span>  
  
## <a name="subtracting-pointers"></a><span data-ttu-id="1f1b1-109">Soustraction de pointeurs</span><span class="sxs-lookup"><span data-stu-id="1f1b1-109">Subtracting Pointers</span></span>  
 <span data-ttu-id="1f1b1-110">Vous pouvez également soustraire des pointeurs du même type.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-110">You can also subtract pointers of the same type.</span></span> <span data-ttu-id="1f1b1-111">Le résultat est toujours du type `long`.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-111">The result is always of the type `long`.</span></span> <span data-ttu-id="1f1b1-112">Par exemple, si `p1` et `p2` sont des pointeurs du type `pointer-type*`, l’expression `p1-p2` produit le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="1f1b1-112">For example, if `p1` and `p2` are pointers of the type `pointer-type*`, then the expression `p1-p2` results in:</span></span>  
  
 `((long)p1 - (long)p2)/sizeof(pointer_type)`  
  
 <span data-ttu-id="1f1b1-113">Aucune exception n’est générée si l’opération arithmétique produit un dépassement de capacité sur le domaine du pointeur, et le résultat dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-113">No exceptions are generated when the arithmetic operation overflows the domain of the pointer, and the result depends on the implementation.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1f1b1-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="1f1b1-114">Example</span></span>  
 [!code-csharp[csProgGuidePointers#14](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/arithmetic-operations-on-pointers_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#15](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/arithmetic-operations-on-pointers_2.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="1f1b1-115">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="1f1b1-115">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="1f1b1-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f1b1-116">See Also</span></span>  
 [<span data-ttu-id="1f1b1-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="1f1b1-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="1f1b1-118">Pointeurs et code unsafe</span><span class="sxs-lookup"><span data-stu-id="1f1b1-118">Unsafe Code and Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/index.md)  
 [<span data-ttu-id="1f1b1-119">Expressions de pointeur</span><span class="sxs-lookup"><span data-stu-id="1f1b1-119">Pointer Expressions</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)  
 [<span data-ttu-id="1f1b1-120">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="1f1b1-120">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
 [<span data-ttu-id="1f1b1-121">Manipulation de pointeurs</span><span class="sxs-lookup"><span data-stu-id="1f1b1-121">Manipulating Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/manipulating-pointers.md)  
 [<span data-ttu-id="1f1b1-122">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="1f1b1-122">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)  
 [<span data-ttu-id="1f1b1-123">Types</span><span class="sxs-lookup"><span data-stu-id="1f1b1-123">Types</span></span>](../../../csharp/language-reference/keywords/types.md)  
 [<span data-ttu-id="1f1b1-124">unsafe</span><span class="sxs-lookup"><span data-stu-id="1f1b1-124">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)  
 [<span data-ttu-id="1f1b1-125">fixed, instruction</span><span class="sxs-lookup"><span data-stu-id="1f1b1-125">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)  
 [<span data-ttu-id="1f1b1-126">stackalloc</span><span class="sxs-lookup"><span data-stu-id="1f1b1-126">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
