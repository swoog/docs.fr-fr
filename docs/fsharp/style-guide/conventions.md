---
title: 'Conventions de codage F #'
description: 'Découvrez les recommandations générales et idiomes lors de l’écriture de code F #.'
ms.date: 05/14/2018
ms.openlocfilehash: f3d16f735ddc1901aeaa5ebb39e2fa2b70a3d836
ms.sourcegitcommit: 43924acbdbb3981d103e11049bbe460457d42073
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2018
ms.locfileid: "34457980"
---
# <a name="f-coding-conventions"></a><span data-ttu-id="34034-103">Conventions de codage F #</span><span class="sxs-lookup"><span data-stu-id="34034-103">F# coding conventions</span></span>

<span data-ttu-id="34034-104">Les conventions suivantes sont formulées d’une expérience d’utilisation de grande taille) (F # codebases.</span><span class="sxs-lookup"><span data-stu-id="34034-104">The following conventions are formulated from experience working with large F# codebases.</span></span> <span data-ttu-id="34034-105">Le [cinq principes du bon code F #](index.md#five-principles-of-good-f-code) constituent la base de chaque recommandation.</span><span class="sxs-lookup"><span data-stu-id="34034-105">The [Five principles of good F# code](index.md#five-principles-of-good-f-code) are the foundation of each recommendation.</span></span> <span data-ttu-id="34034-106">Elles sont liées à la [règles de conception du composant F #](component-design-guidelines.md), mais s’appliquent à n’importe quel code F #, pas seulement les composants tels que les bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="34034-106">They are related to the [F# component design guidelines](component-design-guidelines.md), but are applicable for any F# code, not just components such as libraries.</span></span>

## <a name="organizing-code"></a><span data-ttu-id="34034-107">Organisation du code</span><span class="sxs-lookup"><span data-stu-id="34034-107">Organizing code</span></span>

<span data-ttu-id="34034-108">Fonctionnalités de deux méthodes principales pour organiser le code F # : les modules et les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="34034-108">F# features two primary ways to organize code: modules and namespaces.</span></span> <span data-ttu-id="34034-109">Ceux-ci sont similaires, mais que vous n’ont pas les différences suivantes :</span><span class="sxs-lookup"><span data-stu-id="34034-109">These are similar, but do have the following differences:</span></span>

* <span data-ttu-id="34034-110">Espaces de noms sont compilés en tant qu’espaces de noms .NET.</span><span class="sxs-lookup"><span data-stu-id="34034-110">Namespaces are compiled as .NET namespaces.</span></span> <span data-ttu-id="34034-111">Les modules sont compilés en tant que classes statiques.</span><span class="sxs-lookup"><span data-stu-id="34034-111">Modules are compiled as static classes.</span></span>
* <span data-ttu-id="34034-112">Espaces de noms sont toujours de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="34034-112">Namespaces are always top level.</span></span> <span data-ttu-id="34034-113">Modules peuvent être imbriqués dans d’autres modules et de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="34034-113">Modules can be top-level and nested within other modules.</span></span>
* <span data-ttu-id="34034-114">Espaces de noms peut s’étendre sur plusieurs fichiers.</span><span class="sxs-lookup"><span data-stu-id="34034-114">Namespaces can span multiple files.</span></span> <span data-ttu-id="34034-115">Les modules ne peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="34034-115">Modules cannot.</span></span>
* <span data-ttu-id="34034-116">Modules peuvent être décorées avec `[<RequireQualifiedAccess>]` et `[<AutoOpen>]`.</span><span class="sxs-lookup"><span data-stu-id="34034-116">Modules can be decorated with `[<RequireQualifiedAccess>]` and `[<AutoOpen>]`.</span></span>

<span data-ttu-id="34034-117">Les instructions suivantes vous aideront à utiliser pour organiser votre code.</span><span class="sxs-lookup"><span data-stu-id="34034-117">The following guidelines will help you use these to organize your code.</span></span>

### <a name="prefer-namespaces-at-the-top-level"></a><span data-ttu-id="34034-118">Préférez des espaces de noms au niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="34034-118">Prefer namespaces at the top level</span></span>

<span data-ttu-id="34034-119">Pour tout code utilisable publiquement, espaces de noms sont préférentiels aux modules au niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="34034-119">For any publicly consumable code, namespaces are preferential to modules at the top level.</span></span> <span data-ttu-id="34034-120">Car ils sont compilés en tant qu’espaces de noms .NET, elles sont utilisable à partir de c# sans problème.</span><span class="sxs-lookup"><span data-stu-id="34034-120">Because they are compiled as .NET namespaces, they are consumable from C# with no issue.</span></span>

```fsharp
// Good!
namespace MyCode

type MyClass() =
    ...
```

<span data-ttu-id="34034-121">À l’aide d’un module de niveau supérieur peuvent ne pas apparaît différent lorsqu’elle est appelée uniquement à partir de F #, mais les consommateurs de c#, les appelants peuvent être surpris par devoir qualifier `MyClass` avec la `MyCode` module.</span><span class="sxs-lookup"><span data-stu-id="34034-121">Using a top-level module may not appear different when called only from F#, but for C# consumers, callers may be surprised by having to qualify `MyClass` with the `MyCode` module.</span></span>

```fsharp
// Bad!
module MyCode

type MyClass() =
    ...
```

### <a name="carefully-apply-autoopen"></a><span data-ttu-id="34034-122">Avec soin s’appliquent `[<AutoOpen>]`</span><span class="sxs-lookup"><span data-stu-id="34034-122">Carefully apply `[<AutoOpen>]`</span></span>

<span data-ttu-id="34034-123">Le `[<AutoOpen>]` construction peut pollue pas l’étendue de ce qui est disponible pour les appelants, et la réponse à quelque chose la provenance est « magique ».</span><span class="sxs-lookup"><span data-stu-id="34034-123">The `[<AutoOpen>]` construct can pollute the scope of what is available to callers, and the answer to where something comes from is "magic".</span></span> <span data-ttu-id="34034-124">Cela n’est généralement pas une bonne chose.</span><span class="sxs-lookup"><span data-stu-id="34034-124">This is generally not a good thing.</span></span> <span data-ttu-id="34034-125">Une exception à cette règle est la bibliothèque principale F # lui-même (même si cela est également un peu controversé).</span><span class="sxs-lookup"><span data-stu-id="34034-125">An exception to this rule is the F# Core Library itself (though this fact is also a bit controversial).</span></span>

<span data-ttu-id="34034-126">Toutefois, il est pratique si vous disposez des fonctionnalités d’assistance pour une API publique que vous souhaitez organiser séparément à partir de cette API publique.</span><span class="sxs-lookup"><span data-stu-id="34034-126">However, it is a convenience if you have helper functionality for a public API that you wish to organize separately from that public API.</span></span>

```fsharp
module MyAPI =
    [<AutoOpen>]
    module private Helpers =
        let helper1 x y z =
            ...


    let myFunction1 x =
        let y = ...
        let z = ...

        helper1 x y z
```

<span data-ttu-id="34034-127">Cela vous permet de détails de l’implémentation distincte correctement à partir de l’API publique d’une fonction sans avoir à qualifier complètement un programme d’assistance à chaque fois que vous l’appelez.</span><span class="sxs-lookup"><span data-stu-id="34034-127">This lets you cleanly separate implementation details from the public API of a function without having to fully qualify a helper each time you call it.</span></span>

<span data-ttu-id="34034-128">En outre, exposer des méthodes d’extension et les générateurs d’expressions au niveau de l’espace de noms peut être parfaitement exprimée avec `[<AutoOpen>]`.</span><span class="sxs-lookup"><span data-stu-id="34034-128">Additionally, exposing extension methods and expression builders at the namespace level can be neatly expressed with `[<AutoOpen>]`.</span></span>

### <a name="use-requirequalifiedaccess-whenever-names-could-conflict-or-you-feel-it-helps-with-readability"></a><span data-ttu-id="34034-129">Utilisez `[<RequireQualifiedAccess>]` chaque fois que les noms peuvent être en conflit ou si vous pensez qu’il facilite la lisibilité</span><span class="sxs-lookup"><span data-stu-id="34034-129">Use `[<RequireQualifiedAccess>]` whenever names could conflict or you feel it helps with readability</span></span>

<span data-ttu-id="34034-130">Ajout de la `[<RequireQualifiedAccess>]` attribut à un module indique que le module ne peut-être pas être ouvertes et des références aux éléments du module doivent explicite qualifié accès.</span><span class="sxs-lookup"><span data-stu-id="34034-130">Adding the `[<RequireQualifiedAccess>]` attribute to a module indicates that the module may not be opened and that references to the elements of the module require explicit qualified access.</span></span> <span data-ttu-id="34034-131">Par exemple, le `Microsoft.FSharp.Collections.List` module a cet attribut.</span><span class="sxs-lookup"><span data-stu-id="34034-131">For example, the `Microsoft.FSharp.Collections.List` module has this attribute.</span></span>

<span data-ttu-id="34034-132">Cela est utile lorsque les valeurs dans le module et les fonctions ont des noms qui sont susceptibles d’entrer en conflit avec les noms dans d’autres modules.</span><span class="sxs-lookup"><span data-stu-id="34034-132">This is useful when functions and values in the module have names that are likely to conflict with names in other modules.</span></span> <span data-ttu-id="34034-133">Nécessitant un accès complet peut considérablement améliorer la facilité de maintenance à long terme et evolvability d’une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="34034-133">Requiring qualified access can greatly increase the long-term maintainability and evolvability of a library.</span></span>

```fsharp
[<RequireQualifiedAccess>]
module StringTokenization =
    let parse s = ...

...

let s = getAString()
let parsed = StringTokenization.parse s // Must qualify to use 'parse'
```

### <a name="sort-open-statements-topologically"></a><span data-ttu-id="34034-134">Tri `open` instructions topologiquement</span><span class="sxs-lookup"><span data-stu-id="34034-134">Sort `open` statements topologically</span></span>

<span data-ttu-id="34034-135">En F #, l’ordre des déclarations est important, notamment avec `open` instructions.</span><span class="sxs-lookup"><span data-stu-id="34034-135">In F#, the order of declarations matters, including with `open` statements.</span></span> <span data-ttu-id="34034-136">Contrairement à c#, où l’effet de `using` et `using static` est indépendante de l’ordre de ces instructions dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="34034-136">This is unlike C#, where the effect of `using` and `using static` is independent of the ordering of those statements in a file.</span></span>

<span data-ttu-id="34034-137">En F #, éléments ouverts dans une étendue peuvent occulter autres déjà présent.</span><span class="sxs-lookup"><span data-stu-id="34034-137">In F#, elements opened into a scope can shadow others already present.</span></span> <span data-ttu-id="34034-138">Cela signifie que la réorganisation `open` instructions Impossible de modifier la signification du code.</span><span class="sxs-lookup"><span data-stu-id="34034-138">This means that reordering `open` statements could alter the meaning of code.</span></span> <span data-ttu-id="34034-139">Par conséquent, toute arbitraire de tri de tous les `open` instructions (par exemple, dans l’ordre alphanumérique) n’est généralement pas recommandé, moins vous générez un comportement différent que vous pouvez vous attendre.</span><span class="sxs-lookup"><span data-stu-id="34034-139">As a result, any arbitrary sorting of all `open` statements (for example, alphanumerically) is generally not recommended, lest you generate different behavior that you might expect.</span></span>

<span data-ttu-id="34034-140">Au lieu de cela, nous vous recommandons de les trier [topologiquement](https://en.wikipedia.org/wiki/Topological_sorting); autrement dit, la commande votre `open` dans l’ordre dans lequel les instructions _couches_ de votre système sont définis.</span><span class="sxs-lookup"><span data-stu-id="34034-140">Instead, we recommend that you sort them [topologically](https://en.wikipedia.org/wiki/Topological_sorting); that is, order your `open` statements in the order in which _layers_ of your system are defined.</span></span> <span data-ttu-id="34034-141">Effectuant alphanumérique de tri au sein des différentes couches topologiques peut également être considéré comme.</span><span class="sxs-lookup"><span data-stu-id="34034-141">Doing alphanumeric sorting within different topological layers may also be considered.</span></span>

<span data-ttu-id="34034-142">Par exemple, voici le tri topologique pour le fichier F # du compilateur service public API :</span><span class="sxs-lookup"><span data-stu-id="34034-142">As an example, here is the topological sorting for the F# compiler service public API file:</span></span>

```fsharp
namespace Microsoft.FSharp.Compiler.SourceCodeServices

open System
open System.Collections.Generic
open System.Collections.Concurrent
open System.Diagnostics
open System.IO
open System.Reflection
open System.Text

open Microsoft.FSharp.Compiler
open Microsoft.FSharp.Compiler.AbstractIL
open Microsoft.FSharp.Compiler.AbstractIL.Diagnostics
open Microsoft.FSharp.Compiler.AbstractIL.IL
open Microsoft.FSharp.Compiler.AbstractIL.ILBinaryReader
open Microsoft.FSharp.Compiler.AbstractIL.Internal
open Microsoft.FSharp.Compiler.AbstractIL.Internal.Library

open Microsoft.FSharp.Compiler.AccessibilityLogic
open Microsoft.FSharp.Compiler.Ast
open Microsoft.FSharp.Compiler.CompileOps
open Microsoft.FSharp.Compiler.CompileOptions
open Microsoft.FSharp.Compiler.Driver
open Microsoft.FSharp.Compiler.ErrorLogger
open Microsoft.FSharp.Compiler.Infos
open Microsoft.FSharp.Compiler.InfoReader
open Microsoft.FSharp.Compiler.Lexhelp
open Microsoft.FSharp.Compiler.Layout
open Microsoft.FSharp.Compiler.Lib
open Microsoft.FSharp.Compiler.NameResolution
open Microsoft.FSharp.Compiler.PrettyNaming
open Microsoft.FSharp.Compiler.Parser
open Microsoft.FSharp.Compiler.Range
open Microsoft.FSharp.Compiler.Tast
open Microsoft.FSharp.Compiler.Tastops
open Microsoft.FSharp.Compiler.TcGlobals
open Microsoft.FSharp.Compiler.TypeChecker
open Microsoft.FSharp.Compiler.SourceCodeServices.SymbolHelpers

open Internal.Utilities
open Internal.Utilities.Collections
```

<span data-ttu-id="34034-143">Notez qu’un saut de ligne sépare les couches topologiques, avec chaque couche qui est triée par ordre alphabétique par la suite.</span><span class="sxs-lookup"><span data-stu-id="34034-143">Note that a line break separates topological layers, with each layer being sorted alphanumerically afterwards.</span></span> <span data-ttu-id="34034-144">Cela organise correctement code sans accidentellement clichés instantanés de valeurs.</span><span class="sxs-lookup"><span data-stu-id="34034-144">This cleanly organizes code without accidentally shadowing values.</span></span>

## <a name="use-classes-to-contain-values-that-have-side-effects"></a><span data-ttu-id="34034-145">Utiliser les classes pour contenir des valeurs qui ont des effets secondaires</span><span class="sxs-lookup"><span data-stu-id="34034-145">Use classes to contain values that have side effects</span></span>

<span data-ttu-id="34034-146">Il existe plusieurs fois lorsque l’initialisation d’une valeur peut avoir des effets secondaires, tels que l’instanciation d’un contexte pour une base de données ou d’autres ressources à distance.</span><span class="sxs-lookup"><span data-stu-id="34034-146">There are many times when initializing a value can have side effects, such as instantiating a context to a database or other remote resource.</span></span> <span data-ttu-id="34034-147">Il est tentant d’initialiser des éléments dans un module et l’utiliser dans les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="34034-147">It is tempting to initialize such things in a module and use it in subsequent functions:</span></span>

```fsharp
// This is bad!
module MyApi =
    let dep1 = File.ReadAllText "/Users/{your name}/connectionstring.txt"
    let dep2 = Environment.GetEnvironmentVariable "DEP_2"

    let private r = Random()
    let dep3() = r.Next() // Problematic if multiple threads use this

    let function1 arg = doStuffWith dep1 dep2 dep3 arg
    let function2 arg = doSutffWith dep1 dep2 dep3 arg
```

<span data-ttu-id="34034-148">Il s’agit généralement déconseillé pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="34034-148">This is frequently a bad idea for a few reasons:</span></span>

<span data-ttu-id="34034-149">Tout d’abord, configuration de l’application est placée dans le code de base avec `dep1` et `dep2`.</span><span class="sxs-lookup"><span data-stu-id="34034-149">First, application configuration is pushed into the codebase with `dep1` and `dep2`.</span></span> <span data-ttu-id="34034-150">Il est difficile à maintenir dans codebases supérieure.</span><span class="sxs-lookup"><span data-stu-id="34034-150">This is difficult to maintain in larger codebases.</span></span>

<span data-ttu-id="34034-151">Ensuite, initialisées de manière statique des données ne doivent pas inclure de valeurs qui ne sont pas thread-safe si votre composant lui-même utilise plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="34034-151">Second, statically initialized data should not include values that are not thread safe if your component will itself use multiple threads.</span></span> <span data-ttu-id="34034-152">Cela est enfreinte clairement par `dep3`.</span><span class="sxs-lookup"><span data-stu-id="34034-152">This is clearly violated by `dep3`.</span></span>

<span data-ttu-id="34034-153">Enfin, l’initialisation du module compile dans un constructeur statique pour l’unité de compilation entier.</span><span class="sxs-lookup"><span data-stu-id="34034-153">Finally, module initialization compiles into a static constructor for the entire compilation unit.</span></span> <span data-ttu-id="34034-154">Si une erreur se produit dans l’initialisation de valeurs de liées à let dans ce module, il se manifeste sous un `TypeInitializationException` qui est ensuite mis en cache pour toute la durée de vie de l’application.</span><span class="sxs-lookup"><span data-stu-id="34034-154">If any error occurs in let-bound value initialization in that module, it manifests as a `TypeInitializationException` that is then cached for the entire lifetime of the application.</span></span> <span data-ttu-id="34034-155">Cela peut être difficile à diagnostiquer.</span><span class="sxs-lookup"><span data-stu-id="34034-155">This can be difficult to diagnose.</span></span> <span data-ttu-id="34034-156">Il existe généralement une exception interne que vous pouvez essayer d’analyser, mais s’il n’est pas, il n’existe aucun indiquant la cause racine.</span><span class="sxs-lookup"><span data-stu-id="34034-156">There is usually an inner exception that you can attempt to reason about, but if there is not, then there is no telling what the root cause is.</span></span>

<span data-ttu-id="34034-157">Juste utiliser à la place, une classe simple pour contenir les dépendances :</span><span class="sxs-lookup"><span data-stu-id="34034-157">Instead, just use a simple class to hold dependencies:</span></span>

```fsharp
type MyParametricApi(dep1, dep2, dep3) =
    member __.Function1 arg1 = doStuffWith dep1 dep2 dep3 arg1
    member __.Function2 arg2 = doStuffWith dep1 dep2 dep3 arg2
```

<span data-ttu-id="34034-158">Cela permet les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="34034-158">This enables the following:</span></span>

1. <span data-ttu-id="34034-159">En exécutant un push de n’importe quel état dépendant en dehors de l’API elle-même.</span><span class="sxs-lookup"><span data-stu-id="34034-159">Pushing any dependent state outside of the API itself.</span></span>
2. <span data-ttu-id="34034-160">Configuration peut maintenant être effectuée en dehors de l’API.</span><span class="sxs-lookup"><span data-stu-id="34034-160">Configuration can now be done outside of the API.</span></span>
3. <span data-ttu-id="34034-161">Erreurs dans l’initialisation de valeurs dépendantes ne sont pas susceptibles de se manifester par un `TypeInitializationException`.</span><span class="sxs-lookup"><span data-stu-id="34034-161">Errors in initialization for dependent values are not likely to manifest as a `TypeInitializationException`.</span></span>
4. <span data-ttu-id="34034-162">L’API est désormais plus facile à tester.</span><span class="sxs-lookup"><span data-stu-id="34034-162">The API is now easier to test.</span></span>

## <a name="error-management"></a><span data-ttu-id="34034-163">Gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="34034-163">Error management</span></span>

<span data-ttu-id="34034-164">Gestion des erreurs dans les grands systèmes est un défi subtils et complexe, et il n’existe aucune silver puces vous être assuré de vos systèmes à tolérance de pannes et se comportent correctement.</span><span class="sxs-lookup"><span data-stu-id="34034-164">Error management in large systems is a complex and nuanced endeavor, and there are no silver bullets in ensuring your systems are fault-tolerant and behave well.</span></span> <span data-ttu-id="34034-165">Les instructions suivantes doivent proposer une aide pour la navigation dans cet espace difficile.</span><span class="sxs-lookup"><span data-stu-id="34034-165">The following guidelines should offer guidance in navigating this difficult space.</span></span>

### <a name="represent-error-cases-and-illegal-state-in-types-intrinsic-to-your-domain"></a><span data-ttu-id="34034-166">Représentent les cas d’erreur et d’état non conforme dans les types intrinsèques à votre domaine</span><span class="sxs-lookup"><span data-stu-id="34034-166">Represent error cases and illegal state in types intrinsic to your domain</span></span>

<span data-ttu-id="34034-167">Avec [les Unions discriminées](../language-reference/discriminated-unions.md), F # vous donne la possibilité pour représenter l’état du programme défectueux dans votre système de type.</span><span class="sxs-lookup"><span data-stu-id="34034-167">With [Discriminated Unions](../language-reference/discriminated-unions.md), F# gives you the ability to represent faulty program state in your type system.</span></span> <span data-ttu-id="34034-168">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="34034-168">For example:</span></span>

```fsharp
type MoneyWithdrawalResult =
    | Success of amount:decimal
    | InsufficientFunds of balance:decimal
    | CardExpired of DateTime
    | UndisclosedFailure
```

<span data-ttu-id="34034-169">Dans ce cas, il existe des manières connus retrait de l’argent d’un compte bancaire peut échouer.</span><span class="sxs-lookup"><span data-stu-id="34034-169">In this case, there are three known ways that withdrawing money from a bank account can fail.</span></span> <span data-ttu-id="34034-170">Chaque cas d’erreur est représenté dans le type et peuvent donc être traitées en toute sécurité l’ensemble du programme.</span><span class="sxs-lookup"><span data-stu-id="34034-170">Each error case is represented in the type, and can thus be dealt with safely throughout the program.</span></span>

```fsharp
let handleWithdrawal amount =
    let w = withdrawMoney amount
    match w with
    | Success am -> printfn "Successfully withdrew %f" am
    | InsufficientFunds balance -> printfn "Failed: balance is %f" balance
    | CardExpired expiredDate -> printfn "Failed: card expired on %O" expiredDate
    | UndisclosedFailure -> printfn "Failed: unknown"
```

<span data-ttu-id="34034-171">En règle générale, si vous pouvez modéliser les différentes façons dont il se pouvez **échouer** dans votre domaine, puis gestion du code d’erreur n’est plus traité en tant que quelque chose que vous devez gérer avec en plus des flux de programme régulière.</span><span class="sxs-lookup"><span data-stu-id="34034-171">In general, if you can model the different ways that something can **fail** in your domain, then error handling code is no longer treated as something you must deal with in addition to regular program flow.</span></span> <span data-ttu-id="34034-172">Il est simplement une partie du flux normal du programme et pas considéré comme **exceptionnelles**.</span><span class="sxs-lookup"><span data-stu-id="34034-172">It is simply a part of normal program flow, and not considered **exceptional**.</span></span> <span data-ttu-id="34034-173">Il existe deux grands avantages à cela :</span><span class="sxs-lookup"><span data-stu-id="34034-173">There are two primary benefits to this:</span></span>

1. <span data-ttu-id="34034-174">Il est plus facile à gérer votre domaine que les modifications apportées au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="34034-174">It is easier to maintain as your domain changes over time.</span></span>
2. <span data-ttu-id="34034-175">Cas d’erreur sont plus faciles à des tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="34034-175">Error cases are easier to unit test.</span></span>

### <a name="use-exceptions-when-errors-cannot-be-represented-with-types"></a><span data-ttu-id="34034-176">Utiliser des exceptions lorsque les erreurs ne peut pas être représentés avec les types</span><span class="sxs-lookup"><span data-stu-id="34034-176">Use exceptions when errors cannot be represented with types</span></span>

<span data-ttu-id="34034-177">Toutes les erreurs peuvent être représentés dans un domaine de problème.</span><span class="sxs-lookup"><span data-stu-id="34034-177">Not all errors can be represented in a problem domain.</span></span> <span data-ttu-id="34034-178">Ces types d’erreurs sont *exceptionnelles* par nature, donc la possibilité de déclencher et intercepter les exceptions en F #.</span><span class="sxs-lookup"><span data-stu-id="34034-178">These kinds of faults are *exceptional* in nature, hence the ability to raise and catch exceptions in F#.</span></span>

<span data-ttu-id="34034-179">Tout d’abord, il est recommandé de lire le [les règles de conception Exception](../../standard/design-guidelines/exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="34034-179">First, it is recommended that you read the [Exception Design Guidelines](../../standard/design-guidelines/exceptions.md).</span></span> <span data-ttu-id="34034-180">Ceux-ci sont également applicables à F #.</span><span class="sxs-lookup"><span data-stu-id="34034-180">These are also applicable to F#.</span></span>

<span data-ttu-id="34034-181">Les constructions principales disponibles en F # pour les besoins de déclenchement d’exceptions doivent être considérées dans l’ordre de préférence suivant :</span><span class="sxs-lookup"><span data-stu-id="34034-181">The main constructs available in F# for the purposes of raising exceptions should be considered in the following order of preference:</span></span>

| <span data-ttu-id="34034-182">Fonction</span><span class="sxs-lookup"><span data-stu-id="34034-182">Function</span></span> | <span data-ttu-id="34034-183">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34034-183">Syntax</span></span> | <span data-ttu-id="34034-184">Objectif</span><span class="sxs-lookup"><span data-stu-id="34034-184">Purpose</span></span> |
|----------|--------|---------|
| `nullArg` | `nullArg "argumentName"` | <span data-ttu-id="34034-185">Déclenche un `System.ArgumentNullException` avec le nom de l’argument spécifié.</span><span class="sxs-lookup"><span data-stu-id="34034-185">Raises a `System.ArgumentNullException` with the specified argument name.</span></span> |
| `invalidArg` | `invalidArg "argumentName" "message"` | <span data-ttu-id="34034-186">Déclenche un `System.ArgumentException` avec un nom d’argument spécifié et le message.</span><span class="sxs-lookup"><span data-stu-id="34034-186">Raises a `System.ArgumentException` with a specified argument name and message.</span></span> |
| `invalidOp` | `invalidOp "message"` | <span data-ttu-id="34034-187">Déclenche un `System.InvalidOperationException` avec le message spécifié.</span><span class="sxs-lookup"><span data-stu-id="34034-187">Raises a `System.InvalidOperationException` with the specified message.</span></span> |
|`raise`| `raise (ExceptionType("message"))` | <span data-ttu-id="34034-188">Mécanisme à usage général pour lever des exceptions.</span><span class="sxs-lookup"><span data-stu-id="34034-188">General-purpose mechanism for throwing exceptions.</span></span> |
| `failwith` | `failwith "message"` | <span data-ttu-id="34034-189">Déclenche un `System.Exception` avec le message spécifié.</span><span class="sxs-lookup"><span data-stu-id="34034-189">Raises a `System.Exception` with the specified message.</span></span> |
| `failwithf` | `failwithf "format string" argForFormatString` | <span data-ttu-id="34034-190">Déclenche un `System.Exception` avec un message déterminé par la chaîne de format et de ses entrées.</span><span class="sxs-lookup"><span data-stu-id="34034-190">Raises a `System.Exception` with a message determined by the format string and its inputs.</span></span> |

<span data-ttu-id="34034-191">Utilisez `nullArg`, `invalidArg` et `invalidOp` comme mécanisme de lever `ArgumentNullException`, `ArgumentException` et `InvalidOperationException` quand cela est approprié.</span><span class="sxs-lookup"><span data-stu-id="34034-191">Use `nullArg`, `invalidArg` and `invalidOp` as the mechanism to throw `ArgumentNullException`, `ArgumentException` and `InvalidOperationException` when appropriate.</span></span>

<span data-ttu-id="34034-192">Le `failwith` et `failwithf` fonctions doivent être évitées en règle générale, car elles déclenchent la base de `Exception` de type, pas une exception spécifique.</span><span class="sxs-lookup"><span data-stu-id="34034-192">The `failwith` and `failwithf` functions should generally be avoided because they raise the base `Exception` type, not a specific exception.</span></span> <span data-ttu-id="34034-193">Comme pour le [règles de conception d’Exception](../../standard/design-guidelines/exceptions.md), vous souhaitez lever d’exceptions plus spécifiques dès que possible.</span><span class="sxs-lookup"><span data-stu-id="34034-193">As per the [Exception Design Guidelines](../../standard/design-guidelines/exceptions.md), you want to raise more specific exceptions when you can.</span></span>

### <a name="using-exception-handling-syntax"></a><span data-ttu-id="34034-194">À l’aide de la syntaxe de gestion des exceptions</span><span class="sxs-lookup"><span data-stu-id="34034-194">Using exception-handling syntax</span></span>

<span data-ttu-id="34034-195">F # prend en charge les modèles d’exception via la `try...with` syntaxe :</span><span class="sxs-lookup"><span data-stu-id="34034-195">F# supports exception patterns via the `try...with` syntax:</span></span>

```fsharp
try
    tryGetFileContents()
with
| :? System.IO.FileNotFoundException as e -> // Do something with it here
| :? System.Security.SecurityException as e -> // Do something with it here
```

<span data-ttu-id="34034-196">Rapprochement des fonctionnalités à effectuer en cas d’une exception avec les critères spéciaux peut être un peu difficile si vous souhaitez conserver le code de nettoyage.</span><span class="sxs-lookup"><span data-stu-id="34034-196">Reconciling functionality to perform in the face of an exception with pattern matching can be a bit tricky if you wish to keep the code clean.</span></span> <span data-ttu-id="34034-197">Une telle pour gérer cette situation consiste à utiliser [modèles actifs](../language-reference/active-patterns.md) comme un moyen de la fonctionnalité de groupe se rapportant à un cas d’erreur avec une exception lui-même.</span><span class="sxs-lookup"><span data-stu-id="34034-197">One such way to handle this is to use [active patterns](../language-reference/active-patterns.md) as a means to group functionality surrounding an error case with an exception itself.</span></span> <span data-ttu-id="34034-198">Par exemple, vous pouvez consommer une API qui, lorsqu’il lève une exception, inclut des informations précieuses dans les métadonnées d’exception.</span><span class="sxs-lookup"><span data-stu-id="34034-198">For example, you may be consuming an API that, when it throws an exception, encloses valuable information in the exception metadata.</span></span> <span data-ttu-id="34034-199">Désencapsulage d’une valeur utile dans le corps de l’exception capturée à l’intérieur du modèle actif et en retournant que la valeur peut être utile dans certaines situations.</span><span class="sxs-lookup"><span data-stu-id="34034-199">Unwrapping a useful value in the body of the captured exception inside the Active Pattern and returning that value can be helpful in some situations.</span></span>

### <a name="do-not-use-monadic-error-handling-to-replace-exceptions"></a><span data-ttu-id="34034-200">N’utilisez pas monadic gestion des erreurs pour remplacer des exceptions</span><span class="sxs-lookup"><span data-stu-id="34034-200">Do not use monadic error handling to replace exceptions</span></span>

<span data-ttu-id="34034-201">Les exceptions sont considérées comme quelque peu interdits dans la programmation fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="34034-201">Exceptions are seen as somewhat taboo in functional programming.</span></span> <span data-ttu-id="34034-202">En effet, les exceptions violent pureté, afin de prendre en compte fonctionnel non-tout à fait en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="34034-202">Indeed, exceptions violate purity, so it's safe to consider them not-quite functional.</span></span> <span data-ttu-id="34034-203">Toutefois, il ignore la réalité d’où le code doit s’exécuter et ce runtime erreurs peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="34034-203">However, this ignores the reality of where code must run, and that runtime errors can occur.</span></span> <span data-ttu-id="34034-204">En règle générale, écrire du code sur l’hypothèse que la plupart des éléments sont total, afin de minimiser les surprises désagréables ni pure.</span><span class="sxs-lookup"><span data-stu-id="34034-204">In general, write code on the assumption that most things are neither pure nor total, to minimize unpleasant surprises.</span></span>

<span data-ttu-id="34034-205">Il est important de considérer les principaux atouts/aspects suivants des Exceptions en ce qui concerne leur pertinence et de pertinence dans le runtime .NET et l’écosystème de la gestion interlangage dans son ensemble :</span><span class="sxs-lookup"><span data-stu-id="34034-205">It is important to consider the following core strengths/aspects of Exceptions with respect to their relevance and appropriateness in the .NET runtime and cross-language ecosystem as a whole:</span></span>

1. <span data-ttu-id="34034-206">Elles contiennent des informations de diagnostic détaillées, ce qui est très utiles lors du débogage d’un problème.</span><span class="sxs-lookup"><span data-stu-id="34034-206">They contain detailed diagnostic information, which is very helpful when debugging an issue.</span></span>
2. <span data-ttu-id="34034-207">Ils sont bien compris par le runtime et d’autres langages .NET.</span><span class="sxs-lookup"><span data-stu-id="34034-207">They are well-understood by the runtime and other .NET languages.</span></span>
3. <span data-ttu-id="34034-208">Elles permettent une réduction significative réutilisable lors de la comparaison avec le code sort de sa méthode pour *éviter* exceptions en implémentant un sous-ensemble de leur sémantique sur une base ad hoc.</span><span class="sxs-lookup"><span data-stu-id="34034-208">They can reduce significant boilerplate when compared with code that goes out of its way to *avoid* exceptions by implementing some subset of their semantics on an ad-hoc basis.</span></span>

<span data-ttu-id="34034-209">Cet troisième point est essentiel.</span><span class="sxs-lookup"><span data-stu-id="34034-209">This third point is critical.</span></span> <span data-ttu-id="34034-210">Pour les opérations complexes non triviale, utiliser des exceptions peut limiter dans le traitement des structures, comme suit :</span><span class="sxs-lookup"><span data-stu-id="34034-210">For nontrivial complex operations, failing to use exceptions can result in dealing with structures like this:</span></span>

```fsharp
Result<Result<MyType, string>, string list>
```

<span data-ttu-id="34034-211">Ce qui peut entraîner facilement fragile code telles que les critères spéciaux sur les erreurs de « stringly typée » :</span><span class="sxs-lookup"><span data-stu-id="34034-211">Which can easily lead to fragile code like pattern matching on "stringly-typed" errors:</span></span>

```fsharp
let result = doStuff()
match result with
| Ok r -> ...
| Error e ->
    if e.Contains "Error string 1" then ...
    elif e.Contains "Error string 2" then ...
    else ... // Who knows?
```

<span data-ttu-id="34034-212">En outre, il peut être tentant d’absorber toute exception dans la volonté de disposer d’une fonction « simple » qui retourne un type « agréable » :</span><span class="sxs-lookup"><span data-stu-id="34034-212">Additionally, it can be tempting to swallow any exception in the desire for a "simple" function that returns a "nicer" type:</span></span>

```fsharp
// This is bad!
let tryReadAllText (path : string) =
    try System.IO.File.ReadAllText path |> Some
    with _ -> None
```

<span data-ttu-id="34034-213">Malheureusement, `tryReadAllText` peut lever des exceptions de nombreuses en fonction de la multitude d’éléments peuvent se produire sur un système de fichiers, et ce code annule immédiatement toutes les informations concernant ce qui peut en fait être va pas dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="34034-213">Unfortunately, `tryReadAllText` can throw numerous exceptions based on the myriad of things that can happen on a file system, and this code discards away any information about what might actually be going wrong in your environment.</span></span> <span data-ttu-id="34034-214">Si vous remplacez ce code avec un type de résultat, vous êtes à l’analyse « stringly typée » une erreur :</span><span class="sxs-lookup"><span data-stu-id="34034-214">If you replace this code with a result type, then you're back to "stringly-typed" error message parsing:</span></span>

```fsharp
// This is bad!
let tryReadAllText (path : string) =
    try System.IO.File.ReadAllText path |> Ok
    with e -> Error e.Message

let r = tryReadAllText "path-to-file"
match r with
| Ok text -> ...
| Error e ->
    if e.Contains "uh oh, here we go again..." then ...
    else ...
```

<span data-ttu-id="34034-215">Et en plaçant l’objet exception lui-même dans le `Error` constructeur simplement vous oblige à gérer correctement le type d’exception sur le site d’appel, plutôt que dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="34034-215">And placing the exception object itself in the `Error` constructor just forces you to properly deal with the exception type at the call site rather than in the function.</span></span> <span data-ttu-id="34034-216">Cette opération efficacement crée les exceptions vérifiées, qui sont notoirement unfun à traiter comme un appelant d’une API.</span><span class="sxs-lookup"><span data-stu-id="34034-216">Doing this effectively creates checked exceptions, which are notoriously unfun to deal with as a caller of an API.</span></span>

<span data-ttu-id="34034-217">Une bonne approche pour les exemples ci-dessus est d’intercepter *spécifique* exceptions et retournent une valeur significative dans le contexte de cette exception.</span><span class="sxs-lookup"><span data-stu-id="34034-217">A good alternative to the above examples is to catch *specific* exceptions and return a meaningful value in the context of that exception.</span></span> <span data-ttu-id="34034-218">Si vous modifiez le `tryReadAllText` fonctionnent comme suit, `None` a plus de sens :</span><span class="sxs-lookup"><span data-stu-id="34034-218">If you modify the `tryReadAllText` function as follows, `None` has more meaning:</span></span>

```fsharp
let tryReadAllTextIfPresent (path : string) =
    try System.IO.File.ReadAllText path |> Some
    with :? FileNotFoundException -> None
```

<span data-ttu-id="34034-219">Au lieu de fonctionner comme un tout, cette fonction maintenant correctement gère le cas lorsqu’un fichier n’a été trouvé et affecter ce sens à un retour.</span><span class="sxs-lookup"><span data-stu-id="34034-219">Instead of functioning as a catch-all, this function will now properly handle the case when a file was not found and assign that meaning to a return.</span></span> <span data-ttu-id="34034-220">Cette valeur de retour peut mapper à ce cas d’erreur lors de pas en ignorant toutes les informations contextuelles ou forcer des appelants pour y faire face à un incident ne peut pas s’appliquer à ce stade dans le code.</span><span class="sxs-lookup"><span data-stu-id="34034-220">This return value can map to that error case, while not discarding any contextual information or forcing callers to deal with a case that may not be relevant at that point in the code.</span></span>

<span data-ttu-id="34034-221">Types tels que `Result<'Success, 'Error>` appropriées pour les opérations de base où ils ne sont pas imbriqués, et facultatif types F # sont parfaites pour représenter lorsqu’un élément a un retour *quelque chose* ou *rien*.</span><span class="sxs-lookup"><span data-stu-id="34034-221">Types such as `Result<'Success, 'Error>` are appropriate for basic operations where they aren't nested, and F# optional types are perfect for representing when something could either return *something* or *nothing*.</span></span> <span data-ttu-id="34034-222">Ils ne sont pas un remplacement pour les exceptions, cependant et ne doivent pas servir lors d’une tentative pour remplacer les exceptions.</span><span class="sxs-lookup"><span data-stu-id="34034-222">They are not a replacement for exceptions, though, and should not be used in an attempt to replace exceptions.</span></span> <span data-ttu-id="34034-223">Au lieu de cela, ils doivent être appliqués judicieusement à des aspects spécifiques d’adresse de l’exception et la stratégie de gestion des erreurs de façons ciblé.</span><span class="sxs-lookup"><span data-stu-id="34034-223">Rather, they should be applied judiciously to address specific aspects of exception and error management policy in targeted ways.</span></span>

## <a name="partial-application-and-point-free-programming"></a><span data-ttu-id="34034-224">Application partielle et exempt de point de programmation</span><span class="sxs-lookup"><span data-stu-id="34034-224">Partial application and point-free programming</span></span>

<span data-ttu-id="34034-225">F # prend en charge application partielle et par conséquent, différentes façons de programme dans un style exempt de point.</span><span class="sxs-lookup"><span data-stu-id="34034-225">F# supports partial application, and thus, various ways to program in a point-free style.</span></span> <span data-ttu-id="34034-226">Ceci peut être avantageux de réutilisation du code dans un module ou l’implémentation d’un objet, mais il n’est généralement pas quelque chose pour exposer publiquement.</span><span class="sxs-lookup"><span data-stu-id="34034-226">This can be beneficial for code reuse within a module or the implementation of something, but it is generally not something to expose publicly.</span></span> <span data-ttu-id="34034-227">En général, exempt de point de programmation n’est pas une raison dans et de lui-même et peut ajouter un frein COGNITIF pour les personnes qui ne sont pas immergés dans le style.</span><span class="sxs-lookup"><span data-stu-id="34034-227">In general, point-free programming is not a virtue in and of itself, and can add a significant cognitive barrier for people who are not immersed in the style.</span></span>

### <a name="do-not-use-partial-application-and-currying-in-public-apis"></a><span data-ttu-id="34034-228">N’utilisez pas l’application partielle et curryfication dans les API publiques</span><span class="sxs-lookup"><span data-stu-id="34034-228">Do not use partial application and currying in public APIs</span></span>

<span data-ttu-id="34034-229">Avec peu d’exception, l’utilisation de l’application partielle dans les API publiques permettre prêter à confusion pour les consommateurs.</span><span class="sxs-lookup"><span data-stu-id="34034-229">With little exception, the use of partial application in public APIs can be confusing for consumers.</span></span> <span data-ttu-id="34034-230">En règle générale, `let`-valeurs liées dans le code F # sont **valeurs**, et non **des valeurs de fonction**.</span><span class="sxs-lookup"><span data-stu-id="34034-230">Usually, `let`-bound values in F# code are **values**, not **function values**.</span></span> <span data-ttu-id="34034-231">Mélange de valeurs et les valeurs de fonction peut entraîner l’enregistrement d’un petit nombre de lignes de code en échange d’un peu de surcharge COGNITIF, surtout si combinées avec des opérateurs tels que `>>` pour composer des fonctions.</span><span class="sxs-lookup"><span data-stu-id="34034-231">Mixing together values and function values can result in saving a small number of lines of code in exchange for quite a bit of cognitive overhead, especially if combined with operators such as `>>` to compose functions.</span></span>

### <a name="consider-the-tooling-implications-for-point-free-programming"></a><span data-ttu-id="34034-232">Tenez compte des conséquences des outils pour la programmation de libérer de point</span><span class="sxs-lookup"><span data-stu-id="34034-232">Consider the tooling implications for point-free programming</span></span>

<span data-ttu-id="34034-233">Fonctions curryfiées étiquette pas leurs arguments.</span><span class="sxs-lookup"><span data-stu-id="34034-233">Curried functions do not label their arguments.</span></span> <span data-ttu-id="34034-234">Cela a des implications des outils.</span><span class="sxs-lookup"><span data-stu-id="34034-234">This has tooling implications.</span></span> <span data-ttu-id="34034-235">Prenez en compte les deux fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="34034-235">Consider the following two functions:</span></span>

```fsharp
let func name age =
    printfn "My name is %s and I am %d years old!" name age

let funcWithApplication =
    printfn "My name is %s and I am %d years old!"
```

<span data-ttu-id="34034-236">Les deux sont des fonctions valides, mais `funcWithApplication` est une fonction curryfiée.</span><span class="sxs-lookup"><span data-stu-id="34034-236">Both are valid functions, but `funcWithApplication` is a curried function.</span></span> <span data-ttu-id="34034-237">Lorsque vous pointez sur leurs types dans un éditeur, vous voyez ceci :</span><span class="sxs-lookup"><span data-stu-id="34034-237">When you hover over their types in an editor, you see this:</span></span>

```fsharp
val func : name:string -> age:int -> unit

val funcWithApplication : (string -> int -> unit)
```

<span data-ttu-id="34034-238">Sur le site d’appel, les info-bulles dans des outils tels que Visual Studio ne vous donnera des informations significatives à ce que le `string` et `int` représentent les types d’entrée.</span><span class="sxs-lookup"><span data-stu-id="34034-238">At the call site, tooltips in tooling such as Visual Studio will not give you meaningful information as to what the `string` and `int` input types actually represent.</span></span>

<span data-ttu-id="34034-239">Si vous rencontrez exempt de point de code comme `funcWithApplication` qui est consommable publiquement, il est recommandé de procéder à une expansion de η complète pour que les outils peuvent réponde à des noms explicites pour les arguments.</span><span class="sxs-lookup"><span data-stu-id="34034-239">If you encounter point-free code like `funcWithApplication` that is publicly consumable, it is recommended to do a full η-expansion so that tooling can pick up on meaningful names for arguments.</span></span>

<span data-ttu-id="34034-240">En outre, le débogage du code sans aucun point de peut être difficile, voire impossible.</span><span class="sxs-lookup"><span data-stu-id="34034-240">Furthermore, debugging point-free code can be challenging, if not impossible.</span></span> <span data-ttu-id="34034-241">Outils de débogage s’appuient sur les valeurs liées aux noms (par exemple, `let` liaisons) afin que vous pouvez inspecter l’exécution au milieu de valeurs intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="34034-241">Debugging tools rely on values bound to names (for example, `let` bindings) so that you can inspect intermediate values midway through execution.</span></span> <span data-ttu-id="34034-242">Lorsque votre code n’a aucune valeur à inspecter, il n’est rien à déboguer.</span><span class="sxs-lookup"><span data-stu-id="34034-242">When your code has no values to inspect, there is nothing to debug.</span></span> <span data-ttu-id="34034-243">Dans le futur, outils de débogage peut évoluer pour synthétiser ces valeurs basées sur les chemins d’accès précédemment exécutées, mais il n’est pas judicieux de couvrir vos meilleurs résultats sur *potentiels* fonctionnalités de débogage.</span><span class="sxs-lookup"><span data-stu-id="34034-243">In the future, debugging tools may evolve to synthesize these values based on previously executed paths, but it's not a good idea to hedge your bets on *potential* debugging functionality.</span></span>

### <a name="consider-partial-application-as-a-technique-to-reduce-internal-boilerplate"></a><span data-ttu-id="34034-244">Considérez une application partielle comme une technique afin de réduire le code réutilisable interne</span><span class="sxs-lookup"><span data-stu-id="34034-244">Consider partial application as a technique to reduce internal boilerplate</span></span>

<span data-ttu-id="34034-245">Contrairement au point précédent, application partielle est un outil merveilleux pour réduire le code réutilisable à l’intérieur d’une application ou les détails plus approfondis internes d’une API.</span><span class="sxs-lookup"><span data-stu-id="34034-245">In contrast to the previous point, partial application is a wonderful tool for reducing boilerplate inside of an application or the deeper internals of an API.</span></span> <span data-ttu-id="34034-246">Il peut être utile pour l’implémentation des API plus complexe, où réutilisable est souvent difficiles à gérer de tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="34034-246">It can be helpful for unit testing the implementation of more complicated APIs, where boilerplate is often a pain to deal with.</span></span> <span data-ttu-id="34034-247">Par exemple, le code suivant montre comment vous pouvez accomplir les infrastructures plus factices affichent sans prendre une dépendance externe sur une telle infrastructure et avoir à apprendre un connexes ad hoc API.</span><span class="sxs-lookup"><span data-stu-id="34034-247">For example, the following code shows how you can accomplish what most mocking frameworks give you without taking an external dependency on such a framework and having to learn a related bespoke API.</span></span>

<span data-ttu-id="34034-248">Par exemple, considérez la topographie de solution suivants :</span><span class="sxs-lookup"><span data-stu-id="34034-248">For example, consider the following solution topography:</span></span>

```
MySolution.sln
|_/ImplementationLogic.fsproj
|_/ImplementationLogic.Tests.fsproj
|_/API.fsproj
```

<span data-ttu-id="34034-249">`ImplementationLogic.fsproj` peut exposer du code tel que :</span><span class="sxs-lookup"><span data-stu-id="34034-249">`ImplementationLogic.fsproj` might expose code such as:</span></span>

```fsharp
module Transactions =
    let doTransaction txnContext txnType balance =
        ...

type Transactor(ctx, currentBalance) =
    member __.ExecuteTransaction(txnType) =
        Transactions.doTransaction ctx txtType currentBalance
        ...
```

<span data-ttu-id="34034-250">Tests unitaires `Transactions.doTransaction` dans `ImplementationLogic.Tests.fspoj` est simple :</span><span class="sxs-lookup"><span data-stu-id="34034-250">Unit testing `Transactions.doTransaction` in `ImplementationLogic.Tests.fspoj` is easy:</span></span>

```fsharp
namespace TransactionsTestingUtil

open Transactions

module TransactionsTestable =
    let getTestableTransactionRoutine mockContext = Transactions.doTransaction mockContext
```

<span data-ttu-id="34034-251">Application partiellement `doTransaction` avec un contexte factices objet vous permet d’appeler la fonction dans tous vos tests unitaires sans avoir à construire un contexte factices chaque fois :</span><span class="sxs-lookup"><span data-stu-id="34034-251">Partially applying `doTransaction` with a mocking context object lets you call the function in all of your unit tests without needing to construct a mocked context each time:</span></span>

```fsharp
namespace TransactionTests

open Xunit
open TransactionTypes
open TransactionsTestingUtil
open TransactionsTestingUtil.TransactionsTestable

let testableContext =
    { new ITransactionContext with
        member __.TheFirstMember() = ...
        member __.TheSecondMember() = ... }

let transactionRoutine = getTestableTransactionRoutine testableContext

[<Fact>]
let ``Test withdrawal transaction with 0.0 for balance``() =
    let expected = ...
    let actual = transactionRoutine TransactionType.Withdraw 0.0
    Assert.Equal(expected, actual)
```

<span data-ttu-id="34034-252">Cette technique ne doit pas être appliquée globalement à votre code base entière, mais il s’agit d’un bon moyen de réduire le code réutilisable pour développer des mécanismes complexes et les mécanismes internes de tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="34034-252">This technique should not be universally applied to your entire codebase, but it is a good way to reduce boilerplate for complicated internals and unit testing those internals.</span></span>

## <a name="access-control"></a><span data-ttu-id="34034-253">Contrôle d'accès</span><span class="sxs-lookup"><span data-stu-id="34034-253">Access control</span></span>

<span data-ttu-id="34034-254">F # dispose de plusieurs options pour [le contrôle d’accès](../language-reference/access-control.md), hérité de ce qui est disponible dans le runtime .NET.</span><span class="sxs-lookup"><span data-stu-id="34034-254">F# has multiple options for [Access control](../language-reference/access-control.md), inherited from what is available in the .NET runtime.</span></span> <span data-ttu-id="34034-255">Celles-ci ne sont pas utilisables uniquement pour les types - vous pouvez les utiliser pour les fonctions de trop.</span><span class="sxs-lookup"><span data-stu-id="34034-255">These are not just usable for types - you can use them for functions, too.</span></span>

* <span data-ttu-id="34034-256">Préférez non -`public` types et membres jusqu'à ce que vous avez besoin pour être utilisable publiquement.</span><span class="sxs-lookup"><span data-stu-id="34034-256">Prefer non-`public` types and members until you need them to be publicly consumable.</span></span> <span data-ttu-id="34034-257">Cela réduit également les deux consommateurs à</span><span class="sxs-lookup"><span data-stu-id="34034-257">This also minimizes what consumers couple to</span></span>
* <span data-ttu-id="34034-258">Essayez de conserver toutes les fonctionnalités d’assistance `private`.</span><span class="sxs-lookup"><span data-stu-id="34034-258">Strive to keep all helper functionality `private`.</span></span>
* <span data-ttu-id="34034-259">Envisagez d’utiliser `[<AutoOpen>]` sur un module privé de fonctions d’assistance s’ils sont nombreux.</span><span class="sxs-lookup"><span data-stu-id="34034-259">Consider the use of `[<AutoOpen>]` on a private module of helper functions if they become numerous.</span></span>

## <a name="type-inference-and-generics"></a><span data-ttu-id="34034-260">L’inférence de type et les génériques</span><span class="sxs-lookup"><span data-stu-id="34034-260">Type inference and generics</span></span>

<span data-ttu-id="34034-261">L’inférence de type peut vous permettre d’économiser de la saisie d’une grande quantité de code réutilisable.</span><span class="sxs-lookup"><span data-stu-id="34034-261">Type inference can save you from typing a lot of boilerplate.</span></span> <span data-ttu-id="34034-262">Et généralisation automatique dans le compilateur F # peut vous aider à écrire plus de code générique avec quasiment aucun effort supplémentaire de votre part.</span><span class="sxs-lookup"><span data-stu-id="34034-262">And automatic generalization in the F# compiler can help you write more generic code with almost no extra effort on your part.</span></span> <span data-ttu-id="34034-263">Toutefois, ces fonctionnalités ne sont pas universellement correcte.</span><span class="sxs-lookup"><span data-stu-id="34034-263">However, these features are not universally good.</span></span>

* <span data-ttu-id="34034-264">Envisagez d’étiqueter les noms des arguments avec des types explicites dans les API publiques et n’utilisez pas l’inférence de type pour cela.</span><span class="sxs-lookup"><span data-stu-id="34034-264">Consider labeling argument names with explicit types in public APIs and do not rely on type inference for this.</span></span>

    <span data-ttu-id="34034-265">La raison en est que **vous** doit se trouver dans le contrôle de la forme de votre API, et non par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="34034-265">The reason for this is that **you** should be in control of the shape of your API, not the compiler.</span></span> <span data-ttu-id="34034-266">Bien que le compilateur peut effectuer une tâche convient à déduire les types pour vous, il est possible d’avoir la forme de la modification de l’API si elle s’appuie sur les éléments internes ont été modifiés de types.</span><span class="sxs-lookup"><span data-stu-id="34034-266">Although the compiler can do a fine job at inferring types for you, it is possible to have the shape of your API change if the internals it relies on have changed types.</span></span> <span data-ttu-id="34034-267">Il peut s’agir de ce que vous souhaitez, mais certainement causera une modification avec rupture API qui ont pour traiter les consommateurs en aval.</span><span class="sxs-lookup"><span data-stu-id="34034-267">This may be what you want, but it will almost certainly result in a breaking API change that downstream consumers will then have to deal with.</span></span> <span data-ttu-id="34034-268">En revanche, si vous ne contrôliez explicitement la forme de votre API publique, vous pouvez contrôler ces modifications avec rupture.</span><span class="sxs-lookup"><span data-stu-id="34034-268">Instead, if you explicitly control the shape of your public API, then you can control these breaking changes.</span></span> <span data-ttu-id="34034-269">En termes DDD, cela peut être représenté comme une couche de lutte contre la corruption.</span><span class="sxs-lookup"><span data-stu-id="34034-269">In DDD terms, this can be thought of as an Anti-corruption layer.</span></span>

* <span data-ttu-id="34034-270">Donnez un nom significatif à vos arguments génériques.</span><span class="sxs-lookup"><span data-stu-id="34034-270">Consider giving a meaningful name to your generic arguments.</span></span>

    <span data-ttu-id="34034-271">Sauf si vous écrivez du code réellement générique qui n’est pas spécifique à un domaine particulier, un nom significatif peut aider d’autres programmeurs comprendre le domaine, dans qu'ils travaillent.</span><span class="sxs-lookup"><span data-stu-id="34034-271">Unless you are writing truly generic code that is not specific to a particular domain, a meaningful name can help other programmers understanding the domain they're working in.</span></span> <span data-ttu-id="34034-272">Par exemple, un paramètre de type nommé `'Document` dans le contexte de l’interaction avec un document de base de données plus clairement que les types de document générique peuvent être acceptées par la fonction ou le membre que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="34034-272">For example, a type parameter named `'Document` in the context of interacting with a document database makes it clearer that generic document types can be accepted by the function or member you are working with.</span></span>

* <span data-ttu-id="34034-273">Envisagez de nommer les paramètres de type générique avec PascalCase.</span><span class="sxs-lookup"><span data-stu-id="34034-273">Consider naming generic type parameters with PascalCase.</span></span>

    <span data-ttu-id="34034-274">Il s’agit de la manière générale pour effectuer des opérations dans .NET, il est recommandé d’utiliser PascalCase plutôt que snake_case ou camelCase.</span><span class="sxs-lookup"><span data-stu-id="34034-274">This is the general way to do things in .NET, so it's recommended that you use PascalCase rather than snake_case or camelCase.</span></span>

<span data-ttu-id="34034-275">Enfin, la généralisation automatique n’est pas toujours un boon pour les personnes qui sont nouveaux pour F # ou un code base volumineux.</span><span class="sxs-lookup"><span data-stu-id="34034-275">Finally, automatic generalization is not always a boon for people who are new to F# or a large codebase.</span></span> <span data-ttu-id="34034-276">Charge COGNITIF est à l’aide des composants qui sont génériques.</span><span class="sxs-lookup"><span data-stu-id="34034-276">There is cognitive overhead in using components that are generic.</span></span> <span data-ttu-id="34034-277">En outre, si automatiquement généralisée de fonctions ne sont pas utilisées avec différents types d’entrée (permettent uniquement s’ils sont destinés à être utilisé en tant que tel), il n’existe aucun avantage réel pour les cours générique à ce stade dans le temps.</span><span class="sxs-lookup"><span data-stu-id="34034-277">Furthermore, if automatically generalized functions are not used with different input types (let alone if they are intended to be used as such), then there is no real benefit to them being generic at that point in time.</span></span> <span data-ttu-id="34034-278">Toujours prendre en compte si le code que vous écrivez bénéficieront réellement d’être générique.</span><span class="sxs-lookup"><span data-stu-id="34034-278">Always consider if the code you are writing will actually benefit from being generic.</span></span>

## <a name="performance"></a><span data-ttu-id="34034-279">Performances</span><span class="sxs-lookup"><span data-stu-id="34034-279">Performance</span></span>

<span data-ttu-id="34034-280">Valeurs de F # sont immuables par défaut, ce qui vous permet d’éviter certaines classes de bogues (en particulier les impliquant d’accès concurrentiel et parallélisme).</span><span class="sxs-lookup"><span data-stu-id="34034-280">F# values are immutable by default, which allows you to avoid certain classes of bugs (especially those involving concurrency and parallelism).</span></span> <span data-ttu-id="34034-281">Toutefois, dans certains cas, afin d’optimiser l’efficacité d’optimale (ou même raisonnable) de la durée d’exécution ou des allocations de mémoire, une plage de travail peut mieux être implémentée à l’aide de mutation sur place de l’état.</span><span class="sxs-lookup"><span data-stu-id="34034-281">However, in certain cases, in order to achieve optimal (or even reasonable) efficiency of execution time or memory allocations, a span of work may best be implemented by using in-place mutation of state.</span></span> <span data-ttu-id="34034-282">Cela est possible dans une base opt-in avec F # avec le `mutable` (mot clé).</span><span class="sxs-lookup"><span data-stu-id="34034-282">This is possible in an opt-in basis with F# with the `mutable` keyword.</span></span>

<span data-ttu-id="34034-283">Toutefois, l’utilisation du `mutable` en F # peuvent avoir l’impression ne correspond pas à la pureté fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="34034-283">However, use of `mutable` in F# may feel at odds with functional purity.</span></span> <span data-ttu-id="34034-284">Il s’agit bien, si vous ajustez les attentes de pureté [référentielle transparence](https://en.wikipedia.org/wiki/Referential_transparency).</span><span class="sxs-lookup"><span data-stu-id="34034-284">This is fine, if you adjust expectations from purity to [referential transparency](https://en.wikipedia.org/wiki/Referential_transparency).</span></span> <span data-ttu-id="34034-285">Transparence référentielle - pas à la pureté - est l’objectif final lors de l’écriture de fonctions F #.</span><span class="sxs-lookup"><span data-stu-id="34034-285">Referential transparency - not purity - is the end goal when writing F# functions.</span></span> <span data-ttu-id="34034-286">Cela vous permet d’écrire une interface fonctionnelle sur une implémentation mutation pour le code critique de performances.</span><span class="sxs-lookup"><span data-stu-id="34034-286">This allows you to write a functional interface over a mutation-based implementation for performance critical code.</span></span>

### <a name="wrap-mutable-code-in-immutable-interfaces"></a><span data-ttu-id="34034-287">Encapsuler le code mutable dans les interfaces immuables</span><span class="sxs-lookup"><span data-stu-id="34034-287">Wrap mutable code in immutable interfaces</span></span>

<span data-ttu-id="34034-288">Transparence référentielle comme objectif, il est essentiel d’écrire du code qui n’expose pas l’underbelly mutable des fonctions critiques pour les performances.</span><span class="sxs-lookup"><span data-stu-id="34034-288">With referential transparency as a goal, it is critical to write code that does not expose the mutable underbelly of performance-critical functions.</span></span> <span data-ttu-id="34034-289">Par exemple, le code suivant implémente la `Array.contains` fonction dans la bibliothèque principale F # :</span><span class="sxs-lookup"><span data-stu-id="34034-289">For example, the following code implements the `Array.contains` function in the F# core library:</span></span>

```fsharp
[<CompiledName("Contains")>]
let inline contains value (array:'T[]) =
    checkNonNull "array" array
    let mutable state = false
    let mutable i = 0
    while not state && i < array.Length do
        state <- value = array.[i]
        i <- i + 1
    state
```

<span data-ttu-id="34034-290">Appel de cette fonction plusieurs fois ne modifie pas le tableau sous-jacent, et il vous oblige à conserver un état mutable dans sa consommation.</span><span class="sxs-lookup"><span data-stu-id="34034-290">Calling this function multiple times does not change the underlying array, nor does it require you to maintain any mutable state in consuming it.</span></span> <span data-ttu-id="34034-291">Il est référentielle transparent, même si presque chaque ligne de code utilise la mutation.</span><span class="sxs-lookup"><span data-stu-id="34034-291">It is referentially transparent, even though almost every line of code within it uses mutation.</span></span>

### <a name="consider-encapsulating-mutable-data-in-classes"></a><span data-ttu-id="34034-292">Envisagez d’encapsuler des données mutables dans les classes</span><span class="sxs-lookup"><span data-stu-id="34034-292">Consider encapsulating mutable data in classes</span></span>

<span data-ttu-id="34034-293">L’exemple précédent a utilisé une seule fonction pour encapsuler des opérations à l’aide de données mutables.</span><span class="sxs-lookup"><span data-stu-id="34034-293">The previous example used a single function to encapsulate operations using mutable data.</span></span> <span data-ttu-id="34034-294">Cela n’est pas toujours suffisant pour les jeux de données plus complexes.</span><span class="sxs-lookup"><span data-stu-id="34034-294">This is not always sufficient for more complex sets of data.</span></span> <span data-ttu-id="34034-295">Tenez compte des ensembles de fonctions suivants :</span><span class="sxs-lookup"><span data-stu-id="34034-295">Consider the following sets of functions:</span></span>

```fsharp
open System.Collections.Generic

let addToClosureTable (key, value) (t: Dictionary<_,_>) =
    if not (t.ContainsKey(key)) then
        t.Add(key, value)
    else
        t.[key] <- value

let closureTableCount (t: Dictionary<_,_>) = t.Count

let closureTableContains (key, value) (t: Dictionary<_, HashSet<_>>) =
    match t.TryGetValue(key) with
    | (true, v) -> v.Equals(value)
    | (false, _) -> false
```

<span data-ttu-id="34034-296">Ce code est performant, mais elle présente la structure de données basée sur une mutation que les appelants sont responsables de la maintenance.</span><span class="sxs-lookup"><span data-stu-id="34034-296">This code is performant, but it exposes the mutation-based data structure that callers are responsible for maintaining.</span></span> <span data-ttu-id="34034-297">Cela peut être encapsulée à l’intérieur d’une classe sans membres sous-jacentes qui peuvent changer :</span><span class="sxs-lookup"><span data-stu-id="34034-297">This can be wrapped inside of a class with no underlying members that can change:</span></span>

```fsharp
open System.Collections.Generic

/// The results of computing the LALR(1) closure of an LR(0) kernel
type Closure1Table() =
    let t = Dictionary<Item0, HashSet<TerminalIndex>>()

    member __.Add(key, value) =
        if not (t.ContainsKey(key)) then
            t.Add(key, value)
        else
            t.[key] <- value

    member __.Count = t.Count

    member __.Contains(key, value) =
        match t.TryGetValue(key) with
        | (true, v) -> v.Equals(value)
        | (false, _) -> false
```

<span data-ttu-id="34034-298">`Closure1Table` encapsule la structure sous-jacente de données basées sur une mutation, ne pas forcer l’appelants pour conserver la structure de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="34034-298">`Closure1Table` encapsulates the underlying mutation-based data structure, thereby not forcing callers to maintain the underlying data structure.</span></span> <span data-ttu-id="34034-299">Les classes sont un excellent moyen d’encapsuler des données et des routines qui sont basés sur une mutation sans exposer les détails aux appelants.</span><span class="sxs-lookup"><span data-stu-id="34034-299">Classes are a powerful way to encapsulate data and routines that are mutation-based without exposing the details to callers.</span></span>

### <a name="prefer-let-mutable-to-reference-cells"></a><span data-ttu-id="34034-300">Préférez `let mutable` aux cellules de référence</span><span class="sxs-lookup"><span data-stu-id="34034-300">Prefer `let mutable` to reference cells</span></span>

<span data-ttu-id="34034-301">Cellules de référence sont un moyen pour représenter la référence à une valeur plutôt que la valeur elle-même.</span><span class="sxs-lookup"><span data-stu-id="34034-301">Reference cells are a way to represent the reference to a value rather than the value itself.</span></span> <span data-ttu-id="34034-302">Bien qu’ils peuvent être utilisés pour le code critique pour les performances, ils sont généralement pas recommandés.</span><span class="sxs-lookup"><span data-stu-id="34034-302">Although they can be used for performance-critical code, they are generally not recommended.</span></span> <span data-ttu-id="34034-303">Prenons l'exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="34034-303">Consider the following example:</span></span>

```fsharp
let kernels =
    let acc = ref Set.empty

    processWorkList startKernels (fun kernel ->
        if not ((!acc).Contains(kernel)) then
            acc := (!acc).Add(kernel)
        ...)

    !acc |> Seq.toList
```

<span data-ttu-id="34034-304">L’utilisation d’une cellule de référence est maintenant « pollue « tout le code suivant à la suppression de la référence et re-référencer les données sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="34034-304">The use of a reference cell now "pollutes" all subsequent code with having to dereference and re-reference the underlying data.</span></span> <span data-ttu-id="34034-305">Envisagez plutôt `let mutable`:</span><span class="sxs-lookup"><span data-stu-id="34034-305">Instead, consider `let mutable`:</span></span>

```fsharp
let kernels =
    let mutable acc = Set.empty

    processWorkList startKernels (fun kernel ->
        if not (acc.Contains(kernel)) then
            acc <- acc.Add(kernel)
        ...)

    acc |> Seq.toList
```

<span data-ttu-id="34034-306">Le point de mutation au milieu de l’expression lambda unique, à l’exception de tout autre code qui touche `acc` faire d’une manière qui est identique à l’utilisation d’un vecteur normal `let`-immuable valeur limite.</span><span class="sxs-lookup"><span data-stu-id="34034-306">Aside from the single point of mutation in the middle of the lambda expression, all other code that touches `acc` can do so in a manner that is no different to the usage of a normal `let`-bound immutable value.</span></span> <span data-ttu-id="34034-307">Cela rend plus facile de modifier au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="34034-307">This will make it easier to change over time.</span></span>

## <a name="object-programming"></a><span data-ttu-id="34034-308">Objet de programmation</span><span class="sxs-lookup"><span data-stu-id="34034-308">Object programming</span></span>

<span data-ttu-id="34034-309">F # est prise en charge complète pour les objets et concepts de (OO) et orienté objet.</span><span class="sxs-lookup"><span data-stu-id="34034-309">F# has full support for objects and object-oriented (OO) concepts.</span></span> <span data-ttu-id="34034-310">Bien que de nombreux concepts OO sont puissantes et utiles, tous les sont idéaux pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="34034-310">Although many OO concepts are powerful and useful, not all of them are ideal to use.</span></span> <span data-ttu-id="34034-311">Les listes suivantes offrent des conseils sur les catégories de fonctionnalités OO à un niveau élevé.</span><span class="sxs-lookup"><span data-stu-id="34034-311">The following lists offer guidance on categories of OO features at a high level.</span></span>

<span data-ttu-id="34034-312">**Envisagez d’utiliser ces fonctionnalités dans de nombreuses situations :**</span><span class="sxs-lookup"><span data-stu-id="34034-312">**Consider using these features in many situations:**</span></span>

* <span data-ttu-id="34034-313">Notation par points (`x.Length`)</span><span class="sxs-lookup"><span data-stu-id="34034-313">Dot notation (`x.Length`)</span></span>
* <span data-ttu-id="34034-314">Membres d’instance</span><span class="sxs-lookup"><span data-stu-id="34034-314">Instance members</span></span>
* <span data-ttu-id="34034-315">Constructeurs implicites</span><span class="sxs-lookup"><span data-stu-id="34034-315">Implicit constructors</span></span>
* <span data-ttu-id="34034-316">Membres static</span><span class="sxs-lookup"><span data-stu-id="34034-316">Static members</span></span>
* <span data-ttu-id="34034-317">Notation d’indexeur (`arr.[x]`)</span><span class="sxs-lookup"><span data-stu-id="34034-317">Indexer notation (`arr.[x]`)</span></span>
* <span data-ttu-id="34034-318">Arguments nommés et facultatifs</span><span class="sxs-lookup"><span data-stu-id="34034-318">Named and Optional arguments</span></span>
* <span data-ttu-id="34034-319">Interfaces et implémentations d’interface</span><span class="sxs-lookup"><span data-stu-id="34034-319">Interfaces and interface implementations</span></span>

<span data-ttu-id="34034-320">**Ne pas atteindre tout d’abord pour ces fonctionnalités, mais judicieusement appliquent les lorsqu’ils se trouvent pratiques résoudre un problème :**</span><span class="sxs-lookup"><span data-stu-id="34034-320">**Don't reach for these features first, but do judiciously apply them when they are convenient to solve a problem:**</span></span>

* <span data-ttu-id="34034-321">Surcharge de méthode</span><span class="sxs-lookup"><span data-stu-id="34034-321">Method overloading</span></span>
* <span data-ttu-id="34034-322">Données mutables encapsulées</span><span class="sxs-lookup"><span data-stu-id="34034-322">Encapsulated mutable data</span></span>
* <span data-ttu-id="34034-323">Opérateurs sur les types</span><span class="sxs-lookup"><span data-stu-id="34034-323">Operators on types</span></span>
* <span data-ttu-id="34034-324">Propriétés automatiques</span><span class="sxs-lookup"><span data-stu-id="34034-324">Auto properties</span></span>
* <span data-ttu-id="34034-325">Implémentation de `IDisposable` et `IEnumerable`</span><span class="sxs-lookup"><span data-stu-id="34034-325">Implementing `IDisposable` and `IEnumerable`</span></span>
* <span data-ttu-id="34034-326">Extensions de type</span><span class="sxs-lookup"><span data-stu-id="34034-326">Type extensions</span></span>
* <span data-ttu-id="34034-327">Événements</span><span class="sxs-lookup"><span data-stu-id="34034-327">Events</span></span>
* <span data-ttu-id="34034-328">Structs</span><span class="sxs-lookup"><span data-stu-id="34034-328">Structs</span></span>
* <span data-ttu-id="34034-329">Délégués</span><span class="sxs-lookup"><span data-stu-id="34034-329">Delegates</span></span>
* <span data-ttu-id="34034-330">Enums</span><span class="sxs-lookup"><span data-stu-id="34034-330">Enums</span></span>

<span data-ttu-id="34034-331">**Généralement éviter ces fonctionnalités, sauf si vous devez les utiliser :**</span><span class="sxs-lookup"><span data-stu-id="34034-331">**Generally avoid these features unless you must use them:**</span></span>

* <span data-ttu-id="34034-332">Hiérarchies d’héritage de type et l’héritage d’implémentation</span><span class="sxs-lookup"><span data-stu-id="34034-332">Inheritance-based type hierarchies and implementation inheritance</span></span>
* <span data-ttu-id="34034-333">Les valeurs NULL et `Unchecked.defaultof<_>`</span><span class="sxs-lookup"><span data-stu-id="34034-333">Nulls and `Unchecked.defaultof<_>`</span></span>

### <a name="prefer-composition-over-inheritance"></a><span data-ttu-id="34034-334">Préférer composition d’héritage</span><span class="sxs-lookup"><span data-stu-id="34034-334">Prefer composition over inheritance</span></span>

<span data-ttu-id="34034-335">[Composition de l’héritage](https://en.wikipedia.org/wiki/Composition_over_inheritance) est un idiome de longue date bon code F # peut respecter.</span><span class="sxs-lookup"><span data-stu-id="34034-335">[Composition over inheritance](https://en.wikipedia.org/wiki/Composition_over_inheritance) is a long-standing idiom that good F# code can adhere to.</span></span> <span data-ttu-id="34034-336">Le principe fondamental est que vous ne devez pas exposer une classe de base et forcer les appelants à hériter de cette classe pour obtenir les fonctionnalités de base.</span><span class="sxs-lookup"><span data-stu-id="34034-336">The fundamental principle is that you should not expose a base class and force callers to inherit from that base class to get functionality.</span></span>

### <a name="use-object-expressions-to-implement-interfaces-if-you-dont-need-a-class"></a><span data-ttu-id="34034-337">Utiliser des expressions d’objet pour implémenter les interfaces si vous n’avez pas besoin d’une classe</span><span class="sxs-lookup"><span data-stu-id="34034-337">Use object expressions to implement interfaces if you don't need a class</span></span>

<span data-ttu-id="34034-338">[Expressions d’objet](../language-reference/object-expressions.md) vous permettent d’implémenter des interfaces à la volée, liaison de l’interface implémentée à une valeur sans avoir à le faire à l’intérieur d’une classe.</span><span class="sxs-lookup"><span data-stu-id="34034-338">[Object Expressions](../language-reference/object-expressions.md) allow you to implement interfaces on the fly, binding the implemented interface to a value without needing to do so inside of a class.</span></span> <span data-ttu-id="34034-339">Ceci est pratique, surtout si vous _uniquement_ doivent implémenter l’interface et n’ont pas besoin d’une classe complète.</span><span class="sxs-lookup"><span data-stu-id="34034-339">This is convenient, especially if you _only_ need to implement the interface and have no need for a full class.</span></span>

<span data-ttu-id="34034-340">Par exemple, voici le code qui est exécuté dans [Ionide](http://ionide.io/) pour fournir une action de correction du code si vous avez ajouté un symbole que vous n’avez pas une `open` instruction pour :</span><span class="sxs-lookup"><span data-stu-id="34034-340">For example, here is the code that is run in [Ionide](http://ionide.io/) to provide a code fix action if you've added a symbol that you don't have an `open` statement for:</span></span>

```fsharp
    let private createProvider () =
        { new CodeActionProvider with
            member this.provideCodeActions(doc, range, context, ct) =
                let diagnostics = context.diagnostics
                let diagnostic = diagnostics |> Seq.tryFind (fun d -> d.message.Contains "Unused open statement")
                let res =
                    match diagnostic with
                    | None -> [||]
                    | Some d ->
                        let line = doc.lineAt d.range.start.line
                        let cmd = createEmpty<Command>
                        cmd.title <- "Remove unused open"
                        cmd.command <- "fsharp.unusedOpenFix"
                        cmd.arguments <- Some ([| doc |> unbox; line.range |> unbox; |] |> ResizeArray)
                        [|cmd |]
                res
                |> ResizeArray
                |> U2.Case1
        }
```

<span data-ttu-id="34034-341">Car il n’est pas nécessaire pour une classe lors de l’interaction avec l’API de Code Visual Studio, les Expressions d’objet sont un outil idéal pour cela.</span><span class="sxs-lookup"><span data-stu-id="34034-341">Because there is no need for a class when interacting with the Visual Studio Code API, Object Expressions are an ideal tool for this.</span></span> <span data-ttu-id="34034-342">Ils sont également utiles pour les tests unitaires, lorsque vous souhaitez une interface avec les routines de test de stub de manière ad hoc.</span><span class="sxs-lookup"><span data-stu-id="34034-342">They are also valuable for unit testing, when you want to stub out an interface with test routines in an ad hoc manner.</span></span>

## <a name="type-abbreviations"></a><span data-ttu-id="34034-343">Abréviations de types</span><span class="sxs-lookup"><span data-stu-id="34034-343">Type Abbreviations</span></span>

<span data-ttu-id="34034-344">[Abréviations de types](../language-reference/type-abbreviations.md) sont un moyen pratique pour attribuer une étiquette à un autre type, par exemple une signature de fonction ou un type plus complexe.</span><span class="sxs-lookup"><span data-stu-id="34034-344">[Type Abbreviations](../language-reference/type-abbreviations.md) are a convenient way to assign a label to another type, such as a function signature or a more complex type.</span></span> <span data-ttu-id="34034-345">Par exemple, l’alias suivant attribue une étiquette à ce qui est nécessaire pour définir un calcul avec [CNTK](https://www.microsoft.com/cognitive-toolkit/), une profondeur d’apprentissage :</span><span class="sxs-lookup"><span data-stu-id="34034-345">For example, the following alias assigns a label to what's needed to define a computation with [CNTK](https://www.microsoft.com/cognitive-toolkit/), a deep learning library:</span></span>

```fsharp
open CNTK

// DeviceDescriptor, Variable, and Function all come from CNTK
type Computation = DeviceDescriptor -> Variable -> Function
```

<span data-ttu-id="34034-346">Le `Computation` nom est un moyen pratique pour désigner n’importe quelle fonction qui correspond à la signature, il s’agit d’alias.</span><span class="sxs-lookup"><span data-stu-id="34034-346">The `Computation` name is a convenient way to denote any function that matches the signature it is aliasing.</span></span> <span data-ttu-id="34034-347">À l’aide des abréviations de Type, comme cela est pratique et autorise le code plus concise.</span><span class="sxs-lookup"><span data-stu-id="34034-347">Using Type Abbreviations like this is convenient and allows for more succinct code.</span></span>

### <a name="avoid-using-type-abbreviations-to-represent-your-domain"></a><span data-ttu-id="34034-348">Évitez d’utiliser les abréviations de Type pour représenter votre domaine</span><span class="sxs-lookup"><span data-stu-id="34034-348">Avoid using Type Abbreviations to represent your domain</span></span>

<span data-ttu-id="34034-349">Bien que les abréviations de Type sont pratiques pour donner un nom à des signatures de fonction, elles peuvent être ambigües lors de l’abréviation d’autres types.</span><span class="sxs-lookup"><span data-stu-id="34034-349">Although Type Abbreviations are convenient for giving a name to function signatures, they can be confusing when abbreviating other types.</span></span> <span data-ttu-id="34034-350">Prenez en compte cette abréviation :</span><span class="sxs-lookup"><span data-stu-id="34034-350">Consider this abbreviation:</span></span>

```fsharp
// Does not actually abstract integers.
type BufferSize = int
```

<span data-ttu-id="34034-351">Cela peut prêter à confusion de plusieurs façons :</span><span class="sxs-lookup"><span data-stu-id="34034-351">This can be confusing in multiple ways:</span></span>

* <span data-ttu-id="34034-352">`BufferSize` n’est pas une abstraction ; Il est simplement un autre nom d’un entier.</span><span class="sxs-lookup"><span data-stu-id="34034-352">`BufferSize` is not an abstraction; it is just another name for an integer.</span></span>
* <span data-ttu-id="34034-353">Si `BufferSize` est exposé dans une API publique, il peut facilement être mal interprétée pour signifier plus que `int`.</span><span class="sxs-lookup"><span data-stu-id="34034-353">If `BufferSize` is exposed in a public API, it can easily be misinterpreted to mean more than just `int`.</span></span> <span data-ttu-id="34034-354">En général, les types de domaine ont plusieurs attributs leur et ne sont pas des types primitifs comme `int`.</span><span class="sxs-lookup"><span data-stu-id="34034-354">Generally, domain types have multiple attributes to them and are not primitive types like `int`.</span></span> <span data-ttu-id="34034-355">Cette abréviation viole cette hypothèse.</span><span class="sxs-lookup"><span data-stu-id="34034-355">This abbreviation violates that assumption.</span></span>
* <span data-ttu-id="34034-356">La casse de `BufferSize` (PascalCase) implique que ce type conserve plus de données.</span><span class="sxs-lookup"><span data-stu-id="34034-356">The casing of `BufferSize` (PascalCase) implies that this type holds more data.</span></span>
* <span data-ttu-id="34034-357">Cet alias n’offre pas de souci de clarté accrue par rapport à fournir un argument nommé d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="34034-357">This alias does not offer increased clarity compared with providing a named argument to a function.</span></span>
* <span data-ttu-id="34034-358">L’abréviation n’apparaîtra pas dans IL compilé ; Il s’agit simplement d’un entier, et cet alias est une construction de la compilation.</span><span class="sxs-lookup"><span data-stu-id="34034-358">The abbreviation will not manifest in compiled IL; it is just an integer and this alias is a compile-time construct.</span></span>

```fsharp
module Networking =
    ...
    let send data (bufferSize: int) =
        ...
```

<span data-ttu-id="34034-359">En résumé, le piège avec les abréviations de Type est qu’ils sont **pas** abstractions sur les types qu’ils sont l’abréviation.</span><span class="sxs-lookup"><span data-stu-id="34034-359">In summary, the pitfall with Type Abbreviations is that they are **not** abstractions over the types they are abbreviating.</span></span> <span data-ttu-id="34034-360">Dans l’exemple précédent, `BufferSize` est simplement un `int` en arrière-plan, avec des données supplémentaires, ni les avantages du système de type en dehors de ce que `int` a déjà.</span><span class="sxs-lookup"><span data-stu-id="34034-360">In the previous example, `BufferSize` is just an `int` under the covers, with no additional data, nor any benefits from the type system besides what `int` already has.</span></span>
