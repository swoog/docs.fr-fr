---
title: 'Boucles : expression for...to'
description: Voir comment la F# for.. à l’expression est utilisé pour effectuer une itération dans une boucle sur une plage de valeurs d’une variable de boucle.
ms.date: 05/16/2016
ms.openlocfilehash: 5b7bb9bac659ddf1d457be1ce17e90a2593666de
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65645247"
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
- [Boucles : `for...in` Expression](loops-for-in-expression.md)
- [Boucles : `while...do` Expression](loops-while-do-expression.md)
