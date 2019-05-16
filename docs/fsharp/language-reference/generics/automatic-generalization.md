---
title: Généralisation automatique
description: Découvrez comment F# généralise automatiquement les arguments et les types de fonctions afin qu’ils fonctionnent avec plusieurs types lorsque cela est possible.
ms.date: 05/16/2016
ms.openlocfilehash: 8fc61b5e0c227474a5e913b37f4c0dad9b235a6f
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65641869"
---
# <a name="automatic-generalization"></a>Généralisation automatique

F#utilise l’inférence pour évaluer les types de fonctions et expressions de type. Cette rubrique décrit comment F# généralise automatiquement les arguments et les types de fonctions afin qu’ils fonctionnent avec plusieurs types lorsque cela est possible.

## <a name="automatic-generalization"></a>Généralisation automatique

Le F# compilateur, lorsqu’il effectue l’inférence de type sur une fonction, détermine si un paramètre donné peut être générique. Le compilateur examine chaque paramètre et détermine si la fonction a une dépendance sur le type spécifique de ce paramètre. Si elle n’est pas le cas, le type est déduit de manière générique.

L’exemple de code suivant illustre une fonction que le compilateur déduit pour être générique.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-3/snippet101.fs)]

Le type est déduit pour être `'a -> 'a -> 'a`.

Le type indique qu’il s’agit d’une fonction qui accepte deux arguments du même type inconnu et retourne une valeur de ce même type. Une des raisons qui la fonction précédente peut être générique est que le plus grand-que l’opérateur (`>`) lui-même est générique. Le plus grand-que l’opérateur a la signature `'a -> 'a -> bool`. Tous les opérateurs ne sont génériques, et si le code dans une fonction utilise un type de paramètre avec une fonction non générique ou un opérateur, ce type de paramètre ne peut pas être généralisé.

Étant donné que `max` est générique, il peut être utilisé avec types tels que `int`, `float`, et ainsi de suite, comme indiqué dans les exemples suivants.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-3/snippet102.fs)]

Toutefois, les deux arguments doivent être du même type. La signature est `'a -> 'a -> 'a`, et non `'a -> 'b -> 'a`. Par conséquent, le code suivant génère une erreur car les types ne correspondent pas.

```fsharp
// Error: type mismatch.
let biggestIntFloat = max 2.0 3
```

Le `max` fonction fonctionne également avec tout type qui prend en charge la plus grande-que l’opérateur. Par conséquent, vous pouvez également l’utiliser sur une chaîne, comme indiqué dans le code suivant.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-3/snippet104.fs)]

## <a name="value-restriction"></a>Restriction de valeur

Le compilateur exécute la généralisation automatique uniquement sur les définitions de fonction complètes qui ont des arguments explicites et sur des valeurs immuables simples.

Cela signifie que le compilateur émet une erreur si vous essayez de compiler le code qui n’est pas suffisamment contraint à être un type spécifique, mais est également pas généralisable. Pour résoudre ce problème, le message d’erreur fait référence à cette restriction sur la généralisation automatique pour les valeurs en tant que le *restriction de valeur*.

En règle générale, l’erreur de restriction de valeur se produit lorsqu’une construction de manière générique, mais le compilateur comprend des informations insuffisantes pour la généraliser, ou lorsque vous omettez involontairement des informations de type suffisantes dans une construction non générique. La solution à l’erreur de restriction de valeur consiste à fournir des informations plus explicites pour contraindre plus en détail le problème de l’inférence de type, dans une des manières suivantes :

- Contraindre un type à être générique en ajoutant une annotation de type explicite à une valeur ou un paramètre.

- Si le problème utilise une construction non généralisable pour définir une fonction générique, par exemple une composition de fonction ou incomplète des arguments de fonction curryfiée appliqués, essayez de réécrire la fonction comme une définition de fonction ordinaire.

- Si le problème est une expression qui est trop complexe pour être généralisée, rendre une fonction en ajoutant un paramètre supplémentaire inutilisé.

- Ajouter des paramètres de type générique explicites. Cette option est rarement utilisée.

- Les exemples de code suivants illustrent chacun de ces scénarios.

Cas 1 : Expression trop complexe. Dans cet exemple, la liste `counter` est destinée à être `int option ref`, mais il n’est pas défini comme une valeur immuable simple.

```fsharp
let counter = ref None
// Adding a type annotation fixes the problem:
let counter : int option ref = ref None
```

Cas 2 : À l’aide d’une construction non généralisable pour définir une fonction générique. Dans cet exemple, la construction est non généralisable, car il implique l’application partielle d’arguments de fonction.

```fsharp
let maxhash = max << hash
// The following is acceptable because the argument for maxhash is explicit:
let maxhash obj = (max << hash) obj
```

Cas 3 : Ajout d’un paramètre supplémentaire inutilisé. Étant donné que cette expression n’est pas assez simple pour la généralisation, le compilateur émet l’erreur de restriction de valeur.

```fsharp
let emptyList10 = Array.create 10 []
// Adding an extra (unused) parameter makes it a function, which is generalizable.
let emptyList10 () = Array.create 10 []
```

Cas 4 : Ajout de paramètres de type.

```fsharp
let arrayOf10Lists = Array.create 10 []
// Adding a type parameter and type annotation lets you write a generic value.
let arrayOf10Lists<'T> = Array.create 10 ([]:'T list)
```

Dans le dernier cas, la valeur devient une fonction de type, qui peut être utilisée pour créer des valeurs de nombreux types différents, par exemple comme suit :

```fsharp
let intLists = arrayOf10Lists<int>
let floatLists = arrayOf10Lists<float>
```

## <a name="see-also"></a>Voir aussi

- [Inférence de type](../type-inference.md)
- [Génériques](index.md)
- [Paramètres de type résolus statiquement](statically-resolved-type-parameters.md)
- [Contraintes](constraints.md)
