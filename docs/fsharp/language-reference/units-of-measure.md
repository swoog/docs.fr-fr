---
title: Unités de mesure (F#)
description: 'Découvrez comment flottantes et valeurs d’entier signé en F # peuvent avoir des unités de mesure, qui sont généralement utilisées pour indiquer la longueur, le volume et masse associées.'
ms.date: 05/16/2016
ms.openlocfilehash: ad2193e25f3c0cee6e73cd529ab43d1e4b6b549b
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2018
ms.locfileid: "45616151"
---
# <a name="units-of-measure"></a><span data-ttu-id="1cee9-103">Unités de mesure</span><span class="sxs-lookup"><span data-stu-id="1cee9-103">Units of Measure</span></span>

<span data-ttu-id="1cee9-104">Virgule flottante et entiers auto-signés en F # permettre être associés à des unités de mesure, qui sont généralement utilisées pour indiquer la longueur, volume, en série, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="1cee9-104">Floating point and signed integer values in F# can have associated units of measure, which are typically used to indicate length, volume, mass, and so on.</span></span> <span data-ttu-id="1cee9-105">À l’aide de quantités avec des unités, vous activez le compilateur de vérifier que les relations arithmétiques ont les bonnes unités, qui permet d’éviter des erreurs de programmation.</span><span class="sxs-lookup"><span data-stu-id="1cee9-105">By using quantities with units, you enable the compiler to verify that arithmetic relationships have the correct units, which helps prevent programming errors.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cee9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cee9-106">Syntax</span></span>

```fsharp
[<Measure>] type unit-name [ = measure ]
```

## <a name="remarks"></a><span data-ttu-id="1cee9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1cee9-107">Remarks</span></span>

<span data-ttu-id="1cee9-108">Définit la syntaxe précédente *nom de l’unité* en tant qu’unité de mesure.</span><span class="sxs-lookup"><span data-stu-id="1cee9-108">The previous syntax defines *unit-name* as a unit of measure.</span></span> <span data-ttu-id="1cee9-109">La partie facultative permet de définir une nouvelle mesure en termes d’unités précédemment définies.</span><span class="sxs-lookup"><span data-stu-id="1cee9-109">The optional part is used to define a new measure in terms of previously defined units.</span></span> <span data-ttu-id="1cee9-110">Par exemple, la ligne suivante définit la mesure `cm` (centimètre).</span><span class="sxs-lookup"><span data-stu-id="1cee9-110">For example, the following line defines the measure `cm` (centimeter).</span></span>

```fsharp
[<Measure>] type cm
```

<span data-ttu-id="1cee9-111">La ligne suivante définit la mesure `ml` (millilitre) comme un centimètre cube (`cm^3`).</span><span class="sxs-lookup"><span data-stu-id="1cee9-111">The following line defines the measure `ml` (milliliter) as a cubic centimeter (`cm^3`).</span></span>

```fsharp
[<Measure>] type ml = cm^3
```

<span data-ttu-id="1cee9-112">Dans la syntaxe précédente, *mesure* est une formule qui implique des unités.</span><span class="sxs-lookup"><span data-stu-id="1cee9-112">In the previous syntax, *measure* is a formula that involves units.</span></span> <span data-ttu-id="1cee9-113">Dans les formules qui impliquent des unités, puissances intégrales sont prises en charge (positives et négatives), les espaces entre les unités indiquent un produit des deux unités, `*` indique également un produit d’unités, et `/` indique un quotient d’unités.</span><span class="sxs-lookup"><span data-stu-id="1cee9-113">In formulas that involve units, integral powers are supported (positive and negative), spaces between units indicate a product of the two units, `*` also indicates a product of units, and `/` indicates a quotient of units.</span></span> <span data-ttu-id="1cee9-114">Pour une unité réciproque, vous pouvez utiliser une puissance entier négatif ou une `/` qui indique une séparation entre le numérateur et le dénominateur d’une formule d’unité.</span><span class="sxs-lookup"><span data-stu-id="1cee9-114">For a reciprocal unit, you can either use a negative integer power or a `/` that indicates a separation between the numerator and denominator of a unit formula.</span></span> <span data-ttu-id="1cee9-115">Plusieurs unités dans le dénominateur doivent être placées entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="1cee9-115">Multiple units in the denominator should be surrounded by parentheses.</span></span> <span data-ttu-id="1cee9-116">Unités séparant par des espaces après un `/` sont interprétées comme faisant partie du dénominateur, mais aucune unité suivant un `*` sont interprétées comme faisant partie du numérateur.</span><span class="sxs-lookup"><span data-stu-id="1cee9-116">Units separated by spaces after a `/` are interpreted as being part of the denominator, but any units following a `*` are interpreted as being part of the numerator.</span></span>

<span data-ttu-id="1cee9-117">Vous pouvez utiliser 1 dans les expressions d’unité, soit seul pour indiquer une quantité sans dimension, ou avec d’autres unités, comme dans le numérateur.</span><span class="sxs-lookup"><span data-stu-id="1cee9-117">You can use 1 in unit expressions, either alone to indicate a dimensionless quantity, or together with other units, such as in the numerator.</span></span> <span data-ttu-id="1cee9-118">Par exemple, les unités pour un taux sont écrites en tant que `1/s`, où `s` indique les secondes.</span><span class="sxs-lookup"><span data-stu-id="1cee9-118">For example, the units for a rate would be written as `1/s`, where `s` indicates seconds.</span></span> <span data-ttu-id="1cee9-119">Parenthèses ne sont pas utilisées dans les formules d’unité.</span><span class="sxs-lookup"><span data-stu-id="1cee9-119">Parentheses are not used in unit formulas.</span></span> <span data-ttu-id="1cee9-120">Vous ne spécifiez pas de constantes de conversion numérique dans les formules d’unité ; Toutefois, vous pouvez définir séparément des constantes de conversion avec des unités et les utiliser dans les calculs de vérification des unités.</span><span class="sxs-lookup"><span data-stu-id="1cee9-120">You do not specify numeric conversion constants in the unit formulas; however, you can define conversion constants with units separately and use them in unit-checked computations.</span></span>

<span data-ttu-id="1cee9-121">Formules d’unité qui ont la même signification peuvent être écrit de différentes manières équivalentes.</span><span class="sxs-lookup"><span data-stu-id="1cee9-121">Unit formulas that mean the same thing can be written in various equivalent ways.</span></span> <span data-ttu-id="1cee9-122">Par conséquent, le compilateur convertit les formules d’unité dans un format cohérent, qui convertit des puissances négatives réciproques, unités de groupes en un seul numérateur et dénominateur et les trie par ordre alphabétique les unités dans le numérateur et dénominateur.</span><span class="sxs-lookup"><span data-stu-id="1cee9-122">Therefore, the compiler converts unit formulas into a consistent form, which converts negative powers to reciprocals, groups units into a single numerator and a denominator, and alphabetizes the units in the numerator and denominator.</span></span>

<span data-ttu-id="1cee9-123">Par exemple, les formules d’unité `kg m s^-2` et `m /s s * kg` sont convertis en `kg m/s^2`.</span><span class="sxs-lookup"><span data-stu-id="1cee9-123">For example, the unit formulas `kg m s^-2` and `m /s s * kg` are both converted to `kg m/s^2`.</span></span>

<span data-ttu-id="1cee9-124">Vous utilisez des unités de mesure dans les expressions virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="1cee9-124">You use units of measure in floating point expressions.</span></span> <span data-ttu-id="1cee9-125">À l’aide de nombres à virgule flottante avec unités associées de mesure ajoute un autre niveau de sécurité de type et permet d’éviter les erreurs d’incompatibilité unité qui peuvent se produire dans les formules lorsque vous utilisez des nombres à virgule flottante faiblement typée.</span><span class="sxs-lookup"><span data-stu-id="1cee9-125">Using floating point numbers together with associated units of measure adds another level of type safety and helps avoid the unit mismatch errors that can occur in formulas when you use weakly typed floating point numbers.</span></span> <span data-ttu-id="1cee9-126">Si vous écrivez flottante expression point qui utilise des unités, les unités dans l’expression doivent correspondre.</span><span class="sxs-lookup"><span data-stu-id="1cee9-126">If you write a floating point expression that uses units, the units in the expression must match.</span></span>

<span data-ttu-id="1cee9-127">Vous pouvez annoter des littéraux avec une formule d’unité figurant entre crochets, comme indiqué dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="1cee9-127">You can annotate literals with a unit formula in angle brackets, as shown in the following examples.</span></span>

```fsharp
1.0<cm>
55.0<miles/hour>
```

<span data-ttu-id="1cee9-128">Vous ne placez pas d’espace entre le nombre et le crochet angulaire ; Toutefois, vous pouvez inclure un suffixe littéral comme `f`, comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="1cee9-128">You do not put a space between the number and the angle bracket; however, you can include a literal suffix such as `f`, as in the following example.</span></span>

```fsharp
// The f indicates single-precision floating point.
55.0f<miles/hour>
```

<span data-ttu-id="1cee9-129">Une telle annotation modifie le type du littéral de son type primitif (tel que `float`) en un type dimensionné, tel que `float<cm>` ou, dans ce cas, `float<miles/hour>`.</span><span class="sxs-lookup"><span data-stu-id="1cee9-129">Such an annotation changes the type of the literal from its primitive type (such as `float`) to a dimensioned type, such as `float<cm>` or, in this case, `float<miles/hour>`.</span></span> <span data-ttu-id="1cee9-130">Une annotation d’unité `<1>` indique une quantité sans dimension et son type est équivalent au type primitif sans paramètre d’unité.</span><span class="sxs-lookup"><span data-stu-id="1cee9-130">A unit annotation of `<1>` indicates a dimensionless quantity, and its type is equivalent to the primitive type without a unit parameter.</span></span>

<span data-ttu-id="1cee9-131">Le type d’une unité de mesure est une virgule flottante ou signés de type intégral avec une annotation d’unité supplémentaire, indiquée entre crochets.</span><span class="sxs-lookup"><span data-stu-id="1cee9-131">The type of a unit of measure is a floating point or signed integral type together with an extra unit annotation, indicated in brackets.</span></span> <span data-ttu-id="1cee9-132">Par conséquent, lorsque vous écrivez le type d’une conversion de `g` (g) à `kg` (kilogrammes), vous décrivez les types comme suit.</span><span class="sxs-lookup"><span data-stu-id="1cee9-132">Thus, when you write the type of a conversion from `g` (grams) to `kg` (kilograms), you describe the types as follows.</span></span>

```fsharp
let convertg2kg (x : float<g>) = x / 1000.0<g/kg>
```

<span data-ttu-id="1cee9-133">Unités de mesure sont utilisées pour la vérification des unités au moment de la compilation, mais ne sont pas conservées dans l’environnement d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1cee9-133">Units of measure are used for compile-time unit checking but are not persisted in the run-time environment.</span></span> <span data-ttu-id="1cee9-134">Par conséquent, elles n’affectent pas les performances.</span><span class="sxs-lookup"><span data-stu-id="1cee9-134">Therefore, they do not affect performance.</span></span>

<span data-ttu-id="1cee9-135">Unités de mesure peuvent être appliquées à n’importe quel type, pas seulement types à virgule flottante ; Toutefois, les seuls types à virgule flottante, connecté types intégraux et les types décimaux prise en charge de dimensionner les quantités.</span><span class="sxs-lookup"><span data-stu-id="1cee9-135">Units of measure can be applied to any type, not just floating point types; however, only floating point types, signed integral types, and decimal types support dimensioned quantities.</span></span> <span data-ttu-id="1cee9-136">Par conséquent, il convient uniquement pour les unités de mesure sur les types primitifs et les agrégats qui contiennent ces types primitifs.</span><span class="sxs-lookup"><span data-stu-id="1cee9-136">Therefore, it only makes sense to use units of measure on the primitive types and on aggregates that contain these primitive types.</span></span>

<span data-ttu-id="1cee9-137">L’exemple suivant illustre l’utilisation d’unités de mesure.</span><span class="sxs-lookup"><span data-stu-id="1cee9-137">The following example illustrates the use of units of measure.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6901.fs)]

