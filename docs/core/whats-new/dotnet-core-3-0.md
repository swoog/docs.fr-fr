---
title: Nouveautés de .NET Core 3.0
description: Découvrez les nouvelles fonctionnalités de .NET Core 3.0.
dev_langs:
- csharp
- vb
author: thraka
ms.author: adegeo
ms.date: 12/31/2018
ms.openlocfilehash: 89264098ed17b398c83bc2dcddd98d9d8fc958f7
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57679734"
---
# <a name="whats-new-in-net-core-30-preview-2"></a><span data-ttu-id="446bc-103">Nouveautés de .NET Core 3.0 (Preview 2)</span><span class="sxs-lookup"><span data-stu-id="446bc-103">What's new in .NET Core 3.0 (Preview 2)</span></span>

<span data-ttu-id="446bc-104">Cet article décrit les nouveautés de .NET Core 3.0 (Preview 2).</span><span class="sxs-lookup"><span data-stu-id="446bc-104">This article describes what is new in .NET Core 3.0 (preview 2).</span></span> <span data-ttu-id="446bc-105">Une des principales améliorations est la prise en charge des applications de bureau Windows (Windows uniquement).</span><span class="sxs-lookup"><span data-stu-id="446bc-105">One of the biggest enhancements is support for Windows desktop applications (Windows only).</span></span> <span data-ttu-id="446bc-106">En utilisant un composant du SDK .NET Core 3.0 appelé Windows Desktop, vous pouvez porter vos applications Windows Forms et Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="446bc-106">By utilizing a .NET Core 3.0 SDK component called Windows Desktop, you can port your Windows Forms and Windows Presentation Foundation (WPF) applications.</span></span> <span data-ttu-id="446bc-107">Pour être clair, le composant Windows Desktop est pris en charge et inclus seulement sur Windows.</span><span class="sxs-lookup"><span data-stu-id="446bc-107">To be clear, the Windows Desktop component is only supported and included on Windows.</span></span> <span data-ttu-id="446bc-108">Pour plus d'informations, consultez la section [Bureau Windows](#windows-desktop) ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="446bc-108">For more information, see the section [Windows desktop](#windows-desktop) below.</span></span>

<span data-ttu-id="446bc-109">.NET Core 3.0 prend en charge C# 8.0.</span><span class="sxs-lookup"><span data-stu-id="446bc-109">.NET Core 3.0 adds support for C# 8.0.</span></span>

