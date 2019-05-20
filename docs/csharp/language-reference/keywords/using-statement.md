---
title: using, instruction - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- using statement [C#]
ms.assetid: afc355e6-f0b9-4240-94dd-0d93f17d9fc3
ms.openlocfilehash: e1a1a960fa69be593ea01cab51be576b0055fd5e
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65632900"
---
# <a name="using-statement-c-reference"></a><span data-ttu-id="2c5d8-102">using, instruction (référence C#)</span><span class="sxs-lookup"><span data-stu-id="2c5d8-102">using statement (C# Reference)</span></span>

<span data-ttu-id="2c5d8-103">Fournit une syntaxe pratique qui garantit l’utilisation correcte d’objets <xref:System.IDisposable>.</span><span class="sxs-lookup"><span data-stu-id="2c5d8-103">Provides a convenient syntax that ensures the correct use of <xref:System.IDisposable> objects.</span></span>

## <a name="example"></a><span data-ttu-id="2c5d8-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="2c5d8-104">Example</span></span>

<span data-ttu-id="2c5d8-105">L’exemple suivant montre comment utiliser l’instruction `using`.</span><span class="sxs-lookup"><span data-stu-id="2c5d8-105">The following example shows how to use the `using` statement.</span></span>

[!code-csharp[csrefKeywordsNamespace#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsNamespace/CS/csrefKeywordsNamespace.cs#4)]

## <a name="remarks"></a><span data-ttu-id="2c5d8-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="2c5d8-106">Remarks</span></span>

<span data-ttu-id="2c5d8-107"><xref:System.IO.File> et <xref:System.Drawing.Font> sont des exemples de types managés qui accèdent à des ressources non managées (dans le cas présent, des handles de fichiers et des contextes d’appareil).</span><span class="sxs-lookup"><span data-stu-id="2c5d8-107"><xref:System.IO.File> and <xref:System.Drawing.Font> are examples of managed types that access unmanaged resources (in this case file handles and device contexts).</span></span> <span data-ttu-id="2c5d8-108">Beaucoup d’autres types de ressources non managées et de bibliothèques de classes peuvent les encapsuler.</span><span class="sxs-lookup"><span data-stu-id="2c5d8-108">There are many other kinds of unmanaged resources and class library types that encapsulate them.</span></span> <span data-ttu-id="2c5d8-109">Tous les types de cette sorte doivent implémentent l’interface <xref:System.IDisposable>.</span><span class="sxs-lookup"><span data-stu-id="2c5d8-109">All such types must implement the <xref:System.IDisposable> interface.</span></span>

<span data-ttu-id="2c5d8-110">Quand la durée de vie d’un objet `IDisposable` est limitée à une seule méthode, vous devez le déclarer et l’instancier dans l’instruction `using`.</span><span class="sxs-lookup"><span data-stu-id="2c5d8-110">When the lifetime of an `IDisposable` object is limited to a single method, you should declare and instantiate it in the `using` statement.</span></span> <span data-ttu-id="2c5d8-111">L’instruction `using` appelle la méthode <xref:System.IDisposable.Dispose%2A> correctement sur l’objet et, quand vous l’utilisez comme indiqué précédemment, elle met également l’objet lui-même hors de portée dès que <xref:System.IDisposable.Dispose%2A> est appelée.</span><span class="sxs-lookup"><span data-stu-id="2c5d8-111">The `using` statement calls the <xref:System.IDisposable.Dispose%2A> method on the object in the correct way, and (when you use it as shown earlier) it also causes the object itself to go out of scope as soon as <xref:System.IDisposable.Dispose%2A> is called.</span></span> <span data-ttu-id="2c5d8-112">Dans le bloc `using`, l’objet est en lecture seule et ne peut être ni modifié ni réassigné.</span><span class="sxs-lookup"><span data-stu-id="2c5d8-112">Within the `using` block, the object is read-only and cannot be modified or reassigned.</span></span>

<span data-ttu-id="2c5d8-113">L’instruction `using` garantit que <xref:System.IDisposable.Dispose%2A> est appelée même si une exception se produit dans le bloc `using`.</span><span class="sxs-lookup"><span data-stu-id="2c5d8-113">The `using` statement ensures that <xref:System.IDisposable.Dispose%2A> is called even if an exception occurs within the `using` block.</span></span> <span data-ttu-id="2c5d8-114">Vous pouvez obtenir le même résultat en plaçant l’objet dans un bloc `try`, puis en appelant <xref:System.IDisposable.Dispose%2A> dans un bloc `finally` ; c’est d’ailleurs ainsi que l’instruction `using` est traduite par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="2c5d8-114">You can achieve the same result by putting the object inside a `try` block and then calling <xref:System.IDisposable.Dispose%2A> in a `finally` block; in fact, this is how the `using` statement is translated by the compiler.</span></span> <span data-ttu-id="2c5d8-115">L’exemple de code précédent se développe pour donner le code suivant au moment de la compilation (notez les accolades supplémentaires pour créer la portée limitée de l’objet) :</span><span class="sxs-lookup"><span data-stu-id="2c5d8-115">The code example earlier expands to the following code at compile time (note the extra curly braces to create the limited scope for the object):</span></span>

[!code-csharp[csrefKeywordsNamespace#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsNamespace/CS/csrefKeywordsNamespace.cs#5)]

<span data-ttu-id="2c5d8-116">Pour plus d’informations sur l’instruction `try`-`finally`, consultez la rubrique [try-finally](try-finally.md).</span><span class="sxs-lookup"><span data-stu-id="2c5d8-116">For more information about the `try`-`finally` statement, see the [try-finally](try-finally.md) topic.</span></span>

<span data-ttu-id="2c5d8-117">Vous pouvez déclarer plusieurs instances d’un type dans l’instruction `using`, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="2c5d8-117">Multiple instances of a type can be declared in the `using` statement, as shown in the following example:</span></span>

[!code-csharp[csrefKeywordsNamespace#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsNamespace/CS/csrefKeywordsNamespace.cs#6)]

<span data-ttu-id="2c5d8-118">Il n’est pas recommandé d’instancier l’objet de ressource, puis de passer la variable à l’instruction `using`.</span><span class="sxs-lookup"><span data-stu-id="2c5d8-118">You can instantiate the resource object and then pass the variable to the `using` statement, but this is not a best practice.</span></span> <span data-ttu-id="2c5d8-119">Dans ce cas, une fois que le contrôle a quitté le bloc `using`, l’objet reste dans la portée mais n’a probablement pas accès à ses ressources non managées.</span><span class="sxs-lookup"><span data-stu-id="2c5d8-119">In this case, after control leaves the `using` block, the object remains in scope but probably has no access to its unmanaged resources.</span></span> <span data-ttu-id="2c5d8-120">En d’autres termes, il n’est plus complètement initialisé.</span><span class="sxs-lookup"><span data-stu-id="2c5d8-120">In other words, it's not fully initialized anymore.</span></span> <span data-ttu-id="2c5d8-121">Si vous essayez d’utiliser l’objet à l’extérieur du bloc `using`, vous risquez de provoquer la levée d’une exception.</span><span class="sxs-lookup"><span data-stu-id="2c5d8-121">If you try to use the object outside the `using` block, you risk causing an exception to be thrown.</span></span> <span data-ttu-id="2c5d8-122">C’est pourquoi il est généralement préférable d’instancier l’objet dans l’instruction `using` et de limiter sa portée au bloc `using`.</span><span class="sxs-lookup"><span data-stu-id="2c5d8-122">For this reason, it's generally better to instantiate the object in the `using` statement and limit its scope to the `using` block.</span></span>

[!code-csharp[csrefKeywordsNamespace#7](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsNamespace/CS/csrefKeywordsNamespace.cs#7)]

<span data-ttu-id="2c5d8-123">Pour plus d’informations sur la suppression d’objets `IDisposable`, consultez [Utilisation d’objets qui implémentent IDisposable](../../../standard/garbage-collection/using-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2c5d8-123">For more information about disposing of `IDisposable` objects, see [Using objects that implement IDisposable](../../../standard/garbage-collection/using-objects.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="2c5d8-124">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="2c5d8-124">C# language specification</span></span>

<span data-ttu-id="2c5d8-125">Pour plus d’informations, consultez [Instruction using](~/_csharplang/spec/statements.md#the-using-statement) dans la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="2c5d8-125">For more information, see [The using statement](~/_csharplang/spec/statements.md#the-using-statement) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="2c5d8-126">La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="2c5d8-126">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c5d8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c5d8-127">See also</span></span>

- [<span data-ttu-id="2c5d8-128">Référence C#</span><span class="sxs-lookup"><span data-stu-id="2c5d8-128">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="2c5d8-129">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="2c5d8-129">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="2c5d8-130">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="2c5d8-130">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="2c5d8-131">using, directive</span><span class="sxs-lookup"><span data-stu-id="2c5d8-131">using Directive</span></span>](using-directive.md)
- [<span data-ttu-id="2c5d8-132">Nettoyage de la mémoire</span><span class="sxs-lookup"><span data-stu-id="2c5d8-132">Garbage Collection</span></span>](../../../standard/garbage-collection/index.md)
- [<span data-ttu-id="2c5d8-133">Utilisation d’objets implémentant IDisposable</span><span class="sxs-lookup"><span data-stu-id="2c5d8-133">Using objects that implement IDisposable</span></span>](../../../standard/garbage-collection/using-objects.md)
- [<span data-ttu-id="2c5d8-134">Interface IDisposable</span><span class="sxs-lookup"><span data-stu-id="2c5d8-134">IDisposable interface</span></span>](xref:System.IDisposable)
