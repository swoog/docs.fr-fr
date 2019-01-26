---
title: Extensions de type
description: Découvrez comment F# les extensions de type permettent d’ajouter de nouveaux membres à un type d’objet précédemment défini.
ms.date: 01/23/2019
ms.openlocfilehash: d52bc38850219a142ff4f5d840e418ea4bd50cca
ms.sourcegitcommit: d9a0071d0fd490ae006c816f78a563b9946e269a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55066153"
---
# <a name="type-extensions"></a><span data-ttu-id="ebf4a-103">Extensions de type</span><span class="sxs-lookup"><span data-stu-id="ebf4a-103">Type extensions</span></span>

<span data-ttu-id="ebf4a-104">Extensions de type (également appelé _augmentations_) est une famille de fonctionnalités qui vous permettent d’ajouter de nouveaux membres à un type d’objet précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-104">Type extensions (also called _augmentations_) are a family of features that let you add new members to a previously defined object type.</span></span> <span data-ttu-id="ebf4a-105">Les trois fonctionnalités sont :</span><span class="sxs-lookup"><span data-stu-id="ebf4a-105">The three features are:</span></span>

* <span data-ttu-id="ebf4a-106">Extensions de type intrinsèques</span><span class="sxs-lookup"><span data-stu-id="ebf4a-106">Intrinsic type extensions</span></span>
* <span data-ttu-id="ebf4a-107">Extensions de type facultatif</span><span class="sxs-lookup"><span data-stu-id="ebf4a-107">Optional type extensions</span></span>
* <span data-ttu-id="ebf4a-108">Méthodes d’extension</span><span class="sxs-lookup"><span data-stu-id="ebf4a-108">Extension methods</span></span>

<span data-ttu-id="ebf4a-109">Chacun peut être utilisé dans différents scénarios et a différents compromis.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-109">Each can be used in different scenarios and has different tradeoffs.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf4a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebf4a-110">Syntax</span></span>

```fsharp
// Intrinsic and optional extensions
type typename with
    member self-identifier.member-name =
        body
    ...

// Extension methods
open System.Runtime.CompilerServices

[<Extension>]
type Extensions() =
    [static] member self-identifier.extension-name (ty: typename, [args]) =
        body
    ...
```

## <a name="intrinsic-type-extensions"></a><span data-ttu-id="ebf4a-111">Extensions de type intrinsèques</span><span class="sxs-lookup"><span data-stu-id="ebf4a-111">Intrinsic type extensions</span></span>

<span data-ttu-id="ebf4a-112">Une extension de type intrinsèque est une extension de type qui étend un type défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-112">An intrinsic type extension is a type extension that extends a user-defined type.</span></span>

<span data-ttu-id="ebf4a-113">Extensions de type intrinsèques doivent être définies dans le même fichier **et** dans le même espace de noms ou module en tant que le type de la société étend.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-113">Intrinsic type extensions must be defined in the same file **and** in the same namespace or module as the type they're extending.</span></span> <span data-ttu-id="ebf4a-114">N’importe quel autre définition les entraîne en cours [extensions de type facultatif](type-extensions.md#optional-type-extensions).</span><span class="sxs-lookup"><span data-stu-id="ebf4a-114">Any other definition will result in them being [optional type extensions](type-extensions.md#optional-type-extensions).</span></span>

<span data-ttu-id="ebf4a-115">Extensions de type intrinsèques sont parfois un moyen plus clair de séparer les fonctionnalités de la déclaration de type.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-115">Intrinsic type extensions are sometimes a cleaner way to separate functionality from the type declaration.</span></span> <span data-ttu-id="ebf4a-116">L’exemple suivant montre comment définir une extension de type intrinsèque :</span><span class="sxs-lookup"><span data-stu-id="ebf4a-116">The following example shows how to define an intrinsic type extension:</span></span>

```fsharp
namespace Example

type Variant =
    | Num of int
    | Str of string
  
module Variant =
    let print v =
        match v with
        | Num n -> printf "Num %d" n
        | Str s -> printf "Str %s" s

// Add a member to Variant as an extension
type Variant with
    member x.Print() = Variant.print x
```

<span data-ttu-id="ebf4a-117">À l’aide d’une extension de type vous permet de séparer les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ebf4a-117">Using a type extension allows you to separate each of the following:</span></span>

