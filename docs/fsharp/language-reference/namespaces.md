---
title: Espaces de noms
description: Découvrez comment un F# espace de noms vous permet d’organiser le code en zones de fonctionnalités connexes en vous permettant de joindre un nom à un regroupement d’éléments de programme.
ms.date: 12/08/2018
ms.openlocfilehash: b315d654dad0d36e3584564ad027c68fb3c94cce
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65645269"
---
# <a name="namespaces"></a><span data-ttu-id="b4424-103">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="b4424-103">Namespaces</span></span>

<span data-ttu-id="b4424-104">Un espace de noms vous permet d’organiser le code en zones de fonctionnalités connexes en vous permettant de joindre un nom à un regroupement de F# éléments de programme.</span><span class="sxs-lookup"><span data-stu-id="b4424-104">A namespace lets you organize code into areas of related functionality by enabling you to attach a name to a grouping of F# program elements.</span></span> <span data-ttu-id="b4424-105">Espaces de noms sont des éléments en général de niveau supérieur dans F# fichiers.</span><span class="sxs-lookup"><span data-stu-id="b4424-105">Namespaces are typically top-level elements in F# files.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4424-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4424-106">Syntax</span></span>

```fsharp
namespace [rec] [parent-namespaces.]identifier
```

## <a name="remarks"></a><span data-ttu-id="b4424-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b4424-107">Remarks</span></span>

<span data-ttu-id="b4424-108">Si vous souhaitez placer le code dans un espace de noms, la première déclaration dans le fichier doit déclarer l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b4424-108">If you want to put code in a namespace, the first declaration in the file must declare the namespace.</span></span> <span data-ttu-id="b4424-109">Le contenu du fichier entier puis deviennent partie intégrante de l’espace de noms, fournie par aucune autre déclaration d’espaces de noms n’existe plus dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="b4424-109">The contents of the entire file then become part of the namespace, provided no other namespaces declaration exists further in the file.</span></span> <span data-ttu-id="b4424-110">Si tel est le cas, tout le code jusqu'à la déclaration d’espace de noms suivant est considéré comme se situer dans le premier espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b4424-110">If that is the case, then all code up until the next namespace declaration is considered to be within the first namespace.</span></span>

<span data-ttu-id="b4424-111">Espaces de noms ne peut pas contenir directement les fonctions et les valeurs.</span><span class="sxs-lookup"><span data-stu-id="b4424-111">Namespaces cannot directly contain values and functions.</span></span> <span data-ttu-id="b4424-112">Au lieu de cela, les fonctions et les valeurs doivent figurer dans les modules et les modules sont inclus dans les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="b4424-112">Instead, values and functions must be included in modules, and modules are included in namespaces.</span></span> <span data-ttu-id="b4424-113">Espaces de noms peuvent contenir des types, des modules.</span><span class="sxs-lookup"><span data-stu-id="b4424-113">Namespaces can contain types, modules.</span></span>

<span data-ttu-id="b4424-114">Commentaires de documentation XML peuvent être déclarés au-dessus d’un espace de noms, mais ils sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="b4424-114">XML doc comments can be declared above a namespace, but they're ignored.</span></span> <span data-ttu-id="b4424-115">Directives de compilateur peuvent également être déclarées au-dessus d’un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b4424-115">Compiler directives can also be declared above a namespace.</span></span>

<span data-ttu-id="b4424-116">Espaces de noms peuvent être déclarés explicitement avec le mot clé d’espace de noms, ou implicitement lors de la déclaration d’un module.</span><span class="sxs-lookup"><span data-stu-id="b4424-116">Namespaces can be declared explicitly with the namespace keyword, or implicitly when declaring a module.</span></span> <span data-ttu-id="b4424-117">Pour déclarer un espace de noms explicitement, utilisez le mot clé namespace suivi du nom de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b4424-117">To declare a namespace explicitly, use the namespace keyword followed by the namespace name.</span></span> <span data-ttu-id="b4424-118">L’exemple suivant montre un fichier de code qui déclare un espace de noms `Widgets` avec un type et un module inclus dans cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b4424-118">The following example shows a code file that declares a namespace `Widgets` with a type and a module included in that namespace.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6406.fs)]

