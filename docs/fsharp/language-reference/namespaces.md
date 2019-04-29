---
title: Espaces de noms
description: Découvrez comment un F# espace de noms vous permet d’organiser le code en zones de fonctionnalités connexes en vous permettant de joindre un nom à un regroupement d’éléments de programme.
ms.date: 12/08/2018
ms.openlocfilehash: 526d7a07e4804751811c15fa91b0c74c1954d591
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61666389"
---
# <a name="namespaces"></a>Espaces de noms

Un espace de noms vous permet d’organiser le code en zones de fonctionnalités connexes en vous permettant de joindre un nom à un regroupement de F# éléments de programme. Espaces de noms sont des éléments en général de niveau supérieur dans F# fichiers.

## <a name="syntax"></a>Syntaxe

```fsharp
namespace [rec] [parent-namespaces.]identifier
```

## <a name="remarks"></a>Notes

Si vous souhaitez placer le code dans un espace de noms, la première déclaration dans le fichier doit déclarer l’espace de noms. Le contenu du fichier entier puis deviennent partie intégrante de l’espace de noms, fournie par aucune autre déclaration d’espaces de noms n’existe plus dans le fichier. Si tel est le cas, tout le code jusqu'à la déclaration d’espace de noms suivant est considéré comme se situer dans le premier espace de noms.

Espaces de noms ne peut pas contenir directement les fonctions et les valeurs. Au lieu de cela, les fonctions et les valeurs doivent figurer dans les modules et les modules sont inclus dans les espaces de noms. Espaces de noms peuvent contenir des types, des modules.

Commentaires de documentation XML peuvent être déclarés au-dessus d’un espace de noms, mais ils sont ignorés. Directives de compilateur peuvent également être déclarées au-dessus d’un espace de noms.

Espaces de noms peuvent être déclarés explicitement avec le mot clé d’espace de noms, ou implicitement lors de la déclaration d’un module. Pour déclarer un espace de noms explicitement, utilisez le mot clé namespace suivi du nom de l’espace de noms. L’exemple suivant montre un fichier de code qui déclare un espace de noms `Widgets` avec un type et un module inclus dans cet espace de noms.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6406.fs)]

Si tout le contenu du fichier est dans un module, vous pouvez également déclarer espaces de noms implicitement à l’aide de la `module` mot clé et en fournissant le nouveau nom de l’espace de noms dans le nom qualifié complet du module. L’exemple suivant montre un fichier de code qui déclare un espace de noms `Widgets` et un module `WidgetsModule`, qui contient une fonction.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6401.fs)]

Le code suivant est équivalent au code précédent, mais le module est une déclaration de module locale. Dans ce cas, l’espace de noms doit apparaître sur sa propre ligne.

[!code-fsharp[Main](../../../samples/snippets/fsharp/namespaces/snippet6402.fs)]

Si plusieurs modules est requis dans le même fichier dans un ou plusieurs espaces de noms, vous devez utiliser des déclarations de module locales. Lorsque vous utilisez des déclarations de module locales, vous ne pouvez pas utiliser l’espace de noms qualifié dans les déclarations de module. Le code suivant montre un fichier qui a une déclaration d’espace de noms et deux déclarations de module locales. Dans ce cas, les modules sont contenus directement dans l’espace de noms ; Il n’existe aucun module créé implicitement qui porte le même nom que le fichier. N’importe quel autre code dans le fichier, comme un `do` , la liaison est dans l’espace de noms mais pas dans les modules internes, vous devez qualifier le membre de module `widgetFunction` en utilisant le nom de module.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6403.fs)]

La sortie de cet exemple est la suivante.

```fsharp
Module1 10 20
Module2 5 6
```

Pour plus d’informations, consultez [Modules](modules.md).

## <a name="nested-namespaces"></a>Espaces de noms imbriqués

Lorsque vous créez un espace de noms imbriqué, vous devez le qualifier complètement. Sinon, vous créez un nouvel espace de noms de niveau supérieur. Mise en retrait est ignorée dans les déclarations d’espace de noms.

L’exemple suivant montre comment déclarer un espace de noms imbriqué.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6404.fs)]

## <a name="namespaces-in-files-and-assemblies"></a>Espaces de noms dans les fichiers et assemblys

Espaces de noms peut s’étendre sur plusieurs fichiers dans un projet unique ou de la compilation. Le terme *fragment de l’espace de noms* décrit la partie d’un espace de noms qui est inclus dans un seul fichier. Espaces de noms peuvent également couvrir plusieurs assemblys. Par exemple, le `System` espace de noms inclut l’ensemble .NET Framework, qui couvre de nombreux assemblys et contient de nombreux espaces de noms imbriqués.

## <a name="global-namespace"></a>Global Namespace

Vous utilisez l’espace de noms prédéfini `global` pour mettre des noms dans l’espace de noms de niveau supérieur de .NET.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6407.fs)]

Vous pouvez également utiliser global pour référencer l’espace de noms .NET niveau supérieur, par exemple, pour résoudre les conflits de noms avec d’autres espaces de noms.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6408.fs)]

## <a name="recursive-namespaces"></a>Espaces de noms récursive

Espaces de noms peuvent également être déclarées comme récursive pour autoriser tout le code relation contenant-contenu de s’exclure mutuellement récursives.  Cette opération est effectuée `namespace rec`. Utilisation de `namespace rec` peuvent atténuer certains problèmes rencontrés dans l’impossibilité d’écrire du code mutuellement référentielle entre les types et les modules. Voici un exemple de ceci :

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

Notez que l’exception `DontSqueezeTheBananaException` et la classe `Banana` tous deux se font mutuellement référence.  En outre, le module `BananaHelpers` et la classe `Banana` également se font mutuellement référence. Cela ne serait pas possible d’exprimer dans F# si vous avez supprimé le `rec` mot clé à partir de la `MutualReferences` espace de noms.

Cette fonctionnalité est également disponible pour niveau supérieur [Modules](modules.md).

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Modules](modules.md)
- [F#RFC FS-1009 - autoriser les types mutuellement référentielles et des modules sur des étendues plus grandes dans les fichiers](https://github.com/fsharp/fslang-design/blob/master/FSharp-4.1/FS-1009-mutually-referential-types-and-modules-single-scope.md)