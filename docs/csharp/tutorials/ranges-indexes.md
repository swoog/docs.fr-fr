---
title: Explorer les plages de données à l’aide d’index et de plages
description: Ce tutoriel avancé vous apprend à explorer les données à l’aide d’index et de plages pour examiner les tranches d’un jeu de données séquentiel.
ms.date: 04/19/2019
ms.custom: mvc
ms.openlocfilehash: 64fae4581e265d4f70b8356d5c651b4fdaca3fe9
ms.sourcegitcommit: dd3b897feb5c4ac39732bb165848e37a344b0765
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2019
ms.locfileid: "64431498"
---
# <a name="indices-and-ranges"></a><span data-ttu-id="4a3fa-103">Index et plages</span><span class="sxs-lookup"><span data-stu-id="4a3fa-103">Indices and ranges</span></span>

<span data-ttu-id="4a3fa-104">Les plages et les index fournissent une syntaxe concise pour accéder à des éléments uniques ou des plages dans un <xref:System.Array>, <xref:System.Span%601> ou <xref:System.ReadOnlySpan%601>.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-104">Ranges and indices provide a succinct syntax for accessing single elements or ranges in an <xref:System.Array>, <xref:System.Span%601>, or <xref:System.ReadOnlySpan%601>.</span></span> <span data-ttu-id="4a3fa-105">Ces fonctionnalités permettent d’utiliser une syntaxe plus concise et claire pour accéder à des éléments uniques ou à des plages d’éléments dans une séquence.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-105">These features enable more concise, clear syntax to access single elements or ranges of elements in a sequence.</span></span>

<span data-ttu-id="4a3fa-106">Dans ce tutoriel, vous allez apprendre à :</span><span class="sxs-lookup"><span data-stu-id="4a3fa-106">In this tutorial, you'll learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="4a3fa-107">Utiliser la syntaxe pour les plages dans une séquence.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-107">Use the syntax for ranges in a sequence.</span></span>
> * <span data-ttu-id="4a3fa-108">Comprendre les décisions de conception pour le début et la fin de chaque séquence.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-108">Understand the design decisions for the start and end of each sequence.</span></span>
> * <span data-ttu-id="4a3fa-109">Découvrir des scénarios pour les types <xref:System.Index> et <xref:System.Range>.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-109">Learn scenarios for the <xref:System.Index> and <xref:System.Range> types.</span></span>

## <a name="language-support-for-indices-and-ranges"></a><span data-ttu-id="4a3fa-110">Prise en charge linguistique pour les index et les plages</span><span class="sxs-lookup"><span data-stu-id="4a3fa-110">Language support for indices and ranges</span></span>

<span data-ttu-id="4a3fa-111">Vous pouvez spécifier un index **à partir de la fin** en utilisant le caractère `^` avant l’index.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-111">You can specify an index **from the end** using the `^` character before the index.</span></span> <span data-ttu-id="4a3fa-112">L’indexation à partir de la fin démarre à partir de la règle que `0..^0` spécifie pour la plage entière.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-112">Indexing from the end starts from the rule that `0..^0` specifies the entire range.</span></span> <span data-ttu-id="4a3fa-113">Pour énumérer un tableau entier, vous démarrez *au premier élément* et continuez jusqu’à ce que vous soyez *passé par le dernier élément*.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-113">To enumerate an entire array, you start *at the first element*, and continue until you are *past the last element*.</span></span> <span data-ttu-id="4a3fa-114">Considérez le comportement de la méthode `MoveNext` sur un énumérateur : elle retourne la valeur false quand l’énumération franchit le dernier élément.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-114">Think of the behavior of the `MoveNext` method on an enumerator: it returns false when the enumeration passes the last element.</span></span> <span data-ttu-id="4a3fa-115">L’index `^0` signifie « la fin », `array[array.Length]` ou l’index qui suit le dernier élément.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-115">The index `^0` means "the end", `array[array.Length]`, or the index that follows the last element.</span></span> <span data-ttu-id="4a3fa-116">Vous connaissez déjà `array[2]`, qui signifie l’élément « 2 à partir du début ».</span><span class="sxs-lookup"><span data-stu-id="4a3fa-116">You are familiar with `array[2]` meaning the element "2 from the start".</span></span> <span data-ttu-id="4a3fa-117">Maintenant, `array[^2]` signifie que l’élément « 2 à partir de la fin ».</span><span class="sxs-lookup"><span data-stu-id="4a3fa-117">Now, `array[^2]` means the element "2 from the end".</span></span> 

