---
title: foreach, instruction (C#)
ms.date: 06/29/2018
f1_keywords:
- foreach
- foreach_CSharpKeyword
helpviewer_keywords:
- foreach keyword [C#]
- foreach statement [C#]
- in keyword [C#]
ms.assetid: 5a9c5ddc-5fd3-457a-9bb6-9abffcd874ec
ms.openlocfilehash: d84c68eb102d55b31ba20a6b6b5c01b96963924d
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43405848"
---
# <a name="foreach-in-c-reference"></a><span data-ttu-id="03b99-102">foreach, instruction (C#)</span><span class="sxs-lookup"><span data-stu-id="03b99-102">foreach, in (C# reference)</span></span>

<span data-ttu-id="03b99-103">L’instruction `foreach` exécute une instruction ou un bloc d’instructions pour chaque élément d’une instance du type qui implémente l’interface <xref:System.Collections.IEnumerable?displayProperty=nameWithType> ou <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="03b99-103">The `foreach` statement executes a statement or a block of statements for each element in an instance of the type that implements the <xref:System.Collections.IEnumerable?displayProperty=nameWithType> or <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> interface.</span></span> <span data-ttu-id="03b99-104">L’instruction `foreach` n’est pas limitée à ces types et peut être appliquée à une instance de n’importe quel type répondant aux conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="03b99-104">The `foreach` statement is not limited to those types and can be applied to an instance of any type that satisfies the following conditions:</span></span>

- <span data-ttu-id="03b99-105">comporte la méthode `GetEnumerator` sans paramètre publique dont le retour est de type classe, struct ou interface,</span><span class="sxs-lookup"><span data-stu-id="03b99-105">has the public parameterless `GetEnumerator` method whose return type is either class, struct, or interface type,</span></span>
- <span data-ttu-id="03b99-106">le type de retour de la méthode `GetEnumerator` contient la propriété publique `Current` et la méthode sans paramètre publique `MoveNext`, dont le type de retour est <xref:System.Boolean>.</span><span class="sxs-lookup"><span data-stu-id="03b99-106">the return type of the `GetEnumerator` method has the public `Current` property and the public parameterless `MoveNext` method whose return type is <xref:System.Boolean>.</span></span>

<span data-ttu-id="03b99-107">À tout moment dans le bloc d’instructions `foreach`, vous pouvez sortir de la boucle à l’aide de l’instruction [break](break.md), ou passer à l’itération suivante de la boucle à l’aide de l’instruction [continue](continue.md).</span><span class="sxs-lookup"><span data-stu-id="03b99-107">At any point within the `foreach` statement block, you can break out of the loop by using the [break](break.md) statement, or step to the next iteration in the loop by using the [continue](continue.md) statement.</span></span> <span data-ttu-id="03b99-108">Vous pouvez également quitter une boucle `foreach` en utilisant les instructions [goto](goto.md), [return](return.md) ou [throw](throw.md).</span><span class="sxs-lookup"><span data-stu-id="03b99-108">You also can exit a `foreach` loop by the [goto](goto.md), [return](return.md), or [throw](throw.md) statements.</span></span>

## <a name="examples"></a><span data-ttu-id="03b99-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="03b99-109">Examples</span></span>

[!INCLUDE[interactive-note](~/includes/csharp-interactive-note.md)]

<span data-ttu-id="03b99-110">L’exemple suivant montre l’utilisation de l’instruction `foreach` avec une instance de type <xref:System.Collections.Generic.List%601> qui implémente l’interface <xref:System.Collections.Generic.IEnumerable%601> :</span><span class="sxs-lookup"><span data-stu-id="03b99-110">The following example shows usage of the `foreach` statement with an instance of the <xref:System.Collections.Generic.List%601> type that implements the <xref:System.Collections.Generic.IEnumerable%601> interface:</span></span>

[!code-csharp-interactive[list example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#1)]

<span data-ttu-id="03b99-111">L’exemple suivant utilise l’instruction `foreach` avec une instance de type <xref:System.Span%601?displayProperty=nameWithType> qui n’implémente aucune interface :</span><span class="sxs-lookup"><span data-stu-id="03b99-111">The next example uses the `foreach` statement with an instance of the <xref:System.Span%601?displayProperty=nameWithType> type, which doesn't implement any interfaces:</span></span>

[!code-csharp-interactive[span example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#2)]

<span data-ttu-id="03b99-112">À partir de C# 7.3, si la propriété `Current` de l’énumérateur retourne une [valeur de retour de référence](../../programming-guide/classes-and-structs/ref-returns.md) (`ref T` où `T` est le type de l’élément de collection), vous pouvez déclarer la variable d’itération avec le modificateur `ref` ou `ref readonly`.</span><span class="sxs-lookup"><span data-stu-id="03b99-112">Beginning with C# 7.3, if the enumerator's `Current` property returns a [reference return value](../../programming-guide/classes-and-structs/ref-returns.md) (`ref T` where `T` is the type of the collection element), you can declare the iteration variable with the `ref` or `ref readonly` modifier.</span></span> <span data-ttu-id="03b99-113">L’exemple suivant utilise une variable d’itération `ref` pour définir la valeur de chaque élément dans un tableau stackalloc.</span><span class="sxs-lookup"><span data-stu-id="03b99-113">The following example uses a `ref` iteration variable to set the value of each item in a stackalloc array.</span></span> <span data-ttu-id="03b99-114">La version `ref readonly` effectue une itération de la collection pour imprimer toutes les valeurs.</span><span class="sxs-lookup"><span data-stu-id="03b99-114">The `ref readonly` version iterates the collection to print all the values.</span></span> <span data-ttu-id="03b99-115">La déclaration `readonly` utilise une déclaration de variable locale implicite.</span><span class="sxs-lookup"><span data-stu-id="03b99-115">The `readonly` declaration uses an implicit local variable declaration.</span></span> <span data-ttu-id="03b99-116">Les déclarations de variable implicite peuvent être utilisées avec les déclarations `ref` ou `ref readonly`, tout comme les déclarations de variable explicitement typée.</span><span class="sxs-lookup"><span data-stu-id="03b99-116">Implicit variable declarations can be used with either `ref` or `ref readonly` declarations, as can explicitly typed variable declarations.</span></span>

[!code-csharp-interactive[ref span example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#RefSpan)]

## <a name="c-language-specification"></a><span data-ttu-id="03b99-117">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="03b99-117">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="03b99-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03b99-118">See also</span></span>

- [<span data-ttu-id="03b99-119">L’instruction foreach (spécification du langage C#)</span><span class="sxs-lookup"><span data-stu-id="03b99-119">The foreach statement (C# language specification)</span></span>](/dotnet/csharp/language-reference/language-specification/statements#the-foreach-statement)
- [<span data-ttu-id="03b99-120">Utilisation de foreach avec des tableaux</span><span class="sxs-lookup"><span data-stu-id="03b99-120">Using foreach with Arrays</span></span>](../../programming-guide/arrays/using-foreach-with-arrays.md)
- [<span data-ttu-id="03b99-121">for</span><span class="sxs-lookup"><span data-stu-id="03b99-121">for</span></span>](for.md)
- [<span data-ttu-id="03b99-122">Instructions d’itération</span><span class="sxs-lookup"><span data-stu-id="03b99-122">Iteration Statements</span></span>](iteration-statements.md)
- [<span data-ttu-id="03b99-123">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="03b99-123">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="03b99-124">Référence C#</span><span class="sxs-lookup"><span data-stu-id="03b99-124">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="03b99-125">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="03b99-125">C# Programming Guide</span></span>](../../programming-guide/index.md)
