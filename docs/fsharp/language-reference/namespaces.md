---
title: Espaces de noms (F#)
description: Découvrez comment un espace de noms F# permet d’organiser le code en zones de fonctionnalités connexes en vous permettant de joindre un nom à un regroupement d’éléments de programme.
ms.date: 04/24/2017
ms.openlocfilehash: 769a1241f76ac32d3a6a80bd637078493119bb3c
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "44178251"
---
# <a name="namespaces"></a><span data-ttu-id="27166-103">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="27166-103">Namespaces</span></span>

<span data-ttu-id="27166-104">Un espace de noms vous permet d’organiser le code en zones de fonctionnalités connexes. Pour cela, vous attachez un nom à un regroupement d’éléments de programme.</span><span class="sxs-lookup"><span data-stu-id="27166-104">A namespace lets you organize code into areas of related functionality by enabling you to attach a name to a grouping of program elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="27166-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27166-105">Syntax</span></span>

```fsharp
namespace [parent-namespaces.]identifier
```

## <a name="remarks"></a><span data-ttu-id="27166-106">Notes</span><span class="sxs-lookup"><span data-stu-id="27166-106">Remarks</span></span>

<span data-ttu-id="27166-107">Si vous souhaitez placer le code dans un espace de noms, la première déclaration dans le fichier doit déclarer l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="27166-107">If you want to put code in a namespace, the first declaration in the file must declare the namespace.</span></span> <span data-ttu-id="27166-108">Le contenu du fichier entier fait alors partie de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="27166-108">The contents of the entire file then become part of the namespace.</span></span>

<span data-ttu-id="27166-109">Espaces de noms ne peut pas contenir directement les fonctions et les valeurs.</span><span class="sxs-lookup"><span data-stu-id="27166-109">Namespaces cannot directly contain values and functions.</span></span> <span data-ttu-id="27166-110">Au lieu de cela, les fonctions et les valeurs doivent figurer dans les modules et les modules sont inclus dans les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="27166-110">Instead, values and functions must be included in modules, and modules are included in namespaces.</span></span> <span data-ttu-id="27166-111">Espaces de noms peuvent contenir des types, des modules.</span><span class="sxs-lookup"><span data-stu-id="27166-111">Namespaces can contain types, modules.</span></span>

<span data-ttu-id="27166-112">Espaces de noms peuvent être déclarés explicitement avec le mot clé d’espace de noms, ou implicitement lors de la déclaration d’un module.</span><span class="sxs-lookup"><span data-stu-id="27166-112">Namespaces can be declared explicitly with the namespace keyword, or implicitly when declaring a module.</span></span> <span data-ttu-id="27166-113">Pour déclarer un espace de noms explicitement, utilisez le mot clé namespace suivi du nom de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="27166-113">To declare a namespace explicitly, use the namespace keyword followed by the namespace name.</span></span> <span data-ttu-id="27166-114">L’exemple suivant montre un fichier de code qui déclare un espace de noms Widgets avec un type et un module inclus dans cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="27166-114">The following example shows a code file that declares a namespace Widgets with a type and a module included in that namespace.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6406.fs)]

<span data-ttu-id="27166-115">Si tout le contenu du fichier est dans un module, vous pouvez également déclarer espaces de noms implicitement à l’aide de la `module` mot clé et en fournissant le nouveau nom de l’espace de noms dans le nom qualifié complet du module.</span><span class="sxs-lookup"><span data-stu-id="27166-115">If the entire contents of the file are in one module, you can also declare namespaces implicitly by using the `module` keyword and providing the new namespace name in the fully qualified module name.</span></span> <span data-ttu-id="27166-116">L’exemple suivant montre un fichier de code qui déclare un espace de noms `Widgets` et un module `WidgetsModule`, qui contient une fonction.</span><span class="sxs-lookup"><span data-stu-id="27166-116">The following example shows a code file that declares a namespace `Widgets` and a module `WidgetsModule`, which contains a function.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6401.fs)]

<span data-ttu-id="27166-117">Le code suivant est équivalent au code précédent, mais le module est une déclaration de module locale.</span><span class="sxs-lookup"><span data-stu-id="27166-117">The following code is equivalent to the preceding code, but the module is a local module declaration.</span></span> <span data-ttu-id="27166-118">Dans ce cas, l’espace de noms doit apparaître sur sa propre ligne.</span><span class="sxs-lookup"><span data-stu-id="27166-118">In that case, the namespace must appear on its own line.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/namespaces/snippet6402.fs)]