<span data-ttu-id="446bc-110">[Téléchargez et commencez à utiliser .NET Core 3.0 Preview 2](https://aka.ms/netcore3download) dès maintenant sur Windows, Mac et Linux.</span><span class="sxs-lookup"><span data-stu-id="446bc-110">[Download and get started with .NET Core 3.0 Preview 2](https://aka.ms/netcore3download) right now on Windows, Mac and Linux.</span></span> <span data-ttu-id="446bc-111">Vous pouvez consulter les détails complets de la version dans les [notes de publication de .NET Core 3.0 Preview 2](https://aka.ms/netcore3releasenotes).</span><span class="sxs-lookup"><span data-stu-id="446bc-111">You can see complete details of the release in the [.NET Core 3.0 Preview 2 release notes](https://aka.ms/netcore3releasenotes).</span></span>

<span data-ttu-id="446bc-112">Pour plus d’informations sur les caractéristiques de chaque version, consultez les annonces suivantes :</span><span class="sxs-lookup"><span data-stu-id="446bc-112">For more information about what was released with each version, see the following announcements:</span></span>

- [<span data-ttu-id="446bc-113">Annonce de .NET Core 3.0 Preview 1</span><span class="sxs-lookup"><span data-stu-id="446bc-113">.NET Core 3.0 Preview 1 announcement</span></span>](https://devblogs.microsoft.com/dotnet/announcing-net-core-3-preview-1-and-open-sourcing-windows-desktop-frameworks/)
- [<span data-ttu-id="446bc-114">Annonce de .NET Core 3.0 Preview 2</span><span class="sxs-lookup"><span data-stu-id="446bc-114">.NET Core 3.0 Preview 2 announcement</span></span>](https://devblogs.microsoft.com/dotnet/announcing-net-core-3-preview-2/)

## <a name="c-8"></a><span data-ttu-id="446bc-115">C# 8</span><span class="sxs-lookup"><span data-stu-id="446bc-115">C# 8</span></span>

<span data-ttu-id="446bc-116">.NET Core 3.0 prend en charge C# 8 et, à compter de .NET Core 3.0 Preview 2, prend en charge ces nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="446bc-116">.NET Core 3.0 supports C# 8, and as of .NET Core 3.0 Preview 2, supports these new features.</span></span> <span data-ttu-id="446bc-117">Pour plus d’informations sur les fonctionnalités de C# 8.0, consultez les billets de blog suivants :</span><span class="sxs-lookup"><span data-stu-id="446bc-117">For more information about C# 8.0 features, see the following blog posts:</span></span>

- [<span data-ttu-id="446bc-118">Do more with patterns in C# 8.0</span><span class="sxs-lookup"><span data-stu-id="446bc-118">Do more with patterns in C# 8.0</span></span>](https://devblogs.microsoft.com/dotnet/do-more-with-patterns-in-c-8-0/)
- [<span data-ttu-id="446bc-119">Take C# 8.0 for a spin</span><span class="sxs-lookup"><span data-stu-id="446bc-119">Take C# 8.0 for a spin</span></span>](https://devblogs.microsoft.com/dotnet/take-c-8-0-for-a-spin/)
- [<span data-ttu-id="446bc-120">Building C# 8.0</span><span class="sxs-lookup"><span data-stu-id="446bc-120">Building C# 8.0</span></span>](https://devblogs.microsoft.com/dotnet/building-c-8-0/)


### <a name="ranges-and-indices"></a><span data-ttu-id="446bc-121">Plages et index</span><span class="sxs-lookup"><span data-stu-id="446bc-121">Ranges and indices</span></span>

<span data-ttu-id="446bc-122">Le nouveau type `Index` peut être utilisé pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="446bc-122">The new `Index` type can be used for indexing.</span></span> <span data-ttu-id="446bc-123">Vous pouvez en créer un à partir d’un `int` qui compte à partir du début, ou avec un opérateur (C#) `^` préfixé qui compte à partir de la fin :</span><span class="sxs-lookup"><span data-stu-id="446bc-123">You can create one from an `int` that counts from the beginning, or with a prefix `^` operator (C#) that counts from the end:</span></span>

```csharp
Index i1 = 3;  // number 3 from beginning
Index i2 = ^4; // number 4 from end
int[] a = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
Console.WriteLine($"{a[i1]}, {a[i2]}"); // "3, 6"
```

<span data-ttu-id="446bc-124">Il existe également un type `Range`, composé de deux `Index` valeurs, une pour le début et une pour la fin, et qui peut être écrit avec une expression de plage (C#) `x..y`.</span><span class="sxs-lookup"><span data-stu-id="446bc-124">There is also a `Range` type, which consists of two `Index` values, one for the start and one for the end, and can be written with a `x..y` range expression (C#).</span></span> <span data-ttu-id="446bc-125">Vous pouvez indexer ensuite avec un `Range` afin de produire une tranche :</span><span class="sxs-lookup"><span data-stu-id="446bc-125">You can then index with a `Range` in order to produce a slice:</span></span>

```csharp
var slice = a[i1..i2]; // { 3, 4, 5 }
```

### <a name="async-streams"></a><span data-ttu-id="446bc-126">Flux asynchrones</span><span class="sxs-lookup"><span data-stu-id="446bc-126">Async streams</span></span>

<span data-ttu-id="446bc-127">Le type `IAsyncEnumerable<T>` est une nouvelle version asynchrone de `IEnumerable<T>`.</span><span class="sxs-lookup"><span data-stu-id="446bc-127">The `IAsyncEnumerable<T>` type is a new asynchronous version of `IEnumerable<T>`.</span></span> <span data-ttu-id="446bc-128">Le langage vous permet d’utiliser `await foreach` sur `IAsyncEnumerable<T>` pour consommer ses éléments, et `yield return` sur ceux-ci pour produire des éléments.</span><span class="sxs-lookup"><span data-stu-id="446bc-128">The language lets you `await foreach` over `IAsyncEnumerable<T>` to consume their elements, and use `yield return` to them to produce elements.</span></span>

<span data-ttu-id="446bc-129">L’exemple suivant montre la production et la consommation de flux de données asynchrones.</span><span class="sxs-lookup"><span data-stu-id="446bc-129">The following example demonstrates both production and consumption of async streams.</span></span> <span data-ttu-id="446bc-130">L’instruction `foreach` est asynchrone et utilise elle-même `yield return` afin de produire un flux asynchrone pour les appelants.</span><span class="sxs-lookup"><span data-stu-id="446bc-130">The `foreach` statement is async and itself uses `yield return` to produce an async stream for callers.</span></span> <span data-ttu-id="446bc-131">Ce modèle (qui utilise `yield return`) est le modèle recommandé pour produire des flux de données asynchrones.</span><span class="sxs-lookup"><span data-stu-id="446bc-131">This pattern (using `yield return`) is the recommended model for producing async streams.</span></span>

```csharp
async IAsyncEnumerable<int> GetBigResultsAsync()
{
    await foreach (var result in GetResultsAsync())
    {
        if (result > 20) yield return result; 
    }
}
```

<span data-ttu-id="446bc-132">Outre la possibilité d’effectuer une opération `await foreach`, vous pouvez également créer des itérateurs asynchrones, par exemple un itérateur qui retourne un objet `IAsyncEnumerable/IAsyncEnumerator` auquel vous pouvez à la fois appliquer des opérations `await` et `yield`.</span><span class="sxs-lookup"><span data-stu-id="446bc-132">In addition to being able to `await foreach`, you can also create async iterators, for example, an iterator that returns an `IAsyncEnumerable/IAsyncEnumerator` that you can both `await` and `yield` in.</span></span> <span data-ttu-id="446bc-133">Pour les objets qui doivent être supprimés, vous pouvez utiliser `IAsyncDisposable`, qui implémentent différents types BCL, notamment `Stream` et `Timer`.</span><span class="sxs-lookup"><span data-stu-id="446bc-133">For objects that need to be disposed, you can use `IAsyncDisposable`, which various BCL types implement, such as `Stream` and `Timer`.</span></span>

>[!NOTE]
><span data-ttu-id="446bc-134">Vous avez besoin de .NET Core 3.0 Preview 2 pour utiliser des flux asynchrones si vous voulez développer avec Visual Studio 2019 Preview 2 ou avec la dernière préversion de l’[extension C# pour Visual Studio Code](https://github.com/OmniSharp/omnisharp-vscode/releases/tag/v1.18.0-beta5).</span><span class="sxs-lookup"><span data-stu-id="446bc-134">You need .NET Core 3.0 Preview 2 to use async streams if you want to develop with either Visual Studio 2019 Preview 2 or the latest preview of the [C# extension for Visual Studio Code](https://github.com/OmniSharp/omnisharp-vscode/releases/tag/v1.18.0-beta5).</span></span> <span data-ttu-id="446bc-135">Si vous utilisez .NET Core 3.0 Preview 2 sur la ligne de commande, tout fonctionnera comme prévu.</span><span class="sxs-lookup"><span data-stu-id="446bc-135">If you are using .NET Core 3.0 Preview 2 at the command line, then everything will work as expected.</span></span>

### <a name="using-declarations"></a><span data-ttu-id="446bc-136">Déclarations using</span><span class="sxs-lookup"><span data-stu-id="446bc-136">Using Declarations</span></span>

<span data-ttu-id="446bc-137">Les *déclarations using* sont une nouvelle façon de vérifier que votre objet est correctement supprimé.</span><span class="sxs-lookup"><span data-stu-id="446bc-137">*Using declarations* are a new way to ensure your object is properly disposed.</span></span> <span data-ttu-id="446bc-138">Une *déclaration using* maintient l’objet actif tant qu’il se trouve dans l’étendue.</span><span class="sxs-lookup"><span data-stu-id="446bc-138">A *using declaration* keeps the object alive while it is still in scope.</span></span> <span data-ttu-id="446bc-139">Une fois que l’objet se trouve en dehors de l’étendue, il est automatiquement supprimé.</span><span class="sxs-lookup"><span data-stu-id="446bc-139">Once the object becomes out of scope, it is automatically disposed.</span></span> <span data-ttu-id="446bc-140">Ceci réduit les *instructions using* imbriquées et rend votre code plus propre.</span><span class="sxs-lookup"><span data-stu-id="446bc-140">This will reduce nested *using statements* and make your code cleaner.</span></span>

```csharp
static void Main(string[] args)
{
    using var options = Parse(args);
    if (options["verbose"]) { WriteLine("Logging..."); }

} // options disposed here
```

### <a name="switch-expressions"></a><span data-ttu-id="446bc-141">Expressions switch</span><span class="sxs-lookup"><span data-stu-id="446bc-141">Switch Expressions</span></span>

<span data-ttu-id="446bc-142">Les *expressions switch* sont un moyen plus propre d’effectuer une *instruction switch* ; cependant, comme il s’agit d’expressions, elles retournent une valeur.</span><span class="sxs-lookup"><span data-stu-id="446bc-142">*Switch expressions* are a cleaner way of doing a *switch statement* but, since it's an expression, returns a value.</span></span> <span data-ttu-id="446bc-143">Les *expressions switch* sont aussi entièrement intégrées aux critères spéciaux et utilisent le modèle d’élément ignoré, `_`, pour représenter la valeur `default`.</span><span class="sxs-lookup"><span data-stu-id="446bc-143">*Switch expressions* are also fully integrated with pattern matching, and use the discard pattern, `_`, to represent the `default` value.</span></span>

<span data-ttu-id="446bc-144">Vous pouvez voir la syntaxe des *expressions switch* dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="446bc-144">You can see the syntax for *switch expressions* in the following example:</span></span>

```csharp
static string Display(object o) => o switch
{
    Point { X: 0, Y: 0 }         => "origin",
    Point { X: var x, Y: var y } => $"({x}, {y})",
    _                            => "unknown"
};
```

<span data-ttu-id="446bc-145">Deux modèles sont mis en œuvre dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="446bc-145">There are two patterns at play in this example.</span></span> <span data-ttu-id="446bc-146">`o` correspond d’abord au *modèle de type* `Point`, puis au *modèle de propriété* à l’intérieur des *{accolades}*.</span><span class="sxs-lookup"><span data-stu-id="446bc-146">`o` first matches with the `Point` *type pattern* and then with the *property pattern* inside the *{curly braces}*.</span></span> <span data-ttu-id="446bc-147">Le `_` décrit le `discard pattern`, qui est identique à `default` pour les *instructions switch*.</span><span class="sxs-lookup"><span data-stu-id="446bc-147">The `_` describes the `discard pattern`, which is the same as `default` for *switch statements*.</span></span>

<span data-ttu-id="446bc-148">Les modèles vous permettent d’écrire du code déclaratif qui capture votre intention, au lieu d’un code procédural qui implémente des tests de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="446bc-148">Patterns enable you to write declarative code that captures your intent instead of procedural code that implements tests for it.</span></span> <span data-ttu-id="446bc-149">Le compilateur devient responsable de l’implémentation de ce code procédural fastidieux, et il est garanti qu’il le fait toujours correctement.</span><span class="sxs-lookup"><span data-stu-id="446bc-149">The compiler becomes responsible for implementing that boring procedural code and is guaranteed to always do it correctly.</span></span>

<span data-ttu-id="446bc-150">Il y a toujours cas où les *instructions switch* sont un meilleur choix que des *expressions switch* ; vous pouvez utiliser des modèles avec les deux styles de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="446bc-150">There will still be cases where *switch statements* will be a better choice than *switch expressions* and patterns can be used with both syntax styles.</span></span>

<span data-ttu-id="446bc-151">Pour plus d’informations, consultez [Do more with patterns in C# 8.0](https://devblogs.microsoft.com/dotnet/do-more-with-patterns-in-c-8-0/).</span><span class="sxs-lookup"><span data-stu-id="446bc-151">For more information, see [Do more with patterns in C# 8.0](https://devblogs.microsoft.com/dotnet/do-more-with-patterns-in-c-8-0/).</span></span>

## <a name="ieee-floating-point-improvements"></a><span data-ttu-id="446bc-152">Améliorations apportées à la virgule flottante IEEE</span><span class="sxs-lookup"><span data-stu-id="446bc-152">IEEE Floating-point improvements</span></span>

<span data-ttu-id="446bc-153">Les API de virgule flottante sont en cours de mise à jour pour devenir conformes à la [révision 754-2008 d’IEEE](https://en.wikipedia.org/wiki/IEEE_754-2008_revision).</span><span class="sxs-lookup"><span data-stu-id="446bc-153">Floating point APIs are in the process of being updated to comply with [IEEE 754-2008 revision](https://en.wikipedia.org/wiki/IEEE_754-2008_revision).</span></span> <span data-ttu-id="446bc-154">L’objectif de ces modifications est d’exposer toutes les opérations « obligatoires » et de garantir que leur comportement est conforme à la spécification IEEE.</span><span class="sxs-lookup"><span data-stu-id="446bc-154">The goal of these changes is to expose all "required" operations and ensure that they are behaviorally compliant with the IEEE spec.</span></span>

<span data-ttu-id="446bc-155">Correctifs de l’analyse et de la mise en forme :</span><span class="sxs-lookup"><span data-stu-id="446bc-155">Parsing and formatting fixes:</span></span>

* <span data-ttu-id="446bc-156">Analyse et arrondi corrects des entrées, quelle que soit leur longueur.</span><span class="sxs-lookup"><span data-stu-id="446bc-156">Correctly parse and round inputs of any length.</span></span>
* <span data-ttu-id="446bc-157">Analyse et mise en forme correctes des zéros négatifs.</span><span class="sxs-lookup"><span data-stu-id="446bc-157">Correctly parse and format negative zero.</span></span>
* <span data-ttu-id="446bc-158">Analyse correcte de l’infini et des valeurs NaN en effectuant une vérification sans tenir compte de la casse et en autorisant un signe `+` facultatif de début là où c’est applicable.</span><span class="sxs-lookup"><span data-stu-id="446bc-158">Correctly parse Infinity and NaN by performing a case-insensitive check and allowing an optional preceding `+` where applicable.</span></span>

<span data-ttu-id="446bc-159">Les nouvelles API mathématiques ont :</span><span class="sxs-lookup"><span data-stu-id="446bc-159">New Math APIs have:</span></span>

* `BitIncrement/BitDecrement`\
<span data-ttu-id="446bc-160">Correspond aux opérations IEEE `nextUp` et `nextDown`.</span><span class="sxs-lookup"><span data-stu-id="446bc-160">Corresponds to the `nextUp` and `nextDown` IEEE operations.</span></span> <span data-ttu-id="446bc-161">Elles retournent le plus petit nombre à virgule flottante dont la valeur est supérieure ou inférieure à l’entrée (respectivement).</span><span class="sxs-lookup"><span data-stu-id="446bc-161">They return the smallest floating-point number that compares greater or lesser than the input (respectively).</span></span> <span data-ttu-id="446bc-162">Par exemple, `Math.BitIncrement(0.0)` retourne `double.Epsilon`.</span><span class="sxs-lookup"><span data-stu-id="446bc-162">For example, `Math.BitIncrement(0.0)` would return `double.Epsilon`.</span></span>

* `MaxMagnitude/MinMagnitude`\
<span data-ttu-id="446bc-163">Correspond aux opérations IEEE `maxNumMag` et `minNumMag`. Elles retournent la valeur la plus grande ou la plus petite des deux entrées (respectivement).</span><span class="sxs-lookup"><span data-stu-id="446bc-163">Corresponds to the `maxNumMag` and `minNumMag` IEEE operations, they return the value that is greater or lesser in magnitude of the two inputs (respectively).</span></span> <span data-ttu-id="446bc-164">Par exemple, `Math.MaxMagnitude(2.0, -3.0)` retourne `-3.0`.</span><span class="sxs-lookup"><span data-stu-id="446bc-164">For example, `Math.MaxMagnitude(2.0, -3.0)` would return `-3.0`.</span></span>

* `ILogB`\
<span data-ttu-id="446bc-165">Correspond à l’opération IEEE `logB` qui retourne une valeur intégrale ; elle retourne le logarithme de base 2 intégral du paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="446bc-165">Corresponds to the `logB` IEEE operation which returns an integral value, it returns the integral base-2 log of the input parameter.</span></span> <span data-ttu-id="446bc-166">Ceci est identique à `floor(log2(x))`, mais effectué avec une erreur d’arrondi minimale.</span><span class="sxs-lookup"><span data-stu-id="446bc-166">This is effectively the same as `floor(log2(x))`, but done with minimal rounding error.</span></span>

* `ScaleB`\
<span data-ttu-id="446bc-167">Correspond à l’opération IEEE `scaleB` qui prend une valeur intégrale ; elle retourne `x * pow(2, n)`, mais est effectuée avec une erreur d’arrondi minimale.</span><span class="sxs-lookup"><span data-stu-id="446bc-167">Corresponds to the `scaleB` IEEE operation which takes an integral value, it returns effectively `x * pow(2, n)`, but is done with minimal rounding error.</span></span>

* `Log2`\
<span data-ttu-id="446bc-168">Correspond à l’opération IEEE `log2` ; elle retourne le logarithme de base 2.</span><span class="sxs-lookup"><span data-stu-id="446bc-168">Corresponds to the `log2` IEEE operation, it returns the base-2 logarithm.</span></span> <span data-ttu-id="446bc-169">Son erreur d’arrondi est minimale.</span><span class="sxs-lookup"><span data-stu-id="446bc-169">It minimizes rounding error.</span></span>

* `FusedMultiplyAdd`\
<span data-ttu-id="446bc-170">Correspond à l’opération IEEE `fma` ; elle effectue une multiplication-addition fusionnée.</span><span class="sxs-lookup"><span data-stu-id="446bc-170">Corresponds to the `fma` IEEE operation, it performs a fused multiply add.</span></span> <span data-ttu-id="446bc-171">Elle effectue `(x * y) + z` comme une seule opération, avec une erreur d’arrondi minimale.</span><span class="sxs-lookup"><span data-stu-id="446bc-171">That is, it does `(x * y) + z` as a single operation, there-by minimizing the rounding error.</span></span> <span data-ttu-id="446bc-172">Par exemple, `FusedMultiplyAdd(1e308, 2.0, -1e308)` retourne `1e308`.</span><span class="sxs-lookup"><span data-stu-id="446bc-172">An example would be `FusedMultiplyAdd(1e308, 2.0, -1e308)` which returns `1e308`.</span></span> <span data-ttu-id="446bc-173">L’opération régulière `(1e308 * 2.0) - 1e308` retourne `double.PositiveInfinity`.</span><span class="sxs-lookup"><span data-stu-id="446bc-173">The regular `(1e308 * 2.0) - 1e308` returns `double.PositiveInfinity`.</span></span>

* `CopySign`\
<span data-ttu-id="446bc-174">Correspond à l’opération IEEE `copySign` ; elle retourne la valeur de `x`, mais avec le signe de `y`.</span><span class="sxs-lookup"><span data-stu-id="446bc-174">Corresponds to the `copySign` IEEE operation, it returns the value of `x`, but with the sign of `y`.</span></span>

## <a name="net-platform-dependent-intrinsics"></a><span data-ttu-id="446bc-175">Intrinsèques dépendant de la plateforme .NET</span><span class="sxs-lookup"><span data-stu-id="446bc-175">.NET Platform Dependent Intrinsics</span></span>

<span data-ttu-id="446bc-176">Des API ont été ajoutées, qui permettent d’accéder à certaines instructions de l’UC orientées performances, comme les ensembles **SIMD** ou les ensembles d’**instructions de manipulation de bits**.</span><span class="sxs-lookup"><span data-stu-id="446bc-176">APIs have been added that allow access to certain perf-oriented CPU instructions, such as the **SIMD** or **Bit Manipulation instruction** sets.</span></span> <span data-ttu-id="446bc-177">Ces instructions peuvent améliorer grandement les performances dans certains scénarios, comme le traitement efficace de données en parallèle.</span><span class="sxs-lookup"><span data-stu-id="446bc-177">These instructions can help achieve big performance improvements in certain scenarios, such as processing data efficiently in parallel.</span></span> <span data-ttu-id="446bc-178">En plus d’exposer les API pour permettre à vos programmes de les utiliser, les bibliothèques .NET ont commencé à utiliser ces instructions pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="446bc-178">In addition to exposing the APIs for your programs to use, the .NET libraries have begun using these instructions to improve performance.</span></span>

<span data-ttu-id="446bc-179">Les demandes de tirage CoreCLR suivantes illustrent quelques-uns des intrinsèques, via l’implémentation ou l’utilisation :</span><span class="sxs-lookup"><span data-stu-id="446bc-179">The following CoreCLR PRs demonstrate a few of the intrinsics, either via implementation or use:</span></span>

* [<span data-ttu-id="446bc-180">Implement simple SSE2 hardware intrinsics</span><span class="sxs-lookup"><span data-stu-id="446bc-180">Implement simple SSE2 hardware intrinsics</span></span>](https://github.com/dotnet/coreclr/pull/15585)
* [<span data-ttu-id="446bc-181">Implement the SSE hardware intrinsics</span><span class="sxs-lookup"><span data-stu-id="446bc-181">Implement the SSE hardware intrinsics</span></span>](https://github.com/dotnet/coreclr/pull/15538)
* [<span data-ttu-id="446bc-182">Arm64 Base HW Intrinsics</span><span class="sxs-lookup"><span data-stu-id="446bc-182">Arm64 Base HW Intrinsics</span></span>](https://github.com/dotnet/coreclr/pull/16822)
* [<span data-ttu-id="446bc-183">Use TZCNT and LZCNT for Locate{First|Last}Found{Byte|Char}</span><span class="sxs-lookup"><span data-stu-id="446bc-183">Use TZCNT and LZCNT for Locate{First|Last}Found{Byte|Char}</span></span>](https://github.com/dotnet/coreclr/pull/21073)

<span data-ttu-id="446bc-184">Pour plus d’informations, consultez [.NET Platform Dependent Intrinsics](https://github.com/dotnet/designs/blob/master/accepted/platform-intrinsics.md), qui établit une approche pour la définition de cette infrastructure matérielle, permettant à Microsoft, aux fournisseurs de circuits intégrés, ou à d’autres entreprises ou personnes de définir des API de matériel/circuit intégré qui doivent être exposées au code .NET.</span><span class="sxs-lookup"><span data-stu-id="446bc-184">For more information, see [.NET Platform Dependent Intrinsics](https://github.com/dotnet/designs/blob/master/accepted/platform-intrinsics.md), which defines an approach for defining this hardware infrastructure, allowing Microsoft, chip vendors, or any other company or individual to define hardware/chip APIs that should be exposed to .NET code.</span></span>

## <a name="default-executables"></a><span data-ttu-id="446bc-185">Exécutables par défaut</span><span class="sxs-lookup"><span data-stu-id="446bc-185">Default executables</span></span>

<span data-ttu-id="446bc-186">.NET core génère désormais des [exécutables dépendant du framework](../deploying/index.md#framework-dependent-executables-fde) par défaut.</span><span class="sxs-lookup"><span data-stu-id="446bc-186">.NET Core will now build [framework-dependent executables](../deploying/index.md#framework-dependent-executables-fde) by default.</span></span> <span data-ttu-id="446bc-187">Il s’agit d’une nouvelle fonctionnalité pour les applications qui utilisent une version .NET Core installée de façon globale.</span><span class="sxs-lookup"><span data-stu-id="446bc-187">This is new for applications that use a globally installed version of .NET Core.</span></span> <span data-ttu-id="446bc-188">Jusqu’à présent, seuls les [déploiements autonomes](../deploying/index.md#self-contained-deployments-scd) produisaient un exécutable.</span><span class="sxs-lookup"><span data-stu-id="446bc-188">Until now, only [self-contained deployments](../deploying/index.md#self-contained-deployments-scd) would produce an executable.</span></span>

<span data-ttu-id="446bc-189">Lors de l’étape `dotnet build` ou `dotnet publish`, un exécutable est créé s’il correspond à l’environnement et à la plateforme du Kit de développement que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="446bc-189">During `dotnet build` or `dotnet publish`, an executable is created provided that matches the environment and platform of the SDK you are using.</span></span> <span data-ttu-id="446bc-190">Vous pouvez obtenir le même résultat avec ces exécutables, comme vous le feriez avec d’autres exécutables natifs comme :</span><span class="sxs-lookup"><span data-stu-id="446bc-190">You can expect the same things with these executables as you would other native executables, such as:</span></span>

* <span data-ttu-id="446bc-191">Vous pouvez double-cliquer sur l’exécutable.</span><span class="sxs-lookup"><span data-stu-id="446bc-191">You can double-click on the executable.</span></span>
* <span data-ttu-id="446bc-192">Vous pouvez lancer l’application directement à partir d’une invite de commandes, par exemple `myapp.exe` sous Windows, et `./myapp` sous Linux et macOS.</span><span class="sxs-lookup"><span data-stu-id="446bc-192">You can launch the application from a command prompt directly, such as `myapp.exe` on Windows, and `./myapp` on Linux and macOS.</span></span>

## <a name="build-copies-dependencies"></a><span data-ttu-id="446bc-193">Dépendances de copies de build</span><span class="sxs-lookup"><span data-stu-id="446bc-193">Build copies dependencies</span></span>

<span data-ttu-id="446bc-194">`dotnet build` copie maintenant les dépendances NuGet pour votre application à partir du cache NuGet vers le dossier de sortie de build.</span><span class="sxs-lookup"><span data-stu-id="446bc-194">`dotnet build` now copies NuGet dependencies for your application from the NuGet cache to the build output folder.</span></span> <span data-ttu-id="446bc-195">Auparavant, les dépendances étaient copiées uniquement dans le cadre de `dotnet publish`.</span><span class="sxs-lookup"><span data-stu-id="446bc-195">Previously, dependencies were only copied as part of `dotnet publish`.</span></span> 

<span data-ttu-id="446bc-196">Certaines opérations, par exemple la liaison et la publication d’une page de type Razor, nécessiteront toujours une publication.</span><span class="sxs-lookup"><span data-stu-id="446bc-196">There are some operations, like linking and razor page publishing that will still require publishing.</span></span>


## <a name="local-dotnet-tools"></a><span data-ttu-id="446bc-197">Outils dotnet locaux</span><span class="sxs-lookup"><span data-stu-id="446bc-197">Local dotnet tools</span></span>

>[!WARNING]
><span data-ttu-id="446bc-198">Il y a eu un changement dans les outils .NET Core locaux entre .NET Core 3.0 Preview 1 et .NET Core 3.0 Preview 2.</span><span class="sxs-lookup"><span data-stu-id="446bc-198">There was a change in .NET Core Local Tools between .NET Core 3.0 Preview 1 and .NET Core 3.0 Preview 2.</span></span>  <span data-ttu-id="446bc-199">Si vous avez essayé les outils locaux dans la version Preview 1 en exécutant une commande comme `dotnet tool restore` ou `dotnet tool install`, vous devez supprimer votre dossier de cache des outils locaux pour que ces outils fonctionnent correctement dans la version Preview 2.</span><span class="sxs-lookup"><span data-stu-id="446bc-199">If you tried out local tools in Preview 1 by running a command like `dotnet tool restore` or `dotnet tool install`, you need to delete your local tools cache folder before local tools will work correctly in Preview 2.</span></span> <span data-ttu-id="446bc-200">Ce dossier se trouve à ces emplacements :</span><span class="sxs-lookup"><span data-stu-id="446bc-200">This folder is located at:</span></span>
>
><span data-ttu-id="446bc-201">Sur mac, Linux : `rm -r $HOME/.dotnet/toolResolverCache`</span><span class="sxs-lookup"><span data-stu-id="446bc-201">On mac, Linux: `rm -r $HOME/.dotnet/toolResolverCache`</span></span>
>
><span data-ttu-id="446bc-202">Sur Windows : `rmdir /s %USERPROFILE%\.dotnet\toolResolverCache`</span><span class="sxs-lookup"><span data-stu-id="446bc-202">On Windows: `rmdir /s %USERPROFILE%\.dotnet\toolResolverCache`</span></span>
>
><span data-ttu-id="446bc-203">Si vous ne supprimez pas ce dossier, vous recevez une erreur.</span><span class="sxs-lookup"><span data-stu-id="446bc-203">If you do not delete this folder, you will receive an error.</span></span>

<span data-ttu-id="446bc-204">Alors que .NET Core 2.1 prenant en charge des outils globaux, .NET Core 3.0 dispose maintenant d’outils locaux.</span><span class="sxs-lookup"><span data-stu-id="446bc-204">While .NET Core 2.1 supported global tools, .NET Core 3.0 now has local tools.</span></span> <span data-ttu-id="446bc-205">Les outils locaux sont similaires aux outils globales mais ils sont associés à un emplacement particulier sur le disque.</span><span class="sxs-lookup"><span data-stu-id="446bc-205">Local tools are similar to global tools but are associated with a particular location on disk.</span></span> <span data-ttu-id="446bc-206">Cela permet une utilisation par projet et par référentiel.</span><span class="sxs-lookup"><span data-stu-id="446bc-206">This enables per-project and per-repository tooling.</span></span> <span data-ttu-id="446bc-207">Un outil installé localement n’est pas disponible de façon globale.</span><span class="sxs-lookup"><span data-stu-id="446bc-207">Any tool installed locally isn't available globally.</span></span> <span data-ttu-id="446bc-208">Les outils sont distribués sous forme de packages NuGet.</span><span class="sxs-lookup"><span data-stu-id="446bc-208">Tools are distributed as NuGet packages.</span></span>

<span data-ttu-id="446bc-209">Les outils locaux s’appuient sur un nom de fichier manifeste `dotnet-tools.json` dans votre répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="446bc-209">Local tools rely on a manifest file name `dotnet-tools.json` in your current directory.</span></span> <span data-ttu-id="446bc-210">Ce fichier manifeste définit les outils qui doivent être disponibles dans ce dossier et sous-celui-ci.</span><span class="sxs-lookup"><span data-stu-id="446bc-210">This manifest file defines the tools to be available at that folder and below.</span></span> <span data-ttu-id="446bc-211">En créant ce fichier manifeste à la racine de votre référentiel, vous garantissez que toute personne qui clone votre code pourra restaurer et utiliser les outils nécessaires pour fonctionner correctement avec votre code.</span><span class="sxs-lookup"><span data-stu-id="446bc-211">By creating this manifest file at the root of your repository, you ensure anyone cloning your code can restore and use the tools that are needed to successfully work with your code.</span></span>

<span data-ttu-id="446bc-212">Pour créer un fichier manifeste `dotnet-tools.json`, utilisez :</span><span class="sxs-lookup"><span data-stu-id="446bc-212">To create a `dotnet-tools.json` manifest file, use:</span></span>

```console
dotnet new tool-manifest
```

<span data-ttu-id="446bc-213">Ajoutez un nouvel outil au manifeste local avec :</span><span class="sxs-lookup"><span data-stu-id="446bc-213">Add a new tool to the local manifest with:</span></span>

```console
dotnet tool install <packageId>
```

<span data-ttu-id="446bc-214">Vous pouvez également lister les outils dans le manifeste local avec :</span><span class="sxs-lookup"><span data-stu-id="446bc-214">You can also list the tools in the local manifest with:</span></span>

```console
dotnet tool list
```

<span data-ttu-id="446bc-215">Pour voir quels outils sont installés globalement, utilisez :</span><span class="sxs-lookup"><span data-stu-id="446bc-215">To see what tools are installed globally, use:</span></span>

```console
dotnet tool list -g
```

<span data-ttu-id="446bc-216">Quand le fichier manifeste des outils locaux est disponible, mais que les outils définis dans le manifeste n’ont pas été installés, utilisez la commande suivante pour télécharger et installer automatiquement ces outils :</span><span class="sxs-lookup"><span data-stu-id="446bc-216">When the local tools manifest file is available, but the tools defined in the manifest have not been installed, use the following command to automatically download and install those tools:</span></span>

```console
dotnet tool restore
```

<span data-ttu-id="446bc-217">Exécutez l’outil local avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="446bc-217">Run a local tool with the following command:</span></span>

```console
dotnet tool run <tool-command-name>
```

<span data-ttu-id="446bc-218">Quand un outil local est exécuté, dotnet recherche un manifeste dans la structure du répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="446bc-218">When a local tool is run, dotnet searches for a manifest up the current directory structure.</span></span> <span data-ttu-id="446bc-219">Si le fichier manifeste d’un outil est trouvé, la commande recherche l’outil demandé.</span><span class="sxs-lookup"><span data-stu-id="446bc-219">When a tool manifest file is found, it is searched for the requested tool.</span></span> <span data-ttu-id="446bc-220">Si l’outil est trouvé dans le manifeste mais pas dans le cache, l’utilisateur reçoit une erreur et doit exécuter `dotnet tool restore`.</span><span class="sxs-lookup"><span data-stu-id="446bc-220">If the tool is found in the manifest, but not the cache, the user receives an error and needs to run `dotnet tool restore`.</span></span>

<span data-ttu-id="446bc-221">Pour supprimer un outil du fichier manifeste des outils locaux, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="446bc-221">To remove a tool from the local tool manifest file, run the following command:</span></span>

```console
dotnet tool uninstall <packageId>
```

<span data-ttu-id="446bc-222">Le fichier manifeste de l’outil est conçu pour permettre des modifications manuelles et ainsi mettre à jour la version requise pour une utilisation avec le référentiel.</span><span class="sxs-lookup"><span data-stu-id="446bc-222">The tool manifest file is designed to allow hand editing – which you might do to update the required version for working with the repository.</span></span> <span data-ttu-id="446bc-223">Voici un exemple de fichier `dotnet-tools.json` :</span><span class="sxs-lookup"><span data-stu-id="446bc-223">Here is an example `dotnet-tools.json` file:</span></span>

```json
{
  "version": 1,
  "isRoot": true,
  "tools": {
    "dotnetsay": {
      "version": "2.1.4",
      "commands": [
        "dotnetsay"
      ]
    },
    "t-rex": {
      "version": "1.0.103",
      "commands": [
        "t-rex"
      ]
    }
  }
}
```

<span data-ttu-id="446bc-224">Pour les outils locaux et globaux, une version compatible du runtime est requise.</span><span class="sxs-lookup"><span data-stu-id="446bc-224">For both global and local tools, a compatible version of the runtime is required.</span></span> <span data-ttu-id="446bc-225">De nombreux outils actuellement sur NuGet.org ciblent le runtime .NET Core 2.1.</span><span class="sxs-lookup"><span data-stu-id="446bc-225">Many tools currently on NuGet.org target .NET Core Runtime 2.1.</span></span> <span data-ttu-id="446bc-226">Pour installer ces outils de façon locale ou globale, vous devez toujours installer le [runtime NET Core 2.1](https://dotnet.microsoft.com/download/dotnet-core/2.1).</span><span class="sxs-lookup"><span data-stu-id="446bc-226">To install those globally or locally, you would still need to install the [NET Core 2.1 Runtime](https://dotnet.microsoft.com/download/dotnet-core/2.1).</span></span>

## <a name="windows-desktop"></a><span data-ttu-id="446bc-227">Bureau Windows</span><span class="sxs-lookup"><span data-stu-id="446bc-227">Windows desktop</span></span>

<span data-ttu-id="446bc-228">À compter de .NET Core 3.0 Préversion 1, vous pouvez créer des applications de bureau Windows à l’aide des outils WPF et Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="446bc-228">Starting with .NET Core 3.0 Preview 1, you can build Windows desktop applications using WPF and Windows Forms.</span></span> <span data-ttu-id="446bc-229">Ces infrastructures prennent également en charge l’utilisation de contrôles modernes et le style Fluent à partir de la bibliothèque XAML de l’interface utilisateur Windows (WinUI) via des [îles XAML](/windows/uwp/xaml-platform/xaml-host-controls).</span><span class="sxs-lookup"><span data-stu-id="446bc-229">These frameworks also support using modern controls and Fluent styling from the Windows UI XAML Library (WinUI) via [XAML islands](/windows/uwp/xaml-platform/xaml-host-controls).</span></span>

<span data-ttu-id="446bc-230">Le composant Bureau Windows fait partie du SDK .NET Core 3.0 Windows.</span><span class="sxs-lookup"><span data-stu-id="446bc-230">The Windows Desktop component is part of the Windows .NET Core 3.0 SDK.</span></span>

<span data-ttu-id="446bc-231">Vous pouvez créer une nouvelle application WPF ou Windows Forms à l’aide des commandes `dotnet` suivantes :</span><span class="sxs-lookup"><span data-stu-id="446bc-231">You can create a new WPF or Windows Forms app with the following `dotnet` commands:</span></span>

```console
dotnet new wpf
dotnet new winforms
```

<span data-ttu-id="446bc-232">Visual Studio 2019 Preview 2 ajoute des modèles **Nouveau projet** pour Windows Forms et WPF .NET Core 3.0.</span><span class="sxs-lookup"><span data-stu-id="446bc-232">Visual Studio 2019 Preview 2 adds **New Project** templates for .NET Core 3.0 Windows Forms and WPF.</span></span> <span data-ttu-id="446bc-233">Les concepteurs ne sont pas encore pris en charge.</span><span class="sxs-lookup"><span data-stu-id="446bc-233">Designers are still not yet supported.</span></span> <span data-ttu-id="446bc-234">Vous pouvez ouvrir, lancer et déboguer ces projets dans Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="446bc-234">And you can open, launch, and debug these projects in Visual Studio 2019.</span></span>

<span data-ttu-id="446bc-235">Visual Studio 2017 15.9 ajoute la possibilité d’[activer les préversions de .NET Core](https://devblogs.microsoft.com/dotnet/net-core-tooling-update-for-visual-studio-2017-version-15-9/), mais vous devez activer cette fonctionnalité, et il ne s’agit pas d’un scénario pris en charge.</span><span class="sxs-lookup"><span data-stu-id="446bc-235">Visual Studio 2017 15.9 adds the ability to [enable .NET Core previews](https://devblogs.microsoft.com/dotnet/net-core-tooling-update-for-visual-studio-2017-version-15-9/), but you need to turn that feature on, and it's not a supported scenario.</span></span>

<span data-ttu-id="446bc-236">Les nouveaux projets sont identiques aux projets .NET Core existants, avec quelques ajouts.</span><span class="sxs-lookup"><span data-stu-id="446bc-236">The new projects are the same as existing .NET Core projects, with a couple additions.</span></span> <span data-ttu-id="446bc-237">Voici une comparaison entre le projet de console .NET Core de base et un projet Windows Forms et WPF de base.</span><span class="sxs-lookup"><span data-stu-id="446bc-237">Here is the comparison of the basic .NET Core console project and a basic Windows Forms and WPF project.</span></span>

<span data-ttu-id="446bc-238">Dans un projet de console .NET Core, le projet utilise le SDK `Microsoft.NET.Sdk` et déclare une dépendance sur .NET Core 3.0 via l’infrastructure cible `netcoreapp3.0`.</span><span class="sxs-lookup"><span data-stu-id="446bc-238">In a .NET Core console project, the project uses the `Microsoft.NET.Sdk` SDK and declares a dependency on .NET Core 3.0 via the `netcoreapp3.0` target framework.</span></span> <span data-ttu-id="446bc-239">Pour créer une application Bureau Windows, utilisez le SDK `Microsoft.NET.Sdk.WindowsDesktop` et choisissez l’infrastructure d’interface utilisateur à utiliser :</span><span class="sxs-lookup"><span data-stu-id="446bc-239">To create a Windows Desktop app, use the `Microsoft.NET.Sdk.WindowsDesktop` SDK and choose which UI framework to use:</span></span>

```diff
-<Project Sdk="Microsoft.NET.Sdk">
+<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
+   <UseWPF>true</UseWPF>
  </PropertyGroup>
</Project>
```

<span data-ttu-id="446bc-240">Pour choisir Windows Forms plutôt que WPF, définissez `UseWindowsForms` au lieu de `UseWPF` :</span><span class="sxs-lookup"><span data-stu-id="446bc-240">To choose Windows Forms over WPF, set `UseWindowsForms` instead of `UseWPF`:</span></span>

```diff
<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
-   <UseWPF>true</UseWPF>
+   <UseWindowsForms>true</UseWindowsForms>
  </PropertyGroup>
</Project>
```

<span data-ttu-id="446bc-241">`UseWPF` et `UseWindowsForms` peuvent être définies sur `true` si l’application utilise les deux infrastructures, par exemple lorsqu’une boîte de dialogue Windows Forms héberge un contrôle WPF.</span><span class="sxs-lookup"><span data-stu-id="446bc-241">Both `UseWPF` and `UseWindowsForms` can be set to `true` if the app uses both frameworks, for example when a Windows Forms dialog is hosting a WPF control.</span></span>

<span data-ttu-id="446bc-242">Partagez vos commentaires sur les référentiels [dotnet/winforms](https://github.com/dotnet/winforms/issues), [dotnet/wpf](https://github.com/dotnet/wpf/issues) et [dotnet/core](https://github.com/dotnet/core/issues).</span><span class="sxs-lookup"><span data-stu-id="446bc-242">Please share your feedback on the [dotnet/winforms](https://github.com/dotnet/winforms/issues),  [dotnet/wpf](https://github.com/dotnet/wpf/issues) and [dotnet/core](https://github.com/dotnet/core/issues) repos.</span></span>

## <a name="msix-deployment-for-windows-desktop"></a><span data-ttu-id="446bc-243">Déploiement MSIX pour Windows Desktop</span><span class="sxs-lookup"><span data-stu-id="446bc-243">MSIX Deployment for Windows Desktop</span></span>

<span data-ttu-id="446bc-244">[MSIX](https://docs.microsoft.com/windows/msix/) est un nouveau format de package d’application Windows.</span><span class="sxs-lookup"><span data-stu-id="446bc-244">[MSIX](https://docs.microsoft.com/windows/msix/) is a new Windows app package format.</span></span> <span data-ttu-id="446bc-245">Il peut être utilisé pour déployer des applications de poste de travail .NET Core 3.0 pour Windows 10.</span><span class="sxs-lookup"><span data-stu-id="446bc-245">It can be used to deploy .NET Core 3.0 desktop applications to Windows 10.</span></span>

<span data-ttu-id="446bc-246">Le [projet de package d’application Windows](https://docs.microsoft.com/windows/uwp/porting/desktop-to-uwp-packaging-dot-net), disponible dans Visual Studio 2019 Preview 2, vous permet de créer des packages MSIX avec des applications .NET Core [autonomes](../deploying/index.md#self-contained-deployments-scd).</span><span class="sxs-lookup"><span data-stu-id="446bc-246">The [Windows Application Packaging Project](https://docs.microsoft.com/windows/uwp/porting/desktop-to-uwp-packaging-dot-net), available in Visual Studio 2019 Preview 2, allows you to create MSIX packages with [self-contained](../deploying/index.md#self-contained-deployments-scd) .NET Core applications.</span></span>

><span data-ttu-id="446bc-247">Remarque : Le fichier projet .NET Core doit spécifier les runtimes pris en charge dans la propriété `<RuntimeIdentifiers>` :</span><span class="sxs-lookup"><span data-stu-id="446bc-247">Note: The .NET Core project file must specify the supported runtimes in the `<RuntimeIdentifiers>` property:</span></span>
```xml
<RuntimeIdentifiers>win-x86;win-x64</RuntimeIdentifiers>
```

## <a name="fast-built-in-json-support"></a><span data-ttu-id="446bc-248">Prise en charge JSON intégrée rapide</span><span class="sxs-lookup"><span data-stu-id="446bc-248">Fast built-in JSON support</span></span>

<span data-ttu-id="446bc-249">L’écosystème .NET s’est appuyé sur [**Json.NET**](https://www.newtonsoft.com/json) et d’autres bibliothèques JSON populaires, qui restent de bons choix.</span><span class="sxs-lookup"><span data-stu-id="446bc-249">The .NET ecosystem has relied on [**Json.NET**](https://www.newtonsoft.com/json) and other popular JSON libraries, which continue to be good choices.</span></span> <span data-ttu-id="446bc-250">**Json.NET** utilise des chaînes .NET comme type de données de base, au format UTF-16.</span><span class="sxs-lookup"><span data-stu-id="446bc-250">**Json.NET** uses .NET strings as its base datatype, which are UTF-16 under the hood.</span></span>

<span data-ttu-id="446bc-251">La nouvelle prise en charge JSON intégrée offre des hautes performances et une allocation faible, et elle est basée sur `Span<byte>`.</span><span class="sxs-lookup"><span data-stu-id="446bc-251">The new built-in JSON support is high-performance, low allocation, and based on `Span<byte>`.</span></span> <span data-ttu-id="446bc-252">Trois nouveaux types principaux liés à JSON ont été ajoutés à l’espace de noms `System.Text.Json` de .NET Core 3.0.</span><span class="sxs-lookup"><span data-stu-id="446bc-252">Three new main JSON-related types have been added to .NET Core 3.0 the `System.Text.Json` namespace.</span></span>

### <a name="utf8jsonreader"></a><span data-ttu-id="446bc-253">Utf8JsonReader</span><span class="sxs-lookup"><span data-stu-id="446bc-253">Utf8JsonReader</span></span>

<span data-ttu-id="446bc-254">`System.Text.Json.Utf8JsonReader` est un lecteur hautes performances et à faible allocation de type forward-only pour le texte JSON codé au format UTF-8 et lu à partir de `ReadOnlySpan<byte>`.</span><span class="sxs-lookup"><span data-stu-id="446bc-254">`System.Text.Json.Utf8JsonReader` is a high-performance, low allocation, forward-only reader for UTF-8 encoded JSON text, read from a `ReadOnlySpan<byte>`.</span></span> <span data-ttu-id="446bc-255">`Utf8JsonReader` est un type fondamental de bas niveau, permettant de générer des analyseurs et des désérialiseurs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="446bc-255">The `Utf8JsonReader` is a foundational, low-level type, that can be leveraged to build custom parsers and deserializers.</span></span> <span data-ttu-id="446bc-256">La lecture d’une charge utile JSON à l’aide du nouveau `Utf8JsonReader` est 2 fois plus rapide qu’avec le lecteur proposé par **Json.NET**.</span><span class="sxs-lookup"><span data-stu-id="446bc-256">Reading through a JSON payload using the new `Utf8JsonReader` is 2x faster than using the reader from **Json.NET**.</span></span> <span data-ttu-id="446bc-257">Ce lecteur n’alloue aucune ressource tant que vous n’avez pas besoin d’actualiser des jetons JSON sous forme de chaînes (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="446bc-257">It does not allocate until you need to actualize JSON tokens as (UTF-16) strings.</span></span>

<span data-ttu-id="446bc-258">Cette nouvelle API inclura les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="446bc-258">This new API will include the following components:</span></span>

* <span data-ttu-id="446bc-259">Préversion 1 : lecteur JSON (accès séquentiel)</span><span class="sxs-lookup"><span data-stu-id="446bc-259">In Preview 1: JSON reader (sequential access)</span></span>
* <span data-ttu-id="446bc-260">Prochainement : enregistreur JSON, DOM (accès aléatoire), sérialiseur poco, désérialiseur poco</span><span class="sxs-lookup"><span data-stu-id="446bc-260">Coming next: JSON writer, DOM (random access), poco serializer, poco deserializer</span></span>

<span data-ttu-id="446bc-261">Voici la boucle de lecteur de base pour le `Utf8JsonReader`, utilisable comme point de départ :</span><span class="sxs-lookup"><span data-stu-id="446bc-261">Here is the basic reader loop for the `Utf8JsonReader` that can be used as a starting point:</span></span>

```csharp
using System.Text.Json;

public static void Utf8JsonReaderLoop(ReadOnlySpan<byte> dataUtf8)
{
    var json = new Utf8JsonReader(dataUtf8, isFinalBlock: true, state: default);

    while (json.Read())
    {
        JsonTokenType tokenType = json.TokenType;
        ReadOnlySpan<byte> valueSpan = json.ValueSpan;
        switch (tokenType)
        {
            case JsonTokenType.StartObject:
            case JsonTokenType.EndObject:
                break;
            case JsonTokenType.StartArray:
            case JsonTokenType.EndArray:
                break;
            case JsonTokenType.PropertyName:
                break;
            case JsonTokenType.String:
                string valueString = json.GetStringValue();
                break;
            case JsonTokenType.Number:
                if (!json.TryGetInt32Value(out int valueInteger))
                {
                    throw new FormatException();
                }
                break;
            case JsonTokenType.True:
            case JsonTokenType.False:
                bool valueBool = json.GetBooleanValue();
                break;
            case JsonTokenType.Null:
                break;
            default:
                throw new ArgumentException();
        }
    }

    dataUtf8 = dataUtf8.Slice((int)json.BytesConsumed);
    JsonReaderState state = json.CurrentState;
}
```

### <a name="utf8jsonwriter"></a><span data-ttu-id="446bc-262">Utf8JsonWriter</span><span class="sxs-lookup"><span data-stu-id="446bc-262">Utf8JsonWriter</span></span>

<span data-ttu-id="446bc-263">`System.Text.Json.Utf8JsonWriter` fournit un moyen d’écrire du texte JSON encodé en UTF-8 partir de types .NET courants, comme `String`, `Int32`, et `DateTime`, avec des hautes performances, sans mise en cache et vers l’avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="446bc-263">`System.Text.Json.Utf8JsonWriter` provides a high-performance, non-cached, forward-only way to write UTF-8 encoded JSON text from common .NET types like `String`, `Int32`, and `DateTime`.</span></span> <span data-ttu-id="446bc-264">Comme le lecteur, l’enregistreur (writer) est un type fondamental de bas niveau, permettant de générer des sérialiseurs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="446bc-264">Like the reader, the writer is a foundational, low-level type, that can be leveraged to build custom serializers.</span></span> <span data-ttu-id="446bc-265">L’écriture d’une charge utile JSON avec le nouveau `Utf8JsonWriter` est de 30 à 80 % plus rapide qu’avec l’enregistreur (writer) de **Json.NET** et il n’effectue pas d’allocation.</span><span class="sxs-lookup"><span data-stu-id="446bc-265">Writing a JSON payload using the new `Utf8JsonWriter` is 30-80% faster than using the writer from **Json.NET** and does not allocate.</span></span>

<span data-ttu-id="446bc-266">Voici un exemple d’utilisation de `Utf8JsonWriter`, qui peut être utilisé comme point de départ :</span><span class="sxs-lookup"><span data-stu-id="446bc-266">Here is a sample usage of the `Utf8JsonWriter` that can be used as a starting point:</span></span>

```csharp
static int WriteJson(IBufferWriter<byte> output, long[] extraData)
{
    var json = new Utf8JsonWriter(output, state: default);

    json.WriteStartObject();

    json.WriteNumber("age", 15, escape: false);
    json.WriteString("date", DateTime.Now);
    json.WriteString("first", "John");
    json.WriteString("last", "Smith");

    json.WriteStartArray("phoneNumbers", escape: false);
    json.WriteStringValue("425-000-1212", escape: false);
    json.WriteStringValue("425-000-1213");
    json.WriteEndArray();

    json.WriteStartObject("address");
    json.WriteString("street", "1 Microsoft Way");
    json.WriteString("city", "Redmond");
    json.WriteNumber("zip", 98052);
    json.WriteEndObject();

    json.WriteStartArray("ExtraArray");
    for (var i = 0; i < extraData.Length; i++)
    {
        json.WriteNumberValue(extraData[i]);
    }
    json.WriteEndArray();

    json.WriteEndObject();

    json.Flush(isFinalBlock: true);

    return (int)json.BytesWritten;
}
```

<span data-ttu-id="446bc-267">Le `Utf8JsonWriter` accepte `IBufferWriter<byte>` comme emplacement de sortie pour y écrire de façon synchrone les données JSON, et en tant qu’appelant, vous devez fournir une implémentation concrète.</span><span class="sxs-lookup"><span data-stu-id="446bc-267">The `Utf8JsonWriter` accepts `IBufferWriter<byte>` as the output location to synchronously write the json data into, and you as the caller need to provide a concrete implementation.</span></span> <span data-ttu-id="446bc-268">Actuellement, la plateforme n’inclut pas d’implémentation de cette interface.</span><span class="sxs-lookup"><span data-stu-id="446bc-268">The platform does not currently include an implementation of this interface.</span></span> <span data-ttu-id="446bc-269">Pour obtenir un exemple de `IBufferWriter<byte>`, consultez [https://gist.github.com/ahsonkhan/c76a1cc4dc7107537c3fdc0079a68b35](https://gist.github.com/ahsonkhan/c76a1cc4dc7107537c3fdc0079a68b35)</span><span class="sxs-lookup"><span data-stu-id="446bc-269">For an example of `IBufferWriter<byte>`, see [https://gist.github.com/ahsonkhan/c76a1cc4dc7107537c3fdc0079a68b35](https://gist.github.com/ahsonkhan/c76a1cc4dc7107537c3fdc0079a68b35)</span></span>

### <a name="jsondocument"></a><span data-ttu-id="446bc-270">JsonDocument</span><span class="sxs-lookup"><span data-stu-id="446bc-270">JsonDocument</span></span>

<span data-ttu-id="446bc-271">`System.Text.Json.JsonDocument` est basé sur le `Utf8JsonReader`.</span><span class="sxs-lookup"><span data-stu-id="446bc-271">`System.Text.Json.JsonDocument` is built on top of the `Utf8JsonReader`.</span></span> <span data-ttu-id="446bc-272">Le `JsonDocument` fournit la possibilité d’analyser les données JSON et de générer un modèle DOM (Document Object Model) qui peut être interrogé, et prendre en charge l’accès aléatoire et l’énumération.</span><span class="sxs-lookup"><span data-stu-id="446bc-272">The `JsonDocument` provides the ability to parse JSON data and build a read-only Document Object Model (DOM) that can be queried to support random access and enumeration.</span></span> <span data-ttu-id="446bc-273">Les éléments JSON qui composent les données sont accessibles via le type `JsonElement` qui est exposé par le `JsonDocument` comme propriété appelée `RootElement`.</span><span class="sxs-lookup"><span data-stu-id="446bc-273">The JSON elements that compose the data can be accessed via the `JsonElement` type which is exposed by the `JsonDocument` as a property called `RootElement`.</span></span> <span data-ttu-id="446bc-274">Le `JsonElement` contient le tableau et les énumérateurs d’objets JSON, ainsi que des API pour convertir le texte JSON en types .NET courants.</span><span class="sxs-lookup"><span data-stu-id="446bc-274">The `JsonElement` contains the JSON array and object enumerators along with APIs to convert JSON text to common .NET types.</span></span> <span data-ttu-id="446bc-275">L’analyse d’une charge utile JSON classique et l’accès à tous ses membres avec le `JsonDocument` est de 2 à 3 fois plus rapide que **Json.NET**, avec très peu d’allocations pour les données de dimension raisonnable (par exemple < 1 Mo).</span><span class="sxs-lookup"><span data-stu-id="446bc-275">Parsing a typical JSON payload and accessing all its members using the `JsonDocument` is 2-3x faster than **Json.NET** with very little allocations for data that is reasonably sized (i.e. < 1 MB).</span></span>

<span data-ttu-id="446bc-276">Voici un exemple d’utilisation de `JsonDocument` et de `JsonElement`, qui peut être utilisé comme point de départ :</span><span class="sxs-lookup"><span data-stu-id="446bc-276">Here is a sample usage of the `JsonDocument` and `JsonElement` that can be used as a starting point:</span></span>

```csharp
static double ParseJson()
{
    const string json = " [ { \"name\": \"John\" }, [ \"425-000-1212\", 15 ], { \"grades\": [ 90, 80, 100, 75 ] } ]";

    double average = -1;

    using (JsonDocument doc = JsonDocument.Parse(json))
    {
        JsonElement root = doc.RootElement;
        JsonElement info = root[1];

        string phoneNumber = info[0].GetString();
        int age = info[1].GetInt32();

        JsonElement grades = root[2].GetProperty("grades");

        double sum = 0;
        foreach (JsonElement grade in grades.EnumerateArray())
        {
            sum += grade.GetInt32();
        }

        int numberOfCourses = grades.GetArrayLength();
        average = sum / numberOfCourses;
    }

    return average;
}
```

## <a name="assembly-unloadability"></a><span data-ttu-id="446bc-277">Non-chargeabilité d’assembly</span><span class="sxs-lookup"><span data-stu-id="446bc-277">Assembly Unloadability</span></span>

<span data-ttu-id="446bc-278">La non-chargeabilité d’assembly est une nouveauté de `AssemblyLoadContext`.</span><span class="sxs-lookup"><span data-stu-id="446bc-278">Assembly unloadability is a new capability of `AssemblyLoadContext`.</span></span> <span data-ttu-id="446bc-279">Cette nouvelle fonctionnalité est largement transparente du point de vue d’une API, exposée avec seulement quelques nouvelles API.</span><span class="sxs-lookup"><span data-stu-id="446bc-279">This new feature is largely transparent from an API perspective, exposed with just a few new APIs.</span></span> <span data-ttu-id="446bc-280">Elle permet à un contexte de chargeur d’être déchargé, libérant toute la mémoire pour les types instanciés, pour les champs statiques et pour l’assembly lui-même.</span><span class="sxs-lookup"><span data-stu-id="446bc-280">It enables a loader context to be unloaded, releasing all memory for instantiated types, static fields and for the assembly itself.</span></span> <span data-ttu-id="446bc-281">Une application doit être en mesure de charger et de décharger définitivement des assemblys via ce mécanisme sans subir de fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="446bc-281">An application should be able to load and unload assemblies via this mechanism forever without experiencing a memory leak.</span></span>

<span data-ttu-id="446bc-282">Cette nouvelle fonctionnalité peut être utilisée pour les scénarios similaires à ceux-ci :</span><span class="sxs-lookup"><span data-stu-id="446bc-282">This new capability can be used for scenarios similar to:</span></span>

* <span data-ttu-id="446bc-283">Scénarios avec des plug-ins, où le chargement et le déchargement de plug-in dynamique est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="446bc-283">Plugin scenarios where dynamic plugin loading and unloading is required.</span></span> 
* <span data-ttu-id="446bc-284">Compilation dynamique, exécution puis vidage du code.</span><span class="sxs-lookup"><span data-stu-id="446bc-284">Dynamically compiling, running and then flushing code.</span></span> <span data-ttu-id="446bc-285">Pratique pour les sites web, les moteurs de script, etc.</span><span class="sxs-lookup"><span data-stu-id="446bc-285">Useful for web sites, scripting engines, etc.</span></span>
* <span data-ttu-id="446bc-286">Le chargement des assemblys pour introspection (comme ReflectionOnlyLoad), bien que [MetadataLoadContext](#type-metadataloadcontext) (publiée dans la version Preview 1) soit un meilleur choix dans de nombreux cas.</span><span class="sxs-lookup"><span data-stu-id="446bc-286">Loading assemblies for introspection (like ReflectionOnlyLoad), although [MetadataLoadContext](#type-metadataloadcontext) (released in Preview 1) will be a better choice in many cases.</span></span>

<span data-ttu-id="446bc-287">Pour plus d’informations, consultez [Using Unloadability](https://github.com/dotnet/coreclr/pull/22221).</span><span class="sxs-lookup"><span data-stu-id="446bc-287">For more information, see the [Using Unloadability](https://github.com/dotnet/coreclr/pull/22221) document.</span></span>

<span data-ttu-id="446bc-288">Le déchargement d’assembly nécessite des précautions considérables pour garantir que toutes les références à des objets gérés d’en dehors d’un contexte de chargeur sont comprises et gérées.</span><span class="sxs-lookup"><span data-stu-id="446bc-288">Assembly unloading requires significant care to ensure that all references to managed objects from outside a loader context are understood and managed.</span></span> <span data-ttu-id="446bc-289">Quand la demande de déchargement du contexte de chargeur est faite, toutes les références qui se trouvent en dehors doivent être déréférencées, afin que le contexte de chargeur soit en cohérence seulement avec lui-même.</span><span class="sxs-lookup"><span data-stu-id="446bc-289">When the loader context is requested to be unloaded, any outside references need to have been unreferenced so that the loader context is self-consistent only to itself.</span></span>

<span data-ttu-id="446bc-290">La non-chargeabilité d’assembly a été fournie dans le .NET Framework par les domaines d’application (AppDomains), qui ne sont pas pris en charge avec .NET Core.</span><span class="sxs-lookup"><span data-stu-id="446bc-290">Assembly unloadability was provided in the .NET Framework by Application Domains (AppDomains), which are not supported with .NET Core.</span></span> <span data-ttu-id="446bc-291">Les domaines d’application avaient des avantages et des limitations par rapport à ce nouveau modèle.</span><span class="sxs-lookup"><span data-stu-id="446bc-291">AppDomains had both benefits and limitations compared to this new model.</span></span> <span data-ttu-id="446bc-292">Considérez ce nouveau modèle de chargeur comme étant plus flexible et plus performant que les domaines d’application.</span><span class="sxs-lookup"><span data-stu-id="446bc-292">Consider this new loader model to be more flexible and higher performant when compared to AppDomains.</span></span>

## <a name="windows-native-interop"></a><span data-ttu-id="446bc-293">Interopérabilité native Windows</span><span class="sxs-lookup"><span data-stu-id="446bc-293">Windows Native Interop</span></span>

<span data-ttu-id="446bc-294">Windows offre une API native riche, sous la forme d’API C plates, de COM et de WinRT.</span><span class="sxs-lookup"><span data-stu-id="446bc-294">Windows offers a rich native API, in the form of flat C APIs, COM, and WinRT.</span></span> <span data-ttu-id="446bc-295">À compter de .NET Core 1.0, **P/Invoke** est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="446bc-295">Since .NET Core 1.0, **P/Invoke** has been supported.</span></span> <span data-ttu-id="446bc-296">Désormais, avec .NET Core 3.0, la prise en charge de la capacité de **cocréer des API COM** et d’**activer des API WinRT** a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="446bc-296">Now with .NET Core 3.0, support for the ability to **CoCreate COM APIs** and **Activate WinRT APIs** has been added.</span></span>

<span data-ttu-id="446bc-297">Vous pouvez voir un exemple d’utilisation de COM avec le [code de source de la démonstration Excel](https://github.com/dotnet/samples/tree/master/core/extensions/ExcelDemo).</span><span class="sxs-lookup"><span data-stu-id="446bc-297">You can see an example of using COM with the [Excel Demo source code](https://github.com/dotnet/samples/tree/master/core/extensions/ExcelDemo).</span></span>


## <a name="type-sequencereader"></a><span data-ttu-id="446bc-298">Type : SequenceReader</span><span class="sxs-lookup"><span data-stu-id="446bc-298">Type: SequenceReader</span></span>

<span data-ttu-id="446bc-299">Dans .NET Core 3.0, `System.Buffers.SequenceReader` a été ajouté et peut servir de lecteur pour `ReadOnlySequence<T>`.</span><span class="sxs-lookup"><span data-stu-id="446bc-299">In .NET Core 3.0, `System.Buffers.SequenceReader` has been added which can be used as a reader for `ReadOnlySequence<T>`.</span></span> <span data-ttu-id="446bc-300">Cela permet une analyse facile, hautes performances et à faible allocation des données `System.IO.Pipelines`, capable de couvrir plusieurs mémoires tampon de stockage.</span><span class="sxs-lookup"><span data-stu-id="446bc-300">This allows easy, high performance, low allocation parsing of `System.IO.Pipelines` data that can cross multiple backing buffers.</span></span> 

<span data-ttu-id="446bc-301">L’exemple suivant segmente une entrée `Sequence` en plusieurs lignes délimitées `CR/LF` valides :</span><span class="sxs-lookup"><span data-stu-id="446bc-301">The following example breaks an input `Sequence` into valid `CR/LF` delimited lines:</span></span>

```csharp
private static ReadOnlySpan<byte> CRLF => new byte[] { (byte)'\r', (byte)'\n' };

public static void ReadLines(ReadOnlySequence<byte> sequence)
{
    SequenceReader<byte> reader = new SequenceReader<byte>(sequence);

    while (!reader.End)
    {
        if (!reader.TryReadToAny(out ReadOnlySpan<byte> line, CRLF, advancePastDelimiter:false))
        {
            // Couldn't find another delimiter
            // ...
        }

        if (!reader.IsNext(CRLF, advancePast: true))
        {
            // Not a good CR/LF pair
            // ...
        }

        // line is valid, process
        ProcessLine(line);
    }
}
```

## <a name="type-metadataloadcontext"></a><span data-ttu-id="446bc-302">Type : MetadataLoadContext</span><span class="sxs-lookup"><span data-stu-id="446bc-302">Type: MetadataLoadContext</span></span>

<span data-ttu-id="446bc-303">Le type `MetadataLoadContext` a été ajouté et permet la lecture des métadonnées de l'assembly sans affecter le domaine d’application de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="446bc-303">The `MetadataLoadContext` type has been added that enables reading assembly metadata without affecting the caller’s application domain.</span></span> <span data-ttu-id="446bc-304">Les assemblys sont lus comme des données, y compris ceux générés pour des architectures et plateformes différentes de l’environnement d’exécution actuel.</span><span class="sxs-lookup"><span data-stu-id="446bc-304">Assemblies are read as data, including assemblies built for different architectures and platforms than the current runtime environment.</span></span> <span data-ttu-id="446bc-305">`MetadataLoadContext` se superpose à <xref:System.Reflection.Assembly.ReflectionOnlyLoad*>, qui est uniquement disponible dans .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="446bc-305">`MetadataLoadContext` overlaps with the <xref:System.Reflection.Assembly.ReflectionOnlyLoad*>, which is only available in the .NET Framework.</span></span>

<span data-ttu-id="446bc-306">`MetdataLoadContext` est disponible dans le [package System.Reflection.MetadataLoadContext](https://www.nuget.org/packages/System.Reflection.MetadataLoadContext).</span><span class="sxs-lookup"><span data-stu-id="446bc-306">`MetdataLoadContext` is available in the [System.Reflection.MetadataLoadContext package](https://www.nuget.org/packages/System.Reflection.MetadataLoadContext).</span></span> <span data-ttu-id="446bc-307">Il s’agit d’un package .NET Standard 2.0.</span><span class="sxs-lookup"><span data-stu-id="446bc-307">It is a .NET Standard 2.0 package.</span></span>

<span data-ttu-id="446bc-308">`MetadataLoadContext` expose les API semblables au type <xref:System.Runtime.Loader.AssemblyLoadContext>, mais il n’est pas basé sur ce type.</span><span class="sxs-lookup"><span data-stu-id="446bc-308">The `MetadataLoadContext` exposes APIs similar to the <xref:System.Runtime.Loader.AssemblyLoadContext> type, but is not based on that type.</span></span> <span data-ttu-id="446bc-309">Tout comme <xref:System.Runtime.Loader.AssemblyLoadContext>, `MetadataLoadContext` permet le chargement d’assemblys dans un univers de chargement d’assemblys isolé.</span><span class="sxs-lookup"><span data-stu-id="446bc-309">Much like <xref:System.Runtime.Loader.AssemblyLoadContext>, the `MetadataLoadContext` enables loading assemblies within an isolated assembly loading universe.</span></span> <span data-ttu-id="446bc-310">Les API `MetdataLoadContext` retournent des objets <xref:System.Reflection.Assembly>, permettant l’utilisation des API de réflexion courantes.</span><span class="sxs-lookup"><span data-stu-id="446bc-310">`MetdataLoadContext` APIs return <xref:System.Reflection.Assembly> objects, enabling the use of familiar reflection APIs.</span></span> <span data-ttu-id="446bc-311">Les API orientées exécution, par exemple [MethodBase.Invoke](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/src/System/Reflection/TypeLoading/Methods/RoMethod.cs#L127), ne sont pas autorisées et renverront une exception InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="446bc-311">Execution-oriented APIs, such as [MethodBase.Invoke](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/src/System/Reflection/TypeLoading/Methods/RoMethod.cs#L127), are not allowed and will throw InvalidOperationException.</span></span>

<span data-ttu-id="446bc-312">L’exemple suivant montre comment rechercher des types concrets dans un assembly qui implémente une interface donnée :</span><span class="sxs-lookup"><span data-stu-id="446bc-312">The following sample demonstrates how to find concrete types in an assembly that implements a given interface:</span></span>

```csharp
var paths = new string[] {@"C:\myapp\mscorlib.dll", @"C:\myapp\myapp.dll"};
var resolver = new PathAssemblyResolver(paths);
using (var lc = new MetadataLoadContext(resolver))
{
    Assembly a = lc.LoadFromAssemblyName("myapp");
    Type myInterface = a.GetType("MyApp.IPluginInterface");
    foreach (Type t in a.GetTypes())
    {
        if (t.IsClass && myInterface.IsAssignableFrom(t))
            Console.WriteLine($"Class {t.FullName} implements IPluginInterface");
    }
}
```

<span data-ttu-id="446bc-313">Les scénarios pour `MetadataLoadContext` incluent des fonctionnalités et des outils au moment de la conception, ainsi que des fonctionnalités de runtime qui doivent inspecter un ensemble d’assemblys en tant que données et dont l’intégralité des verrous appliqués aux fichiers et à la mémoire doivent être supprimés une l’inspection terminée.</span><span class="sxs-lookup"><span data-stu-id="446bc-313">Scenarios for `MetadataLoadContext` include design-time features, build-time tooling, and runtime light-up features that need to inspect a set of assemblies as data and have all file locks and memory freed after inspection is performed.</span></span>

<span data-ttu-id="446bc-314">`MetadataLoadContext` contient une classe de résolution passée à son constructeur.</span><span class="sxs-lookup"><span data-stu-id="446bc-314">The `MetadataLoadContext` has a resolver class passed to its constructor.</span></span> <span data-ttu-id="446bc-315">La tâche du programme de résolution consiste à charger un `Assembly` en fonction de son `AssemblyName`.</span><span class="sxs-lookup"><span data-stu-id="446bc-315">The resolver's job is to load an `Assembly` given its `AssemblyName`.</span></span> <span data-ttu-id="446bc-316">La classe de résolution est dérivée de la classe abstraite `MetadataAssemblyResolver`.</span><span class="sxs-lookup"><span data-stu-id="446bc-316">The resolver class derives from the abstract `MetadataAssemblyResolver` class.</span></span> <span data-ttu-id="446bc-317">Une implémentation du programme de résolution pour des scénarios basés sur le chemin d’accès est fournie avec `PathAssemblyResolver`.</span><span class="sxs-lookup"><span data-stu-id="446bc-317">An implementation of the resolver for path-based scenarios is provided with `PathAssemblyResolver`.</span></span>

<span data-ttu-id="446bc-318">Les [tests MetadataLoadContext](https://github.com/dotnet/corefx/tree/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests) illustrent de nombreux cas d’usage.</span><span class="sxs-lookup"><span data-stu-id="446bc-318">The [MetadataLoadContext tests](https://github.com/dotnet/corefx/tree/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests) demonstrate many use cases.</span></span> <span data-ttu-id="446bc-319">Les [tests Assembly](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests/Assembly/AssemblyTests.cs) constituent un bon point de départ.</span><span class="sxs-lookup"><span data-stu-id="446bc-319">The [Assembly tests](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests/Assembly/AssemblyTests.cs) are a good place to start.</span></span>

## <a name="tls-13--openssl-111-on-linux"></a><span data-ttu-id="446bc-320">TLS 1.3 et OpenSSL 1.1.1 sous Linux</span><span class="sxs-lookup"><span data-stu-id="446bc-320">TLS 1.3 & OpenSSL 1.1.1 on Linux</span></span>

<span data-ttu-id="446bc-321">.NET Core tire désormais parti de la [prise en charge de TLS 1.3 dans OpenSSL 1.1.1](https://www.openssl.org/blog/blog/2018/09/11/release111/), si disponible dans un environnement donné.</span><span class="sxs-lookup"><span data-stu-id="446bc-321">.NET Core will now take advantage of [TLS 1.3 support in OpenSSL 1.1.1](https://www.openssl.org/blog/blog/2018/09/11/release111/), when it is available in a given environment.</span></span> <span data-ttu-id="446bc-322">Selon l’[équipe OpenSSL](https://www.openssl.org/blog/blog/2018/09/11/release111/), TLS 1.3 présentent plusieurs avantages :</span><span class="sxs-lookup"><span data-stu-id="446bc-322">There are multiple benefits of TLS 1.3, per the [OpenSSL team](https://www.openssl.org/blog/blog/2018/09/11/release111/):</span></span>

* <span data-ttu-id="446bc-323">Délais de connexion améliorés grâce à une réduction du nombre d’allers-retours requis entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="446bc-323">Improved connection times due to a reduction in the number of round trips required between the client and server.</span></span>

* <span data-ttu-id="446bc-324">Sécurité améliorée grâce à la suppression de différents algorithmes de chiffrement obsolètes et non sécurisés et à un chiffrement plus complet de la négociation de connexion.</span><span class="sxs-lookup"><span data-stu-id="446bc-324">Improved security due to the removal of various obsolete and insecure cryptographic algorithms and encryption of more of the connection handshake.</span></span>

<span data-ttu-id="446bc-325">.NET Core 3.0 Préversion 1 est capable d’utiliser **OpenSSL 1.1.1**, **OpenSSL 1.1.0** ou **OpenSSL 1.0.2** (soit la meilleure version trouvée, sur un système Linux).</span><span class="sxs-lookup"><span data-stu-id="446bc-325">.NET Core 3.0 Preview 1 is capable of utilizing **OpenSSL 1.1.1**, **OpenSSL 1.1.0**, or **OpenSSL 1.0.2** (whatever the best version found is, on a Linux system).</span></span>  <span data-ttu-id="446bc-326">Si **OpenSSL 1.1.1** est disponible, les types SslStream et HttpClient utiliseront **TLS 1.3** avec `SslProtocols.None` (protocoles système par défaut), en supposant que le client et le serveur prennent en charge **TLS 1.3**.</span><span class="sxs-lookup"><span data-stu-id="446bc-326">When **OpenSSL 1.1.1** is available the SslStream and HttpClient types will use **TLS 1.3** when using `SslProtocols.None` (system default protocols), assuming both the client and server support **TLS 1.3**.</span></span>

<span data-ttu-id="446bc-327">L’exemple suivant montre comment .NET Core 3.0 Préversion 1 sous Ubuntu 18.10 se connecte à <https://www.cloudflare.com> :</span><span class="sxs-lookup"><span data-stu-id="446bc-327">The following sample demonstrates .NET Core 3.0 Preview 1 on Ubuntu 18.10 connecting to <https://www.cloudflare.com>:</span></span>

```csharp
using System;
using System.Net.Security;
using System.Net.Sockets;
using System.Threading.Tasks;

namespace tlstest
{
    class Program
    {
        static async Task Main()
        {
            using (TcpClient tcpClient = new TcpClient())
            {
                string targetHost = "www.cloudflare.com";

                await tcpClient.ConnectAsync(targetHost, 443);

                using (SslStream sslStream = new SslStream(tcpClient.GetStream()))
                {
                    await sslStream.AuthenticateAsClientAsync(targetHost);
                    await Console.Out.WriteLineAsync($"Connected to {targetHost} with {sslStream.SslProtocol}");
                }
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/tlstest$ dotnet run
Connected to www.cloudflare.com with Tls13
user@comp-ubuntu1810:~/tlstest$ openssl version
OpenSSL 1.1.1  11 Sep 2018
```

>[!IMPORTANT]
><span data-ttu-id="446bc-328">Windows et macOS ne prennent pas encore en charge **TLS 1.3**.</span><span class="sxs-lookup"><span data-stu-id="446bc-328">Windows and macOS do not yet support **TLS 1.3**.</span></span> <span data-ttu-id="446bc-329">.NET Core 3.0 prendra en charge **TLS 1.3** sur ces systèmes d’exploitation dès que de la prise en charge sera disponible.</span><span class="sxs-lookup"><span data-stu-id="446bc-329">.NET Core 3.0 will support **TLS 1.3** on these operating systems when support becomes available.</span></span>

## <a name="cryptography"></a><span data-ttu-id="446bc-330">Chiffrement</span><span class="sxs-lookup"><span data-stu-id="446bc-330">Cryptography</span></span>

<span data-ttu-id="446bc-331">La prise en charge a été ajoutée pour les chiffrements **AES-GCM** et **AES-CCM**, avec une implémentation via `System.Security.Cryptography.AesGcm` et `System.Security.Cryptography.AesCcm`.</span><span class="sxs-lookup"><span data-stu-id="446bc-331">Support has been added for **AES-GCM** and **AES-CCM** ciphers, implemented via `System.Security.Cryptography.AesGcm` and `System.Security.Cryptography.AesCcm`.</span></span> <span data-ttu-id="446bc-332">Ces algorithmes sont de type [Authenticated Encryption with Association Data (AEAD)](https://en.wikipedia.org/wiki/Authenticated_encryption), et les premiers algorithmes Authenticated Encryption (AE) ont été ajoutés à .NET Core.</span><span class="sxs-lookup"><span data-stu-id="446bc-332">These algorithms are both [Authenticated Encryption with Association Data (AEAD) algorithms](https://en.wikipedia.org/wiki/Authenticated_encryption), and the first Authenticated Encryption (AE) algorithms added to .NET Core.</span></span>

<span data-ttu-id="446bc-333">Le code suivant montre l’utilisation du chiffrement **AesGcm** pour chiffrer et déchiffrer des données aléatoires.</span><span class="sxs-lookup"><span data-stu-id="446bc-333">The following code demonstrates using **AesGcm** cipher to encrypt and decrypt random data.</span></span>

<span data-ttu-id="446bc-334">Le code pour **AesCcm** sera presque identique (seuls les noms des variables de classe seraient différents).</span><span class="sxs-lookup"><span data-stu-id="446bc-334">The code for **AesCcm** would look almost identical (only the class variable names would be different).</span></span>

```csharp
// key should be: pre-known, derived, or transported via another channel, such as RSA encryption
byte[] key = new byte[16];
RandomNumberGenerator.Fill(key);

byte[] nonce = new byte[12];
RandomNumberGenerator.Fill(nonce);

// normally this would be your data
byte[] dataToEncrypt = new byte[1234];
byte[] associatedData = new byte[333];
RandomNumberGenerator.Fill(dataToEncrypt);
RandomNumberGenerator.Fill(associatedData);

// these will be filled during the encryption
byte[] tag = new byte[16];
byte[] ciphertext = new byte[dataToEncrypt.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Encrypt(nonce, dataToEncrypt, ciphertext, tag, associatedData);
}

// tag, nonce, ciphertext, associatedData should be sent to the other part

byte[] decryptedData = new byte[ciphertext.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Decrypt(nonce, ciphertext, tag, decryptedData, associatedData);
}

// do something with the data
// this should always print that data is the same
Console.WriteLine($"AES-GCM: Decrypted data is{(dataToEncrypt.SequenceEqual(decryptedData) ? "the same as" : "different than")} original data.");
```

## <a name="cryptographic-key-importexport"></a><span data-ttu-id="446bc-335">Importation/exportation d’une clé de chiffrement</span><span class="sxs-lookup"><span data-stu-id="446bc-335">Cryptographic Key Import/Export</span></span>

<span data-ttu-id="446bc-336">.NET Core 3.0 Préversion 1 prend en charge l’importation et l’exportation de clés publiques et privées asymétriques aux formats standard, sans avoir à utiliser un certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="446bc-336">.NET Core 3.0 Preview 1 supports the import and export of asymmetric public and private keys from standard formats, without needing to use an X.509 certificate.</span></span>

<span data-ttu-id="446bc-337">Tous les types de clés (RSA, DSA, ECDsa, ECDiffieHellman) prennent en charge le format **X.509 SubjectPublicKeyInfo** pour les clés publiques, et les formats **PKCS #8 PrivateKeyInfo** et **PKCS #8 EncryptedPrivateKeyInfo** pour les clés privées.</span><span class="sxs-lookup"><span data-stu-id="446bc-337">All key types (RSA, DSA, ECDsa, ECDiffieHellman) support the **X.509 SubjectPublicKeyInfo** format for public keys, and the **PKCS#8 PrivateKeyInfo** and **PKCS#8 EncryptedPrivateKeyInfo** formats for private keys.</span></span> <span data-ttu-id="446bc-338">Le chiffrement RSA prend également en charge **PKCS #1 RSAPublicKey** et **PKCS #1 RSAPrivateKey**.</span><span class="sxs-lookup"><span data-stu-id="446bc-338">RSA additionally supports **PKCS#1 RSAPublicKey** and **PKCS#1 RSAPrivateKey**.</span></span> <span data-ttu-id="446bc-339">Les méthodes d’exportation produisent toutes des données binaires encodées au format DER, tout comme les méthodes d’importation.</span><span class="sxs-lookup"><span data-stu-id="446bc-339">The export methods all produce DER-encoded binary data, and the import methods expect the same.</span></span> <span data-ttu-id="446bc-340">Si une clé est stockée au format PEM compatible avec le texte, l’appelant devra décoder le contenu au format base64 avant d’appeler une méthode d’importation.</span><span class="sxs-lookup"><span data-stu-id="446bc-340">If a key is stored in the text-friendly PEM format, the caller will need to base64-decode the content before calling an import method.</span></span>

```csharp
using System;
using System.IO;
using System.Security.Cryptography;

namespace rsakeyprint
{
    class Program
    {
        static void Main(string[] args)
        {
            using (RSA rsa = RSA.Create())
            {
                byte[] keyBytes = File.ReadAllBytes(args[0]);
                rsa.ImportRSAPrivateKey(keyBytes, out int bytesRead);
 
                Console.WriteLine($"Read {bytesRead} bytes, {keyBytes.Length-bytesRead} extra byte(s) in file.");
                RSAParameters rsaParameters = rsa.ExportParameters(true);
                Console.WriteLine(BitConverter.ToString(rsaParameters.D));
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/rsakeyprint$ echo Making a small key to save on screen space.
Making a small key to save on screen space.
user@comp-ubuntu1810:~/rsakeyprint$ openssl genrsa 768 | openssl rsa -outform der -out rsa.key
Generating RSA private key, 768 bit long modulus (2 primes)
..+++++++
........+++++++
e is 65537 (0x010001)
writing RSA key
user@comp-ubuntu1810:~/rsakeyprint$ dotnet run rsa.key
Read 461 bytes, 0 extra byte(s) in file.
0F-D0-82-34-F8-13-38-4A-7F-C7-52-4A-F6-93-F8-FB-6D-98-7A-6A-04-3B-BC-35-8C-7D-AC-A5-A3-6E-AD-C1-66-30-81-2C-2A-DE-DA-60-03-6A-2C-D9-76-15-7F-61-97-57-
79-E1-6E-45-62-C3-83-04-97-CB-32-EF-C5-17-5F-99-60-92-AE-B6-34-6F-30-06-03-AC-BF-15-24-43-84-EB-83-60-EF-4D-3B-BD-D9-5D-56-26-F0-51-CE-F1
user@comp-ubuntu1810:~/rsakeyprint$ openssl rsa -in rsa.key -inform der -text -noout | grep -A7 private
privateExponent:
    0f:d0:82:34:f8:13:38:4a:7f:c7:52:4a:f6:93:f8:
    fb:6d:98:7a:6a:04:3b:bc:35:8c:7d:ac:a5:a3:6e:
    ad:c1:66:30:81:2c:2a:de:da:60:03:6a:2c:d9:76:
    15:7f:61:97:57:79:e1:6e:45:62:c3:83:04:97:cb:
    32:ef:c5:17:5f:99:60:92:ae:b6:34:6f:30:06:03:
    ac:bf:15:24:43:84:eb:83:60:ef:4d:3b:bd:d9:5d:
    56:26:f0:51:ce:f1
```

<span data-ttu-id="446bc-341">Les fichiers PKCS #8 peuvent être inspectés avec la classe `System.Security.Cryptography.Pkcs.Pkcs8PrivateKeyInfo`.</span><span class="sxs-lookup"><span data-stu-id="446bc-341">PKCS#8 files can be inspected with the `System.Security.Cryptography.Pkcs.Pkcs8PrivateKeyInfo` class.</span></span>

<span data-ttu-id="446bc-342">Les fichiers PFX/PKCS#12 peuvent être inspectés et manipulés avec `System.Security.Cryptography.Pkcs.Pkcs12Info` et `System.Security.Cryptography.Pkcs.Pkcs12Builder`, respectivement.</span><span class="sxs-lookup"><span data-stu-id="446bc-342">PFX/PKCS#12 files can be inspected and manipulated with `System.Security.Cryptography.Pkcs.Pkcs12Info` and `System.Security.Cryptography.Pkcs.Pkcs12Builder`, respectively.</span></span>

## <a name="serialport-for-linux"></a><span data-ttu-id="446bc-343">SerialPort pour Linux</span><span class="sxs-lookup"><span data-stu-id="446bc-343">SerialPort for Linux</span></span>

<span data-ttu-id="446bc-344">.NET Core 3.0 prend désormais en charge <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType> sous Linux.</span><span class="sxs-lookup"><span data-stu-id="446bc-344">.NET Core 3.0 now supports <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType> on Linux.</span></span>

<span data-ttu-id="446bc-345">Auparavant, .NET Core était uniquement pris en charge grâce au type `SerialPort` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="446bc-345">Previously, .NET Core only supported using the `SerialPort` type on Windows.</span></span>

## <a name="more-bcl-improvements"></a><span data-ttu-id="446bc-346">Plusieurs améliorations BCL</span><span class="sxs-lookup"><span data-stu-id="446bc-346">More BCL Improvements</span></span>

<span data-ttu-id="446bc-347">Les types `Span<T>`, `Memory<T>` et autres types associés qui avaient été introduits dans .NET Core 2.1 ont été optimisées dans .NET Core 3.0.</span><span class="sxs-lookup"><span data-stu-id="446bc-347">The `Span<T>`, `Memory<T>`, and related types that were introduced in .NET Core 2.1, have been optimized in .NET Core 3.0.</span></span> <span data-ttu-id="446bc-348">Les opérations courantes comme la construction de type span, le découpage, l’analyse et la mise en forme sont maintenant plus performantes.</span><span class="sxs-lookup"><span data-stu-id="446bc-348">Common operations such as span construction, slicing, parsing, and formatting now perform better.</span></span> 

<span data-ttu-id="446bc-349">En outre, les types comme `String` ont bénéficié d’améliorations en arrière-plan pour les rendre plus efficaces lorsqu’ils sont utilisés comme des clés avec `Dictionary<TKey, TValue>` et d’autres collections.</span><span class="sxs-lookup"><span data-stu-id="446bc-349">Additionally, types like `String` have seen under-the-cover improvements to make them more efficient when used as keys with `Dictionary<TKey, TValue>` and other collections.</span></span> <span data-ttu-id="446bc-350">Aucune modification de code n’est nécessaire pour tirer parti de ces améliorations.</span><span class="sxs-lookup"><span data-stu-id="446bc-350">No code changes are required to benefit from these improvements.</span></span>

<span data-ttu-id="446bc-351">Les améliorations suivantes sont également des nouveautés dans .NET Core 3 Préversion 1 :</span><span class="sxs-lookup"><span data-stu-id="446bc-351">The following improvements are also new in .NET Core 3 Preview 1:</span></span>

* <span data-ttu-id="446bc-352">Prise en charge de Brotli intégrée à HttpClient</span><span class="sxs-lookup"><span data-stu-id="446bc-352">Brotli support built in to HttpClient</span></span>
* <span data-ttu-id="446bc-353">ThreadPool.UnsafeQueueWorkItem(IThreadPoolWorkItem)</span><span class="sxs-lookup"><span data-stu-id="446bc-353">ThreadPool.UnsafeQueueWorkItem(IThreadPoolWorkItem)</span></span>
* <span data-ttu-id="446bc-354">Unsafe.Unbox</span><span class="sxs-lookup"><span data-stu-id="446bc-354">Unsafe.Unbox</span></span>
* <span data-ttu-id="446bc-355">CancellationToken.Unregister</span><span class="sxs-lookup"><span data-stu-id="446bc-355">CancellationToken.Unregister</span></span>
* <span data-ttu-id="446bc-356">Opérateurs arithmétiques complexes</span><span class="sxs-lookup"><span data-stu-id="446bc-356">Complex arithmetic operators</span></span>
* <span data-ttu-id="446bc-357">API de socket pour TCP keep alive</span><span class="sxs-lookup"><span data-stu-id="446bc-357">Socket APIs for TCP keep alive</span></span>
* <span data-ttu-id="446bc-358">StringBuilder.GetChunks</span><span class="sxs-lookup"><span data-stu-id="446bc-358">StringBuilder.GetChunks</span></span>
* <span data-ttu-id="446bc-359">Analyse IPEndPoint</span><span class="sxs-lookup"><span data-stu-id="446bc-359">IPEndPoint parsing</span></span>
* <span data-ttu-id="446bc-360">RandomNumberGenerator.GetInt32</span><span class="sxs-lookup"><span data-stu-id="446bc-360">RandomNumberGenerator.GetInt32</span></span>

## <a name="tiered-compilation"></a><span data-ttu-id="446bc-361">Compilation hiérarchisée</span><span class="sxs-lookup"><span data-stu-id="446bc-361">Tiered compilation</span></span>

<span data-ttu-id="446bc-362">La [compilation hiérarchisée](https://devblogs.microsoft.com/dotnet/tiered-compilation-preview-in-net-core-2-1/) est activée par défaut avec .NET Core 3.0.</span><span class="sxs-lookup"><span data-stu-id="446bc-362">[Tiered compilation](https://devblogs.microsoft.com/dotnet/tiered-compilation-preview-in-net-core-2-1/) is on by default with .NET Core 3.0.</span></span> <span data-ttu-id="446bc-363">Cette fonctionnalité permet au runtime d’utiliser de manière plus adaptative le compilateur juste-à-temps (Just-In-Time ou JIT) pour obtenir de meilleures performances, à la fois au démarrage et pour optimiser le débit.</span><span class="sxs-lookup"><span data-stu-id="446bc-363">It is a feature that enables the runtime to more adaptively use the Just-In-Time (JIT) compiler to get better performance, both at startup and to maximize throughput.</span></span>

<span data-ttu-id="446bc-364">Cette fonctionnalité avait été ajoutée en option dans [.NET Core 2.1](https://devblogs.microsoft.com/dotnet/announcing-net-core-2-1/) et était activée par défaut dans [.NET Core 2.2 Préversion 2](https://devblogs.microsoft.com/dotnet/announcing-net-core-2-2-preview-2/).</span><span class="sxs-lookup"><span data-stu-id="446bc-364">This feature was added as an opt-in feature in [.NET Core 2.1](https://devblogs.microsoft.com/dotnet/announcing-net-core-2-1/) and then was enabled by default in [.NET Core 2.2 Preview 2](https://devblogs.microsoft.com/dotnet/announcing-net-core-2-2-preview-2/).</span></span> <span data-ttu-id="446bc-365">Elle est ensuite redevenue une option dans la version .NET Core 2.2.</span><span class="sxs-lookup"><span data-stu-id="446bc-365">Subsequently, it has been reverted back to opt in with the .NET Core 2.2 release.</span></span>

## <a name="arm64-linux-support"></a><span data-ttu-id="446bc-366">Support ARM64 Linux</span><span class="sxs-lookup"><span data-stu-id="446bc-366">ARM64 Linux support</span></span>

<span data-ttu-id="446bc-367">La prise en charge d’ARM64 pour Linux a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="446bc-367">Support has been added for ARM64 for Linux.</span></span> <span data-ttu-id="446bc-368">Actuellement, ARM64 est principallement utilisé dans des scénarios IoT.</span><span class="sxs-lookup"><span data-stu-id="446bc-368">The primary use case for ARM64 is currently with IoT scenarios.</span></span>

<span data-ttu-id="446bc-369">Des [images Docker Alpine, Debian et Ubuntu sont disponibles avec .NET Core pour ARM64](https://hub.docker.com/r/microsoft/dotnet/).</span><span class="sxs-lookup"><span data-stu-id="446bc-369">Alpine, Debian and Ubuntu [Docker images are available for .NET Core for ARM64](https://hub.docker.com/r/microsoft/dotnet/).</span></span>

<span data-ttu-id="446bc-370">Consultez [État de .NET Core ARM64](https://github.com/dotnet/announcements/issues/82) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="446bc-370">Please check [.NET Core ARM64 Status](https://github.com/dotnet/announcements/issues/82) for more information.</span></span>

>[!NOTE]
> <span data-ttu-id="446bc-371">La prise en charge d’**ARM64** sous Windows n’est pas encore disponible.</span><span class="sxs-lookup"><span data-stu-id="446bc-371">**ARM64** Windows support isn't yet available.</span></span>

## <a name="install-net-core-30-previews-on-linux-with-snap"></a><span data-ttu-id="446bc-372">Installer des préversions de .NET Core 3.0 sur Linux avec Snap</span><span class="sxs-lookup"><span data-stu-id="446bc-372">Install .NET Core 3.0 Previews on Linux with Snap</span></span>

<span data-ttu-id="446bc-373">Snap est le meilleur moyen d’installer et d’essayer les préversions de .NET Core sur les [distributions Linux qui prennent en charge Snap](https://docs.snapcraft.io/installing-snapd/6735).</span><span class="sxs-lookup"><span data-stu-id="446bc-373">Snap is the preferred way to install and try .NET Core previews on [Linux distributions that support Snap](https://docs.snapcraft.io/installing-snapd/6735).</span></span>

<span data-ttu-id="446bc-374">Après avoir configuré Snap sur votre système, exécutez la commande suivante pour installer le [SDK de .NET Core SDK 3.0 Preview](https://snapcraft.io/dotnet-sdk).</span><span class="sxs-lookup"><span data-stu-id="446bc-374">After configuring Snap on your system, run the following command to install the [.NET Core SDK 3.0 Preview SDK](https://snapcraft.io/dotnet-sdk).</span></span>

```console
sudo snap install dotnet-sdk --beta --classic
```
 
<span data-ttu-id="446bc-375">Quand .NET Core est installé en utilisant le package Snap, la commande .NET Core par défaut est `dotnet-sdk.dotnet`, et non pas simplement `dotnet`.</span><span class="sxs-lookup"><span data-stu-id="446bc-375">When .NET Core in installed using the Snap package, the default .NET Core command is `dotnet-sdk.dotnet`, as opposed to just `dotnet`.</span></span> <span data-ttu-id="446bc-376">L’avantage de la commande avec l’espace de noms est qu’elle ne sera pas en conflit avec une éventuelle version de .NET Core installée globalement.</span><span class="sxs-lookup"><span data-stu-id="446bc-376">The benefit of the namespaced command is that it will not conflict with a globally installed .NET Core version you may have.</span></span> <span data-ttu-id="446bc-377">Vous pouvez créer l’alias `dotnet` pour cette commande avec :</span><span class="sxs-lookup"><span data-stu-id="446bc-377">This command can be aliased to `dotnet` with:</span></span>

```console
sudo snap alias dotnet-sdk.dotnet dotnet
```

<span data-ttu-id="446bc-378">Certaines distributions nécessitent une étape supplémentaire pour permettre l’accès au certificat SSL.</span><span class="sxs-lookup"><span data-stu-id="446bc-378">Some distros require an additional step to enable access to the SSL certificate.</span></span> <span data-ttu-id="446bc-379">Pour plus d’informations, consultez notre [configuration de Linux](https://github.com/dotnet/core/blob/master/Documentation/linux-setup.md).</span><span class="sxs-lookup"><span data-stu-id="446bc-379">See our [Linux Setup](https://github.com/dotnet/core/blob/master/Documentation/linux-setup.md) for details.</span></span>

## <a name="gpio-support-for-raspberry-pi"></a><span data-ttu-id="446bc-380">Prise en charge de GPIO pour Raspberry Pi</span><span class="sxs-lookup"><span data-stu-id="446bc-380">GPIO Support for Raspberry Pi</span></span>

<span data-ttu-id="446bc-381">Deux nouveaux packages ont été publiés sur NuGet, que vous pouvez utiliser pour la programmation de GPIO.</span><span class="sxs-lookup"><span data-stu-id="446bc-381">Two new packages have been released to NuGet that you can use for GPIO programming.</span></span>

* [<span data-ttu-id="446bc-382">System.Device.Gpio</span><span class="sxs-lookup"><span data-stu-id="446bc-382">System.Device.Gpio</span></span>](https://www.nuget.org/packages/System.Device.Gpio/0.1.0-prerelease.19078.2)
* [<span data-ttu-id="446bc-383">Iot.Device.Bindings</span><span class="sxs-lookup"><span data-stu-id="446bc-383">Iot.Device.Bindings</span></span>](https://www.nuget.org/packages/Iot.Device.Bindings/0.1.0-prerelease.19078.2)

<span data-ttu-id="446bc-384">Les packages GPIO incluent des API pour les appareils GPIO, SPI, I2C et PWM.</span><span class="sxs-lookup"><span data-stu-id="446bc-384">The GPIO Packages includes APIs for GPIO, SPI, I2C and PWM devices.</span></span> <span data-ttu-id="446bc-385">Le package de liaisons IoT inclut [des liaisons d’appareil](https://github.com/dotnet/iot/blob/master/src/devices/README.md) pour différents circuits intégrés et capteurs, les mêmes que ceux qui sont disponibles dans [dotnet/iot - src/devices](https://github.com/dotnet/iot/tree/master/src/devices).</span><span class="sxs-lookup"><span data-stu-id="446bc-385">The IoT bindings package includes [device bindings](https://github.com/dotnet/iot/blob/master/src/devices/README.md) for various chips and sensors, the same ones available at [dotnet/iot - src/devices](https://github.com/dotnet/iot/tree/master/src/devices).</span></span>

<span data-ttu-id="446bc-386">Les API de port série mis à jour qui ont été annoncés dans le cadre de .NET Core 3.0 Preview 1 ne font pas partie de ces packages, mais elles sont disponibles dans le cadre de la plateforme .NET Core.</span><span class="sxs-lookup"><span data-stu-id="446bc-386">The updated serial port APIs that were announced as part of .NET Core 3.0 Preview 1 are not part of these packages but are available as part of the .NET Core platform.</span></span>


## <a name="platform-support"></a><span data-ttu-id="446bc-387">Prise en charge de plateforme</span><span class="sxs-lookup"><span data-stu-id="446bc-387">Platform Support</span></span>

<span data-ttu-id="446bc-388">.NET Core 3 sera pris en charge sur les systèmes d’exploitation suivants :</span><span class="sxs-lookup"><span data-stu-id="446bc-388">.NET Core 3 will be supported on the following operating systems:</span></span>

* <span data-ttu-id="446bc-389">Client Windows : 7, 8.1, 10 (1607+)</span><span class="sxs-lookup"><span data-stu-id="446bc-389">Windows Client: 7, 8.1, 10 (1607+)</span></span>
* <span data-ttu-id="446bc-390">Windows Server : 2012 R2 SP1+</span><span class="sxs-lookup"><span data-stu-id="446bc-390">Windows Server: 2012 R2 SP1+</span></span>
* <span data-ttu-id="446bc-391">macOS : 10.12+</span><span class="sxs-lookup"><span data-stu-id="446bc-391">macOS: 10.12+</span></span>
* <span data-ttu-id="446bc-392">RHEL : 6+</span><span class="sxs-lookup"><span data-stu-id="446bc-392">RHEL: 6+</span></span>
* <span data-ttu-id="446bc-393">Fedora : 26+</span><span class="sxs-lookup"><span data-stu-id="446bc-393">Fedora: 26+</span></span>
* <span data-ttu-id="446bc-394">Ubuntu : 16.04+</span><span class="sxs-lookup"><span data-stu-id="446bc-394">Ubuntu: 16.04+</span></span>
* <span data-ttu-id="446bc-395">Debian : 9+</span><span class="sxs-lookup"><span data-stu-id="446bc-395">Debian: 9+</span></span>
* <span data-ttu-id="446bc-396">SLES : 12+</span><span class="sxs-lookup"><span data-stu-id="446bc-396">SLES: 12+</span></span>
* <span data-ttu-id="446bc-397">openSUSE : 42.3+</span><span class="sxs-lookup"><span data-stu-id="446bc-397">openSUSE: 42.3+</span></span>
* <span data-ttu-id="446bc-398">Alpine : 3.8+</span><span class="sxs-lookup"><span data-stu-id="446bc-398">Alpine: 3.8+</span></span>

<span data-ttu-id="446bc-399">La prise en charge des circuits intégrés suit :</span><span class="sxs-lookup"><span data-stu-id="446bc-399">Chip support follows:</span></span>

* <span data-ttu-id="446bc-400">x64 sur Windows, macOS et Linux</span><span class="sxs-lookup"><span data-stu-id="446bc-400">x64 on Windows, macOS, and Linux</span></span>
* <span data-ttu-id="446bc-401">x86 sur Windows</span><span class="sxs-lookup"><span data-stu-id="446bc-401">x86 on Windows</span></span>
* <span data-ttu-id="446bc-402">ARM32 sur Windows et Linux</span><span class="sxs-lookup"><span data-stu-id="446bc-402">ARM32 on Windows and Linux</span></span>
* <span data-ttu-id="446bc-403">ARM64 sur Linux</span><span class="sxs-lookup"><span data-stu-id="446bc-403">ARM64 on Linux</span></span>

<span data-ttu-id="446bc-404">Pour Linux, ARM32 est pris en charge sur Debian 9+ et Ubuntu 16.04+.</span><span class="sxs-lookup"><span data-stu-id="446bc-404">For Linux, ARM32 is supported on Debian 9+ and Ubuntu 16.04+.</span></span> <span data-ttu-id="446bc-405">Pour ARM64, la prise en charge est identique à ARM32, avec en plus Alpine 3.8.</span><span class="sxs-lookup"><span data-stu-id="446bc-405">For ARM64, it is the same as ARM32 with the addition of Alpine 3.8.</span></span> <span data-ttu-id="446bc-406">Il s’agit des mêmes versions de ces distributions que ce qui est pris en charge pour X64.</span><span class="sxs-lookup"><span data-stu-id="446bc-406">These are the same versions of those distros as is supported for X64.</span></span>

<span data-ttu-id="446bc-407">Les images Docker pour .NET Core 3.0 sont disponibles dans [microsoft/dotnet sur Docker Hub](https://hub.docker.com/r/microsoft/dotnet/).</span><span class="sxs-lookup"><span data-stu-id="446bc-407">Docker images for .NET Core 3.0 are available at [microsoft/dotnet on Docker Hub](https://hub.docker.com/r/microsoft/dotnet/).</span></span> <span data-ttu-id="446bc-408">Microsoft travaille actuellement à l’adoption du [Registre de conteneurs Microsoft (MCR, Microsoft Container Registry)](https://cloudblogs.microsoft.com/opensource/2019/01/17/improved-discovery-experience-microsoft-containers-docker-hub/) et il est prévu que les images .NET Core 3.0 finales soient publiées seulement sur MCR.</span><span class="sxs-lookup"><span data-stu-id="446bc-408">Microsoft is currently in the process of adopting [Microsoft Container Registry (MCR)](https://cloudblogs.microsoft.com/opensource/2019/01/17/improved-discovery-experience-microsoft-containers-docker-hub/) and it is expected that the final .NET Core 3.0 images will only be published to MCR.</span></span>