<span data-ttu-id="b4424-119">Si tout le contenu du fichier est dans un module, vous pouvez également déclarer espaces de noms implicitement à l’aide de la `module` mot clé et en fournissant le nouveau nom de l’espace de noms dans le nom qualifié complet du module.</span><span class="sxs-lookup"><span data-stu-id="b4424-119">If the entire contents of the file are in one module, you can also declare namespaces implicitly by using the `module` keyword and providing the new namespace name in the fully qualified module name.</span></span> <span data-ttu-id="b4424-120">L’exemple suivant montre un fichier de code qui déclare un espace de noms `Widgets` et un module `WidgetsModule`, qui contient une fonction.</span><span class="sxs-lookup"><span data-stu-id="b4424-120">The following example shows a code file that declares a namespace `Widgets` and a module `WidgetsModule`, which contains a function.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6401.fs)]

<span data-ttu-id="b4424-121">Le code suivant est équivalent au code précédent, mais le module est une déclaration de module locale.</span><span class="sxs-lookup"><span data-stu-id="b4424-121">The following code is equivalent to the preceding code, but the module is a local module declaration.</span></span> <span data-ttu-id="b4424-122">Dans ce cas, l’espace de noms doit apparaître sur sa propre ligne.</span><span class="sxs-lookup"><span data-stu-id="b4424-122">In that case, the namespace must appear on its own line.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/namespaces/snippet6402.fs)]

<span data-ttu-id="b4424-123">Si plusieurs modules est requis dans le même fichier dans un ou plusieurs espaces de noms, vous devez utiliser des déclarations de module locales.</span><span class="sxs-lookup"><span data-stu-id="b4424-123">If more than one module is required in the same file in one or more namespaces, you must use local module declarations.</span></span> <span data-ttu-id="b4424-124">Lorsque vous utilisez des déclarations de module locales, vous ne pouvez pas utiliser l’espace de noms qualifié dans les déclarations de module.</span><span class="sxs-lookup"><span data-stu-id="b4424-124">When you use local module declarations, you cannot use the qualified namespace in the module declarations.</span></span> <span data-ttu-id="b4424-125">Le code suivant montre un fichier qui a une déclaration d’espace de noms et deux déclarations de module locales.</span><span class="sxs-lookup"><span data-stu-id="b4424-125">The following code shows a file that has a namespace declaration and two local module declarations.</span></span> <span data-ttu-id="b4424-126">Dans ce cas, les modules sont contenus directement dans l’espace de noms ; Il n’existe aucun module créé implicitement qui porte le même nom que le fichier.</span><span class="sxs-lookup"><span data-stu-id="b4424-126">In this case, the modules are contained directly in the namespace; there is no implicitly created module that has the same name as the file.</span></span> <span data-ttu-id="b4424-127">N’importe quel autre code dans le fichier, comme un `do` , la liaison est dans l’espace de noms mais pas dans les modules internes, vous devez qualifier le membre de module `widgetFunction` en utilisant le nom de module.</span><span class="sxs-lookup"><span data-stu-id="b4424-127">Any other code in the file, such as a `do` binding, is in the namespace but not in the inner modules, so you need to qualify the module member `widgetFunction` by using the module name.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6403.fs)]

<span data-ttu-id="b4424-128">La sortie de cet exemple est la suivante.</span><span class="sxs-lookup"><span data-stu-id="b4424-128">The output of this example is as follows.</span></span>

```fsharp
Module1 10 20
Module2 5 6
```

<span data-ttu-id="b4424-129">Pour plus d’informations, consultez [Modules](modules.md).</span><span class="sxs-lookup"><span data-stu-id="b4424-129">For more information, see [Modules](modules.md).</span></span>

