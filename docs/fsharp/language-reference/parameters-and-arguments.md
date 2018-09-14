---
title: Paramètres et arguments (F#)
description: 'En savoir plus sur F # prise en charge linguistique pour la définition de paramètres et en transmettant des arguments aux fonctions, méthodes et propriétés.'
ms.date: 05/16/2016
ms.openlocfilehash: a1e2a70ca560bbb09d2cd10f47485cbe5c5e029d
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2018
ms.locfileid: "45591657"
---
# <a name="parameters-and-arguments"></a>Paramètres et arguments

Cette rubrique décrit la prise en charge de langage de définition de paramètres et en transmettant des arguments aux fonctions, méthodes et propriétés. Il inclut des informations sur le passage par référence et comment définir et utiliser des méthodes qui peuvent prendre un nombre variable d’arguments.

## <a name="parameters-and-arguments"></a>Paramètres et arguments

Le terme *paramètre* est utilisé pour décrire les noms des valeurs qui sont censées être fournies. Le terme *argument* est utilisé pour les valeurs fournies pour chaque paramètre.

Paramètres peuvent être spécifiés sous forme de tuple ou curryfiés ou dans une combinaison des deux. Vous pouvez passer des arguments à l’aide d’un nom de paramètre explicite. Les paramètres des méthodes peuvent être spécifiés comme étant facultatifs et une valeur par défaut.

## <a name="parameter-patterns"></a>Modèles de paramètre

En règle générale, les paramètres fournis à des fonctions et méthodes sont des modèles en les séparant par des espaces. Cela signifie que, en principe, les modèles décrits dans [Expressions de correspondance](match-expressions.md) peut être utilisé dans une liste de paramètres pour une fonction ou un membre.

Méthodes utilisent généralement la forme de tuple de passage d’arguments. Cela permet d’obtenir un résultat plus clair à partir de la perspective d’autres langages .NET, car la forme de tuple correspond à la façon d’arguments sont passés dans les méthodes .NET.

La forme curryfiée est souvent utilisée avec des fonctions créées à l’aide de `let` liaisons.

Le pseudo-code suivant montre des exemples de tuple et d’arguments curryfiés.

```fsharp
// Tuple form.
member this.SomeMethod(param1, param2) = ...
// Curried form.
let function1 param1 param2 = ...
```

Combiner les formes sont possibles lorsque certains arguments sont dans des tuples et d’autres pas.

```fsharp
let function2 param1 (param2a, param2b) param3 = ...
```

Autres modèles peuvent également servir dans les listes de paramètres, mais si le modèle de paramètre ne correspond pas à toutes les entrées possibles, il peut y avoir une correspondance incomplète en cours d’exécution. L’exception `MatchFailureException` est générée lorsque la valeur d’un argument ne correspond pas aux modèles spécifiés dans la liste de paramètres. Le compilateur émet un avertissement lorsqu’un modèle de paramètre accepte des correspondances incomplètes. Au moins un autre modèle est souvent utile pour les listes de paramètres, et c’est le modèle de caractère générique. Vous utilisez le modèle de caractère générique dans une liste de paramètres lorsque vous souhaitez simplement ignorer tous les arguments sont fournis. Le code suivant illustre l’utilisation du modèle de caractère générique dans une liste d’arguments.

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3801.fs)]

Le modèle de caractère générique peut être utile chaque fois que vous n’avez pas besoin des arguments transmis, comme illustré dans le point d’entrée principal pour un programme, lorsque vous n’êtes pas intéressé par les arguments de ligne de commande qui sont normalement fournis en tant que tableau de chaînes, comme dans le code suivant.

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3802.fs)]

Autres modèles qui sont parfois utilisés dans les arguments sont les `as` modèle et les modèles d’identificateur associés aux unions discriminées et modèles actifs. Vous pouvez utiliser le modèle d’union discriminée cas unique comme suit.

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3803.fs)]

La sortie est la suivante.

```
Data begins at 0 and ends at 4 in string Et tu, Brute?
Et tu
```

Modèles actifs peuvent être utiles en tant que paramètres, par exemple, lors de la transformation d’un argument dans un format de votre choix, comme dans l’exemple suivant :

```fsharp
type Point = { x : float; y : float }

let (| Polar |) { x = x; y = y} =
    ( sqrt (x*x + y*y), System.Math.Atan (y/ x) )

let radius (Polar(r, _)) = r
let angle (Polar(_, theta)) = theta
```

Vous pouvez utiliser la `as` modèle pour stocker une valeur mise en correspondance comme une valeur locale, comme indiqué dans la ligne de code suivante.

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3805.fs)]

Un autre modèle qui est parfois utilisé est une fonction qui laisse le dernier argument sans nom en fournissant, en tant que le corps de la fonction, une expression lambda qui exécute immédiatement une correspondance de modèle sur l’argument implicite. Un exemple de ceci est la ligne de code suivante.

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3804.fs)]

Ce code définit une fonction qui prend une liste générique et retourne `true` si la liste est vide, et `false` dans le cas contraire. L’utilisation de telles techniques peut rendre le code plus difficile à lire.

Parfois, les modèles qui impliquent des correspondances incomplètes sont utiles, par exemple, si vous savez que les listes dans votre programme uniquement trois éléments, vous pouvez utiliser un modèle semblable à la suivante dans une liste de paramètres.

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3806.fs)]

