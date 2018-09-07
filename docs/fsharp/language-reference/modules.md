---
title: Modules (F#)
description: 'Découvrez comment un module F # est un regroupement de code F #, telles que les valeurs, les types et les valeurs de fonction dans un programme F #.'
ms.date: 04/24/2017
ms.openlocfilehash: fb0aa1d508d1141933b4fbdf10633f67ed078dc7
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44048307"
---
# <a name="modules"></a><span data-ttu-id="ad857-103">Modules</span><span class="sxs-lookup"><span data-stu-id="ad857-103">Modules</span></span>

<span data-ttu-id="ad857-104">Dans le contexte du langage F #, un *module* est un regroupement de code F #, telles que les valeurs, les types et les valeurs de fonction dans un programme F #.</span><span class="sxs-lookup"><span data-stu-id="ad857-104">In the context of the F# language, a *module* is a grouping of F# code, such as values, types, and function values, in an F# program.</span></span> <span data-ttu-id="ad857-105">Le regroupement de code en modules vous permet de centraliser le code connexe et d’éviter les conflits de nom dans votre programme.</span><span class="sxs-lookup"><span data-stu-id="ad857-105">Grouping code in modules helps keep related code together and helps avoid name conflicts in your program.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad857-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad857-106">Syntax</span></span>

```fsharp
// Top-level module declaration.
module [accessibility-modifier] [qualified-namespace.]module-name
declarations
// Local module declaration.
module [accessibility-modifier] module-name =
    declarations
```

## <a name="remarks"></a><span data-ttu-id="ad857-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ad857-107">Remarks</span></span>

<span data-ttu-id="ad857-108">Un module F # est un regroupement de constructions de code F # tels que les types, les valeurs, les valeurs de fonction et les code dans `do` liaisons.</span><span class="sxs-lookup"><span data-stu-id="ad857-108">An F# module is a grouping of F# code constructs such as types, values, function values, and code in `do` bindings.</span></span> <span data-ttu-id="ad857-109">Il est implémenté comme une classe du common language runtime (CLR) qui comporte uniquement des membres statiques.</span><span class="sxs-lookup"><span data-stu-id="ad857-109">It is implemented as a common language runtime (CLR) class that has only static members.</span></span> <span data-ttu-id="ad857-110">Il existe deux types de déclarations de module, selon que la totalité du fichier est inclus dans le module : une déclaration de module de niveau supérieur et une déclaration de module locale.</span><span class="sxs-lookup"><span data-stu-id="ad857-110">There are two types of module declarations, depending on whether the whole file is included in the module: a top-level module declaration and a local module declaration.</span></span> <span data-ttu-id="ad857-111">Une déclaration de module de niveau supérieur comprend la totalité du fichier dans le module.</span><span class="sxs-lookup"><span data-stu-id="ad857-111">A top-level module declaration includes the whole file in the module.</span></span> <span data-ttu-id="ad857-112">Une déclaration de module de niveau supérieur peut apparaître uniquement comme la première déclaration dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="ad857-112">A top-level module declaration can appear only as the first declaration in a file.</span></span>

<span data-ttu-id="ad857-113">Dans la syntaxe pour la déclaration de module de niveau supérieur, le paramètre facultatif *espace de noms qualifié* est la séquence de noms de l’espace de noms imbriqué qui contient le module.</span><span class="sxs-lookup"><span data-stu-id="ad857-113">In the syntax for the top-level module declaration, the optional *qualified-namespace* is the sequence of nested namespace names that contains the module.</span></span> <span data-ttu-id="ad857-114">L’espace de noms qualifié ne devra pas être déclaré précédemment.</span><span class="sxs-lookup"><span data-stu-id="ad857-114">The qualified namespace does not have to be previously declared.</span></span>

<span data-ttu-id="ad857-115">Il est inutile de mettre en retrait les déclarations dans un module de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="ad857-115">You do not have to indent declarations in a top-level module.</span></span> <span data-ttu-id="ad857-116">Vous avez à mettre en retrait toutes les déclarations dans les modules locaux.</span><span class="sxs-lookup"><span data-stu-id="ad857-116">You do have to indent all declarations in local modules.</span></span> <span data-ttu-id="ad857-117">Dans une déclaration de module locale, seules les déclarations sont mises en retrait sous cette déclaration de module font partie du module.</span><span class="sxs-lookup"><span data-stu-id="ad857-117">In a local module declaration, only the declarations that are indented under that module declaration are part of the module.</span></span>

<span data-ttu-id="ad857-118">Si un fichier de code ne commence pas par une déclaration de module de niveau supérieur ou une déclaration d’espace de noms, tout le contenu du fichier, y compris tous les modules locaux, devient partie d’un module de niveau supérieur créé implicitement qui porte le même nom que le fichier, sans l’extension, avec la première lettre en majuscules.</span><span class="sxs-lookup"><span data-stu-id="ad857-118">If a code file does not begin with a top-level module declaration or a namespace declaration, the whole contents of the file, including any local modules, becomes part of an implicitly created top-level module that has the same name as the file, without the extension, with the first letter converted to uppercase.</span></span> <span data-ttu-id="ad857-119">Par exemple, considérez le fichier suivant.</span><span class="sxs-lookup"><span data-stu-id="ad857-119">For example, consider the following file.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/modules/snippet6601.fs)]

