---
title: 'Boucles : expression for...to (F#)'
description: Voir comment le F# for.. à l’expression est utilisé pour effectuer une itération dans une boucle sur une plage de valeurs d’une variable de boucle.
ms.date: 05/16/2016
ms.openlocfilehash: 8160fd30c4f3afe8bb6b58f468802ef1c0ef32ee
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "43800467"
---
# <a name="loops-forto-expression"></a>Boucles : expression for...to

Le `for...to` expression est utilisée pour effectuer une itération dans une boucle sur une plage de valeurs d’une variable de boucle.

## <a name="syntax"></a>Syntaxe

```fsharp
for identifier = start [ to | downto ] finish do
    body-expression
```

## <a name="remarks"></a>Notes

Le type de l’identificateur est déduit du type de la *Démarrer* et *Terminer* expressions. Types de ces expressions doivent être des entiers 32 bits.

Bien que techniquement une expression, `for...to` s’apparente à une instruction traditionnelle dans un langage de programmation impérative. Le type de retour pour la *expression de corps* doit être `unit`. Les exemples suivants montrent différentes utilisations de la `for...to` expression.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5101.fs)]

La sortie du code précédent est la suivante.

```
1 2 3 4 5 6 7 8 9 10
10 9 8 7 6 5 4 3 2 1
2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18
```

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Boucles : expression `for...in`](loops-for-in-expression.md)
- [Boucles : expression `while...do`](loops-while-do-expression.md)