<span data-ttu-id="4a3fa-118">Vous pouvez spécifier une **plage** avec **l’opérateur de plage** : `..`.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-118">You can specify a **range** with the **range operator**: `..`.</span></span> <span data-ttu-id="4a3fa-119">Par exemple, `0..^0` spécifie la totalité de la plage du tableau : 0 à partir du début jusqu'à 0 à partir de la fin non inclus.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-119">For example, `0..^0` specifies the entire range of the array: 0 from the start up to, but not including 0 from the end.</span></span> <span data-ttu-id="4a3fa-120">Les deux opérandes peuvent utiliser « à partir du début » ou « à partir de la fin ».</span><span class="sxs-lookup"><span data-stu-id="4a3fa-120">Either operand may use "from the start" or "from the end".</span></span> <span data-ttu-id="4a3fa-121">L’un comme l’autre peuvent être omis.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-121">Furthermore, either operand may be omitted.</span></span> <span data-ttu-id="4a3fa-122">Les valeurs par défaut sont `0` pour l’index de début et `^0` pour l’index de fin.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-122">The defaults are `0` for the start index, and `^0` for the end index.</span></span>

```csharp-interactive
string[] words = new string[]
{
                // index from start    index from end
    "The",      // 0                   ^9
    "quick",    // 1                   ^8
    "brown",    // 2                   ^7
    "fox",      // 3                   ^6
    "jumped",   // 4                   ^5
    "over",     // 5                   ^4
    "the",      // 6                   ^3
    "lazy",     // 7                   ^2
    "dog"       // 8                   ^1
};              // 9 (or words.Length) ^0
```

<span data-ttu-id="4a3fa-123">L’index de chaque élément renforce le concept « à partir du début » et « à partir de la fin » ; ces plages excluent la fin de la plage.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-123">The index of each element reinforces the concept of "from the start", and "from the end", and that ranges are exclusive of the end of the range.</span></span> <span data-ttu-id="4a3fa-124">Le « début » de la totalité du tableau est le premier élément.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-124">The "start" of the entire array is the first element.</span></span> <span data-ttu-id="4a3fa-125">La « fin » de la totalité du tableau se trouve *après* le dernier élément.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-125">The "end" of the entire array is *past* the last element.</span></span>

<span data-ttu-id="4a3fa-126">Vous pouvez récupérer le dernier mot avec l’index `^1`.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-126">You can retrieve the last word with the `^1` index.</span></span> <span data-ttu-id="4a3fa-127">Ajoutez le code suivant sous l’initialisation :</span><span class="sxs-lookup"><span data-stu-id="4a3fa-127">Add the following code below the initialization:</span></span>