<span data-ttu-id="ad857-120">Ce fichier est compilé comme s’il était écrit de cette manière :</span><span class="sxs-lookup"><span data-stu-id="ad857-120">This file would be compiled as if it were written in this manner:</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/modules/snippet6602.fs)]

<span data-ttu-id="ad857-121">Si vous avez plusieurs modules dans un fichier, vous devez utiliser une déclaration de module locale pour chaque module.</span><span class="sxs-lookup"><span data-stu-id="ad857-121">If you have multiple modules in a file, you must use a local module declaration for each module.</span></span> <span data-ttu-id="ad857-122">Si un espace de noms englobant est déclaré, ces modules font partie de l’espace de noms englobant.</span><span class="sxs-lookup"><span data-stu-id="ad857-122">If an enclosing namespace is declared, these modules are part of the enclosing namespace.</span></span> <span data-ttu-id="ad857-123">Si un espace de noms englobant n’est pas déclaré, les modules deviennent partie intégrante du module de niveau supérieur créé implicitement.</span><span class="sxs-lookup"><span data-stu-id="ad857-123">If an enclosing namespace is not declared, the modules become part of the implicitly created top-level module.</span></span> <span data-ttu-id="ad857-124">L’exemple de code suivant montre un fichier de code qui contient plusieurs modules.</span><span class="sxs-lookup"><span data-stu-id="ad857-124">The following code example shows a code file that contains multiple modules.</span></span> <span data-ttu-id="ad857-125">Le compilateur crée implicitement un module de niveau supérieur nommé `Multiplemodules`, et `MyModule1` et `MyModule2` sont imbriqués dans ce module de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="ad857-125">The compiler implicitly creates a top-level module named `Multiplemodules`, and `MyModule1` and `MyModule2` are nested in that top-level module.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/modules/snippet6603.fs)]

<span data-ttu-id="ad857-126">Si vous avez plusieurs fichiers dans un projet ou dans une seule compilation, ou si vous générez une bibliothèque, vous devez inclure une déclaration d’espace de noms ou module en haut du fichier.</span><span class="sxs-lookup"><span data-stu-id="ad857-126">If you have multiple files in a project or in a single compilation, or if you are building a library, you must include a namespace declaration or module declaration at the top of the file.</span></span> <span data-ttu-id="ad857-127">Le compilateur F # détermine uniquement un nom de module implicitement lorsqu’il existe un seul fichier dans une ligne de commande de compilation ou de projet, et que vous créez une application.</span><span class="sxs-lookup"><span data-stu-id="ad857-127">The F# compiler only determines a module name implicitly when there is only one file in a project or compilation command line, and you are creating an application.</span></span>

<span data-ttu-id="ad857-128">Le *-modificateur d’accessibilité* peut prendre l’une des opérations suivantes : `public`, `private`, `internal`.</span><span class="sxs-lookup"><span data-stu-id="ad857-128">The *accessibility-modifier* can be one of the following: `public`, `private`, `internal`.</span></span> <span data-ttu-id="ad857-129">Pour plus d’informations, consultez [Contrôle d’accès](access-control.md).</span><span class="sxs-lookup"><span data-stu-id="ad857-129">For more information, see [Access Control](access-control.md).</span></span> <span data-ttu-id="ad857-130">La valeur par défaut est « public ».</span><span class="sxs-lookup"><span data-stu-id="ad857-130">The default is public.</span></span>

## <a name="referencing-code-in-modules"></a><span data-ttu-id="ad857-131">Code de référencement dans des Modules</span><span class="sxs-lookup"><span data-stu-id="ad857-131">Referencing Code in Modules</span></span>

