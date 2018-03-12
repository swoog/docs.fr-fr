---
title: "Expressions conditionnelles : if... then...else (F#)"
description: "Découvrez comment écrire des expressions conditionnelles en F # pour exécuter les différentes branches de code."
keywords: visual f#, f#, programmation fonctionnelle
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 16e1871c-4d4d-4691-9ab2-bd2c6f65589a
ms.openlocfilehash: 5823e46cd13053fcd31f94f2d79d1f7470ca5118
ms.sourcegitcommit: d3cfda0943364aaf6ccd574f55f584576c8a4fee
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2018
---
# <a name="conditional-expressions-ifthenelse"></a>Expressions conditionnelles : `if...then...else`

Le `if...then...else` expression exécute différentes branches de code et prend une valeur différente selon l’expression booléenne donnée.


## <a name="syntax"></a>Syntaxe

```fsharp
if boolean-expression then expression1 [ else expression2 ]
```

## <a name="remarks"></a>Notes
Dans la syntaxe précédente, *expression1* s’exécute lorsque l’expression booléenne renvoie `true`; sinon, *expression2* s’exécute.

Contrairement à d’autres langages, les `if...then...else` construction est une expression, pas une instruction. Cela signifie qu’il génère une valeur, ce qui est la valeur de la dernière expression dans la branche qui s’exécute. Les types des valeurs produites dans chaque branche doivent correspondre. S’il existe n’explicite `else` , son type est `unit`. Par conséquent, si le type de la `then` branche est d’un type autre que `unit`, il doit y avoir un `else` branche avec le même type de retour. Lors du chaînage `if...then...else` expressions ensemble, vous pouvez utiliser le mot clé `elif` au lieu de `else if`; ils sont équivalents.

## <a name="example"></a>Exemple
L’exemple suivant illustre comment utiliser le `if...then...else` expression.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4501.fs)]

```
10 is less than 20
What is your name? John
How old are you? 9
You are only 9 years old and already learning F#? Wow!
```

## <a name="see-also"></a>Voir aussi
[Informations de référence du langage F#](index.md)