<span data-ttu-id="27166-119">Si plusieurs modules est requis dans le même fichier dans un ou plusieurs espaces de noms, vous devez utiliser des déclarations de module locales.</span><span class="sxs-lookup"><span data-stu-id="27166-119">If more than one module is required in the same file in one or more namespaces, you must use local module declarations.</span></span> <span data-ttu-id="27166-120">Lorsque vous utilisez des déclarations de module locales, vous ne pouvez pas utiliser l’espace de noms qualifié dans les déclarations de module.</span><span class="sxs-lookup"><span data-stu-id="27166-120">When you use local module declarations, you cannot use the qualified namespace in the module declarations.</span></span> <span data-ttu-id="27166-121">Le code suivant montre un fichier qui a une déclaration d’espace de noms et deux déclarations de module locales.</span><span class="sxs-lookup"><span data-stu-id="27166-121">The following code shows a file that has a namespace declaration and two local module declarations.</span></span> <span data-ttu-id="27166-122">Dans ce cas, les modules sont contenus directement dans l’espace de noms ; Il n’existe aucun module créé implicitement qui porte le même nom que le fichier.</span><span class="sxs-lookup"><span data-stu-id="27166-122">In this case, the modules are contained directly in the namespace; there is no implicitly created module that has the same name as the file.</span></span> <span data-ttu-id="27166-123">N’importe quel autre code dans le fichier, comme un `do` , la liaison est dans l’espace de noms mais pas dans les modules internes, vous devez qualifier le membre de module `widgetFunction` en utilisant le nom de module.</span><span class="sxs-lookup"><span data-stu-id="27166-123">Any other code in the file, such as a `do` binding, is in the namespace but not in the inner modules, so you need to qualify the module member `widgetFunction` by using the module name.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6403.fs)]

<span data-ttu-id="27166-124">La sortie de cet exemple est la suivante.</span><span class="sxs-lookup"><span data-stu-id="27166-124">The output of this example is as follows.</span></span>

```fsharp
Module1 10 20
Module2 5 6
```

<span data-ttu-id="27166-125">Pour plus d’informations, consultez [Modules](modules.md).</span><span class="sxs-lookup"><span data-stu-id="27166-125">For more information, see [Modules](modules.md).</span></span>

## <a name="nested-namespaces"></a><span data-ttu-id="27166-126">Espaces de noms imbriqués</span><span class="sxs-lookup"><span data-stu-id="27166-126">Nested Namespaces</span></span>

<span data-ttu-id="27166-127">Lorsque vous créez un espace de noms imbriqué, vous devez le qualifier complètement.</span><span class="sxs-lookup"><span data-stu-id="27166-127">When you create a nested namespace, you must fully qualify it.</span></span> <span data-ttu-id="27166-128">Sinon, vous créez un nouvel espace de noms de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="27166-128">Otherwise, you create a new top-level namespace.</span></span> <span data-ttu-id="27166-129">Mise en retrait est ignorée dans les déclarations d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="27166-129">Indentation is ignored in namespace declarations.</span></span>

<span data-ttu-id="27166-130">L’exemple suivant montre comment déclarer un espace de noms imbriqué.</span><span class="sxs-lookup"><span data-stu-id="27166-130">The following example shows how to declare a nested namespace.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6404.fs)]

## <a name="namespaces-in-files-and-assemblies"></a><span data-ttu-id="27166-131">Espaces de noms dans les fichiers et assemblys</span><span class="sxs-lookup"><span data-stu-id="27166-131">Namespaces in Files and Assemblies</span></span>

<span data-ttu-id="27166-132">Espaces de noms peut s’étendre sur plusieurs fichiers dans un projet unique ou de la compilation.</span><span class="sxs-lookup"><span data-stu-id="27166-132">Namespaces can span multiple files in a single project or compilation.</span></span> <span data-ttu-id="27166-133">Le terme *fragment de l’espace de noms* décrit la partie d’un espace de noms qui est inclus dans un seul fichier.</span><span class="sxs-lookup"><span data-stu-id="27166-133">The term *namespace fragment* describes the part of a namespace that is included in one file.</span></span> <span data-ttu-id="27166-134">Espaces de noms peuvent également couvrir plusieurs assemblys.</span><span class="sxs-lookup"><span data-stu-id="27166-134">Namespaces can also span multiple assemblies.</span></span> <span data-ttu-id="27166-135">Par exemple, le `System` espace de noms inclut l’ensemble .NET Framework, qui couvre de nombreux assemblys et contient de nombreux espaces de noms imbriqués.</span><span class="sxs-lookup"><span data-stu-id="27166-135">For example, the `System` namespace includes the whole .NET Framework, which spans many assemblies and contains many nested namespaces.</span></span>

