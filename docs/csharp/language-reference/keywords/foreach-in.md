---
title: foreach, in (référence C#)
ms.date: 05/24/2018
f1_keywords:
- foreach
- foreach_CSharpKeyword
helpviewer_keywords:
- foreach keyword [C#]
- foreach statement [C#]
- in keyword [C#]
ms.assetid: 5a9c5ddc-5fd3-457a-9bb6-9abffcd874ec
ms.openlocfilehash: b6b7dc0a4d3970ddfbbb6635ccebbbd5b75671e4
ms.sourcegitcommit: 54231aa56fca059e9297888a96fbca1d4cf3746c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2018
ms.locfileid: "34549374"
---
# <a name="foreach-in-c-reference"></a><span data-ttu-id="77bab-102">foreach, in (référence C#)</span><span class="sxs-lookup"><span data-stu-id="77bab-102">foreach, in (C# Reference)</span></span>

<span data-ttu-id="77bab-103">L’instruction `foreach` exécute une instruction ou un bloc d’instructions pour chaque élément d’une instance du type qui implémente l’interface <xref:System.Collections.IEnumerable?displayProperty=nameWithType> ou <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="77bab-103">The `foreach` statement executes a statement or a block of statements for each element in an instance of the type that implements the <xref:System.Collections.IEnumerable?displayProperty=nameWithType> or <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> interface.</span></span> <span data-ttu-id="77bab-104">L’instruction `foreach` n’est pas limitée à ces types et peut être appliquée à une instance de n’importe quel type répondant aux conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="77bab-104">The `foreach` statement is not limited to those types and can be applied to an instance of any type that satisfies the following conditions:</span></span>

- <span data-ttu-id="77bab-105">comporte la méthode `GetEnumerator` sans paramètre publique dont le retour est de type classe, struct ou interface,</span><span class="sxs-lookup"><span data-stu-id="77bab-105">has the public parameterless `GetEnumerator` method whose return type is either class, struct, or interface type,</span></span>
- <span data-ttu-id="77bab-106">le type de retour de la méthode `GetEnumerator` contient la propriété publique `Current` et la méthode sans paramètre publique `MoveNext`, dont le type de retour est <xref:System.Boolean>.</span><span class="sxs-lookup"><span data-stu-id="77bab-106">the return type of the `GetEnumerator` method has the public `Current` property and the public parameterless `MoveNext` method whose return type is <xref:System.Boolean>.</span></span>

<span data-ttu-id="77bab-107">Vous pouvez quitter la boucle à n’importe quel endroit du bloc d’instruction `foreach` à l’aide du mot clé [break](break.md), ou passer à l’itération suivante de la boucle à l’aide du mot clé [continue](continue.md).</span><span class="sxs-lookup"><span data-stu-id="77bab-107">At any point within the `foreach` statement block, you can break out of the loop by using the [break](break.md) keyword, or step to the next iteration in the loop by using the [continue](continue.md) keyword.</span></span> <span data-ttu-id="77bab-108">Vous pouvez également quitter une boucle `foreach` en utilisant les instructions [goto](goto.md), [return](return.md) ou [throw](throw.md).</span><span class="sxs-lookup"><span data-stu-id="77bab-108">You also can exit a `foreach` loop by the [goto](goto.md), [return](return.md), or [throw](throw.md) statements.</span></span>

## <a name="examples"></a><span data-ttu-id="77bab-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="77bab-109">Examples</span></span>

[!INCLUDE[interactive-note](~/includes/csharp-interactive-note.md)]

<span data-ttu-id="77bab-110">L’exemple suivant montre l’utilisation de l’instruction `foreach` avec une instance de type <xref:System.Collections.Generic.List%601> qui implémente l’interface <xref:System.Collections.Generic.IEnumerable%601> :</span><span class="sxs-lookup"><span data-stu-id="77bab-110">The following example shows usage of the `foreach` statement with an instance of the <xref:System.Collections.Generic.List%601> type that implements the <xref:System.Collections.Generic.IEnumerable%601> interface:</span></span>

[!code-csharp-interactive[list example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#1)]

<span data-ttu-id="77bab-111">L’exemple suivant utilise l’instruction `foreach` avec une instance de type <xref:System.Span%601?displayProperty=nameWithType> qui n’implémente aucune interface :</span><span class="sxs-lookup"><span data-stu-id="77bab-111">The next example uses the `foreach` statement with an instance of the <xref:System.Span%601?displayProperty=nameWithType> type, which doesn't implement any interfaces:</span></span>

[!code-csharp-interactive[span example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#2)]

## <a name="c-language-specification"></a><span data-ttu-id="77bab-112">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="77bab-112">C# Language Specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="77bab-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77bab-113">See also</span></span>

[<span data-ttu-id="77bab-114">L’instruction foreach (spécification du langage C#)</span><span class="sxs-lookup"><span data-stu-id="77bab-114">The foreach statement (C# language specification)</span></span>](/dotnet/csharp/language-reference/language-specification/statements#the-foreach-statement)  
[<span data-ttu-id="77bab-115">Utilisation de foreach avec des tableaux</span><span class="sxs-lookup"><span data-stu-id="77bab-115">Using foreach with Arrays</span></span>](../../programming-guide/arrays/using-foreach-with-arrays.md)  
[<span data-ttu-id="77bab-116">for</span><span class="sxs-lookup"><span data-stu-id="77bab-116">for</span></span>](for.md)  
[<span data-ttu-id="77bab-117">Instructions d’itération</span><span class="sxs-lookup"><span data-stu-id="77bab-117">Iteration Statements</span></span>](iteration-statements.md)  
[<span data-ttu-id="77bab-118">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="77bab-118">C# Keywords</span></span>](index.md)  
[<span data-ttu-id="77bab-119">Référence C#</span><span class="sxs-lookup"><span data-stu-id="77bab-119">C# Reference</span></span>](../index.md)  
[<span data-ttu-id="77bab-120">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="77bab-120">C# Programming Guide</span></span>](../../programming-guide/index.md)  