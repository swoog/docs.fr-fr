---
title: 'Boucles : expression for...in'
description: Voir comment la F# for.. dans l’expression de construction en boucle est utilisée pour itérer sur les correspondances d’un modèle dans une collection énumérable.
ms.date: 05/16/2016
ms.openlocfilehash: 5346713b1747227f3fe79e308455d976e506f968
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65641805"
---
# <a name="loops-forin-expression"></a>Boucles : expression for...in

Cette construction en boucle est utilisée pour itérer sur les correspondances d’un modèle dans une collection énumérable comme une expression de plage, séquence, liste, tableau ou autre construction qui prend en charge l’énumération.

## <a name="syntax"></a>Syntaxe

```fsharp
for pattern in enumerable-expression do
    body-expression
```

## <a name="remarks"></a>Notes

Le `for...in` expression peut être comparée à la `for each` instruction dans d’autres langages .NET, car il est utilisé pour effectuer une boucle sur les valeurs dans une collection énumérable. Toutefois, `for...in` prend également en charge les critères spéciaux à la collection au lieu de simplement itération sur la collection entière.

L’expression énumérable peut être spécifiée en tant que collection énumérable ou, à l’aide de la `..` opérateur, sous forme de plage sur un type intégral. Collections énumérables incluent des listes, séquences, tableaux, jeux, mappages et ainsi de suite. Tout type qui implémente `System.Collections.IEnumerable` peut être utilisé.

Lorsque vous exprimer une plage en utilisant le `..` opérateur, vous pouvez utiliser la syntaxe suivante.

*Démarrer* ... *finish*

Vous pouvez également utiliser une version qui inclut un incrément appelé le *ignorer*, comme dans le code suivant.

*Démarrer* ... *skip* .. *finish*

Lorsque vous utilisez des plages intégrales et une variable de compteur simple comme modèle, le comportement standard consiste à incrémenter la variable de compteur de 1 à chaque itération, mais si la plage inclut une valeur de l’ignorer, le compteur est incrémenté par la valeur Ignorer à la place.

Valeurs correspondantes dans le modèle peuvent également être utilisées dans l’expression de corps.

Les exemples de code suivants illustrent l’utilisation de la `for...in` expression.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5201.fs)]

La sortie est la suivante.

```
1
5
100
450
788
```

L’exemple suivant montre comment effectuer une boucle sur une séquence et comment utiliser un modèle de tuple au lieu d’une variable simple.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5202.fs)]

La sortie est la suivante.

```
1 squared is 1
2 squared is 4
3 squared is 9
4 squared is 16
5 squared is 25
6 squared is 36
7 squared is 49
8 squared is 64
9 squared is 81
10 squared is 100
```

L’exemple suivant montre comment effectuer une boucle sur une plage d’entiers simple.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5203.fs)]

La sortie de function1 est comme suit.

```
1 2 3 4 5 6 7 8 9 10
```

L’exemple suivant montre comment effectuer une boucle sur une plage avec un saut de 2, qui inclut tous les autres éléments de la plage.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5204.fs)]

La sortie de `function2` se présente comme suit.

```
1 3 5 7 9
```

L’exemple suivant montre comment utiliser une plage de caractères.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5205.fs)]

La sortie de `function3` se présente comme suit.

```
a b c d e f g h i j k l m n o p q r s t u v w x y z
```

L’exemple suivant montre comment utiliser une valeur négative skip pour une itération inverse.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5208.fs)]

La sortie de `function4` se présente comme suit.

```
10 9 8 7 6 5 4 3 2 1 ... Lift off!
```

Le début et la fin de la plage peuvent également être des expressions, telles que des fonctions, comme dans le code suivant.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5206.fs)]

La sortie de `function5` avec cette entrée est la suivante.

```
2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18
```

L’exemple suivant illustre l’utilisation d’un caractère générique (\_) lorsque l’élément n’est pas nécessaire dans la boucle.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5207.fs)]

La sortie est la suivante.

```
Number of elements in list1: 5
```

`Note` Vous pouvez utiliser `for...in` dans les expressions de séquence et autres expressions de calcul, auquel cas une version personnalisée de la `for...in` expression est utilisée. Pour plus d’informations, consultez [séquences](sequences.md), [flux de travail asynchrones](asynchronous-workflows.md), et [Expressions de calcul](computation-expressions.md).

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Boucles : `for...to` Expression](loops-for-to-expression.md)
- [Boucles : `while...do` Expression](loops-while-do-expression.md)