<span data-ttu-id="1cee9-138">L’exemple de code suivant illustre comment convertir à partir d’un nombre à virgule flottante sans dimension en une valeur à virgule flottante dimensionnée.</span><span class="sxs-lookup"><span data-stu-id="1cee9-138">The following code example illustrates how to convert from a dimensionless floating point number to a dimensioned floating point value.</span></span> <span data-ttu-id="1cee9-139">Vous multipliez simplement par 1.0, appliquant les dimensions à la version 1.0.</span><span class="sxs-lookup"><span data-stu-id="1cee9-139">You just multiply by 1.0, applying the dimensions to the 1.0.</span></span> <span data-ttu-id="1cee9-140">Vous pouvez l’extraire dans une fonction comme `degreesFahrenheit`.</span><span class="sxs-lookup"><span data-stu-id="1cee9-140">You can abstract this into a function like `degreesFahrenheit`.</span></span>

<span data-ttu-id="1cee9-141">En outre, lorsque vous transmettez des valeurs dimensionnées aux fonctions qui attendent des nombres à virgule flottante sans dimension, vous devez annuler les unités ou effectuer un cast en `float` à l’aide de la `float` opérateur.</span><span class="sxs-lookup"><span data-stu-id="1cee9-141">Also, when you pass dimensioned values to functions that expect dimensionless floating point numbers, you must cancel out the units or cast to `float` by using the `float` operator.</span></span> <span data-ttu-id="1cee9-142">Dans cet exemple, vous divisez par `1.0<degC>` pour les arguments de `printf` car `printf` attend des quantités sans dimension.</span><span class="sxs-lookup"><span data-stu-id="1cee9-142">In this example, you divide by `1.0<degC>` for the arguments to `printf` because `printf` expects dimensionless quantities.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6902.fs)]