<span data-ttu-id="ad857-132">Lorsque vous référencez des fonctions, des types et des valeurs à partir d’un autre module, vous devez utiliser un nom qualifié ou ouvrez le module.</span><span class="sxs-lookup"><span data-stu-id="ad857-132">When you reference functions, types, and values from another module, you must either use a qualified name or open the module.</span></span> <span data-ttu-id="ad857-133">Si vous utilisez un nom qualifié, vous devez spécifier les espaces de noms, le module et l’identificateur de l’élément de programme.</span><span class="sxs-lookup"><span data-stu-id="ad857-133">If you use a qualified name, you must specify the namespaces, the module, and the identifier for the program element you want.</span></span> <span data-ttu-id="ad857-134">Vous séparez chaque partie du chemin d’accès qualifié par un point (.), comme suit.</span><span class="sxs-lookup"><span data-stu-id="ad857-134">You separate each part of the qualified path with a dot (.), as follows.</span></span>

`Namespace1.Namespace2.ModuleName.Identifier`

<span data-ttu-id="ad857-135">Vous pouvez ouvrir le module ou un ou plusieurs des espaces de noms pour simplifier le code.</span><span class="sxs-lookup"><span data-stu-id="ad857-135">You can open the module or one or more of the namespaces to simplify the code.</span></span> <span data-ttu-id="ad857-136">Pour plus d’informations sur les espaces de noms ouverture et de modules, consultez [déclarations d’importation : le `open` mot clé](import-declarations-the-open-keyword.md).</span><span class="sxs-lookup"><span data-stu-id="ad857-136">For more information about opening namespaces and modules, see [Import Declarations: The `open` Keyword](import-declarations-the-open-keyword.md).</span></span>

<span data-ttu-id="ad857-137">L’exemple de code suivant montre un module de niveau supérieur qui contient tout le code jusqu'à la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="ad857-137">The following code example shows a top-level module that contains all the code up to the end of the file.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/modules/snippet6604.fs)]

<span data-ttu-id="ad857-138">Pour utiliser ce code à partir d’un autre fichier dans le même projet, vous utiliser des noms qualifiés ou ouvrir le module avant d’utiliser les fonctions, comme indiqué dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="ad857-138">To use this code from another file in the same project, you either use qualified names or you open the module before you use the functions, as shown in the following examples.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/modules/snippet6605.fs)]

## <a name="nested-modules"></a><span data-ttu-id="ad857-139">Modules imbriqués</span><span class="sxs-lookup"><span data-stu-id="ad857-139">Nested Modules</span></span>

<span data-ttu-id="ad857-140">Les modules peuvent être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="ad857-140">Modules can be nested.</span></span> <span data-ttu-id="ad857-141">Modules internes doivent être mises en retrait en ce qui concerne les déclarations de module externe pour indiquer qu’ils sont des modules internes, pas de nouveaux modules.</span><span class="sxs-lookup"><span data-stu-id="ad857-141">Inner modules must be indented as far as outer module declarations to indicate that they are inner modules, not new modules.</span></span> <span data-ttu-id="ad857-142">Par exemple, comparez les deux exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="ad857-142">For example, compare the following two examples.</span></span> <span data-ttu-id="ad857-143">Module `Z` est un module interne dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="ad857-143">Module `Z` is an inner module in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/modules/snippet6607.fs)]

<span data-ttu-id="ad857-144">Mais le module `Z` est un frère du module `Y` dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="ad857-144">But module `Z` is a sibling to module `Y` in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/modules/snippet6608.fs)]
<span data-ttu-id="ad857-145">Module `Z` est également un module frère dans le code suivant, car il n’est pas mis en retrait en ce qui concerne les autres déclarations de module `Y`.</span><span class="sxs-lookup"><span data-stu-id="ad857-145">Module `Z` is also a sibling module in the following code, because it is not indented as far as other declarations in module `Y`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/modules/snippet6609.fs)]
<span data-ttu-id="ad857-146">Enfin, si le module externe a pas de déclarations et est suivi immédiatement par une autre déclaration de module, la nouvelle déclaration de module est considéré comme un module interne, mais le compilateur vous avertit si la deuxième définition de module n’est pas mis en retrait règle le première.</span><span class="sxs-lookup"><span data-stu-id="ad857-146">Finally, if the outer module has no declarations and is followed immediately by another module declaration, the new module declaration is assumed to be an inner module, but the compiler will warn you if the second module definition is not indented farther than the first.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/modules/snippet6610.fs)]
<span data-ttu-id="ad857-147">Pour éliminer l’avertissement, mettre en retrait le module interne.</span><span class="sxs-lookup"><span data-stu-id="ad857-147">To eliminate the warning, indent the inner module.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/modules/snippet6611.fs)]
<span data-ttu-id="ad857-148">Si vous souhaitez tout le code dans un fichier dans un seul module externe et vous souhaitez que les modules internes, le module externe ne requiert pas le signe égal, et les déclarations, y compris toutes les déclarations de module interne qui iront dans le module externe n’ont pas à être mis en retrait.</span><span class="sxs-lookup"><span data-stu-id="ad857-148">If you want all the code in a file to be in a single outer module and you want inner modules, the outer module does not require the equal sign, and the declarations, including any inner module declarations, that will go in the outer module do not have to be indented.</span></span> <span data-ttu-id="ad857-149">Déclarations dans les déclarations de module interne doivent être mis en retrait.</span><span class="sxs-lookup"><span data-stu-id="ad857-149">Declarations inside the inner module declarations do have to be indented.</span></span> <span data-ttu-id="ad857-150">Le code suivant illustre ce cas.</span><span class="sxs-lookup"><span data-stu-id="ad857-150">The following code shows this case.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/modules/snippet6612.fs)]