* <span data-ttu-id="ebf4a-118">La déclaration d’un `Variant` type</span><span class="sxs-lookup"><span data-stu-id="ebf4a-118">The declaration of a `Variant` type</span></span>
* <span data-ttu-id="ebf4a-119">Fonctionnalités pour imprimer la `Variant` classe selon sa « forme »</span><span class="sxs-lookup"><span data-stu-id="ebf4a-119">Functionality to print the `Variant` class depending on its "shape"</span></span>
* <span data-ttu-id="ebf4a-120">Un moyen d’accéder à la fonctionnalité d’impression avec le style de l’objet `.`-notation</span><span class="sxs-lookup"><span data-stu-id="ebf4a-120">A way to access the printing functionality with object-style `.`-notation</span></span>

<span data-ttu-id="ebf4a-121">Il s’agit d’une alternative à la définition de tous les éléments en tant que membre sur `Variant`.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-121">This is an alternative to defining everything as a member on `Variant`.</span></span> <span data-ttu-id="ebf4a-122">Il n’est pas intrinsèquement une meilleure approche, mais il peut être une représentation plus claire de fonctionnalités dans certaines situations.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-122">Although it is not an inherently better approach, it can be a cleaner representation of functionality in some situations.</span></span>

<span data-ttu-id="ebf4a-123">Extensions de type intrinsèques sont compilées en tant que membres du type augmenter, ils apparaissent sur le type lorsque le type est examiné par réflexion.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-123">Intrinsic type extensions are compiled as members of the type they augment, and appear on the type when the type is examined by reflection.</span></span>

## <a name="optional-type-extensions"></a><span data-ttu-id="ebf4a-124">Extensions de type facultatif</span><span class="sxs-lookup"><span data-stu-id="ebf4a-124">Optional type extensions</span></span>

<span data-ttu-id="ebf4a-125">Une extension de type facultatif est une extension qui s’affiche à l’extérieur du module, espace de noms ou assembly du type étendu d’origine.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-125">An optional type extension is an extension that appears outside the original module, namespace, or assembly of the type being extended.</span></span>

<span data-ttu-id="ebf4a-126">Extensions de type facultatives sont utiles pour l’extension d’un type que vous n’avez pas défini vous-même.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-126">Optional type extensions are useful for extending a type that you have not defined yourself.</span></span> <span data-ttu-id="ebf4a-127">Exemple :</span><span class="sxs-lookup"><span data-stu-id="ebf4a-127">For example:</span></span>

```fsharp
module Extensions

open System.Collections.Generic

type IEnumerable<'T> with
    /// Repeat each element of the sequence n times
    member xs.RepeatElements(n: int) =
        seq {
            for x in xs do
                for i in 1 .. n do
                    yield x
        }
```

<span data-ttu-id="ebf4a-128">Vous pouvez désormais accéder `RepeatElements` comme s’il est membre de <xref:System.Collections.Generic.IEnumerable%601> tant que le `Extensions` module est ouvert dans l’étendue que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-128">You can now access `RepeatElements` as if it's a member of <xref:System.Collections.Generic.IEnumerable%601> as long as the `Extensions` module is opened in the scope that you are working in.</span></span>

<span data-ttu-id="ebf4a-129">Des extensions facultatives n’apparaissent pas sur le type étendu quand il est examiné par réflexion.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-129">Optional extensions do not appear on the extended type when examined by reflection.</span></span> <span data-ttu-id="ebf4a-130">Des extensions facultatives doivent être dans des modules, et ils sont uniquement dans la portée lorsque le module qui contient l’extension est ouvert ou dans la portée.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-130">Optional extensions must be in modules, and they're only in scope when the module that contains the extension is open or is otherwise in scope.</span></span>

<span data-ttu-id="ebf4a-131">Membres d’extension facultatifs sont compilés en membres statiques pour lequel l’instance d’objet est passée implicitement comme premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-131">Optional extension members are compiled to static members for which the object instance is passed implicitly as the first parameter.</span></span> <span data-ttu-id="ebf4a-132">Toutefois, ils agissent comme si elles sont membres d’instance ou des membres statiques selon la façon dont elles sont déclarées.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-132">However, they act as if they're instance members or static members according to how they're declared.</span></span>

## <a name="generic-limitation-of-intrinsic-and-optional-type-extensions"></a><span data-ttu-id="ebf4a-133">Limitation générique des extensions de type intrinsèque et facultatifs</span><span class="sxs-lookup"><span data-stu-id="ebf4a-133">Generic limitation of intrinsic and optional type extensions</span></span>

<span data-ttu-id="ebf4a-134">Il est possible de déclarer une extension de type sur un type générique, où la variable de type est contraint.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-134">It's possible to declare a type extension on a generic type where the type variable is constrained.</span></span> <span data-ttu-id="ebf4a-135">L’exigence est que la contrainte de la déclaration de l’extension correspond à la contrainte du type déclaré.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-135">The requirement is that the constraint of the extension declaration matches the constraint of the declared type.</span></span>