<span data-ttu-id="1cee9-143">La session de l’exemple suivant montre les entrées à ce code et sorties.</span><span class="sxs-lookup"><span data-stu-id="1cee9-143">The following example session shows the outputs from and inputs to this code.</span></span>

```
Enter a temperature in degrees Fahrenheit.
90
That temperature in degrees Celsius is    32.22.
```

## <a name="using-generic-units"></a><span data-ttu-id="1cee9-144">Utilisation d’unités génériques</span><span class="sxs-lookup"><span data-stu-id="1cee9-144">Using Generic Units</span></span>

<span data-ttu-id="1cee9-145">Vous pouvez écrire des fonctions génériques qui fonctionnent sur les données associées à une unité de mesure.</span><span class="sxs-lookup"><span data-stu-id="1cee9-145">You can write generic functions that operate on data that has an associated unit of measure.</span></span> <span data-ttu-id="1cee9-146">Cela en spécifiant un type avec une unité générique comme un paramètre de type, comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="1cee9-146">You do this by specifying a type together with a generic unit as a type parameter, as shown in the following code example.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6903.fs)]

## <a name="creating-aggregate-types-with-generic-units"></a><span data-ttu-id="1cee9-147">Créer des Types d’agrégats avec unités génériques</span><span class="sxs-lookup"><span data-stu-id="1cee9-147">Creating Aggregate Types with Generic Units</span></span>

