---
title: '[], opérateur - Référence C#'
ms.custom: seodec18
ms.date: 01/10/2019
f1_keywords:
- '[]_CSharpKeyword'
helpviewer_keywords:
- subscript operator [C#]
- square brackets [ ] operator [C#]
- '[] operator [C#]'
- indexing operator [C#]
ms.assetid: 5c16bb45-88f7-45ff-b42c-1af1972b042c
ms.openlocfilehash: 9088393f61d300ee76e56e320bec17b4a79bfebb
ms.sourcegitcommit: bd28ff1e312eaba9718c4f7ea272c2d4781a7cac
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56835588"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="ef5d4-102">[], opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="ef5d4-102">[] operator (C# Reference)</span></span>

<span data-ttu-id="ef5d4-103">Les crochets, `[]`, sont généralement utilisés pour l’accès à un élément tableau, indexeur ou pointeur.</span><span class="sxs-lookup"><span data-stu-id="ef5d4-103">Square brackets, `[]`, are typically used for array, indexer, or pointer element access.</span></span>

<span data-ttu-id="ef5d4-104">Pour plus d’informations sur l’accès aux éléments pointeur, consultez [Guide pratique pour accéder à un élément de tableau à l’aide d’un pointeur](../../programming-guide/unsafe-code-pointers/how-to-access-an-array-element-with-a-pointer.md).</span><span class="sxs-lookup"><span data-stu-id="ef5d4-104">For more information about pointer element access, see [How to: access an array element with a pointer](../../programming-guide/unsafe-code-pointers/how-to-access-an-array-element-with-a-pointer.md).</span></span>

<span data-ttu-id="ef5d4-105">Vous utilisez également des crochets pour spécifier des [attributs](../../programming-guide/concepts/attributes/index.md) :</span><span class="sxs-lookup"><span data-stu-id="ef5d4-105">You also use square brackets to specify [attributes](../../programming-guide/concepts/attributes/index.md):</span></span>

```csharp
[System.Diagnostics.Conditional("DEBUG")]
void TraceMethod() {}
```

## <a name="array-access"></a><span data-ttu-id="ef5d4-106">Accès aux tableaux</span><span class="sxs-lookup"><span data-stu-id="ef5d4-106">Array access</span></span>

<span data-ttu-id="ef5d4-107">L’exemple suivant montre comment accéder à des éléments tableau :</span><span class="sxs-lookup"><span data-stu-id="ef5d4-107">The following example demonstrates how to access array elements:</span></span>

[!code-csharp-interactive[array access](~/samples/snippets/csharp/language-reference/operators/IndexOperatorExamples.cs#Arrays)]

<span data-ttu-id="ef5d4-108">Si un index de tableau est en dehors des limites de la dimension correspondante d’un tableau, une <xref:System.IndexOutOfRangeException> est levée.</span><span class="sxs-lookup"><span data-stu-id="ef5d4-108">If an array index is outside the bounds of the corresponding dimension of an array, an <xref:System.IndexOutOfRangeException> is thrown.</span></span>

<span data-ttu-id="ef5d4-109">Comme le montre l’exemple précédent, vous utilisez également des crochets dans la déclaration d’un type tableau et l’instanciation des instances de tableau.</span><span class="sxs-lookup"><span data-stu-id="ef5d4-109">As the preceding example shows, you also use square brackets in declaration of an array type and instantiation of array instances.</span></span>

<span data-ttu-id="ef5d4-110">Pour plus d’informations sur les tableaux, consultez [Tableaux](../../programming-guide/arrays/index.md).</span><span class="sxs-lookup"><span data-stu-id="ef5d4-110">For more information about arrays, see [Arrays](../../programming-guide/arrays/index.md).</span></span>

## <a name="indexer-access"></a><span data-ttu-id="ef5d4-111">Accès aux indexeurs</span><span class="sxs-lookup"><span data-stu-id="ef5d4-111">Indexer access</span></span>

<span data-ttu-id="ef5d4-112">L’exemple suivant utilise le type .NET <xref:System.Collections.Generic.Dictionary%602> afin d’illustrer l’accès aux indexeurs :</span><span class="sxs-lookup"><span data-stu-id="ef5d4-112">The following example uses .NET <xref:System.Collections.Generic.Dictionary%602> type to demonstrate indexer access:</span></span>

[!code-csharp-interactive[indexer access](~/samples/snippets/csharp/language-reference/operators/IndexOperatorExamples.cs#Indexers)]

<span data-ttu-id="ef5d4-113">Les indexeurs vous permettent d’indexer des instances d’un type défini par l’utilisateur en procédant de la même façon que pour l’indexation de tableau.</span><span class="sxs-lookup"><span data-stu-id="ef5d4-113">Indexers allow you to index instances of a user-defined type in the similar way as array indexing.</span></span> <span data-ttu-id="ef5d4-114">Contrairement aux index de tableau, qui doivent être des entiers, les arguments d’indexeur peuvent être déclarés comme étant de n’importe quel type.</span><span class="sxs-lookup"><span data-stu-id="ef5d4-114">Unlike array indices, which must be integer, the indexer arguments can be declared to be of any type.</span></span>

<span data-ttu-id="ef5d4-115">Pour plus d’informations sur les indexeurs, consultez [Indexeurs](../../programming-guide/indexers/index.md).</span><span class="sxs-lookup"><span data-stu-id="ef5d4-115">For more information about indexers, see [Indexers](../../programming-guide/indexers/index.md).</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="ef5d4-116">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="ef5d4-116">Operator overloadability</span></span>

<span data-ttu-id="ef5d4-117">L’opérateur d’accès à un élément `[]` n’est pas considéré comme un opérateur surchargeable.</span><span class="sxs-lookup"><span data-stu-id="ef5d4-117">Element access `[]` is not considered an overloadable operator.</span></span> <span data-ttu-id="ef5d4-118">Utilisez des [indexeurs](../../programming-guide/indexers/index.md) pour prendre en charge l’indexation avec des types définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ef5d4-118">Use [indexers](../../programming-guide/indexers/index.md) to support indexing with user-defined types.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="ef5d4-119">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="ef5d4-119">C# language specification</span></span>

<span data-ttu-id="ef5d4-120">Pour plus d’informations, consultez les sections [Accès à un élément](~/_csharplang/spec/expressions.md#element-access) et [Accès aux éléments de pointeur](~/_csharplang/spec/unsafe-code.md#pointer-element-access) de la [Spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="ef5d4-120">For more information, see the [Element access](~/_csharplang/spec/expressions.md#element-access) and [Pointer element access](~/_csharplang/spec/unsafe-code.md#pointer-element-access) sections of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ef5d4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef5d4-121">See also</span></span>

- [<span data-ttu-id="ef5d4-122">Référence C#</span><span class="sxs-lookup"><span data-stu-id="ef5d4-122">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="ef5d4-123">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="ef5d4-123">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="ef5d4-124">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="ef5d4-124">C# Operators</span></span>](index.md)
- [<span data-ttu-id="ef5d4-125">Tableaux</span><span class="sxs-lookup"><span data-stu-id="ef5d4-125">Arrays</span></span>](../../programming-guide/arrays/index.md)
- [<span data-ttu-id="ef5d4-126">Indexeurs</span><span class="sxs-lookup"><span data-stu-id="ef5d4-126">Indexers</span></span>](../../programming-guide/indexers/index.md)
- [<span data-ttu-id="ef5d4-127">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="ef5d4-127">Pointer types</span></span>](../../programming-guide/unsafe-code-pointers/pointer-types.md)
- [<span data-ttu-id="ef5d4-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="ef5d4-128">Attributes</span></span>](../../programming-guide/concepts/attributes/index.md)
- <span data-ttu-id="ef5d4-129">[Opérateurs ?. et ?[]](null-conditional-operators.md)</span><span class="sxs-lookup"><span data-stu-id="ef5d4-129">[?. and ?[] operators](null-conditional-operators.md)</span></span>