<span data-ttu-id="ebf4a-136">Toutefois, même lorsque les contraintes sont mises en correspondance entre un type déclaré et une extension de type, il est possible pour une contrainte à être déduit par le corps d’un membre d’étendue qui impose des exigences différentes sur le paramètre de type que le type déclaré.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-136">However, even when constraints are matched between a declared type and a type extension, it's possible for a constraint to be inferred by the body of an extended member that imposes a different requirement on the type parameter than the declared type.</span></span> <span data-ttu-id="ebf4a-137">Exemple :</span><span class="sxs-lookup"><span data-stu-id="ebf4a-137">For example:</span></span>

```fsharp
open System.Collections.Generic

// NOT POSSIBLE AND FAILS TO COMPILE!
//
// The member 'Sum' has a different requirement on 'T than the type IEnumerable<'T>
type IEnumerable<'T> with
    member this.Sum() = Seq.sum this
```

<span data-ttu-id="ebf4a-138">Il n’existe aucun moyen pour obtenir ce code fonctionne avec une extension de type facultatif :</span><span class="sxs-lookup"><span data-stu-id="ebf4a-138">There is no way to get this code to work with an optional type extension:</span></span>

* <span data-ttu-id="ebf4a-139">En l’état, le `Sum` membre a une contrainte différente `'T` (`static member get_Zero` et `static member (+)`) à ce qui définit l’extension du type.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-139">As is, the `Sum` member has a different constraint on `'T` (`static member get_Zero` and `static member (+)`) than what the type extension defines.</span></span>
* <span data-ttu-id="ebf4a-140">Modification de l’extension de type pour avoir la même contrainte en tant que `Sum` n’est pas la contrainte définie sur `IEnumerable<'T>`.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-140">Modifying the type extension to have the same constraint as `Sum` will no longer match the defined constraint on `IEnumerable<'T>`.</span></span>
* <span data-ttu-id="ebf4a-141">Modification `member this.Sum` à `member inline this.Sum` générera une erreur d’incompatibilité de contraintes de type.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-141">Changing `member this.Sum` to `member inline this.Sum` will give an error that type constraints are mismatched.</span></span>

<span data-ttu-id="ebf4a-142">Ce que vous souhaitez sont des méthodes statiques qui « flottant dans l’espace » et peuvent être présentés comme s’ils vous étendez un type.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-142">What is desired are static methods that "float in space" and can be presented as if they're extending a type.</span></span> <span data-ttu-id="ebf4a-143">Il s’agit dans lequel les méthodes d’extension devient nécessaires.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-143">This is where extension methods become necessary.</span></span>

## <a name="extension-methods"></a><span data-ttu-id="ebf4a-144">Méthodes d’extension</span><span class="sxs-lookup"><span data-stu-id="ebf4a-144">Extension methods</span></span>