<span data-ttu-id="1cee9-148">Le code suivant montre comment créer un type d’agrégation qui se compose de valeurs à virgule flottante individuels qui ont des unités qui sont génériques.</span><span class="sxs-lookup"><span data-stu-id="1cee9-148">The following code shows how to create an aggregate type that consists of individual floating point values that have units that are generic.</span></span> <span data-ttu-id="1cee9-149">Ainsi, un seul type qui fonctionne avec un large éventail d’unités doit être créé.</span><span class="sxs-lookup"><span data-stu-id="1cee9-149">This enables a single type to be created that works with a variety of units.</span></span> <span data-ttu-id="1cee9-150">Unités génériques conservent également, la sécurité de type en veillant à ce qu’un type générique qui a un ensemble d’unités est un autre type que le même type générique avec un autre ensemble d’unités.</span><span class="sxs-lookup"><span data-stu-id="1cee9-150">Also, generic units preserve type safety by ensuring that a generic type that has one set of units is a different type than the same generic type with a different set of units.</span></span> <span data-ttu-id="1cee9-151">La base de cette technique est que le `Measure` attribut peut être appliqué au paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="1cee9-151">The basis of this technique is that the `Measure` attribute can be applied to the type parameter.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6904.fs)]

## <a name="units-at-runtime"></a><span data-ttu-id="1cee9-152">Unités lors de l’exécution</span><span class="sxs-lookup"><span data-stu-id="1cee9-152">Units at Runtime</span></span>

<span data-ttu-id="1cee9-153">Unités de mesure sont utilisées pour la vérification de type statique.</span><span class="sxs-lookup"><span data-stu-id="1cee9-153">Units of measure are used for static type checking.</span></span> <span data-ttu-id="1cee9-154">Lorsque des valeurs à virgule flottante sont compilées, les unités de mesure sont éliminées, par conséquent, les unités sont perdues au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="1cee9-154">When floating point values are compiled, the units of measure are eliminated, so the units are lost at run time.</span></span> <span data-ttu-id="1cee9-155">Par conséquent, toute tentative pour implémenter des fonctionnalités qui dépendent de la vérification des unités au moment de l’exécution n’est pas possible.</span><span class="sxs-lookup"><span data-stu-id="1cee9-155">Therefore, any attempt to implement functionality that depends on checking the units at run time is not possible.</span></span> <span data-ttu-id="1cee9-156">Par exemple, mise en œuvre un `ToString` (fonction) pour imprimer le nombre d’unités n’est pas possible.</span><span class="sxs-lookup"><span data-stu-id="1cee9-156">For example, implementing a `ToString` function to print out the units is not possible.</span></span>