## <a name="nested-namespaces"></a><span data-ttu-id="b4424-130">Espaces de noms imbriqués</span><span class="sxs-lookup"><span data-stu-id="b4424-130">Nested Namespaces</span></span>

<span data-ttu-id="b4424-131">Lorsque vous créez un espace de noms imbriqué, vous devez le qualifier complètement.</span><span class="sxs-lookup"><span data-stu-id="b4424-131">When you create a nested namespace, you must fully qualify it.</span></span> <span data-ttu-id="b4424-132">Sinon, vous créez un nouvel espace de noms de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="b4424-132">Otherwise, you create a new top-level namespace.</span></span> <span data-ttu-id="b4424-133">Mise en retrait est ignorée dans les déclarations d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b4424-133">Indentation is ignored in namespace declarations.</span></span>

<span data-ttu-id="b4424-134">L’exemple suivant montre comment déclarer un espace de noms imbriqué.</span><span class="sxs-lookup"><span data-stu-id="b4424-134">The following example shows how to declare a nested namespace.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6404.fs)]

## <a name="namespaces-in-files-and-assemblies"></a><span data-ttu-id="b4424-135">Espaces de noms dans les fichiers et assemblys</span><span class="sxs-lookup"><span data-stu-id="b4424-135">Namespaces in Files and Assemblies</span></span>

<span data-ttu-id="b4424-136">Espaces de noms peut s’étendre sur plusieurs fichiers dans un projet unique ou de la compilation.</span><span class="sxs-lookup"><span data-stu-id="b4424-136">Namespaces can span multiple files in a single project or compilation.</span></span> <span data-ttu-id="b4424-137">Le terme *fragment de l’espace de noms* décrit la partie d’un espace de noms qui est inclus dans un seul fichier.</span><span class="sxs-lookup"><span data-stu-id="b4424-137">The term *namespace fragment* describes the part of a namespace that is included in one file.</span></span> <span data-ttu-id="b4424-138">Espaces de noms peuvent également couvrir plusieurs assemblys.</span><span class="sxs-lookup"><span data-stu-id="b4424-138">Namespaces can also span multiple assemblies.</span></span> <span data-ttu-id="b4424-139">Par exemple, le `System` espace de noms inclut l’ensemble .NET Framework, qui couvre de nombreux assemblys et contient de nombreux espaces de noms imbriqués.</span><span class="sxs-lookup"><span data-stu-id="b4424-139">For example, the `System` namespace includes the whole .NET Framework, which spans many assemblies and contains many nested namespaces.</span></span>

## <a name="global-namespace"></a><span data-ttu-id="b4424-140">Global Namespace</span><span class="sxs-lookup"><span data-stu-id="b4424-140">Global Namespace</span></span>

<span data-ttu-id="b4424-141">Vous utilisez l’espace de noms prédéfini `global` pour mettre des noms dans l’espace de noms de niveau supérieur de .NET.</span><span class="sxs-lookup"><span data-stu-id="b4424-141">You use the predefined namespace `global` to put names in the .NET top-level namespace.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6407.fs)]

<span data-ttu-id="b4424-142">Vous pouvez également utiliser global pour référencer l’espace de noms .NET niveau supérieur, par exemple, pour résoudre les conflits de noms avec d’autres espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="b4424-142">You can also use global to reference the top-level .NET namespace, for example, to resolve name conflicts with other namespaces.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6408.fs)]

## <a name="recursive-namespaces"></a><span data-ttu-id="b4424-143">Espaces de noms récursive</span><span class="sxs-lookup"><span data-stu-id="b4424-143">Recursive namespaces</span></span>

