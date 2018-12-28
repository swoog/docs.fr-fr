---
title: Fonctions inline
description: Découvrez comment utiliser F# les fonctions inline sont intégrées directement dans le code appelant.
ms.date: 05/16/2016
ms.openlocfilehash: 12c175e3e46e12d978fe02d3e1fe83142e71a25d
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53610565"
---
# <a name="inline-functions"></a>Fonctions inline

*Les fonctions inline* sont des fonctions qui sont intégrées directement dans le code appelant.

## <a name="using-inline-functions"></a>À l’aide de fonctions Inline

Lorsque vous utilisez des paramètres de type statique, toutes les fonctions qui sont paramétrées par les paramètres de type doivent être inline. Cela garantit que le compilateur peut résoudre ces paramètres de type. Lorsque vous utilisez des paramètres de type générique ordinaire, il n’existe aucune restriction de ce type.

Permettent l’utilisation de contraintes de membre, les fonctions inline peuvent être utiles pour optimiser le code. Toutefois, utilisation abusive des fonctions inline peut rendre votre code moins résistant aux modifications dans les optimisations du compilateur et l’implémentation de fonctions de bibliothèque. Pour cette raison, évitez d’utiliser des fonctions inline pour l’optimisation, sauf si vous avez essayé toutes les autres techniques d’optimisation. Rendre une fonction ou méthode inline peut parfois améliorer les performances, mais qui n’est pas toujours le cas. Par conséquent, vous devez également utiliser les mesures de performances pour vérifier que la fabrication d’une fonction donnée inline n’a en fait un effet positif.

Le `inline` modificateur peut être appliqué aux fonctions au niveau supérieur, au niveau du module ou au niveau de la méthode dans une classe.

L’exemple de code suivant illustre une fonction inline au niveau supérieur, une méthode d’instance inline et une méthode statique inline.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-3/snippet201.fs)]

## <a name="inline-functions-and-type-inference"></a>Les fonctions inline et inférence de Type

La présence de `inline` affecte l’inférence de type. Il s’agit, car les fonctions inline peuvent avoir résolus statiquement des paramètres de type, tandis que les fonctions non inline ne peut pas. L’exemple de code suivant illustre un cas où `inline` est utile, car vous utilisez une fonction qui a un paramètre de type résolus statiquement, le `float` opérateur de conversion.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-3/snippet202.fs)]

Sans le `inline` modificateur, l’inférence de type force la fonction à prendre un type spécifique, dans ce cas `int`. Mais avec la `inline` modificateur, la fonction est également déduit pour avoir un paramètre de type résolus statiquement. Avec le `inline` modificateur, le type déduit est ce qui suit :

```fsharp
^a -> unit when ^a : (static member op_Explicit : ^a -> float)
```

Cela signifie que la fonction accepte n’importe quel type qui prend en charge une conversion vers **float**.

## <a name="see-also"></a>Voir aussi

- [Fonctions](index.md)
- [Contraintes](../generics/constraints.md)
- [Paramètres de type résolus statiquement](../generics/statically-resolved-type-parameters.md)