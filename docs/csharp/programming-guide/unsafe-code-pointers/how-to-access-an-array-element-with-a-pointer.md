---
title: Guide pratique pour accéder à un élément de tableau à l’aide d’un pointeur - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], array access
ms.assetid: 6c46f2af-a730-4855-8638-f136d9abaa12
ms.openlocfilehash: 59765dbcad6c28cf2ad9f3df2052df19cafd08f1
ms.sourcegitcommit: 75567a3cb437009db55949c6092f4e77ed1a9da4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/15/2019
ms.locfileid: "54307277"
---
# <a name="how-to-access-an-array-element-with-a-pointer-c-programming-guide"></a><span data-ttu-id="50742-102">Guide pratique pour accéder à un élément de tableau à l’aide d’un pointeur (guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="50742-102">How to: access an array element with a pointer (C# Programming Guide)</span></span>

<span data-ttu-id="50742-103">Dans un contexte unsafe, vous pouvez accéder à un élément en mémoire en utilisant l’accès à un élément de pointeur, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="50742-103">In an unsafe context, you can access an element in memory by using pointer element access, as shown in the following example:</span></span>

```csharp
char* charPointer = stackalloc char[123];
for (int i = 65; i < 123; i++)
{
    charPointer[i] = (char)i; //access array elements
}
```

<span data-ttu-id="50742-104">L’expression entre crochets doit être implicitement convertible en `int`, `uint`, `long` ou `ulong`.</span><span class="sxs-lookup"><span data-stu-id="50742-104">The expression in square brackets must be implicitly convertible to `int`, `uint`, `long`, or `ulong`.</span></span> <span data-ttu-id="50742-105">L’opération `p[e]` équivaut à `*(p+e)`.</span><span class="sxs-lookup"><span data-stu-id="50742-105">The operation `p[e]` is equivalent to `*(p+e)`.</span></span> <span data-ttu-id="50742-106">Comme C et C++, l’accès à un élément de pointeur ne recherche pas les erreurs de dépassement des limites.</span><span class="sxs-lookup"><span data-stu-id="50742-106">Like C and C++, the pointer element access does not check for out-of-bounds errors.</span></span>

## <a name="example"></a><span data-ttu-id="50742-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="50742-107">Example</span></span>

<span data-ttu-id="50742-108">Dans cet exemple, 123 emplacements de mémoire sont alloués à un tableau de caractères, `charPointer`.</span><span class="sxs-lookup"><span data-stu-id="50742-108">In this example, 123 memory locations are allocated to a character array, `charPointer`.</span></span> <span data-ttu-id="50742-109">Le tableau est utilisé pour afficher les lettres minuscules et les lettres majuscules dans deux boucles [for](../../../csharp/language-reference/keywords/for.md).</span><span class="sxs-lookup"><span data-stu-id="50742-109">The array is used to display the lowercase letters and the uppercase letters in two [for](../../../csharp/language-reference/keywords/for.md) loops.</span></span>

<span data-ttu-id="50742-110">Remarquez que l’expression `charPointer[i]` équivaut à l’expression `*(charPointer + i)`, et vous pouvez obtenir le même résultat en utilisant l’une ou l’autre expression.</span><span class="sxs-lookup"><span data-stu-id="50742-110">Notice that the expression `charPointer[i]` is equivalent to the expression `*(charPointer + i)`, and you can obtain the same result by using either of the two expressions.</span></span>

[!code-csharp[csProgGuidePointers#11](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-access-an-array-element-with-a-pointer_1.cs)]

[!code-csharp[csProgGuidePointers#12](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-access-an-array-element-with-a-pointer_2.cs)]

<span data-ttu-id="50742-111">**Lettres majuscules :**</span><span class="sxs-lookup"><span data-stu-id="50742-111">**Uppercase letters:**</span></span>  
<span data-ttu-id="50742-112">**ABCDEFGHIJKLMNOPQRSTUVWXYZ**</span><span class="sxs-lookup"><span data-stu-id="50742-112">**ABCDEFGHIJKLMNOPQRSTUVWXYZ**</span></span>  
<span data-ttu-id="50742-113">**Lettres minuscules :**</span><span class="sxs-lookup"><span data-stu-id="50742-113">**Lowercase letters:**</span></span>  
<span data-ttu-id="50742-114">**abcdefghijklmnopqrstuvwxyz**</span><span class="sxs-lookup"><span data-stu-id="50742-114">**abcdefghijklmnopqrstuvwxyz**</span></span>  

## <a name="see-also"></a><span data-ttu-id="50742-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50742-115">See also</span></span>

- [<span data-ttu-id="50742-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="50742-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="50742-117">Expressions de pointeur</span><span class="sxs-lookup"><span data-stu-id="50742-117">Pointer Expressions</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)
- [<span data-ttu-id="50742-118">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="50742-118">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)
- [<span data-ttu-id="50742-119">Types</span><span class="sxs-lookup"><span data-stu-id="50742-119">Types</span></span>](../../../csharp/language-reference/keywords/types.md)
- [<span data-ttu-id="50742-120">unsafe</span><span class="sxs-lookup"><span data-stu-id="50742-120">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)
- [<span data-ttu-id="50742-121">fixed, instruction</span><span class="sxs-lookup"><span data-stu-id="50742-121">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)
- [<span data-ttu-id="50742-122">stackalloc</span><span class="sxs-lookup"><span data-stu-id="50742-122">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
