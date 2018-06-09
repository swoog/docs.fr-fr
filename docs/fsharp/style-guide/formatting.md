---
title: 'Les instructions de mise en forme de code F #'
description: 'Découvrez les instructions de mise en forme du code F #.'
ms.date: 05/14/2018
ms.openlocfilehash: 6c8e4059fd4bf1e7450118a6df02609217c4f4db
ms.sourcegitcommit: 2ad7d06f4f469b5d8a5280ac0e0289a81867fc8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2018
ms.locfileid: "35231504"
---
# <a name="f-code-formatting-guidelines"></a><span data-ttu-id="50215-103">Les instructions de mise en forme de code F #</span><span class="sxs-lookup"><span data-stu-id="50215-103">F# code formatting guidelines</span></span>

<span data-ttu-id="50215-104">Cet article propose des recommandations pour la mise en forme votre code afin que votre code F # est :</span><span class="sxs-lookup"><span data-stu-id="50215-104">This article offers guidelines for how to format your code so that your F# code is:</span></span>

* <span data-ttu-id="50215-105">Généralement affichées comme plus lisibles</span><span class="sxs-lookup"><span data-stu-id="50215-105">Generally viewed as more legible</span></span>
* <span data-ttu-id="50215-106">Est conformément aux conventions appliquées par les outils dans Visual Studio et autres éditeurs de mise en forme</span><span class="sxs-lookup"><span data-stu-id="50215-106">Is in accordance with conventions applied by formatting tools in Visual Studio and other editors</span></span>
* <span data-ttu-id="50215-107">Similaire à un autre code en ligne</span><span class="sxs-lookup"><span data-stu-id="50215-107">Similar to other code online</span></span>