L’utilisation de modèles avec des correspondances incomplètes doit être réservée aux prototypage rapide et d’autres utilisations temporaires. Le compilateur émet un avertissement pour ce code. Ces modèles ne peuvent pas couvrir le cas général de toutes les entrées possibles et par conséquent ne conviennent pas pour les API de composant.

## <a name="named-arguments"></a>Arguments nommés

Les arguments de méthodes peuvent être spécifiés par position dans une liste d’arguments séparés par des virgules, ou passés explicitement à une méthode en fournissant le nom, suivi par un signe égal et la valeur à passer dans. S’il est spécifié en fournissant le nom, ils peuvent apparaître dans un ordre différent de celui utilisé dans la déclaration.

Arguments nommés peuvent rendre code plus lisible et plus adaptable à certains types de modifications dans l’API, telles que la réorganisation des paramètres de méthode.

Arguments nommés sont autorisés uniquement pour les méthodes, pas pour `let`-lié des fonctions, des valeurs de fonction ou des expressions lambda.

L’exemple de code suivant illustre l’utilisation d’arguments nommés.

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3807.fs)]

Dans un appel à un constructeur de classe, vous pouvez définir les valeurs des propriétés de la classe à l’aide d’une syntaxe similaire à celle des arguments nommés. L’exemple suivant illustre cette syntaxe.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet3506.fs)]

Pour plus d’informations, consultez [constructeurs (F #)](https://msdn.microsoft.com/library/2cd0ed07-d214-4125-8317-4f288af99f05).

## <a name="optional-parameters"></a>Paramètres facultatifs

Vous pouvez spécifier un paramètre facultatif pour une méthode à l’aide d’un point d’interrogation devant le nom du paramètre. Paramètres facultatifs sont interprétés comme le type d’option F #, vous pouvez les interroger de façon habituelle que les types d’option sont interrogées, à l’aide un `match` expression avec `Some` et `None`. Paramètres facultatifs sont autorisés uniquement sur les membres, et non sur les fonctions créées à l’aide de `let` liaisons.

Vous pouvez également utiliser une fonction `defaultArg`, qui définit une valeur par défaut d’un argument facultatif. Le `defaultArg` fonction prend le paramètre facultatif comme premier argument et la valeur par défaut en tant que la seconde.

L’exemple suivant illustre l’utilisation de paramètres facultatifs.

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3808.fs)]

La sortie est la suivante.

```
Baud Rate: 9600 Duplex: Full Parity: false
Baud Rate: 4800 Duplex: Half Parity: false
Baud Rate: 300 Duplex: Half Parity: true
```

## <a name="passing-by-reference"></a>Passage par référence

Passage d’une valeur de F # par référence implique [ByRef](byrefs.md), qui sont des types de pointeur managé. Conseils pour le type à utiliser sont la suivante :

* Utilisez `inref<'T>` si vous avez besoin uniquement de lire le pointeur.
* Utilisez `outref<'T>` si vous avez besoin uniquement d’écrire dans le pointeur.
* Utilisez `byref<'T>` si vous avez besoin à la fois lire et écrire dans le pointeur.

```fsharp
let example1 (x: inref<int>) = printfn "It's %d" x

let example2 (x: outref<int>) = x <- x + 1

let example3 (x: byref<int>) =
    printfn "It'd %d" x
    x <- x + 1

// No need to make it mutable, since it's read-only
let x = 1
example1 &x

// Needs to be mutable, since we write to it
let mutable y = 2
example2 &y
example3 &y // Now 'y' is 3
```

Étant donné que le paramètre est un pointeur et la valeur est mutable, les modifications apportées à la valeur sont conservées après l’exécution de la fonction.

Vous pouvez utiliser un tuple comme valeur de retour pour stocker les `out` paramètres dans les méthodes de la bibliothèque .NET. Vous pouvez également traiter les `out` paramètre comme un `byref` paramètre. L’exemple de code suivant illustre les deux sens.

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3810.fs)]

## <a name="parameter-arrays"></a>Tableaux de paramètres

Parfois, il est nécessaire de définir une fonction qui accepte un nombre arbitraire de paramètres de type hétérogène. Il ne serait pas pratique de créer toutes les méthodes surchargées possibles pour prendre en compte pour tous les types qui peuvent être utilisées. Les implémentations de .NET prennent en charge ces méthodes via la fonctionnalité de tableau de paramètre. Une méthode qui prend un tableau de paramètres dans sa signature peut être fournie avec un nombre arbitraire de paramètres. Les paramètres sont placés dans un tableau. Le type des éléments du tableau détermine les types de paramètres qui peuvent être passés à la fonction. Si vous définissez le tableau de paramètres avec `System.Object` en tant que le type d’élément, puis le code client peut passer des valeurs de n’importe quel type.

En F #, les tableaux de paramètres peuvent uniquement être définies dans les méthodes. Ils ne peuvent pas être utilisés dans des fonctions autonomes ou des fonctions qui sont définies dans les modules.

Vous définissez un tableau de paramètres à l’aide de la `ParamArray` attribut. Le `ParamArray` attribut peut uniquement être appliqué au dernier paramètre.

Le code suivant illustre l’appel à une méthode .NET qui prend un tableau de paramètres et la définition d’un type en F # qui a une méthode qui prend un tableau de paramètres.

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-2/snippet3811.fs)]

Lorsque vous exécutez dans un projet, la sortie du code précédent est comme suit :

```console
a 1 10 Hello world 1 True
"a"
1
10.0
"Hello world"
1u
true
```

## <a name="see-also"></a>Voir aussi

- [Membres](members/index.md)