## <a name="recursive-modules"></a><span data-ttu-id="ad857-151">Modules récursive</span><span class="sxs-lookup"><span data-stu-id="ad857-151">Recursive modules</span></span>

<span data-ttu-id="ad857-152">F # 4.1 introduit la notion de modules qui permettent la relation contenant-contenu tout le code d’être mutuellement récursives.</span><span class="sxs-lookup"><span data-stu-id="ad857-152">F# 4.1 introduces the notion of modules which allow for all contained code to be mutually recursive.</span></span>  <span data-ttu-id="ad857-153">Cette opération est effectuée `module rec`.</span><span class="sxs-lookup"><span data-stu-id="ad857-153">This is done via `module rec`.</span></span>  <span data-ttu-id="ad857-154">Utilisation de `module rec` peuvent atténuer certains problèmes rencontrés dans l’impossibilité d’écrire du code mutuellement référentielle entre les types et les modules.</span><span class="sxs-lookup"><span data-stu-id="ad857-154">Use of `module rec` can alleviate some pains in not being able to write mutually referential code between types and modules.</span></span>  <span data-ttu-id="ad857-155">Voici un exemple de ceci :</span><span class="sxs-lookup"><span data-stu-id="ad857-155">The following is an example of this:</span></span>

```fsharp
module rec RecursiveModule =
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

<span data-ttu-id="ad857-156">Notez que l’exception `DontSqueezeTheBananaException` et la classe `Banana` tous deux se font mutuellement référence.</span><span class="sxs-lookup"><span data-stu-id="ad857-156">Note that the exception `DontSqueezeTheBananaException` and the class `Banana` both refer to each other.</span></span>  <span data-ttu-id="ad857-157">En outre, le module `BananaHelpers` et la classe `Banana` également se font mutuellement référence.</span><span class="sxs-lookup"><span data-stu-id="ad857-157">Additionally, the module `BananaHelpers` and the class `Banana` also refer to each other.</span></span>  <span data-ttu-id="ad857-158">Cela ne serait pas possible d’exprimer en F # si vous avez supprimé le `rec` mot clé à partir de la `RecursiveModule` module.</span><span class="sxs-lookup"><span data-stu-id="ad857-158">This would not be possible to express in F# if you removed the `rec` keyword from the `RecursiveModule` module.</span></span>

<span data-ttu-id="ad857-159">Cette fonctionnalité est également possible dans [espaces de noms](namespaces.md) avec F # 4.1.</span><span class="sxs-lookup"><span data-stu-id="ad857-159">This capability is also possible in [Namespaces](namespaces.md) with F# 4.1.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad857-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad857-160">See also</span></span>

- [<span data-ttu-id="ad857-161">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="ad857-161">F# Language Reference</span></span>](index.md)  
- [<span data-ttu-id="ad857-162">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="ad857-162">Namespaces</span></span>](namespaces.md)  
- [<span data-ttu-id="ad857-163">F # RFC FS-1009 - autoriser les types mutuellement référentielles et des modules sur des étendues plus grandes dans les fichiers</span><span class="sxs-lookup"><span data-stu-id="ad857-163">F# RFC FS-1009 - Allow mutually referential types and modules over larger scopes within files</span></span>](https://github.com/fsharp/fslang-design/blob/master/FSharp-4.1/FS-1009-mutually-referential-types-and-modules-single-scope.md)  
