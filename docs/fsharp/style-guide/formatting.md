---
title: 'Les instructions de mise en forme de code F #'
description: 'Découvrez les instructions de mise en forme de code F #.'
ms.date: 05/14/2018
ms.openlocfilehash: 0d7d2d1771710db55bf990f3a06079b2aec48fd7
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43858003"
---
# <a name="f-code-formatting-guidelines"></a><span data-ttu-id="b1e40-103">Les instructions de mise en forme de code F #</span><span class="sxs-lookup"><span data-stu-id="b1e40-103">F# code formatting guidelines</span></span>

<span data-ttu-id="b1e40-104">Cet article propose des instructions pour savoir comment mettre en forme votre code afin que votre code F # est :</span><span class="sxs-lookup"><span data-stu-id="b1e40-104">This article offers guidelines for how to format your code so that your F# code is:</span></span>

* <span data-ttu-id="b1e40-105">Généralement considérée comme plus lisibles</span><span class="sxs-lookup"><span data-stu-id="b1e40-105">Generally viewed as more legible</span></span>
* <span data-ttu-id="b1e40-106">Est conformément aux conventions appliquées par la mise en forme des outils dans Visual Studio et autres éditeurs</span><span class="sxs-lookup"><span data-stu-id="b1e40-106">Is in accordance with conventions applied by formatting tools in Visual Studio and other editors</span></span>
* <span data-ttu-id="b1e40-107">Similaire à un autre code en ligne</span><span class="sxs-lookup"><span data-stu-id="b1e40-107">Similar to other code online</span></span>

