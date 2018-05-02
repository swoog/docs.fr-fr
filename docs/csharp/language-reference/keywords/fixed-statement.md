---
title: fixed, instruction (référence C#)
ms.date: 04/20/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- fixed_CSharpKeyword
- fixed
helpviewer_keywords:
- fixed keyword [C#]
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 5dd117461f792ec7a10b740fbad277de52d05623
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="fixed-statement-c-reference"></a><span data-ttu-id="43e0b-102">fixed, instruction (référence C#)</span><span class="sxs-lookup"><span data-stu-id="43e0b-102">fixed Statement (C# Reference)</span></span>

<span data-ttu-id="43e0b-103">L’instruction `fixed` empêche le récupérateur de mémoire de déplacer une variable mobile.</span><span class="sxs-lookup"><span data-stu-id="43e0b-103">The `fixed` statement prevents the garbage collector from relocating a movable variable.</span></span> <span data-ttu-id="43e0b-104">L’instruction `fixed` est uniquement autorisée dans un contexte [unsafe](unsafe.md).</span><span class="sxs-lookup"><span data-stu-id="43e0b-104">The `fixed` statement is only permitted in an [unsafe](unsafe.md) context.</span></span> <span data-ttu-id="43e0b-105">`Fixed` peut également être utilisé pour créer des [mémoires tampons de taille fixe](../../programming-guide/unsafe-code-pointers/fixed-size-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="43e0b-105">`Fixed` can also be used to create [fixed size buffers](../../programming-guide/unsafe-code-pointers/fixed-size-buffers.md).</span></span>

<span data-ttu-id="43e0b-106">L’instruction `fixed` définit un pointeur vers une variable managée et épingle cette variable pendant l’exécution de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="43e0b-106">The `fixed` statement sets a pointer to a managed variable and "pins" that variable during the execution of the statement.</span></span> <span data-ttu-id="43e0b-107">Les pointeurs vers des variables managées ne sont utiles que dans un contexte `fixed`.</span><span class="sxs-lookup"><span data-stu-id="43e0b-107">Pointers to movable managed variables are useful only in a `fixed` context.</span></span> <span data-ttu-id="43e0b-108">Sans contexte `fixed`, le garbage collection peut déplacer les variables de manière imprévisible.</span><span class="sxs-lookup"><span data-stu-id="43e0b-108">Without a `fixed` context, garbage collection could relocate the variables unpredictably.</span></span> <span data-ttu-id="43e0b-109">Le compilateur C# permet seulement d’assigner un pointeur à une variable managée dans une instruction `fixed`.</span><span class="sxs-lookup"><span data-stu-id="43e0b-109">The C# compiler only lets you assign a pointer to a managed variable in a `fixed` statement.</span></span>

[!code-csharp[Accessing fixed memory](../../../../samples/snippets/csharp/keywords/FixedKeywordExamples.cs#1)]

<span data-ttu-id="43e0b-110">Vous pouvez initialiser un pointeur à l’aide d’un tableau, d’une chaîne, d’un tampon de taille fixe ou de l’adresse d’une variable.</span><span class="sxs-lookup"><span data-stu-id="43e0b-110">You can initialize a pointer by using an array, a string, a fixed-size buffer, or the address of a variable.</span></span> <span data-ttu-id="43e0b-111">L’exemple suivant montre l’utilisation des adresses de variables, des tableaux et des chaînes.</span><span class="sxs-lookup"><span data-stu-id="43e0b-111">The following example illustrates the use of variable addresses, arrays, and strings.</span></span> <span data-ttu-id="43e0b-112">Pour plus d’informations sur les mémoires tampons de taille fixe, consultez [Mémoires tampons de taille fixe](../../programming-guide/unsafe-code-pointers/fixed-size-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="43e0b-112">For more information about fixed-size buffers, see [Fixed Size Buffers](../../programming-guide/unsafe-code-pointers/fixed-size-buffers.md).</span></span>

[!code-csharp[Initializing fixed size buffers](../../../../samples/snippets/csharp/keywords/FixedKeywordExamples.cs#2)]

<span data-ttu-id="43e0b-113">Plusieurs pointeurs peuvent être initialisés dans une instruction s’ils sont tous du même type :</span><span class="sxs-lookup"><span data-stu-id="43e0b-113">Multiple pointers can be initialized in one statement if they are all the same type:</span></span>

```csharp
fixed (byte* ps = srcarray, pd = dstarray) {...}
```

<span data-ttu-id="43e0b-114">Pour initialiser des pointeurs de types différents, imbriquez des instructions `fixed`, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="43e0b-114">To initialize pointers of different types, simply nest `fixed` statements, as shown in the following example.</span></span>

[!code-csharp[Initializing multiple pointers](../../../../samples/snippets/csharp/keywords/FixedKeywordExamples.cs#3)]

<span data-ttu-id="43e0b-115">Une fois que le code de l’instruction est exécuté, toutes les variables épinglées sont libérées et soumises au garbage collection.</span><span class="sxs-lookup"><span data-stu-id="43e0b-115">After the code in the statement is executed, any pinned variables are unpinned and subject to garbage collection.</span></span> <span data-ttu-id="43e0b-116">Par conséquent, ne pointez pas vers ces variables en dehors de l’instruction `fixed`.</span><span class="sxs-lookup"><span data-stu-id="43e0b-116">Therefore, do not point to those variables outside the `fixed` statement.</span></span> <span data-ttu-id="43e0b-117">La portée des variables déclarées dans l’instruction `fixed` est limitée à cette instruction, ce qui facilite les choses :</span><span class="sxs-lookup"><span data-stu-id="43e0b-117">The variables declared in the `fixed` statement are scoped to that statement, making this easier:</span></span>

```csharp
fixed (byte* ps = srcarray, pd = dstarray)
{
   ...
}
// ps and pd are no longer in scope here.
```

<span data-ttu-id="43e0b-118">Les pointeurs initialisés dans des instructions `fixed` sont des variables en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="43e0b-118">Pointers initialized in `fixed` statements are readonly variables.</span></span> <span data-ttu-id="43e0b-119">Pour modifier la valeur du pointeur, vous devez déclarer une deuxième variable de pointeur et la modifier.</span><span class="sxs-lookup"><span data-stu-id="43e0b-119">If you want to modify the pointer value, you must declare a second pointer variable, and modify that.</span></span> <span data-ttu-id="43e0b-120">La variable déclarée dans l’instruction `fixed` ne peut pas être modifiée :</span><span class="sxs-lookup"><span data-stu-id="43e0b-120">The variable declared in the `fixed` statement cannot be modified:</span></span>

```csharp
fixed (byte* ps = srcarray, pd = dstarray)
{
    byte* pSourceCopy = ps;
    pSourceCopy++; // point to the next element.
    ps++; // invalid: cannot modify ps, as it is declared in the fixed statement.
}
```


<span data-ttu-id="43e0b-121">En mode unsafe, vous pouvez allouer de la mémoire sur la pile, où elle n’est pas soumise au garbage collection et n’a donc pas besoin d’être épinglée.</span><span class="sxs-lookup"><span data-stu-id="43e0b-121">In unsafe mode, you can allocate memory on the stack, where it is not subject to garbage collection and therefore does not need to be pinned.</span></span> <span data-ttu-id="43e0b-122">Pour plus d’informations, consultez [stackalloc](stackalloc.md).</span><span class="sxs-lookup"><span data-stu-id="43e0b-122">For more information, see [stackalloc](stackalloc.md).</span></span>

[!code-csharp[Initializing multiple pointers](../../../../samples/snippets/csharp/keywords/FixedKeywordExamples.cs#4)]

## <a name="c-language-specification"></a><span data-ttu-id="43e0b-123">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="43e0b-123">C# Language Specification</span></span>

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="43e0b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43e0b-124">See Also</span></span>

 [<span data-ttu-id="43e0b-125">Référence C#</span><span class="sxs-lookup"><span data-stu-id="43e0b-125">C# Reference</span></span>](../index.md)  
 [<span data-ttu-id="43e0b-126">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="43e0b-126">C# Programming Guide</span></span>](../../programming-guide/index.md)  
 [<span data-ttu-id="43e0b-127">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="43e0b-127">C# Keywords</span></span>](index.md)  
 [<span data-ttu-id="43e0b-128">unsafe</span><span class="sxs-lookup"><span data-stu-id="43e0b-128">unsafe</span></span>](unsafe.md)  
 [<span data-ttu-id="43e0b-129">Mémoires tampons de taille fixe</span><span class="sxs-lookup"><span data-stu-id="43e0b-129">Fixed Size Buffers</span></span>](../../programming-guide/unsafe-code-pointers/fixed-size-buffers.md)