<span data-ttu-id="ebf4a-145">Enfin, les méthodes d’extension (parfois appelé «C# membres d’extension de style ») peuvent être déclarés dans F# comme une méthode de membre statique sur une classe.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-145">Finally, extension methods (sometimes called "C# style extension members") can be declared in F# as a static member method on a class.</span></span>

<span data-ttu-id="ebf4a-146">Méthodes d’extension sont utiles pour lorsque vous souhaitez définir des extensions sur un type générique qui contrainte la variable de type.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-146">Extension methods are useful for when you wish to define extensions on a generic type that will constrain the type variable.</span></span> <span data-ttu-id="ebf4a-147">Exemple :</span><span class="sxs-lookup"><span data-stu-id="ebf4a-147">For example:</span></span>

```fsharp
namespace Extensions

open System.Runtime.CompilerServices

[<Extension>]
type IEnumerableExtensions() =
    [<Extension>]
    static member inline Sum(xs: IEnumerable<'T>) = Seq.sum xs
```

<span data-ttu-id="ebf4a-148">Lorsqu’il est utilisé, ce code sera faire apparaître comme si `Sum` est défini sur <xref:System.Collections.Generic.IEnumerable%601>, à condition que `Extensions` a été ouvert ou est dans la portée.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-148">When used, this code will make it appear as if `Sum` is defined on <xref:System.Collections.Generic.IEnumerable%601>, so long as `Extensions` has been opened or is in scope.</span></span>

## <a name="other-remarks"></a><span data-ttu-id="ebf4a-149">Autres remarques</span><span class="sxs-lookup"><span data-stu-id="ebf4a-149">Other remarks</span></span>

<span data-ttu-id="ebf4a-150">Extensions de type ont également les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="ebf4a-150">Type extensions also have the following attributes:</span></span>

* <span data-ttu-id="ebf4a-151">N’importe quel type accessible peut être étendu.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-151">Any type that can be accessed can be extended.</span></span>
* <span data-ttu-id="ebf4a-152">Définissent des extensions de type intrinsèques et facultatif _n’importe quel_ type de membre, pas seulement méthodes.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-152">Intrinsic and optional type extensions can define _any_ member type, not just methods.</span></span> <span data-ttu-id="ebf4a-153">Par conséquent, les propriétés d’extension sont également possibles, par exemple.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-153">So extension properties are also possible, for example.</span></span>
* <span data-ttu-id="ebf4a-154">Le `self-identifier` jeton dans le [syntaxe](type-extensions.md#syntax) représente l’instance du type appelé, comme des membres ordinaires.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-154">The `self-identifier` token in the [syntax](type-extensions.md#syntax) represents the instance of the type being invoked, just like ordinary members.</span></span>
* <span data-ttu-id="ebf4a-155">Étendues peuvent être statiques ou membres d’instance.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-155">Extended members can be static or instance members.</span></span>
* <span data-ttu-id="ebf4a-156">Les variables de type sur une extension de type doivent correspondre aux contraintes du type déclaré.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-156">Type variables on a type extension must match the constraints of the declared type.</span></span>

<span data-ttu-id="ebf4a-157">Les limitations suivantes existent également pour les extensions de type :</span><span class="sxs-lookup"><span data-stu-id="ebf4a-157">The following limitations also exist for type extensions:</span></span>

* <span data-ttu-id="ebf4a-158">Extensions de type ne prennent pas en charge les méthodes virtuelles ou abstraites.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-158">Type extensions do not support virtual or abstract methods.</span></span>
* <span data-ttu-id="ebf4a-159">Extensions de type ne gèrent pas les méthodes override en tant que les augmentations.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-159">Type extensions do not support override methods as augmentations.</span></span>
* <span data-ttu-id="ebf4a-160">Extensions de type ne gèrent pas [paramètres résolus statiquement Type](generics/statically-resolved-type-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ebf4a-160">Type extensions do not support [Statically Resolved Type Parameters](generics/statically-resolved-type-parameters.md).</span></span>
* <span data-ttu-id="ebf4a-161">Les extensions de Type facultatives ne gèrent pas les constructeurs en tant que les augmentations.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-161">Optional Type extensions do not support constructors as augmentations.</span></span>
* <span data-ttu-id="ebf4a-162">Extensions de type ne peut pas être définies sur [abréviations de types](type-abbreviations.md).</span><span class="sxs-lookup"><span data-stu-id="ebf4a-162">Type extensions cannot be defined on [type abbreviations](type-abbreviations.md).</span></span>
* <span data-ttu-id="ebf4a-163">Extensions de type ne sont pas valides pour `byref<'T>` (même si elles peuvent être déclarées).</span><span class="sxs-lookup"><span data-stu-id="ebf4a-163">Type extensions are not valid for `byref<'T>` (though they can be declared).</span></span>
* <span data-ttu-id="ebf4a-164">Extensions de type ne sont pas valides pour les attributs (même si elles peuvent être déclarées).</span><span class="sxs-lookup"><span data-stu-id="ebf4a-164">Type extensions are not valid for attributes (though they can be declared).</span></span>
* <span data-ttu-id="ebf4a-165">Vous pouvez définir des extensions qui surchargent les autres méthodes du même nom, mais la F# compilateur donne la préférence aux méthodes d’extension non s’il existe un appel ambigu.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-165">You can define extensions that overload other methods of the same name, but the F# compiler gives preference to non-extension methods if there is an ambiguous call.</span></span>

<span data-ttu-id="ebf4a-166">Enfin, si plusieurs extensions de type intrinsèques existent pour un type, tous les membres doivent être uniques.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-166">Finally, if multiple intrinsic type extensions exist for one type, all members must be unique.</span></span> <span data-ttu-id="ebf4a-167">Pour les extensions de type facultatif, les membres dans différentes extensions de type vers le même type peuvent avoir les mêmes noms.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-167">For optional type extensions, members in different type extensions to the same type can have the same names.</span></span> <span data-ttu-id="ebf4a-168">Erreurs d’ambiguïté se produisent uniquement si le code client ouvre deux portées différentes qui définissent les mêmes noms de membre.</span><span class="sxs-lookup"><span data-stu-id="ebf4a-168">Ambiguity errors occur only if client code opens two different scopes that define the same member names.</span></span>

## <a name="see-also"></a><span data-ttu-id="ebf4a-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebf4a-169">See also</span></span>

- [<span data-ttu-id="ebf4a-170">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="ebf4a-170">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="ebf4a-171">Membres</span><span class="sxs-lookup"><span data-stu-id="ebf4a-171">Members</span></span>](members/index.md)
