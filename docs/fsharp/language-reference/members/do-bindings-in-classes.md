---
title: Liaisons do dans les classes
description: Découvrez comment utiliser un F# 'do' liaison dans une définition de classe, qui effectue des actions lorsque l’objet est construit ou lorsque le type est tout d’abord utilisé.
ms.date: 05/16/2016
ms.openlocfilehash: c924c882974989436d8ea404ebee0a7ef3c54fd3
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65641797"
---
# <a name="do-bindings-in-classes"></a>Liaisons do dans les classes

Un `do` liaison dans une définition de classe effectue des actions lorsque l’objet est construit ou, pour une analyse statique `do` liaison, lorsque le type est tout d’abord utilisé.

## <a name="syntax"></a>Syntaxe

```fsharp
[static] do expression
```

## <a name="remarks"></a>Notes

Un `do` liaison apparaît avec ou après `let` liaisons mais avant les définitions de membre dans une définition de classe. Bien que le `do` mot clé est facultatif pour `do` liaisons au niveau du module, il n’est pas facultatif pour `do` liaisons dans une définition de classe.

Pour la construction de chaque objet d’un type donné, non statique `do` liaisons et non statiques `let` sont exécutées dans l’ordre dans lequel ils apparaissent dans la définition de classe. Plusieurs `do` liaisons peuvent se produire dans un type. Le non-static `let` liaisons et non statiques `do` deviennent le corps du constructeur principal. Le code dans le non-static `do` section des liaisons peut référencer les paramètres du constructeur principal et des valeurs ou des fonctions qui sont définies dans le `let` section des liaisons.

Non statiques `do` liaisons peuvent accéder aux membres de la classe tant que la classe a un auto-identificateur défini par un `as` mot clé dans la classe de titre et tant que toutes les utilisations de ces membres sont qualifiées avec l’auto-identificateur pour la classe.

Étant donné que `let` liaisons initialisent les champs privés d’une classe, ce qui est souvent nécessaire pour garantir que les membres se comportent comme prévu, `do` liaisons sont généralement placées après `let` liaisons afin que le code dans le `do` peut de liaison exécuter avec un objet entièrement initialisé. Si votre code tente d’utiliser un membre avant l’initialisation est terminée, une exception InvalidOperationException est déclenchée.

Statique `do` liaisons peuvent référencer des membres statiques ou champs de la classe, mais pas de membres ou des champs de l’instance. Statique `do` liaisons deviennent partie intégrante de l’initialiseur statique pour la classe, qui est toujours exécuté avant la première utilisation de la classe.

Les attributs sont ignorés pour `do` liaisons dans les types. Si un attribut n’est requis pour le code qui s’exécute dans un `do` de liaison, elle doit s’appliquer au constructeur principal.

Dans le code suivant, une classe a statique `do` liaison et non statiques `do` liaison. L’objet a un constructeur qui possède deux paramètres, `a` et `b`, et deux champs privés sont définis dans le `let` liaisons pour la classe. Deux propriétés sont également définies. Tous ces éléments sont dans la portée de la non statique `do` section des liaisons, comme cela est illustré par la ligne qui imprime toutes ces valeurs.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3101.fs)]

La sortie est la suivante.

```console
Initializing MyType.
Initializing object 1 2 2 4 8 16
```

## <a name="see-also"></a>Voir aussi

- [Membres](index.md)
- [Classes](../classes.md)
- [Constructeurs](constructors.md)
- [Liaisons `let` dans des classes](let-bindings-in-classes.md)
- [`do` liaisons](../functions/do-Bindings.md)
