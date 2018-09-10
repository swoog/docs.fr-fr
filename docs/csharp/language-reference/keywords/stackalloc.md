---
title: stackalloc (référence C#)
ms.date: 04/12/2018
f1_keywords:
- stackalloc_CSharpKeyword
- stackalloc
helpviewer_keywords:
- stackalloc keyword [C#]
ms.openlocfilehash: 5926550eea1f5a2f8fb74645f22ca54c2bed3136
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43508578"
---
# <a name="stackalloc-c-reference"></a><span data-ttu-id="b10b5-102">stackalloc (référence C#)</span><span class="sxs-lookup"><span data-stu-id="b10b5-102">stackalloc (C# Reference)</span></span>
<span data-ttu-id="b10b5-103">Le mot clé `stackalloc` est utilisé dans un contexte de code unsafe pour allouer un bloc de mémoire sur la pile.</span><span class="sxs-lookup"><span data-stu-id="b10b5-103">The `stackalloc` keyword is used in an unsafe code context to allocate a block of memory on the stack.</span></span>

```csharp
int* block = stackalloc int[100];
```

## <a name="remarks"></a><span data-ttu-id="b10b5-104">Notes</span><span class="sxs-lookup"><span data-stu-id="b10b5-104">Remarks</span></span>

<span data-ttu-id="b10b5-105">Le mot clé est valide uniquement dans les initialiseurs de variable locale.</span><span class="sxs-lookup"><span data-stu-id="b10b5-105">The keyword is valid only in local variable initializers.</span></span> <span data-ttu-id="b10b5-106">Le code suivant génère des erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="b10b5-106">The following code causes compiler errors.</span></span>

```csharp
int* block;
// The following assignment statement causes compiler errors. You
// can use stackalloc only when declaring and initializing a local
// variable.
block = stackalloc int[100];
```

<span data-ttu-id="b10b5-107">Dans C# 7.3 et les versions ultérieures, vous pouvez utiliser la syntaxe d’initialiseur de tableau pour les tableaux `stackalloc`.</span><span class="sxs-lookup"><span data-stu-id="b10b5-107">Beginning with C# 7.3, you can use array initializer syntax for `stackalloc` arrays.</span></span> <span data-ttu-id="b10b5-108">Toutes les déclarations suivantes déclarent un tableau de trois éléments ayant pour valeurs les entiers `1`, `2` et `3` :</span><span class="sxs-lookup"><span data-stu-id="b10b5-108">All the following declarations declare an array with three elements whose values are the integers `1`, `2`, and `3`:</span></span>

```csharp
// Valid starting with C# 7.3
int* first = stackalloc int[3] { 1, 2, 3 };
int* second = stackalloc int[] { 1, 2, 3 };
int* third = stackalloc[] { 1, 2, 3 };
```

<span data-ttu-id="b10b5-109">Des types pointeur étant impliqués, `stackalloc` requiert un contexte [unsafe](unsafe.md).</span><span class="sxs-lookup"><span data-stu-id="b10b5-109">Because pointer types are involved, `stackalloc` requires an [unsafe](unsafe.md) context.</span></span> <span data-ttu-id="b10b5-110">Pour plus d’informations, consultez [Pointeurs et code unsafe](../../programming-guide/unsafe-code-pointers/index.md)</span><span class="sxs-lookup"><span data-stu-id="b10b5-110">For more information, see [Unsafe Code and Pointers](../../programming-guide/unsafe-code-pointers/index.md)</span></span> 

<span data-ttu-id="b10b5-111">`stackalloc` est similaire à [_alloca](/cpp/c-runtime-library/reference/alloca) dans la bibliothèque Runtime C.</span><span class="sxs-lookup"><span data-stu-id="b10b5-111">`stackalloc` is like [_alloca](/cpp/c-runtime-library/reference/alloca) in the C run-time library.</span></span>

## <a name="examples"></a><span data-ttu-id="b10b5-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="b10b5-112">Examples</span></span>

<span data-ttu-id="b10b5-113">L’exemple suivant calcule et affiche les 20 premiers nombres de la suite de Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="b10b5-113">The following example calculates and displays the first 20 numbers in the Fibonacci sequence.</span></span> <span data-ttu-id="b10b5-114">Chaque nombre est la somme des deux nombres précédents.</span><span class="sxs-lookup"><span data-stu-id="b10b5-114">Each number is the sum of the previous two numbers.</span></span> <span data-ttu-id="b10b5-115">Dans le code, un bloc de mémoire de taille suffisante pour contenir 20 éléments de type `int` est alloué sur la pile, et non sur le tas.</span><span class="sxs-lookup"><span data-stu-id="b10b5-115">In the code, a block of memory of sufficient size to contain 20 elements of type `int` is allocated on the stack, not the heap.</span></span> <span data-ttu-id="b10b5-116">L’adresse du bloc est stockée dans le pointeur `fib`.</span><span class="sxs-lookup"><span data-stu-id="b10b5-116">The address of the block is stored in the pointer `fib`.</span></span> <span data-ttu-id="b10b5-117">Cette mémoire n’est pas soumise au garbage collection et n’est donc pas tenue d’être épinglée (en utilisant [fixed](fixed-statement.md)).</span><span class="sxs-lookup"><span data-stu-id="b10b5-117">This memory is not subject to garbage collection and therefore does not have to be pinned (by using [fixed](fixed-statement.md)).</span></span> <span data-ttu-id="b10b5-118">La durée de vie du bloc de mémoire est limitée à la durée de vie de la méthode qui le définit.</span><span class="sxs-lookup"><span data-stu-id="b10b5-118">The lifetime of the memory block is limited to the lifetime of the method that defines it.</span></span> <span data-ttu-id="b10b5-119">Vous ne pouvez pas libérer la mémoire avant le retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="b10b5-119">You cannot free the memory before the method returns.</span></span>

[!code-csharp[csrefKeywordsOperator#15](../../../../samples/snippets/csharp/keywords/StackAllocExamples.cs#1)]

<span data-ttu-id="b10b5-120">L’exemple suivant initialise un tableau `stackalloc` d’entiers sur un masque de bits où un bit est défini dans chaque élément.</span><span class="sxs-lookup"><span data-stu-id="b10b5-120">The following example initializes a `stackalloc` array of integers to a bit mask with one bit set in each element.</span></span> <span data-ttu-id="b10b5-121">Cela illustre la nouvelle syntaxe d’initialiseur disponible à partir de C# 7.3 :</span><span class="sxs-lookup"><span data-stu-id="b10b5-121">This demonstrates the new initializer syntax available starting in C# 7.3:</span></span>

[!code-csharp[csrefKeywordsOperator#15](../../../../samples/snippets/csharp/keywords/StackAllocExamples.cs#2)]

## <a name="security"></a><span data-ttu-id="b10b5-122">Sécurité</span><span class="sxs-lookup"><span data-stu-id="b10b5-122">Security</span></span>

<span data-ttu-id="b10b5-123">Le code unsafe est moins sûr que les alternatives safe.</span><span class="sxs-lookup"><span data-stu-id="b10b5-123">Unsafe code is less secure than safe alternatives.</span></span> <span data-ttu-id="b10b5-124">Toutefois, l’utilisation de `stackalloc` active automatiquement les fonctionnalités de détection des dépassements de mémoire tampon dans le Common Language Runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="b10b5-124">However, the use of `stackalloc` automatically enables buffer overrun detection features in the common language runtime (CLR).</span></span> <span data-ttu-id="b10b5-125">Si un dépassement de mémoire tampon est détecté, le processus est terminé aussi rapidement que possible pour réduire les risques d’exécution de code malveillant.</span><span class="sxs-lookup"><span data-stu-id="b10b5-125">If a buffer overrun is detected, the process is terminated as quickly as possible to minimize the chance that malicious code is executed.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="b10b5-126">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="b10b5-126">C# Language Specification</span></span>
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="b10b5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b10b5-127">See Also</span></span>

- [<span data-ttu-id="b10b5-128">Référence C#</span><span class="sxs-lookup"><span data-stu-id="b10b5-128">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="b10b5-129">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b10b5-129">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="b10b5-130">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="b10b5-130">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="b10b5-131">Mots clés des opérateurs</span><span class="sxs-lookup"><span data-stu-id="b10b5-131">Operator Keywords</span></span>](../../../csharp/language-reference/keywords/operator-keywords.md)  
- [<span data-ttu-id="b10b5-132">Pointeurs et code unsafe</span><span class="sxs-lookup"><span data-stu-id="b10b5-132">Unsafe Code and Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/index.md)