## <a name="global-namespace"></a><span data-ttu-id="27166-136">Global Namespace</span><span class="sxs-lookup"><span data-stu-id="27166-136">Global Namespace</span></span>

<span data-ttu-id="27166-137">Vous utilisez l’espace de noms prédéfini `global` pour mettre des noms dans l’espace de noms de niveau supérieur de .NET.</span><span class="sxs-lookup"><span data-stu-id="27166-137">You use the predefined namespace `global` to put names in the .NET top-level namespace.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6407.fs)]

<span data-ttu-id="27166-138">Vous pouvez également utiliser global pour référencer l’espace de noms .NET niveau supérieur, par exemple, pour résoudre les conflits de noms avec d’autres espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="27166-138">You can also use global to reference the top-level .NET namespace, for example, to resolve name conflicts with other namespaces.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6408.fs)]

## <a name="recursive-namespaces"></a><span data-ttu-id="27166-139">Espaces de noms récursive</span><span class="sxs-lookup"><span data-stu-id="27166-139">Recursive namespaces</span></span>

<span data-ttu-id="27166-140">F# 4.1 introduit la notion d’espaces de noms qui autorisent tout le code relation contenant-contenu de s’exclure mutuellement récursives.</span><span class="sxs-lookup"><span data-stu-id="27166-140">F# 4.1 introduces the notion of namespaces which allow for all contained code to be mutually recursive.</span></span>  <span data-ttu-id="27166-141">Cette opération est effectuée `namespace rec`.</span><span class="sxs-lookup"><span data-stu-id="27166-141">This is done via `namespace rec`.</span></span>  <span data-ttu-id="27166-142">Utilisation de `namespace rec` peuvent atténuer certains problèmes rencontrés dans l’impossibilité d’écrire du code mutuellement référentielle entre les types et les modules.</span><span class="sxs-lookup"><span data-stu-id="27166-142">Use of `namespace rec` can alleviate some pains in not being able to write mutually referential code between types and modules.</span></span>  <span data-ttu-id="27166-143">Voici un exemple de ceci :</span><span class="sxs-lookup"><span data-stu-id="27166-143">The following is an example of this:</span></span>

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

<span data-ttu-id="27166-144">Notez que l’exception `DontSqueezeTheBananaException` et la classe `Banana` tous deux se font mutuellement référence.</span><span class="sxs-lookup"><span data-stu-id="27166-144">Note that the exception `DontSqueezeTheBananaException` and the class `Banana` both refer to each other.</span></span>  <span data-ttu-id="27166-145">En outre, le module `BananaHelpers` et la classe `Banana` également se font mutuellement référence.</span><span class="sxs-lookup"><span data-stu-id="27166-145">Additionally, the module `BananaHelpers` and the class `Banana` also refer to each other.</span></span>  <span data-ttu-id="27166-146">Cela ne serait pas possible d’exprimer en F# si vous avez supprimé le `rec` mot clé à partir de la `MutualReferences` espace de noms.</span><span class="sxs-lookup"><span data-stu-id="27166-146">This would not be possible to express in F# if you removed the `rec` keyword from the `MutualReferences` namespace.</span></span>

<span data-ttu-id="27166-147">Cette fonctionnalité est également disponible pour niveau supérieur [Modules](modules.md) dans F# 4.1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="27166-147">This feature is also available for top-level [Modules](modules.md) in F# 4.1 or higher.</span></span>

## <a name="see-also"></a><span data-ttu-id="27166-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27166-148">See also</span></span>

- [<span data-ttu-id="27166-149">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="27166-149">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="27166-150">Modules</span><span class="sxs-lookup"><span data-stu-id="27166-150">Modules</span></span>](modules.md)
- [<span data-ttu-id="27166-151">F# RFC FS-1009 - autoriser les types mutuellement référentielles et des modules sur des étendues plus grandes dans les fichiers</span><span class="sxs-lookup"><span data-stu-id="27166-151">F# RFC FS-1009 - Allow mutually referential types and modules over larger scopes within files</span></span>](https://github.com/fsharp/fslang-design/blob/master/FSharp-4.1/FS-1009-mutually-referential-types-and-modules-single-scope.md)