<span data-ttu-id="b4424-144">Espaces de noms peuvent également être déclarées comme récursive pour autoriser tout le code relation contenant-contenu de s’exclure mutuellement récursives.</span><span class="sxs-lookup"><span data-stu-id="b4424-144">Namespaces can also be declared as recursive to allow for all contained code to be mutually recursive.</span></span>  <span data-ttu-id="b4424-145">Cette opération est effectuée `namespace rec`.</span><span class="sxs-lookup"><span data-stu-id="b4424-145">This is done via `namespace rec`.</span></span> <span data-ttu-id="b4424-146">Utilisation de `namespace rec` peuvent atténuer certains problèmes rencontrés dans l’impossibilité d’écrire du code mutuellement référentielle entre les types et les modules.</span><span class="sxs-lookup"><span data-stu-id="b4424-146">Use of `namespace rec` can alleviate some pains in not being able to write mutually referential code between types and modules.</span></span> <span data-ttu-id="b4424-147">Voici un exemple de ceci :</span><span class="sxs-lookup"><span data-stu-id="b4424-147">The following is an example of this:</span></span>

```fsharp
namespace rec MutualReferences

type Orientation = Up | Down
type PeelState = Peeled | Unpeeled

// This exception depends on the type below.
exception DontSqueezeTheBananaException of Banana

type BananaPeel() = class end

type Banana(orientation : Orientation) =
    member val IsPeeled = false with get, set
    member val Orientation = orientation with get, set
    member val Sides: PeelState list = [ Unpeeled; Unpeeled; Unpeeled; Unpeeled] with get, set

    member self.Peel() = BananaHelpers.peel self // Note the dependency on the BananaHelpers module.
    member self.SqueezeJuiceOut() = raise (DontSqueezeTheBananaException self) // This member depends on the exception above.

module BananaHelpers =
    let peel (b: Banana) =
        let flip (banana: Banana) =
            match banana.Orientation with
            | Up -> 
                banana.Orientation <- Down
                banana
            | Down -> banana

        let peelSides (banana: Banana) =
            banana.Sides
            |> List.map (function
                         | Unpeeled -> Peeled
                         | Peeled -> Peeled)

        match b.Orientation with
        | Up ->   b |> flip |> peelSides
        | Down -> b |> peelSides
```

<span data-ttu-id="b4424-148">Notez que l’exception `DontSqueezeTheBananaException` et la classe `Banana` tous deux se font mutuellement référence.</span><span class="sxs-lookup"><span data-stu-id="b4424-148">Note that the exception `DontSqueezeTheBananaException` and the class `Banana` both refer to each other.</span></span>  <span data-ttu-id="b4424-149">En outre, le module `BananaHelpers` et la classe `Banana` également se font mutuellement référence.</span><span class="sxs-lookup"><span data-stu-id="b4424-149">Additionally, the module `BananaHelpers` and the class `Banana` also refer to each other.</span></span> <span data-ttu-id="b4424-150">Cela ne serait pas possible d’exprimer dans F# si vous avez supprimé le `rec` mot clé à partir de la `MutualReferences` espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b4424-150">This wouldn't be possible to express in F# if you removed the `rec` keyword from the `MutualReferences` namespace.</span></span>

<span data-ttu-id="b4424-151">Cette fonctionnalité est également disponible pour niveau supérieur [Modules](modules.md).</span><span class="sxs-lookup"><span data-stu-id="b4424-151">This feature is also available for top-level [Modules](modules.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b4424-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4424-152">See also</span></span>

- [<span data-ttu-id="b4424-153">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="b4424-153">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="b4424-154">Modules</span><span class="sxs-lookup"><span data-stu-id="b4424-154">Modules</span></span>](modules.md)
- [<span data-ttu-id="b4424-155">F#RFC FS-1009 - autoriser les types mutuellement référentielles et des modules sur des étendues plus grandes dans les fichiers</span><span class="sxs-lookup"><span data-stu-id="b4424-155">F# RFC FS-1009 - Allow mutually referential types and modules over larger scopes within files</span></span>](https://github.com/fsharp/fslang-design/blob/master/FSharp-4.1/FS-1009-mutually-referential-types-and-modules-single-scope.md)
