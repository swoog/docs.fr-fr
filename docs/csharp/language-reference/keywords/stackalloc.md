---
title: stackalloc (référence C#)
ms.date: 04/12/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- stackalloc_CSharpKeyword
- stackalloc
helpviewer_keywords:
- stackalloc keyword [C#]
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: c4cde254bb6a5601d10619c4a3bd2f00f1f146d3
ms.sourcegitcommit: 9a4fe1a1c37b26532654b4bbe22d702237950009
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2018
---
# <a name="stackalloc-c-reference"></a><span data-ttu-id="dbcf9-102">stackalloc (référence C#)</span><span class="sxs-lookup"><span data-stu-id="dbcf9-102">stackalloc (C# Reference)</span></span>
<span data-ttu-id="dbcf9-103">Le mot clé `stackalloc` est utilisé dans un contexte de code unsafe pour allouer un bloc de mémoire sur la pile.</span><span class="sxs-lookup"><span data-stu-id="dbcf9-103">The `stackalloc` keyword is used in an unsafe code context to allocate a block of memory on the stack.</span></span>

```csharp
int* block = stackalloc int[100];
```

## <a name="remarks"></a><span data-ttu-id="dbcf9-104">Notes</span><span class="sxs-lookup"><span data-stu-id="dbcf9-104">Remarks</span></span>

<span data-ttu-id="dbcf9-105">Le mot clé est valide uniquement dans les initialiseurs de variable locale.</span><span class="sxs-lookup"><span data-stu-id="dbcf9-105">The keyword is valid only in local variable initializers.</span></span> <span data-ttu-id="dbcf9-106">Le code suivant génère des erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="dbcf9-106">The following code causes compiler errors.</span></span>

```csharp
int* block;
// The following assignment statement causes compiler errors. You
// can use stackalloc only when declaring and initializing a local
// variable.
block = stackalloc int[100];
```

<span data-ttu-id="dbcf9-107">Dans C# 7.3 et les versions ultérieures, vous pouvez utiliser la syntaxe d’initialiseur de tableau pour les tableaux `stackalloc`.</span><span class="sxs-lookup"><span data-stu-id="dbcf9-107">Beginning with C# 7.3, you can use array initializer syntax for `stackalloc` arrays.</span></span> <span data-ttu-id="dbcf9-108">Toutes les déclarations suivantes déclarent un tableau de trois éléments ayant pour valeurs les entiers `1`, `2` et `3` :</span><span class="sxs-lookup"><span data-stu-id="dbcf9-108">All the following declarations declare an array with three elements whose values are the integers `1`, `2`, and `3`:</span></span>

```csharp
// Valid starting with C# 7.3
int* first = stackalloc int[3] { 1, 2, 3 };
int* second = stackalloc int[] { 1, 2, 3 };
int* third = stackalloc[] { 1, 2, 3 };
```

<span data-ttu-id="dbcf9-109">Des types pointeur étant impliqués, `stackalloc` requiert un contexte [unsafe](unsafe.md).</span><span class="sxs-lookup"><span data-stu-id="dbcf9-109">Because pointer types are involved, `stackalloc` requires an [unsafe](unsafe.md) context.</span></span> <span data-ttu-id="dbcf9-110">Pour plus d’informations, consultez [Pointeurs et code unsafe](../../programming-guide/unsafe-code-pointers/index.md)</span><span class="sxs-lookup"><span data-stu-id="dbcf9-110">For more information, see [Unsafe Code and Pointers](../../programming-guide/unsafe-code-pointers/index.md)</span></span> 

<span data-ttu-id="dbcf9-111">`stackalloc` est similaire à [_alloca](/cpp/c-runtime-library/reference/alloca) dans la bibliothèque Runtime C.</span><span class="sxs-lookup"><span data-stu-id="dbcf9-111">`stackalloc` is like [_alloca](/cpp/c-runtime-library/reference/alloca) in the C run-time library.</span></span>

## <a name="examples"></a><span data-ttu-id="dbcf9-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="dbcf9-112">Examples</span></span>

<span data-ttu-id="dbcf9-113">L’exemple suivant calcule et affiche les 20 premiers nombres de la suite de Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="dbcf9-113">The following example calculates and displays the first 20 numbers in the Fibonacci sequence.</span></span> <span data-ttu-id="dbcf9-114">Chaque nombre est la somme des deux nombres précédents.</span><span class="sxs-lookup"><span data-stu-id="dbcf9-114">Each number is the sum of the previous two numbers.</span></span> <span data-ttu-id="dbcf9-115">Dans le code, un bloc de mémoire de taille suffisante pour contenir 20 éléments de type `int` est alloué sur la pile, et non sur le tas.</span><span class="sxs-lookup"><span data-stu-id="dbcf9-115">In the code, a block of memory of sufficient size to contain 20 elements of type `int` is allocated on the stack, not the heap.</span></span> <span data-ttu-id="dbcf9-116">L’adresse du bloc est stockée dans le pointeur `fib`.</span><span class="sxs-lookup"><span data-stu-id="dbcf9-116">The address of the block is stored in the pointer `fib`.</span></span> <span data-ttu-id="dbcf9-117">Cette mémoire n’est pas soumise au garbage collection et n’est donc pas tenue d’être épinglée (en utilisant [fixed](fixed-statement.md)).</span><span class="sxs-lookup"><span data-stu-id="dbcf9-117">This memory is not subject to garbage collection and therefore does not have to be pinned (by using [fixed](fixed-statement.md)).</span></span> <span data-ttu-id="dbcf9-118">La durée de vie du bloc de mémoire est limitée à la durée de vie de la méthode qui le définit.</span><span class="sxs-lookup"><span data-stu-id="dbcf9-118">The lifetime of the memory block is limited to the lifetime of the method that defines it.</span></span> <span data-ttu-id="dbcf9-119">Vous ne pouvez pas libérer la mémoire avant le retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="dbcf9-119">You cannot free the memory before the method returns.</span></span>

[!code-csharp[csrefKeywordsOperator#15](../../../../samples/snippets/csharp/keywords/StackAllocExamples.cs#1)]

<span data-ttu-id="dbcf9-120">L’exemple suivant initialise un tableau `stackalloc` d’entiers sur un masque de bits où un bit est défini dans chaque élément.</span><span class="sxs-lookup"><span data-stu-id="dbcf9-120">The following example initializes a `stackalloc` array of integers to a bit mask with one bit set in each element.</span></span> <span data-ttu-id="dbcf9-121">Cela illustre la nouvelle syntaxe d’initialiseur disponible à partir de C# 7.3 :</span><span class="sxs-lookup"><span data-stu-id="dbcf9-121">This demonstrates the new initializer syntax available starting in C# 7.3:</span></span>

[!code-csharp[csrefKeywordsOperator#15](../../../../samples/snippets/csharp/keywords/StackAllocExamples.cs#2)]

## <a name="security"></a><span data-ttu-id="dbcf9-122">Sécurité</span><span class="sxs-lookup"><span data-stu-id="dbcf9-122">Security</span></span>

<span data-ttu-id="dbcf9-123">Le code unsafe est moins sûr que les alternatives safe.</span><span class="sxs-lookup"><span data-stu-id="dbcf9-123">Unsafe code is less secure than safe alternatives.</span></span> <span data-ttu-id="dbcf9-124">Toutefois, l’utilisation de `stackalloc` active automatiquement les fonctionnalités de détection des dépassements de mémoire tampon dans le Common Language Runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="dbcf9-124">However, the use of `stackalloc` automatically enables buffer overrun detection features in the common language runtime (CLR).</span></span> <span data-ttu-id="dbcf9-125">Si un dépassement de mémoire tampon est détecté, le processus est terminé aussi rapidement que possible pour réduire les risques d’exécution de code malveillant.</span><span class="sxs-lookup"><span data-stu-id="dbcf9-125">If a buffer overrun is detected, the process is terminated as quickly as possible to minimize the chance that malicious code is executed.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="dbcf9-126">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="dbcf9-126">C# Language Specification</span></span>
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="dbcf9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbcf9-127">See Also</span></span>
 [<span data-ttu-id="dbcf9-128">Référence C#</span><span class="sxs-lookup"><span data-stu-id="dbcf9-128">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="dbcf9-129">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="dbcf9-129">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="dbcf9-130">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="dbcf9-130">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="dbcf9-131">Mots clés des opérateurs</span><span class="sxs-lookup"><span data-stu-id="dbcf9-131">Operator Keywords</span></span>](../../../csharp/language-reference/keywords/operator-keywords.md)  
 [<span data-ttu-id="dbcf9-132">Pointeurs et code unsafe</span><span class="sxs-lookup"><span data-stu-id="dbcf9-132">Unsafe Code and Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/index.md)