<span data-ttu-id="b1e40-108">Ces instructions sont basées sur [un guide complet sur les Conventions de mise en forme F #](https://github.com/dungpa/fantomas/blob/master/docs/FormattingConventions.md) par [Anh-Dung Phan](https://github.com/dungpa).</span><span class="sxs-lookup"><span data-stu-id="b1e40-108">These guidelines are based on [A comprehensive guide to F# Formatting Conventions](https://github.com/dungpa/fantomas/blob/master/docs/FormattingConventions.md) by [Anh-Dung Phan](https://github.com/dungpa).</span></span>

## <a name="general-rules-for-indentation"></a><span data-ttu-id="b1e40-109">Règles générales pour la mise en retrait</span><span class="sxs-lookup"><span data-stu-id="b1e40-109">General rules for indentation</span></span>

<span data-ttu-id="b1e40-110">F # utilise des espaces blancs significatifs par défaut.</span><span class="sxs-lookup"><span data-stu-id="b1e40-110">F# uses significant white space by default.</span></span> <span data-ttu-id="b1e40-111">Les instructions suivantes sont destinées à fournir des conseils quant à jongler avec des défis que cela peut imposer.</span><span class="sxs-lookup"><span data-stu-id="b1e40-111">The following guidelines are intended to provide guidance as to how to juggle some challenges this can impose.</span></span>

### <a name="using-spaces"></a><span data-ttu-id="b1e40-112">L’utilisation des espaces</span><span class="sxs-lookup"><span data-stu-id="b1e40-112">Using spaces</span></span>

<span data-ttu-id="b1e40-113">Lors de la mise en retrait est requise, vous devez utiliser des espaces, tabulations pas.</span><span class="sxs-lookup"><span data-stu-id="b1e40-113">When indentation is required, you must use spaces, not tabs.</span></span> <span data-ttu-id="b1e40-114">Au moins un espace est requis.</span><span class="sxs-lookup"><span data-stu-id="b1e40-114">At least one space is required.</span></span> <span data-ttu-id="b1e40-115">Votre organisation peut créer des normes de codage pour spécifier le nombre d’espaces à utiliser pour la mise en retrait ; deux, trois ou quatre espaces de mise en retrait à chaque niveau de mise en retrait est typique.</span><span class="sxs-lookup"><span data-stu-id="b1e40-115">Your organization can create coding standards to specify the number of spaces to use for indentation; two, three or four spaces of indentation at each level where indentation occurs is typical.</span></span>

<span data-ttu-id="b1e40-116">**Nous vous recommandons 4 espaces par mise en retrait.**</span><span class="sxs-lookup"><span data-stu-id="b1e40-116">**We recommend 4 spaces per indentation.**</span></span>

<span data-ttu-id="b1e40-117">Ceci dit, la mise en retrait de programmes est très subjective.</span><span class="sxs-lookup"><span data-stu-id="b1e40-117">That said, indentation of programs is a subjective matter.</span></span> <span data-ttu-id="b1e40-118">Variations sont OK, mais la première règle, vous devez suivre est *la cohérence de la mise en retrait*.</span><span class="sxs-lookup"><span data-stu-id="b1e40-118">Variations are OK, but the first rule you should follow is *consistency of indentation*.</span></span> <span data-ttu-id="b1e40-119">Choisir un style généralement accepté de mise en retrait et l’utiliser systématiquement tout au long de votre base de code.</span><span class="sxs-lookup"><span data-stu-id="b1e40-119">Choose a generally accepted style of indentation and use it systematically throughout your codebase.</span></span>

## <a name="formatting-blank-lines"></a><span data-ttu-id="b1e40-120">Mise en forme des lignes vides</span><span class="sxs-lookup"><span data-stu-id="b1e40-120">Formatting blank lines</span></span>

* <span data-ttu-id="b1e40-121">Distinct niveau supérieur (fonction) et classe les définitions avec deux lignes vides.</span><span class="sxs-lookup"><span data-stu-id="b1e40-121">Separate top-level function and class definitions with two blank lines.</span></span>
* <span data-ttu-id="b1e40-122">Les définitions de méthode à l’intérieur d’une classe sont séparées par une ligne vierge.</span><span class="sxs-lookup"><span data-stu-id="b1e40-122">Method definitions inside a class are separated by a single blank line.</span></span>
* <span data-ttu-id="b1e40-123">Lignes vierges supplémentaires peuvent servir (avec parcimonie) pour séparer les groupes de fonctions associées.</span><span class="sxs-lookup"><span data-stu-id="b1e40-123">Extra blank lines may be used (sparingly) to separate groups of related functions.</span></span> <span data-ttu-id="b1e40-124">Peuvent être omis des lignes vides entre un ensemble de commandes associées à une ligne (par exemple, un ensemble d’implémentations factices).</span><span class="sxs-lookup"><span data-stu-id="b1e40-124">Blank lines may be omitted between a bunch of related one-liners (for example, a set of dummy implementations).</span></span>
* <span data-ttu-id="b1e40-125">Utiliser avec parcimonie, des lignes vides dans les fonctions, pour indiquer les sections logiques.</span><span class="sxs-lookup"><span data-stu-id="b1e40-125">Use blank lines in functions, sparingly, to indicate logical sections.</span></span>

## <a name="formatting-comments"></a><span data-ttu-id="b1e40-126">Mise en forme de commentaires</span><span class="sxs-lookup"><span data-stu-id="b1e40-126">Formatting comments</span></span>

<span data-ttu-id="b1e40-127">Préférez généralement plusieurs commentaires double barre oblique sur les commentaires de bloc de style de ML.</span><span class="sxs-lookup"><span data-stu-id="b1e40-127">Generally prefer multiple double-slash comments over ML-style block comments.</span></span>

```fsharp
// Prefer this style of comments when you want
// to express written ideas on multiple lines.

(*
    ML-style comments are fine, but not a .NET-ism.
    They are useful when needing to modify multi-line comments, though.
*)
```

<span data-ttu-id="b1e40-128">Les commentaires incorporés doivent mettre en majuscule la première lettre.</span><span class="sxs-lookup"><span data-stu-id="b1e40-128">Inline comments should capitalize the first letter.</span></span>

```fsharp
let f x = x + 1 // Increment by one.
```

## <a name="naming-conventions"></a><span data-ttu-id="b1e40-129">Conventions d'attribution d'un nom</span><span class="sxs-lookup"><span data-stu-id="b1e40-129">Naming conventions</span></span>

### <a name="use-camelcase-for-class-bound-expression-bound-and-pattern-bound-values-and-functions"></a><span data-ttu-id="b1e40-130">Utilisent une casse mixte pour les fonctions et les valeurs de limite de classe, expression-liées aux et modèle</span><span class="sxs-lookup"><span data-stu-id="b1e40-130">Use camelCase for class-bound, expression-bound and pattern-bound values and functions</span></span>

<span data-ttu-id="b1e40-131">Il est courant et acceptés F # style à utiliser une casse mixte pour tous les noms liée en tant que variables locales ou dans les correspondances de modèle et les définitions de fonction.</span><span class="sxs-lookup"><span data-stu-id="b1e40-131">It is common and accepted F# style to use camelCase for all names bound as local variables or in pattern matches and function definitions.</span></span>

```fsharp
// OK
let addIAndJ i j = i + j

// Bad
let addIAndJ I J = I+J

// Bad
let AddIAndJ i j = i + j
```

<span data-ttu-id="b1e40-132">Fonctions liées à localement dans les classes doivent également utiliser une casse mixte.</span><span class="sxs-lookup"><span data-stu-id="b1e40-132">Locally-bound functions in classes should also use camelCase.</span></span>

```fsharp
type MyClass() =

    let doSomething () =

    let firstResult = ...

    let secondResult = ...

    member x.Result = doSomething()
```

### <a name="use-camelcase-for-module-bound-public-functions"></a><span data-ttu-id="b1e40-133">Utilisent une casse mixte pour les fonctions publiques liées à un module</span><span class="sxs-lookup"><span data-stu-id="b1e40-133">Use camelCase for module-bound public functions</span></span>

<span data-ttu-id="b1e40-134">Quand une fonction liée au module fait partie d’une API publique, il doit utiliser une casse mixte :</span><span class="sxs-lookup"><span data-stu-id="b1e40-134">When a module-bound function is part of a public API, it should use camelCase:</span></span>

```fsharp
module MyAPI =
    let publicFunctionOne param1 param2 param2 = ...

    let publicFunctionTwo param1 param2 param3 = ...
```

### <a name="use-camelcase-for-internal-and-private-module-bound-values-and-functions"></a><span data-ttu-id="b1e40-135">Utilisent une casse mixte pour les fonctions et les valeurs de module dépendant internes et privés</span><span class="sxs-lookup"><span data-stu-id="b1e40-135">Use camelCase for internal and private module-bound values and functions</span></span>

<span data-ttu-id="b1e40-136">Utilisez la casse mixte pour les valeurs liée aux module privées, y compris les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b1e40-136">Use camelCase for private module-bound values, including the following:</span></span>

* <span data-ttu-id="b1e40-137">Fonctions ad hoc dans les scripts</span><span class="sxs-lookup"><span data-stu-id="b1e40-137">Ad hoc functions in scripts</span></span>

* <span data-ttu-id="b1e40-138">Valeurs constituant l’implémentation interne d’un module ou un type</span><span class="sxs-lookup"><span data-stu-id="b1e40-138">Values making up the internal implementation of a module or type</span></span>

```fsharp
let emailMyBossTheLatestResults =
    ...
```

### <a name="use-camelcase-for-parameters"></a><span data-ttu-id="b1e40-139">Utilisez la casse mixte pour les paramètres</span><span class="sxs-lookup"><span data-stu-id="b1e40-139">Use camelCase for parameters</span></span>

<span data-ttu-id="b1e40-140">Tous les paramètres doivent utiliser une casse mixte conformément aux conventions d’affectation de noms .NET.</span><span class="sxs-lookup"><span data-stu-id="b1e40-140">All parameters should use camelCase in accordance with .NET naming conventions.</span></span>

```fsharp
module MyModule =
    let myFunction paramOne paramTwo = ...

type MyClass() =
    member this.MyMethod(paramOne, paramTwo) = ...
```

### <a name="use-pascalcase-for-modules"></a><span data-ttu-id="b1e40-141">Utiliser la casse Pascal pour les modules</span><span class="sxs-lookup"><span data-stu-id="b1e40-141">Use PascalCase for modules</span></span>

<span data-ttu-id="b1e40-142">Tous les modules (niveau supérieur, internes, privés, imbriquées) doivent utiliser la casse Pascal.</span><span class="sxs-lookup"><span data-stu-id="b1e40-142">All modules (top-level, internal, private, nested) should use PascalCase.</span></span>

```fsharp
module MyTopLevelModule

module Helpers =
    module private SuperHelpers =
        ...

    ...
```

### <a name="use-pascalcase-for-type-declarations-members-and-labels"></a><span data-ttu-id="b1e40-143">Utilisez la casse Pascal pour les déclarations de type, les membres et les étiquettes</span><span class="sxs-lookup"><span data-stu-id="b1e40-143">Use PascalCase for type declarations, members, and labels</span></span>

<span data-ttu-id="b1e40-144">Classes, interfaces, structures, énumérations, délégués, les enregistrements et les unions discriminées doivent être nommées avec la casse Pascal.</span><span class="sxs-lookup"><span data-stu-id="b1e40-144">Classes, interfaces, structs, enumerations, delegates, records, and discriminated unions should all be named with PascalCase.</span></span> <span data-ttu-id="b1e40-145">Membres au sein des types et des étiquettes pour les enregistrements et les unions discriminées doivent également utiliser la casse Pascal.</span><span class="sxs-lookup"><span data-stu-id="b1e40-145">Members within types and labels for records and discriminated unions should also use PascalCase.</span></span>

```fsharp
type IMyInterface =
    abstract Something: int

type MyClass() =
    member this.MyMethod(x, y) = x + y

type MyRecord = { IntVal: int; StringVal: string }

type SchoolPerson =
    | Professor
    | Student
    | Advisor
    | Administrator
```

### <a name="use-pascalcase-for-constructs-intrinsic-to-net"></a><span data-ttu-id="b1e40-146">Utilisez la casse Pascal pour les constructions intrinsèques pour .NET</span><span class="sxs-lookup"><span data-stu-id="b1e40-146">Use PascalCase for constructs intrinsic to .NET</span></span>

<span data-ttu-id="b1e40-147">Espaces de noms, exceptions, événements et projet /`.dll` noms doivent également utiliser la casse Pascal.</span><span class="sxs-lookup"><span data-stu-id="b1e40-147">Namespaces, exceptions, events, and project/`.dll` names should also use PascalCase.</span></span> <span data-ttu-id="b1e40-148">Non seulement est-ce que la consommation à partir d’autres langages .NET sembler plus naturelle pour les consommateurs, il est également cohérente avec les conventions d’affectation de noms .NET que vous êtes susceptible de rencontrer.</span><span class="sxs-lookup"><span data-stu-id="b1e40-148">Not only does this make consumption from other .NET languages feel more natural to consumers, it's also consistent with .NET naming conventions that you are likely to encounter.</span></span>

### <a name="avoid-underscores-in-names"></a><span data-ttu-id="b1e40-149">Éviter les traits de soulignement dans les noms</span><span class="sxs-lookup"><span data-stu-id="b1e40-149">Avoid underscores in names</span></span>

<span data-ttu-id="b1e40-150">Historiquement, certaines bibliothèques F # ont utilisé des traits de soulignement dans les noms.</span><span class="sxs-lookup"><span data-stu-id="b1e40-150">Historically, some F# libraries have used underscores in names.</span></span> <span data-ttu-id="b1e40-151">Toutefois, cela est n’est plus largement acceptée, en partie parce qu’il est en conflit avec les conventions d’affectation de noms .NET.</span><span class="sxs-lookup"><span data-stu-id="b1e40-151">However, this is no longer widely accepted, partly because it clashes with .NET naming conventions.</span></span> <span data-ttu-id="b1e40-152">Ceci dit, certains programmeurs F # utilisent des traits de soulignement fortement, en partie pour des raisons historiques, et la tolérance de panne et le respect est important.</span><span class="sxs-lookup"><span data-stu-id="b1e40-152">That said, some F# programmers use underscores heavily, partly for historical reasons, and tolerance and respect is important.</span></span> <span data-ttu-id="b1e40-153">Toutefois, n’oubliez pas que le style n’est souvent pas satisfaisant par d’autres personnes qui ont la possibilité d’utiliser.</span><span class="sxs-lookup"><span data-stu-id="b1e40-153">However, be aware that the style is often disliked by others who have a choice about whether to use it.</span></span>

<span data-ttu-id="b1e40-154">Certaines exceptions inclut l’interopérabilité avec les composants natifs, où des traits de soulignement sont très courantes.</span><span class="sxs-lookup"><span data-stu-id="b1e40-154">Some exceptions includes interoperating with native components, where underscores are very common.</span></span>

### <a name="use-standard-f-operators"></a><span data-ttu-id="b1e40-155">Utilisez les opérateurs standard F #</span><span class="sxs-lookup"><span data-stu-id="b1e40-155">Use standard F# operators</span></span>

<span data-ttu-id="b1e40-156">Les opérateurs suivants sont définis dans la bibliothèque standard F # et doivent être utilisés au lieu de définir des équivalents.</span><span class="sxs-lookup"><span data-stu-id="b1e40-156">The following operators are defined in the F# standard library and should be used instead of defining equivalents.</span></span> <span data-ttu-id="b1e40-157">L’utilisation de ces opérateurs est recommandée car elle a tendance à rendre le code plus lisible et idiomatique.</span><span class="sxs-lookup"><span data-stu-id="b1e40-157">Using these operators is recommended as it tends to make code more readable and idiomatic.</span></span> <span data-ttu-id="b1e40-158">Les développeurs avec un arrière-plan dans OCaml ou autre langage de programmation fonctionnel peut-être habitués à différents idiomes.</span><span class="sxs-lookup"><span data-stu-id="b1e40-158">Developers with a background in OCaml or other functional programming language may be accustomed to different idioms.</span></span> <span data-ttu-id="b1e40-159">La liste suivante récapitule les opérateurs F # recommandées.</span><span class="sxs-lookup"><span data-stu-id="b1e40-159">The following list summarizes the recommended F# operators.</span></span>

```fsharp
x |> f // Forward pipeline
f >> g // Forward composition
x |> ignore // Discard away a value
x + y // Overloaded addition (including string concatenation)
x - y // Overloaded subtraction
x * y // Overloaded multiplication
x / y // Overloaded division
x % y // Overloaded modulus
x && y // Lazy/short-cut "and"
x || y // Lazy/short-cut "or"
x <<< y // Bitwise left shift
x >>> y // Bitwise right shift
x ||| y // Bitwise or, also for working with “flags” enumeration
x &&& y // Bitwise and, also for working with “flags” enumeration
x ^^^ y // Bitwise xor, also for working with “flags” enumeration
```

### <a name="use-prefix-syntax-for-generics-foot-in-preference-to-postfix-syntax-t-foo"></a><span data-ttu-id="b1e40-160">Utiliser la syntaxe du préfixe pour les génériques (`Foo<T>`) plutôt que de la syntaxe de suffixe (`T Foo`)</span><span class="sxs-lookup"><span data-stu-id="b1e40-160">Use prefix syntax for generics (`Foo<T>`) in preference to postfix syntax (`T Foo`)</span></span>

<span data-ttu-id="b1e40-161">F # hérite à la fois le style de ML suffixe de nommage des types génériques (par exemple, `int list`), ainsi que le préfixe de style .NET (par exemple, `list<int>`).</span><span class="sxs-lookup"><span data-stu-id="b1e40-161">F# inherits both the postfix ML style of naming generic types (for example, `int list`) as well as the prefix .NET style (for example, `list<int>`).</span></span> <span data-ttu-id="b1e40-162">Préférer le style de .NET, à l’exception des quatre types spécifiques :</span><span class="sxs-lookup"><span data-stu-id="b1e40-162">Prefer the .NET style, except for four specific types:</span></span>

1. <span data-ttu-id="b1e40-163">Pour les listes F #, utilisez la forme suffixée : `int list` plutôt que `list<int>`.</span><span class="sxs-lookup"><span data-stu-id="b1e40-163">For F# Lists, use the postfix form: `int list` rather than `list<int>`.</span></span>
2. <span data-ttu-id="b1e40-164">Pour les Options F #, utilisez la forme suffixée : `int option` plutôt que `option<int>`.</span><span class="sxs-lookup"><span data-stu-id="b1e40-164">For F# Options, use the postfix form: `int option` rather than `option<int>`.</span></span>
3. <span data-ttu-id="b1e40-165">Pour les tableaux F #, utilisez le nom syntaxique `int[]` plutôt que `int array` ou `array<int>`.</span><span class="sxs-lookup"><span data-stu-id="b1e40-165">For F# arrays, use the syntactic name `int[]` rather than `int array` or `array<int>`.</span></span>
4. <span data-ttu-id="b1e40-166">Pour les cellules de référence, utilisez `int ref` plutôt que `ref<int>` ou `Ref<int>`.</span><span class="sxs-lookup"><span data-stu-id="b1e40-166">For Reference Cells, use `int ref` rather than `ref<int>` or `Ref<int>`.</span></span>

<span data-ttu-id="b1e40-167">Pour tous les autres types, utilisez la forme de préfixe.</span><span class="sxs-lookup"><span data-stu-id="b1e40-167">For all other types, use the prefix form.</span></span>

## <a name="formatting-tuples"></a><span data-ttu-id="b1e40-168">Mise en forme de tuples</span><span class="sxs-lookup"><span data-stu-id="b1e40-168">Formatting tuples</span></span>

<span data-ttu-id="b1e40-169">Une instanciation de tuple doit être entre parenthèses, et les virgules de délimitation dans doivent être suivies par un espace, par exemple : `(1, 2)`, `(x, y, z)`.</span><span class="sxs-lookup"><span data-stu-id="b1e40-169">A tuple instantiation should be parenthesized, and the delimiting commas within should be followed by a single space, for example: `(1, 2)`, `(x, y, z)`.</span></span>

<span data-ttu-id="b1e40-170">Il est généralement admis pour omettre les parenthèses dans les critères spéciaux de tuples :</span><span class="sxs-lookup"><span data-stu-id="b1e40-170">It is commonly accepted to omit parentheses in pattern matching of tuples:</span></span>

```fsharp
let (x, y) = z // Destructuring
let x, y = z // OK

// OK
match x, y with
| 1, _ -> 0
| x, 1 -> 0
| x, y -> 1
```

## <a name="formatting-discriminated-union-declarations"></a><span data-ttu-id="b1e40-171">Mise en forme discriminée des déclarations d’union</span><span class="sxs-lookup"><span data-stu-id="b1e40-171">Formatting discriminated union declarations</span></span>

<span data-ttu-id="b1e40-172">Mettre en retrait `|` dans la définition de type par des 4 espaces :</span><span class="sxs-lookup"><span data-stu-id="b1e40-172">Indent `|` in type definition by 4 spaces:</span></span>

```fsharp
// OK
type Volume =
    | Liter of float
    | FluidOunce of float
    | ImperialPint of float

// Not OK
type Volume =
| Liter of float
| USPint of float
| ImperialPint of float
```

## <a name="formatting-discriminated-unions"></a><span data-ttu-id="b1e40-173">Mise en forme des unions discriminées</span><span class="sxs-lookup"><span data-stu-id="b1e40-173">Formatting discriminated unions</span></span>

<span data-ttu-id="b1e40-174">Instancié Unions discriminées qui réparties sur plusieurs lignes doit fournir des données qu’il contient une nouvelle étendue avec la mise en retrait :</span><span class="sxs-lookup"><span data-stu-id="b1e40-174">Instantiated Discriminated Unions that split across multiple lines should give contained data a new scope with indentation:</span></span>

```fsharp
let tree1 =
    BinaryNode
        (BinaryNode(BinaryValue 1, BinaryValue 2),
         BinaryNode(BinaryValue 3, BinaryValue 4))
```

<span data-ttu-id="b1e40-175">La parenthèse fermante peut également être sur une nouvelle ligne :</span><span class="sxs-lookup"><span data-stu-id="b1e40-175">The closing parenthesis can also be on a new line:</span></span>

```fsharp
let tree1 =
    BinaryNode(
        BinaryNode(BinaryValue 1, BinaryValue 2),
        BinaryNode(BinaryValue 3, BinaryValue 4)
    )
```

## <a name="formatting-record-declarations"></a><span data-ttu-id="b1e40-176">Mise en forme de déclarations d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="b1e40-176">Formatting record declarations</span></span>

<span data-ttu-id="b1e40-177">Mettre en retrait `{` dans le type de définition par 4 espaces et démarrer la liste de champs sur la même ligne :</span><span class="sxs-lookup"><span data-stu-id="b1e40-177">Indent `{` in type definition by 4 spaces and start the field list on the same line:</span></span>

```fsharp
// OK
type PostalAddress =
    { Address: string
      City: string
      Zip: string }
    member x.ZipAndCity = sprintf "%s %s" x.Zip x.City

// Not OK
type PostalAddress =
  { Address: string
    City: string
    Zip: string }
    member x.ZipAndCity = sprintf "%s %s" x.Zip x.City
    
// Unusual in F#
type PostalAddress =
    { 
        Address: string
        City: string
        Zip: string
    }
```

<span data-ttu-id="b1e40-178">Le fait de placer le jeton d’ouverture sur la même ligne et le jeton de fermeture sur une nouvelle ligne consiste également, mais n’oubliez pas que vous devez utiliser le [syntaxe détaillée](../language-reference/verbose-syntax.md) pour définir les membres (le `with` mot clé) :</span><span class="sxs-lookup"><span data-stu-id="b1e40-178">Placing the opening token on the same line and the closing token on a new line is also fine, but be aware that you need to use the [verbose syntax](../language-reference/verbose-syntax.md) to define members (the `with` keyword):</span></span>

```fsharp
//  OK, but verbose syntax required
type PostalAddress = { 
    Address: string
    City: string
    Zip: string
} with
    member x.ZipAndCity = sprintf "%s %s" x.Zip x.City
```

## <a name="formatting-records"></a><span data-ttu-id="b1e40-179">Mise en forme d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="b1e40-179">Formatting records</span></span>

<span data-ttu-id="b1e40-180">Enregistrements courts peuvent être écrite sur une seule ligne :</span><span class="sxs-lookup"><span data-stu-id="b1e40-180">Short records can be written in one line:</span></span>

```fsharp
let point = { X = 1.0; Y = 0.0 }
```

<span data-ttu-id="b1e40-181">Les enregistrements qui sont plus longs doivent utiliser les nouvelles lignes pour les étiquettes :</span><span class="sxs-lookup"><span data-stu-id="b1e40-181">Records that are longer should use new lines for labels:</span></span>

```fsharp
let rainbow =
    { Boss = "Jeffrey"
      Lackeys = ["Zippy"; "George"; "Bungle"] }
```

<span data-ttu-id="b1e40-182">Le fait de placer le jeton d’ouverture sur la même ligne et le jeton de fermeture sur une nouvelle ligne est également correcte :</span><span class="sxs-lookup"><span data-stu-id="b1e40-182">Placing the opening token on the same line and the closing token on a new line is also fine:</span></span>

```fsharp
let rainbow = {
    Boss1 = "Jeffrey"
    Boss2 = "Jeffrey"
    Boss3 = "Jeffrey"
    Boss4 = "Jeffrey"
    Boss5 = "Jeffrey"
    Boss6 = "Jeffrey"
    Boss7 = "Jeffrey"
    Boss8 = "Jeffrey"
    Lackeys = ["Zippy"; "George"; "Bungle"]
}
```

<span data-ttu-id="b1e40-183">Les mêmes règles s’appliquent pour les éléments de liste et tableau.</span><span class="sxs-lookup"><span data-stu-id="b1e40-183">The same rules apply for list and array elements.</span></span>

## <a name="formatting-lists-and-arrays"></a><span data-ttu-id="b1e40-184">Mise en forme des listes et des tableaux</span><span class="sxs-lookup"><span data-stu-id="b1e40-184">Formatting lists and arrays</span></span>

<span data-ttu-id="b1e40-185">Écrire `x :: l` avec des espaces autour de la `::` opérateur (`::` est un opérateur infixe, par conséquent, entouré d’espaces) et `[1; 2; 3]` (`;` est un délimiteur, par conséquent, suivi d’un espace).</span><span class="sxs-lookup"><span data-stu-id="b1e40-185">Write `x :: l` with spaces around the `::` operator (`::` is an infix operator, hence surrounded by spaces) and `[1; 2; 3]` (`;` is a delimiter, hence followed by a space).</span></span>

<span data-ttu-id="b1e40-186">Utilisez toujours au moins un espace entre les deux opérateurs distincts de type accolade.</span><span class="sxs-lookup"><span data-stu-id="b1e40-186">Always use at least one space between two distinct brace-like operators.</span></span> <span data-ttu-id="b1e40-187">Par exemple, laissez un espace entre un `[` et un `{`.</span><span class="sxs-lookup"><span data-stu-id="b1e40-187">For example, leave a space between a `[` and a `{`.</span></span>

```fsharp
// OK
[ { IngredientName = "Green beans"; Quantity = 250 }
  { IngredientName = "Pine nuts"; Quantity = 250 }
  { IngredientName = "Feta cheese"; Quantity = 250 }
  { IngredientName = "Olive oil"; Quantity = 10 }
  { IngredientName = "Lemon"; Quantity = 1 } ]

// Not OK
[{ IngredientName = "Green beans"; Quantity = 250 }
 { IngredientName = "Pine nuts"; Quantity = 250 }
 { IngredientName = "Feta cheese"; Quantity = 250 }
 { IngredientName = "Olive oil"; Quantity = 10 }
 { IngredientName = "Lemon"; Quantity = 1 }]
```

<span data-ttu-id="b1e40-188">Listes et des tableaux réparties sur plusieurs lignes suivent une règle similaire comme enregistrements :</span><span class="sxs-lookup"><span data-stu-id="b1e40-188">Lists and arrays that split across multiple lines follow a similar rule as records do:</span></span>

```fsharp
let pascalsTriangle = [|
    [|1|]
    [|1; 1|]
    [|1; 2; 1|]
    [|1; 3; 3; 1|]
    [|1; 4; 6; 4; 1|]
    [|1; 5; 10; 10; 5; 1|]
    [|1; 6; 15; 20; 15; 6; 1|]
    [|1; 7; 21; 35; 35; 21; 7; 1|]
    [|1; 8; 28; 56; 70; 56; 28; 8; 1|]
|]
```

## <a name="formatting-if-expressions"></a><span data-ttu-id="b1e40-189">Mise en forme if expressions</span><span class="sxs-lookup"><span data-stu-id="b1e40-189">Formatting if expressions</span></span>

<span data-ttu-id="b1e40-190">Mise en retrait des instructions conditionnelles varie selon les tailles des expressions qui les composent.</span><span class="sxs-lookup"><span data-stu-id="b1e40-190">Indentation of conditionals depends on the sizes of the expressions that make them up.</span></span> <span data-ttu-id="b1e40-191">Si `cond`, `e1` et `e2` sont courtes, il vous suffit de les écrire sur une seule ligne :</span><span class="sxs-lookup"><span data-stu-id="b1e40-191">If `cond`, `e1` and `e2` are short, simply write them on one line:</span></span>

```fsharp
if cond then e1 else e2
```

<span data-ttu-id="b1e40-192">Si `cond`, `e1` ou `e2` sont plus de temps, mais pas plusieurs lignes :</span><span class="sxs-lookup"><span data-stu-id="b1e40-192">If either `cond`, `e1` or `e2` are longer, but not multi-line:</span></span>

```fsharp
if cond
then e1
else e2
```

<span data-ttu-id="b1e40-193">Si une des expressions est multiligne :</span><span class="sxs-lookup"><span data-stu-id="b1e40-193">If any of the expressions are multi-line:</span></span>

```fsharp
if cond then
    e1
else
    e2
```

<span data-ttu-id="b1e40-194">Plusieurs instructions conditionnelles avec `elif` et `else` sont mises en retrait dans la même étendue en tant que le `if`:</span><span class="sxs-lookup"><span data-stu-id="b1e40-194">Multiple conditionals with `elif` and `else` are indented at the same scope as the `if`:</span></span>

```fsharp
if cond1 then e1
elif cond2 then e2
elif cond3 then e3
else e4
```

### <a name="pattern-matching-constructs"></a><span data-ttu-id="b1e40-195">Constructions de correspondance de modèle</span><span class="sxs-lookup"><span data-stu-id="b1e40-195">Pattern matching constructs</span></span>

<span data-ttu-id="b1e40-196">Utilisez un `|` pour chaque clause d’une correspondance avec aucune mise en retrait.</span><span class="sxs-lookup"><span data-stu-id="b1e40-196">Use a `|` for each clause of a match with no indentation.</span></span> <span data-ttu-id="b1e40-197">Si l’expression est courte, vous pouvez envisager d’utiliser une seule ligne si chaque sous-expression est également simple.</span><span class="sxs-lookup"><span data-stu-id="b1e40-197">If the expression is short, you can consider using a single line if each subexpression is also simple.</span></span>

```fsharp
// OK
match l with
| { him = x; her = "Posh" } :: tail -> _
| _ :: tail -> findDavid tail
| [] -> failwith "Couldn't find David"

// Not OK
match l with
    | { him = x; her = "Posh" } :: tail -> _
    | _ :: tail -> findDavid tail
    | [] -> failwith "Couldn't find David"
```

<span data-ttu-id="b1e40-198">Si l’expression à droite de la flèche de critères spéciaux est trop volumineuse, déplacez-le vers la ligne suivante, mis en retrait d’une seule étape à partir de la `match` / `|`.</span><span class="sxs-lookup"><span data-stu-id="b1e40-198">If the expression on the right of the pattern matching arrow is too large, move it to the following line, indented one step from the `match`/`|`.</span></span>

```fsharp
match lam with
| Var v -> 1
| Abs(x, body) ->
    1 + sizeLambda body
| App(lam1, lam2) ->
    sizeLambda lam1 + sizeLambda lam2

```

<span data-ttu-id="b1e40-199">Filtre de correspondance de fonctions anonymes, en commençant par `function`, doit généralement pas mettre en retrait trop loin.</span><span class="sxs-lookup"><span data-stu-id="b1e40-199">Pattern matching of anonymous functions, starting by `function`, should generally not indent too far.</span></span> <span data-ttu-id="b1e40-200">Par exemple, il est bien de mise en retrait d’une étendue comme suit :</span><span class="sxs-lookup"><span data-stu-id="b1e40-200">For example, indenting one scope as follows is fine:</span></span>

```fsharp
lambdaList
|> List.map (function
    | Abs(x, body) -> 1 + sizeLambda 0 body
    | App(lam1, lam2) -> sizeLambda (sizeLambda 0 lam1) lam2
    | Var v -> 1)
```

<span data-ttu-id="b1e40-201">Critères spéciaux dans les fonctions définies par `let` ou `let rec` doit être mis en retrait 4 espaces après le démarrage de `let`, même si `function` mot clé est utilisé :</span><span class="sxs-lookup"><span data-stu-id="b1e40-201">Pattern matching in functions defined by `let` or `let rec` should be indented 4 spaces after starting of `let`, even if `function` keyword is used:</span></span>

```fsharp
let rec sizeLambda acc = function
    | Abs(x, body) -> sizeLambda (succ acc) body
    | App(lam1, lam2) -> sizeLambda (sizeLambda acc lam1) lam2
    | Var v -> succ acc
```

<span data-ttu-id="b1e40-202">Nous vous déconseillons d’alignement des flèches.</span><span class="sxs-lookup"><span data-stu-id="b1e40-202">We do not recommend aligning arrows.</span></span>

## <a name="formatting-trywith-expressions"></a><span data-ttu-id="b1e40-203">Mise en forme try / with expressions</span><span class="sxs-lookup"><span data-stu-id="b1e40-203">Formatting try/with expressions</span></span>

<span data-ttu-id="b1e40-204">Critères spéciaux sur le type d’exception doit être mis en retrait au même niveau que `with`.</span><span class="sxs-lookup"><span data-stu-id="b1e40-204">Pattern matching on the exception type should be indented at the same level as `with`.</span></span>

```fsharp
try
    if System.DateTime.Now.Second % 3 = 0 then
        raise (new System.Exception())
    else
        raise (new System.ApplicationException())
with
| :? System.ApplicationException ->
    printfn "A second that was not a multiple of 3"
| _ ->
    printfn "A second that was a multiple of 3"
```

## <a name="formatting-function-parameter-application"></a><span data-ttu-id="b1e40-205">Mise en forme d’application de paramètre de fonction</span><span class="sxs-lookup"><span data-stu-id="b1e40-205">Formatting function parameter application</span></span>

<span data-ttu-id="b1e40-206">En règle générale, la plupart des applications de paramètre de fonction sont effectuée sur la même ligne.</span><span class="sxs-lookup"><span data-stu-id="b1e40-206">In general, most function parameter application is done on the same line.</span></span>

<span data-ttu-id="b1e40-207">Si vous souhaitez appliquer des paramètres à une fonction sur une nouvelle ligne, mettre en retrait les par une étendue.</span><span class="sxs-lookup"><span data-stu-id="b1e40-207">If you wish to apply parameters to a function on a new line, indent them by one scope.</span></span>

```fsharp
// OK
sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity

// OK
sprintf
     "\t%s - %i\n\r"
     x.IngredientName x.Quantity

// OK
let printVolumes x =
    printf "Volume in liters = %f, in us pints = %f, in imperial = %f"
        (convertVolumeToLiter x)
        (convertVolumeUSPint x)
        (convertVolumeImperialPint x)
```

<span data-ttu-id="b1e40-208">Les mêmes règles s’appliquent pour les expressions lambda en tant qu’arguments de fonction.</span><span class="sxs-lookup"><span data-stu-id="b1e40-208">The same guidelines apply for lambda expressions as function arguments.</span></span> <span data-ttu-id="b1e40-209">Si le corps d’une expression lambda, le corps peut avoir une autre ligne, la mise en retrait par une étendue</span><span class="sxs-lookup"><span data-stu-id="b1e40-209">If the body of a lambda expression, the body can have another line, indented by one scope</span></span>

```fsharp
let printListWithOffset a list1 =
    List.iter
        (fun elem -> printfn "%d" (a + elem))
        list1

// OK if lambda body is long enough
let printListWithOffset a list1 =
    List.iter
        (fun elem ->
            printfn "%d" (a + elem))
        list1
```

<span data-ttu-id="b1e40-210">Toutefois, si le corps d’une expression lambda est plusieurs lignes, envisagez factorisant dans une fonction distincte plutôt que d’avoir une construction multiligne appliquée en tant qu’un seul argument à une fonction.</span><span class="sxs-lookup"><span data-stu-id="b1e40-210">However, if the body of a lambda expression is more than one line, consider factoring it out into a separate function rather than have a multi-line construct applied as a single argument to a function.</span></span>

### <a name="formatting-infix-operators"></a><span data-ttu-id="b1e40-211">Opérateurs infixes mise en forme</span><span class="sxs-lookup"><span data-stu-id="b1e40-211">Formatting infix operators</span></span>

<span data-ttu-id="b1e40-212">Opérateurs distincts par des espaces.</span><span class="sxs-lookup"><span data-stu-id="b1e40-212">Separate operators by spaces.</span></span> <span data-ttu-id="b1e40-213">Exceptions évident à cette règle sont les `!` et `.` opérateurs.</span><span class="sxs-lookup"><span data-stu-id="b1e40-213">Obvious exceptions to this rule are the `!` and `.` operators.</span></span>

<span data-ttu-id="b1e40-214">Expressions de correspondance des infixes sont OK pour l’alignement sur la même colonne :</span><span class="sxs-lookup"><span data-stu-id="b1e40-214">Infix expressions are OK to lineup on same column:</span></span>

```fsharp
acc +
(sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity)

let function1 arg1 arg2 arg3 arg4 =
    arg1 + arg2 +
    arg3 + arg4
```

### <a name="formatting-pipeline-operators"></a><span data-ttu-id="b1e40-215">Mise en forme des opérateurs de pipeline</span><span class="sxs-lookup"><span data-stu-id="b1e40-215">Formatting pipeline operators</span></span>

<span data-ttu-id="b1e40-216">Pipeline `|>` opérateurs doivent figurer sous elles opèrent selon des expressions.</span><span class="sxs-lookup"><span data-stu-id="b1e40-216">Pipeline `|>` operators should go underneath the expressions they operate on.</span></span>

```fsharp
// Preferred approach
let methods2 =
    System.AppDomain.CurrentDomain.GetAssemblies()
    |> List.ofArray
    |> List.map (fun assm -> assm.GetTypes())
    |> Array.concat
    |> List.ofArray
    |> List.map (fun t -> t.GetMethods())
    |> Array.concat

// Not OK
let methods2 = System.AppDomain.CurrentDomain.GetAssemblies()
            |> List.ofArray
            |> List.map (fun assm -> assm.GetTypes())
            |> Array.concat
            |> List.ofArray
            |> List.map (fun t -> t.GetMethods())
            |> Array.concat
```

### <a name="formatting-modules"></a><span data-ttu-id="b1e40-217">Mise en forme de modules</span><span class="sxs-lookup"><span data-stu-id="b1e40-217">Formatting modules</span></span>

<span data-ttu-id="b1e40-218">Code dans un module local doit être mis en retrait par rapport au module, mais le code dans un module de niveau supérieur ne doit pas être mis en retrait.</span><span class="sxs-lookup"><span data-stu-id="b1e40-218">Code in a local module must be indented relative to the module, but code in a top-level module should not be indented.</span></span> <span data-ttu-id="b1e40-219">Les éléments Namespace n’ont pas à être mis en retrait.</span><span class="sxs-lookup"><span data-stu-id="b1e40-219">Namespace elements do not have to be indented.</span></span>

```fsharp
// A is a top-level module.
module A

let function1 a b = a - b * b
```

```fsharp
// A1 and A2 are local modules.
module A1 =
    let function1 a b = a*a + b*b

module A2 =
    let function2 a b = a*a - b*b
```

### <a name="formatting-object-expressions-and-interfaces"></a><span data-ttu-id="b1e40-220">Mise en forme d’expressions d’objet et des interfaces</span><span class="sxs-lookup"><span data-stu-id="b1e40-220">Formatting object expressions and interfaces</span></span>

<span data-ttu-id="b1e40-221">Expressions d’objet et les interfaces doivent être alignées dans la même façon avec `member` en cours de mise en retrait après 4 espaces.</span><span class="sxs-lookup"><span data-stu-id="b1e40-221">Object expressions and interfaces should be aligned in the same way with `member` being indented after 4 spaces.</span></span>

```fsharp
let comparer =
    { new IComparer<string> with
          member x.Compare(s1, s2) =
              let rev (s : String) =
                  new String (Array.rev (s.ToCharArray()))
              let reversed = rev s1
              reversed.CompareTo (rev s2) }
```

### <a name="formatting-white-space-in-expressions"></a><span data-ttu-id="b1e40-222">Mise en forme des espaces blancs dans les expressions</span><span class="sxs-lookup"><span data-stu-id="b1e40-222">Formatting white space in expressions</span></span>

<span data-ttu-id="b1e40-223">Évitez les espaces superflus dans les expressions F #.</span><span class="sxs-lookup"><span data-stu-id="b1e40-223">Avoid extraneous white space in F# expressions.</span></span>

```fsharp
// OK
spam (ham.[1])

// Not OK
spam ( ham.[ 1 ] )
```

<span data-ttu-id="b1e40-224">Arguments nommés doivent avoir également pas espace entourant le `=`:</span><span class="sxs-lookup"><span data-stu-id="b1e40-224">Named arguments should also not have space surrounding the `=`:</span></span>

```fsharp
// OK
let makeStreamReader x = new System.IO.StreamReader(path=x)

// Not OK
let makeStreamReader x = new System.IO.StreamReader(path = x)
```