<span data-ttu-id="50215-108">Ces instructions sont basées sur [un guide complet sur les Conventions de mise en forme F #](https://github.com/dungpa/fantomas/blob/master/docs/FormattingConventions.md) par [Anh-fumier Phan](https://github.com/dungpa).</span><span class="sxs-lookup"><span data-stu-id="50215-108">These guidelines are based on [A comprehensive guide to F# Formatting Conventions](https://github.com/dungpa/fantomas/blob/master/docs/FormattingConventions.md) by [Anh-Dung Phan](https://github.com/dungpa).</span></span>

## <a name="general-rules-for-indentation"></a><span data-ttu-id="50215-109">Règles générales pour la mise en retrait</span><span class="sxs-lookup"><span data-stu-id="50215-109">General rules for indentation</span></span>

<span data-ttu-id="50215-110">F # utilise un espace blanc significatif par défaut.</span><span class="sxs-lookup"><span data-stu-id="50215-110">F# uses significant whitespace by default.</span></span> <span data-ttu-id="50215-111">Les instructions suivantes sont destinées à fournir des conseils sur la manière de jongler avec des défis que cela peut imposer.</span><span class="sxs-lookup"><span data-stu-id="50215-111">The following guidelines are intended to provide guidance as to how to juggle some challenges this can impose.</span></span>

### <a name="using-spaces"></a><span data-ttu-id="50215-112">L’utilisation des espaces</span><span class="sxs-lookup"><span data-stu-id="50215-112">Using spaces</span></span>

<span data-ttu-id="50215-113">Lors de la mise en retrait est requise, vous devez utiliser des espaces, tabulations pas.</span><span class="sxs-lookup"><span data-stu-id="50215-113">When indentation is required, you must use spaces, not tabs.</span></span> <span data-ttu-id="50215-114">Au moins un espace est requis.</span><span class="sxs-lookup"><span data-stu-id="50215-114">At least one space is required.</span></span> <span data-ttu-id="50215-115">Votre organisation peut créer des normes de codage pour spécifier le nombre d’espaces à utiliser pour la mise en retrait ; deux, trois ou quatre espaces de mise en retrait à chaque niveau de mise en retrait est typique.</span><span class="sxs-lookup"><span data-stu-id="50215-115">Your organization can create coding standards to specify the number of spaces to use for indentation; two, three or four spaces of indentation at each level where indentation occurs is typical.</span></span>

<span data-ttu-id="50215-116">**Nous vous recommandons 4 espaces par mise en retrait.**</span><span class="sxs-lookup"><span data-stu-id="50215-116">**We recommend 4 spaces per indentation.**</span></span>

<span data-ttu-id="50215-117">Ceci dit, la mise en retrait des programmes est une question subjective.</span><span class="sxs-lookup"><span data-stu-id="50215-117">That said, indentation of programs is a subjective matter.</span></span> <span data-ttu-id="50215-118">Variations sont OK, mais la première règle, vous devez suivre est *la cohérence de la mise en retrait*.</span><span class="sxs-lookup"><span data-stu-id="50215-118">Variations are OK, but the first rule you should follow is *consistency of indentation*.</span></span> <span data-ttu-id="50215-119">Choisissez un style de mise en retrait de généralement accepté et utiliser systématiquement dans l’ensemble de votre code base.</span><span class="sxs-lookup"><span data-stu-id="50215-119">Choose a generally accepted style of indentation and use it systematically throughout your codebase.</span></span>

## <a name="formatting-blank-lines"></a><span data-ttu-id="50215-120">Mise en forme des lignes vides</span><span class="sxs-lookup"><span data-stu-id="50215-120">Formatting blank lines</span></span>

* <span data-ttu-id="50215-121">Distinct niveau supérieur (fonction) et la classe définitions avec deux lignes vides.</span><span class="sxs-lookup"><span data-stu-id="50215-121">Separate top-level function and class definitions with two blank lines.</span></span>
* <span data-ttu-id="50215-122">Les définitions de méthode à l’intérieur d’une classe sont séparées par une ligne vide.</span><span class="sxs-lookup"><span data-stu-id="50215-122">Method definitions inside a class are separated by a single blank line.</span></span>
* <span data-ttu-id="50215-123">Lignes vierges supplémentaires peuvent servir (avec parcimonie) pour séparer les groupes de fonctions connexes.</span><span class="sxs-lookup"><span data-stu-id="50215-123">Extra blank lines may be used (sparingly) to separate groups of related functions.</span></span> <span data-ttu-id="50215-124">Lignes vides peuvent être omises entre un ensemble de commandes associées à une ligne (par exemple, un ensemble d’implémentations fictives).</span><span class="sxs-lookup"><span data-stu-id="50215-124">Blank lines may be omitted between a bunch of related one-liners (for example, a set of dummy implementations).</span></span>
* <span data-ttu-id="50215-125">Utiliser avec parcimonie lignes vides dans les fonctions, pour indiquer les sections logiques.</span><span class="sxs-lookup"><span data-stu-id="50215-125">Use blank lines in functions, sparingly, to indicate logical sections.</span></span>

## <a name="formatting-comments"></a><span data-ttu-id="50215-126">Mise en forme de commentaires</span><span class="sxs-lookup"><span data-stu-id="50215-126">Formatting comments</span></span>

<span data-ttu-id="50215-127">Préférez généralement plusieurs commentaires double barre oblique sur les commentaires en bloc style ML.</span><span class="sxs-lookup"><span data-stu-id="50215-127">Generally prefer multiple double-slash comments over ML-style block comments.</span></span>

```fsharp
// Prefer this style of comments when you want
// to express written ideas on multiple lines.

(*
    ML-style comments are fine, but not a .NET-ism.
    They are useful when needing to modify multi-line comments, though.
*)
```

<span data-ttu-id="50215-128">Commentaires incorporés doivent mettre en majuscule la première lettre.</span><span class="sxs-lookup"><span data-stu-id="50215-128">Inline comments should capitalize the first letter.</span></span>

```fsharp
let f x = x + 1 // Increment by one.
```

## <a name="naming-conventions"></a><span data-ttu-id="50215-129">Conventions d'attribution d'un nom</span><span class="sxs-lookup"><span data-stu-id="50215-129">Naming conventions</span></span>

### <a name="use-camelcase-for-class-bound-expression-bound-and-pattern-bound-values-and-functions"></a><span data-ttu-id="50215-130">Utilisez camelCase pour les fonctions et les valeurs de limite de classe, expression-modèle liées et</span><span class="sxs-lookup"><span data-stu-id="50215-130">Use camelCase for class-bound, expression-bound and pattern-bound values and functions</span></span>

<span data-ttu-id="50215-131">Il est courant et acceptée style F # à utiliser camelCase pour tous les noms lié en tant que variables locales ou dans les correspondances de modèle et les définitions de fonction.</span><span class="sxs-lookup"><span data-stu-id="50215-131">It is common and accepted F# style to use camelCase for all names bound as local variables or in pattern matches and function definitions.</span></span>

```fsharp
// OK
let addIAndJ i j = i + j

// Bad
let addIAndJ I J = I+J

// Bad
let AddIAndJ i j = i + j
```

<span data-ttu-id="50215-132">Fonctions liées au localement dans les classes doivent également utiliser camelCase.</span><span class="sxs-lookup"><span data-stu-id="50215-132">Locally-bound functions in classes should also use camelCase.</span></span>

```fsharp
type MyClass() =

    let doSomething () =

    let firstResult = ...

    let secondResult = ...

    member x.Result = doSomething()
```

### <a name="use-camelcase-for-module-bound-public-functions"></a><span data-ttu-id="50215-133">Utilisez camelCase pour les fonctions liées au module public</span><span class="sxs-lookup"><span data-stu-id="50215-133">Use camelCase for module-bound public functions</span></span>

<span data-ttu-id="50215-134">Lorsqu’une fonction liée au module fait partie d’une API publique, il doit utiliser camelCase :</span><span class="sxs-lookup"><span data-stu-id="50215-134">When a module-bound function is part of a public API, it should use camelCase:</span></span>

```fsharp
module MyAPI =
    let publicFunctionOne param1 param2 param2 = ...

    let publicFunctionTwo param1 param2 param3 = ...
```

### <a name="use-camelcase-for-internal-and-private-module-bound-values-and-functions"></a><span data-ttu-id="50215-135">Utilisez camelCase pour les fonctions et les valeurs liées au module internes et privés</span><span class="sxs-lookup"><span data-stu-id="50215-135">Use camelCase for internal and private module-bound values and functions</span></span>

<span data-ttu-id="50215-136">Utilisez camelCase pour des valeurs liées au module privées, notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="50215-136">Use camelCase for private module-bound values, including the following:</span></span>

* <span data-ttu-id="50215-137">Les fonctions ad hoc dans les scripts</span><span class="sxs-lookup"><span data-stu-id="50215-137">Ad hoc functions in scripts</span></span>

* <span data-ttu-id="50215-138">Valeurs constituant l’implémentation interne de type ou module</span><span class="sxs-lookup"><span data-stu-id="50215-138">Values making up the internal implementation of a module or type</span></span>

```fsharp
let emailMyBossTheLatestResults =
    ...
```

### <a name="use-camelcase-for-parameters"></a><span data-ttu-id="50215-139">Utilisez camelCase pour les paramètres</span><span class="sxs-lookup"><span data-stu-id="50215-139">Use camelCase for parameters</span></span>

<span data-ttu-id="50215-140">Tous les paramètres doivent utiliser camelCase conformément aux conventions d’affectation de noms de .NET.</span><span class="sxs-lookup"><span data-stu-id="50215-140">All parameters should use camelCase in accordance with .NET naming conventions.</span></span>

```fsharp
module MyModule =
    let myFunction paramOne paramTwo = ...

type MyClass() =
    member this.MyMethod(paramOne, paramTwo) = ...
```

### <a name="use-pascalcase-for-modules"></a><span data-ttu-id="50215-141">Utiliser PascalCase pour les modules</span><span class="sxs-lookup"><span data-stu-id="50215-141">Use PascalCase for modules</span></span>

<span data-ttu-id="50215-142">Tous les modules (niveau supérieur, internes, privés, imbriquées) doivent utiliser PascalCase.</span><span class="sxs-lookup"><span data-stu-id="50215-142">All modules (top-level, internal, private, nested) should use PascalCase.</span></span>

```fsharp
module MyTopLevelModule

module Helpers =
    module private SuperHelpers =
        ...

    ...
```

### <a name="use-pascalcase-for-type-declarations-members-and-labels"></a><span data-ttu-id="50215-143">Utilisez PascalCase pour les étiquettes, les membres et les déclarations de type</span><span class="sxs-lookup"><span data-stu-id="50215-143">Use PascalCase for type declarations, members, and labels</span></span>

<span data-ttu-id="50215-144">Classes, interfaces, structures, énumérations, délégués, les enregistrements et les unions discriminées doivent être nommées avec PascalCase.</span><span class="sxs-lookup"><span data-stu-id="50215-144">Classes, interfaces, structs, enumerations, delegates, records, and discriminated unions should all be named with PascalCase.</span></span> <span data-ttu-id="50215-145">Les membres dans les types et les étiquettes pour les enregistrements et les unions discriminées doivent également utiliser PascalCase.</span><span class="sxs-lookup"><span data-stu-id="50215-145">Members within types and labels for records and discriminated unions should also use PascalCase.</span></span>

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

### <a name="use-pascalcase-for-constructs-intrinsic-to-net"></a><span data-ttu-id="50215-146">Utilisez PascalCase pour les constructions intrinsèques pour .NET</span><span class="sxs-lookup"><span data-stu-id="50215-146">Use PascalCase for constructs intrinsic to .NET</span></span>

<span data-ttu-id="50215-147">Espaces de noms, exceptions, événements et le projet /`.dll` noms doivent également utiliser PascalCase.</span><span class="sxs-lookup"><span data-stu-id="50215-147">Namespaces, exceptions, events, and project/`.dll` names should also use PascalCase.</span></span> <span data-ttu-id="50215-148">N’est pas seulement cela rend la consommation à partir d’autres langages .NET semble plus naturel aux consommateurs, il est également cohérent avec les conventions d’affectation de noms .NET que vous êtes susceptible de rencontrer.</span><span class="sxs-lookup"><span data-stu-id="50215-148">Not only does this make consumption from other .NET languages feel more natural to consumers, it's also consistent with .NET naming conventions that you are likely to encounter.</span></span>

### <a name="avoid-underscores-in-names"></a><span data-ttu-id="50215-149">Éviter les traits de soulignement dans les noms</span><span class="sxs-lookup"><span data-stu-id="50215-149">Avoid underscores in names</span></span>

<span data-ttu-id="50215-150">Historiquement, certaines bibliothèques F # ont utilisé des traits de soulignement dans les noms.</span><span class="sxs-lookup"><span data-stu-id="50215-150">Historically, some F# libraries have used underscores in names.</span></span> <span data-ttu-id="50215-151">Toutefois, cela est n’est plus largement accepté, car il est en conflit avec les conventions d’affectation de noms .NET.</span><span class="sxs-lookup"><span data-stu-id="50215-151">However, this is no longer widely accepted, partly because it clashes with .NET naming conventions.</span></span> <span data-ttu-id="50215-152">Ceci dit, certains programmeurs F # utilisent des traits de soulignement importante, en partie pour des raisons historiques, et la tolérance de panne et de respect est important.</span><span class="sxs-lookup"><span data-stu-id="50215-152">That said, some F# programmers use underscores heavily, partly for historical reasons, and tolerance and respect is important.</span></span> <span data-ttu-id="50215-153">Toutefois, sachez que le style est souvent disliked par d’autres personnes ont la possibilité d’utiliser.</span><span class="sxs-lookup"><span data-stu-id="50215-153">However, be aware that the style is often disliked by others who have a choice about whether to use it.</span></span>

<span data-ttu-id="50215-154">Certaines exceptions inclut l’interopérabilité avec des composants natifs, où des traits de soulignement sont très courantes.</span><span class="sxs-lookup"><span data-stu-id="50215-154">Some exceptions includes interoperating with native components, where underscores are very common.</span></span>

### <a name="use-standard-f-operators"></a><span data-ttu-id="50215-155">Utilisez les opérateurs standard F #</span><span class="sxs-lookup"><span data-stu-id="50215-155">Use standard F# operators</span></span>

<span data-ttu-id="50215-156">Les opérateurs suivants sont définis dans la bibliothèque standard) (F # et doivent être utilisées au lieu de définir des équivalents.</span><span class="sxs-lookup"><span data-stu-id="50215-156">The following operators are defined in the F# standard library and should be used instead of defining equivalents.</span></span> <span data-ttu-id="50215-157">L’utilisation de ces opérateurs est recommandée car il a tendance à rendre le code plus lisible et idiomatique.</span><span class="sxs-lookup"><span data-stu-id="50215-157">Using these operators is recommended as it tends to make code more readable and idiomatic.</span></span> <span data-ttu-id="50215-158">Les développeurs avec un arrière-plan dans OCaml ou autre langage de programmation fonctionnelle peuvent être habitués à différents langages.</span><span class="sxs-lookup"><span data-stu-id="50215-158">Developers with a background in OCaml or other functional programming language may be accustomed to different idioms.</span></span> <span data-ttu-id="50215-159">La liste suivante résume les opérateurs F # recommandées.</span><span class="sxs-lookup"><span data-stu-id="50215-159">The following list summarizes the recommended F# operators.</span></span>

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

### <a name="use-prefix-syntax-for-generics-foot-in-preference-to-postfix-syntax-t-foo"></a><span data-ttu-id="50215-160">Utilisez la syntaxe de préfixe des génériques (`Foo<T>`), plutôt que la syntaxe de suffixe (`T Foo`)</span><span class="sxs-lookup"><span data-stu-id="50215-160">Use prefix syntax for generics (`Foo<T>`) in preference to postfix syntax (`T Foo`)</span></span>

<span data-ttu-id="50215-161">F # hérite à la fois le style de ML suffixée des noms de types génériques (par exemple, `int list`), ainsi que le préfixe style .NET (par exemple, `list<int>`).</span><span class="sxs-lookup"><span data-stu-id="50215-161">F# inherits both the postfix ML style of naming generic types (for example, `int list`) as well as the prefix .NET style (for example, `list<int>`).</span></span> <span data-ttu-id="50215-162">Préférez le style de .NET, à l’exception des quatre types spécifiques :</span><span class="sxs-lookup"><span data-stu-id="50215-162">Prefer the .NET style, except for four specific types:</span></span>

1. <span data-ttu-id="50215-163">Pour F # les listes, utilisez la forme suffixée : `int list` plutôt que `list<int>`.</span><span class="sxs-lookup"><span data-stu-id="50215-163">For F# Lists, use the postfix form: `int list` rather than `list<int>`.</span></span>
2. <span data-ttu-id="50215-164">Pour les Options F #, utilisez la forme suffixée : `int option` plutôt que `option<int>`.</span><span class="sxs-lookup"><span data-stu-id="50215-164">For F# Options, use the postfix form: `int option` rather than `option<int>`.</span></span>
3. <span data-ttu-id="50215-165">Pour les tableaux F #, utilisez le nom syntaxique `int[]` plutôt que `int array` ou `array<int>`.</span><span class="sxs-lookup"><span data-stu-id="50215-165">For F# arrays, use the syntactic name `int[]` rather than `int array` or `array<int>`.</span></span>
4. <span data-ttu-id="50215-166">Pour les cellules de référence, utilisez `int ref` plutôt que `ref<int>` ou `Ref<int>`.</span><span class="sxs-lookup"><span data-stu-id="50215-166">For Reference Cells, use `int ref` rather than `ref<int>` or `Ref<int>`.</span></span>

<span data-ttu-id="50215-167">Pour tous les autres types, utilisez le format de préfixe.</span><span class="sxs-lookup"><span data-stu-id="50215-167">For all other types, use the prefix form.</span></span>

## <a name="formatting-discriminated-union-declarations"></a><span data-ttu-id="50215-168">Mise en forme discriminée déclarations d’union</span><span class="sxs-lookup"><span data-stu-id="50215-168">Formatting discriminated union declarations</span></span>

<span data-ttu-id="50215-169">Mettre en retrait `|` dans la définition de type par 4 espaces :</span><span class="sxs-lookup"><span data-stu-id="50215-169">Indent `|` in type definition by 4 spaces:</span></span>

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

<span data-ttu-id="50215-170">Instancié Unions discriminées réparties sur plusieurs lignes doit fournir des données qu’ils contiennent une nouvelle étendue avec mise en retrait :</span><span class="sxs-lookup"><span data-stu-id="50215-170">Instantiated Discriminated Unions that split across multiple lines should give contained data a new scope with indentation:</span></span>

```fsharp
let tree1 =
    BinaryNode
        (BinaryNode(BinaryValue 1, BinaryValue 2),
         BinaryNode(BinaryValue 3, BinaryValue 4))
```

<span data-ttu-id="50215-171">La parenthèse fermante peut également être sur une nouvelle ligne :</span><span class="sxs-lookup"><span data-stu-id="50215-171">The closing parenthesis can also be on a new line:</span></span>

```fsharp
let tree1 =
    BinaryNode(
        BinaryNode(BinaryValue 1, BinaryValue 2),
        BinaryNode(BinaryValue 3, BinaryValue 4)
    )
```

## <a name="formatting-tuples"></a><span data-ttu-id="50215-172">Mise en forme des tuples</span><span class="sxs-lookup"><span data-stu-id="50215-172">Formatting tuples</span></span>

<span data-ttu-id="50215-173">Une instanciation de tuple doit être entre parenthèses et les virgules de délimitation dans doivent être suivis par un espace, par exemple : `(1, 2)`, `(x, y, z)`.</span><span class="sxs-lookup"><span data-stu-id="50215-173">A tuple instantiation should be parenthesized, and the delimiting commas within should be followed by a single space, for example: `(1, 2)`, `(x, y, z)`.</span></span>

<span data-ttu-id="50215-174">Une exception couramment acceptée est d’omettre les parenthèses dans les critères spéciaux de tuples :</span><span class="sxs-lookup"><span data-stu-id="50215-174">A commonly accepted exception is to omit parentheses in pattern matching of tuples:</span></span>

```fsharp
let (x, y) = z // Destructuring

match x, y with
| 1, _ -> 0
| x, 1 -> 0
| x, y -> 1
```

## <a name="formatting-records"></a><span data-ttu-id="50215-175">Mise en forme des enregistrements</span><span class="sxs-lookup"><span data-stu-id="50215-175">Formatting records</span></span>

<span data-ttu-id="50215-176">Enregistrements courts peuvent être écrites dans une seule ligne :</span><span class="sxs-lookup"><span data-stu-id="50215-176">Short records can be written in one line:</span></span>

```fsharp
let point = { X = 1.0; Y = 0.0 }
```

<span data-ttu-id="50215-177">Les enregistrements qui sont plus longs doivent utiliser les nouvelles lignes pour les étiquettes :</span><span class="sxs-lookup"><span data-stu-id="50215-177">Records that are longer should use new lines for labels:</span></span>

```fsharp
let rainbow =
    { Boss = "Jeffrey"
      Lackeys = ["Zippy"; "George"; "Bungle"] }
```

<span data-ttu-id="50215-178">Placer le jeton d’ouverture sur la même ligne et le jeton de fermeture sur une nouvelle ligne est également correct :</span><span class="sxs-lookup"><span data-stu-id="50215-178">Placing the opening token on the same line and the closing token on a new line is also fine:</span></span>

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

<span data-ttu-id="50215-179">Les mêmes règles s’appliquent pour les éléments de liste et tableau.</span><span class="sxs-lookup"><span data-stu-id="50215-179">The same rules apply for list and array elements.</span></span>

## <a name="formatting-lists-and-arrays"></a><span data-ttu-id="50215-180">Mise en forme de listes et des tableaux</span><span class="sxs-lookup"><span data-stu-id="50215-180">Formatting lists and arrays</span></span>

<span data-ttu-id="50215-181">Écrire `x :: l` avec les espaces autour de le `::` (opérateur) (`::` est un opérateur infixe, par conséquent, entouré par des espaces) et `[1; 2; 3]` (`;` est un délimiteur, par conséquent, suivi d’un espace).</span><span class="sxs-lookup"><span data-stu-id="50215-181">Write `x :: l` with spaces around the `::` operator (`::` is an infix operator, hence surrounded by spaces) and `[1; 2; 3]` (`;` is a delimiter, hence followed by a space).</span></span>

<span data-ttu-id="50215-182">Utilisez toujours au moins un espace entre les deux opérateurs accolade de type distincts.</span><span class="sxs-lookup"><span data-stu-id="50215-182">Always use at least one space between two distinct brace-like operators.</span></span> <span data-ttu-id="50215-183">Par exemple, laissez un espace entre un `[` et un `{`.</span><span class="sxs-lookup"><span data-stu-id="50215-183">For example, leave a space between a `[` and a `{`.</span></span>

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

<span data-ttu-id="50215-184">Listes et aux tableaux réparties sur plusieurs lignes respecte une règle similaire comme enregistrements :</span><span class="sxs-lookup"><span data-stu-id="50215-184">Lists and arrays that split across multiple lines follow a similar rule as records do:</span></span>

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

## <a name="formatting-if-expressions"></a><span data-ttu-id="50215-185">Mise en forme if expressions</span><span class="sxs-lookup"><span data-stu-id="50215-185">Formatting if expressions</span></span>

<span data-ttu-id="50215-186">Mise en retrait des éléments conditionnels varie selon les tailles des expressions qui les composent.</span><span class="sxs-lookup"><span data-stu-id="50215-186">Indentation of conditionals depends on the sizes of the expressions that make them up.</span></span> <span data-ttu-id="50215-187">Si `cond`, `e1` et `e2` sont petites, il vous suffit de les écrire sur une seule ligne :</span><span class="sxs-lookup"><span data-stu-id="50215-187">If `cond`, `e1` and `e2` are small, simply write them on one line:</span></span>

```fsharp
if cond then e1 else e2
```

<span data-ttu-id="50215-188">Si `e1` et `cond` sont petits, mais `e2` est importante :</span><span class="sxs-lookup"><span data-stu-id="50215-188">If `e1` and `cond` are small, but `e2` is large:</span></span>

```fsharp
if cond then e1
else
    e2
```

<span data-ttu-id="50215-189">Si `e1` et `cond` sont volumineux et `e2` est petite :</span><span class="sxs-lookup"><span data-stu-id="50215-189">If `e1` and `cond` are large and `e2` is small:</span></span>

```fsharp
if cond then
    e1
else e2
```

<span data-ttu-id="50215-190">Si toutes les expressions sont volumineuses :</span><span class="sxs-lookup"><span data-stu-id="50215-190">If all the expressions are large:</span></span>

```fsharp
if cond then
    e1
else
    e2
```

<span data-ttu-id="50215-191">Plusieurs conditions avec `elif` et `else` sont mises en retrait à la même portée que la `if`:</span><span class="sxs-lookup"><span data-stu-id="50215-191">Multiple conditionals with `elif` and `else` are indented at the same scope as the `if`:</span></span>

```fsharp
if cond1 then e1
elif cond2 then e2
elif cond3 then e3
else e4
```

### <a name="pattern-matching-constructs"></a><span data-ttu-id="50215-192">Constructions de correspondance de modèle</span><span class="sxs-lookup"><span data-stu-id="50215-192">Pattern matching constructs</span></span>

<span data-ttu-id="50215-193">Utilisez un `|` pour chaque clause d’une correspondance avec aucune mise en retrait.</span><span class="sxs-lookup"><span data-stu-id="50215-193">Use a `|` for each clause of a match with no indentation.</span></span> <span data-ttu-id="50215-194">Si l’expression est courte, vous pouvez envisager d’utiliser une seule ligne si chaque sous-expression est aussi simple.</span><span class="sxs-lookup"><span data-stu-id="50215-194">If the expression is short, you can consider using a single line if each subexpression is also simple.</span></span>

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

<span data-ttu-id="50215-195">Si l’expression à droite de la flèche de mise en correspondance est trop grande, déplacez-le vers la ligne suivante, la mise en retrait d’une seule étape à partir de la `match` / `|`.</span><span class="sxs-lookup"><span data-stu-id="50215-195">If the expression on the right of the pattern matching arrow is too large, move it to the following line, indented one step from the `match`/`|`.</span></span>

```fsharp
match lam with
| Var v -> 1
| Abs(x, body) ->
    1 + sizeLambda body
| App(lam1, lam2) ->
    sizeLambda lam1 + sizeLambda lam2

```

<span data-ttu-id="50215-196">Filtre de correspondance de fonctions anonymes, en commençant par `function`, doit généralement pas mettre en retrait trop loin.</span><span class="sxs-lookup"><span data-stu-id="50215-196">Pattern matching of anonymous functions, starting by `function`, should generally not indent too far.</span></span> <span data-ttu-id="50215-197">Par exemple, il est correct de mise en retrait d’une étendue comme suit :</span><span class="sxs-lookup"><span data-stu-id="50215-197">For example, indenting one scope as follows is fine:</span></span>

```fsharp
lambdaList
|> List.map (function
    | Abs(x, body) -> 1 + sizeLambda 0 body
    | App(lam1, lam2) -> sizeLambda (sizeLambda 0 lam1) lam2
    | Var v -> 1)
```

<span data-ttu-id="50215-198">Mise en correspondance dans les fonctions définies par `let` ou `let rec` doit être mis en retrait 4 espaces après le démarrage de `let`, même si `function` mot clé est utilisé :</span><span class="sxs-lookup"><span data-stu-id="50215-198">Pattern matching in functions defined by `let` or `let rec` should be indented 4 spaces after starting of `let`, even if `function` keyword is used:</span></span>

```fsharp
let rec sizeLambda acc = function
    | Abs(x, body) -> sizeLambda (succ acc) body
    | App(lam1, lam2) -> sizeLambda (sizeLambda acc lam1) lam2
    | Var v -> succ acc
```

<span data-ttu-id="50215-199">Nous vous déconseillons d’alignement des flèches.</span><span class="sxs-lookup"><span data-stu-id="50215-199">We do not recommend aligning arrows.</span></span>

## <a name="formatting-trywith-expressions"></a><span data-ttu-id="50215-200">Essayez de mise en forme / avec des expressions</span><span class="sxs-lookup"><span data-stu-id="50215-200">Formatting try/with expressions</span></span>

<span data-ttu-id="50215-201">Mise en correspondance sur le type d’exception doit être mis en retrait au même niveau que `with`.</span><span class="sxs-lookup"><span data-stu-id="50215-201">Pattern matching on the exception type should be indented at the same level as `with`.</span></span>

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

## <a name="formatting-function-parameter-application"></a><span data-ttu-id="50215-202">Application de paramètre de fonction de mise en forme</span><span class="sxs-lookup"><span data-stu-id="50215-202">Formatting function parameter application</span></span>

<span data-ttu-id="50215-203">En règle générale, la plupart des applications de paramètre de fonction sont effectuée sur la même ligne.</span><span class="sxs-lookup"><span data-stu-id="50215-203">In general, most function parameter application is done on the same line.</span></span>

<span data-ttu-id="50215-204">Si vous souhaitez appliquer des paramètres à une fonction sur une nouvelle ligne, les mettre en retrait une étendue.</span><span class="sxs-lookup"><span data-stu-id="50215-204">If you wish to apply parameters to a function on a new line, indent them by one scope.</span></span>

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

<span data-ttu-id="50215-205">Les mêmes règles s’appliquent pour les expressions lambda en tant qu’arguments de fonction.</span><span class="sxs-lookup"><span data-stu-id="50215-205">The same guidelines apply for lambda expressions as function arguments.</span></span> <span data-ttu-id="50215-206">Si le corps d’une expression lambda, le corps peut avoir une autre ligne, la mise en retrait par une étendue</span><span class="sxs-lookup"><span data-stu-id="50215-206">If the body of a lambda expression, the body can have another line, indented by one scope</span></span>

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

<span data-ttu-id="50215-207">Toutefois, si le corps d’une expression lambda est plusieurs lignes, envisagez factorisant dans une fonction distincte plutôt que d’avoir une construction multiligne appliquée en tant qu’un seul argument à une fonction.</span><span class="sxs-lookup"><span data-stu-id="50215-207">However, if the body of a lambda expression is more than one line, consider factoring it out into a separate function rather than have a multi-line construct applied as a single argument to a function.</span></span>

### <a name="formatting-infix-operators"></a><span data-ttu-id="50215-208">Opérateurs infix mise en forme</span><span class="sxs-lookup"><span data-stu-id="50215-208">Formatting infix operators</span></span>

<span data-ttu-id="50215-209">Opérateurs distincts par des espaces.</span><span class="sxs-lookup"><span data-stu-id="50215-209">Separate operators by spaces.</span></span> <span data-ttu-id="50215-210">Exceptions évidentes à cette règle sont les `!` et `.` opérateurs.</span><span class="sxs-lookup"><span data-stu-id="50215-210">Obvious exceptions to this rule are the `!` and `.` operators.</span></span>

<span data-ttu-id="50215-211">Les expressions infix sont OK l’alignement sur la même colonne :</span><span class="sxs-lookup"><span data-stu-id="50215-211">Infix expressions are OK to lineup on same column:</span></span>

```fsharp
acc +
(sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity)

let function1 arg1 arg2 arg3 arg4 =
    arg1 + arg2 +
    arg3 + arg4
```

### <a name="formatting-pipeline-operators"></a><span data-ttu-id="50215-212">Opérateurs de pipeline de mise en forme</span><span class="sxs-lookup"><span data-stu-id="50215-212">Formatting pipeline operators</span></span>

<span data-ttu-id="50215-213">Pipeline `|>` opérateurs doivent figurer sous les ils opèrent sur des expressions.</span><span class="sxs-lookup"><span data-stu-id="50215-213">Pipeline `|>` operators should go underneath the expressions they operate on.</span></span>

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

### <a name="formatting-modules"></a><span data-ttu-id="50215-214">Mise en forme de modules</span><span class="sxs-lookup"><span data-stu-id="50215-214">Formatting modules</span></span>

<span data-ttu-id="50215-215">Code dans un module local doit être mis en retrait par rapport au module, mais le code dans un module de niveau supérieur ne doit pas être mis en retrait.</span><span class="sxs-lookup"><span data-stu-id="50215-215">Code in a local module must be indented relative to the module, but code in a top-level module should not be indented.</span></span> <span data-ttu-id="50215-216">Les éléments Namespace n’ont pas à être mis en retrait.</span><span class="sxs-lookup"><span data-stu-id="50215-216">Namespace elements do not have to be indented.</span></span>

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

### <a name="formatting-object-expressions-and-interfaces"></a><span data-ttu-id="50215-217">Mise en forme d’expressions d’objet et des interfaces</span><span class="sxs-lookup"><span data-stu-id="50215-217">Formatting object expressions and interfaces</span></span>

<span data-ttu-id="50215-218">Expressions d’objet et les interfaces doivent être alignées dans la même façon avec `member` en cours de mise en retrait après 4 espaces.</span><span class="sxs-lookup"><span data-stu-id="50215-218">Object expressions and interfaces should be aligned in the same way with `member` being indented after 4 spaces.</span></span>

```fsharp
let comparer =
    { new IComparer<string> with
          member x.Compare(s1, s2) =
              let rev (s : String) =
                  new String (Array.rev (s.ToCharArray()))
              let reversed = rev s1
              reversed.CompareTo (rev s2) }
```

### <a name="formatting-whitespace-in-expressions"></a><span data-ttu-id="50215-219">Mise en forme des espaces blancs dans les expressions</span><span class="sxs-lookup"><span data-stu-id="50215-219">Formatting whitespace in expressions</span></span>

<span data-ttu-id="50215-220">Évitez l’espace superflu dans les expressions F #.</span><span class="sxs-lookup"><span data-stu-id="50215-220">Avoid extraneous whitespace in F# expressions.</span></span>

```fsharp
// OK
spam (ham.[1])

// Not OK
spam ( ham.[ 1 ] )
```

<span data-ttu-id="50215-221">Arguments nommés doivent avoir également pas espace entourant le `=`:</span><span class="sxs-lookup"><span data-stu-id="50215-221">Named arguments should also not have space surrounding the `=`:</span></span>

```fsharp
// OK
let makeStreamReader x = new System.IO.StreamReader(path=x)

// Not OK
let makeStreamReader x = new System.IO.StreamReader(path = x)
```