## <a name="conversions"></a><span data-ttu-id="1cee9-157">Conversions</span><span class="sxs-lookup"><span data-stu-id="1cee9-157">Conversions</span></span>

<span data-ttu-id="1cee9-158">Pour convertir un type qui a des unités (par exemple, `float<'u>`) à un type qui n’a pas d’unités, vous pouvez utiliser la fonction de conversion standard.</span><span class="sxs-lookup"><span data-stu-id="1cee9-158">To convert a type that has units (for example, `float<'u>`) to a type that does not have units, you can use the standard conversion function.</span></span> <span data-ttu-id="1cee9-159">Par exemple, vous pouvez utiliser `float` pour convertir un `float` valeur qui n’a pas d’unités, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="1cee9-159">For example, you can use `float` to convert to a `float` value that does not have units, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6905.fs)]

<span data-ttu-id="1cee9-160">Pour convertir une valeur sans unité en une valeur qui a des unités, vous pouvez multiplier par une valeur de 1 ou 1.0 annotée avec les unités appropriées.</span><span class="sxs-lookup"><span data-stu-id="1cee9-160">To convert a unitless value to a value that has units, you can multiply by a 1 or 1.0 value that is annotated with the appropriate units.</span></span> <span data-ttu-id="1cee9-161">Toutefois, pour écrire des couches d’interopérabilité, il existe également certaines fonctions explicites que vous pouvez utiliser pour convertir des valeurs sans unité avec les unités.</span><span class="sxs-lookup"><span data-stu-id="1cee9-161">However, for writing interoperability layers, there are also some explicit functions that you can use to convert unitless values to values with units.</span></span> <span data-ttu-id="1cee9-162">Il s’agit dans le [Microsoft.FSharp.Core.LanguagePrimitives](https://msdn.microsoft.com/library/69d08ac5-5d51-4c20-bf1e-850fd312ece3) module.</span><span class="sxs-lookup"><span data-stu-id="1cee9-162">These are in the [Microsoft.FSharp.Core.LanguagePrimitives](https://msdn.microsoft.com/library/69d08ac5-5d51-4c20-bf1e-850fd312ece3) module.</span></span> <span data-ttu-id="1cee9-163">Par exemple, pour convertir un sans unité `float` à un `float<cm>`, utilisez [FloatWithMeasure](https://msdn.microsoft.com/library/69520bc7-d67b-46b8-9004-7cac9646b8d9), comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="1cee9-163">For example, to convert from a unitless `float` to a `float<cm>`, use [FloatWithMeasure](https://msdn.microsoft.com/library/69520bc7-d67b-46b8-9004-7cac9646b8d9), as shown in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6906.fs)]

## <a name="units-of-measure-in-the-f-core-library"></a><span data-ttu-id="1cee9-164">Unités de mesure dans la bibliothèque principale F #</span><span class="sxs-lookup"><span data-stu-id="1cee9-164">Units of Measure in the F# Core library</span></span>

<span data-ttu-id="1cee9-165">Une unité de bibliothèque est disponible dans le `FSharp.Data.UnitSystems.SI` espace de noms.</span><span class="sxs-lookup"><span data-stu-id="1cee9-165">A unit library is available in the `FSharp.Data.UnitSystems.SI` namespace.</span></span> <span data-ttu-id="1cee9-166">Il inclut des unités SI dans les deux leur forme de symbole (comme `m` compteur) dans le `UnitSymbols` sub-espace de noms et leur nom complet (comme `meter` compteur) dans le `UnitNames` sub-espace de noms.</span><span class="sxs-lookup"><span data-stu-id="1cee9-166">It includes SI units in both their symbol form (like `m` for meter) in the `UnitSymbols` sub-namespace, and their full name (like `meter` for meter) in the `UnitNames` sub-namespace.</span></span>

## <a name="see-also"></a><span data-ttu-id="1cee9-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cee9-167">See also</span></span>

- [<span data-ttu-id="1cee9-168">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="1cee9-168">F# Language Reference</span></span>](index.md)