[!code-csharp[LastIndex](~/samples/csharp/tutorials/RangesIndexes/IndicesAndRanges.cs#IndicesAndRanges_LastIndex)]

<span data-ttu-id="4a3fa-128">Le code suivant crée une sous-plage qui comporte les mots « quick », « brown » et « fox »</span><span class="sxs-lookup"><span data-stu-id="4a3fa-128">The following code creates a subrange with the words "quick", "brown", and "fox".</span></span> <span data-ttu-id="4a3fa-129">et va de `words[1]` à `words[3]`.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-129">It includes `words[1]` through `words[3]`.</span></span> <span data-ttu-id="4a3fa-130">L’élément `words[4]` n’est pas dans la plage.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-130">The element `words[4]` isn't in the range.</span></span> <span data-ttu-id="4a3fa-131">Ajoutez le code suivant à la même méthode.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-131">Add the following code to the same method.</span></span> <span data-ttu-id="4a3fa-132">Copiez-le et collez-le en bas de la fenêtre interactive.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-132">Copy and paste it at the bottom of the interactive window.</span></span>

[!code-csharp[Range](~/samples/csharp/tutorials/RangesIndexes/IndicesAndRanges.cs#IndicesAndRanges_Range)]

<span data-ttu-id="4a3fa-133">Le code suivant crée une sous-plage qui comporte « lazy » et « dog »</span><span class="sxs-lookup"><span data-stu-id="4a3fa-133">The following code creates a subrange with "lazy" and "dog".</span></span> <span data-ttu-id="4a3fa-134">et comprend `words[^2]` et `words[^1]`.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-134">It includes `words[^2]` and `words[^1]`.</span></span> <span data-ttu-id="4a3fa-135">L’index de fin `words[^0]` n’est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-135">The end index `words[^0]` isn't included.</span></span> <span data-ttu-id="4a3fa-136">Ajoutez également le code suivant :</span><span class="sxs-lookup"><span data-stu-id="4a3fa-136">Add the following code as well:</span></span>

[!code-csharp[LastRange](~/samples/csharp/tutorials/RangesIndexes/IndicesAndRanges.cs#IndicesAndRanges_LastRange)]

<span data-ttu-id="4a3fa-137">Les exemples suivants créent des plages ouvertes au début, à la fin ou les deux :</span><span class="sxs-lookup"><span data-stu-id="4a3fa-137">The following examples create ranges that are open ended for the start, end, or both:</span></span>

[!code-csharp[PartialRange](~/samples/csharp/tutorials/RangesIndexes/IndicesAndRanges.cs#IndicesAndRanges_PartialRanges)]

<span data-ttu-id="4a3fa-138">Vous pouvez également déclarer des plages ou index comme variables.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-138">You can also declare ranges or indices as variables.</span></span> <span data-ttu-id="4a3fa-139">La variable peut ensuite être utilisée à l’intérieur des caractères `[` et `]` :</span><span class="sxs-lookup"><span data-stu-id="4a3fa-139">The variable can then be used inside the `[` and `]` characters:</span></span>

[!code-csharp[IndexRangeTypes](~/samples/csharp/tutorials/RangesIndexes/IndicesAndRanges.cs#IndicesAndRanges_RangeIndexTypes)]

<span data-ttu-id="4a3fa-140">Les exemples précédents montrent deux décisions de conception qui nécessitent des explications supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="4a3fa-140">The previous examples show two design decisions that require more explanation:</span></span>

- <span data-ttu-id="4a3fa-141">Les plages sont *exclusives*, ce qui signifie que l’élément au dernier index n’est pas dans la plage.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-141">Ranges are *exclusive*, meaning the element at the last index isn't in the range.</span></span>
- <span data-ttu-id="4a3fa-142">L’index `^0` est *la fin* de la collection, pas *le dernier élément* de la collection.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-142">The index `^0` is *the end* of the collection, not *the last element* in the collection.</span></span>

<span data-ttu-id="4a3fa-143">L’exemple suivant montre un grand nombre des raisons de ces choix.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-143">The following sample shows many of the reasons for those choices.</span></span> <span data-ttu-id="4a3fa-144">Modifiez `x`, `y` et `z` pour essayer différentes combinaisons.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-144">Modify `x`, `y`, and `z` to try different combinations.</span></span> <span data-ttu-id="4a3fa-145">Quand vous effectuez des essais, utilisez des valeurs de telle sorte que `x` soit inférieur à `y` et `y` inférieur à `z` pour avoir des combinaisons valides.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-145">When you experiment, use values where `x` is less than `y`, and `y` is less than `z` for valid combinations.</span></span> <span data-ttu-id="4a3fa-146">Ajoutez le code suivant à une nouvelle méthode.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-146">Add the following code in a new method.</span></span> <span data-ttu-id="4a3fa-147">Essayez différentes combinaisons :</span><span class="sxs-lookup"><span data-stu-id="4a3fa-147">Try different combinations:</span></span>

[!code-csharp[SemanticsExamples](~/samples/csharp/tutorials/RangesIndexes/IndicesAndRanges.cs#IndicesAndRanges_Semantics)]

## <a name="scenarios-for-indices-and-ranges"></a><span data-ttu-id="4a3fa-148">Scénarios pour les index et les plages</span><span class="sxs-lookup"><span data-stu-id="4a3fa-148">Scenarios for Indices and Ranges</span></span>

<span data-ttu-id="4a3fa-149">L’utilisation de plages et d’index est fréquente pour effectuer une analyse sur une sous-plage d’une séquence entière.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-149">You'll often use ranges and indices when you want to perform some analysis on subrange of an entire sequence.</span></span> <span data-ttu-id="4a3fa-150">La nouvelle syntaxe permet de mieux lire la sous-plage exactement impliquée.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-150">The new syntax is clearer in reading exactly what subrange is involved.</span></span> <span data-ttu-id="4a3fa-151">La fonction locale `MovingAverage` prend un <xref:System.Range> comme argument.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-151">The local function `MovingAverage` takes a <xref:System.Range> as its argument.</span></span> <span data-ttu-id="4a3fa-152">La méthode énumère ensuite simplement cette plage lors du calcul des valeurs minimale, maximale et moyenne.</span><span class="sxs-lookup"><span data-stu-id="4a3fa-152">The method then enumerates just that range when calculating the min, max, and average.</span></span> <span data-ttu-id="4a3fa-153">Essayez le code suivant dans votre projet :</span><span class="sxs-lookup"><span data-stu-id="4a3fa-153">Try the following code in your project:</span></span>

[!code-csharp[MovingAverages](~/samples/csharp/tutorials/RangesIndexes/IndicesAndRanges.cs#IndicesAndRanges_MovingAverage)]

<span data-ttu-id="4a3fa-154">Vous pouvez télécharger le code terminé à partir du dépôt GitHub [dotnet/samples](https://github.com/dotnet/samples/tree/master/csharp/tutorials/RangesIndexes).</span><span class="sxs-lookup"><span data-stu-id="4a3fa-154">You can download the completed code from the [dotnet/samples](https://github.com/dotnet/samples/tree/master/csharp/tutorials/RangesIndexes) repository.</span></span>
